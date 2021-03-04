---
title: タスクにリソースを割り当てる
description: このトピックでは、タスクにリソースを割り当てる方法について説明します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149999"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="45a6f-103">タスクにリソースを割り当てる</span><span class="sxs-lookup"><span data-stu-id="45a6f-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="45a6f-104">Microsoft Dynamics 365 Project Service Automation には、リタスクにリソースを割り当てる 3つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="45a6f-105">リソースをチームのメンバーとして予約し、タスクにリソースを割り当てる</span><span class="sxs-lookup"><span data-stu-id="45a6f-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="45a6f-106">プロジェクトチームに対してリソースを追加してから、プロジェクトスケジュールでリソースをタスクへ割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="45a6f-107">**チーム メンバー** タブで、 **新規** を選択してチーム メンバーを追加します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="45a6f-108">**チーム メンバーのクイック作成** パネルが開きます。予約可能なリソース名を選択し、役割を設定できます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="45a6f-109">リソースを予約するには、以下の割り当て方法のいずれかを選択してください:</span><span class="sxs-lookup"><span data-stu-id="45a6f-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="45a6f-110">**全キャパシティ** は、指定されている開始日と終了日のリソースの全キャパシティを予約します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="45a6f-111">**キャパシティの割合** は、指定されている開始日と終了日のリソースのキャパシティの割合でリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="45a6f-112">**時間別 - 均等分布** は、指定された時間だけリソースを予約し、指定された開始日と終了日までの各日に均等に配分します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="45a6f-113">**時間別 - 前倒し** は、指定された開始日から終了日まで 1 日あたりの前倒し時間で、指定された時間数のリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="45a6f-114">**なし** は、チームに対してリソースを追加しますが、このキャパシティを吸収する予約は作成されません。</span><span class="sxs-lookup"><span data-stu-id="45a6f-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="45a6f-115">タスクの **スケジュール** グリッドの、リソースセルで **リソース** アイコンを選択し、 **チームメンバー** にて追加したチーム メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="45a6f-116">**チーム メンバー** タブと **調整** タブの両方で、リソースに予約された時間および割り当てられた時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="45a6f-117">時間は同じである必要がありますが、予約と割り当ては密接に結びついていないため、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="45a6f-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="45a6f-118">**調整** タブには、予約した時間よりも多くの時間をリソースに割り当てた場合など、リソースが異なる場合の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="45a6f-119">必要に応じて、リソースの登録を延長するか、割り当てを変更して、情報を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="45a6f-120">タスク割り当てを使用して汎用チーム メンバーを作成する</span><span class="sxs-lookup"><span data-stu-id="45a6f-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="45a6f-121">タスクの割り当てを使用して汎用チームメンバーを作成する場合は、そのタスクで最終的に作業するリソースの特性を表すプレースホルダまたは標準リソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="45a6f-122">その後、指定されたリソースの検索および予約に使用される要件を生成します (または要件を使用してリクエストを提出します)。</span><span class="sxs-lookup"><span data-stu-id="45a6f-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="45a6f-123">タスクの **スケジュール** グリッドで、 リソース セルの **リソース** アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="45a6f-124">プレースホルダー リソースの名前として使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="45a6f-125">例: プログラム マネージャー</span><span class="sxs-lookup"><span data-stu-id="45a6f-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="45a6f-126">**プロジェクトチームメンバーのクイック作成** フィールドにて **作成** を選択し、汎用リソースの役割を設定します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="45a6f-127">引き続きタスクの **リソース セレクタ** でリソースを選択することで、このプレースホルダー リソースへのタスクの割り当てをすることができます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="45a6f-128">**チーム メンバー** の配下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="45a6f-129">汎用リソースの割り当てが終了したら、 **チーム** タブの汎用リソースを選択し、 **要件の生成** を選択して汎用リソースのリソース要件を作成します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="45a6f-130">汎用リソースの **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="45a6f-131">次に、スケジュール ボードを使用して実際のリソースを検索して予約することができます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="45a6f-132">また、リソース マネージャーによって実行するための要件を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="45a6f-133">指定されたリソースによって汎用リソースが実行されると、汎用リソースがチームから削除され、汎用リソースのタスク割り当ては汎用リソースのリソース要件を実行したリソースに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="45a6f-134">すべての予約可能リソースの一覧から名前付きリソースを割り当てる</span><span class="sxs-lookup"><span data-stu-id="45a6f-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="45a6f-135">**リソースセレクタ** の検索ボックスを使用して、すべての予約可能リソースを検索し、タスクに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="45a6f-136">この方法で割り当てられたリソースは、予約なしでチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="45a6f-137">これは、チームメンバーを追加し、割り当ての方法として 「なし」 を選択するのと似ています。</span><span class="sxs-lookup"><span data-stu-id="45a6f-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="45a6f-138">このリソースは、 **チーム** タブと **調整** タブに、割り当てのみで予約不足のリソースとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="45a6f-139">可用性を使用する場合は、それらを予約します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="45a6f-140">タスクの **スケジュール** グリッドで、 リソース セルの **リソース** アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="45a6f-141">名前の入力を開始します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-141">Start typing a name.</span></span> <span data-ttu-id="45a6f-142">名前の検索結果は **その他リソース** 配下の **リソースセレクタ** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="45a6f-143">タスクに割り当てるリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-143">Select the resource that you want to assign to the task.</span></span>

