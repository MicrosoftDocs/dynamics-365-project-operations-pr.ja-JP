---
title: プロジェクトの工数の追跡
description: このトピックでは、プロジェクトの工数と進行状況を追跡する方法について説明します。
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3fdf7787f0144dace84852a0442406085bdc1639
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010882"
---
# <a name="project-effort-tracking"></a><span data-ttu-id="6e6e3-103">プロジェクトの工数の追跡</span><span class="sxs-lookup"><span data-stu-id="6e6e3-103">Project effort tracking</span></span>

<span data-ttu-id="6e6e3-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="6e6e3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e6e3-105">スケジュールに対して進行状況を追跡する必要性は業種によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="6e6e3-106">一部の業界では詳細なレベルで追跡しますが、より高いレベルでの追跡をおこなう業界もあります。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="6e6e3-107">このトピックでは、組織の要件を満たすためのスケジュール方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="6e6e3-108">工数の追跡の表示</span><span class="sxs-lookup"><span data-stu-id="6e6e3-108">Effort tracking view</span></span>

<span data-ttu-id="6e6e3-109">**工数の追跡** ビューは、タスクに費やされた実際の工数時間をタスクの計画された工数時間と比較することにより、スケジュール内のタスクの進行状況を追跡します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="6e6e3-110">Dynamics 365 Project Operations は次の計算式を使用して追跡指標を計算します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="6e6e3-111">**進捗率**: 今までに費やした実際の工数 ÷ 完了時の見積もり (EAC)</span><span class="sxs-lookup"><span data-stu-id="6e6e3-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="6e6e3-112">**残り工数**: 完了時予測 – 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="6e6e3-112">**Remaining Effort**: Estimated effort at complete – Actual effort spent to date</span></span> 
- <span data-ttu-id="6e6e3-113">**EAC**: 残りの工数 + 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="6e6e3-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="6e6e3-114">**予想される工数の差異**: 計画工数 – EAC</span><span class="sxs-lookup"><span data-stu-id="6e6e3-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="6e6e3-115">Project Operations は、タスクでの工数の差異の予測を示します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="6e6e3-116">EAC が予定工数を超える場合、タスクの元の計画よりも長い時間を要すると予測され、スケジュールから遅れています。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="6e6e3-117">EAC が予定工数より少ない場合、タスクが最初の計画より時間がかからないと予測され、スケジュールより早まります。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort-on-leaf-node-tasks"></a><span data-ttu-id="6e6e3-118">リーフ ノード タスクの工数の再予測</span><span class="sxs-lookup"><span data-stu-id="6e6e3-118">Reprojecting effort on leaf node tasks</span></span>

<span data-ttu-id="6e6e3-119">プロジェクト マネージャーが、タスクの最初の予測を変更することはよくあります。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="6e6e3-120">プロジェクトの再予測は、プロジェクトの現在の状態を踏まえた、プロジェクト マネージャーの見積もりの認識です。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="6e6e3-121">ただし、プロジェクト マネージャーが計画された工数を変更することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-121">However, we don't recommend that project managers change the planned effort numbers.</span></span> <span data-ttu-id="6e6e3-122">これは、プロジェクトの計画された工数が、プロジェクトのスケジュールとコスト見積もりの確立された情報源であり、すべてのプロジェクトの利害関係者がそれに同意しているためです。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-122">This is because the project planned effort represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="6e6e3-123">プロジェクト マネージャーは、タスクの新しい見積もりで既定の **残りの工数** フィールドを更新することにより、タスクの工数を再予測できます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-123">A project manager can reproject effort on tasks by updating the default **Remaining Effort** with a new estimate on the task.</span></span> <span data-ttu-id="6e6e3-124">これにより、タスクの完了時の工数見積もり (EAC)、進行率、およびタスクの予測された工数差異が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-124">This update causes a recalculation of the task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="6e6e3-125">集計タスクの EAC、ETC、および進捗率も再計算され、工数の差異の新しい予測が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-125">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="6e6e3-126">集計タスクの工数の再予測</span><span class="sxs-lookup"><span data-stu-id="6e6e3-126">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="6e6e3-127">概要タスクまたはコンテナー タスク上の工数を再プロジェクトできます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-127">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="6e6e3-128">プロジェクト マネージャーは、サマリー タスクの残り工数を更新できます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-128">Project managers can update remaining effort on the summary tasks.</span></span> <span data-ttu-id="6e6e3-129">残り工数を更新すると、アプリケーションで次の一連の計算がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-129">Updating the remaining effort triggers the following set of calculations in the application:</span></span>

- <span data-ttu-id="6e6e3-130">EAC およびタスクの進捗率が計算されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-130">The EAC and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="6e6e3-131">新しい EAC が、元の EAC がタスクにしたのと同じタスク率で下位の子のタスクへ配布されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-131">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="6e6e3-132">リーフ ノード タスクまでの個々のタスクごとに新規 EAC が計算されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-132">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="6e6e3-133">影響を受ける下位のリーフにノードまでの子のタスクには、EAC 値に基づいて再計算された、自分たちの残り工数と進捗率があります。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-133">The affected child tasks down to the leaf nodes have their remaining effort and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="6e6e3-134">これにより、タスクの工数差異の新しいプロジェクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-134">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="6e6e3-135">ルート ノードまでのサマリー タスクの EAC が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-135">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>


## <a name="project-status-summary"></a><span data-ttu-id="6e6e3-136">プロジェクト ステータス サマリー</span><span class="sxs-lookup"><span data-stu-id="6e6e3-136">Project status summary</span></span>

<span data-ttu-id="6e6e3-137">**工数の追跡** と **コストの追跡** ビューの追跡データは、プロジェクト ルート ノード、サマリー タスク、リーフ ノード タスクレベルの進行状況とコスト消費を示します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-137">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="6e6e3-138">**プロジェクトのエンティティ** ページの **状態** ページには、プロジェクト レベルのステータス サマリーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-138">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="6e6e3-139">ステータス サマリー フィールド</span><span class="sxs-lookup"><span data-stu-id="6e6e3-139">Status summary fields</span></span>

<span data-ttu-id="6e6e3-140">**プロジェクト全体のステータス** フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-140">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="6e6e3-141">また、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-141">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="6e6e3-142">**コメント** フィールドでは、プロジェクト マネージャーはステータスについて特定のコメントを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-142">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="6e6e3-143">**ステータス更新日** フィールドは編集不可で、値は、ステータスが最後に更新された時を示すタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-143">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="6e6e3-144">**スケジュール パフォーマンス** フィールドと **コスト パフォーマンス** フィールドは追跡日から設定されます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-144">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="6e6e3-145">**工数の追跡** ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドを **先行** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-145">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="6e6e3-146">ルート ノードのスケジュールとコストの差異が負の場合は、**遅延** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6e6e3-146">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
