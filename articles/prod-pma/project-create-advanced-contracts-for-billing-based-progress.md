---
title: 進捗状況に基づいた請求のための詳細な契約を作成する
description: このトピックでは、完了した作業の割合に基づいて顧客の請求書を生成できるように、プロジェクト契約を作成する方法について説明します。
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079397"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="491bc-103">進捗状況に基づいた請求のための詳細な契約を作成する</span><span class="sxs-lookup"><span data-stu-id="491bc-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="491bc-104">このトピックでは、完了した作業の割合に基づいて顧客の請求書を作成できるように、プロジェクト契約を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="491bc-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="491bc-105">請求書の金額は、プロジェクトに設定した作業の予算カテゴリに対して自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="491bc-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="491bc-106">請求書のタイミングは、顧客とプロジェクト契約を交渉するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="491bc-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="491bc-107">このトピックの手順を使用して、契約、関連プロジェクト、およびプロジェクトに設定した作業の予算カテゴリに対して請求額を計算する請求ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="491bc-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="491bc-108">契約とプロジェクトを作成したら、プロジェクトの詳細を設定できます。</span><span class="sxs-lookup"><span data-stu-id="491bc-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="491bc-109">たとえば、アクティビティを定義し、プロジェクトに従業者を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="491bc-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="491bc-110">例</span><span class="sxs-lookup"><span data-stu-id="491bc-110">Example</span></span>

<span data-ttu-id="491bc-111">あなたの組織はソフトウェア開発会社です。</span><span class="sxs-lookup"><span data-stu-id="491bc-111">Your organization is a software development firm.</span></span> <span data-ttu-id="491bc-112">合計 20,000 米国ドル (USD) の顧客向けの給与計算パッケージを開発することに同意します。</span><span class="sxs-lookup"><span data-stu-id="491bc-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="491bc-113">プロジェクトの特定の割合を完了したら、組織は顧客に請求することに同意します。</span><span class="sxs-lookup"><span data-stu-id="491bc-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="491bc-114">請求プロセスで使用できるように、作業に対して次のプロジェクト カテゴリを設定します:</span><span class="sxs-lookup"><span data-stu-id="491bc-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="491bc-115">コンサルティング</span><span class="sxs-lookup"><span data-stu-id="491bc-115">Consulting</span></span>
- <span data-ttu-id="491bc-116">デザイン</span><span class="sxs-lookup"><span data-stu-id="491bc-116">Design</span></span>
- <span data-ttu-id="491bc-117">インストール</span><span class="sxs-lookup"><span data-stu-id="491bc-117">Installation</span></span>

<span data-ttu-id="491bc-118">また、各カテゴリで完了したプロジェクト作業の割合に対する請求金額を自動的に計算する請求ルールも設定します。</span><span class="sxs-lookup"><span data-stu-id="491bc-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="491bc-119">予算マネージャーは、プロジェクト カテゴリに対して予算を作成します。</span><span class="sxs-lookup"><span data-stu-id="491bc-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="491bc-120">完了した作業の量は、予算金額と比較した実際の作業の割合として自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="491bc-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="491bc-121">前提条件</span><span class="sxs-lookup"><span data-stu-id="491bc-121">Prerequisites</span></span>

<span data-ttu-id="491bc-122">請求ルールを使用するプロジェクトを作成する前に、請求ルールの番号シーケンスと、進捗請求の転記に使用する料金仕訳を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="491bc-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="491bc-123">**プロジェクト管理および会計** \> **設定** \> **プロジェクト管理および会計パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="491bc-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="491bc-124">**プロジェクト管理および会計パラメーター** ページの **番号シーケンス** タブで、請求ルールの作成時に使用する番号シーケンスを設定します。</span><span class="sxs-lookup"><span data-stu-id="491bc-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="491bc-125">**プロジェクト管理および会計** \> **仕訳** \> **料金** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="491bc-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="491bc-126">**料金仕訳** ページで **新規** を選択し、仕訳名を入力します。</span><span class="sxs-lookup"><span data-stu-id="491bc-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="491bc-127">進捗請求の契約を作成する</span><span class="sxs-lookup"><span data-stu-id="491bc-127">Create a contract for progress billings</span></span>

<span data-ttu-id="491bc-128">この手順を使用して、固定価格プロジェクトに対してプロジェクト契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="491bc-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="491bc-129">プロジェクトで完了した作業が指定された割合に達したときに、プロジェクト請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="491bc-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="491bc-130">**プロジェクト管理および会計** \> **プロジェクト** \> **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="491bc-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="491bc-131">**プロジェクト契約** ページで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="491bc-132">**新しいプロジェクト契約** ダイアログ ボックスで、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="491bc-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="491bc-133">**名前**</span><span class="sxs-lookup"><span data-stu-id="491bc-133">**Name**</span></span>
    - <span data-ttu-id="491bc-134">**資金調達の種類**</span><span class="sxs-lookup"><span data-stu-id="491bc-134">**Funding type**</span></span>
    - <span data-ttu-id="491bc-135">**資金調達ソース**</span><span class="sxs-lookup"><span data-stu-id="491bc-135">**Funding source**</span></span>
    - <span data-ttu-id="491bc-136">**販売通貨** – 既定では、この通貨はプロジェクト契約に関連付けられている顧客の請求書に使用されます。</span><span class="sxs-lookup"><span data-stu-id="491bc-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="491bc-137">ただし、特定の顧客の請求書の販売通貨を変更することはできます。</span><span class="sxs-lookup"><span data-stu-id="491bc-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="491bc-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-138">Select **OK**.</span></span> <span data-ttu-id="491bc-139">情報は **プロジェクト契約** ページのヘッダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="491bc-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="491bc-140">**プロジェクト契約** ページに、プロジェクトに必要な残りの情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="491bc-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="491bc-141">進捗請求のプロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="491bc-141">Create a project for progress billings</span></span>

<span data-ttu-id="491bc-142">次の手順に従って、プロジェクトと、プロジェクト契約に関連付けられているサブプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="491bc-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="491bc-143">**プロジェクト管理と会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="491bc-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="491bc-144">**すべてのプロジェクト** ページで **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="491bc-145">**新しいプロジェクト** ダイアログ ボックスの **プロジェクト タイプ** フィールドで、 **時間と材料** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="491bc-146">プロジェクト グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-146">Select a project group.</span></span> <span data-ttu-id="491bc-147">プロジェクト グループは、グループに割り当てられているプロジェクトの転記情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="491bc-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="491bc-148">**プロジェクトの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-148">Select **Create project**.</span></span>
6. <span data-ttu-id="491bc-149">プロジェクトが作成されたら、プロジェクト ステージを **処理中** に設定します。</span><span class="sxs-lookup"><span data-stu-id="491bc-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="491bc-150">プロジェクトの予算を作成する</span><span class="sxs-lookup"><span data-stu-id="491bc-150">Create a budget for a project</span></span>

<span data-ttu-id="491bc-151">予算カテゴリは、各カテゴリで完了した作業の割合に対する請求金額を自動的に計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="491bc-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="491bc-152">次の手順に従って、見積もりコストの予算カテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="491bc-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="491bc-153">**プロジェクト管理と会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="491bc-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="491bc-154">**すべてのプロジェクト** ページで、必要なプロジェクトを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="491bc-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="491bc-155">**プロジェクト** ページのアクション ペインにある **計画** タブの **予算** グループで、 **プロジェクト予算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="491bc-156">**プロジェクト予算** ページに、プロジェクトの各カテゴリに対する見積もりコストを入力します。</span><span class="sxs-lookup"><span data-stu-id="491bc-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="491bc-157">進捗請求の請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="491bc-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="491bc-158">**プロジェクト管理および会計** \> **プロジェクト** \> **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="491bc-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="491bc-159">**プロジェクト契約** ページで、プロジェクト契約を選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="491bc-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="491bc-160">プロジェクト契約ページの **請求ルール** クイック タブで、 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="491bc-161">**請求ルール** ページの **行タイプ** フィールドで、 **進捗状況** を選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="491bc-162">**請求ルール行の詳細** クイック タブの **契約価値** フィールドに、契約の総額を入力します。</span><span class="sxs-lookup"><span data-stu-id="491bc-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="491bc-163">**カテゴリ** フィールドで、料金のトランザクションを転記するカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="491bc-164">**プロジェクト** フィールドで、この請求ルールを使用するプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="491bc-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="491bc-165">オプション: 請求ルールを追加プロジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="491bc-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="491bc-166">**プロジェクト** クイック タブの **利用可能なプロジェクト** セクションでプロジェクトを選択し、右矢印ボタンを選択して、 **選択したプロジェクト** セクションにプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="491bc-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="491bc-167">オプション: 顧客が請求書の支払いから差し引く金額の割合を計算します。</span><span class="sxs-lookup"><span data-stu-id="491bc-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="491bc-168">**支払い保持条件** クイック タブで資金調達ソース を選択してから、 **保持率** フィールドに、保持率を入力します。</span><span class="sxs-lookup"><span data-stu-id="491bc-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="491bc-169">これらの手順を繰り返して、プロジェクト契約の追加請求ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="491bc-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
