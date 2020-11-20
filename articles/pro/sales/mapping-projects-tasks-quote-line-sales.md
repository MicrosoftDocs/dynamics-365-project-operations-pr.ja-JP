---
title: プロジェクトとタスクをプロジェクトベースの見積依頼明細行にマップする
description: このトピックでは、プロジェクトとタスクをプロジェクトベースのタスク明細行にマップする方法について説明します。
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130719"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="f325e-103">プロジェクトとタスクをプロジェクトベースの見積依頼明細行にマップする</span><span class="sxs-lookup"><span data-stu-id="f325e-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="f325e-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="f325e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f325e-105">プロジェクトベースの見積明細行では、見積依頼明細行にすでに関連付けられているプロジェクトの特定のタスクをマップできます。</span><span class="sxs-lookup"><span data-stu-id="f325e-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="f325e-106">タスクを見積依頼明細行にマップする場合、見積依頼明細行で定義した次の項目は、それらのタスクにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f325e-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="f325e-107">請求方法</span><span class="sxs-lookup"><span data-stu-id="f325e-107">Billing method</span></span>
- <span data-ttu-id="f325e-108">請求可否オプション</span><span class="sxs-lookup"><span data-stu-id="f325e-108">Chargeability options</span></span>
- <span data-ttu-id="f325e-109">上限</span><span class="sxs-lookup"><span data-stu-id="f325e-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="f325e-110">顧客</span><span class="sxs-lookup"><span data-stu-id="f325e-110">Customers</span></span>

<span data-ttu-id="f325e-111">たとえば、1 つのフェーズが固定価格で、他のすべてのフェーズが時間と材料であるプロジェクトがあるとします。</span><span class="sxs-lookup"><span data-stu-id="f325e-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="f325e-112">この場合、固定価格の請求方法を使用するフェーズの見積依頼明細行に、最初のフェーズとそのすべての子タスクを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f325e-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="f325e-113">次に、他のすべてのフェーズを時間および材料ベースの見積依頼明細行に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f325e-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="f325e-114">タスクをプロジェクトベースの見積依頼明細行に関連付ける</span><span class="sxs-lookup"><span data-stu-id="f325e-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="f325e-115">次の場所から、タスクを見積依頼明細行に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f325e-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="f325e-116">**プロジェクト** ページ > **タスクの請求** タブ (最適)</span><span class="sxs-lookup"><span data-stu-id="f325e-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="f325e-117">**見積依頼明細行** ページ > **請求可能タスク** タブ</span><span class="sxs-lookup"><span data-stu-id="f325e-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="f325e-118">プロジェクト ページから</span><span class="sxs-lookup"><span data-stu-id="f325e-118">From the Project page</span></span>

<span data-ttu-id="f325e-119">**プロジェクト** ページは、タスクを見積依頼明細行に関連付けるための最適なエクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f325e-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="f325e-120">このページを使用して複数のタスクを選択し、そのすべてと子タスクを、選択した見積依頼明細行に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f325e-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="f325e-121">プロジェクトベースの見積依頼明細行の **全般** タブで、**プロジェクト** フィールドが入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f325e-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="f325e-122">**含まれるタスク** フィールドで、**選択したタスクのみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="f325e-123">プロジェクトベースの見積依頼明細行を保存します。</span><span class="sxs-lookup"><span data-stu-id="f325e-123">Save the project-based quote line.</span></span> <span data-ttu-id="f325e-124">フォームが更新されると、**請求可能タスク** タブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f325e-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="f325e-125">**全般** タブで、**プロジェクト** フィールドからプロジェクトのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="f325e-126">**プロジェクト** ページで **タスクの請求** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="f325e-127">タスク固有の請求の設定に適用される 2 番目のグリッドで、1 つ以上のタスクを選択してから、**見積依頼明細行を関連付ける** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="f325e-128">表示されるダイアログ ページで、見積もりでプロジェクトベースの見積依頼明細行を表示する見積依頼明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="f325e-129">**請求の種類** フィールドで、これらのタスクが請求可能か請求不可かを示します。</span><span class="sxs-lookup"><span data-stu-id="f325e-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="f325e-130">チェック ボックスをオンにして、選択したタスクの子タスクを関連付けに含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f325e-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="f325e-131">チェック ボックスをオンにすると、選択したタスクの子タスクが見積依頼明細行に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f325e-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="f325e-132">**OK** を選択してダイアログを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f325e-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="f325e-133">見積依頼明細行ページから</span><span class="sxs-lookup"><span data-stu-id="f325e-133">From the Quote line page</span></span>

<span data-ttu-id="f325e-134">**見積依頼明細行** ページの **請求可能タスク** タブからプロジェクト タスクを見積依頼明細行に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f325e-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="f325e-135">プロジェクト タスクを見積依頼明細行に関連付けるのに最適な場所は、**プロジェクト** ページの **タスクの請求** タブです。</span><span class="sxs-lookup"><span data-stu-id="f325e-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="f325e-136">**見積依頼明細行** ページの **請求可能タスク** タブからタスクを関連付ける場合、各プロジェクトを手動で関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f325e-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="f325e-137">プロジェクトベースの見積依頼明細行の **全般** タブで、**プロジェクト** フィールドでプロジェクトが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f325e-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="f325e-138">**含まれるタスク** フィールドで、**選択したタスクのみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="f325e-139">プロジェクトベースの見積依頼明細行を保存します。</span><span class="sxs-lookup"><span data-stu-id="f325e-139">Save the project-based quote line.</span></span> <span data-ttu-id="f325e-140">フォームが更新されると、**請求可能タスク** タブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f325e-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="f325e-141">**請求可能タスク** タブで、**見積依頼明細行タスクの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="f325e-142">**見積依頼明細行タスク** ページの **タスク** フィールドでタスクを選択して、**請求の種類** フィールドで **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="f325e-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f325e-143">Close the page.</span></span> <span data-ttu-id="f325e-144">選択したタスクが見積依頼明細行に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f325e-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="f325e-145">タスクをプロジェクトベースの見積依頼明細行から関連付け解除する</span><span class="sxs-lookup"><span data-stu-id="f325e-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="f325e-146">プロジェクト ページから</span><span class="sxs-lookup"><span data-stu-id="f325e-146">From the Project page</span></span>

<span data-ttu-id="f325e-147">このメソッドは、タスクを見積依頼明細行から関連付け解除するための最も最適なエクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f325e-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="f325e-148">このページを使用して複数のタスクを選択し、そのすべてと子タスクを、選択した見積依頼明細行から関連付け解除することができます。</span><span class="sxs-lookup"><span data-stu-id="f325e-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="f325e-149">プロジェクトベースの見積依頼明細行の **全般** タブで、**プロジェクト** フィールドでプロジェクト リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="f325e-150">**プロジェクト** ページで **タスクの請求** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="f325e-151">タスク固有の請求の設定に適用される 2 番目のグリッドで、1 つ以上のタスクを選択してから、**見積依頼明細行の関連付けを解除する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="f325e-152">表示されるダイアログ ページで、見積依頼明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="f325e-153">チェック ボックスをオンにして、選択したタスクの子タスクの関連付けも削除するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f325e-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="f325e-154">チェック ボックスをオンにすると、選択したタスクの子タスクも見積依頼明細行から関連付け解除されます。</span><span class="sxs-lookup"><span data-stu-id="f325e-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="f325e-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-155">Select **OK**.</span></span> <span data-ttu-id="f325e-156">この関連付けを削除すると、警告メッセージは、タスクに以前に記録された実績が取り消される可能性があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="f325e-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="f325e-157">**OK** を選択して続行し、タスクとプロジェクトベースの見積依頼明細行の間の関連付けを削除します。</span><span class="sxs-lookup"><span data-stu-id="f325e-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="f325e-158">見積依頼明細行ページから</span><span class="sxs-lookup"><span data-stu-id="f325e-158">From the Quote line page</span></span>

<span data-ttu-id="f325e-159">**見積依頼明細行** ページの **請求可能タスク** タブで、プロジェクト タスクを見積依頼明細行から関連付け削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="f325e-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="f325e-160">**請求可能タスク** タブで、**見積依頼明細行タスクの削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="f325e-161">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f325e-161">Select **OK**.</span></span> <span data-ttu-id="f325e-162">この関連付けを削除すると、警告メッセージは、タスクに以前に記録された実績が取り消される可能性があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="f325e-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="f325e-163">**OK** を選択して続行し、タスクとプロジェクトベースの見積依頼明細行の間の関連付けを削除します。</span><span class="sxs-lookup"><span data-stu-id="f325e-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="f325e-164">この手順では、プロジェクトからタスクは削除されません。</span><span class="sxs-lookup"><span data-stu-id="f325e-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="f325e-165">プロジェクトベースの見積依頼明細行からタスクの関連付けを削除するだけです。</span><span class="sxs-lookup"><span data-stu-id="f325e-165">It only removes the task association from the project-based quote line.</span></span>
