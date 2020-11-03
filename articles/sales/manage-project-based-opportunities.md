---
title: プロジェクトベースの営業案件の管理
description: このトピックでは、プロジェクトに関連する営業案件を処理する方法について説明します。
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087983"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="ce800-103">プロジェクトベースの営業案件の管理</span><span class="sxs-lookup"><span data-stu-id="ce800-103">Manage project-based opportunities</span></span>

<span data-ttu-id="ce800-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ce800-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ce800-105">プロジェクトベースの企業は通常、複数の国や地域にまたがったサービスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="ce800-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="ce800-106">プロジェクトの実行とサービス提供のコストは、サービス提供を管理する地域または部門によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ce800-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="ce800-107">一方、これは、取引の利益に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ce800-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="ce800-108">プロジェクトベースのサービスの提供には、通常、大量の人的資源の時間、相当な旅費、材料費、その他の費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ce800-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="ce800-109">Dynamics 365 Project Operations のプロジェクトベースの営業案件は、Dynamics 365 Sales の拡張機能を使用して設計されています。</span><span class="sxs-lookup"><span data-stu-id="ce800-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="ce800-110">このトピックでは、プロジェクトベースの営業案件を管理するために、プロジェクトベースの企業が必要とする追加機能に含まれる、さまざまなフィールドとビジネス ロジックについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="ce800-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="ce800-111">プロジェクトベースの営業案件をすべて表示する</span><span class="sxs-lookup"><span data-stu-id="ce800-111">View all project-based opportunities</span></span>

<span data-ttu-id="ce800-112">すべてのプロジェクトベースの営業案件の一覧は、 **営業案件** の一覧ページから確認できます。</span><span class="sxs-lookup"><span data-stu-id="ce800-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="ce800-113">**営業** > **営業案件** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce800-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="ce800-114">**ビュー スイッチャー** を使用して、営業案件の他のフィルター ビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce800-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="ce800-115">カスタム フィルター条件を使用して独自のビューを作成し、これらのビューとナビゲーション オプションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="ce800-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="ce800-116">プロジェクトの営業案件は、この一覧ページまたは詳細ページから作成または削除できます。</span><span class="sxs-lookup"><span data-stu-id="ce800-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="ce800-117">プロジェクト ベース取引のビジネス プロセス フロー</span><span class="sxs-lookup"><span data-stu-id="ce800-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="ce800-118">次のビジネス プロセス フローは、プロジェクト オペレーションのプロジェクト ベース取引に対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ce800-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="ce800-119">リードから営業案件へのビジネス プロセス</span><span class="sxs-lookup"><span data-stu-id="ce800-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="ce800-120">営業案件の営業プロセス</span><span class="sxs-lookup"><span data-stu-id="ce800-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="ce800-121">リードから営業案件へのビジネス プロセス</span><span class="sxs-lookup"><span data-stu-id="ce800-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="ce800-122">リードから営業案件へのビジネス プロセスは、次のステージをサポートしています:</span><span class="sxs-lookup"><span data-stu-id="ce800-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="ce800-123">段階</span><span class="sxs-lookup"><span data-stu-id="ce800-123">Stage</span></span> | <span data-ttu-id="ce800-124">マップされているエンティティ</span><span class="sxs-lookup"><span data-stu-id="ce800-124">Mapped entity</span></span> | <span data-ttu-id="ce800-125">機能</span><span class="sxs-lookup"><span data-stu-id="ce800-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ce800-126">見込みありと評価</span><span class="sxs-lookup"><span data-stu-id="ce800-126">Qualify</span></span> | <span data-ttu-id="ce800-127">​​リード</span><span class="sxs-lookup"><span data-stu-id="ce800-127">Lead</span></span> | <span data-ttu-id="ce800-128">リードを見込みありと評価して、取引先企業、取引先担当者、および営業案件を作成します。</span><span class="sxs-lookup"><span data-stu-id="ce800-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="ce800-129">提案作成</span><span class="sxs-lookup"><span data-stu-id="ce800-129">Develop</span></span> | <span data-ttu-id="ce800-130">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="ce800-130">Opportunity</span></span> | <span data-ttu-id="ce800-131">関係する作業、主要な関係者、および競争に情報を追加するために営業案件を提案作成します。</span><span class="sxs-lookup"><span data-stu-id="ce800-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="ce800-132">提案</span><span class="sxs-lookup"><span data-stu-id="ce800-132">Propose</span></span> | <span data-ttu-id="ce800-133">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="ce800-133">Opportunity</span></span> | <span data-ttu-id="ce800-134">提案を提案作成し、内部レビュー チームから承認を得ます。</span><span class="sxs-lookup"><span data-stu-id="ce800-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="ce800-135">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="ce800-135">Close</span></span> | <span data-ttu-id="ce800-136">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="ce800-136">Opportunity</span></span> | <span data-ttu-id="ce800-137">取引を成立させるために営業案件を獲得します。</span><span class="sxs-lookup"><span data-stu-id="ce800-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="ce800-138">営業案件の営業プロセス</span><span class="sxs-lookup"><span data-stu-id="ce800-138">Opportunity sales process</span></span>
<span data-ttu-id="ce800-139">Project Operations の営業案件の営業プロセスは、Sales アプリケーションの営業案件の営業プロセス業務フローの拡張です。</span><span class="sxs-lookup"><span data-stu-id="ce800-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="ce800-140">このビジネス プロセスは、プロジェクトベースの営業案件で次の段階をサポートするために、すぐに使用できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ce800-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="ce800-141">段階</span><span class="sxs-lookup"><span data-stu-id="ce800-141">Stage</span></span> | <span data-ttu-id="ce800-142">マップされているエンティティ</span><span class="sxs-lookup"><span data-stu-id="ce800-142">Mapped entity</span></span> | <span data-ttu-id="ce800-143">機能</span><span class="sxs-lookup"><span data-stu-id="ce800-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ce800-144">見込みありと評価</span><span class="sxs-lookup"><span data-stu-id="ce800-144">Qualify</span></span> | <span data-ttu-id="ce800-145">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="ce800-145">Opportunity</span></span> | <span data-ttu-id="ce800-146">リードを見込みありと評価して、取引先企業、取引先担当者、および営業案件を作成します。</span><span class="sxs-lookup"><span data-stu-id="ce800-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="ce800-147">提案</span><span class="sxs-lookup"><span data-stu-id="ce800-147">Propose</span></span> | <span data-ttu-id="ce800-148">見積もり </span><span class="sxs-lookup"><span data-stu-id="ce800-148">Quote</span></span> | <span data-ttu-id="ce800-149">プロジェクトの見積もりを使用して提案を作成し、内部レビュー チームから承認を得ます。</span><span class="sxs-lookup"><span data-stu-id="ce800-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="ce800-150">契約 </span><span class="sxs-lookup"><span data-stu-id="ce800-150">Contract</span></span> | <span data-ttu-id="ce800-151">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="ce800-151">Project Contract</span></span> | <span data-ttu-id="ce800-152">見積もりを獲得して契約を作成し、プロジェクトの実行とサービス提供を開始します。</span><span class="sxs-lookup"><span data-stu-id="ce800-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="ce800-153">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="ce800-153">Close</span></span> | <span data-ttu-id="ce800-154">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="ce800-154">Project Contract</span></span> | <span data-ttu-id="ce800-155">作業を正常に終了し、プロジェクト契約を閉じます。</span><span class="sxs-lookup"><span data-stu-id="ce800-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="ce800-156">プロジェクトベースの取引がリードから始まった場合は、リードから営業案件へのビジネス プロセスが優先されます。</span><span class="sxs-lookup"><span data-stu-id="ce800-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="ce800-157">プロジェクトベースの取引が営業案件から始まった場合は、営業案件の営業プロセスが優先されます。</span><span class="sxs-lookup"><span data-stu-id="ce800-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="ce800-158">製品のビジネス プロセス フローを編集するか、独自のビジネス プロセス フローを作成して、必要に応じて営業プロセスを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="ce800-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="ce800-159">ビジネス プロセス フローの詳細については、[ビジネス プロセス フローの概要](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce800-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>
