---
title: 予約できるリソースがプロジェクトで複数のロールを満たす場合に、プロジェクトの売上とコストを見積もる
description: このトピックでは、プロジェクトで複数のロールを満たすリソースの価格とコストの見積もりを、価格ディメンションを使用してサポートする方法を説明します。
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531475"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a><span data-ttu-id="c01d9-103">予約できるリソースがプロジェクトで複数のロールを満たす場合に、プロジェクトの売上とコストを見積もる</span><span class="sxs-lookup"><span data-stu-id="c01d9-103">Estimate project sales and costs when a bookable resource fills multiple roles on a project</span></span> 

<span data-ttu-id="c01d9-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations、Lite 展開 - 見積もり請求の取引、在庫/製造ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c01d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, Project Operations for stocked/production-based scenarios_</span></span> 

<span data-ttu-id="c01d9-105">プロジェクト ベースの企業では、プロジェクトで 1 件のリソースによって複数のロールを満たす必要が頻繁にあります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-105">Project-based companies often have the need for one resource to fill multiple roles on a project.</span></span> <span data-ttu-id="c01d9-106">それぞれのロールで価格とコストが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-106">Each role can be priced and costed differently.</span></span> <span data-ttu-id="c01d9-107">これはつまり、プロジェクトの同じリソースの時間が、それぞれのロールの請求額と原価率に応じて異なる財務見積もりを取得する可能性があるということです。</span><span class="sxs-lookup"><span data-stu-id="c01d9-107">This means that the same resource's time on a project could get a different financial estimate depending on the bill and cost rates for each role.</span></span> <span data-ttu-id="c01d9-108">チーム メンバーを割り当てたタスクごとに異なるオーバーライドで、名前付きリソースのチーム メンバー レコードに値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-108">You can set up the values on the team member record for the named resource with different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="c01d9-109">次の例では、コストと請求レートが異なるプロジェクトで複数のロールを持つリソースを、値の単純なオーバーライドによって実現する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-109">The following example walks you through how the simple override of a value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="c01d9-110">タスクの作成</span><span class="sxs-lookup"><span data-stu-id="c01d9-110">Create tasks</span></span>
<span data-ttu-id="c01d9-111">タスクを作成する場合は、タスクと概要タスクを追加する必要があり、その後タスク期間を追加する前にタスクを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-111">To create tasks, you need to add tasks, as well as summary tasks, after which you need to assign the task before you add task duration.</span></span> 

### <a name="add-tasks-and-summary-tasks"></a><span data-ttu-id="c01d9-112">タスクと概要タスクを追加する</span><span class="sxs-lookup"><span data-stu-id="c01d9-112">Add tasks and summary tasks</span></span>
<span data-ttu-id="c01d9-113">タスクを追加する場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-113">To add a task, complete the following steps.</span></span>

1. <span data-ttu-id="c01d9-114">**プロジェクト** に移動してタスクを追加するプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-114">Go to **Projects** and open the project to which you want to add tasks.</span></span>
2. <span data-ttu-id="c01d9-115">**新しいタスクの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-115">Select **Add new task**.</span></span> <span data-ttu-id="c01d9-116">タスクに名前を付けて **Enter** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-116">Name the task, and then press **Enter**.</span></span>
3. <span data-ttu-id="c01d9-117">別のタスク名を入力して **Enter** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-117">Enter another task name and press **Enter**.</span></span> <span data-ttu-id="c01d9-118">これを完全なタスク一覧になるまで繰り返します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-118">Repeat this until you have a full list of tasks.</span></span>
3. <span data-ttu-id="c01d9-119">**概要** タスク配下のタスクをインデントする場合は、タスク名の脇にある 3 つの縦ドットを選択して **サブタスクの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-119">To indent tasks under **Summary** tasks, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 

  > [!TIP]
  > <span data-ttu-id="c01d9-120">複数のタスクを選択する場合は、タスクを選択してから **Ctrl** キーを押しながら別のタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-120">To select more than one task, select a task, press and hold **Ctrl**, and then select another task.</span></span>
  >
  > <span data-ttu-id="c01d9-121">**サブタスクの昇格** を選択して、**概要** タスク配下のタスクを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-121">You can also choose **Promote subtask** to move tasks out from under **Summary** tasks.</span></span>

### <a name="assign-tasks"></a><span data-ttu-id="c01d9-122">タスクの割り当て</span><span class="sxs-lookup"><span data-stu-id="c01d9-122">Assign tasks</span></span>

<span data-ttu-id="c01d9-123">タスクを割り当てる場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-123">Complete the following steps to assign tasks.</span></span>

1. <span data-ttu-id="c01d9-124">タスクの **割り当て先** 列で、人物アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-124">In the  **Assigned to**  column for a task, select the person icon.</span></span>
2. <span data-ttu-id="c01d9-125">一覧からチーム メンバーを選択するか、テキストを入力して名前を検索します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-125">Choose a team member from the list or enter text to search for a name.</span></span>

### <a name="add-task-duration-and-columns"></a><span data-ttu-id="c01d9-126">タスクの期間と列を追加する</span><span class="sxs-lookup"><span data-stu-id="c01d9-126">Add task duration and columns</span></span>

<span data-ttu-id="c01d9-127">多くの場合、プロジェクトの構築を期間を指定して開始するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="c01d9-127">It's often easiest to begin constructing your project with duration.</span></span> <span data-ttu-id="c01d9-128">次の手順を実行してタスクの期間を追加します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-128">Complete the following steps to add a task duration.</span></span>

1. <span data-ttu-id="c01d9-129">タスクの **期間** 列に、タスクの完了に必要と考えられる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-129">In the **Duration** column for a task, type the number of days you think it will take to accomplish the task.</span></span> <span data-ttu-id="c01d9-130">別の時間単位を使用する場合は、数値に加えて **時間**、**週間**、**か月間** などの単語を入力します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-130">If you want to use a different unit of time, enter a number plus the word **hours**, **weeks**, or **months**.</span></span>
2. <span data-ttu-id="c01d9-131">**タイムライン** ビューのひし形のマイルストーンとしてタスクを表示する場合は、**期間** 列に **0 日**  と入力します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-131">If you want your task to appear as a diamond-shaped milestone in the **Timeline** view, in the **Duration** column, enter **0 days** .</span></span>
3. <span data-ttu-id="c01d9-132">**Enter** キーを押して次のタスクの **期間** フィールドに移動し、期間の入力を続けます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-132">Press **Enter**  to go to the next task's **Duration** field and continue entering durations.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c01d9-133">概要タスクの期間を入力できません。</span><span class="sxs-lookup"><span data-stu-id="c01d9-133">You can't enter a duration for summary tasks.</span></span>

<span data-ttu-id="c01d9-134">プロジェクトに列を追加して詳細を提供できます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-134">You can add columns to your project to provide more details.</span></span> <span data-ttu-id="c01d9-135">これを行うには **列の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-135">To do this, select **Add column**.</span></span> 

<span data-ttu-id="c01d9-136">詳細については [プロジェクトの作成](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c01d9-136">For more information, see [Create a project](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).</span></span>

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="c01d9-137">一般的なプロジェクト チーム メンバーのロールと組織単位を設定します</span><span class="sxs-lookup"><span data-stu-id="c01d9-137">Set up the role and organization unit for a generic project team member</span></span>
<span data-ttu-id="c01d9-138">次の手順を実行して、一般的なチーム メンバーのロールと組織単位を設定します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-138">Complete the following steps to set up a role and organizational unit for a generic team member.</span></span>

1. <span data-ttu-id="c01d9-139">**タスク** ページで **タスク A** の **タスク** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-139">On the **Tasks** page, select the **Task** row for **Task A**.</span></span> 
2. <span data-ttu-id="c01d9-140">**割り当て先** で **一般的なリソースを追加する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-140">In **Assigned To**, select **Add generic resource**.</span></span> <span data-ttu-id="c01d9-141">これで **チーム メンバーの簡易作成** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-141">This opens the **Team Member Quick Create** page.</span></span>
3. <span data-ttu-id="c01d9-142">**チーム メンバーのクイック作成** ページで、このタスクを実行できる汎用チーム メンバーの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-142">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="c01d9-143">適切なロールと組織単位を選択してから **保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-143">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="c01d9-144">汎用チーム メンバーが作成され、このタスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-144">A generic team member is created and assigned to this task.</span></span> 
5. <span data-ttu-id="c01d9-145">**タスク B** に対して手順 1〜4 を繰り返します。ただし **タスク B** では **タスク A** と異なるロールと組織単位を一般のチームメンバーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-145">Repeat steps 1-4 for **Task B**. However, **Task B** must have a different role and organizational unit assigned for the generic team member than **Task A**.</span></span> 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="c01d9-146">プロジェクト タスクにロールと組織単位を設定する</span><span class="sxs-lookup"><span data-stu-id="c01d9-146">Set up the role and organization unit for a project task</span></span>
<span data-ttu-id="c01d9-147">次の手順を実行して、タスクにロールと組織単位を設定します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-147">Complete the following steps to set up a role and organizational unit for a task.</span></span>

1. <span data-ttu-id="c01d9-148">**タスク A** の作成後にこのタスクを選択し、**i** アイコンを選択して **タスクの詳細** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-148">After you create **Task A**, select the task, and then select the **i** icon to open the **Task Details** pane.</span></span> 
2. <span data-ttu-id="c01d9-149">**タスクの詳細** ウィンドウの一番下までスクロールし、**詳細の表示** を選択して **タスクの詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-149">On the **Task Details** pane, scroll to the bottom and select **View Details** to open the **Task Details** page.</span></span>
3. <span data-ttu-id="c01d9-150">**タスクの詳細** ページの **ロール** と **組織単位** で、このタスクの実行に必要な値をリソースに追加します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-150">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required to perform this task for the resource.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="c01d9-151">このシナリオを Project Operations のデモ データを使用して完了する場合は、ロールに **コンサルティング リード** を選択し、組織単位に **Fabrikam US** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-151">If you complete this scenario using the Project Operations demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

4. <span data-ttu-id="c01d9-152">**タスク B** を選択してから、このタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-152">Select **Task B**, and then select the task.</span></span>
5. <span data-ttu-id="c01d9-153">**i** アイコンを選択して **タスクの詳細** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-153">Select the **i** icon to open **Task Details** pane.</span></span> 
6. <span data-ttu-id="c01d9-154">**タスクの詳細** ウィンドウの一番下までスクロールし、**詳細の表示** を選択して **タスクの詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-154">On the **Task Details** pane, scroll to the bottom and select **View details** to open the **Task Details** page.</span></span>
7. <span data-ttu-id="c01d9-155">**タスクの詳細** ページの **ロール** と **組織単位** で、このタスクを実行するリソースに必要な値を追加します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-155">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="c01d9-156">**タスク B** の **ロール** と **組織単位** の値は、**タスク A** の値と異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-156">The values in **Role** and **Organizational Unit** for **Task B** must be different than those for **Task A**.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="c01d9-157">このシナリオを Project Operations のデモ データを使用して完了する場合は、ロールに **ネットワーク技術者** を選択し、組織単位に **Fabrikam US** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-157">If you complete this scenario using the Project Operations demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

8. <span data-ttu-id="c01d9-158">**タスクの詳細** ページを保存して、閉じます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-158">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="c01d9-159">チーム メンバーと行動見積もり</span><span class="sxs-lookup"><span data-stu-id="c01d9-159">Team member and estimates behavior</span></span> 
<span data-ttu-id="c01d9-160">**チーム メンバー** グリッドで行動を理解して見積もる場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-160">To understand the behavior on the **Team Member** grid and the estimates, complete the following steps.</span></span>

1. <span data-ttu-id="c01d9-161">**チーム メンバー** グリッドで、一般的なチーム メンバーを 2 人選択して **要件の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-161">On the **Team Member** grid, select the two generic team members, and then select **Generate Requirements**.</span></span> <span data-ttu-id="c01d9-162">これにより、リソース要件が生成されます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-162">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="c01d9-163">**コンサルティング リード** のチーム メンバー行を選択し、**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-163">Select the team member row for **Consulting Lead**, and then select **Book**.</span></span> <span data-ttu-id="c01d9-164">スケジュール ボードが開き、リソース一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-164">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="c01d9-165">リソースを選択してから **予約** を選択し、その要件に合ったリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-165">Select a resource and then select **Book** to book the resource to that requirement.</span></span>
3. <span data-ttu-id="c01d9-166">**ネットワーク技術者** のチーム メンバー行を選択し、**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-166">Select the team member row for **Network Technician**, and then select **Book**.</span></span> <span data-ttu-id="c01d9-167">スケジュール ボードが開き、リソース一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-167">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="c01d9-168">上記と同じリソースを選択して **予約** を選択し、その要件に合ったリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-168">Select the same resource as above and then select **Book** to book the resource to that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="c01d9-169">チーム メンバー グリッド</span><span class="sxs-lookup"><span data-stu-id="c01d9-169">Team Member grid</span></span> 

<span data-ttu-id="c01d9-170">**チーム メンバー** グリッドで一般的なチーム メンバー レコード 2 件を削除し、1 件のリソースのみに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-170">On the **Team Member** grid, the two generic team member records are deleted and replaced with only one resource.</span></span> <span data-ttu-id="c01d9-171">そのリソースには 1 セットの値があり、これは **ロール** と **組織単位** の値の既定セットです。</span><span class="sxs-lookup"><span data-stu-id="c01d9-171">There is one set of values for that resource, which are a default set of values for **Role** and **Organizational Unit**.</span></span>

<span data-ttu-id="c01d9-172">そのチーム メンバー レコード行を展開すると、両方のタスクのチーム メンバー レコードに個別の割り当てを表示します。</span><span class="sxs-lookup"><span data-stu-id="c01d9-172">When you expand the row for that team member record, you can see distinct assignments on the team member record for both tasks.</span></span> <span data-ttu-id="c01d9-173">各割り当て行には、**ロール** と **組織単位** のタスク固有の値があります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-173">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="c01d9-174">見積もり グリッド</span><span class="sxs-lookup"><span data-stu-id="c01d9-174">Estimates grid</span></span> 

<span data-ttu-id="c01d9-175">**見積り** グリッドにある同じリソースの両方の割り当ては、価格が異なります。</span><span class="sxs-lookup"><span data-stu-id="c01d9-175">On the **Estimates** grid, both assignments for the same resource are priced differently.</span></span> <span data-ttu-id="c01d9-176">**タスク A** のリソースの割り当ては、**コンサルティング リード** の **ロール** 属性値を使用して価格設定されます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-176">The assignment for the resource on **Task A** is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="c01d9-177">**タスク B** の同じリソースの割り当ては、**ネットワーク技術者** の **ロール** 属性値を使用して価格設定されます。</span><span class="sxs-lookup"><span data-stu-id="c01d9-177">The assignment for the same resource on **Task B** is priced using the **Role** attribute value of **Network Technician**.</span></span>
