---
title: 予約可能なリソースをウェブアプリケーションのタスクに割り当てる方法
description: 予約可能なリソースアサインする方法の概要。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286299"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="5d9dd-103">Web アプリ (Project Service アプリ v2.x) で予約可能なリソースをタスクに割り当てる方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5d9dd-104">Project Service には、リソースをタスクを割り当てる 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="5d9dd-105">リソースをチーム メンバーとして予約し、タスクにリソースを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="5d9dd-106">または、タスクでロールの割り当てを通じて汎用チーム メンバーを作成し、チームを生成した後、指定されたリソースを含むバッキング要件を実現できます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="5d9dd-107">タスクに予約可能リソースを割り当てる場合、予約可能リソース チームのメンバーに十分な予約が必要な点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="5d9dd-108">予約の状態は、[コミットの状態] が [本予約]、[状態] が [確定済み] でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="5d9dd-109">リソースに十分な予約がない場合、Project Service は割り当てを削除して、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="5d9dd-110">*リソースをタスクを割り当てることができません - 次のリソースにはプロジェクトで予約するための十分な時間がありません*</span><span class="sxs-lookup"><span data-stu-id="5d9dd-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="5d9dd-111">リソースをチーム メンバーとして予約し、タスクにリソースを割り当てる</span><span class="sxs-lookup"><span data-stu-id="5d9dd-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="5d9dd-112">この方法では、プロジェクト チームに対してリソースを追加してから、プロジェクト スケジュールでタスクをリソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="5d9dd-113">この方法は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="5d9dd-114">チーム メンバー グリッドで、**新規作成** を選択してチーム メンバーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="5d9dd-115">チーム メンバーのクイック作成画面で、予約可能なリソース名を選択し、ロールを設定します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="5d9dd-116">**開始** 日と **終了** 日を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="5d9dd-117">![チームメンバー追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-1.png "チームメンバー追加のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="5d9dd-118">リソースを予約する次の割り当て方法の 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="5d9dd-119">**全キャパシティ** は、指定されている開始日と終了日のリソースの全キャパシティを予約します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="5d9dd-120">**キャパシティの割合** は、指定されている開始日と終了日のリソースのキャパシティの割合でリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="5d9dd-121">**時間別 - 均等分布** は、指定された開始日から終了日まで 1 日あたりに等しく分散して、指定された時間数のリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="5d9dd-122">**時間別 - 前倒し** は、指定された開始日から終了日まで 1 日あたりの前倒し時間で、指定された時間数のリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="5d9dd-123">**なし** を選択しないでください。この方法は、チームにリソースを追加しますが、リソースのキャパシティを吸収する予約は作成しません。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="5d9dd-124">**保存** を選びます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-124">Select **Save**.</span></span>

    <span data-ttu-id="5d9dd-125">予約の時間数が、このリソースを割り当てるタスクの工数と日付範囲をカバーするのに十分であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="5d9dd-126">合っていない場合は、リソースをタスクに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="5d9dd-127">タスクの WBS (作業分解構造) で、リソース セル ドロップダウンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="5d9dd-128">次に、以下の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-128">Then:</span></span> 

    1. <span data-ttu-id="5d9dd-129">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-129">Select **Add**.</span></span>
    2. <span data-ttu-id="5d9dd-130">**リソース** の下でドロップダウンを選択し、上で追加したチーム メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="5d9dd-131">**OK** を選びます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-131">Select **OK**.</span></span> <span data-ttu-id="5d9dd-132">チーム メンバーがタスクに割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="5d9dd-133">![WBSを使用したリソース追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-2.png "WBSを使用したリソース追加のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="5d9dd-134">チーム メンバー グリッドの [割り当てられた時間] には、リソースの割り当てられた時間の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="5d9dd-135">これは、リソースに予約された時間以内の時間になります。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5d9dd-136">![リソースに割り当てられた時間のスクリーンショット](media/FAQ-Resources-to-Tasks2-3.png "リソースに割り当てられた時間のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="5d9dd-137">リソースに割り当てようとしているタスクがリソース予約の終了日より後に始まる場合、リソースはドロップダウンに表示されません。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="5d9dd-138">リソースに未割り当てのキャパシティがある場合、予約された時間より多くの時間をリソースに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="5d9dd-139">この場合、リソースの一部分のみその予約に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="5d9dd-140">WBS (作業分解構造) に [スタッフが配置されていない時間] を追加することで、このような残りの見割り当てタスクを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="5d9dd-141">リソースがその予約された時間に割り当てられた場合 (予約された時間は割り当てられた時間と等しい)、さらにタスクを割り当てようとすると次のようなエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="5d9dd-142">*リソースをタスクを割り当てることができません - 次のリソースにはプロジェクトで予約するための十分な時間がありません。*</span><span class="sxs-lookup"><span data-stu-id="5d9dd-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="5d9dd-143">また、プロジェクトを作成するときにチームに追加された既定のプロジェクト マネージャー プロジェクト チーム メンバーは予約なしで追加され、タスクに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="5d9dd-144">これらは、タスクのリソース ドロップダウンには表示されません。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="5d9dd-145">このリソースを割り当て場合、それらをチームから削除し、[なし] 以外の割り当て方法を使用して再追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="5d9dd-146">プロジェクトを作成するときにそれらがチームに追加される理由は、プロジェクトに少なくとも 1 人プロジェクト承認者が既定でいるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="5d9dd-147">タスクでのロール割り当てを通じた汎用チーム メンバーの作成</span><span class="sxs-lookup"><span data-stu-id="5d9dd-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="5d9dd-148">この方法では、リソースにタスクの予約が十分にあることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="5d9dd-149">まず、ロールをタスクに割り当てた後に生成することで、最終的にタスクで作業する指定したリソースの特性を示すプレースホルダーまたは汎用リソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="5d9dd-150">この方法は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="5d9dd-151">WBS (作業分解構造) で、タスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="5d9dd-152">リソース セルの **割り当てられたロール** ドロップダウン アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="5d9dd-153">**ロール** ドロップダウンを選択し、汎用リソースのロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="5d9dd-154">**OK** を選びます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="5d9dd-155">![WBSを使用したリソースの追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-4.png "WBSを使用したリソースの追加のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="5d9dd-156">WBS でタスクへロールの割り当てを完了したら、**プロジェクト チームの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="5d9dd-157">Project Service では、タスクの割り当てを集計することで、ロール、リソース組織単位、およびプロジェクトの予定表に基づいて汎用チーム メンバーの最小数が作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5d9dd-158">![プロジェクトチームの生成のスクリーンショット](media/FAQ-Resources-to-Tasks2-5.png "プロジェクトチームの生成のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="5d9dd-159">チーム メンバー グリッドでは、汎用リソースの種類のリソースが、ロールとポジション名と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="5d9dd-160">ロールが作業を完了するために 2 つのリソースが必要な場合、チームの生成機能は 2 名のチーム メンバーを作成し、ポジション名を使用してそれらを別々に設定します。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5d9dd-161">![2つの汎用リソース追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-6.png "2つの汎用リソース追加のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="5d9dd-162">リソース要件の下のリンクを選択すると、汎用チーム メンバーのバッキング リソース要件を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5d9dd-163">![関連するリソースの要件を起動するスクリーンショット](media/FAQ-Resources-to-Tasks2-7.png "関連するリソースの要件を起動するスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="5d9dd-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="5d9dd-164">汎用リソースの **予約** を選択した後、実質のリソースの検索と予約にスケジュール ボードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="5d9dd-165">また、**要求の送信** を選択することで、リソース マネージャーによって実行するための要件を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="5d9dd-166">指定されたリソースによって汎用リソースが実行されると、汎用リソースがチームから削除され、汎用リソースのタスク割り当ては汎用リソースのリソース要件を実行したリソースに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5d9dd-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]