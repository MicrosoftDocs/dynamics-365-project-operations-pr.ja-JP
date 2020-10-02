---
title: 提案されたリソースの確認
description: このトピックでは、プロジェクト リソースを提案する方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897367"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="4b898-103">提案されたリソースの確認</span><span class="sxs-lookup"><span data-stu-id="4b898-103">Review proposed resources</span></span>

<span data-ttu-id="4b898-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="4b898-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b898-105">リソース マネージャーは、リソース要求を使用してプロジェクト マネージャーにリソースを提案できます。</span><span class="sxs-lookup"><span data-stu-id="4b898-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="4b898-106">その要求のグリッドまたは要求自体から、**リソースの検索**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b898-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="4b898-107">**アシスタントをスケジュール**ページで、リソースを選択した後、**リソース予約の作成**ウィンドウの、**予約状態**フィールドで、**予約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b898-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="4b898-108">次のステータス更新がおこなわれます:</span><span class="sxs-lookup"><span data-stu-id="4b898-108">The following status updates occur:</span></span>

- <span data-ttu-id="4b898-109">**スケジュール アシスタント**ページで、状態インジケーターが、予約が本予約ではなく、提案されたことを示すように更新されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="4b898-110">リソース要求で、状態が **要レビュー**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="4b898-111">プロジェクトの**チーム**タブで、汎用チーム メンバーの**要求の状態**値が**要確認**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="4b898-112">プロジェクト マネージャーは、提案を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="4b898-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="4b898-113">リソース マネージャーがプロセス リソースを処理する場合、以下のいずれかのアプローチを使用できます:</span><span class="sxs-lookup"><span data-stu-id="4b898-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="4b898-114">必要とされる時間を履行するために使用可能なリソースが 1 つもない場合は、要求を満たすために複数のリソースを提案します。</span><span class="sxs-lookup"><span data-stu-id="4b898-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="4b898-115">提案された時間はその後必須時間を満たすことができる複数のリソースで分割されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="4b898-116">このシナリオでは、時間は重複しません。</span><span class="sxs-lookup"><span data-stu-id="4b898-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="4b898-117">必要とされているよりも少ないリソースを提案します。</span><span class="sxs-lookup"><span data-stu-id="4b898-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="4b898-118">このシナリオでは、提案したリソースのキャパシティは、要求者が指定した必要とされる時間よりも少なくなります。</span><span class="sxs-lookup"><span data-stu-id="4b898-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="4b898-119">したがって、要求者が提案されたリソースを承諾した場合、残りの要求をキャプチャするために履行されていないリソース要件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="4b898-120">作業を完了するために使用可能なリソースが 1 つもない場合は、その要求を満たすために複数のリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="4b898-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="4b898-121">必要とされているよりも少ないリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="4b898-121">Book fewer resources than are required.</span></span> <span data-ttu-id="4b898-122">このシナリオで、予約された時間は、必要とされる時間よりも少なくなります。</span><span class="sxs-lookup"><span data-stu-id="4b898-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="4b898-123">システムはリソースの予約ではなく提案するようにガイドしますので、要求者は残りの要求の確認や追跡をおこなえます。</span><span class="sxs-lookup"><span data-stu-id="4b898-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="4b898-124">請求可能な稼働率</span><span class="sxs-lookup"><span data-stu-id="4b898-124">Billable utilization</span></span>

<span data-ttu-id="4b898-125">リソースは支払請求可能な目標稼働率を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4b898-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="4b898-126">この目標稼働率は、リソースの規定ロールの属性として定義されるか、個々の予約可能なリソースのレコードで設定されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="4b898-127">稼働率計算は、リソースが承認された時間エントリを使用して報告した実際の時間に基づいています。</span><span class="sxs-lookup"><span data-stu-id="4b898-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="4b898-128">次の計算式を使用して稼働率を計算します:</span><span class="sxs-lookup"><span data-stu-id="4b898-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="4b898-129">支払請求可能な稼働率 = 課金対象となる実際の時間 ÷ リソースのキャパシティ</span><span class="sxs-lookup"><span data-stu-id="4b898-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="4b898-130">支払請求不可な稼働率 = 請求タイプ ID を持つ実際の時間 = 非課金対象、補助、利用不可 ÷ リソースのキャパシティ</span><span class="sxs-lookup"><span data-stu-id="4b898-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="4b898-131">内部 = 営業契約なしの実際の時間 ÷ リソースのキャパシティ</span><span class="sxs-lookup"><span data-stu-id="4b898-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="4b898-132">リソースのキャパシティ = リソースの作業時間 – 不在 – 非作業日</span><span class="sxs-lookup"><span data-stu-id="4b898-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="4b898-133">**リソース**ウィンドウの**リソース稼働率**ビューがあります。</span><span class="sxs-lookup"><span data-stu-id="4b898-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="4b898-134">グリッド内の各セルは、日、週、または月などの期間でのリソースの支払請求可能な稼働率パーセントを表します。</span><span class="sxs-lookup"><span data-stu-id="4b898-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="4b898-135">セルの色付けには次の計算式が使用されます:</span><span class="sxs-lookup"><span data-stu-id="4b898-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="4b898-136">**緑:** 支払請求可能な稼働率 \>= リソースの目標稼働率</span><span class="sxs-lookup"><span data-stu-id="4b898-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="4b898-137">**黄色:** 目標稼働率 – 20 \<= 支払請求可能な稼働率 \< 目標稼働率</span><span class="sxs-lookup"><span data-stu-id="4b898-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="4b898-138">**赤:** 支払い請求可能な稼働率 \< 目標稼働率 – 20</span><span class="sxs-lookup"><span data-stu-id="4b898-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="4b898-139">**リソースの稼働率** ビューはスケジュール ボードに基づいているため、スケジュール ボードのフィルター処理機能を使用して結果をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="4b898-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="4b898-140">グリッドでは、ロールまたは個々のリソースのいずれかで目標稼働率を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b898-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="4b898-141">これを設定するには、**リソース** \> **リソース ロール**へと移動します。</span><span class="sxs-lookup"><span data-stu-id="4b898-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="4b898-142">さらに、既定ロールは各予約可能リソースに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b898-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="4b898-143">**リソース** \> **リソース**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="4b898-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="4b898-144">**Project Service** タブでは、リソース ロールが定義され、**既定** フィールドが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4b898-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="4b898-145">**規定 = いいえ**のところにはその他のロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="4b898-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="4b898-146">**規定 = はい**のところのロールは、そのロールの目標に対するリソースの稼働率を評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="4b898-147">**Project Service** タブでは、リソースの個々の目標リソース稼働率も設定できます。</span><span class="sxs-lookup"><span data-stu-id="4b898-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="4b898-148">その後、稼働率計算を使って、リソースの既定ロールの目標の代わりに、リソースの目標を評価します。</span><span class="sxs-lookup"><span data-stu-id="4b898-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="4b898-149">稼働率はリソースが承認した場合に限りリソースに対してのみ、それがグリッドで表示される期間中の課金対象時間に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="4b898-150">リソースの空き時間</span><span class="sxs-lookup"><span data-stu-id="4b898-150">Resource availability</span></span>

<span data-ttu-id="4b898-151">リソース マネージャーがリソースの空き時間を表示し、予約を更新することができることは必要不可欠です。</span><span class="sxs-lookup"><span data-stu-id="4b898-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="4b898-152">場合によっては、正式な要求 (リソース要求) はありませんが、リソース マネージャーは、電子メール、電話、またはインスタント メッセージなどのチャンネルから来る予定外の要求に応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b898-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="4b898-153">リソース マネージャーはスケジュール ボードを使用して、リソースと予約を更新します。</span><span class="sxs-lookup"><span data-stu-id="4b898-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="4b898-154">リソースの作業時間は、リソースの空き時間を計算するための基本として使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b898-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="4b898-155">リソースの予約は、リソースのキャパシティを消費します。</span><span class="sxs-lookup"><span data-stu-id="4b898-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="4b898-156">スケジュール ボードは、色と影を使用して、予約、空き時間、予約超過、さらに予約状況も表示します。</span><span class="sxs-lookup"><span data-stu-id="4b898-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="4b898-157">スケジュール ボード設定の設定は凡例を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4b898-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="4b898-158">スケジュール ボードの個々の予約可能リソースの横に右向きの矢印が表示されている場合は、そのリソースは予約された作業の詳細表示を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="4b898-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="4b898-159">Dynamics 365 プロジェクト オペレーションは Universal Resource Scheduling エンジンを使用しているため、 Dynamics 365 Field Service がインストールされている場合は、プロジェクトの予約、作業指示書、スケジュールをするにあたって拡張したその他のエンティティの詳細を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4b898-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="4b898-160">個々のリソースに関する詳細を表示するには、右クリックしてリソース カードを開きます。</span><span class="sxs-lookup"><span data-stu-id="4b898-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

