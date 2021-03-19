---
title: 会計年度の終わりにプロジェクトの予算を転送する
description: この記事では、残りの予算金額を将来の年度に振り替え、予算登録の詳細を作成する方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289735"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="602b3-103">会計年度の終わりにプロジェクトの予算を転送する</span><span class="sxs-lookup"><span data-stu-id="602b3-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="602b3-104">複数年にわたるプロジェクトに取り組む場合、会計年度の終わりに予算が残っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="602b3-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="602b3-105">残りの予算金額を将来の年度に振り替え、関連する総勘定元帳勘定で金額に予算登録の詳細を作成できます。</span><span class="sxs-lookup"><span data-stu-id="602b3-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="602b3-106">残りの金額を繰り越す前に、残りの予算金額を確認して分析します。</span><span class="sxs-lookup"><span data-stu-id="602b3-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="602b3-107">残りの予算金額を確認および分析する</span><span class="sxs-lookup"><span data-stu-id="602b3-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="602b3-108">次の手順を実行して、プロジェクトの年末の予算金額を確認しますが、金額を繰り越さないでください。</span><span class="sxs-lookup"><span data-stu-id="602b3-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="602b3-109">**プロジェクト管理および会計** > **定期処理** > **予算** > **繰越予算** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="602b3-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="602b3-110">**プロジェクト予算の繰り越しプロセス** ページの **年度末オプション** タブで、**残りのプロジェクト予算金額を繰り越す** が有効になっていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="602b3-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="602b3-111">**パラメーター** タブの **プロジェクト予算年度** フィールドで、残りの予算金額を表示する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="602b3-112">**開始会計年度** フィールドで、残りの予算金額を表示する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="602b3-113">**予測モデルから** フィールドで、**予算残高** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="602b3-114">選択した条件を満たし、予算残高がないプロジェクトを含めるには、**残りゼロを表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="602b3-115">**予算の選択** タブで **すべての予算を取得** を選択し、選択した条件に一致するすべての予算を読み込み、**プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="602b3-116">特定の予算セットをペインに読み込むデータベース クエリを設計するには、**選択した予算を取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="602b3-117">ペイン内の特定の行の詳細については、行を選択してから、**予算の詳細を表示** または **アカウントを表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="602b3-118">残りの予算金額を繰り越す</span><span class="sxs-lookup"><span data-stu-id="602b3-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="602b3-119">残りの予算金額を処理するときに、繰越金額のトランザクションを総勘定元帳に作成できます。</span><span class="sxs-lookup"><span data-stu-id="602b3-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="602b3-120">総勘定元帳トランザクションを作成するには、[予算金額の繰越と総勘定元帳トランザクションの作成](#carry-forward) セクションの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="602b3-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="602b3-121">繰り越された予算金額は、繰越予測モデルとして **予測モデル** ページで選択された予測モデルに転送されます。</span><span class="sxs-lookup"><span data-stu-id="602b3-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="602b3-122">予算金額の繰越と総勘定元帳トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="602b3-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="602b3-123">**プロジェクト管理および会計** > **定期処理** > **予算** > **繰越予算** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="602b3-124">**プロジェクト予算の繰り越しプロセス** ページで **年度末** を選択し、**残りのプロジェクト予算金額を繰り越す** と **総勘定元帳で予算登録エントリの作成** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="602b3-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="602b3-125">**パラメーター** タブの **プロジェクト パラメーター** フィールド グループで、以下を選択します:</span><span class="sxs-lookup"><span data-stu-id="602b3-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="602b3-126">**プロジェクト予算年度**: 残りの予算金額を表示する会計年度の初めを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="602b3-127">**損益**: 総勘定元帳で損益トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="602b3-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="602b3-128">**WIP**: 総勘定元帳で仕掛品 (WIP) トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="602b3-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="602b3-129">**給与**: 総勘定元帳で給与配賦トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="602b3-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="602b3-130">**総勘定元帳** フィールド グループで、次の情報を入力します:</span><span class="sxs-lookup"><span data-stu-id="602b3-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="602b3-131">**開始会計年度** フィールドで、プロジェクトの残りの予算金額を転送する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="602b3-132">既定値は、**プロジェクト予算年度** フィールドの値の 1 年後です。</span><span class="sxs-lookup"><span data-stu-id="602b3-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="602b3-133">**繰越期間** フィールドで、総勘定元帳に予算登録の詳細を作成する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="602b3-134">これは通常、開始会計年度の 1 期目です。</span><span class="sxs-lookup"><span data-stu-id="602b3-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="602b3-135">**コピー元/先** フィールド グループで、次の情報を入力します:</span><span class="sxs-lookup"><span data-stu-id="602b3-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="602b3-136">**予測モデルから** フィールドで、プロジェクトに転送する残りの予算金額に関連付けられているプロジェクト予算の予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="602b3-137">**元帳予算モデルへ** フィールドで、総勘定元帳に転送する予算金額に関連付けられている元帳予算モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="602b3-138">**販売通貨の転送** を選択して、プロジェクトの予算金額を転送するときに作成される総勘定元帳トランザクションに、プロジェクトの販売通貨を使用します。</span><span class="sxs-lookup"><span data-stu-id="602b3-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="602b3-139">オプションが選択されていない場合、トランザクションは会計通貨を使用します。</span><span class="sxs-lookup"><span data-stu-id="602b3-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="602b3-140">**残りゼロを表示** を選択して、残りの予算金額がないが、下部ペインに表示されるプロジェクトで選択した他の条件を満たすプロジェクトを含めます。</span><span class="sxs-lookup"><span data-stu-id="602b3-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="602b3-141">**予算の選択** タブで **すべての予算を取得** を選択し、選択した条件に一致するすべての予算を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="602b3-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="602b3-142">特定のプロジェクト予算セットをペインに読み込むデータベース クエリを設計する場合は、**選択した予算を取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="602b3-143">処理するプロジェクトごとに、プロジェクトの行の先頭にあるオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="602b3-144">すべてまたはほとんどのプロジェクトを選択するには、左上隅のチェック マークを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="602b3-145">プロジェクトの処理を除外するには、そのプロジェクトのチェック マークをクリアします。</span><span class="sxs-lookup"><span data-stu-id="602b3-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="602b3-146">選択したプロジェクトの残りの予算金額を選択した会計年度に転送し、総勘定元帳に予算登録の詳細を作成するには、**プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="602b3-147">総勘定元帳トランザクションを作成せずに予算金額を繰り越す</span><span class="sxs-lookup"><span data-stu-id="602b3-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="602b3-148">**プロジェクト管理および会計** > **定期処理** > **予算** > **繰越予算** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="602b3-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="602b3-149">**プロジェクト予算の繰り越しプロセス** ページの **年度末オプション** フィールドで、**残りのプロジェクト予算金額を繰り越す** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="602b3-150">**パラメーター** グループの **プロジェクト予算年度** フィールドで、残りの予算金額を表示する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="602b3-151">**コピー元/先** グループで、次の情報を入力します:</span><span class="sxs-lookup"><span data-stu-id="602b3-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="602b3-152">**予測モデルから** フィールドで、プロジェクトに転送する残りの予算金額に関連付けられているプロジェクト予算の予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="602b3-153">残りの予算残高はないが、選択した他の条件を満たすプロジェクトを含めるには、**残りゼロを表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="602b3-154">**予算の選択** グループで **すべての予算を取得** を選択し、選択した条件に一致するすべての予算を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="602b3-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="602b3-155">特定のプロジェクト予算セットをペインに読み込むデータベース クエリを設計するには、**選択した予算を取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="602b3-156">処理するプロジェクトごとに、プロジェクトの行の先頭にあるオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="602b3-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="602b3-157">**プロセス** を選択して、選択したプロジェクトの残りの予算金額を選択した会計年度に転送します。</span><span class="sxs-lookup"><span data-stu-id="602b3-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]