---
title: プロジェクトとタスクをプロジェクトベースの契約品目にマップする - Lite
description: このトピックは、契約品目へのプロジェクトとタスクの追加と削除に関する情報を提供します。
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b86e03192625b0dabb89080f2ade1ed9e3567cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994638"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a><span data-ttu-id="5494f-103">プロジェクトとタスクをプロジェクトベースの契約品目にマップする</span><span class="sxs-lookup"><span data-stu-id="5494f-103">Map projects and tasks to a project-based contract line</span></span> 

<span data-ttu-id="5494f-104">_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5494f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5494f-105">プロジェクトベースの契約品目では、プロジェクト内の特定のタスクを契約品目にマップできます。</span><span class="sxs-lookup"><span data-stu-id="5494f-105">On project-based contract lines, you can map specific tasks in a project to the contract line.</span></span>

<span data-ttu-id="5494f-106">特定のタスクを契約品目にマップする場合、契約品目で定義された請求方法、課金オプション、上限、および顧客は、それらの特定のタスクにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="5494f-106">When you map specific tasks to a contract line, the billing method, chargeability options, Not-to-exceed limits, and the customers defined on the contract line will be applicable to those specific tasks only.</span></span>

<span data-ttu-id="5494f-107">プロジェクトの 1 つのフェーズ (たとえば、プロトタイプ フェーズ) が固定価格であり、他のすべてのフェーズが時間と材料であるシナリオがある場合、固定価格の請求方法を使用して、プロトタイプ フェーズと関連するすべての子タスクを、そのフェーズの契約品目に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5494f-107">If you have a scenario where one phase of a project, for example the Prototype Phase, is fixed price and all the other phases are time and material, you will be able to associate the Prototype phase and all the associated child tasks to the contract line for that phase with a fixed price billing method.</span></span>

<span data-ttu-id="5494f-108">プロジェクトの作業分解図 (WBS) の他のすべてのフェーズは、時間および材料ベースの契約品目に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5494f-108">All the other phases in your project work breakdown structure (WBS) can be associated to the time and material-based contract line.</span></span>

## <a name="associate-tasks-to-project-based-contract-lines"></a><span data-ttu-id="5494f-109">プロジェクトベースの契約品目にタスクを関連付ける</span><span class="sxs-lookup"><span data-stu-id="5494f-109">Associate tasks to project-based contract lines</span></span>

<span data-ttu-id="5494f-110">タスクは、**契約品目** ページの **請求可能タスク** タブ、または **プロジェクト** ページの **タスクの請求** タブから契約品目に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5494f-110">Tasks can be associated to contract lines from the **Chargeable Tasks** tab on the **Contract Line** page or from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="5494f-111">契約品目ページから</span><span class="sxs-lookup"><span data-stu-id="5494f-111">From the Contract line page</span></span>

<span data-ttu-id="5494f-112">次の手順を実行して、プロジェクト タスクを **契約品目** ページの **請求可能タスク** タブから契約品目に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="5494f-112">Complete the following steps to associate project tasks to the contract line from the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="5494f-113">プロジェクトベース契約品目の **全般** タブで、**プロジェクト** が入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5494f-113">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="5494f-114">**含まれるタスク** フィールドで **選択したタスクのみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-114">In the **Included Tasks** field, select the **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="5494f-115">変更を保存。</span><span class="sxs-lookup"><span data-stu-id="5494f-115">Save your changes.</span></span> <span data-ttu-id="5494f-116">フォームが更新され、**請求可能タスク** タブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5494f-116">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span>
4. <span data-ttu-id="5494f-117">**請求可能タスク** タブを選択し、サブグリッドで **契約品目タスクを追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-117">Select the **Chargeable Tasks** tab, and in the subgrid, select **Add a Contract Line Task**.</span></span>
5. <span data-ttu-id="5494f-118">**契約品目タスク** ページの **タスク** ドロップダウンで、タスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-118">On the **Contract Line Tasks** page, in the **Tasks** drop-down, select the task.</span></span> 
6. <span data-ttu-id="5494f-119">**請求の種類** フィールドに情報を入力し、**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-119">Enter information in the **Billing Type** field, and then select **Save and Close**.</span></span> <span data-ttu-id="5494f-120">選択したタスクは契約品目に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="5494f-120">The selected task is associated to the contract line.</span></span>

> [!NOTE]
> <span data-ttu-id="5494f-121">これは、プロジェクト タスクを契約品目に関連付けるための最も最適なエクスペリエンスではありません。</span><span class="sxs-lookup"><span data-stu-id="5494f-121">This is not the most optimal experience for associating project tasks to contract lines.</span></span> <span data-ttu-id="5494f-122">このエクスペリエンスでは、各プロジェクトを手動で関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5494f-122">Each project will have to be manually associated in this experience.</span></span> <span data-ttu-id="5494f-123">推奨される方法は、**プロジェクト** ページの **タスクの請求** タブからです。</span><span class="sxs-lookup"><span data-stu-id="5494f-123">The preferred way is from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="5494f-124">プロジェクト ページから</span><span class="sxs-lookup"><span data-stu-id="5494f-124">From the project page</span></span>

<span data-ttu-id="5494f-125">これは、タスクを契約品目に関連付ける最適な方法です。</span><span class="sxs-lookup"><span data-stu-id="5494f-125">This is the optimal method to associate tasks to contract lines.</span></span> <span data-ttu-id="5494f-126">複数のタスクを選択して、それらすべてとその子タスクを選択した契約品目に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5494f-126">You can select multiple tasks and associate all of the them and their child tasks to the selected contract line.</span></span> <span data-ttu-id="5494f-127">次の手順を実行して、タスクを **プロジェクト** ページから契約品目に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="5494f-127">Complete the following steps to associate tasks to the contract line from the **Project** page.</span></span>

1. <span data-ttu-id="5494f-128">プロジェクトベース契約品目の **全般** タブで、**プロジェクト** が入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5494f-128">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="5494f-129">**含まれるタスク** フィールドで **選択したタスクのみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-129">On the **Included Tasks** field, select **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="5494f-130">プロジェクトベースの契約品目を保存します。</span><span class="sxs-lookup"><span data-stu-id="5494f-130">Save the project-based contract line.</span></span> <span data-ttu-id="5494f-131">フォームが更新され、**請求可能タスク** タブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5494f-131">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span> <span data-ttu-id="5494f-132">これは検証のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="5494f-132">This is just for verification purposes only.</span></span>
4. <span data-ttu-id="5494f-133">プロジェクトベース契約品目の **全般** タブにある **プロジェクト** フィールドで、プロジェクト リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-133">On the **General** tab of the project-based contract line, in the **Project** field, select the project link.</span></span>
5. <span data-ttu-id="5494f-134">**プロジェクト** ページで、**タスクの請求の設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-134">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
6. <span data-ttu-id="5494f-135">2 つのグリッドがあります。</span><span class="sxs-lookup"><span data-stu-id="5494f-135">There are two grids.</span></span> <span data-ttu-id="5494f-136">1 つのグリッドは、プロジェクト全体に適用される契約品目用です。</span><span class="sxs-lookup"><span data-stu-id="5494f-136">One grid is for contract lines that apply to the whole project.</span></span> <span data-ttu-id="5494f-137">2 番目のグリッドは、タスク固有の請求設定に適用されます。</span><span class="sxs-lookup"><span data-stu-id="5494f-137">The second grid applies to task-specific billing setup.</span></span> <span data-ttu-id="5494f-138">2 番目のグリッドで 1 つ以上のタスクを選択してから、**契約品目の関連付け** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-138">In the second grid, select one or more tasks, and then select **Associate Contract Lines**.</span></span>
7. <span data-ttu-id="5494f-139">表示されるダイアログ ページで、ドロップダウンから契約品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-139">In the dialog page that opens, select a contract line from the drop-down.</span></span>
8. <span data-ttu-id="5494f-140">**請求の種類** ドロップダウンを使用して、タスクを請求可能または請求不可としてマークします。</span><span class="sxs-lookup"><span data-stu-id="5494f-140">Use the **Billing Type** drop-down to mark the tasks as chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="5494f-141">選択したタスクの子タスクも関連付けに含めるかどうかを示すには、チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-141">Select the check box to indicate if the association should also include child tasks of the selected tasks.</span></span> <span data-ttu-id="5494f-142">このボックスをオンにすると、選択したタスクの子タスクも契約品目に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5494f-142">Checking the box will also associate the child tasks of the selected tasks to the contract line.</span></span>
10. <span data-ttu-id="5494f-143">**OK** を選択してダイアログを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5494f-143">Select **OK** to close the dialog.</span></span>

## <a name="unassociate-tasks-from-project-based-contract-lines"></a><span data-ttu-id="5494f-144">プロジェクトベースの契約品目からタスクの関連付けを解除する</span><span class="sxs-lookup"><span data-stu-id="5494f-144">Unassociate tasks from project-based contract lines</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="5494f-145">契約品目ページから</span><span class="sxs-lookup"><span data-stu-id="5494f-145">From the contract line page</span></span>

<span data-ttu-id="5494f-146">次の手順を実行して、**契約品目** ページにある **請求可能タスク** タブの契約品目からプロジェクト タスクの関連付けを解除します。</span><span class="sxs-lookup"><span data-stu-id="5494f-146">Complete the following steps to unassociate project tasks from the contract line on the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="5494f-147">**請求可能タスク** タブで、**契約品目タスクを削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-147">On the **Chargeable Tasks** tab, select **Delete a Contract Line Task**.</span></span>
2. <span data-ttu-id="5494f-148">警告メッセージは、この関連付けを削除すると、タスクに以前に記録された実績が取り消される可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="5494f-148">A warning message indicates that removing this association could result in reversal of any actuals previously recorded on the task.</span></span> <span data-ttu-id="5494f-149">ダイアログで **OK** を選択し、タスクとプロジェクトベースの契約品目間の関連付けを削除します。</span><span class="sxs-lookup"><span data-stu-id="5494f-149">Select **OK** on the dialog to remove the association between the task and the project-based contract line.</span></span> 

> [!NOTE]
> <span data-ttu-id="5494f-150">これは、プロジェクトからタスクを削除しません。</span><span class="sxs-lookup"><span data-stu-id="5494f-150">This doesn't delete the task from the project.</span></span> <span data-ttu-id="5494f-151">代わりに、プロジェクトベースの契約品目からタスクの関連付けを削除します。</span><span class="sxs-lookup"><span data-stu-id="5494f-151">Instead, it removes the task association from the project-based contract line.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="5494f-152">プロジェクト ページから</span><span class="sxs-lookup"><span data-stu-id="5494f-152">From the project page</span></span>

<span data-ttu-id="5494f-153">これは、契約品目からタスクの関連付けを解除するためのより最適なエクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="5494f-153">This is the more optimal experience for unassociating tasks from contract lines.</span></span> <span data-ttu-id="5494f-154">複数のタスクを選択して、選択した契約品目から、それらすべてとその子タスクの関連付けを解除できます。</span><span class="sxs-lookup"><span data-stu-id="5494f-154">You can select multiple tasks and unassociate all of the them and their child tasks from the selected contract line.</span></span> <span data-ttu-id="5494f-155">次の手順を実行して、契約品目からタスクの関連付けを解除します。</span><span class="sxs-lookup"><span data-stu-id="5494f-155">Complete the following steps to unassociate tasks from the contract line.</span></span>

1. <span data-ttu-id="5494f-156">プロジェクトベース契約品目の **全般** タブから、**プロジェクト** フィールドのプロジェクトのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5494f-156">From **General** tab of the project-based contract line, in the **Project** field, click on the link for project.</span></span>
2. <span data-ttu-id="5494f-157">**プロジェクト** ページで、**タスクの請求の設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-157">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
3. <span data-ttu-id="5494f-158">ページには 2 つのグリッドがあります。</span><span class="sxs-lookup"><span data-stu-id="5494f-158">There are two grids on the page.</span></span> <span data-ttu-id="5494f-159">1 つのグリッドは、プロジェクト全体に適用される契約品目用で、もう 1 つはタスク固有の請求設定に適用されます。</span><span class="sxs-lookup"><span data-stu-id="5494f-159">One grid is for contract lines that apply to the whole project and the second applies to task-specific billing setup.</span></span> <span data-ttu-id="5494f-160">2 番目のグリッドで 1 つ以上のタスクを選択してから、**契約品目の関連付け解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-160">In the second grid, select one or more tasks and the select **Disassociate Contract Lines**.</span></span>
4. <span data-ttu-id="5494f-161">表示されるダイアログ ページで、ドロップダウンから契約品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-161">In the  dialog page that opens, select a contract line from the drop-down.</span></span>
5. <span data-ttu-id="5494f-162">選択したタスクの子タスクからも関連付けを削除するかどうかを示すには、チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-162">Select the check box to indicate if the association should also be removed from any child tasks of the selected tasks.</span></span> <span data-ttu-id="5494f-163">このボックスをオンにすると、契約品目から選択したタスクの子タスクの関連付けも解除されます。</span><span class="sxs-lookup"><span data-stu-id="5494f-163">Checking the box will also unassociate the child tasks of the selected tasks from the contract line.</span></span>
6. <span data-ttu-id="5494f-164">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5494f-164">Select **OK**.</span></span> <span data-ttu-id="5494f-165">警告メッセージは、この関連付けを削除すると、以前にタスクに記録された実績が取り消される可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="5494f-165">A warning message indicates that removing this association could result in reversal of any actuals recorded on the task previously.</span></span> <span data-ttu-id="5494f-166">警告ダイアログで **OK** を選択し、タスクとプロジェクトベースの契約品目間の関連付けを削除します。</span><span class="sxs-lookup"><span data-stu-id="5494f-166">Select **OK** on the warning dialog to remove the association between the task and the project-based contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
