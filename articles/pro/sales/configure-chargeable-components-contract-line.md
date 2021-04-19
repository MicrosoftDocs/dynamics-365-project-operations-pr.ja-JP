---
title: プロジェクトベースの契約品目の請求可能コンポーネントを構成する
description: このトピックでは、Project Operations の契約品目に課金コンポーネントを追加する方法ついて解説します。
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858479"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>プロジェクトベースの契約品目の請求可能コンポーネントを構成する

_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_

プロジェクト ベースの契約品目には、*付属型* コンポーネントと *課金型* コンポーネントが含まれています。

付属型コンポーネントは、以下の対象となるコンポーネントです :

  - 請求方法と顧客の分割
  - 上限 
  - プロジェクトベースの契約品目で定義された請求書の発行の頻度設定

付属型コンポーネントのサブセットは、**請求タイプ** フィールドを使用して課金型としてマークですることができます。 **請求タイプ** フィールドは、契約品目のコンテキストで次の値を許可するオプションセットです :

  - 請求可能
  - 請求不可

課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。

課金対象は、プロジェクト契約品目のタスクで定義され、品目に含まれるすべてのトランザクション クラスに適用されます。 契約品目の **タスクを含める** フィールドが空白であるか、**プロジェクト全体** に設定されている場合は **課金型タスク** タブを使用できません。

プロジェクト契約品目のロールで定義された課金対象は、**時間** トランザクション クラスにのみ適用されます。 契約品目の **時間を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**課金型ロール** タブは使用できません。

プロジェクト契約品目のトランザクション カテゴリで定義された課金対象は、**経費** トランザクション クラスにのみ適用されます。 **経費を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**課金型カテゴリ** タブは使用できません。

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>プロジェクト タスクを課金対象または非課金対象として更新します

プロジェクト タスクは、特定の契約品目で課金/非課金にすることができます。これにより、次の設定が可能になります: 

プロジェクト ベースの契約品目に **時間** と特定のタスクが含まれる場合、、**T1** が課金として関連付けられています。 **経費** を含む 2 つ目の契約品目がある場合は、契約品目の T1 タスクを非課金として関連付けることができます。 その結果、タスクに記録されたすべての時間は課金対象となり、すべての経費は課金対象外になります。

タスクの課金タイプは、契約品目タスク サブグリッドの **課金タイプ** フィールドを更新することで、契約品目の **課金タスク** タブで設定することができます。 または、タスクに関連付けられた契約品目を表示するプロジェクトのタスクの課金設定のサブグリッドの **課金タイプ** フィールドを更新することができます。

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>ロールを課金対象または非課金対象として更新します

ロールは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。

ロールの請求タイプは、契約品目の **課金対象ロール** タブで構成することができます。 これを行うには、**課金対象の役割** サブグリッドの **課金タイプ** フィールドを更新します。

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>トランザクション カテゴリを課金対象、または非課金対象として更新する

トランザクション カテゴリは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。

トランザクションの請求タイプは、プロジェクトベースの契約品目の **課金対象カテゴリ** タブで構成することができます。 これを行うには、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドを更新します。

### <a name="resolve-chargeability"></a>課金対象の解決

時間に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。

   - **時間** が契約品目に含まれている。
   - **役割** が契約品目で請求可能と構成されている。
   - **含まれるタスク** が、契約品目で **選択したタスク** に設定されている。
 
 これらの 3 つの条件が当てはまる場合、タスクは請求可能と構成されます。 

経費に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。

   - **経費** が契約品目に含まれている
   - **トランザクション カテゴリ** が、契約品目で請求可能と構成されている
   - **含まれるタスク** が、契約品目で **選択したタスク** に設定されている
  
 これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。 

材料に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。

   - **材料** が契約品目に含まれている
   - **含まれるタスク** が、契約品目で **選択したタスク** に設定されている

これらの 2 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>時間を含む</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>経費を含む</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>材料を含む</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>含まれるタスク</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>ロール</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>カテゴリ</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>タスク​</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>請求可否</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="70" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
実績時間に基づく請求: <strong>請求可能</strong>
                </p>
                <p>
経費の実績に基づく請求タイプ: <strong>課金</strong>
                </p>
                <p>
材料実績の請求タイプ: <strong>請求可能</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="70" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="350" valign="top">
                <p>
実績時間に基づく請求: <strong>請求可能</strong>
                </p>
                <p>
経費の実績に基づく請求タイプ: <strong>課金</strong>
                </p>
                <p>
材料実績の請求タイプ: <strong>請求可能</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求: <strong>請求不可</strong>
                </p>
                <p>
経費の実績に基づく請求タイプ : 課金 </p>
                <p>
材料実績の請求タイプ: 請求可能 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="70" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求: <strong>請求不可</strong>
                </p>
                <p>
経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
                <p>
材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求: <strong>請求不可</strong>
                </p>
                <p>
経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
                <p>
材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
選択したタスクのみ </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求: <strong>請求不可</strong>
                </p>
                <p>
経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
                <p>
材料実績の請求タイプ: 請求可能 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>無効</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>請求可能</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求:<strong>非対応</strong>
                </p>
                <p>
経費の実績に基づく請求タイプ : 課金 </p>
                <p>
材料実績の請求タイプ: 請求可能 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>無効</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求:<strong>非対応</strong>
                </p>
                <p>
経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
                <p>
材料実績の請求タイプ: 請求可能 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>無効</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="70" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
実績時間に基づく請求 : 課金 </p>
                <p>
経費実績に基づく請求タイプ: <strong>非対応</strong>
                </p>
                <p>
材料実績の請求タイプ: 請求可能 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>無効</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
有効 </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求: <strong>請求不可</strong>
                </p>
                <p>
経費実績に基づく請求タイプ: <strong>非対応</strong>
                </p>
                <p>
材料実績の請求タイプ: 請求可能 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>無効</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="70" valign="top">
                <p>
請求可能 </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
実績時間に基づく請求 : 課金 </p>
                <p>
経費の実績に基づく請求タイプ : 課金 </p>
                <p>
資材実績に基づく請求タイプ: <strong>非対応</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
有効 </p>
            </td>
            <td width="78" valign="top">
                <p>
有効 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>無効</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
プロジェクトの全体 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>請求不可</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
設定できません </p>
            </td>
            <td width="350" valign="top">
                <p>
時間実績に基づく請求: <strong>請求不可</strong>
                </p>
                <p>
経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </p>
                <p>
資材実績に基づく請求タイプ: <strong>非対応</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
