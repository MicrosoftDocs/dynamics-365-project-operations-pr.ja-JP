---
title: 現金前払い
description: このトピックでは、現金前払いについて説明します。
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079151"
---
# <a name="cash-advance"></a><span data-ttu-id="669c8-103">現金前払い</span><span class="sxs-lookup"><span data-stu-id="669c8-103">Cash advance</span></span>

<span data-ttu-id="669c8-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="669c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="669c8-105">現金前払いにより、従業員は経費が発生する前に会社からお金を借りることができます。</span><span class="sxs-lookup"><span data-stu-id="669c8-105">A cash advance allows employees to borrow money from their company prior to incurring any expenses.</span></span> <span data-ttu-id="669c8-106">要求された現金前払いが承認されて支払われると、従業員はそのお金を、これから発生する可能性のある経費に使用できます。</span><span class="sxs-lookup"><span data-stu-id="669c8-106">When a requested cash advance is approved and paid, the employee can use the money for the business expenses they may be about to incur.</span></span> 

## <a name="create-and-submit-a-cash-advance-request"></a><span data-ttu-id="669c8-107">現金前払い申請を作成して送信する</span><span class="sxs-lookup"><span data-stu-id="669c8-107">Create and submit a cash advance request</span></span>

1. <span data-ttu-id="669c8-108">**自分の経費** の下にある **現金前払い** > **新規** を選択し、新規の現金前払いを作成します。</span><span class="sxs-lookup"><span data-stu-id="669c8-108">Under **My Expenses** , select **Cash advances** > **New** to create a new cash advance.</span></span> 
2. <span data-ttu-id="669c8-109">に **新規現金前払い申請** ページで、経費の目的を入力し、経費が発生する場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-109">On the **New cash advance request** page, enter the expense purpose and select the location where the expense will be incurred.</span></span>
3. <span data-ttu-id="669c8-110">要求された金額と通貨を入力してから、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-110">Enter the requested amount and currency, and then select **Save**.</span></span> 
4. <span data-ttu-id="669c8-111">現金前払い申請を送信する準備ができたら、 **現金前払い申請** ページで、 **ワークフロー** > **送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-111">When you are ready to submit the cash advance request, on the **Cash advance request** page, select **Workflow** > **Submit**.</span></span>

## <a name="modify-a-cash-advance-request"></a><span data-ttu-id="669c8-112">現金前払い申請を修正する</span><span class="sxs-lookup"><span data-stu-id="669c8-112">Modify a cash advance request</span></span>

<span data-ttu-id="669c8-113">承認のために提出されていない場合は、現金前払い申請を修正できます。</span><span class="sxs-lookup"><span data-stu-id="669c8-113">You can modify a cash advance request if it has not been submitted for approval.</span></span>

1. <span data-ttu-id="669c8-114">**自分の経費: 現金前払い** の下で、修正したい現金前払いを検索して修正します。</span><span class="sxs-lookup"><span data-stu-id="669c8-114">Under **My Expenses: Cash Advances** locate and select the cash advance you want to edit.</span></span>
2. <span data-ttu-id="669c8-115">**編集** を選択し、現金前払い申請に必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="669c8-115">Select **Edit** , and make the necessary changes to the cash advance request.</span></span> 
3. <span data-ttu-id="669c8-116">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-116">Select **Save and close**.</span></span>


## <a name="view-cash-advance-requests"></a><span data-ttu-id="669c8-117">現金前払い申請を表示する</span><span class="sxs-lookup"><span data-stu-id="669c8-117">View cash advance requests</span></span>
<span data-ttu-id="669c8-118">**自分の経費: 現金前払い** の下で、下書き、送信済、レビュー済、または支払い済すべての現金前払いリストを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="669c8-118">You can review the list of all the cash advances that are in draft, submitted, in review, or paid under **My Expenses: Cash Advances**.</span></span> 

## <a name="approve-cash-advance-requests"></a><span data-ttu-id="669c8-119">現金前払い申請を承認する</span><span class="sxs-lookup"><span data-stu-id="669c8-119">Approve cash advance requests</span></span>

<span data-ttu-id="669c8-120">ワークフローで承認者として構成されたマネージャーまたはユーザーは、レビューのために送信された現金支払いを承認できます。</span><span class="sxs-lookup"><span data-stu-id="669c8-120">Managers or users configured as approvers in the workflow will be able to approve the cash advances submitted to them for review.</span></span> 

1. <span data-ttu-id="669c8-121">現金前払いを承認するには、 **現金前払いのプロセス** の下の、 **レビュー用現金前払い** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-121">To approve a cash advance, under **Process cash advances** , select **Cash advances for my review**.</span></span>
2. <span data-ttu-id="669c8-122">レビューの必要がある現金前払いを選択し、 **承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-122">Select the cash advance you need to review and select **Approve**.</span></span>  

## <a name="pay-cash-advances"></a><span data-ttu-id="669c8-123">現金前払いの支払い</span><span class="sxs-lookup"><span data-stu-id="669c8-123">Pay cash advances</span></span> 
<span data-ttu-id="669c8-124">次の手順は、通常、会計士または会計権限を持つユーザーが実行します。</span><span class="sxs-lookup"><span data-stu-id="669c8-124">The following procedure is typically completed by an accountant or a user with accounting permissions.</span></span>

1. <span data-ttu-id="669c8-125">承認された現金前払いを投稿するには、 **承認された現金前払い** を選択してから、 **支払いと送金** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-125">To post approved cash advances, select **Approved cash advances** , and then select **Pay and transfer**.</span></span>  
2. <span data-ttu-id="669c8-126">現金前払いのために仕訳帳詳細に入力し、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="669c8-126">Provide the journal details for the cash advances, and then select **OK**.</span></span> 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a><span data-ttu-id="669c8-127">支払われた現金前払いに対して経費清算書を送信する</span><span class="sxs-lookup"><span data-stu-id="669c8-127">Submit an expense report against a paid cash advance</span></span> 

<span data-ttu-id="669c8-128">すでに受け取った現金前払いの経費清算書を作成して送信すると、経費はその現金前払いに対して自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="669c8-128">When you create and submit an expense report for the cash advance you already received, the expenses will be automatically adjusted against that advance.</span></span> <span data-ttu-id="669c8-129">現金前払いが経費額よりも大きい場合は、 **現金償還** 経費カテゴリを使用して、残高を会社に返還する必要があります。</span><span class="sxs-lookup"><span data-stu-id="669c8-129">If your cash advance is greater than the expensed amount, you must return the balance to the company using the **Return cash** expense category.</span></span> <span data-ttu-id="669c8-130">会社が支払った現金前払いが経費より少ない場合、会社はあなたに残高を払い戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="669c8-130">If the company-paid cash advance is less than the amount you expensed, the company must reimburse you the balance.</span></span> 

### <a name="example"></a><span data-ttu-id="669c8-131">例</span><span class="sxs-lookup"><span data-stu-id="669c8-131">Example</span></span>
<span data-ttu-id="669c8-132">あなたはシアトルからニューヨーク市へ会議のために旅行することを計画しています。</span><span class="sxs-lookup"><span data-stu-id="669c8-132">You plan to travel for a conference from Seattle to New York City.</span></span> <span data-ttu-id="669c8-133">会議のチケット、フライト、ホテル、食事、タクシーの費用を見積もって、$3000 USD の現金前払い申請を作成します。</span><span class="sxs-lookup"><span data-stu-id="669c8-133">You create a cash advance request for 3000.00 USD as you have estimated the cost of the conference ticket, flights, hotel, meals, and taxi to be apporximately this amount.</span></span> <span data-ttu-id="669c8-134">上司がこの申請を承認しない限り、支払いは行われません。</span><span class="sxs-lookup"><span data-stu-id="669c8-134">You will not be paid unless your manager approved this request.</span></span> <span data-ttu-id="669c8-135">上司が承認した後、要求された現金前払い $3000 USDは銀行口座に支払われます。</span><span class="sxs-lookup"><span data-stu-id="669c8-135">After your manager approves, the requested cash advance is paid as 3000.00 USD into your bank account.</span></span> <span data-ttu-id="669c8-136">それから会議に参加します。</span><span class="sxs-lookup"><span data-stu-id="669c8-136">You then attend the conference.</span></span> <span data-ttu-id="669c8-137">旅行を終えた後、合計支出は$2790 USDだけだったことがわかります。</span><span class="sxs-lookup"><span data-stu-id="669c8-137">After completing your trip, you find that the total expenditure was only 2790.00 USD.</span></span> <span data-ttu-id="669c8-138">**支払方法** フィールドの **現金** を選択し、$2790 USDの経費を送信します。</span><span class="sxs-lookup"><span data-stu-id="669c8-138">Select **Cash** in the **Payment method** field, and submits your expense for 2790.00 USD.</span></span> <span data-ttu-id="669c8-139">送信された経費額は、貸与された $3000 USD の現金前払いに対して自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="669c8-139">Your submitted expense amount is automatically adjusted against the cash advance of 3000.00 USD that was loaned to you.</span></span> <span data-ttu-id="669c8-140">これで、会社に $210 USD (3000.00-2790.00) の借りがあり、 **現金償還** 経費カテゴリを使用して会社に返金することができます。</span><span class="sxs-lookup"><span data-stu-id="669c8-140">You now owe a balance of 210.00 USD (3000.00-2790.00) to the company, which you can return to company using the **Return cash** expense category.</span></span> 
