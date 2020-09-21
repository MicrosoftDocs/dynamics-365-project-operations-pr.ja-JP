---
title: プロジェクトの進捗状況とコスト消費
description: このトピックでは、プロジェクトの進行状況とコスト消費を追跡する方法について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752914"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="aa6bb-103">プロジェクトの進捗状況とコスト消費</span><span class="sxs-lookup"><span data-stu-id="aa6bb-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aa6bb-104">スケジュールに対して進行状況を追跡する必要性は業種によって異なります。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="aa6bb-105">一部の業界では細かいレベルで追跡しますが、より高いレベルでの追跡をおこなう業界もあります。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="aa6bb-106">このトピックでは、組織の要件を満たすためのスケジュール方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="aa6bb-107">工数の追跡の表示</span><span class="sxs-lookup"><span data-stu-id="aa6bb-107">Effort tracking view</span></span>

<span data-ttu-id="aa6bb-108">**工数の追跡**ビューは、スケジュール内のタスクの進捗状況を追跡します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="aa6bb-109">タスクで費やされた実際の工数時間をタスクの計画工数時間と比較します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="aa6bb-110">PSA は次の計算式を使用して追跡指標を計算します :</span><span class="sxs-lookup"><span data-stu-id="aa6bb-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="aa6bb-111">進行状況率 = 今までに費やした実際の工数 ÷ 計画されたタスクの工数</span><span class="sxs-lookup"><span data-stu-id="aa6bb-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="aa6bb-112">完了までの予測 (ETC) = 計画工数 – 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="aa6bb-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="aa6bb-113">完了時予測 (EAC) = 残りの工数 – 今までに費やした実際の工数</span><span class="sxs-lookup"><span data-stu-id="aa6bb-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="aa6bb-114">予測工数差異 = 計画工数 - EAC</span><span class="sxs-lookup"><span data-stu-id="aa6bb-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="aa6bb-115">PSA はタスクの工数差異のプロジェクションを示します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="aa6bb-116">EAC が計画工数を上回る場合は、そのタスクは最初に計画された時間よりも多くかかると予測されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="aa6bb-117">したがって、これは予定より遅れていることになります。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="aa6bb-118">EAC が計画工数を下まわる場合は、そのタスクは最初に計画された時間よりも少ない時間ですむ予測されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="aa6bb-119">したがって、予定より先行していることになります。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="aa6bb-120">工数の再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="aa6bb-120">Re-projecting effort</span></span>

<span data-ttu-id="aa6bb-121">プロジェクト マネージャーが、タスクの最初の予測を変更することはよくあります。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="aa6bb-122">プロジェクトの再プロジェクションは、プロジェクトの現在の状態による、プロジェクト マネージャーの予測の認識です。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="aa6bb-123">ただし、プロジェクトのベースラインは、プロジェクトのスケジュールおよびコスト見積もりに関する公表済みの真実のソースを表しており、これはプロジェクトの全利害関係者が既に合意しているため、プロジェクト マネージャーがベースライン値を変更することは推奨されません。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="aa6bb-124">プロジェクト マネージャーがタスクを再プロジェクションするには二つの方法があります:</span><span class="sxs-lookup"><span data-stu-id="aa6bb-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="aa6bb-125">規定の ETC をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="aa6bb-126">規定の進捗率をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="aa6bb-127">これらのアプローチはそれぞれ、タスクの ETC、EAC、および進捗率の再計算やタスクの予測工数差異を生じます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="aa6bb-128">サマリー タスクの EAC、ETC、および進捗率も再計算され、工数差異の新しいプロジェクションを生成します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="aa6bb-129">サマリー タスク上の工数の再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="aa6bb-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="aa6bb-130">サマリー タスク上の工数またはコンテナー タスクは再プロジェクションできます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="aa6bb-131">ユーザーがサマリー タスク上の残りの工数や進捗率を使用して再プロジェクトしたかにかかわらず、次の計算セットが開始します:</span><span class="sxs-lookup"><span data-stu-id="aa6bb-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="aa6bb-132">EAC、ETC、およびタスクの進捗率が計算されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="aa6bb-133">新しい EAC が、元の EAC がタスクにしたのと同じタスク率で下位の子のタスクへ配布されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="aa6bb-134">下位のリーフ ノードまでの個々のタスクの新規 EAC が計算されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="aa6bb-135">影響を受ける下位のリーフにノードまでの子のタスクには、EAC 値に基づいて再計算された、自分たちの ETC と進捗率があります。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="aa6bb-136">これにより、タスクの工数差異の新しいプロジェクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="aa6bb-137">ルート ノードまでのサマリー タスクの EAC が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="aa6bb-138">コスト追跡ビュー</span><span class="sxs-lookup"><span data-stu-id="aa6bb-138">Cost tracking view</span></span> 

<span data-ttu-id="aa6bb-139">**コストの追跡**ビューには、タスクで費やされた実際のコストをタスクの計画コストと比較します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="aa6bb-140">このビューは人件費のみを示し、経費予測からのコストは含みません。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="aa6bb-141">PSA は次の計算式を使用して追跡指標を計算します :</span><span class="sxs-lookup"><span data-stu-id="aa6bb-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="aa6bb-142">費やしたコスト率 = 今までに費やした実際のコスト ÷ タスクの計画コスト</span><span class="sxs-lookup"><span data-stu-id="aa6bb-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="aa6bb-143">完了までのコスト (CTC) = 計画コスト – 今までに実際に費やしたコスト</span><span class="sxs-lookup"><span data-stu-id="aa6bb-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="aa6bb-144">EAC = CTC + 今までに使った実際のコスト</span><span class="sxs-lookup"><span data-stu-id="aa6bb-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="aa6bb-145">予測コスト差異 = 予測コスト – EAC</span><span class="sxs-lookup"><span data-stu-id="aa6bb-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="aa6bb-146">コスト差異のプロジェクションはタスク上に示されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="aa6bb-147">EAC が計画コストを上回る場合、そのタスクは最初に計画されたコストよりも多くかかると予測されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="aa6bb-148">したがって、予算オーバーの傾向が出ています。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="aa6bb-149">EAC が計画コストを下まわる場合、そのタスクは最初に計画されたコストよりも少なくてすむと予測されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="aa6bb-150">したがって、予算以内に収まる傾向が出ています。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="aa6bb-151">プロジェクト マネージャーのコストの再プロジェクション</span><span class="sxs-lookup"><span data-stu-id="aa6bb-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="aa6bb-152">工程が再プロジェクションされる場合、CTC、EAC、コストの使用率、および予測コスト差異はすべて**コストの追跡**ビューで再計算されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="aa6bb-153">プロジェクト ステータス サマリー</span><span class="sxs-lookup"><span data-stu-id="aa6bb-153">Project status summary</span></span>

<span data-ttu-id="aa6bb-154">**工数の追跡**と**コストの追跡**ビューの追跡データは、プロジェクト ルート ノード、サマリー タスク、リーフ ノード タスクレベルの進行状況とコスト消費を示します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="aa6bb-155">**プロジェクトのエンティティ**ページの**状態**ページには、プロジェクト レベルのステータス サマリーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="aa6bb-156">ステータス サマリー フィールド</span><span class="sxs-lookup"><span data-stu-id="aa6bb-156">Status summary fields</span></span>

<span data-ttu-id="aa6bb-157">**プロジェクト全体のステータス**フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="aa6bb-158">また、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="aa6bb-159">**コメント**フィールドでは、プロジェクト マネージャーはステータスについて特定のコメントを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="aa6bb-160">**ステータス更新日**フィールドは編集不可で、値は、ステータスが最後に更新された時を示すタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="aa6bb-161">**スケジュール パフォーマンス**フィールドと**コスト パフォーマンス**フィールドは追跡日から設定されます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="aa6bb-162">**工数の追跡**ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドを**先行**に設定できます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="aa6bb-163">ルート ノードのスケジュールとコスト差異がマイナスの場合、これらは**遅延**に設定できます。</span><span class="sxs-lookup"><span data-stu-id="aa6bb-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
