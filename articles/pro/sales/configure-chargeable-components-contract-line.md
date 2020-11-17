---
title: プロジェクトベースの契約品目の請求可能コンポーネントを構成する
description: このトピックでは、Project Operations の契約品目に課金コンポーネントを追加する方法ついて解説します。
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079175"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>プロジェクトベースの契約品目の請求可能コンポーネントを構成する

_**適用対象:** ライト展開 - 見積もり請求の取引_

プロジェクト ベースの契約品目には、 *付属型* コンポーネントと *課金型* コンポーネントが含まれています。

付属型コンポーネントは、以下の対象となるコンポーネントです :

  - 請求方法と顧客の分割
  - 上限 
  - プロジェクトベースの契約品目で定義された請求書の発行の頻度設定

付属型コンポーネントのサブセットは、 **請求タイプ** フィールドを使用して課金型としてマークですることができます。 **請求タイプ** フィールドは、契約品目のコンテキストで次の値を許可するオプションセットです :

  - 請求可能
  - 請求不可

課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。

課金対象は、プロジェクト契約品目のタスクで定義され、品目に含まれるすべてのトランザクション クラスに適用されます。 契約品目の **タスクを含める** フィールドが空白であるか、* *プロジェクト全体* *に設定されている場合は、 **課金型タスク** タブは使用できません。

プロジェクト契約品目のロールで定義された課金対象は、 **時間** トランザクション クラスにのみ適用されます。 契約品目の **時間を含める** フィールドが空白であるか、 **いいえ** に設定されている場合は、 **課金型ロール** タブは使用できません。

プロジェクト契約品目のトランザクション カテゴリで定義された課金対象は、 **経費** トランザクション クラスにのみ適用されます。 **経費を含める** フィールドが空白であるか、 **いいえ** に設定されている場合は、 **課金型カテゴリ** タブは使用できません。

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>プロジェクト タスクを課金対象または非課金対象として更新します

プロジェクト タスクは、特定の契約品目で課金/非課金にすることができます。これにより、次の設定が可能になります :

プロジェクト ベースの契約品目に **時間** と特定のタスクが含まれる場合、、 **T1** が課金として関連付けられています。 **経費** を含む 2 つ目の契約品目がある場合は、契約品目の T1 タスクを非課金として関連付けることができます。 その結果、タスクに記録されたすべての時間は課金対象となり、すべての経費は課金対象外になります。

タスクの請求タイプは、契約品目のタスク サブグリッドの **請求タイプ** フィールドを更新することで、契約品目の **課金タスク** タブで構成することができます。 あるいは、タスクに関連付けられた契約品目が表示される、プロジェクトのタスク請求設定のサブグリッドの **請求タイプ** フィールドを更新することもできます。

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>ロールを課金対象または非課金対象として更新します

ロールは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。

ロールの請求タイプは、契約品目の **課金対象ロール** タブで構成することができます。 これを行うには、 **課金対象ロール** サブグリッドの **請求タイプ** フィールドを更新します。

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>トランザクション カテゴリを課金対象、または非課金対象として更新する

トランザクション カテゴリは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。

トランザクションの請求タイプは、プロジェクトベースの契約品目の **課金対象カテゴリ** タブで構成することができます。 これを行うには、 **課金対象カテゴリ** サブグリッドの **請求タイプ** フィールドを更新します。

### <a name="resolve-chargeability"></a>課金対象の解決

時間に対して作成された見積もりや実績は、契約品目に **時間** が含まれていて、かつ契約品目で **タスク** と **ロール** が課金対象として設定されている場合にのみ、課金対象とみなされます。

経費に対して作成された見積もりや実績は、契約品目に **経費** が含まれている場合、かつ契約品目で **タスク** と **トランザクション** のカテゴリが経費として設定されている場合にのみ、経費が発生するとみなされます。


| 時間を含む | 経費を含む | タスクを含む | ロール           | カテゴリ       | タスク​                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| 有効           | 有効              | プロジェクトの全体 | 請求可能     | 請求可能     | 実績時間に基づく請求 : **課金** </br> 経費の実績に基づく請求タイプ : **課金**           |
| 有効           | 有効              | 選択したタスク | 請求可能     | 請求可能     | 実績時間に基づく請求 : **課金** </br> 経費の実績に基づく請求タイプ : **課金**           |
| 有効           | 有効              | 選択したタスク | 請求不可 | 請求可能     | 実績時間に基づく請求 : **非課金** </br> 経費の実績に基づく請求タイプ : **課金**       |
| 有効           | 有効              | 選択したタスク | 請求可能     | 請求可能     | 実績時間に基づく請求 : **非課金** </br> 経費の実績に基づく請求タイプ : **非課金** |
| 有効           | 有効              | 選択したタスク | 請求不可 | 請求可能     | 実績時間に基づく請求 : **非課金** </br> 経費の実績に基づく請求タイプ : **非課金** |
| 有効           | 有効              | 選択したタスク | 請求不可 | 請求不可 | 実績時間に基づく請求 : **非課金** </br> 経費の実績に基づく請求タイプ : **非課金** |
| 無効            | 有効              | プロジェクトの全体 | 設定できません   | 請求可能     | 実績時間に基づく請求 : **非対応**</br>経費の実績に基づく請求タイプ : **課金**          |
| 無効            | 有効              | プロジェクトの全体 | 設定できません   | 請求不可 | 実績時間に基づく請求 : **非対応**</br> 経費の実績に基づく請求タイプ : **非課金**     |
| 有効           | 無効               | プロジェクトの全体 | 請求可能     | 設定できません   | 実績時間に基づく請求 : **課金** </br> 経費の実績に基づく請求タイプ : **非対応**        |
| 有効           | 無効               | プロジェクトの全体 | 請求不可 | 設定できません   | 実績時間に基づく請求 : **非課金** </br>経費の実績に基づく請求タイプ : **非対応**   |