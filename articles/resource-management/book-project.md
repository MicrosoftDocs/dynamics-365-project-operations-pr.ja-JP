---
title: プロジェクトの予約
description: このトピックでは、プロジェクトにリソースを予約する方法について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c87b0c32ef081f601ed79c11687f008bb454dd45
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131079"
---
# <a name="book-to-a-project"></a><span data-ttu-id="711a4-103">プロジェクトの予約</span><span class="sxs-lookup"><span data-stu-id="711a4-103">Book to a project</span></span>

<span data-ttu-id="711a4-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="711a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="711a4-105">プロジェクト マネージャーまたはリソース マネージャーが汎用チーム メンバーから特定の要件を定義せずに、プロジェクトにリソースを割り当てることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="711a4-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="711a4-106">これは、3 つの方法で実現できます。</span><span class="sxs-lookup"><span data-stu-id="711a4-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="711a4-107">チーム メンバー グリッドから予約</span><span class="sxs-lookup"><span data-stu-id="711a4-107">Book from the team member grid</span></span>
- <span data-ttu-id="711a4-108">スケジュール ボードから予約</span><span class="sxs-lookup"><span data-stu-id="711a4-108">Book from the schedule board</span></span>
- <span data-ttu-id="711a4-109">**プロジェクト** フォームから予約</span><span class="sxs-lookup"><span data-stu-id="711a4-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="711a4-110">チーム メンバー グリッドから予約</span><span class="sxs-lookup"><span data-stu-id="711a4-110">Book from the team member grid</span></span>

<span data-ttu-id="711a4-111">組織がハイブリッド リソース割り当てモードで運用している場合、プロジェクト マネージャーは、次の手順を実行することにより、プロジェクトにリソースを直接予約できます。</span><span class="sxs-lookup"><span data-stu-id="711a4-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="711a4-112">プロジェクトから、チーム メンバー グリッドに移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="711a4-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="711a4-113">ポジション名とリソースのロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="711a4-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="711a4-114">利用可能な検索から予約可能リソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="711a4-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="711a4-115">リソースを選択した後、次のフィールド情報を定義してリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="711a4-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="711a4-116">開始日</span><span class="sxs-lookup"><span data-stu-id="711a4-116">Start date</span></span>
    - <span data-ttu-id="711a4-117">終了日</span><span class="sxs-lookup"><span data-stu-id="711a4-117">Finish date</span></span>
    - <span data-ttu-id="711a4-118">割り当て方法</span><span class="sxs-lookup"><span data-stu-id="711a4-118">Allocation method</span></span>
    - <span data-ttu-id="711a4-119">時間 (該当する場合)</span><span class="sxs-lookup"><span data-stu-id="711a4-119">Hours, if applicable</span></span>
    - <span data-ttu-id="711a4-120">プロジェクト承認者</span><span class="sxs-lookup"><span data-stu-id="711a4-120">Project approver</span></span>

6. <span data-ttu-id="711a4-121">**保存して閉じる** を選択する</span><span class="sxs-lookup"><span data-stu-id="711a4-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="711a4-122">スケジュール ボードから予約</span><span class="sxs-lookup"><span data-stu-id="711a4-122">Book from the schedule board</span></span>

<span data-ttu-id="711a4-123">リソース マネージャーがリソースをプロジェクトに直接予約する必要がある場合、スケジュール ボードとプロジェクト要件を使用できます。</span><span class="sxs-lookup"><span data-stu-id="711a4-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="711a4-124">プロジェクト要件は、いつでも予約可能なリソース要件です。</span><span class="sxs-lookup"><span data-stu-id="711a4-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="711a4-125">スケジュール ボードからプロジェクトに直接予約を行うには、以下の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="711a4-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="711a4-126">スケジュールボードに移動し、左側のページで、要件について検討しているリソースをフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="711a4-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="711a4-127">下のペインで、**事業** タブをクリックして、プロジェクト要件のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="711a4-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="711a4-128">要件をリソースにドラッグし、次の情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="711a4-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="711a4-129">開始日</span><span class="sxs-lookup"><span data-stu-id="711a4-129">Start date</span></span>
    - <span data-ttu-id="711a4-130">終了日</span><span class="sxs-lookup"><span data-stu-id="711a4-130">Finish date</span></span>
    - <span data-ttu-id="711a4-131">予約状態</span><span class="sxs-lookup"><span data-stu-id="711a4-131">Booking status</span></span>
    - <span data-ttu-id="711a4-132">予約方法</span><span class="sxs-lookup"><span data-stu-id="711a4-132">Booking method</span></span>
    - <span data-ttu-id="711a4-133">時間</span><span class="sxs-lookup"><span data-stu-id="711a4-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="711a4-134">プロジェクト フォームから予約する</span><span class="sxs-lookup"><span data-stu-id="711a4-134">Book from the Project form</span></span>

<span data-ttu-id="711a4-135">プロジェクト マネージャーとして、プロジェクトにリソースを予約する必要があるかもしれませんが、リソースの名前ではなくて条件だけを知っているかもしれません。</span><span class="sxs-lookup"><span data-stu-id="711a4-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="711a4-136">スケジュール アシスタントを使用して、リソースの使用可能な属性に基づいてリソースを検索するには、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="711a4-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="711a4-137">プロジェクトに移動して、**予約** を選択し、スケジュール アシスタントを開きます。</span><span class="sxs-lookup"><span data-stu-id="711a4-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="711a4-138">スケジュール アシスタントの左側にあるフィルターを使用して、条件を絞り込み、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="711a4-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="711a4-139">結果で返されたリソースに基づいて、リソースを予約できます。</span><span class="sxs-lookup"><span data-stu-id="711a4-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="711a4-140">この方法では、任意のリソースの予約は作成されません。</span><span class="sxs-lookup"><span data-stu-id="711a4-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="711a4-141">代わりに、リソースがチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="711a4-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="711a4-142">チーム メンバーがプロジェクトに追加された後、プロジェクト マネージャーは、予約の維持または予約の延長を使用して、必要な予約をリソースに追加できます。</span><span class="sxs-lookup"><span data-stu-id="711a4-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
