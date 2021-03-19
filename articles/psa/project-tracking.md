---
title: プロジェクトの進捗状況とコストの使用
description: このトピックでは、プロジェクトの進行状況とコスト消費を追跡する方法について説明します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283644"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="96909-103">プロジェクトの進捗状況とコストの使用</span><span class="sxs-lookup"><span data-stu-id="96909-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="96909-104">スケジュールに対して進行状況を追跡する必要性は業種によって異なります。</span><span class="sxs-lookup"><span data-stu-id="96909-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="96909-105">一部の業界では細かいレベルで追跡しますが、より高いレベルでの追跡をおこなう業界もあります。</span><span class="sxs-lookup"><span data-stu-id="96909-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="96909-106">このトピックでは、組織の要件を満たすためのスケジュール方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="96909-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="96909-107">工数の追跡の表示</span><span class="sxs-lookup"><span data-stu-id="96909-107">Effort tracking view</span></span>

<span data-ttu-id="96909-108">**工数の追跡** ビューは、スケジュール内のタスクの進捗状況を追跡します。</span><span class="sxs-lookup"><span data-stu-id="96909-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="96909-109">タスクに費やされたの実際の工数とタスクの計画工数を比較します。</span><span class="sxs-lookup"><span data-stu-id="96909-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="96909-110">Project Service Automation は次の計算式を使用して追跡指標を計算します:</span><span class="sxs-lookup"><span data-stu-id="96909-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="96909-111">最初のタスク作成時: 計画コストは、完了時の見積原価に設定されます。</span><span class="sxs-lookup"><span data-stu-id="96909-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="96909-112">実績がタスクに記録されると、工数の追跡ビューで次の計算が行われます</span><span class="sxs-lookup"><span data-stu-id="96909-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="96909-113">進捗率 = 今までに費やした実際の工数 ÷ 完了時予測 (EAC)</span><span class="sxs-lookup"><span data-stu-id="96909-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="96909-114">完了までの予測 (ETC) = 完了時予測 (EAC) – 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="96909-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="96909-115">EAC = 残りの工数 + 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="96909-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="96909-116">予測工数差異 = 計画工数 - EAC</span><span class="sxs-lookup"><span data-stu-id="96909-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="96909-117">Project Service Automation はタスクの工数差異のプロジェクションを示します。</span><span class="sxs-lookup"><span data-stu-id="96909-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="96909-118">EAC が計画工数を上回る場合は、そのタスクは最初に計画された時間よりも多くかかると予測されます。</span><span class="sxs-lookup"><span data-stu-id="96909-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="96909-119">したがって、これは予定より遅れていることになります。</span><span class="sxs-lookup"><span data-stu-id="96909-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="96909-120">EAC が計画工数を下まわる場合は、そのタスクは最初に計画された時間よりも少ない時間ですむ予測されます。</span><span class="sxs-lookup"><span data-stu-id="96909-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="96909-121">したがって、予定より先行していることになります。</span><span class="sxs-lookup"><span data-stu-id="96909-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="96909-122">工数の再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="96909-122">Reprojecting effort</span></span>

<span data-ttu-id="96909-123">プロジェクト マネージャーが、タスクの最初の予測を変更することはよくあります。</span><span class="sxs-lookup"><span data-stu-id="96909-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="96909-124">プロジェクトの再プロジェクションは、プロジェクトの現在の状態による、プロジェクト マネージャーの予測の認識です。</span><span class="sxs-lookup"><span data-stu-id="96909-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="96909-125">ただし、プロジェクトのベースラインは、プロジェクトのスケジュールおよびコスト見積もりに関する公表済みの真実のソースを表しており、これはプロジェクトの全利害関係者が既に合意しているため、プロジェクト マネージャーがベースライン値を変更することは推奨されません。</span><span class="sxs-lookup"><span data-stu-id="96909-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="96909-126">プロジェクト マネージャーがタスクの工数を再プロジェクトするには 2 つの方法があります:</span><span class="sxs-lookup"><span data-stu-id="96909-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="96909-127">規定の ETC をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="96909-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="96909-128">規定の進捗率をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="96909-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="96909-129">これらのアプローチはそれぞれ、タスクの ETC、EAC、および進捗率の再計算やタスクの予測工数差異を生じます。</span><span class="sxs-lookup"><span data-stu-id="96909-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="96909-130">サマリー タスクの EAC、ETC、および進捗率も再計算され、工数差異の新しいプロジェクションを生成します。</span><span class="sxs-lookup"><span data-stu-id="96909-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="96909-131">概要タスク上の工数の再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="96909-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="96909-132">概要タスクまたはコンテナー タスク上の工数を再プロジェクトできます。</span><span class="sxs-lookup"><span data-stu-id="96909-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="96909-133">ユーザーが概要タスク上の残りの工数や進捗率を使用して再プロジェクトしたかにかかわらず、次の一連の計算が開始されます:</span><span class="sxs-lookup"><span data-stu-id="96909-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="96909-134">EAC、ETC、およびタスクの進捗率が計算されます。</span><span class="sxs-lookup"><span data-stu-id="96909-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="96909-135">新しい EAC が、元の EAC がタスクにしたのと同じタスク率で下位の子のタスクへ配布されます。</span><span class="sxs-lookup"><span data-stu-id="96909-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="96909-136">リーフ ノード タスクまでの個々のタスクごとに新規 EAC が計算されます。</span><span class="sxs-lookup"><span data-stu-id="96909-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="96909-137">影響を受ける下位のリーフにノードまでの子のタスクには、EAC 値に基づいて再計算された、自分たちの ETC と進捗率があります。</span><span class="sxs-lookup"><span data-stu-id="96909-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="96909-138">これにより、タスクの工数差異の新しいプロジェクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="96909-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="96909-139">ルート ノードまでのサマリー タスクの EAC が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="96909-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="96909-140">コスト追跡ビュー</span><span class="sxs-lookup"><span data-stu-id="96909-140">Cost tracking view</span></span> 

<span data-ttu-id="96909-141">**コスト追跡** ビューは、タスクで費やされた実際のコストを計画コストと比較します。</span><span class="sxs-lookup"><span data-stu-id="96909-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="96909-142">このビューは人件費のみを示し、経費予測からのコストは含みません。</span><span class="sxs-lookup"><span data-stu-id="96909-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="96909-143">Project Service Automation は次の計算式を使用して追跡指標を計算します:</span><span class="sxs-lookup"><span data-stu-id="96909-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="96909-144">タスクが作成されると、計画コストは完了時の見積原価と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="96909-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="96909-145">実績がタスクに記録されると、コストの **追跡** ビューで次の計算が行われます:</span><span class="sxs-lookup"><span data-stu-id="96909-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="96909-146">費やしたコスト率 = 今までに費やした実際のコスト ÷ タスクの完了時見積原価</span><span class="sxs-lookup"><span data-stu-id="96909-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="96909-147">完了までのコスト (CTC) = 完了時見積原価 – 今までに費やした実際のコスト</span><span class="sxs-lookup"><span data-stu-id="96909-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="96909-148">完了時見積原価 = CTC + 今までに費やした実際のコスト</span><span class="sxs-lookup"><span data-stu-id="96909-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="96909-149">予測コスト差異 = 計画コスト – 完了時見積原価</span><span class="sxs-lookup"><span data-stu-id="96909-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="96909-150">コスト差異のプロジェクションはタスク上に示されます。</span><span class="sxs-lookup"><span data-stu-id="96909-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="96909-151">完了時見積原価が計画コストを上回る場合、そのタスクは最初に計画されたコストよりも多くかかると予測されます。</span><span class="sxs-lookup"><span data-stu-id="96909-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="96909-152">したがって、予算オーバーの傾向が出ています。</span><span class="sxs-lookup"><span data-stu-id="96909-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="96909-153">完了時見積原価が計画コストを下回る場合、タスクは最初に計画されたコストよりも少なくなると予測され、予算を下回る傾向にあります。</span><span class="sxs-lookup"><span data-stu-id="96909-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="96909-154">プロジェクト マネージャーのコストの再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="96909-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="96909-155">工程が再プロジェクションされる場合、CTC、完了時見積原価、コストの使用率、および推定原価差異はすべて **コスト追跡** ビューで再計算されます。</span><span class="sxs-lookup"><span data-stu-id="96909-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="96909-156">プロジェクト ステータス サマリー</span><span class="sxs-lookup"><span data-stu-id="96909-156">Project status summary</span></span>

<span data-ttu-id="96909-157">**工数の追跡** と **コストの追跡** ビューの追跡データは、プロジェクト ルート ノード、サマリー タスク、リーフ ノード タスクレベルの進行状況とコスト消費を示します。</span><span class="sxs-lookup"><span data-stu-id="96909-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="96909-158">**プロジェクトのエンティティ** ページの **状態** ページには、プロジェクト レベルのステータス サマリーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96909-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="96909-159">ステータス サマリー フィールド</span><span class="sxs-lookup"><span data-stu-id="96909-159">Status summary fields</span></span>

<span data-ttu-id="96909-160">**プロジェクト全体のステータス** フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="96909-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="96909-161">また、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。</span><span class="sxs-lookup"><span data-stu-id="96909-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="96909-162">**コメント** フィールドでは、プロジェクト マネージャーはステータスについて特定のコメントを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="96909-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="96909-163">**ステータス更新日** フィールドは編集不可で、値は、ステータスが最後に更新された時を示すタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="96909-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="96909-164">**スケジュール パフォーマンス** フィールドと **コスト パフォーマンス** フィールドは追跡日から設定されます。</span><span class="sxs-lookup"><span data-stu-id="96909-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="96909-165">**工数の追跡** ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドを **先行** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="96909-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="96909-166">ルート ノードのスケジュールとコスト差異がマイナスの場合、これらは **遅延** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="96909-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]