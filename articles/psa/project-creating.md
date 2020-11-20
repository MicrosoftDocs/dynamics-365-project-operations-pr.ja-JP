---
title: プロジェクト スケジュール
description: このトピックでは、スケジュールの作成方法に関する情報を提供します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bad7a8712057b60d202c37cc75ea68bf04fd4cc9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123247"
---
# <a name="project-schedules"></a><span data-ttu-id="d49a4-103">プロジェクト スケジュール</span><span class="sxs-lookup"><span data-stu-id="d49a4-103">Project schedules</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d49a4-104">プロジェクト スケジュールは、どの作業を完了する必要があるか、どのリソースが作業を実行するか、および作業を完了する必要がある時間枠とやり取りします。</span><span class="sxs-lookup"><span data-stu-id="d49a4-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="d49a4-105">これは、プロジェクトを時間通りに提供することに関連したすべての作業を反映します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="d49a4-106">Dynamics 365 Project Service Automation では、作業を管理可能なタスクに分割し、各タスクの実行に必要な時間を見積もり、タスクの依存関係を設定し、タスクの期間を設定し、タスクを実行する汎用リソースを見積もり、プロジェクト スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="d49a4-107">プロジェクト スケジュールは、プロジェクト ページの **スケジュール** タブで作成します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="d49a4-108">仕事</span><span class="sxs-lookup"><span data-stu-id="d49a4-108">Tasks</span></span>

<span data-ttu-id="d49a4-109">プロジェクト スケジュールを作成するための最初のステップは、作業を管理可能な部分に分割することです。</span><span class="sxs-lookup"><span data-stu-id="d49a4-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="d49a4-110">PSAのスケジュールは次の機能をサポートしています:</span><span class="sxs-lookup"><span data-stu-id="d49a4-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="d49a4-111">プロジェクトのルート ノード。</span><span class="sxs-lookup"><span data-stu-id="d49a4-111">Project root node</span></span>
- <span data-ttu-id="d49a4-112">概要またはコンテナー タスク</span><span class="sxs-lookup"><span data-stu-id="d49a4-112">Summary or container tasks</span></span>
- <span data-ttu-id="d49a4-113">リーフ ノード タスク</span><span class="sxs-lookup"><span data-stu-id="d49a4-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="d49a4-114">プロジェクトのルート ノード。</span><span class="sxs-lookup"><span data-stu-id="d49a4-114">Project root node</span></span>

<span data-ttu-id="d49a4-115">プロジェクト ルート ノードは、プロジェクトの最上位概要タスクです。</span><span class="sxs-lookup"><span data-stu-id="d49a4-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="d49a4-116">他のすべてのプロジェクト タスクはその下に作成されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-116">All other project tasks are created under it.</span></span> <span data-ttu-id="d49a4-117">ルート ノードの名前は常に、プロジェクト名に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="d49a4-118">ルート ノードの負荷、日付、および期間は、その下の階層の値に基づいて集約されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="d49a4-119">ルート ノードのプロパテは編集できません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="d49a4-120">ルート ノードを削除することもできません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="d49a4-121">概要またはコンテナー タスク</span><span class="sxs-lookup"><span data-stu-id="d49a4-121">Summary or container tasks</span></span> 

<span data-ttu-id="d49a4-122">概要タスクには、サブタスクまたはコンテナー タスクがあります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="d49a4-123">それらのタスクには、作業負荷やコストはありません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="d49a4-124">代わりに、作業負荷とコストは、コンテナー タスクの作業負荷とコストのロールアップです。</span><span class="sxs-lookup"><span data-stu-id="d49a4-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="d49a4-125">概要タスクの開始日は、コンテナー タスクの開始日であり、終了日はコンテナー タスクの終了日です。</span><span class="sxs-lookup"><span data-stu-id="d49a4-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="d49a4-126">概要タスクの名前は編集できますが、スケジュール プロパティ (負荷、日付、期間) は編集できません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="d49a4-127">概要タスクを削除すると、そのコンテナー タスクもすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="d49a4-128">リーフ ノード タスク</span><span class="sxs-lookup"><span data-stu-id="d49a4-128">Leaf node tasks</span></span>

<span data-ttu-id="d49a4-129">リーフ ノード タスクは、プロジェクトで最も詳細な作業です。</span><span class="sxs-lookup"><span data-stu-id="d49a4-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="d49a4-130">予想される工数、リソース、計画された開始日および終了日、および期間があります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="d49a4-131">タスク階層の作成</span><span class="sxs-lookup"><span data-stu-id="d49a4-131">Creating a task hierarchy</span></span>

<span data-ttu-id="d49a4-132">次のオプションを使用して、タスク階層を作成できます:</span><span class="sxs-lookup"><span data-stu-id="d49a4-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="d49a4-133">**タスクの追加** ボタン</span><span class="sxs-lookup"><span data-stu-id="d49a4-133">**Add task** button</span></span>
- <span data-ttu-id="d49a4-134">**インデント タスク** ボタン</span><span class="sxs-lookup"><span data-stu-id="d49a4-134">**Indent task** button</span></span>
- <span data-ttu-id="d49a4-135">**インデントを戻すタスク** ボタン</span><span class="sxs-lookup"><span data-stu-id="d49a4-135">**Outdent task** button</span></span>
- <span data-ttu-id="d49a4-136">**上へ移動** および **下へ移動** ボタン</span><span class="sxs-lookup"><span data-stu-id="d49a4-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="d49a4-137">ユーザー補助およびキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="d49a4-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="d49a4-138">タスクの追加</span><span class="sxs-lookup"><span data-stu-id="d49a4-138">Add task</span></span>

<span data-ttu-id="d49a4-139">**タスクの追加** ボタンを使用すると、階層内に新しいタスクを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="d49a4-140">場所を選択しない場合、タスクは最後に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="d49a4-141">スケジュール IDは、すべてのタスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="d49a4-142">スケジュール IDは、階層内のタスクの深さと場所を表します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="d49a4-143">アウトライン番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-143">It uses outline numbering.</span></span> <span data-ttu-id="d49a4-144">プロジェクト ルート ノードの下の第 1 レベルのタスクでは、 1, 2, 3 などの付番スキームが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="d49a4-145">第 1 レベルのタスクでは、 1.1, 1.2, 1.3 などの付番スキームが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="d49a4-146">インデント タスク</span><span class="sxs-lookup"><span data-stu-id="d49a4-146">Indent task</span></span>

<span data-ttu-id="d49a4-147">タスクがインデントされると、そのすぐ上にあるタスクの子になります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="d49a4-148">次に、タスクのスケジュール IDが再計算され、新しい親のスケジュール IDに基づいてアウトライン付番スキームに従います。</span><span class="sxs-lookup"><span data-stu-id="d49a4-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="d49a4-149">これで、親タスクはサマリー タスクまたはコンテナー タスクになります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="d49a4-150">したがって、その子タスクのロールアップになります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="d49a4-151">インデントを戻すタスク</span><span class="sxs-lookup"><span data-stu-id="d49a4-151">Outdent task</span></span> 

<span data-ttu-id="d49a4-152">タスクがインデントを戻すと、そのタスクはその親であったタスクの子ではなくなります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="d49a4-153">スケジュール IDが再計算され、階層内のタスクの更新された深さと場所が反映されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="d49a4-154">直前の親タスクの負荷、コスト、日付は再計算され、このタスクは含まれなくなります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="d49a4-155">上へ移動、下へ移動</span><span class="sxs-lookup"><span data-stu-id="d49a4-155">Move up and Move down</span></span> 

<span data-ttu-id="d49a4-156">**上へ移動** および **下へ移動** ボタンは、親階層内のタスクの場所を変更します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="d49a4-157">この種類の変更は、タスクの負荷、コスト、日付、または期間に影響しません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="d49a4-158">タスクのスケジュール IDのみが、影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="d49a4-159">スケジュール IDが再計算され、子タスクの親リスト内でのタスクの新しい場所が反映されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="d49a4-160">ユーザー補助およびキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="d49a4-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="d49a4-161">**スケジュール** グリッドは、完全にアクセスでき、ナレーター、JAWS、またはNVDAなどのスクリーン リーダーで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="d49a4-162">矢印キー (Microsoft Excel のように) を使用してグリッド領域内を移動したり、 Tab キーを使用して対話型UI要素間を移動したり、下方向キー、Enter キー、または Space キーを使用して、ドロップダウン メニュー選択して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="d49a4-163">列見出しも対話型です。</span><span class="sxs-lookup"><span data-stu-id="d49a4-163">The column headers are also interactive.</span></span> <span data-ttu-id="d49a4-164">列の表示と非表示を切り替えたり、Tab キーと矢印キーを使用して列見出しを移動したり、ツール バーのアクション ボタンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="d49a4-165">さらに、次のショートカット キーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="d49a4-166">**更新**: ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="d49a4-166">**Refresh**: ALT+SHIFT+F5</span></span>
- <span data-ttu-id="d49a4-167">**追加**: ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="d49a4-167">**Add**: ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="d49a4-168">**削除**: ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="d49a4-168">**Delete**: ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="d49a4-169">**上/下へ移動**: ALT+SHIFT+上下矢印</span><span class="sxs-lookup"><span data-stu-id="d49a4-169">**Move up/down**: ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="d49a4-170">**インデント/インデントを戻す**: ALT_SHIFT+左または右矢印</span><span class="sxs-lookup"><span data-stu-id="d49a4-170">**Indent/Outdent**: ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="d49a4-171">**階層の展開/折りたたみ**: ALT+SHIFT+ +/- キー</span><span class="sxs-lookup"><span data-stu-id="d49a4-171">**Expand/Collapse Hierarchies**: ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="d49a4-172">タスクの属性</span><span class="sxs-lookup"><span data-stu-id="d49a4-172">Task attributes</span></span>

<span data-ttu-id="d49a4-173">タスク名は完了しなければならない作業について説明しています。</span><span class="sxs-lookup"><span data-stu-id="d49a4-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="d49a4-174">PSAでは、タスクに関連付けられた属性は、タスクのスケジュールおよびスタッフ要件を示します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![タスクの属性](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="d49a4-176">スケジュール属性</span><span class="sxs-lookup"><span data-stu-id="d49a4-176">Schedule attributes</span></span>

<span data-ttu-id="d49a4-177">**負荷**、 **開始日**、 **終了日**、 **期間** の属性は、タスクのスケジュールを定義します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-177">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="d49a4-178">追加のスケジュール属性には次のものが含まれます:</span><span class="sxs-lookup"><span data-stu-id="d49a4-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="d49a4-179">**工数**: タスクを完了するために必要な時間の見積を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-179">**Effort hours**: Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="d49a4-180">**期間**: タスクを完了するために必要な作業日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-180">**Duration**: Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="d49a4-181">**スケジュール ID**: この自動生成された IDは、階層内のタスクの順序付けに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-181">**Schedule ID**: This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="d49a4-182">タスク間の依存関係によって、タスクが処理される実際の受注を管理します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="d49a4-183">スタッフ属性</span><span class="sxs-lookup"><span data-stu-id="d49a4-183">Staffing attributes</span></span>

<span data-ttu-id="d49a4-184">スタッフの属性には、スケジュールの **リソース** フィールドからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d49a4-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="d49a4-185">既存のリソースを検索するか、 **作成** をクリックして **簡易作成** ウィンドウで、新しいリソースとしてプロジェクト チーム メンバーを追加します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="d49a4-186">**ロール**、 **リソース単位**、 **ポジション名** フィールドは、タスクのスタッフ要件を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="d49a4-187">これらのスタッフ属性とタスク スケジュールは、このタスクを実行するために使用可能なリソースを見つけるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="d49a4-188">**ロール** - タスクの実行に必要なリソースの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="d49a4-189">**リソース単位** - タスクのリソースの割り当て元となる単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="d49a4-190">リソースのコストと請求レートがリソース単位に基づいて設定されている場合、この属性はタスクのコストと売上予測に影響します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="d49a4-191">**ポジション名** – 最終的に、作業を実行するリソースのプレースホルダーとして機能する汎用リソースのフレンドリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="d49a4-192">**リソース** フィールドには、汎用リソースまたはそれが見つかる場合は名前付きリソースの位置名が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="d49a4-193">**カテゴリ** フィールドには、タスクをグループ化できるより幅広い作業の種類を示す値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="d49a4-194">このフィールドは、スケジュールやスタッフには影響しません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="d49a4-195">レポートにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="d49a4-196">タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="d49a4-196">Task dependencies</span></span> 

<span data-ttu-id="d49a4-197">PSAのスケジュールを使用して、タスク間に先行オペレーション関係を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="d49a4-198">**タスク** の **前のタスク** フィールドは、タスクが依存するタスクを示す 1 つ以上の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="d49a4-199">タスクに先行オペレーション値が割り当てられている場合、そのタスクは、すべての先行オペレーション タスクが完了した後でのみ開始できます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="d49a4-200">依存関係のため、タスクの計画された開始日は、先行オペレーション タスクが完了した日にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="d49a4-201">タスク モードは、先行オペレーション/依存タスクの開始日と終了日に対して行われた更新には影響しません。</span><span class="sxs-lookup"><span data-stu-id="d49a4-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="d49a4-202">タスク モード</span><span class="sxs-lookup"><span data-stu-id="d49a4-202">Task mode</span></span> 

<span data-ttu-id="d49a4-203">タスク モードは、リーフ ノード タスクのスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="d49a4-204">PSAは、すべてのタスクで、自動スケジュールと手動スケジュールの 2 つのタスク モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d49a4-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="d49a4-205">自動スケジュール</span><span class="sxs-lookup"><span data-stu-id="d49a4-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="d49a4-206">タスク モードがタスクの **自動的にスケジュール済み** に設定されている場合、タスク スケジュール設定エンジンは、タスク属性上のスケジュール設定ルールを使用してタスクのスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="d49a4-207">スケジュール ルール</span><span class="sxs-lookup"><span data-stu-id="d49a4-207">Scheduling rules</span></span>

<span data-ttu-id="d49a4-208">既定では、リーフ ノード タスクが先行オペレーションを持たない場合、その開始日はプロジェクトのスケジュールされた開始日に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="d49a4-209">リーフ ノード タスクの期間は、常に開始日および終了日の間の作業日日数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="d49a4-210">タスクが自動的にスケジュールされる場合、スケジュール エンジンは次のルールに従います:</span><span class="sxs-lookup"><span data-stu-id="d49a4-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="d49a4-211">プロジェクトのスケジュール カレンダーに従って、タスクの開始日と終了日は、稼働日にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d49a4-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="d49a4-212">先行オペレーション タスクの場合、開始日はその先行オペレーションの最終終了日に自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="d49a4-213">負荷は、数式を使用して計算されます: 人数 × 期間 × プロジェクト カレンダーの標準稼働日の時間数。</span><span class="sxs-lookup"><span data-stu-id="d49a4-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="d49a4-214">手動スケジュール</span><span class="sxs-lookup"><span data-stu-id="d49a4-214">Manual scheduling</span></span>

<span data-ttu-id="d49a4-215">自動スケジュールのルールが要件を満たしていない場合、タスクのタスク モードを **手動でスケジュール済み** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d49a4-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="d49a4-216">この設定は、スケジュール エンジンは他のスケジュール属性の値の計算を停止します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="d49a4-217">タスク モードに関係なく、タスクに前のタスクを設定すると、常に依存タスクの開始日に影響します。</span><span class="sxs-lookup"><span data-stu-id="d49a4-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>
