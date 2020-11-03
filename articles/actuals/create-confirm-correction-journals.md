---
title: 修正された仕訳帳の作成と確認
description: このトピックでは、修正された仕訳帳の作成と確認方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 855593df1ea14827f06961dda5b4becd2fa75c18
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079265"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="4deb3-103">修正された仕訳帳の作成と確認</span><span class="sxs-lookup"><span data-stu-id="4deb3-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="4deb3-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="4deb3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4deb3-105">時間や経費の入力が誤入力される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4deb3-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="4deb3-106">たとえば、コンサルタントが時間エントリを作成する際に間違った日付を選択したり、経費を入力する際に数値を入れ替える場合があります。</span><span class="sxs-lookup"><span data-stu-id="4deb3-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="4deb3-107">コンサルタントが送信した入力値を更新できない場合は、管理者がプロジェクトの入力値を直接修正できます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="4deb3-108">このトピックの手順を完了するには、管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="4deb3-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="4deb3-109">承認済みの時間入力を修正する</span><span class="sxs-lookup"><span data-stu-id="4deb3-109">Correct approved time entries</span></span>     

<span data-ttu-id="4deb3-110">プロジェクトの単一または複数の時間入力を修正するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="4deb3-111">**営業** エリアにて、 **取引** を選択し、続いて **承認済みの時間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-111">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="4deb3-112">**承認済みの時間** リストにて、1 または複数の承認済み時間入力を検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="4deb3-113">フィルターを使用して、関連する入力を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="4deb3-114">たとえば、プロジェクト IDでフィルターし、同じプロジェクト ID で承認されたすべての時間入力を選択できます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="4deb3-115">**入力の修正** の修正を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-115">Select **Correct entries**.</span></span> <span data-ttu-id="4deb3-116">**時間の修正** という割り当てタイプの、新しい修正ジャーナルが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="4deb3-117">選択した入力値がジャーナルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="4deb3-118">**新しいジャーナル** ページで、修正ジャーナルの **説明** を入力し、続いて **時間入力の修正** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="4deb3-119">**時間入力を更新する** セクションで、必要に応じてフィールドを正しい情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="4deb3-120">たとえば、割り当てられたプロジェクトや予約可能なリソースを変更できます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="4deb3-121">**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-121">Select **Preview**.</span></span> <span data-ttu-id="4deb3-122">ダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="4deb3-123">**ジャーナル ライン** タブでは、選択した時間項目に関連する元の実績を反転させたものと、作成した修正済みの対応行の一覧を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="4deb3-124">追加の修正を行う必要がある場合は、手順 5 と 6 を繰り返してください。</span><span class="sxs-lookup"><span data-stu-id="4deb3-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="4deb3-125">修正されたすべての実績には、 **時間入力を修正する** セクションで選択したものと同じ値が反映されます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="4deb3-126">修正が期待どおりに表示された場合は、 **確認** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="4deb3-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="4deb3-127">ダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="4deb3-128">**営業** エリアに戻り、 **プロジェクト** を選択し、続いて時間入力を更新したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-128">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="4deb3-129">**プロジェクト** ページの、 **実績** タブで、行った変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="4deb3-130">もし **実績** タブが表示されない場合は、 **関連** > **実績** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="4deb3-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="4deb3-131">**実際の関連ビュー** リスト、元の時間が逆になっていても、これに対応する修正済みの時間が表示されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="4deb3-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="4deb3-132">たとえば、次の図では、数量が 8.00 となっている 2 つの明細があり、[金額] 列に借方がリストされています。</span><span class="sxs-lookup"><span data-stu-id="4deb3-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="4deb3-133">さらに、[金額] 列に貸し方の数量を示す、-8.00 となっている 2 つの明細があります。</span><span class="sxs-lookup"><span data-stu-id="4deb3-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="4deb3-134">この修正を行うことで、数量はゼロになります。</span><span class="sxs-lookup"><span data-stu-id="4deb3-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="4deb3-135">承認済みの経費入力を修正する</span><span class="sxs-lookup"><span data-stu-id="4deb3-135">Correct approved expense entries</span></span>

<span data-ttu-id="4deb3-136">次の手順を実行して、1 つまたは複数の経費のエントリを修正します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="4deb3-137">**営業** エリアにて、 **取引** 配下にある、左側のナビゲーション ウィンドウで、 **承認済みの経費** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="4deb3-138">**承認済みの費用** リストにて、修正するプロジェクトを選択して、 **入力値の修正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="4deb3-139">**経費の修正** という割り当てタイプの、新しい修正ジャーナルが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="4deb3-140">**新しいジャーナル** ページで、修正の **説明** を入力し、 **経費修正** タブの **経費を修正する** セクションで、選択した経費明細の修正をするデータ フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="4deb3-141">たとえば、費用を別の **プロジェクト** に割り当てる、または **経費区分** 、 **経費日** 、 **予約可能なリソース** を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="4deb3-142">**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-142">Select **Preview**.</span></span> <span data-ttu-id="4deb3-143">ダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="4deb3-144">**ジャーナル ライン** タブでは修正内容を確認します。選択した支出項目に関連する元の実績を反転させたものと、作成した修正済みの対応行の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="4deb3-145">期待どおりに修正された場合は、 **確認** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="4deb3-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="4deb3-146">ダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="4deb3-147">値が期待どおりに表示されない場合は、 **キャンセル** を選択して **承認済みの費用** リストに戻ってください。</span><span class="sxs-lookup"><span data-stu-id="4deb3-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="4deb3-148">手順 2 から 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="4deb3-149">修正されたすべての実績には、 **経費を修正する** セクションで選択したものと同じ値が反映されます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="4deb3-150">修正ジャーナルを確認したら、更新したプロジェクトに戻って変更を表示します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="4deb3-151">プロジェクト ページの **実績** タブ、 **実際の関連ビュー** を確認します。</span><span class="sxs-lookup"><span data-stu-id="4deb3-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="4deb3-152">元の入力値と修正された入力値が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4deb3-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="4deb3-153">以下の図は、元の経費入力金額と、それに対応する修正後の経費入力金額を示しています。</span><span class="sxs-lookup"><span data-stu-id="4deb3-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


