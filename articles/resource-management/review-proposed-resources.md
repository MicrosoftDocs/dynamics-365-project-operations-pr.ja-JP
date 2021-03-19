---
title: 提案されたリソースの確認
description: このトピックでは、プロジェクト リソースを提案する方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279279"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="0cc4e-103">提案されたリソースの確認</span><span class="sxs-lookup"><span data-stu-id="0cc4e-103">Review proposed resources</span></span>

<span data-ttu-id="0cc4e-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="0cc4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0cc4e-105">リソース マネージャーは、リソース要求を使用してプロジェクト マネージャーにリソースを提案できます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="0cc4e-106">その要求のグリッドまたは要求自体から、**リソースの検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="0cc4e-107">**アシスタントをスケジュール** ページで、リソースを選択した後、**リソース予約の作成** ウィンドウの、**予約状態** フィールドで、**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="0cc4e-108">次のステータス更新がおこなわれます:</span><span class="sxs-lookup"><span data-stu-id="0cc4e-108">The following status updates occur:</span></span>

- <span data-ttu-id="0cc4e-109">**スケジュール アシスタント** ページで、状態インジケーターが、予約が本予約ではなく、提案されたことを示すように更新されます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="0cc4e-110">リソース要求で、状態が **要レビュー** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="0cc4e-111">プロジェクトの **チーム** タブで、汎用チーム メンバーの **要求の状態** 値が **要確認** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="0cc4e-112">プロジェクト マネージャーは、提案を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="0cc4e-113">リソース マネージャーがプロセス リソースを処理する場合、以下のいずれかのアプローチを使用できます:</span><span class="sxs-lookup"><span data-stu-id="0cc4e-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="0cc4e-114">要求された時間を満たす単一のリソースがない場合、複数のリソースを提案します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="0cc4e-115">提案された時間はその後必須時間を満たすことができる複数のリソースで分割されます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="0cc4e-116">このシナリオでは、時間は重複しません。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="0cc4e-117">必要とされているよりも少ないリソースを提案します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="0cc4e-118">このシナリオでは、提案したリソースのキャパシティは、要求者が指定した必要とされる時間よりも少なくなります。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="0cc4e-119">したがって、要求者が提案されたリソースを受け入れる際、残りの要求を満たすために、未達成のリソース要件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="0cc4e-120">要求された業務を満たす単一のリソースがない場合、複数のリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="0cc4e-121">要求されたリソース数よりも少ないリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-121">Book fewer resources than are required.</span></span> <span data-ttu-id="0cc4e-122">このシナリオでは、予約された時間は要求された時間より少なくなります。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="0cc4e-123">システムはリソースの予約ではなく提案するようにガイドしますので、要求者は残りの要求の確認や追跡をおこなえます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="0cc4e-124">リソースの空き時間</span><span class="sxs-lookup"><span data-stu-id="0cc4e-124">Resource availability</span></span>

<span data-ttu-id="0cc4e-125">リソース マネージャーがリソースの空き時間を表示し、予約を更新することができることは必要不可欠です。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="0cc4e-126">場合によっては、正式な要求 (リソース要求) はありませんが、リソース マネージャーは、電子メール、電話、またはインスタント メッセージなどのチャンネルから来る予定外の要求に応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="0cc4e-127">リソース マネージャーはスケジュール ボードを使用して、リソースと予約を更新します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="0cc4e-128">リソースの作業時間は、リソースの空き時間を計算するための基本として使用されます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="0cc4e-129">リソースの予約は、リソースのキャパシティを消費します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="0cc4e-130">スケジュール ボードは、色と影を使用して、予約、空き時間、予約超過、さらに予約状況も表示します。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="0cc4e-131">スケジュール ボード設定の設定は凡例を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="0cc4e-132">スケジュール ボードの個々の予約可能リソースの横に右向きの矢印が表示されている場合は、そのリソースは予約された作業の詳細表示を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="0cc4e-133">Dynamics 365 Project Operations は Universal Resource Scheduling エンジンを使用していることから、Dynamics 365 Field Service がインストールされている場合は、プロジェクトの予約、作業指示書、スケジュールするために拡張したその他のエンティティの詳細を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="0cc4e-134">個々のリソースに関する詳細を表示するには、右クリックしてリソース カードを開きます。</span><span class="sxs-lookup"><span data-stu-id="0cc4e-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]