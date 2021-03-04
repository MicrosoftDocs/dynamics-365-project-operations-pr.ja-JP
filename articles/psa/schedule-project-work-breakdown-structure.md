---
title: 作業分解構造でプロジェクトをスケジュールする
description: Project Service での WBS (作業分解構造) でプロジェクトをスケジュールする方法
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149819"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="fb787-103">WBS (作業分解構造) でプロジェクトをスケジュールする (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fb787-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fb787-104">プロジェクト スケジュールは、どの作業を実行する必要があるか、どのリソースにより作業が実行されるか、および作業を完了する必要がある時間枠とやり取りします。</span><span class="sxs-lookup"><span data-stu-id="fb787-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="fb787-105">プロジェクト スケジュールは、プロジェクトを時間通りに提供することに関連したすべての作業を反映します。</span><span class="sxs-lookup"><span data-stu-id="fb787-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="fb787-106">プロジェクトの開始ステージの最初のステップの 1 つは、プロジェクトのスケジュールを考えることです。</span><span class="sxs-lookup"><span data-stu-id="fb787-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="fb787-107">プロジェクト スケジュールを確立するには、作業分解構造を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb787-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="fb787-108">作業分解構造を使用してプロジェクト構造を作成します。これは以下の訳に立ちます。</span><span class="sxs-lookup"><span data-stu-id="fb787-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="fb787-109">作業を管理可能なタスクに分割</span><span class="sxs-lookup"><span data-stu-id="fb787-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="fb787-110">タスクを完了するために必要な時間の推定</span><span class="sxs-lookup"><span data-stu-id="fb787-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="fb787-111">タスク依存関係およびタスク期間の設定</span><span class="sxs-lookup"><span data-stu-id="fb787-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="fb787-112">各タスクを完了するために必要なロールの決定</span><span class="sxs-lookup"><span data-stu-id="fb787-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="fb787-113">作業分解構造のプロジェクト スケジュールの外見は見慣れた、対話型ガント チャートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="fb787-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="fb787-114">プロジェクト用作業分解構造の作成</span><span class="sxs-lookup"><span data-stu-id="fb787-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="fb787-115">プロジェクトの一連のタスクを示す作業分解構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb787-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="fb787-116">作業分解構造には、タスク、各タスクの要件、および売り上げとコストの情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb787-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="fb787-117">作業分解構造に、以下のものを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="fb787-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="fb787-118">階層内のタスクの順序</span><span class="sxs-lookup"><span data-stu-id="fb787-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="fb787-119">他のタスクがある場合、タスク開始前に完了する必要があります</span><span class="sxs-lookup"><span data-stu-id="fb787-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="fb787-120">タスクの開始日、終了日、および期間</span><span class="sxs-lookup"><span data-stu-id="fb787-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="fb787-121">タスクに必要な時間数</span><span class="sxs-lookup"><span data-stu-id="fb787-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="fb787-122">必要な作業者のスキルおよび教育</span><span class="sxs-lookup"><span data-stu-id="fb787-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="fb787-123">タスクに割り当てられている作業者</span><span class="sxs-lookup"><span data-stu-id="fb787-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="fb787-124">予想される売上とコスト</span><span class="sxs-lookup"><span data-stu-id="fb787-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="fb787-125">タスクの種類</span><span class="sxs-lookup"><span data-stu-id="fb787-125">Task types</span></span>  
<span data-ttu-id="fb787-126">作業分解構造を作成するとき、以下の種類のタスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb787-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="fb787-127">**プロジェクトのルート ノード**。</span><span class="sxs-lookup"><span data-stu-id="fb787-127">**Project root node**</span></span> | <span data-ttu-id="fb787-128">プロジェクトのトップレベルの概要タスク。</span><span class="sxs-lookup"><span data-stu-id="fb787-128">The top-level summary task for the project.</span></span> <span data-ttu-id="fb787-129">他のすべてのプロジェクト タスクはその下に作成されます。</span><span class="sxs-lookup"><span data-stu-id="fb787-129">All other project tasks are created under it.</span></span> <span data-ttu-id="fb787-130">ルート タスクの名前はプロジェクト名です。</span><span class="sxs-lookup"><span data-stu-id="fb787-130">The name of the root task is the project name.</span></span> <span data-ttu-id="fb787-131">ルート ノードの負荷、日付、および期間は、その下の階層の値に基づきます。</span><span class="sxs-lookup"><span data-stu-id="fb787-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="fb787-132">ルート ノードのプロパティを編集したり、ルート ノードを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="fb787-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="fb787-133">**概要またはコンテナー タスク**</span><span class="sxs-lookup"><span data-stu-id="fb787-133">**Summary or container tasks**</span></span> | <span data-ttu-id="fb787-134">概要タスクは、その下にサブタスクがあるタスクです。</span><span class="sxs-lookup"><span data-stu-id="fb787-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="fb787-135">概要タスクには、それ自身の作業負荷またはコストがありません。</span><span class="sxs-lookup"><span data-stu-id="fb787-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="fb787-136">その作業負荷およびコストは、そのサブタスクのロールアップです。</span><span class="sxs-lookup"><span data-stu-id="fb787-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="fb787-137">概要タスクの名前は変更することができますが、負荷、日付、または期間は自動的に計算されるため、これらを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="fb787-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="fb787-138">概要タスクを削除すると、そのタスクおよびすべてのサブタスクが削除されます。</span><span class="sxs-lookup"><span data-stu-id="fb787-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="fb787-139">**リーフ ノード タスク**</span><span class="sxs-lookup"><span data-stu-id="fb787-139">**Leaf node tasks**</span></span> | <span data-ttu-id="fb787-140">リーフ ノード タスクはプロジェクトで最も詳細な作業です。</span><span class="sxs-lookup"><span data-stu-id="fb787-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="fb787-141">予測負荷、計画されたリソース数、計画された開始日および終了日、および期間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb787-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="fb787-142">タスク階層</span><span class="sxs-lookup"><span data-stu-id="fb787-142">Task hierarchy</span></span>  
 <span data-ttu-id="fb787-143">タスク階層を作成するとき、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="fb787-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="fb787-144">**タスクの追加**。</span><span class="sxs-lookup"><span data-stu-id="fb787-144">**Add task**.</span></span>   <span data-ttu-id="fb787-145">タスク階層内で選択した場所にタスクを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="fb787-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="fb787-146">場所を選択しない場合、新しいタスクは最後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb787-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="fb787-147">**インデント タスク**。</span><span class="sxs-lookup"><span data-stu-id="fb787-147">**Indent task**.</span></span>   <span data-ttu-id="fb787-148">タスクをインデントし、そのすぐ上のタスクの子にします。</span><span class="sxs-lookup"><span data-stu-id="fb787-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="fb787-149">**インデントを戻すタスク**。</span><span class="sxs-lookup"><span data-stu-id="fb787-149">**Outdent task**.</span></span>   <span data-ttu-id="fb787-150">タスクのインデントを戻し、元の親タスクのサブタスクではなくなります。</span><span class="sxs-lookup"><span data-stu-id="fb787-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="fb787-151">**上へ移動および下へ移動**。</span><span class="sxs-lookup"><span data-stu-id="fb787-151">**Move up and Move down**.</span></span>   <span data-ttu-id="fb787-152">タスクを親タスクの階層の上下に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb787-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="fb787-153">タスクの上下移動は、負荷、コスト、日付、または期間に影響しません。</span><span class="sxs-lookup"><span data-stu-id="fb787-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="fb787-154">タスクの属性</span><span class="sxs-lookup"><span data-stu-id="fb787-154">Task attributes</span></span>  
 <span data-ttu-id="fb787-155">タスク名は完了する必要がある作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb787-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="fb787-156">様々なタスク属性を使用して、タスクのスケジュールおよびスタッフ要件を説明します。</span><span class="sxs-lookup"><span data-stu-id="fb787-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="fb787-157">スケジュール属性</span><span class="sxs-lookup"><span data-stu-id="fb787-157">Schedule attributes</span></span>

 - <span data-ttu-id="fb787-158">値に **行動時間**、**リソースの数**、**開始日**、**終了日**、および **期間** を割り当て、タスクのスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb787-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="fb787-159">**行動** はタスクを完了するためにかかる予測時間です。</span><span class="sxs-lookup"><span data-stu-id="fb787-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="fb787-160">**リソースの数** はプロジェクト管理者が可能な限り最善のスケジュールを考えるために役立つ、タスクに投入できる見積です。</span><span class="sxs-lookup"><span data-stu-id="fb787-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="fb787-161">**期間** (日数) はタスクを完了するためにかかる作業日数を示します。</span><span class="sxs-lookup"><span data-stu-id="fb787-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="fb787-162">スタッフ属性</span><span class="sxs-lookup"><span data-stu-id="fb787-162">Staffing attributes</span></span>

 - <span data-ttu-id="fb787-163">**ロール**、**リソースの組織単位**、**リソースの数**、および **リソース** は、タスクのスタッフ要件を説明します。</span><span class="sxs-lookup"><span data-stu-id="fb787-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="fb787-164">**ロール** はタスクを実行するために必要なリソースの種類について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb787-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="fb787-165">**リソースの組織単位** は、タスクにスタッフを送るリソースの組織単位を示します。また、これはリソースの出荷単位販売価格を決定するときに考慮されるため、タスクのコストおよび営業の見積もりが影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="fb787-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="fb787-166">**リソース** には汎用リソース、またはそれが見つかる場合は名前付きリソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb787-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="fb787-167">タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="fb787-167">Task dependencies</span></span>  
 <span data-ttu-id="fb787-168">作業分解構造内の 1 つ以上のタスク間に、先行オペレーション関係を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="fb787-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="fb787-169">タスクの先行オペレーション フィールドに 1 つ以上の値をセットし、従属関係にあるタスクを示します。</span><span class="sxs-lookup"><span data-stu-id="fb787-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="fb787-170">タスクに先行オペレーション値を割り当てると、そのタスクは、すべての先行オペレーション タスクが完了したときにのみ開始することができます。</span><span class="sxs-lookup"><span data-stu-id="fb787-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="fb787-171">タスクにこの先行オペレーションを設定すると、タスクの計画された開始日が、その先行オペレーションすべての最後の終了日として再計算されます。</span><span class="sxs-lookup"><span data-stu-id="fb787-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="fb787-172">スケジュール上で先行オペレーションが関係する影響は、タスクで定義されたタスク モードにより制限されません。</span><span class="sxs-lookup"><span data-stu-id="fb787-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="fb787-173">タスク モード</span><span class="sxs-lookup"><span data-stu-id="fb787-173">Task mode</span></span>  
 <span data-ttu-id="fb787-174">タスク モードは、リーフ モード タスクのスケジュールを決定する重要な要素の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="fb787-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="fb787-175">すべてのタスクには、自動スケジュール モードと手動スケジュール モードの 2 つのタスク モードがあります。</span><span class="sxs-lookup"><span data-stu-id="fb787-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="fb787-176">**自動スケジュール設定**。</span><span class="sxs-lookup"><span data-stu-id="fb787-176">**Auto scheduling**.</span></span>   <span data-ttu-id="fb787-177">タスク モードを自動的にスケジュール済みにセットするとき、タスクスケジュール設定エンジンは、次のタスク属性上のスケジュール設定ルールを使用してタスクのスケジュールを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb787-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="fb787-178">前のタスク</span><span class="sxs-lookup"><span data-stu-id="fb787-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="fb787-179">工数</span><span class="sxs-lookup"><span data-stu-id="fb787-179">Effort</span></span>  
  
    -   <span data-ttu-id="fb787-180">リソースの数</span><span class="sxs-lookup"><span data-stu-id="fb787-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="fb787-181">開始日と終了日。</span><span class="sxs-lookup"><span data-stu-id="fb787-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="fb787-182">**スケジュール ルール**。</span><span class="sxs-lookup"><span data-stu-id="fb787-182">**Scheduling rules**.</span></span>   <span data-ttu-id="fb787-183">先行オペレーションを持たないリーフ ノード タスクの開始日が、既定のプロジェクトのスケジュール開始日になります。</span><span class="sxs-lookup"><span data-stu-id="fb787-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="fb787-184">リーフ ノード タスクの期間は、常に開始日および終了日の間の作業日日数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="fb787-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="fb787-185">タスクが自動的にスケジュールされる場合、スケジュール エンジンは次のルールに従います。</span><span class="sxs-lookup"><span data-stu-id="fb787-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="fb787-186">タスクの開始日と終了日は、常にプロジェクトのスケジュール カレンダーに従う作業日です</span><span class="sxs-lookup"><span data-stu-id="fb787-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="fb787-187">先行オペレーションがあるタスクの開始日は、既定の、その先行オペレーションの最後の終了日となります</span><span class="sxs-lookup"><span data-stu-id="fb787-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="fb787-188">負荷 = 人数 \* 期間 \* プロジェクト カレンダーの標準作業日内の時間</span><span class="sxs-lookup"><span data-stu-id="fb787-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="fb787-189">**手動スケジュール**。</span><span class="sxs-lookup"><span data-stu-id="fb787-189">**Manual scheduling**.</span></span>   <span data-ttu-id="fb787-190">一部のケースでは、これらの値からそれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb787-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="fb787-191">これらの場合、手動スケジュール設定のタスクにタスク モードをセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="fb787-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="fb787-192">これにより、スケジュール エンジンは他のスケジュール属性の値の計算を停止します。</span><span class="sxs-lookup"><span data-stu-id="fb787-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="fb787-193">タスクに先行オペレーションを設定すると、従属タスクの開始日に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="fb787-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="fb787-194">作業分解構造の作成</span><span class="sxs-lookup"><span data-stu-id="fb787-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="fb787-195">**Project Service > プロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb787-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="fb787-196">作業対象のプロジェクトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb787-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="fb787-197">画面上部のバーで、プロジェクト名の隣の下矢印を選択してから、[作業分解構造] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb787-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="fb787-198">タスクを追加するには、**タスクの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb787-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="fb787-199">タスクのフィールドに記入してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb787-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="fb787-200">作業分解構造が完了するまでタスクの追加を継続します。</span><span class="sxs-lookup"><span data-stu-id="fb787-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="fb787-201">作業分解構造の作成中、タスクを整理するために以下の内容を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="fb787-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="fb787-202">タスクを選択して、**インデント** をクリックしてそれを別のタスクの下に移動するか、[インデントを戻す] をクリックして元のレベルに戻します。</span><span class="sxs-lookup"><span data-stu-id="fb787-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="fb787-203">タスクを選択し、**上へ移動** または **下へ移動** をクリックして、リストの上下に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb787-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="fb787-204">**ガントの非表示** をクリックしてガント チャートを非表示にし、**ガントの表示** をクリックして再び表示します。</span><span class="sxs-lookup"><span data-stu-id="fb787-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="fb787-205">ガント チャートの別の期間を **タイム スケール** で選択します。</span><span class="sxs-lookup"><span data-stu-id="fb787-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="fb787-206">作業分解構造で指定したロールをプロジェクトのチーム メンバーに追加するには、**プロジェクト チームの生成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb787-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="fb787-207">変更が完了したら、画面の右下隅にある **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb787-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fb787-208">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb787-208">See Also</span></span>  
 [<span data-ttu-id="fb787-209">プロジェクト管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="fb787-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
