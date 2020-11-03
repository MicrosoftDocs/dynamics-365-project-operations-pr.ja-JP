---
title: プロジェクトベースの見積依頼明細行 (Pro)
description: このトピックは、プロジェクト作業のプロジェクトベースの見積依頼明細行の使用に関する情報を提供します。 (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079198"
---
# <a name="project-based-quote-lines-pro"></a>プロジェクトベースの見積依頼明細行 (Pro)

_**適用対象:** ライト展開 - 見積もり請求の取引_

プロジェクトベースの見積依頼明細行は、エンゲージメントに関するプロジェクトの作業の見積もりに役立つように設計されています。 プロジェクトベースの見積依頼明細行の構造は、次の概念を使用してプロジェクト見積もり用に拡張されています。

- 請求方法
- プロジェクトとタスク マッピング
- 含まれるトランザクション クラス
- 上限
- 請求可否の設定
- 見積依頼明細行の詳細を使用した見積もり
- 見積依頼明細行の顧客

次の表に、プロジェクトベースの見積依頼明細行の **一般** タブのフィールドに関する情報を示します。 これらのフィールドは、プロジェクト作業の詳細な基礎的な見積もりの規準を設定するのに役立ちます。

| **フィールド** | **関連性、目的、およびガイダンス** | **下位への影響** |
| --- | --- | --- |
| 件名 | 見積もられている見積もりの個別のコンポーネントを識別するのに役立つ見積依頼明細行の名前。 | 見積もりをが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 請求方法 | 営業案件から作成された見積もりでは、この値は営業案件品目の対応するフィールドからコピーされます。 このフィールドには、Dynamics 365 Project Operations でサポートされている 2 つの主要な契約モデルが含まれています。</br>- 固定価格</br>- 時間と材料。| このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| Project | このオプションのフィールドを使用して、このエンゲージメントの作業を提供するために使用されるプロジェクトを特定します。 プロジェクトが見積依頼明細行にマップされると、請求可能タスクを設定したり、プロジェクトベースの見積もりを見積依頼明細行の詳細として見積依頼明細行に取り込むことができます。 プロジェクトがプロジェクトベースの見積依頼明細行にマップされていない場合は、各見積依頼明細行の詳細を作成して、見積もりを手動で作成する必要があります。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。|
| 含まれるタスク | この見積依頼明細行が、選択したプロジェクトのすべてまたは一部のプロジェクト タスクに使用されているかどうかを示します。 このフィールドには以下の指定できる値が入ります。</br>- すべてのプロジェクト タスク</br>- 選択したプロジェクト タスクのみ</br>このフィールドの空白の値は、 **すべてのプロジェクト タスク** オプションに相当します。 | **選択したプロジェクト タスクのみ** が選択され、プロジェクト ページで、 **タスクの請求の設定** タブでは、特定のタスクを選択して、それらをこの見積依頼明細行に関連付けることができます。 このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 時間を含む | **はい**/**いいえ** のフラグは、選択したプロジェクトの時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれないことを示します。 **はい** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれることを示します。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 経費を含む | **はい**/**いいえ** のフラグは、選択したプロジェクトの経費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、経費がこの見積依頼明細行の見積もりに含まれないことを示します。 **はい** の値は、経費がこの見積依頼明細行の見積もりに含まれることを示します。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 料金を含む | **はい**/**いいえ** のフラグは、選択したプロジェクトの料金がこの見積依頼明細行の見積もりに含まれるかどうかを示します。 **いいえ** の値は、料金がこの見積依頼明細行の見積もりに含まれないことを示します。 **はい** の値は、料金がこの見積依頼明細行の見積もりに含まれることを示します。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 見積もり金額 | これは、このプロジェクトベースの見積依頼明細行で予測されるすべての作業について顧客に見積もられる金額です。 営業案件から作成された見積もりでは、この値は営業案件品目の **顧客予算** フィールドからコピーされます。 プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の金額から集計されます。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 予測税額 | これは、ユーザーが見積依頼明細行に推定税額を追加するための編集可能なフィールドです。 プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の税額から集計されます。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 税引き後の見積もり金額 | このフィールドは税引き後の見積依頼明細行の金額であり、読み取り専用です。 このフィールドの金額は *見積もり金額+税* として計算されます。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 上限 | このフィールドは編集可能であり、 **時間と材料** 請求方法があるプロジェクトベースの見積依頼明細行でのみ使用できます。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |
| 顧客の予算 | このフィールドは編集可能であり、営業案件から見積もりが作成されると、営業案件品目の対応するフィールドからコピーされます。 | このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。 |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>プロジェクトベースの見積依頼明細行の全般タブのフィールドの検証ルール

**ルール 1** : **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトは見積依頼明細行に含まれています。

**ルール 2** : **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの 1 つのプロジェクトベースの見積依頼明細行にのみ含めることができます。

**ルール 3** : **含まれるタスク** フィールドが **選択したプロジェクト タスクのみ** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの複数のプロジェクトベースの見積依頼明細行に含めることができます。

**ルール 4** : 営業案件に複数の見積もりがある場合、すべてが同じプロジェクトを参照し、同じトランザクション クラスを含む異なる見積もりからの見積依頼明細行が存在する可能性があります。

**ルール 5** : 見積もりが同じ営業案件に属していない場合、同じプロジェクトとトランザクション クラスを含めることはできません。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>営業案件</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>見積もり</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>見積依頼明細行</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
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
                    <strong>含む</strong>
                </p>
                <p>
                    <strong>料金</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>有効/無効</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>理由</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ルール #2 に違反。 P1 プロジェクトの時間、経費、および料金は、見積依頼明細行 QL1 および QL2 に含まれています。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ルール #2 に違反。 P1 プロジェクトの時間および料金は、見積依頼明細行 QL1 および QL2 に含まれています。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
P1 プロジェクトの時間および料金は QL1 に含まれています。
P1 プロジェクトの経費は QL2 に含まれています。
各見積依頼明細行に含まれているものに重複はなく、有効です。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
無効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
上記のルール #2 に違反 </p>
                <p>
Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、経費、および料金が含まれます。
                </p>
                <p>
QL2 には、プロジェクト P1 全体の時間、経費、および料金が含まれており、Q1 に含まれているものと重複しています。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
空 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
有効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
上記のルール #3 に従い、 </p>
                <p>
Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、経費、および料金が含まれます。
                </p>
                <p>
QL2 には、プロジェクト P1 のタスクのサブセットに関する時間、経費、および料金が含まれます。
                </p>
                <p>
唯一の追加の検証は、QL2 のタスクのサブセットとは異なる QL1 のタスクのサブセットに関するものです。 これにより、重複がなくなります。 これは、タスクが関連付けられたときにシステムによって実行されます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
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
            <td width="54" valign="top">
                <p>
有効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ルール #5 に基づいて、Q1 と Q2 は同じ営業案件の 2 つの見積もりであるため、両方ともプロジェクトの同じコンポーネントを見積もることができます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
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
            <td width="54" valign="top">
                <p>
有効 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ルール #4 に基づいて、Q1 と Q2 は異なる営業案件の 2 つの見積もりであるため、両方が同じプロジェクトの同じコンポーネントを見積もることはできません。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
すべてのプロジェクト タスクまたは空白 </p>
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
            <td width="54" valign="top">
                <p>
無効 </p>
            </td>
        </tr>
    </tbody>
</table>

