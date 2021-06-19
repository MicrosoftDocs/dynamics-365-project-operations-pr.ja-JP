---
title: 予約できるリソースがプロジェクトで複数のロールを満たす場合に、プロジェクトの売上とコストを見積もる
description: このトピックでは、価格ディメンションを使用してプロジェクトで複数のロールを満たすリソースの価格とコストをサポートできる方法に関する情報を提供します。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013267"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="32e1e-103">予約できるリソースがプロジェクトで複数のロールを満たす場合に、プロジェクトの売上とコストを見積もる</span><span class="sxs-lookup"><span data-stu-id="32e1e-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="32e1e-104">プロジェクト ベースの企業では、プロジェクトで 1 件のリソースによって複数のロールを実行する必要が頻繁にあります。</span><span class="sxs-lookup"><span data-stu-id="32e1e-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="32e1e-105">これらのロールのそれぞれは、プロジェクト上で同じリソースの時間が、各ロールの請求およびコスト レートに応じて異なる財務見積もりを取得することができることを意味し、価格とコストは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="32e1e-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="32e1e-106">Project Service Automation を使用すると、名前付きリソースのチーム メンバー レコードに値を設定でき、チーム メンバーが割り当てられている各タスクで異なる上書きを実行できます。</span><span class="sxs-lookup"><span data-stu-id="32e1e-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="32e1e-107">次の例では、この値を単純に単純に上書きすることで、コストと請求レートが異なるプロジェクトでリソースが複数のロールを持つことができるようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="32e1e-108">タスクの作成</span><span class="sxs-lookup"><span data-stu-id="32e1e-108">Create tasks</span></span>
<span data-ttu-id="32e1e-109">タスク A とタスク B の 2 つのプロジェクト タスクをそれぞれ 40 時間作成します。タスク B の先行タスクとしてタスク A を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="32e1e-110">汎用プロジェクト チーム メンバーのロールと組織単位を設定する</span><span class="sxs-lookup"><span data-stu-id="32e1e-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="32e1e-111">**スケジュール** ページでタスク A の **タスク** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="32e1e-112">**リソース** フィールドでドロップダウン リストから **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="32e1e-113">**チーム メンバーのクイック作成** ページで、このタスクを実行できる汎用チーム メンバーの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="32e1e-114">適切なロールと組織単位を選択してから **保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="32e1e-115">汎用チーム メンバーが作成され、このタスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="32e1e-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="32e1e-116">タスク B に対してこれらの手順を繰り返し、タスク B 用に作成された汎用チーム メンバーのロールと組織単位がタスク A と異なることを確認します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="32e1e-117">プロジェクト タスクのロールと組織単位を設定する</span><span class="sxs-lookup"><span data-stu-id="32e1e-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="32e1e-118">タスク A を作成したら、タスクを選択し、**タスクの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="32e1e-119">**タスクの詳細** ページで、**ロール** と **組織単位** フィールドを検索し、このタスクを実行するリソースに必要な値を追加します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="32e1e-120">Project Service Automation デモ データを使用してこのシナリオを完了する場合は、ロールには **コンサルティング リード** を、そして組織単位として **Fabrikam US** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="32e1e-121">タスク B を選択して、**タスクの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="32e1e-122">**タスクの詳細** ページで、**ロール** と **組織単位** フィールドを検索し、このタスクを実行するリソースに必要な値を追加します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="32e1e-123">**役割** と **組織単位** フィールドの値が、タスクBとタスクAで異なることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="32e1e-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="32e1e-124">Project Service Automation デモ データを使用してこのシナリオを完了する場合は、ロールには **ネットワーク技術者** を、そして組織単位として **Fabrikam US** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="32e1e-125">**タスクの詳細** ページを保存して、閉じます。</span><span class="sxs-lookup"><span data-stu-id="32e1e-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="32e1e-126">チーム メンバーと行動見積もり</span><span class="sxs-lookup"><span data-stu-id="32e1e-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="32e1e-127">**タスクの詳細** ページの **チーム メンバー** で 2 つの汎用チーム メンバーを選択してから、**要件の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="32e1e-128">**コンサルティング リード** のチーム メンバー行を選択し、**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="32e1e-129">スケジュール ボードが開き、その要件にリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="32e1e-130">**ネットワーク技術者** のチーム メンバー行を選択し、**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="32e1e-131">スケジュール ボードが開き、その要件に同じリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="32e1e-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="32e1e-132">チーム メンバー グリッド</span><span class="sxs-lookup"><span data-stu-id="32e1e-132">Team Member grid</span></span> 
<span data-ttu-id="32e1e-133">**チーム メンバー** グリッドで、2 つの汎用チーム メンバ レコードが削除され、1 つのリソースに置き換えられていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="32e1e-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="32e1e-134">そのリソースには、**ロール** と **組織単位** の既定の値のセットを示す値のセットが 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="32e1e-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="32e1e-135">そのチーム メンバー レコードの行を展開すると、これらのタスクの両方について、チーム メンバー レコードに個別の割り当てが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32e1e-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="32e1e-136">各割り当て行には、**ロール** と **組織単位** のタスク固有の値があります。</span><span class="sxs-lookup"><span data-stu-id="32e1e-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="32e1e-137">見積もり グリッド</span><span class="sxs-lookup"><span data-stu-id="32e1e-137">Estimates grid</span></span> 
<span data-ttu-id="32e1e-138">**見積り** グリッドに移動すると、同じリソースの両方の割り当ての価格が異なることがわかります。</span><span class="sxs-lookup"><span data-stu-id="32e1e-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="32e1e-139">タスク A のリソースの割り当ては、**コンサルティング リード** の **ロール** 属性値を使用して価格設定されます。</span><span class="sxs-lookup"><span data-stu-id="32e1e-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="32e1e-140">タスク B の同じリソースの割り当ては、**ネットワーク技術者** の **ロール** 属性値を使用して価格設定されます。</span><span class="sxs-lookup"><span data-stu-id="32e1e-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]