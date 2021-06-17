---
title: プロジェクトベースの営業案件の管理
description: このトピックでは、プロジェクトに関連する営業案件を処理する方法について説明します。
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aebff4d3a94735e76bcb9cafd25a058207dae846
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996347"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="b472f-103">プロジェクトベースの営業案件の管理</span><span class="sxs-lookup"><span data-stu-id="b472f-103">Manage project-based opportunities</span></span>

<span data-ttu-id="b472f-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="b472f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b472f-105">プロジェクトベースの企業は通常、複数の国や地域にまたがったサービスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="b472f-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="b472f-106">プロジェクトの実行とサービス提供のコストは、サービス提供を管理する地域または部門によって異なります。</span><span class="sxs-lookup"><span data-stu-id="b472f-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="b472f-107">一方、これは、取引の利益に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b472f-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="b472f-108">プロジェクトベースのサービスの提供には、通常、大量の人的資源の時間、相当な旅費、材料費、その他の費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b472f-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="b472f-109">Dynamics 365 Project Operations のプロジェクト ベースの機会は、Dynamics 365 Sales への拡張を念頭に置いて設計されています。</span><span class="sxs-lookup"><span data-stu-id="b472f-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="b472f-110">このトピックでは、プロジェクトベースの営業案件を管理するために、プロジェクトベースの企業が必要とする追加機能に含まれる、さまざまなフィールドとビジネス ロジックについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="b472f-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="b472f-111">プロジェクトベースの営業案件をすべて表示する</span><span class="sxs-lookup"><span data-stu-id="b472f-111">View all project-based opportunities</span></span>

<span data-ttu-id="b472f-112">すべてのプロジェクトベースの営業案件の一覧は、**営業案件** の一覧ページから確認できます。</span><span class="sxs-lookup"><span data-stu-id="b472f-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="b472f-113">**営業** > **営業案件** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b472f-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="b472f-114">**ビュー スイッチャー** を使用して、営業案件の他のフィルター ビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="b472f-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="b472f-115">カスタム フィルター条件を使用して独自のビューを作成し、これらのビューとナビゲーション オプションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="b472f-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="b472f-116">プロジェクトの営業案件は、この一覧ページまたは詳細ページから作成または削除できます。</span><span class="sxs-lookup"><span data-stu-id="b472f-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="b472f-117">プロジェクト ベース取引のビジネス プロセス フロー</span><span class="sxs-lookup"><span data-stu-id="b472f-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="b472f-118">次のビジネス プロセス フローは、プロジェクト オペレーションのプロジェクト ベース取引に対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b472f-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="b472f-119">リードから営業案件へのビジネス プロセス</span><span class="sxs-lookup"><span data-stu-id="b472f-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="b472f-120">営業案件の営業プロセス</span><span class="sxs-lookup"><span data-stu-id="b472f-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="b472f-121">リードから営業案件へのビジネス プロセス</span><span class="sxs-lookup"><span data-stu-id="b472f-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="b472f-122">リードから営業案件へのビジネス プロセスは、次のステージをサポートしています:</span><span class="sxs-lookup"><span data-stu-id="b472f-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="b472f-123">段階</span><span class="sxs-lookup"><span data-stu-id="b472f-123">Stage</span></span> | <span data-ttu-id="b472f-124">マップされているエンティティ</span><span class="sxs-lookup"><span data-stu-id="b472f-124">Mapped entity</span></span> | <span data-ttu-id="b472f-125">機能</span><span class="sxs-lookup"><span data-stu-id="b472f-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b472f-126">見込みありと評価</span><span class="sxs-lookup"><span data-stu-id="b472f-126">Qualify</span></span> | <span data-ttu-id="b472f-127">​​リード</span><span class="sxs-lookup"><span data-stu-id="b472f-127">Lead</span></span> | <span data-ttu-id="b472f-128">リードを見込みありと評価して、取引先企業、取引先担当者、および営業案件を作成します。</span><span class="sxs-lookup"><span data-stu-id="b472f-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="b472f-129">提案作成</span><span class="sxs-lookup"><span data-stu-id="b472f-129">Develop</span></span> | <span data-ttu-id="b472f-130">営業案件</span><span class="sxs-lookup"><span data-stu-id="b472f-130">Opportunity</span></span> | <span data-ttu-id="b472f-131">営業案件を開発して、含まれる作業、主要な利害関係者、および競合に関する情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="b472f-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="b472f-132">提案</span><span class="sxs-lookup"><span data-stu-id="b472f-132">Propose</span></span> | <span data-ttu-id="b472f-133">営業案件</span><span class="sxs-lookup"><span data-stu-id="b472f-133">Opportunity</span></span> | <span data-ttu-id="b472f-134">提案を作成し、内部のレビュー チームの承認を得ます。</span><span class="sxs-lookup"><span data-stu-id="b472f-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="b472f-135">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="b472f-135">Close</span></span> | <span data-ttu-id="b472f-136">営業案件</span><span class="sxs-lookup"><span data-stu-id="b472f-136">Opportunity</span></span> | <span data-ttu-id="b472f-137">営業案件を成功させ、商談を成立させます。</span><span class="sxs-lookup"><span data-stu-id="b472f-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="b472f-138">営業案件の営業プロセス</span><span class="sxs-lookup"><span data-stu-id="b472f-138">Opportunity sales process</span></span>
<span data-ttu-id="b472f-139">Project Operations のリードから営業案件の販売プロセスは、Sales アプリケーションの営業案件の販売プロセス ビジネス フローの拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="b472f-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="b472f-140">このビジネス プロセスは、プロジェクト ベースの営業案件で次のステージをサポートするためにすぐに使用できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="b472f-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="b472f-141">段階</span><span class="sxs-lookup"><span data-stu-id="b472f-141">Stage</span></span> | <span data-ttu-id="b472f-142">マップされているエンティティ</span><span class="sxs-lookup"><span data-stu-id="b472f-142">Mapped entity</span></span> | <span data-ttu-id="b472f-143">機能</span><span class="sxs-lookup"><span data-stu-id="b472f-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b472f-144">見込みありと評価</span><span class="sxs-lookup"><span data-stu-id="b472f-144">Qualify</span></span> | <span data-ttu-id="b472f-145">営業案件</span><span class="sxs-lookup"><span data-stu-id="b472f-145">Opportunity</span></span> | <span data-ttu-id="b472f-146">リードを見込みありと評価して、取引先企業、取引先担当者、および営業案件を作成します。</span><span class="sxs-lookup"><span data-stu-id="b472f-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="b472f-147">提案</span><span class="sxs-lookup"><span data-stu-id="b472f-147">Propose</span></span> | <span data-ttu-id="b472f-148">見積もり </span><span class="sxs-lookup"><span data-stu-id="b472f-148">Quote</span></span> | <span data-ttu-id="b472f-149">プロジェクトの見積もりを使用して提案を作成し、内部レビュー チームから承認を得ます。</span><span class="sxs-lookup"><span data-stu-id="b472f-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="b472f-150">契約 </span><span class="sxs-lookup"><span data-stu-id="b472f-150">Contract</span></span> | <span data-ttu-id="b472f-151">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="b472f-151">Project Contract</span></span> | <span data-ttu-id="b472f-152">見積もりを獲得して契約を作成し、プロジェクトの実行とサービス提供を開始します。</span><span class="sxs-lookup"><span data-stu-id="b472f-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="b472f-153">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="b472f-153">Close</span></span> | <span data-ttu-id="b472f-154">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="b472f-154">Project Contract</span></span> | <span data-ttu-id="b472f-155">作業を正常に終了し、プロジェクト契約を閉じます。</span><span class="sxs-lookup"><span data-stu-id="b472f-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="b472f-156">プロジェクトベースの取引がリードから始まった場合は、リードから営業案件へのビジネス プロセスが優先されます。</span><span class="sxs-lookup"><span data-stu-id="b472f-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="b472f-157">プロジェクトベースの取引が営業案件から始まった場合は、営業案件の営業プロセスが優先されます。</span><span class="sxs-lookup"><span data-stu-id="b472f-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="b472f-158">製品のビジネス プロセス フローを編集するか、独自のビジネス プロセス フローを作成して、必要に応じて営業プロセスを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="b472f-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="b472f-159">ビジネス プロセス フローの詳細については、[ビジネス プロセス フローの概要](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b472f-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]