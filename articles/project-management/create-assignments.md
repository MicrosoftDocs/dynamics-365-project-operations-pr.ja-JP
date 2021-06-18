---
title: リソース割り当ての作成
description: このトピックでは、汎用および名前付きリソース割り当ての作成について説明します。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 610d9f7abbe7bc2eea8cc9a238dd7cfa1c626787
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006967"
---
# <a name="create-resource-assignments"></a><span data-ttu-id="5121a-103">リソース割り当ての作成</span><span class="sxs-lookup"><span data-stu-id="5121a-103">Create resource assignments</span></span>

<span data-ttu-id="5121a-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="5121a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5121a-105">リソース割り当ては、プロジェクト チーム メンバーをリーフ ノード タスクに直接関連付けることです。</span><span class="sxs-lookup"><span data-stu-id="5121a-105">A resource assignment is the direct association of a project team member to a leaf node task.</span></span> <span data-ttu-id="5121a-106">このトピックでは、リソースを割り当てるさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5121a-106">This topic provides information about the different ways to assign resources.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="5121a-107">タスク割り当てを使用して汎用チーム メンバーを作成する</span><span class="sxs-lookup"><span data-stu-id="5121a-107">Create a generic team member through task assignment</span></span>


<span data-ttu-id="5121a-108">タスクの割り当てを通じて汎用チーム メンバーを作成する場合、プレースホルダーまたは汎用リソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="5121a-108">When you create a generic team member through task assignment, you create a placeholder or generic resource.</span></span> <span data-ttu-id="5121a-109">この汎用リソースは、最終的にタスクで作業する名前付きリソースの特性について説明します。</span><span class="sxs-lookup"><span data-stu-id="5121a-109">This generic resource describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="5121a-110">次に、要件を生成するか、または名前付きリソースの検索および予約に使用されるリクエストを提出します。</span><span class="sxs-lookup"><span data-stu-id="5121a-110">You then generate a requirement, or submit a request using the requirement, that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="5121a-111">タスクのスケジュール グリッドで、**リソース** セルのリソース アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="5121a-111">On the Schedule grid for a task, select the Resource icon in the **Resource** cell.</span></span>
2. <span data-ttu-id="5121a-112">プレースホルダー リソースの名前として使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5121a-112">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="5121a-113">例: プログラム マネージャー</span><span class="sxs-lookup"><span data-stu-id="5121a-113">For example, Program Manager.</span></span>
3. <span data-ttu-id="5121a-114">**プロジェクトチームメンバーのクイック作成** フィールドにて **作成** を選択し、汎用リソースの役割を設定します。</span><span class="sxs-lookup"><span data-stu-id="5121a-114">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>
4. <span data-ttu-id="5121a-115">タスクの **リソース セレクタ** でリソースを選択することで、このプレースホルダー リソースへの必要なタスクを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5121a-115">Assign tasks as needed to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="5121a-116">リソースは **チーム メンバー** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5121a-116">The resources listed under **Team Members**.</span></span>
5. <span data-ttu-id="5121a-117">汎用リソースの割り当てが終了したら、**チーム** タブで汎用リソースを選択してから、**要件の生成** を選択して汎用リソースのリソース要件を作成します。</span><span class="sxs-lookup"><span data-stu-id="5121a-117">When you’re finished assigning the generic resource, on the **Team** tab, select the generic resource, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>
6. <span data-ttu-id="5121a-118">汎用リソースの **予約** を選択した後、実際のリソースの検索と予約にスケジュール ボードを使用します。</span><span class="sxs-lookup"><span data-stu-id="5121a-118">Select **Book** for the generic resource and then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="5121a-119">また、リソース マネージャーによって実行するための要件を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="5121a-119">You can also submit the requirement for fulfillment by a resource manager.</span></span>
7. <span data-ttu-id="5121a-120">汎用リソースが名前付きリソースで完全に満たされると (部分的なリソース要件の履行によってリソースが割り当てられることはありません)、汎用リソースはチームから削除されます。</span><span class="sxs-lookup"><span data-stu-id="5121a-120">When the generic resource is fully fulfilled (partial resource requirement fulfillment will not result in a resource assignment) with a named resource, the generic resource is removed from the team.</span></span> <span data-ttu-id="5121a-121">汎用リソースのタスク割り当ては、汎用リソースのリソース要件を満たした名前付きリソースに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5121a-121">The task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="5121a-122">すべての予約可能リソースの一覧から名前付きリソースを割り当てる</span><span class="sxs-lookup"><span data-stu-id="5121a-122">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="5121a-123">**リソース選択** の検索ボックスを使用して、すべての有効な予約可能リソースを検索し、リーフ ノード タスクに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5121a-123">You can use the search box in the **Resource Picker** to search all active bookable resources and assign them to any leaf node task.</span></span> <span data-ttu-id="5121a-124">この方法で割り当てられたリソースは、予約なしでチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5121a-124">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="5121a-125">これは、チームメンバーを追加し、割り当ての方法として **なし** を選択するのと似ています。</span><span class="sxs-lookup"><span data-stu-id="5121a-125">This is similar to adding a team member and selecting **None** as the allocation method.</span></span> <span data-ttu-id="5121a-126">このリソースは、**チーム**、**リソース割り当て**、および **調整** タブには、割り当てのみで予約不足のリソースとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="5121a-126">The resource is displayed on the **Team**, **Resource Assignment**, and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="5121a-127">可用性を使用する場合は、それらを予約します。</span><span class="sxs-lookup"><span data-stu-id="5121a-127">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="5121a-128">タスク グリッド、ボード、またはタイムラインから、**割り当て先** セルに移動します。</span><span class="sxs-lookup"><span data-stu-id="5121a-128">From the task grid, board, or timeline, navigate to the **Assigned To** cell.</span></span>
2. <span data-ttu-id="5121a-129">検索ボックスで、名前の入力を開始します。</span><span class="sxs-lookup"><span data-stu-id="5121a-129">In the search box, start typing a name.</span></span> <span data-ttu-id="5121a-130">名前の検索結果は **その他リソース** 配下の **リソースセレクタ** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5121a-130">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>
3. <span data-ttu-id="5121a-131">タスクに割り当てるリソースを選択するか、**その他のチーム リソース** にあるリソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="5121a-131">Select the resource that you want to assign to the task or select the name of the resource under **Other Team Resources**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]