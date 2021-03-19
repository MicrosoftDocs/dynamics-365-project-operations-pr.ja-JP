---
title: 承認された時間と経費の入力によって作成された実績の一括修正
description: このトピックでは、請求が完了していない場合に、以前承認された時間または経費の入力を、管理者が単一または一括で修正する方法について説明します。
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290905"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="b0da7-103">承認された時間と経費の入力によって作成された実績の一括修正</span><span class="sxs-lookup"><span data-stu-id="b0da7-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b0da7-104">時間や経費の入力が誤入力される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b0da7-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="b0da7-105">たとえば、コンサルタントが時間エントリを作成する際に間違った日付を選択したり、経費を入力する際に数値を入れ替える場合があります。</span><span class="sxs-lookup"><span data-stu-id="b0da7-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="b0da7-106">コンサルタントが送信した入力値を更新できない場合は、管理者がプロジェクトの入力値を直接修正できます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="b0da7-107">このトピックの手順を完了するには、管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="b0da7-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="b0da7-108">承認済みの時間入力を修正する</span><span class="sxs-lookup"><span data-stu-id="b0da7-108">Correct approved time entries</span></span>     

<span data-ttu-id="b0da7-109">プロジェクトの単一または複数の時間入力を修正するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="b0da7-110">**営業** エリアにて、**取引** を選択し、続いて **承認済みの時間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="b0da7-111">**承認済みの時間** リストにて、1 または複数の承認済み時間入力を検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="b0da7-112">フィルターを使用して、関連する入力を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="b0da7-113">たとえば、プロジェクト IDでフィルターし、同じプロジェクト ID で承認されたすべての時間入力を選択できます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="b0da7-114">**入力の修正** の修正を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-114">Select **Correct entries**.</span></span> <span data-ttu-id="b0da7-115">**時間の修正** という割り当てタイプの、新しい修正ジャーナルが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="b0da7-116">選択した入力値がジャーナルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="b0da7-117">**新しいジャーナル** ページで、修正ジャーナルの **説明** を入力し、続いて **時間入力の修正** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="b0da7-118">**時間入力を更新する** セクションで、必要に応じてフィールドを正しい情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="b0da7-119">たとえば、割り当てられたプロジェクトや予約可能なリソースを変更できます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="b0da7-120">**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-120">Select **Preview**.</span></span> <span data-ttu-id="b0da7-121">ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="b0da7-122">**ジャーナル ライン** タブでは、選択した時間項目に関連する元の実績を反転させたものと、作成した修正済みの対応行の一覧を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="b0da7-123">追加の修正を行う必要がある場合は、手順 5 と 6 を繰り返してください。</span><span class="sxs-lookup"><span data-stu-id="b0da7-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="b0da7-124">修正されたすべての実績には、**時間入力を修正する** セクションで選択したものと同じ値が反映されます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="b0da7-125">修正が期待どおりに表示された場合は、**確認** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="b0da7-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="b0da7-126">ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="b0da7-127">**営業** エリアに戻り、**プロジェクト** を選択し、続いて時間入力を更新したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="b0da7-128">**プロジェクト** ページの、**実績** タブで、行った変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="b0da7-129">もし **実績** タブが表示されない場合は、**関連** > **実績** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="b0da7-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="b0da7-130">**実際の関連ビュー** リスト、元の時間が逆になっていても、これに対応する修正済みの時間が表示されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="b0da7-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="b0da7-131">たとえば、次の図では、数量が 8.00 となっている 2 つの明細があり、[金額] 列に借方がリストされています。</span><span class="sxs-lookup"><span data-stu-id="b0da7-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="b0da7-132">さらに、[金額] 列に貸し方の数量を示す、-8.00 となっている 2 つの明細があります。</span><span class="sxs-lookup"><span data-stu-id="b0da7-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="b0da7-133">この修正を行うことで、数量はゼロになります。</span><span class="sxs-lookup"><span data-stu-id="b0da7-133">These corrections bring the quantity to zero.</span></span>

![実績に関連するビューのリスト](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="b0da7-135">承認済みの経費入力を修正する</span><span class="sxs-lookup"><span data-stu-id="b0da7-135">Correct approved expense entries</span></span>

<span data-ttu-id="b0da7-136">次の手順を実行して、1 つまたは複数の経費のエントリを修正します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="b0da7-137">**営業** エリアにて、**取引** 配下にある、左側のナビゲーション ウィンドウで、**承認済みの経費** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="b0da7-138">**承認済みの費用** リストにて、修正するプロジェクトを選択して、**入力値の修正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="b0da7-139">**経費の修正** という割り当てタイプの、新しい修正ジャーナルが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="b0da7-140">**新しいジャーナル** ページで、修正の **説明** を入力し、**経費修正** タブの **経費を修正する** セクションで、選択した経費明細の修正をするデータ フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="b0da7-141">たとえば、費用を別の **プロジェクト** に割り当てる、または **経費区分**、**経費日**、**予約可能なリソース** を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="b0da7-142">**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-142">Select **Preview**.</span></span> <span data-ttu-id="b0da7-143">ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="b0da7-144">**ジャーナル ライン** タブでは修正内容を確認します。選択した支出項目に関連する元の実績を反転させたものと、作成した修正済みの対応行の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="b0da7-145">期待どおりに修正された場合は、**確認** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="b0da7-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="b0da7-146">ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="b0da7-147">値が期待どおりに表示されない場合は、**キャンセル** を選択して **承認済みの費用** リストに戻ってください。</span><span class="sxs-lookup"><span data-stu-id="b0da7-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="b0da7-148">手順 2 から 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="b0da7-149">修正されたすべての実績には、**経費を修正する** セクションで選択したものと同じ値が反映されます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="b0da7-150">修正ジャーナルを確認したら、更新したプロジェクトに戻って変更を表示します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="b0da7-151">プロジェクト ページの **実績** タブ、**実際の関連ビュー** を確認します。</span><span class="sxs-lookup"><span data-stu-id="b0da7-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="b0da7-152">元の入力値と修正された入力値が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0da7-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="b0da7-153">以下の図は、元の経費入力金額と、それに対応する修正後の経費入力金額を示しています。</span><span class="sxs-lookup"><span data-stu-id="b0da7-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![実際の経費](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]