---
title: WBS (作業分解構造) テンプレートでロールを設定する
description: このトピックは、WBS (作業分解構造)テンプレートでのロール情報の設定に関する情報を提供します。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997607"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a><span data-ttu-id="78f83-103">WBS (作業分解構造) テンプレートでロールを設定する</span><span class="sxs-lookup"><span data-stu-id="78f83-103">Set up roles on Work breakdown structure templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78f83-104">プロジェクト マネージャーは、新しいプロジェクトのWBS (作業分解構造) を作成するときに適用できる WBS テンプレートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="78f83-104">Project managers can set up Work breakdown structure (WBS) templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="78f83-105">プロジェクト マネージャーは、テンプレートを作成するときにロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="78f83-105">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="78f83-106">次の手順を使用して、WBS テンプレートにロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="78f83-106">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="78f83-107">**プロジェクト管理と会計** > **設定** > **プロジェクト** > **WBS (作業分解構造)** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-107">Select **Project management and accounting** > **Setup** > **Projects** > **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="78f83-108">選択した WBS テンプレートの **詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-108">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="78f83-109">リストでタスクを選択し、**ロール** フィールドで、タスクに割り当てるロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-109">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

## <a name="work-with-a-wbs"></a><span data-ttu-id="78f83-110">WBS を使用する</span><span class="sxs-lookup"><span data-stu-id="78f83-110">Work with a WBS</span></span>

<span data-ttu-id="78f83-111">新しい WBS を作成、または既存の WBS テンプレートから WBS をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="78f83-111">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="78f83-112">プロジェクト マネージャーは、WBS の新しいタスクにロールを割り当てることにより、リソースを簡単に管理できます。</span><span class="sxs-lookup"><span data-stu-id="78f83-112">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="78f83-113">ロールは、リソースが取得された後、またはタスクで作業するために確認されたリソースが確認された後に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="78f83-113">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="78f83-114">この柔軟性により、プロジェクト マネージャーは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="78f83-114">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="78f83-115">WBS 作業パッケージに必要なリソースの数を特定します。</span><span class="sxs-lookup"><span data-stu-id="78f83-115">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="78f83-116">プロジェクト コストを見積もります。</span><span class="sxs-lookup"><span data-stu-id="78f83-116">Estimate project costs.</span></span>
- <span data-ttu-id="78f83-117">暫定予算を決定します。</span><span class="sxs-lookup"><span data-stu-id="78f83-117">Determine a preliminary budget.</span></span>
- <span data-ttu-id="78f83-118">ロールとリソースに基づいて、活動期間を見積もります。</span><span class="sxs-lookup"><span data-stu-id="78f83-118">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="78f83-119">使用可能なプロジェクト情報に基づいて、いくつかのプロジェクト管理計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="78f83-119">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="78f83-120">リソース機能をより効果的に使用するために、WBS に追加オプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="78f83-120">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78f83-121">オプション</span><span class="sxs-lookup"><span data-stu-id="78f83-121">Option</span></span></th>
<th><span data-ttu-id="78f83-122">内容</span><span class="sxs-lookup"><span data-stu-id="78f83-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78f83-123">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="78f83-123">Resource assignments</span></span></td>
<td><span data-ttu-id="78f83-124">WBS でタスクに割り当てられたリソース、日付、時間数、予約の種類を表示します。</span><span class="sxs-lookup"><span data-stu-id="78f83-124">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78f83-125">チームを自動生成</span><span class="sxs-lookup"><span data-stu-id="78f83-125">Auto generate team</span></span></td>
<td><span data-ttu-id="78f83-126">タスクに関連付けられているロールを使用して、計画されたリソースを自動的に追加します。</span><span class="sxs-lookup"><span data-stu-id="78f83-126">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="78f83-127">財務は、ロールに基づく複数条件の意思決定分析を使用して、計画されたリソースを自動的に提案します。</span><span class="sxs-lookup"><span data-stu-id="78f83-127">Finance automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="78f83-128">WBS でタスクにロールと工数 (時間) が設定し、構造がリリースされた後、<strong>チームの自動生成</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-128">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="78f83-129">計画リソースの必要な数が WBS と<strong>プロジェクトとチームのスケジュール</strong> タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="78f83-129">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78f83-130">リソース (ドロップダウン リスト)</span><span class="sxs-lookup"><span data-stu-id="78f83-130">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="78f83-131"><strong>リソース割り当てを起動する</strong>ページで、指定した期間に基づいて、本予約または仮予約へのリソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="78f83-131">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="78f83-132">ビュー設定を調整し、リソース活動の期間を表示および設定できます。</span><span class="sxs-lookup"><span data-stu-id="78f83-132">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="78f83-133">以下のオプションを使用して、作業パッケージ レベルでリソースを選択して割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="78f83-133">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="78f83-134"><strong>同意する</strong> – タスクに割り当てられているリソースへの変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="78f83-134"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="78f83-135"><strong>キャンセル</strong> – タスクに割り当てられているリソースへの変更をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="78f83-135"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="78f83-136"><strong>自動的に割り当てる</strong> – 一致するロールを持つ使用可能なスタッフが配置されたリソースが自動的に選択され、選択したタスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="78f83-136"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="78f83-137">**すべてのプロジェクト** ページで、**XYZ アップグレード フェーズ 2** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-137">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="78f83-138">**計画** > **活動** > **WBS (作業分解構造)** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-138">Select **Plan** > **Activities** > **Work breakdown structure**.</span></span>
3. <span data-ttu-id="78f83-139">**新着** を選択し、次のレベル 1 の活動を WBS に追加します。</span><span class="sxs-lookup"><span data-stu-id="78f83-139">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="78f83-140">開始</span><span class="sxs-lookup"><span data-stu-id="78f83-140">Initiating</span></span>
    - <span data-ttu-id="78f83-141">プランニング</span><span class="sxs-lookup"><span data-stu-id="78f83-141">Planning</span></span>
    - <span data-ttu-id="78f83-142">実行中</span><span class="sxs-lookup"><span data-stu-id="78f83-142">Executing</span></span>
    - <span data-ttu-id="78f83-143">監視とコントロール</span><span class="sxs-lookup"><span data-stu-id="78f83-143">Monitoring and Control</span></span>
    - <span data-ttu-id="78f83-144">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="78f83-144">Close</span></span>

4. <span data-ttu-id="78f83-145">次の図に示すように、日付と工数 (時間) を設定します。</span><span class="sxs-lookup"><span data-stu-id="78f83-145">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="78f83-146">[![日付と工数の設定](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="78f83-146">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="78f83-147">**開始** タスク ライン、**ロール** フィールド、**シニア プロジェクト マネージャー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-147">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="78f83-148">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-148">Select **Publish**.</span></span>
7. <span data-ttu-id="78f83-149">同じラインの、**リソース** フィールドで、**Daniel Goldschmidt**、次に **同意** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-149">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="78f83-150">**計画** タスク ラインを選択し、**ロール** フィールドで、**ビジネス アナリスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-150">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="78f83-151">**公開** を選択し、次に **チームの自動生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-151">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="78f83-152">表示されるメッセージ ボックスで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-152">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="78f83-153">**リソース** フィールドで、値が **ビジネス アナリスト 1** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="78f83-153">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="78f83-154">**ビジネス アナリスト 1** リソースのために、検索を開き、**リソース割り当ての起動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-154">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="78f83-155">次に、タスクの作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-155">Then select a worker for the task.</span></span>
13. <span data-ttu-id="78f83-156">**ソフト割り当て**&gt;**全キャパシティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-156">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="78f83-157">リソースの数が 1 のままであるため、指定したリソースが 2 であるという警告は表示されません。</span><span class="sxs-lookup"><span data-stu-id="78f83-157">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="78f83-158">**作業分解構造** ページで、WBS でのリソース割り当てを検証し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="78f83-158">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]