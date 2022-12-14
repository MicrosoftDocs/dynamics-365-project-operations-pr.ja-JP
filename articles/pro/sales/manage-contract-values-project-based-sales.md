---
title: プロジェクト契約品目の概要
description: この記事では、Project Operations でのプロジェクト契約品目の操作に関する情報を提供します。
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824632"
---
# <a name="project-contract-lines-overview"></a>プロジェクト契約品目の概要

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations のプロジェクトベースの契約品目は、エンゲージメントに関するプロジェクト作業の特定のコンポーネントの見積もりおよび請求契約を保持するように設計されています。 プロジェクトベースの契約品目の構造は、次の概念によりプロジェクト見積および請求シナリオに対して拡張されます。

- 請求方法
- プロジェクトとタスクのスケジュール
- 含まれるトランザクションのクラス
- 上限
- 請求可否の設定
- 契約品目の詳細を使用した見積もり
- 契約品目の顧客

以下の表には、プロジェクトベースの契約品目の **全般** タブのフィールドが含まれており、プロジェクトベースの作業で使用する詳細なゼロからの見積もりと請求の取り決めの基礎を設定するのに役立ちます。

| フィールド | 内容 | 下位への影響 |
| --- | --- | --- |
| **名前** | 契約品目の名前です。 見積もられている契約の個別のコンポーネントを識別します。 見積から作成されたプロジェクト契約書の場合、この値はプロジェクトベースの見積明細行の対応する値からコピーされます。 | 請求書作成時にこの契約品目から作成されるプロジェクトの請求書行にコピーされた名前です。 |
| **請求方法** | 見積から作成されたプロジェクト契約書では、この値は見積明細行の対応するフィールドからコピーされます。 これはオプション セットであり、Project Operations で対応している 2 つの主要な契約モデルを表しています :</br>- **固定価格**</br>- **時間と材料** | 参照した契約品目の課金方法に基づいて、実際のトランザクションが処理されます。 実績で参照された契約品目に時間と材料に基づく課金方式がある場合は、原価と未請求の売上実績レコードが作成されます。 実質が参照している契約品目に固定の課金方式がある場合は、原価実質のみを作成します。 |
| **Project** | このフィールドを使用して、このエンゲージメントの作業の提供に使用されるプロジェクトを特定します。 | この値は、**含まれるタスク** そして **含まれるトランザクション クラス** と併用して、実績または見積もり行レコードで契約品目参照を解決します。 |
| **含まれるタスク** | この契約品目に、選択したプロジェクトのすべてのプロジェクト タスクが含まれるのか、タスクのサブセットのみが含まれるのかを示します。 これは、次の値を持つオプション セットです :</br>- **すべてのプロジェクト タスク**</br>- **選択したプロジェクト タスクのみ**。 このフィールドの空白の値は、**すべてのプロジェクトタスク** 選択することと同じとなります。 | **選択されたタスクのみ** が選択されている場合、特定のタスクを選択して、**プロジェクト** ページの **タスク請求設定** タブでこの契約ラインに関連付けることができます。 この値は、実際の品目レコードまたは見積品目レコードの契約品目参照を解決する目的で、**プロジェクト** クラスおよび **含まれるトランザクション** クラスと組み合わせて使用されます。 |
| **時間を含む** | **はい**/**いいえ** の値は、選択したプロジェクトの時間トランザクションまたは労務費がこの契約行に含まれるかどうかを示します。 値が **いいえ** となっている場合は、時間トランザクションまたは人件費がこの契約品目に含まれないことを示します。 値が **はい** の場合は、含まれることを示します。 | この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。 |
| **経費を含む** | **はい**/**いいえ** の値は、選択したプロジェクトの経費原価がこの契約行に含まれるかどうかを示します。 値が **いいえ** となっている場合は、この契約品目には経費として計上されません。 値が **はい** の場合は、計上されることを示します。 | この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。 |
| **材料を含む** | **はい**/**いいえ** の値は、選択したプロジェクトの材料原価がこの契約行に含まれるかどうかを示します。 **いいえ** の値は、選択したプロジェクトの材料原価がこの契約行に含まれないことを示します。 値が **はい** の場合は、計上されることを示します。 | この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。 |
| **料金を含む** | **はい**/**いいえ** の値は、選択したプロジェクトの手数料がこの契約行に含まれるかどうかを示します。 値が **いいえ** となっている場合は、この契約品目には料金として計上されません。 値が **はい** の場合は、含まれることを示します。 | この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。 |
| **契約金額** | 固定価格の契約品目では、この金額は、この契約品目に関連するすべての作業コンポーネントについて顧客に請求される合意された値です。 時間と材料の契約品目では、この金額は、この契約品目に関連するすべての作業コンポーネントについて顧客に請求されるものの推定値です。 見積から作成されたプロジェクト契約書では、この値は見積明細行の対応するフィールドからコピーされます。 プロジェクトベースの契約品目に明細行がある場合、このフィールドは編集用にロックされ、契約行の明細の金額から集計されます。 | 契約品目に明細行がある場合、この値は明細の金額を変更することで、この値を変更することができます。 固定価格の契約品目では、この値を利用して定期的な請求マイルストーンの税引前金額を生成します。 |
| **予測税額** | ユーザーはこのフィールドを編集して、契約品目に推定税額を入力できます。 プロジェクトベースの契約品目に明細行がある場合、このフィールドは編集用にロックされ、契約行の明細の税額から集計されます。 | 契約品目に明細行がある場合、この値は明細の金額を変更することで、この税額を変更することができます。 固定価格契約品目では、この値は定期的な請求マイルストーンに対する税額を生成するために使用されます。 |
| **税引き後の契約金額** | 税引き後の契約品目です。 このフィールドは読み取り専用であり、**契約金額+税金** として計算されます。 | 固定価格の契約品目では、この値は定期的な課金のマイルストーンを生成する目的で使用されます。 |
| **上限** | ユーザーはこのフィールドを編集することができ、請求方法が時間と材料に設定されているプロジェクト ベースの契約品目でのみ利用可能です。 | ユーザーはこのフィールドを編集できます。 時間および材料の実績がこの時間および材料の契約品目を参照している場合、実績の金額は契約品目の超過しない限度額と比較して評価されます。 この評価は、既に支出された金額とコミットされた金額を処理した後に完了します。 |
| **顧客の予算** | このフィールドは編集可能であり、契約が見積書から作成された場合、見積書の明細の対応するフィールドからコピーされます。 | このフィールドは情報としてのみ使用され、、ダウンストリームへの影響はありません。 |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>プロジェクト ベースの契約品目の全般タブのオプションで使用する検証ルール

ルール 1 : **含まれるタスク** フィールドが空白であるか、**すべてのプロジェクトタスク** に設定されている場合、プロジェクトのすべてのタスクは契約品目に含まれます。

ルール 2 : **含まれるタスク** フィールドが空白であるか、**すべてのプロジェクト タスク** に明示的にに設定されている場合、プロジェクトと特定のトランザクション クラスは、プロジェクトベースの契約の 1 つの契約品目にのみ含めることができます。

ルール 3 : **含まれるタスク** フィールドが空白であるか、**選択されたプロジェクト タスクのみ** に明示的にに設定されている場合、プロジェクトと特定のトランザクション クラスは、契約の複数のプロジェクト ベースの契約品目に含めることができます。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>契約書</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>契約品目</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>含まれるタスク</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>時間を含む</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>経費を含む</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>材料を含む</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>参照項目</strong>
                </p>
                <p>
                    <strong>料金</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>有効/無効</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>理由</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
ルール #2 に違反。 P1 プロジェクトの時間、経費、材料、および手数料は、契約行 CL1 と CL2 の両方に含まれています。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
無効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
ルール #2 に違反。 P1 プロジェクトの時間、材料、および手数料は、契約行 CL1 と CL2 の両方に含まれています。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
無効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1 プロジェクトの時間、材料、および手数料は CL1 に含まれています。
                </p>
                <ul>
                    <li>
P1 プロジェクトの経費は CL2 に含まれています。
                    </li>
                </ul>
                <p>
各契約行に含まれているものに重複がないため、有効です。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
無効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
無効 </p>
            </td>
            <td width="42" valign="top">
                <p>
無効 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
ルール #2 に違反 </p>
                <p>
C1 には、プロジェクト P1 のタスクのサブセットに関する時間、材料、経費、および手数料が含まれています。
                </p>
                <p>
CL2 には、プロジェクト P1 全体の時間、材料、経費、および手数料が含まれているため、C1 に含まれているものと重複しています。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
ルール #3 による </p>
                <p>
C1 には、プロジェクト P1 のタスクのサブセットに関する時間、手数料、材料、経費、および手数料が含まれています。
                </p>
                <p>
CL2 には、プロジェクト P1 のタスクのサブセットに対する時間、手数料、材料、経費、および手数料が含まれています。
                </p>
                <p>
唯一の追加の検証は、CL1 のタスクのサブセットが、CL2 のタスクのサブセットとは異なり、重複がないことを確認することです。 これは、タスクが関連付けられたときにシステムによって実行されます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="48" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
            <td width="42" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
