---
title: プロジェクトの追跡の概要
description: このトピックでは、プロジェクトの進行状況とコスト消費を追跡する方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 14094d603be2834dc66abff2ff1faf5e940b1ffa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286614"
---
# <a name="project-tracking-overview"></a><span data-ttu-id="ec5fc-103">プロジェクトの追跡の概要</span><span class="sxs-lookup"><span data-stu-id="ec5fc-103">Project tracking overview</span></span>

<span data-ttu-id="ec5fc-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ec5fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec5fc-105">スケジュールに対して進行状況を追跡する必要性は業種によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="ec5fc-106">一部の業界では詳細なレベルで追跡しますが、より高いレベルでの追跡をおこなう業界もあります。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="ec5fc-107">このトピックでは、組織の要件を満たすためのスケジュール方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="ec5fc-108">工数の追跡の表示</span><span class="sxs-lookup"><span data-stu-id="ec5fc-108">Effort tracking view</span></span>

<span data-ttu-id="ec5fc-109">**工数の追跡** ビューは、タスクに費やされた実際の工数時間をタスクの計画された工数時間と比較することにより、スケジュール内のタスクの進行状況を追跡します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="ec5fc-110">Dynamics 365 Project Operations は次の計算式を使用して追跡指標を計算します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="ec5fc-111">**進捗率**: 今までに費やした実際の工数 ÷ 完了時の見積もり (EAC)</span><span class="sxs-lookup"><span data-stu-id="ec5fc-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="ec5fc-112">**完了までの予測 (ETC)**: 計画工数 – 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="ec5fc-112">**Estimate to complete (ETC)**: Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="ec5fc-113">**EAC**: 残りの工数 + 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="ec5fc-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="ec5fc-114">**予測工数差異**: 計画工数 – EAC</span><span class="sxs-lookup"><span data-stu-id="ec5fc-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="ec5fc-115">Project Operations はタスクの工数差異のプロジェクションを示します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="ec5fc-116">EAC が計画工数より多い場合、タスクが最初の計画より時間がかかると予測され、スケジュールより遅れます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="ec5fc-117">EAC が予定工数より少ない場合、タスクが最初の計画より時間がかからないと予測され、スケジュールより早まります。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="ec5fc-118">工数の再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="ec5fc-118">Reprojecting effort</span></span>

<span data-ttu-id="ec5fc-119">プロジェクト マネージャーが、タスクの最初の予測を変更することはよくあります。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="ec5fc-120">プロジェクトの再プロジェクションは、プロジェクトの現在の状態による、プロジェクト マネージャーの予測の認識です。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="ec5fc-121">ただし、プロジェクト マネージャーがベースライン値を変更することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-121">However, we don't recommend that project managers change the baseline numbers.</span></span> <span data-ttu-id="ec5fc-122">これは、プロジェクト ベースラインがプロジェクト スケジュールおよびコスト見積もりの信頼できる情報源であり、すべてのプロジェクトの利害関係者が合意しているためです。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-122">This is because the project baseline represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="ec5fc-123">プロジェクト マネージャーがタスクの工数を再プロジェクトするには 2 つの方法があります:</span><span class="sxs-lookup"><span data-stu-id="ec5fc-123">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="ec5fc-124">規定の ETC をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-124">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="ec5fc-125">規定の進捗率をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-125">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="ec5fc-126">各方法により、タスクの ETC、EAC、進捗率、およびタスクの予測工数差異が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-126">Each approach causes a recalculation of the task's ETC, EAC, progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="ec5fc-127">サマリー タスクの EAC、ETC、および進捗率も再計算され、工数差異の新しいプロジェクションを生成します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-127">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="ec5fc-128">概要タスク上の工数の再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="ec5fc-128">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="ec5fc-129">概要タスクまたはコンテナー タスク上の工数を再プロジェクトできます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-129">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="ec5fc-130">ユーザーが概要タスク上の残りの工数や進捗率を使用して再プロジェクトしたかにかかわらず、次の一連の計算が開始されます:</span><span class="sxs-lookup"><span data-stu-id="ec5fc-130">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="ec5fc-131">EAC、ETC、およびタスクの進捗率が計算されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-131">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="ec5fc-132">新しい EAC が、元の EAC がタスクにしたのと同じタスク率で下位の子のタスクへ配布されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-132">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="ec5fc-133">リーフ ノード タスクまでの個々のタスクごとに新規 EAC が計算されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-133">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="ec5fc-134">影響を受ける下位のリーフにノードまでの子のタスクには、EAC 値に基づいて再計算された、自分たちの ETC と進捗率があります。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-134">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="ec5fc-135">これにより、タスクの工数差異の新しいプロジェクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-135">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="ec5fc-136">ルート ノードまでのサマリー タスクの EAC が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-136">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="ec5fc-137">コスト追跡ビュー</span><span class="sxs-lookup"><span data-stu-id="ec5fc-137">Cost tracking view</span></span> 

<span data-ttu-id="ec5fc-138">**コストの追跡** ビューには、タスクで費やされた実際のコストをタスクの計画コストと比較します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-138">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="ec5fc-139">このビューは人件費のみを示し、経費予測からのコストは含みません。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-139">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> <span data-ttu-id="ec5fc-140">Project Operations は、次の計算式を使用して追跡指標を計算します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-140">Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="ec5fc-141">**消費されたコスト率**: 今までに費やした実際のコスト ÷ 完了時見積原価</span><span class="sxs-lookup"><span data-stu-id="ec5fc-141">**Percentage of cost consumed**: Actual cost spent to date ÷ Estimated cost at completion</span></span>
- <span data-ttu-id="ec5fc-142">**完了までのコスト (CTC)**: 計画コスト – 今までに実際に費やしたコスト</span><span class="sxs-lookup"><span data-stu-id="ec5fc-142">**Cost to complete (CTC)**: Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="ec5fc-143">**EAC**: 残コスト + 今までに実際に費やしたコスト</span><span class="sxs-lookup"><span data-stu-id="ec5fc-143">**EAC**: Remaining cost + Actual cost spent to date</span></span>
- <span data-ttu-id="ec5fc-144">**予測コスト差異**: 計画コスト – EAC</span><span class="sxs-lookup"><span data-stu-id="ec5fc-144">**Projected cost variance**: Planned cost – EAC</span></span>

<span data-ttu-id="ec5fc-145">コスト差異のプロジェクションはタスク上に示されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-145">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="ec5fc-146">EAC が計画コストを上回る場合、そのタスクは最初に計画されたコストよりも多くかかると予測されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-146">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="ec5fc-147">したがって、予算オーバーの傾向が出ています。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-147">Therefore, it's trending over budget.</span></span> <span data-ttu-id="ec5fc-148">EAC が計画コストを下まわる場合、そのタスクは最初に計画されたコストよりも少なくてすむと予測されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-148">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="ec5fc-149">したがって、予算以内に収まる傾向が出ています。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-149">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="ec5fc-150">プロジェクト マネージャーのコストの再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="ec5fc-150">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="ec5fc-151">工程が再プロジェクトされる場合、CTC、EAC、コストの使用率、および予測コスト差異はすべて **コストの追跡** ビューで再計算されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-151">When effort is reprojected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="ec5fc-152">プロジェクト ステータス サマリー</span><span class="sxs-lookup"><span data-stu-id="ec5fc-152">Project status summary</span></span>

<span data-ttu-id="ec5fc-153">**工数の追跡** と **コストの追跡** ビューの追跡データは、プロジェクト ルート ノード、サマリー タスク、リーフ ノード タスクレベルの進行状況とコスト消費を示します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-153">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="ec5fc-154">**プロジェクトのエンティティ** ページの **状態** ページには、プロジェクト レベルのステータス サマリーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-154">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="ec5fc-155">ステータス サマリー フィールド</span><span class="sxs-lookup"><span data-stu-id="ec5fc-155">Status summary fields</span></span>

<span data-ttu-id="ec5fc-156">**プロジェクト全体のステータス** フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-156">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="ec5fc-157">また、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-157">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="ec5fc-158">**コメント** フィールドでは、プロジェクト マネージャーはステータスについて特定のコメントを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-158">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="ec5fc-159">**ステータス更新日** フィールドは編集不可で、値は、ステータスが最後に更新された時を示すタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-159">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="ec5fc-160">**スケジュール パフォーマンス** フィールドと **コスト パフォーマンス** フィールドは追跡日から設定されます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-160">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="ec5fc-161">**工数の追跡** ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドを **先行** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-161">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="ec5fc-162">ルート ノードのスケジュールとコスト差異がマイナスの場合、これらは **遅延** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-162">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]