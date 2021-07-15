---
title: プロジェクトベースの見積依頼明細行の概要
description: このトピックは、プロジェクト作業のプロジェクトベースの見積依頼明細行の使用に関する情報を提供します。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369877"
---
# <a name="project-based-quote-lines-overview"></a>プロジェクトベースの見積依頼明細行の概要 

_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_

プロジェクトベースの見積依頼明細行は、エンゲージメントに関するプロジェクトの作業の見積もりに役立つように設計されています。 プロジェクトベースの見積依頼明細行の構造は、次の概念を使用してプロジェクト見積もり用に拡張されています。

- 請求方法
- プロジェクトとタスク マッピング
- 含まれるトランザクション クラス
- 上限
- 請求可否の設定
- 見積依頼明細行の詳細を使用した見積もり
- 見積依頼明細行の顧客

次の表に、プロジェクトベースの見積依頼明細行の **一般** タブのフィールドに関する情報を示します。 これらのフィールドは、プロジェクト作業の詳細な基礎的な見積もりの規準を設定するのに役立ちます。

| **フィールド** | **説明** | **下流への影響** |
| --- | --- | --- |
| 件名 | 見積もり対象の見積もりの個別のコンポーネントを識別するのに役立つ見積もり行の名前。 | 見積もりをが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 請求方法 | 営業案件から作成された見積もりでは、この値は営業案件品目の対応するフィールドからコピーされます。 このフィールドには、Dynamics 365 Project Operations によってサポートされる 2 つの主要な契約モデルが含まれます。</br>- 固定価格</br>- 時間と材料。| この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| Project | このオプションのフィールドを使用して、このエンゲージメントの作業を提供するために使用されるプロジェクトを特定します。 プロジェクトが見積依頼明細行にマップされると、請求可能タスクを設定したり、プロジェクトベースの見積もりを見積依頼明細行の詳細として見積依頼明細行に取り込むことができます。 プロジェクトがプロジェクトベースの見積依頼明細行にマップされていない場合は、各見積依頼明細行の詳細を作成して、見積もりを手動で作成する必要があります。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。|
| 含まれるタスク | この見積依頼明細行が、選択したプロジェクトのすべてまたは一部のプロジェクト タスクに使用されているかどうかを示します。 このフィールドには以下の指定できる値が入ります。</br>- すべてのプロジェクト タスク</br>- 選択したプロジェクト タスクのみ</br>このフィールドの空白の値は、**すべてのプロジェクト タスク** オプションに相当します。 | プロジェクト ページで **選択したプロジェクト タスクのみ** が選択されている場合、**タスクの請求設定** タブを使用すると、特定のタスクを選択して、それらをこの見積もり行に関連付けることができます。 この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 時間を含む | **はい**/**いいえ** の値は、選択したプロジェクトの時間トランザクションまたは労務費がこの見積もり行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれないことを示します。 **はい** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれることを示します。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 経費を含む | **はい**/**いいえ** の値は、選択したプロジェクトの経費の原価がこの見積もり行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、経費がこの見積依頼明細行の見積もりに含まれないことを示します。 **はい** の値は、経費がこの見積依頼明細行の見積もりに含まれることを示します。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 材料を含む | **はい**/**いいえ** の値は、選択したプロジェクトの材料の原価がこの見積もり行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、選択したプロジェクトの材料原価がこの見積もり行の見積もりに含まれないことを示します。 **はい** の値は、選択したプロジェクトの材料原価がこの見積もり行の見積もりに含まれることを示します。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 料金を含む | **はい**/**いいえ** の値は、選択したプロジェクトの手数料がこの見積もり行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、料金がこの見積依頼明細行の見積もりに含まれないことを示します。 **はい** の値は、料金がこの見積依頼明細行の見積もりに含まれることを示します。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 見積もり金額 | これは、このプロジェクトベースの見積もり行で予測されるすべての作業について顧客に見積もられる金額です。 営業案件から作成された見積もりでは、この値は営業案件品目の **顧客予算** フィールドからコピーされます。 プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の金額から集計されます。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 予測税額 | これは、ユーザーが見積依頼明細行に推定税額を追加するための編集可能なフィールドです。 プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の税額から集計されます。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 税引き後の見積もり金額 | このフィールドは税引き後の見積依頼明細行の金額であり、読み取り専用です。 このフィールドの金額は *見積もり金額+税* として計算されます。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 上限 | このフィールドは編集可能であり、**時間と材料** 請求方法があるプロジェクトベースの見積依頼明細行でのみ使用できます。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 顧客の予算 | このフィールドは編集可能であり、営業案件から見積もりが作成されると、営業案件品目の対応するフィールドからコピーされます。 | この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。 |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>プロジェクトベースの見積依頼明細行の全般タブのフィールドの検証ルール

**ルール 1**: **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトは見積依頼明細行に含まれています。

**ルール 2**: **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの 1 つのプロジェクトベースの見積依頼明細行にのみ含めることができます。

**ルール 3**: **含まれるタスク** フィールドが **選択したプロジェクト タスクのみ** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの複数のプロジェクトベースの見積依頼明細行に含めることができます。

**ルール 4**: 営業案件に複数の見積もりがある場合、すべてが同じプロジェクトを参照し、同じトランザクション クラスを含む異なる見積もりからの見積依頼明細行が存在する可能性があります。

**ルール 5**: 見積もりが同じ営業案件に属していない場合、同じプロジェクトとトランザクション クラスを含めることはできません。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>営業案件</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>見積もり</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>見積依頼明細行</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>含まれるタスク</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>時間を含む</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>経費を含む</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>材料を含む</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>参照項目</strong>
                </p>
                <p>
                    <strong>料金</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>有効/無効</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>理由</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
ルール #2 に違反。 P1 プロジェクトの時間、経費、および料金は、見積依頼明細行 QL1 および QL2 に含まれています </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
無効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
ルール #2 に違反。 P1 プロジェクトの時間、材料、提供は、見積依頼明細行 QL1 および QL2 に含まれています </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
無効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
P1 プロジェクトの時間、材料、および手数料は QL1 に含まれています <br>
P1 プロジェクトの経費は QL2 に含まれています <br>
各見積もり行に含まれているものに重複がないため、有効です。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
無効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
無効 </p>
            </td>
            <td width="41" valign="top">
                <p>
無効 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
ルール #2 に違反 </p>
                <p>
Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、材料、経費、および手数料が含まれています </p>
                <p>
QL2 には、プロジェクト P1 全体の時間、費用、手数料が含まれているため、C1 に含まれるものと重複します。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
ルール #3 により、 </p>
                <p>
Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、材料、経費、および手数料が含まれています。
                </p>
                <p>
QL2 には、プロジェクト P1 のタスクのサブセットに対する時間、材料、経費、および手数料が含まれています。
                </p>
                <p>
唯一の追加の検証は、CL1 のタスクのサブセットが、CL2 のタスクのサブセットとは異なり、重複がないことを確認することです。 これは、タスクが関連付けられたときにシステムによって実行されます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
ルール #5 によると、Q1 と Q2 は同じ営業案件の 2 つの見積もりであるため、どちらもプロジェクトの同じコンポーネントを見積もることができます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
ルール #4 によると、Q1 と Q2 は異なる営業案件の 2 つの見積もりであるため、どちらもプロジェクトの同じコンポーネントを見積もることはできません。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
有効 </p>
            </td>
            <td width="46" valign="top">
                <p>
有効 </p>
            </td>
            <td width="43" valign="top">
                <p>
有効 </p>
            </td>
            <td width="41" valign="top">
                <p>
有効 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
