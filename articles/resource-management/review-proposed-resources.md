---
title: 提案されたリソースの確認
description: このトピックでは、プロジェクト リソースを提案する方法について説明します。
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000757"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="8f40c-103">提案されたリソースの確認</span><span class="sxs-lookup"><span data-stu-id="8f40c-103">Review proposed resources</span></span>

<span data-ttu-id="8f40c-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="8f40c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f40c-105">リソース マネージャーは、リソース要求を使用してプロジェクト マネージャーにリソースを提案できます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="8f40c-106">その要求のグリッドまたは要求自体から、**リソースの検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="8f40c-107">**アシスタントをスケジュール** ページで、リソースを選択した後、**リソース予約の作成** ウィンドウの、**予約状態** フィールドで、**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="8f40c-108">次のようなステータスの更新が発生します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-108">The following status updates occur:</span></span>

- <span data-ttu-id="8f40c-109">**スケジュール アシスタント** ページでステータス インジケーターが更新され、予約が「本予約」ではなく「提案」と表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="8f40c-110">リソース要求で、ステータスが **レビューが必要** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="8f40c-111">プロジェクトの **チーム** タブで、汎用チーム メンバーの **要求の状態** 値が **要確認** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="8f40c-112">プロジェクト マネージャーは、提案を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="8f40c-113">リソース マネージャーがプロセス リソースを処理する場合、以下のいずれかのアプローチを使用できます:</span><span class="sxs-lookup"><span data-stu-id="8f40c-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="8f40c-114">要求された時間を満たす単一のリソースがない場合、複数のリソースを提案します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="8f40c-115">提案された時間はその後必須時間を満たすことができる複数のリソースで分割されます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="8f40c-116">このシナリオでは、時間は重複しません。</span><span class="sxs-lookup"><span data-stu-id="8f40c-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="8f40c-117">必要とされているよりも少ないリソースを提案します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="8f40c-118">このシナリオでは、提案したリソースのキャパシティは、要求者が指定した必要とされる時間よりも少なくなります。</span><span class="sxs-lookup"><span data-stu-id="8f40c-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="8f40c-119">したがって、要求者が提案されたリソースを受け入れる際、残りの要求を満たすために、未達成のリソース要件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="8f40c-120">要求された業務を満たす単一のリソースがない場合、複数のリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="8f40c-121">要求されたリソース数よりも少ないリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-121">Book fewer resources than are required.</span></span> <span data-ttu-id="8f40c-122">このシナリオでは、予約された時間は要求された時間より少なくなります。</span><span class="sxs-lookup"><span data-stu-id="8f40c-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="8f40c-123">システムはリソースの予約ではなく提案するようにガイドしますので、要求者は残りの要求の確認や追跡をおこなえます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="8f40c-124">リソースの空き時間</span><span class="sxs-lookup"><span data-stu-id="8f40c-124">Resource availability</span></span>

<span data-ttu-id="8f40c-125">リソース マネージャーがリソースの空き時間を表示し、予約を更新することができることは必要不可欠です。</span><span class="sxs-lookup"><span data-stu-id="8f40c-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="8f40c-126">場合によっては、正式な要求 (リソース要求) はありませんが、リソース マネージャーは、電子メール、電話、またはインスタント メッセージなどのチャンネルから来る予定外の要求に応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f40c-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="8f40c-127">リソース マネージャーはスケジュール ボードを使用して、リソースと予約を更新します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="8f40c-128">リソースの作業時間は、リソースの空き時間を計算するための基本として使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="8f40c-129">リソースの予約は、リソースのキャパシティを消費します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="8f40c-130">スケジュール ボードは、色と影を使用して、予約、空き時間、予約超過、さらに予約状況も表示します。</span><span class="sxs-lookup"><span data-stu-id="8f40c-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="8f40c-131">スケジュール ボード設定の設定は凡例を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="8f40c-132">スケジュール ボードの個々の予約可能リソースの横に右向きの矢印が表示されている場合は、そのリソースは予約された作業の詳細表示を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="8f40c-133">Dynamics 365 Project Operations は Universal Resource Scheduling エンジンを使用していることから、Dynamics 365 Field Service がインストールされている場合は、プロジェクトの予約、作業指示書、スケジュールするために拡張したその他のエンティティの詳細を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="8f40c-134">個々のリソースに関する詳細を表示するには、右クリックしてリソース カードを開きます。</span><span class="sxs-lookup"><span data-stu-id="8f40c-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]