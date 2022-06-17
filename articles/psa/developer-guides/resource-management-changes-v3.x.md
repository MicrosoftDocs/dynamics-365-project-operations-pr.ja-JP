---
title: リソースの管理の変更 (Project Service Automation 3.x)
description: この記事では、リソース管理領域への変更について説明します。
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916018"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>リソースの管理の変更 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

この記事のこのセクションでは、Dynamics 365 Project Service Automation バージョン 3.x のリソース管理領域に加える変更について説明します。

## <a name="project-estimates"></a>プロジェクト見積もり

**msdyn\_projecttask** エンティティ (**プロジェクト タスク**) に基づく代わりに、プロジェクト見積は **msdyn\_resourceassignment** エンティティ (**リソースの割り当て**) に基づいています。 リソースの割り当ては、タスク スケジュールと価格設定の「真実のソース」となりました。

## <a name="line-tasks"></a>ライン タスク

PSA 3.x では、ライン タスクは現在不使用となっています (非推奨)。 割り当ては現在、ライン タスクではなく全タスクを指します。

次の例では、PSA の前のバージョンと、PSA 3.x で、「テストタスク」と言う名前の付いたタスクが、チームメンバー A と B に割り当てられる方法を示します。

- **PSA 3.x より前:**

    - テスト タスク

        - テスト タスク – ライン タスク 1

            - A への割り当て

        - テスト タスク – ライン タスク 2

            - B への割り当て

- **PSA 3.x:**

    - テスト タスク

        - A への割り当て
        - B への割り当て

## <a name="unassigned-assignment"></a>割り当てされていない割り当て

PSA 3.x では、割り当てされていない割り当ては **NULL** チーム メンバーと **NULL** リソースに割り当てられた割り当てです。 割り当てされていない割り当てはいくつかのシナリオで発生します:

- タスクが作成されたが、どのチーム メンバーにもまだ割り当てられていない場合、割り当てされていない割り当てが常に作成されます。 
- タスクのすべての担当者が削除された場合は、割り当てされていない割り当てがそのタスクに対して再度作成されます。

## <a name="scheduling-fields-on-the-project-task-entity"></a>プロジェクト タスク エンティティ上のフィールドのスケジュール

**msdyn\_projecttask** エンティティのフィールドは、非推奨となるか **msdyn\_resourceassignment** エンティティへと移動されている、あるいは現在は **msdyn\_projectteam** エンティティ (**プロジェクト チーム メンバー**) から参照されています。

| msdyn\_projecttask (プロジェクト タスク) の非推奨のフィールド | msdyn\_resourceassignment (リソース割り当て) の新しいフィールド | コメント |
|---|---|---|
| msdyn\_assignedresources | なし | |
| msdyn\_assignedteammembers | なし | |
| msdyn\_numberofresources | なし | |
| msdyn\_scheduledhours | なし | |
| msdyn\_effortcontour | msdyn\_plannedwork | フィールドに格納された JavaScript Object Notation (JSON) のデータ構造の形式が変更されました。 |

## <a name="schedule-contour"></a>スケジュール輪郭

スケジュール輪郭は、**リソース割り当て** の各エンティティ (**msdyn\_resourceassignment**) の **計画作業** フィールド (**msdyn\_plannedwork**) に保存されています。

### <a name="structure"></a>構造体

このスケジュール輪郭の新しい構造は、スケジュールの各日に対して定義されている柔軟性の高いタイム スライスから構成されます。 各タイム スライスには以下のプロパティがあります。

- **開始** – プロジェクトのカレンダーに従った、その日の作業時間の始まり。
- **終了** – プロジェクトのカレンダーに従った、その日の作業時間の終わり。
- **時間** – その日に割り当てられた時間数。

**例**

この例では、作業日が UTC-8 タイム ゾーンの 9 AM から 5 PM のプロジェクト カレンダーが使用されます。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>自動スケジュールと手動スケジュール

タスクが自動スケジュールされた場合は、時間は減少型になるので、タスク期間が減少する可能性があります。

**例**

次のタスクは、3 日間のうちの 18 時間（2018 年 12 月 3 日から 2018 年 12 月 5 日まで）を使用して自動スケジュールが実行されます。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

タスクが手動でスケジュールされた場合は、時間はすべての日付に対して均等に分配されます。

**例**

次のタスクは、3 日間のうちの 18 時間（2018 年 12 月 3 日から 2018 年 12 月 5 日まで）を使用して手動スケジュールが実行されます。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>割り当て単位

割り当て単位は  PSA 3.x では非推奨となっています。 タスク工数は、すべての割り当てられたリソース間で 1 日当たりで現在は等しく分割されています。

**例**

この例では、タスクは 2 つのリソースに割り当てられ、3 日間のうちの 36 時間（2018年12月3日から2018年12月5日まで）を使用して自動スケジュールされます。

- 割り当て 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 割り当て 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>価格ディメンション

PSA 3.x では、リソース固有の価格ディメンションのフィールド (**ロール** と **組織単位** など) は **msdyn\_projecttask** エンティティから削除されています。 これらのフィールドは、プロジェクト見積が生成された際に、リソース割り当て (**msdyn\_resourceassignment**) の対応するプロジェクト チーム メンバー (**msdyn\_projectteam**) から取得できるようになりました。 新規フィールドである、**msdyn\_organizationalunit** が、**msdyn\_projectteam** エンティティに追加されました。

| msdyn\_projecttask (プロジェクト タスク) の非推奨のフィールド | 代わり使用される、msdyn\_projectteam (プロジェクト チーム メンバー) からのフィールド |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>輪郭

価格および見積もり輪郭フィールドは、**msdyn\_projecttask** エンティティでは非推奨となりました。 これらのフィールドは、**msdyn\_resourceassignment** エンティティに移動されました。

| msdyn\_projecttask (プロジェクト タスク) の非推奨のフィールド | msdyn\_resourceassignment (リソース割り当て) の新しいフィールド |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

以下のフィールドは、**msdyn\_resourceassignment** エンティティに追加されました。

* msdyn\_plannedcost
* msdyn\_plannedsales

計画済み、実績、および残りのコストおよび売上に対する次のフィールドは、**msdyn\_projecttask** エンティティでは変更されていません:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
