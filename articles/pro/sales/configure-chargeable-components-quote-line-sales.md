---
title: 見積依頼明細行の請求可能コンポーネントを構成する
description: このトピックでは、プロジェクトベースの見積明細での課金対象コンポーネントと非課金対象コンポーネントの設定に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079389"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>見積依頼明細行の請求可能コンポーネントを構成する

_**適用対象:** ライト展開 - 見積もり請求の取引_

プロジェクト ベースの見積品目には、 *付属型* コンポーネントと *有料型* コンポーネントの概念があります。

含まれているコンポーネントは、次の対象となります :

  - 請求方法と顧客の分割
  - 上限 
  - プロジェクト ベースの見積明細で定義された請求書の発行の頻度設定

付属型コンポーネントのサブセットは、 **請求タイプ** フィールドを使用して課金型としてマークですることができます。 **請求タイプ** フィールドは、見積明細のコンテキストで次の値を許可するオプションセットです :

  - 請求可能
  - 請求不可

課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。

課金対象は、見積明細のタスクで定義され、明細に含まれるすべてのトランザクション クラスに適用されます。 契約品目の **タスクを含める** フィールドが空白であるか、 **プロジェクト全体** に設定されている場合は、 **有料型タスク** タブは使用できません。

プロジェクトの見積明細のロールで定義された課金対象は、 **時間** トランザクション クラスにのみ適用されます。 プロジェクトの見積明細の **時間を含める** フィールドが空白であるか、 **いいえ** に設定されている場合は、 **有料型ロール** タブは使用できません。

見積品目のトランザクション カテゴリで定義された課金対象は、 **経費** トランザクション クラスにのみ適用されます。 プロジェクトの見積明細の **経費を含める** フィールドが空白であるか、 **いいえ** に設定されている場合は、 **有料型カテゴリ** タブは使用できません。

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>プロジェクト タスクを課金対象または非課金対象として更新します

プロジェクト タスクは、特定のプロジェクトベースの見積明細で課金/非課金にすることができます。これにより、次の設定が可能になります :

プロジェクトベースの見積明細に **時間** とタスク **T1** が含まれている場合、タスクは課金対象として見積もり行に関連付けられています。 **経費** を含む 2 つ目の見積明細がある場合は、契約品目の **T1** タスクを非課金として関連付けることができます。 その結果、タスクに記録されたすべての時間は課金対象となり、経費に記録されているすべてのタスクは課金対象外になります。

タスクの請求タイプは、 **見積明細タスク** サブグリッドの **請求タイプ** フィールドを更新することで、プロジェクトベースの見積明細の **課金タスク** タブで構成することができます。 あるいは、タスクに関連付けられた見積明細を表示するプロジェクトの、タスク請求設定のサブグリッドの **請求タイプ** フィールドで、プロジェクト タスクの課金タイプを更新することもできます。

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>ロールを課金対象、または非課金対象として更新します

ロールは、特定のプロジェクト ベースの見積明細のコンテキストによっては、課金または非課金にすることができます。

ロールの課金タイプは、 **課金ロール** サブグリッドの **請求タイプ** フィールドを更新することで、見積書ラインの **課金ロール** タブで設定することができます。

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>トランザクション カテゴリを課金対象、または非課金対象として更新する

トランザクション カテゴリは、特定の見積明細では課金対象となる場合と非課金対象となる場合があります。

トランザクションの課金タイプは、 **課金カテゴリ** サブグリッドの **請求タイプ** フィールドを更新することで、見積書ラインの **課金カテゴリ** タブで設定することができます。

### <a name="resolve-chargeability"></a>課金対象の解決
時間に対して作成された見積もりや実績は、見積明細に **時間** が含まれていて、かつ見積明細で **タスク** と **ロール** が課金対象として設定されている場合にのみ、課金対象とみなされます。

経費に対して作成された見積もりや実績は、見積品目に **経費** が含まれている場合、かつ見積品目で **タスク** と **トランザクション カテゴリ** のカテゴリが経費として設定されている場合にのみ、経費が発生するとみなされます。

| 時間を含む | 経費を含む | 含まれるタスク | ロール | カテゴリ | タスク​ | 請求先 |
| --- | --- | --- | --- | --- | --- | --- |
| 有効 | 有効 | プロジェクトの全体 | 請求可能 | 請求可能 | 設定できません | 実績時間に基づく請求 : 課金 </br>経費の実績に基づく請求タイプ : 課金 |
| 有効 | 有効 | 選択したタスクのみ | 請求可能 | 請求可能 | 請求可能 | 実績時間に基づく請求 : 課金</br>経費の実績に基づく請求タイプ : 課金 |
| 有効 | 有効 | 選択したタスクのみ | 請求不可 | 請求可能 | 請求可能 | 実績時間に基づく請求 : 非課金</br>経費の実績に基づく請求タイプ : 課金 |
| 有効 | 有効 | 選択したタスクのみ | 請求可能 | 請求可能 | 請求不可 | 実績時間に基づく請求 : 非課金</br> 経費の実績に基づく請求タイプ : 非課金 |
| 有効 | 有効 | 選択したタスクのみ | 請求不可 | 請求可能 | 請求不可 | 実績時間に基づく請求 : 非課金</br> 経費の実績に基づく請求タイプ : 非課金 |
| 有効 | 有効 | 選択したタスクのみ | 請求不可 | 請求不可 | 請求可能 | 実績時間に基づく請求 : 非課金</br> 経費の実績に基づく請求タイプ : 非課金 |
| 無効 | 有効 | プロジェクトの全体 | 設定できません | 請求可能 | 設定できません | 実績時間に基づく請求 : 非対応 </br>経費の実績に基づく請求タイプ : 課金 |
| 無効 | 有効 | プロジェクトの全体 | 設定できません | 請求不可 | 設定できません | 実績時間に基づく請求 : 非対応 </br>経費の実績に基づく請求タイプ : 非課金 |
| 有効 | 無効 | プロジェクトの全体 | 請求可能 | 設定できません | 設定できません | 実績時間に基づく請求 : 課金</br>経費の実績に基づく請求タイプ : 非対応 |
| 有効 | 無効 | プロジェクトの全体 | 請求不可 | 設定できません | 設定できません | 実績時間に基づく請求 : 非課金 </br>経費の実績に基づく請求タイプ : 非対応 |