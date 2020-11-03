---
title: 出張申請書
description: このトピックでは、出張申請書について説明します。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079137"
---
# <a name="travel-requisitions"></a><span data-ttu-id="d1167-103">出張申請書</span><span class="sxs-lookup"><span data-stu-id="d1167-103">Travel requisitions</span></span>

<span data-ttu-id="d1167-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d1167-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d1167-105">出張申請書には、出張目的のために発生する費用が一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="d1167-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="d1167-106">出張申請書はレビューのために送信され、経費の承認に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d1167-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="d1167-107">組織に請求される経費が発生する前に、出張申請書を提出する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d1167-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="d1167-108">この要件は、会社のクレジット カードに経費が請求されるか、現金前払いから受け取った現金を使うか、または組織によって払い戻される自己負担の経費が発生するかに関係なく適用されます。</span><span class="sxs-lookup"><span data-stu-id="d1167-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="d1167-109">出張申請書とポリシーは、組織の経費管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d1167-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="d1167-110">たとえば、組織が出張を必要とする固定価格プロジェクトの作業を行っている場合、プロジェクト チーム メンバーの出張費はプロジェクトの予算内に収まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1167-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="d1167-111">出張費が発生する前に承認を要求することにより、組織はプロジェクトが予算内に収まるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1167-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="d1167-112">構成</span><span class="sxs-lookup"><span data-stu-id="d1167-112">Configuration</span></span> 

<span data-ttu-id="d1167-113">経費管理パラメーターで「出張の事前承認が必須である」パラメーターを有効にすることにより、出張申請書を「必須」として設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d1167-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="d1167-114">出張申請書の作成および送信</span><span class="sxs-lookup"><span data-stu-id="d1167-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="d1167-115">**自分の経費: 出張申請書** に移動し、 **新しい出張申請書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1167-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="d1167-116">申請書に目的と出張先を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1167-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="d1167-117">**出張の説明** フィールドに、追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1167-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="d1167-118">フライト、食事、レンタカーなどの各予定経費について、経費明細行品目を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1167-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="d1167-119">各経費について、予定日、見積もり金額、および通貨を含めます。</span><span class="sxs-lookup"><span data-stu-id="d1167-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="d1167-120">予想される経費の追加が完了したら、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1167-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="d1167-121">出張申請書を送信する準備ができたら、 **ワークフロー** > **送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1167-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="d1167-122">**自分の経費: 出張申請書** の下で承認された出張申請書を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d1167-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="d1167-123">利用可能な出張申請書の表示</span><span class="sxs-lookup"><span data-stu-id="d1167-123">View available travel requisitions</span></span>

<span data-ttu-id="d1167-124">**自分の経費: 出張申請書** の下ですべての出張申請書を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d1167-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="d1167-125">承認された出張申請書</span><span class="sxs-lookup"><span data-stu-id="d1167-125">Approve travel requisitions</span></span>

<span data-ttu-id="d1167-126">承認する出張申請書を選択し、 **ワークフロー** > **承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1167-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="d1167-127">承認された出張申請書を使用して経費報告書を送信する</span><span class="sxs-lookup"><span data-stu-id="d1167-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="d1167-128">新しい経費報告書を作成し、経費報告書ヘッダーで、承認された出張申請書の一覧から **出張申請書へのマップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1167-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="d1167-129">経費報告書ヘッダーの **出張申請書金額** フィールドは自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="d1167-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="d1167-130">出張で発生した各経費を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1167-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="d1167-131">**事前承認済み** フィールドが有効になっていると、特定の経費カテゴリの調整された金額と承認された金額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="d1167-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="d1167-132">経費報告書を承認された出張申請書にマップする場合、取引金額は承認された金額を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="d1167-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
