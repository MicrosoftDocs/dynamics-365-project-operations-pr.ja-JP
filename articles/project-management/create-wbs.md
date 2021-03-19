---
title: WBS (作業分解構造) の作成
description: このトピックは、新しいスケジューリング インターフェイスの基本コントロールを含む WBS (作業分解構造) を作成する方法を説明しています。
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287019"
---
# <a name="create-a-work-breakdown-structure-wbs"></a><span data-ttu-id="8149a-103">WBS (作業分解構造) の作成</span><span class="sxs-lookup"><span data-stu-id="8149a-103">Create a work breakdown structure (WBS)</span></span>

<span data-ttu-id="8149a-104">プロジェクト スケジュールは、どの作業を完了する必要があるか、どのリソースが作業を実行するか、および作業を完了すべき時間枠を伝えます。</span><span class="sxs-lookup"><span data-stu-id="8149a-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe in which the work must be completed.</span></span> <span data-ttu-id="8149a-105">スケジュールは、プロジェクトを時間通りに提供することに関連したすべての作業を反映します。</span><span class="sxs-lookup"><span data-stu-id="8149a-105">The schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="8149a-106">Dynamics 365 Project Operations では、次の方法でプロジェクト スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="8149a-106">In Dynamics 365 Project Operations, you create a project schedule by:</span></span>

  - <span data-ttu-id="8149a-107">作業を管理可能なタスクに分割する。</span><span class="sxs-lookup"><span data-stu-id="8149a-107">Breaking the work down into manageable tasks.</span></span>
  - <span data-ttu-id="8149a-108">各タスクの実行に必要な時間を見積もる。</span><span class="sxs-lookup"><span data-stu-id="8149a-108">Estimating the time that is required to do each task.</span></span>
  - <span data-ttu-id="8149a-109">依存関係を設定する。</span><span class="sxs-lookup"><span data-stu-id="8149a-109">Setting task dependencies.</span></span>
  - <span data-ttu-id="8149a-110">タスク期間を設定する。</span><span class="sxs-lookup"><span data-stu-id="8149a-110">Setting task durations.</span></span>
  - <span data-ttu-id="8149a-111">タスクを実行する一般的なリソースを見積もる。</span><span class="sxs-lookup"><span data-stu-id="8149a-111">Estimating the generic resources that will do the tasks.</span></span> 

<span data-ttu-id="8149a-112">プロジェクト スケジュールは、**プロジェクト** ページの **スケジュール** タブで作成されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-112">The project schedule is created on the **Schedule** tab on the **Project** page.</span></span>

## <a name="tasks"></a><span data-ttu-id="8149a-113">タスク</span><span class="sxs-lookup"><span data-stu-id="8149a-113">Tasks</span></span>

<span data-ttu-id="8149a-114">プロジェクト スケジュールを作成するための最初のステップは、作業を管理可能な部分に分割することです。</span><span class="sxs-lookup"><span data-stu-id="8149a-114">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="8149a-115">Project Operations のスケジュールは次の機能をサポートしています:</span><span class="sxs-lookup"><span data-stu-id="8149a-115">The schedule in Project Operations supports the following features:</span></span>

- <span data-ttu-id="8149a-116">概要またはコンテナー タスク</span><span class="sxs-lookup"><span data-stu-id="8149a-116">Summary or container tasks</span></span>
- <span data-ttu-id="8149a-117">リーフ ノード タスク</span><span class="sxs-lookup"><span data-stu-id="8149a-117">Leaf node tasks</span></span>

### <a name="summary-tasks"></a><span data-ttu-id="8149a-118">概要タスク</span><span class="sxs-lookup"><span data-stu-id="8149a-118">Summary tasks</span></span>

<span data-ttu-id="8149a-119">概要タスクには、他の概要タスクまたはリーフノード タスクを保存できます。</span><span class="sxs-lookup"><span data-stu-id="8149a-119">Summary tasks can store other summary tasks or leaf node tasks.</span></span> <span data-ttu-id="8149a-120">それらのタスクには、作業負荷やコストはありません。</span><span class="sxs-lookup"><span data-stu-id="8149a-120">They have no work effort or cost of their own.</span></span> <span data-ttu-id="8149a-121">代わりに、作業負荷とコストは、コンテナー タスクの作業負荷とコストのロールアップです。</span><span class="sxs-lookup"><span data-stu-id="8149a-121">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="8149a-122">概要タスクの開始日は、コンテナー タスクの開始日であり、終了日はコンテナー タスクの終了日です。</span><span class="sxs-lookup"><span data-stu-id="8149a-122">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="8149a-123">概要タスクの名前は編集できますが、負荷、日付、期間などのスケジュール プロパティは編集できません。</span><span class="sxs-lookup"><span data-stu-id="8149a-123">The name of a summary task can be edited, but scheduling properties, including effort, dates, and duration, can't be edited.</span></span> <span data-ttu-id="8149a-124">概要タスクを削除すると、そのコンテナー タスクもすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-124">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="8149a-125">リーフ ノード タスク</span><span class="sxs-lookup"><span data-stu-id="8149a-125">Leaf node tasks</span></span>

<span data-ttu-id="8149a-126">リーフ ノード タスクは、プロジェクトで最も詳細な作業です。</span><span class="sxs-lookup"><span data-stu-id="8149a-126">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="8149a-127">予想される工数、リソース、計画された開始日および終了日、および期間があります。</span><span class="sxs-lookup"><span data-stu-id="8149a-127">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>

## <a name="create-a-task-hierarchy"></a><span data-ttu-id="8149a-128">タスク階層の作成</span><span class="sxs-lookup"><span data-stu-id="8149a-128">Create a task hierarchy</span></span>

### <a name="add-a-task"></a><span data-ttu-id="8149a-129">タスクの追加</span><span class="sxs-lookup"><span data-stu-id="8149a-129">Add a task</span></span>

<span data-ttu-id="8149a-130">次の手順を実行して 1 つ以上のタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="8149a-130">Complete the following steps to add one or more tasks.</span></span>

1. <span data-ttu-id="8149a-131">**プロジェクト** に移動して、スケジュールを作成するプロジェクト レコードを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="8149a-131">Go to **Projects** and select and open the project record for which you want to create a schedule.</span></span> 
2. <span data-ttu-id="8149a-132">**タスク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8149a-132">Select the **Tasks** tab.</span></span> 
3. <span data-ttu-id="8149a-133">**新しいタスクを追加する** を選択して、タスクの名前を入力し、Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8149a-133">Select **Add new task**, enter a name for the task, and then press Enter.</span></span>
2. <span data-ttu-id="8149a-134">別のタスク名を入力し、タスクの完全なリストが表示されるまでもう一度 Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8149a-134">Enter another task name and press Enter again until you have a full list of tasks.</span></span>

### <a name="manage-hierarchy-of-a-task"></a><span data-ttu-id="8149a-135">タスクの階層の管理</span><span class="sxs-lookup"><span data-stu-id="8149a-135">Manage hierarchy of a task</span></span>

<span data-ttu-id="8149a-136">タスクがインデントされると、そのすぐ上にあるタスクの子になります。</span><span class="sxs-lookup"><span data-stu-id="8149a-136">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="8149a-137">次に、タスクのスケジュール IDが再計算され、新しい親のスケジュール IDに基づいてアウトライン付番スキームに従います。</span><span class="sxs-lookup"><span data-stu-id="8149a-137">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="8149a-138">これで親タスクが概要タスクになりました。</span><span class="sxs-lookup"><span data-stu-id="8149a-138">The parent task is now a summary task.</span></span> <span data-ttu-id="8149a-139">したがって、その子タスクのロールアップになります。</span><span class="sxs-lookup"><span data-stu-id="8149a-139">Therefore, it becomes a rollup of its child tasks.</span></span> <span data-ttu-id="8149a-140">タスクがレベル上げされると、そのタスクはその親であったタスクの子ではなくなります。</span><span class="sxs-lookup"><span data-stu-id="8149a-140">When a task is promoted, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="8149a-141">スケジュール IDが再計算され、階層内のタスクの更新された深さと場所が反映されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-141">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="8149a-142">直前の親タスクの負荷、コスト、日付は再計算され、このタスクは含まれなくなります。</span><span class="sxs-lookup"><span data-stu-id="8149a-142">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

<span data-ttu-id="8149a-143">次の手順を実行してタスクをインデントまたはレベル上げします。</span><span class="sxs-lookup"><span data-stu-id="8149a-143">Complete the following steps to indent or promote a task.</span></span>

1. <span data-ttu-id="8149a-144">**プロジェクト** ページの **タスク** タブの **概要タスク** の下で、タスク名の脇にある 3 つの縦ドットを選択して **サブタスクの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8149a-144">On the **Project** page, on the **Tasks** tab, under **Summary tasks**, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 
2. <span data-ttu-id="8149a-145">インデントまたはレベル上げするタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="8149a-145">Select the task to indent or promote.</span></span> <span data-ttu-id="8149a-146">複数のタスクを選択する場合は、タスクを選択してから Ctrl キーを押しながらその他のタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="8149a-146">To select more than one task, select a task, press and hold Ctrl, and then select additional tasks.</span></span>
2. <span data-ttu-id="8149a-147">**インデント** または **サブタスクの昇格** を選択して、概要タスク下または外にタスクを移動します。</span><span class="sxs-lookup"><span data-stu-id="8149a-147">Select **Indent** or **Promote subtask**  to move tasks under or out from under summary tasks.</span></span>

### <a name="move-tasks-up-and-down"></a><span data-ttu-id="8149a-148">タスクを上下に動かす</span><span class="sxs-lookup"><span data-stu-id="8149a-148">Move tasks up and down</span></span>

<span data-ttu-id="8149a-149">タスクは、次の 2 つの方法のいずれかで、WBS (作業分解構造) の任意のレベルに移動できます。</span><span class="sxs-lookup"><span data-stu-id="8149a-149">Tasks can me moved to any level in the work breakdown structure in one of two ways:</span></span>

- <span data-ttu-id="8149a-150">1 つ以上のタスクを選択し、目的の場所にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="8149a-150">Select one more tasks and drag them to the desired location.</span></span>
- <span data-ttu-id="8149a-151">1 つ以上のタスクを選択し、右クリックして **切り取り** を選択し、スケジュールで移動先セルを選択し、右クリックして **ペースト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8149a-151">Select one or more tasks, right-click and select **Cut**, select the destination cell in the schedule, and then right-click and select **Paste**.</span></span>

## <a name="task-attributes"></a><span data-ttu-id="8149a-152">タスクの属性</span><span class="sxs-lookup"><span data-stu-id="8149a-152">Task attributes</span></span>

<span data-ttu-id="8149a-153">タスク名は完了しなければならない作業について説明しています。</span><span class="sxs-lookup"><span data-stu-id="8149a-153">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="8149a-154">Project Operationsでは、タスクに関連付けられた属性は、タスクのスケジュールおよびスタッフ要件を示します。</span><span class="sxs-lookup"><span data-stu-id="8149a-154">In Project Operations, the attributes associated with a task describe the schedule of the task and its staffing requirements.</span></span>

## <a name="schedule-attributes"></a><span data-ttu-id="8149a-155">スケジュール属性</span><span class="sxs-lookup"><span data-stu-id="8149a-155">Schedule attributes</span></span>

<span data-ttu-id="8149a-156">**負荷**、 **開始日**、 **終了日**、 **期間** の属性は、タスクのスケジュールを定義します。</span><span class="sxs-lookup"><span data-stu-id="8149a-156">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="8149a-157">次のテーブルは、追加のスケジュール属性を示しています。</span><span class="sxs-lookup"><span data-stu-id="8149a-157">The following table shows additional schedule attributes.</span></span>

| <span data-ttu-id="8149a-158">**最終表示名**</span><span class="sxs-lookup"><span data-stu-id="8149a-158">**Final display name**</span></span> | <span data-ttu-id="8149a-159">**最終説明**</span><span class="sxs-lookup"><span data-stu-id="8149a-159">**Final description**</span></span> |
| --- | --- |
| <span data-ttu-id="8149a-160">完了工数 (時間)</span><span class="sxs-lookup"><span data-stu-id="8149a-160">Effort Completed (Hours)</span></span> | <span data-ttu-id="8149a-161">タスクの完了した作業 (時間)。</span><span class="sxs-lookup"><span data-stu-id="8149a-161">Completed work for the task in hours.</span></span> |
| <span data-ttu-id="8149a-162">期間</span><span class="sxs-lookup"><span data-stu-id="8149a-162">Duration</span></span> | <span data-ttu-id="8149a-163">タスクの期間 (日数) を表示します。</span><span class="sxs-lookup"><span data-stu-id="8149a-163">Displays the duration in days for the task.</span></span> |
| <span data-ttu-id="8149a-164">工数の合計</span><span class="sxs-lookup"><span data-stu-id="8149a-164">Total Effort</span></span> | <span data-ttu-id="8149a-165">タスクの合計作業 (時間)。</span><span class="sxs-lookup"><span data-stu-id="8149a-165">Total work for the task in hours.</span></span> |
| <span data-ttu-id="8149a-166">完了</span><span class="sxs-lookup"><span data-stu-id="8149a-166">Finish</span></span> | <span data-ttu-id="8149a-167">完了日時。</span><span class="sxs-lookup"><span data-stu-id="8149a-167">Finish date and time.</span></span> |
| <span data-ttu-id="8149a-168">完了 (%)</span><span class="sxs-lookup"><span data-stu-id="8149a-168">% Complete</span></span> | <span data-ttu-id="8149a-169">完了したタスクの割合。</span><span class="sxs-lookup"><span data-stu-id="8149a-169">The percentage of the task that is complete.</span></span> |
| <span data-ttu-id="8149a-170">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="8149a-170">Project Bucket</span></span> | <span data-ttu-id="8149a-171">タスク ボードはバケットを使用してグループ化できるため、各バケットには固有の列があります。</span><span class="sxs-lookup"><span data-stu-id="8149a-171">The task board can be grouped by bucket so each bucket has its own column.</span></span> |
| <span data-ttu-id="8149a-172">残りの工数 (時間)</span><span class="sxs-lookup"><span data-stu-id="8149a-172">Effort Remaining (Hours)</span></span> | <span data-ttu-id="8149a-173">タスクの残りの作業 (時間)。</span><span class="sxs-lookup"><span data-stu-id="8149a-173">The remaining work for the task in hours.</span></span> |
| <span data-ttu-id="8149a-174">スタート画面</span><span class="sxs-lookup"><span data-stu-id="8149a-174">Start</span></span> | <span data-ttu-id="8149a-175">開始日時。</span><span class="sxs-lookup"><span data-stu-id="8149a-175">Start date and time.</span></span> |
| <span data-ttu-id="8149a-176">件名</span><span class="sxs-lookup"><span data-stu-id="8149a-176">Name</span></span> | <span data-ttu-id="8149a-177">タスクの名前。</span><span class="sxs-lookup"><span data-stu-id="8149a-177">The name of the task.</span></span> |
| <span data-ttu-id="8149a-178">ID</span><span class="sxs-lookup"><span data-stu-id="8149a-178">ID</span></span> | <span data-ttu-id="8149a-179">WBS (作業分解構造) のタスクの ID。</span><span class="sxs-lookup"><span data-stu-id="8149a-179">The ID of the task in the work breakdown structure.</span></span> |

<span data-ttu-id="8149a-180">管理者として、タスク エンティティでカスタム フィールドを定義できます。</span><span class="sxs-lookup"><span data-stu-id="8149a-180">As an administrator, you can define custom fields on the task entity.</span></span> <span data-ttu-id="8149a-181">ただし、フィールドをスケジュール グリッドに表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="8149a-181">However the fields can't be displayed on the schedule grid.</span></span> <span data-ttu-id="8149a-182">カスタム フィールドを表示するには、それらを **プロジェクト タスク** 詳細ページに追加します。</span><span class="sxs-lookup"><span data-stu-id="8149a-182">To see your custom fields, add them to the **Project Task** details page.</span></span>

## <a name="staffing-attributes"></a><span data-ttu-id="8149a-183">スタッフ属性</span><span class="sxs-lookup"><span data-stu-id="8149a-183">Staffing attributes</span></span>

<span data-ttu-id="8149a-184">スタッフの属性には、スケジュールの **リソース** フィールドからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8149a-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="8149a-185">既存のリソースを検索するか、 **作成** を選択して **簡易作成** ウィンドウで、新しいリソースとしてプロジェクト チーム メンバーを追加します。</span><span class="sxs-lookup"><span data-stu-id="8149a-185">You can either search for an existing resource, or select **Create**, and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="8149a-186">**ロール**、 **リソース単位**、 **ポジション名** フィールドは、タスクのスタッフ要件を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="8149a-187">これらのスタッフ属性とタスク スケジュールは、このタスクを実行するために使用可能なリソースを見つけるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-187">These staffing attributes, together with the task schedule are used to find available resources to do this task.</span></span>

   - <span data-ttu-id="8149a-188">**ロール**: タスクの実行に必要なリソースの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="8149a-188">**Role**: Specify the type of resource that is required to do the task.</span></span>
   - <span data-ttu-id="8149a-189">**リソース単位**: タスクのリソースの割り当て元となる単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="8149a-189">**Resourcing unit**: Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="8149a-190">リソースのコストと請求レートがリソース単位に基づいて設定されている場合、この属性はタスクのコストと売上予測に影響します。</span><span class="sxs-lookup"><span data-stu-id="8149a-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>
   - <span data-ttu-id="8149a-191">**ポジション名**: 最終的に、作業を実行するリソースのプレースホルダーとして機能する汎用リソースの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8149a-191">**Position name**: Enter a name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="8149a-192">**リソース** フィールドには、汎用リソースまたはそれが見つかる場合は名前付きリソースの位置名が格納されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="8149a-193">**カテゴリ** フィールドには、タスクをグループ化できるより幅広い作業の種類を示す値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="8149a-194">このフィールドは、スケジュールやスタッフには影響しません。</span><span class="sxs-lookup"><span data-stu-id="8149a-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="8149a-195">代わりに、このフィールドはレポートにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="8149a-195">Instead, the field is used only for reporting.</span></span>

## <a name="task-dependencies"></a><span data-ttu-id="8149a-196">タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="8149a-196">Task dependencies</span></span>

<span data-ttu-id="8149a-197">Project Operations のスケジュールを使用して、タスク間に先行オペレーション関係を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="8149a-197">You can use the schedule in Project Operations to create predecessor relationships between tasks.</span></span> <span data-ttu-id="8149a-198">**前のタスク** フィールドでは、タスクが依存するタスクを示す 1 つ以上の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8149a-198">The **Predecessor** field uses one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="8149a-199">タスクに先行オペレーション値が割り当てられている場合、そのタスクは、すべての先行オペレーション タスクが完了した後でのみ開始できます。</span><span class="sxs-lookup"><span data-stu-id="8149a-199">When predecessor values are assigned to a task, the task can start only after all of the predecessor tasks have been completed.</span></span> <span data-ttu-id="8149a-200">依存関係のため、タスクの計画された開始日は、先行オペレーション タスクが完了した日にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="8149a-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="8149a-201">タスク モードは、先行オペレーション/依存タスクの開始日と終了日に対して行われた更新には影響しません。</span><span class="sxs-lookup"><span data-stu-id="8149a-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="8149a-202">ユーザー補助およびキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="8149a-202">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="8149a-203">**スケジュール** グリッドは、完全にアクセスでき、ナレーター、JAWS、またはNVDAなどのスクリーン リーダーで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8149a-203">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="8149a-204">矢印キー (Microsoft Excel のように) を使用してグリッド領域内を移動したり、 Tab キーを使用して対話型ユーザー インターフェイス要素間を移動したり、下方向キー、Enter キー、または Space キーを使用して、ドロップダウン メニューを開く選択して開くことができます。</span><span class="sxs-lookup"><span data-stu-id="8149a-204">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive user interface elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and open the drop-down menus.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]