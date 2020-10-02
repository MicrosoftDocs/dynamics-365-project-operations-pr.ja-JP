---
title: リソースの調整の概要
description: このトピックでは、リソースの予約とプロジェクトへの割り当てを確実に一致させる方法について説明します。
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
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897457"
---
# <a name="resource-reconciliation-overview"></a><span data-ttu-id="09144-103">リソースの調整の概要</span><span class="sxs-lookup"><span data-stu-id="09144-103">Resource reconciliation overview</span></span>

<span data-ttu-id="09144-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="09144-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09144-105">チーム メンバーの場合、予約と割り当ては緩く結び付けられます。</span><span class="sxs-lookup"><span data-stu-id="09144-105">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="09144-106">つまり、リソースに割り当てはあっても予約はないか、リソースに予約はあっても割り当てはありません。</span><span class="sxs-lookup"><span data-stu-id="09144-106">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="09144-107">理想としてはリソースがタスク割り当てを実行するキャパシティを持つように、予約と割り当てを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09144-107">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="09144-108">ただし、予約は空き時間に基づいて行われ、プロジェクトの続行に応じてタスクのタイミングが変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="09144-108">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="09144-109">したがって、予約と割り当ての緩い結合は柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="09144-109">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="09144-110">**プロジェクト**フォームの**調整** タブを使用すると、プロジェクト マネージャーはプロジェクト チームへのチーム メンバーの予約や割り当てを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="09144-110">The **Reconciliation** tab on the **Project** form lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

<span data-ttu-id="09144-111">**調整** タブには、チームメンバーごとの個別タスク割り当てのレベルまで予約と割り当てが表示されています。</span><span class="sxs-lookup"><span data-stu-id="09144-111">The **Reconciliation** tab also shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="09144-112">時間は、月から日までの期間を表すセルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="09144-112">Hours are displayed in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="09144-113">タブには、**合計** 列とともにプロジェクトの全体的な合計額も表示されます。</span><span class="sxs-lookup"><span data-stu-id="09144-113">The tab also shows an overall net total for the project, together with a **Total** column.</span></span>

<span data-ttu-id="09144-114">リソースごとに、タブはチーム メンバーの予約とチーム メンバーのタスクの割り当てのロールアップの差を計算します。</span><span class="sxs-lookup"><span data-stu-id="09144-114">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="09144-115">理想としては、この差は 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="09144-115">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="09144-116">つまり、予約と割り当てに差はありません。</span><span class="sxs-lookup"><span data-stu-id="09144-116">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="09144-117">差は、 2 つの条件に注意を引くために色分けと影つけされます:</span><span class="sxs-lookup"><span data-stu-id="09144-117">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="09144-118">**予約不足** – 予約不足はリソースに予約よりも多くの割り当てがある場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="09144-118">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="09144-119">この容量が予約されていないため、プロジェクト管理者は不足分に対応するためにリソースの予約を延長して、条件を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="09144-119">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="09144-120">**予約過剰** – リソースがプロジェクトに予約されているがタスクには割り当てられていない場合に過剰予約が発生します。</span><span class="sxs-lookup"><span data-stu-id="09144-120">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="09144-121">この条件はタスクの割り当てが発生する前に、リソースがプロジェクトに予約された場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="09144-121">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="09144-122">ただし、他の場合は、リソースはタスクに割り当てるように計画されていません。</span><span class="sxs-lookup"><span data-stu-id="09144-122">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="09144-123">このような場合、プロジェクト マネージャーは、そのリソースの予約のキャンセルを検討する必要があり、これによってキャパシティを他のプロジェクトに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="09144-123">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="09144-124">場合によっては、時間を日レベルより上位レベル (たとえば、月レベル) で表示すると、リソース (つまり、予約=割り当て) の正味差がゼロになることがあります。</span><span class="sxs-lookup"><span data-stu-id="09144-124">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="09144-125">ただし、週レベルで時間を表示すると、最初の週には 0 時間の割り当てと 40 時間の予約があり、2週目には 40 時間の割り当てと 0 時間の予約があることがわかります。</span><span class="sxs-lookup"><span data-stu-id="09144-125">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="09144-126">全体として、予約と割り当ては調整されますが、週ごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="09144-126">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="09144-127">上位レベルで時間を表示すると、 **調整** タブのセルには、下位レベルで差があることを知らせるインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="09144-127">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="09144-128">セルをダブルクリックすると、拡大して差を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="09144-128">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="09144-129">次に、右クリックして縮小します。リソースを選択して、グリッド ツール バーの **次の差分** コントロールを使用すると、そのリソースの予約と割り当ての次の差分に移動できます。</span><span class="sxs-lookup"><span data-stu-id="09144-129">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="09144-130">その後、 **前の差分** コントロールを使用して、戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="09144-130">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="09144-131">**設定** で差分インジケータととナビゲーション動作をオフにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="09144-131">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>


<span data-ttu-id="09144-132">リソースのタスク割り当てがあり、予約がない場合、 **プロジェクト** ページの **調整** タブで、予約不足を選択し、 **予約の延長** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09144-132">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="09144-133">**予約の延長** ダイアログ ボックスが表示され、リソースの不足に対応するために必要な予約が表示されます。</span><span class="sxs-lookup"><span data-stu-id="09144-133">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="09144-134">また、すべてのプロジェクトまたは他のスケジュール可能なエンティティにわたるリソースの既存の予約も表示されます。</span><span class="sxs-lookup"><span data-stu-id="09144-134">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="09144-135">**OK** を選択してリソースの予約を作成すると、そのリソースが使用可能かどうかにかかわらず、オーバブッキングが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="09144-135">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

<span data-ttu-id="09144-136">プロジェクト管理者やリソース マネージャーは、スケジュール ボードを使用して、リソースが容量を超えてオーバーブッキングされる状況を管理できます。</span><span class="sxs-lookup"><span data-stu-id="09144-136">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>

