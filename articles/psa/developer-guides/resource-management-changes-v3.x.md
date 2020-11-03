---
title: リソースの管理の変更 (Project Service Automation 3.x)
description: このトピックでは、リソース管理領域について説明します。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079459"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="b48f2-103">リソースの管理の変更 (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="b48f2-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="b48f2-104">このトピックのセクションでは、Dynamics 365 Project Service Automation バージョン 3.x のリソース管理領域に加える変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="b48f2-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="b48f2-105">プロジェクト見積もり</span><span class="sxs-lookup"><span data-stu-id="b48f2-105">Project estimates</span></span>

<span data-ttu-id="b48f2-106">**msdyn\_projecttask** エンティティ ( **プロジェクト タスク** ) に基づく代わりに、プロジェクト見積は **msdyn\_resourceassignment** エンティティ ( **リソースの割り当て** ) に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b48f2-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="b48f2-107">リソースの割り当ては、タスク スケジュールと価格設定の「真実のソース」となりました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="b48f2-108">ライン タスク</span><span class="sxs-lookup"><span data-stu-id="b48f2-108">Line tasks</span></span>

<span data-ttu-id="b48f2-109">PSA 3.x では、ライン タスクは現在不使用となっています (非推奨)。</span><span class="sxs-lookup"><span data-stu-id="b48f2-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="b48f2-110">割り当ては現在、ライン タスクではなく全タスクを指します。</span><span class="sxs-lookup"><span data-stu-id="b48f2-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="b48f2-111">次の例では、PSA の前のバージョンと、PSA 3.x で、「テストタスク」と言う名前の付いたタスクが、チームメンバー A と B に割り当てられる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b48f2-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="b48f2-112">**PSA 3.x より前:**</span><span class="sxs-lookup"><span data-stu-id="b48f2-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="b48f2-113">テスト タスク</span><span class="sxs-lookup"><span data-stu-id="b48f2-113">Test task</span></span>

        - <span data-ttu-id="b48f2-114">テスト タスク – ライン タスク 1</span><span class="sxs-lookup"><span data-stu-id="b48f2-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="b48f2-115">A への割り当て</span><span class="sxs-lookup"><span data-stu-id="b48f2-115">Assignment to A</span></span>

        - <span data-ttu-id="b48f2-116">テスト タスク – ライン タスク 2</span><span class="sxs-lookup"><span data-stu-id="b48f2-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="b48f2-117">B への割り当て</span><span class="sxs-lookup"><span data-stu-id="b48f2-117">Assignment to B</span></span>

- <span data-ttu-id="b48f2-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="b48f2-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="b48f2-119">テスト タスク</span><span class="sxs-lookup"><span data-stu-id="b48f2-119">Test task</span></span>

        - <span data-ttu-id="b48f2-120">A への割り当て</span><span class="sxs-lookup"><span data-stu-id="b48f2-120">Assignment to A</span></span>
        - <span data-ttu-id="b48f2-121">B への割り当て</span><span class="sxs-lookup"><span data-stu-id="b48f2-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="b48f2-122">割り当てされていない割り当て</span><span class="sxs-lookup"><span data-stu-id="b48f2-122">Unassigned assignment</span></span>

<span data-ttu-id="b48f2-123">PSA 3.x では、割り当てされていない割り当ては **NULL** チーム メンバーと **NULL** リソースに割り当てられた割り当てです。</span><span class="sxs-lookup"><span data-stu-id="b48f2-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="b48f2-124">割り当てされていない割り当てはいくつかのシナリオで発生します:</span><span class="sxs-lookup"><span data-stu-id="b48f2-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="b48f2-125">タスクが作成されたが、どのチーム メンバーにもまだ割り当てられていない場合、割り当てされていない割り当てが常に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="b48f2-126">タスクのすべての担当者が削除された場合は、割り当てされていない割り当てがそのタスクに対して再度作成されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="b48f2-127">プロジェクト タスク エンティティ上のフィールドのスケジュール</span><span class="sxs-lookup"><span data-stu-id="b48f2-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="b48f2-128">**msdyn\_projecttask** エンティティのフィールドは、非推奨となるか **msdyn\_resourceassignment** エンティティへと移動されている、あるいは現在は **msdyn\_projectteam** エンティティ ( **プロジェクト チーム メンバー** ) から参照されています。</span><span class="sxs-lookup"><span data-stu-id="b48f2-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="b48f2-129">msdyn\_projecttask (プロジェクト タスク) の非推奨のフィールド</span><span class="sxs-lookup"><span data-stu-id="b48f2-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="b48f2-130">msdyn\_resourceassignment (リソース割り当て) の新しいフィールド</span><span class="sxs-lookup"><span data-stu-id="b48f2-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="b48f2-131">コメント</span><span class="sxs-lookup"><span data-stu-id="b48f2-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="b48f2-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="b48f2-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="b48f2-133">なし</span><span class="sxs-lookup"><span data-stu-id="b48f2-133">None</span></span> | |
| <span data-ttu-id="b48f2-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="b48f2-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="b48f2-135">なし</span><span class="sxs-lookup"><span data-stu-id="b48f2-135">None</span></span> | |
| <span data-ttu-id="b48f2-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="b48f2-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="b48f2-137">なし</span><span class="sxs-lookup"><span data-stu-id="b48f2-137">None</span></span> | |
| <span data-ttu-id="b48f2-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="b48f2-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="b48f2-139">なし</span><span class="sxs-lookup"><span data-stu-id="b48f2-139">None</span></span> | |
| <span data-ttu-id="b48f2-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="b48f2-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="b48f2-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="b48f2-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="b48f2-142">フィールドに格納された JavaScript Object Notation (JSON) のデータ構造の形式が変更されました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="b48f2-143">スケジュール輪郭</span><span class="sxs-lookup"><span data-stu-id="b48f2-143">Schedule contour</span></span>

<span data-ttu-id="b48f2-144">スケジュール輪郭は、 **リソース割り当て** の各エンティティ ( **msdyn\_resourceassignment** ) の **計画作業** フィールド ( **msdyn\_plannedwork** ) に保存されています。</span><span class="sxs-lookup"><span data-stu-id="b48f2-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="b48f2-145">構造体</span><span class="sxs-lookup"><span data-stu-id="b48f2-145">Structure</span></span>

<span data-ttu-id="b48f2-146">このスケジュール輪郭の新しい構造は、スケジュールの各日に対して定義されている柔軟性の高いタイム スライスから構成されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="b48f2-147">各タイム スライスには以下のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="b48f2-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="b48f2-148">**開始** – プロジェクトのカレンダーに従った、その日の作業時間の始まり。</span><span class="sxs-lookup"><span data-stu-id="b48f2-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="b48f2-149">**終了** – プロジェクトのカレンダーに従った、その日の作業時間の終わり。</span><span class="sxs-lookup"><span data-stu-id="b48f2-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="b48f2-150">**時間** – その日に割り当てられた時間数。</span><span class="sxs-lookup"><span data-stu-id="b48f2-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="b48f2-151">**例**</span><span class="sxs-lookup"><span data-stu-id="b48f2-151">**Example**</span></span>

<span data-ttu-id="b48f2-152">この例では、作業日が UTC-8 タイム ゾーンの 9 AM から 5 PM のプロジェクト カレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="b48f2-153">自動スケジュールと手動スケジュール</span><span class="sxs-lookup"><span data-stu-id="b48f2-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="b48f2-154">タスクが自動スケジュールされた場合は、時間は減少型になるので、タスク期間が減少する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b48f2-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="b48f2-155">**例**</span><span class="sxs-lookup"><span data-stu-id="b48f2-155">**Example**</span></span>

<span data-ttu-id="b48f2-156">次のタスクは、3 日間のうちの 18 時間（2018 年 12 月 3 日から 2018 年 12 月 5 日まで）を使用して自動スケジュールが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="b48f2-157">タスクが手動でスケジュールされた場合は、時間はすべての日付に対して均等に分配されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="b48f2-158">**例**</span><span class="sxs-lookup"><span data-stu-id="b48f2-158">**Example**</span></span>

<span data-ttu-id="b48f2-159">次のタスクは、3 日間のうちの 18 時間（2018 年 12 月 3 日から 2018 年 12 月 5 日まで）を使用して手動スケジュールが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="b48f2-160">割り当て単位</span><span class="sxs-lookup"><span data-stu-id="b48f2-160">Assignment unit</span></span>

<span data-ttu-id="b48f2-161">割り当て単位は  PSA 3.x では非推奨となっています。</span><span class="sxs-lookup"><span data-stu-id="b48f2-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="b48f2-162">タスク工数は、すべての割り当てられたリソース間で 1 日当たりで現在は等しく分割されています。</span><span class="sxs-lookup"><span data-stu-id="b48f2-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="b48f2-163">**例**</span><span class="sxs-lookup"><span data-stu-id="b48f2-163">**Example**</span></span>

<span data-ttu-id="b48f2-164">この例では、タスクは 2 つのリソースに割り当てられ、3 日間のうちの 36 時間（2018年12月3日から2018年12月5日まで）を使用して自動スケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="b48f2-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="b48f2-165">割り当て 1:</span><span class="sxs-lookup"><span data-stu-id="b48f2-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="b48f2-166">割り当て 2:</span><span class="sxs-lookup"><span data-stu-id="b48f2-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="b48f2-167">価格ディメンション</span><span class="sxs-lookup"><span data-stu-id="b48f2-167">Pricing dimensions</span></span>

<span data-ttu-id="b48f2-168">PSA 3.x では、リソース固有の価格ディメンションのフィールド ( **ロール** と **組織単位** など) は **msdyn\_projecttask** エンティティから削除されています。</span><span class="sxs-lookup"><span data-stu-id="b48f2-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="b48f2-169">これらのフィールドは、プロジェクト見積が生成された際に、リソース割り当て ( **msdyn\_resourceassignment** ) の対応するプロジェクト チーム メンバー ( **msdyn\_projectteam** ) から取得できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="b48f2-170">新規フィールドである、 **msdyn\_organizationalunit** が、 **msdyn\_projectteam** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="b48f2-171">msdyn\_projecttask (プロジェクト タスク) の非推奨のフィールド</span><span class="sxs-lookup"><span data-stu-id="b48f2-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="b48f2-172">代わり使用される、msdyn\_projectteam (プロジェクト チーム メンバー) からのフィールド</span><span class="sxs-lookup"><span data-stu-id="b48f2-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="b48f2-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b48f2-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="b48f2-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b48f2-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="b48f2-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="b48f2-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="b48f2-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="b48f2-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="b48f2-177">輪郭</span><span class="sxs-lookup"><span data-stu-id="b48f2-177">Contours</span></span>

<span data-ttu-id="b48f2-178">価格および見積もり輪郭フィールドは、 **msdyn\_projecttask** エンティティでは非推奨となりました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="b48f2-179">これらのフィールドは、 **msdyn\_resourceassignment** エンティティに移動されました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="b48f2-180">msdyn\_projecttask (プロジェクト タスク) の非推奨のフィールド</span><span class="sxs-lookup"><span data-stu-id="b48f2-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="b48f2-181">msdyn\_resourceassignment (リソース割り当て) の新しいフィールド</span><span class="sxs-lookup"><span data-stu-id="b48f2-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="b48f2-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="b48f2-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="b48f2-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="b48f2-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="b48f2-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="b48f2-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="b48f2-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="b48f2-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="b48f2-186">以下のフィールドは、 **msdyn\_resourceassignment** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="b48f2-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="b48f2-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b48f2-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="b48f2-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b48f2-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="b48f2-189">計画済み、実績、および残りのコストおよび売上に対する次のフィールドは、 **msdyn\_projecttask** エンティティでは変更されていません:</span><span class="sxs-lookup"><span data-stu-id="b48f2-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="b48f2-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b48f2-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="b48f2-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b48f2-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="b48f2-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="b48f2-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="b48f2-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="b48f2-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="b48f2-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b48f2-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="b48f2-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b48f2-195">msdyn\_remainingsales</span></span>
