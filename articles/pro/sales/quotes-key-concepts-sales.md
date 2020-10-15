---
title: プロジェクト見積もりの重要な概念
description: このトピックは、Project Operations でプロジェクト見積もりの使用に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896287"
---
# <a name="project-quote-key-concepts"></a><span data-ttu-id="7a695-103">プロジェクト見積もりの重要な概念</span><span class="sxs-lookup"><span data-stu-id="7a695-103">Project quote key concepts</span></span>

<span data-ttu-id="7a695-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="7a695-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7a695-105">以下は、Dynamics 365 Project Operations でプロジェクト見積もりを使用する前に知っておくべき重要な概念です。</span><span class="sxs-lookup"><span data-stu-id="7a695-105">The following are key concepts to be aware of before you begin using project quotes in Dynamics 365 Project Operations:</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="7a695-106">契約単位</span><span class="sxs-lookup"><span data-stu-id="7a695-106">Contracting unit</span></span>

<span data-ttu-id="7a695-107">契約単位は、プロジェクトの実施を所有する部門または業務を表します。</span><span class="sxs-lookup"><span data-stu-id="7a695-107">The contracting unit represents the division or practice that owns the project delivery.</span></span> <span data-ttu-id="7a695-108">各契約単位ごとにリソース コストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-108">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="7a695-109">契約ユニット内のリソースのリソース コストを指定すると、この契約ユニットが借りるリソース、または企業内の他の部門や慣行に対して異なる原価率を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="7a695-109">When you specify resource cost for a resource in the contracting unit, you will also be able to set up different cost rates for resources that this contracting unit borrows from, or other division or practices within the enterprise.</span></span> <span data-ttu-id="7a695-110">これらは、移転価格、リソース借入、または為替価格と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7a695-110">These are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="7a695-111">他の部門からリソースを借りるコストを設定する場合、それらの原価率を貸し出し部門の通貨で設定することも選択できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-111">When you set up the cost of borrowing resources from other divisions, you can also choose to set up those cost rates in the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="7a695-112">原価通貨</span><span class="sxs-lookup"><span data-stu-id="7a695-112">Cost currency</span></span>

<span data-ttu-id="7a695-113">Project Operations の原価通貨は、コストが報告される通貨です。</span><span class="sxs-lookup"><span data-stu-id="7a695-113">Cost currency in Project Operations is the currency in which costs are reported.</span></span> <span data-ttu-id="7a695-114">この通貨は、見積もり、契約、およびプロジェクトの**契約単位**フィールドに添付されている通貨から派生しています。</span><span class="sxs-lookup"><span data-stu-id="7a695-114">This currency is derived from the currency attached to the **Contracting unit** field on the quote, contract, and project.</span></span> <span data-ttu-id="7a695-115">コストは、プロジェクトに対して任意の通貨で記録できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-115">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="7a695-116">ただし、記録された通貨コストからプロジェクトの原価通貨への通貨換算があります。</span><span class="sxs-lookup"><span data-stu-id="7a695-116">However, there is currency conversion from the currency costs were recorded in, to the cost currency of the project.</span></span>

<span data-ttu-id="7a695-117">CDS プラットフォームの為替レートは日付を有効にできないため、通貨為替レートを更新すると、画面に表示されるコストの合計が時間の経過とともに変化する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a695-117">Because of the exchange rates in the CDS platform can't be date-effective, the on-screen totals for cost may change over time if you update currency exchange rates.</span></span> <span data-ttu-id="7a695-118">ただし、コストは発生した通貨で保存されるため、データベースに記録されるコストは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7a695-118">However, costs recorded in the database remain unchanged because the amounts are stored in the currency that they were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="7a695-119">販売通貨</span><span class="sxs-lookup"><span data-stu-id="7a695-119">Sales currency</span></span>

<span data-ttu-id="7a695-120">Project Operations の販売通貨は、推定および販売実績額が記録および表示される通貨です。</span><span class="sxs-lookup"><span data-stu-id="7a695-120">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="7a695-121">これは、顧客が取引に対して請求される通貨でもあります。</span><span class="sxs-lookup"><span data-stu-id="7a695-121">It is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="7a695-122">プロジェクト見積もりでは、販売通貨は既定で顧客または取引先企業レコードから設定され、見積もりの作成時に変更できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-122">On a project quote, the sales currency defaults from the customer or account record and can be changed when the quote is created.</span></span> <span data-ttu-id="7a695-123">見積もりが保存された後は、販売通貨を変更できません。</span><span class="sxs-lookup"><span data-stu-id="7a695-123">After the quote is saved, the sales currency can't be changed.</span></span> <span data-ttu-id="7a695-124">製品およびプロジェクトの価格リストは、見積もりの販売通貨に基づいて既定となります。</span><span class="sxs-lookup"><span data-stu-id="7a695-124">Product and project price lists default based on the sales currency of the quote.</span></span>

<span data-ttu-id="7a695-125">原価とは異なり、販売額は販売通貨でのみ記録できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-125">Unlike costs, sales values can only be recorded in the Sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="7a695-126">請求方法</span><span class="sxs-lookup"><span data-stu-id="7a695-126">Billing method</span></span>

<span data-ttu-id="7a695-127">プロジェクトには通常、固定料金と消費ベースの契約モデルがあります。</span><span class="sxs-lookup"><span data-stu-id="7a695-127">Projects typically have fixed fee and consumption-based contracting models.</span></span> <span data-ttu-id="7a695-128">これは、プロジェクト運用では**請求方法**として表され、時間、材料および固定価格の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="7a695-128">This is represented in Project Operations as **Billing Method** and has two values, time and material and fixed price.</span></span>

- <span data-ttu-id="7a695-129">**時間と材料:** これは消費ベースの契約モデルであり、発生した各コストは対応する売上によって裏付けられます。</span><span class="sxs-lookup"><span data-stu-id="7a695-129">**Time and material:** This is a consumption-based contract model where each cost incurred is backed by corresponding revenue.</span></span> <span data-ttu-id="7a695-130">見積もりまたはより多くのコストが発生すると、対応する見積もりおよび販売実績も増加します。</span><span class="sxs-lookup"><span data-stu-id="7a695-130">As you estimate or incur more costs, the corresponding estimated and actual sales will also increase.</span></span> <span data-ttu-id="7a695-131">この請求方法を持つ見積依頼明細行には、上限を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-131">You can specify not-to-exceed limits on quote lines that have this billing method.</span></span> <span data-ttu-id="7a695-132">これにより、実際の売上が制限されます。</span><span class="sxs-lookup"><span data-stu-id="7a695-132">This will cap off the actual revenue.</span></span> <span data-ttu-id="7a695-133">売上見込みは、上限を超えないことによる影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="7a695-133">Estimated revenue is not impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="7a695-134">**固定価格:** これは、販売額が発生したコストとは無関係であることを示す固定料金契約モデルです。</span><span class="sxs-lookup"><span data-stu-id="7a695-134">**Fixed price:** This is a fixed fee contract model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="7a695-135">販売額は固定されており、見積もりや追加のコストが発生しても変化しません。</span><span class="sxs-lookup"><span data-stu-id="7a695-135">The sales value is fixed and does not change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="7a695-136">プロジェクト価格表</span><span class="sxs-lookup"><span data-stu-id="7a695-136">Project price lists</span></span>

<span data-ttu-id="7a695-137">プロジェクト価格表は、時間、経費、およびその他のプロジェクト関連コンポーネントについて、コスト率ではなく既定の価格に使用される価格表です。</span><span class="sxs-lookup"><span data-stu-id="7a695-137">Project price lists are price lists that are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="7a695-138">複数の価格表が存在する可能性があり、各リストには、プロジェクトの見積もりごとに独自の日付有効性を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7a695-138">There can be multiple prices lists, and each list can have its own date effectivity for each project quote.</span></span> <span data-ttu-id="7a695-139">プロジェクト価格表での重複する日付の有効性は、Project Operations ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7a695-139">Overlapping date effectivity on project price lists is not supported in Project Operations.</span></span>

## <a name="product-price-lists"></a><span data-ttu-id="7a695-140">製品価格表</span><span class="sxs-lookup"><span data-stu-id="7a695-140">Product price lists</span></span>

<span data-ttu-id="7a695-141">製品価格表は、見積もりの製品ベース品目の原価率ではなく、既定の価格に使用される価格表です。</span><span class="sxs-lookup"><span data-stu-id="7a695-141">Product price lists are price lists that are used to default prices, not cost rates, for product-based lines on a quote.</span></span> <span data-ttu-id="7a695-142">見積もりごとに 1 つの製品価格表のみがあります。</span><span class="sxs-lookup"><span data-stu-id="7a695-142">There is only one product price list per quote.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="7a695-143">トランザクション クラス</span><span class="sxs-lookup"><span data-stu-id="7a695-143">Transaction classes</span></span>

<span data-ttu-id="7a695-144">Project Operations は、次の 4 種類のトランザクション クラスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7a695-144">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="7a695-145">時間</span><span class="sxs-lookup"><span data-stu-id="7a695-145">Time</span></span>
- <span data-ttu-id="7a695-146">経費</span><span class="sxs-lookup"><span data-stu-id="7a695-146">Expense</span></span>
- <span data-ttu-id="7a695-147">材料</span><span class="sxs-lookup"><span data-stu-id="7a695-147">Material</span></span>
- <span data-ttu-id="7a695-148">料金</span><span class="sxs-lookup"><span data-stu-id="7a695-148">Fee</span></span>

<span data-ttu-id="7a695-149">コストと販売額は、時間、経費、および材料のトランザクション クラスで見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="7a695-149">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="7a695-150">手数料は、売上のみのトランザクションのクラスです。</span><span class="sxs-lookup"><span data-stu-id="7a695-150">Fee is a revenue only class of transactions.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="7a695-151">作業エンティティと請求エンティティ</span><span class="sxs-lookup"><span data-stu-id="7a695-151">Work entities and billing entities</span></span>

<span data-ttu-id="7a695-152">作業を表すエンティティは、プロジェクトとタスクです。</span><span class="sxs-lookup"><span data-stu-id="7a695-152">Entities that represent work are Projects and Tasks.</span></span> <span data-ttu-id="7a695-153">請求を表すエンティティは、見積依頼明細行と契約品目です。</span><span class="sxs-lookup"><span data-stu-id="7a695-153">Entities that represent billing are Quote lines and Contract lines.</span></span> <span data-ttu-id="7a695-154">見積もりまたは契約品目に関連付けることにより、さまざまな作業エンティティを請求オプションにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="7a695-154">You can link different work entities to billing options by associating them with Quote or Contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="7a695-155">複数の顧客との取引</span><span class="sxs-lookup"><span data-stu-id="7a695-155">Multi-customer deals</span></span>

<span data-ttu-id="7a695-156">複数の顧客との取引は、請求する顧客が複数いる場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="7a695-156">Multi-customer deals occur are when there is more than one customer to invoice.</span></span> <span data-ttu-id="7a695-157">一般的な例は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="7a695-157">Common examples of this include:</span></span>

- <span data-ttu-id="7a695-158">**OEM 企業とそのパートナー:** パートナーや再販業者は、付加価値サービスを備えた製品を販売しています。</span><span class="sxs-lookup"><span data-stu-id="7a695-158">**OEM Enterprises and their partners:** Partners and resellers sell a product with value-added services.</span></span> <span data-ttu-id="7a695-159">これは通常、顧客との特定の取引中に、OEM がプロジェクトの一部の資金調達を申し出るシナリオです。</span><span class="sxs-lookup"><span data-stu-id="7a695-159">This is usually a scenario where during a particular deal with a customer, the OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="7a695-160">**公的機関のプロジェクト:** 地方自治体の複数の部署がプロジェクトに資金を提供することに同意し、以前に合意された分割に従って請求されます。</span><span class="sxs-lookup"><span data-stu-id="7a695-160">**Public sector projects:** Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="7a695-161">たとえば、学区と市または地方自治体の部署は、スイミング プールの建設に資金を提供することに同意しています。</span><span class="sxs-lookup"><span data-stu-id="7a695-161">For example, a school district and the city or local government department agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="7a695-162">請求スケジュール</span><span class="sxs-lookup"><span data-stu-id="7a695-162">Invoice schedules</span></span>

<span data-ttu-id="7a695-163">請求書のスケジュールは各見積依頼明細行に固有であり、オプションでもあります。</span><span class="sxs-lookup"><span data-stu-id="7a695-163">Invoice schedules are specific to each quote line and are also optional.</span></span> <span data-ttu-id="7a695-164">請求書のスケジュールは、特定の開始日と終了日、および請求頻度に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="7a695-164">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="7a695-165">請求書スケジュールは、自動請求書作成プロセスが構成されている契約ステージで使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a695-165">Invoice schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="7a695-166">見積もりステージでは、スケジュールはオプションです。</span><span class="sxs-lookup"><span data-stu-id="7a695-166">In the quote stage, the schedules are optional.</span></span> <span data-ttu-id="7a695-167">請求書のスケジュールが**見積もり**ステージで作成された場合、プロジェクト見積もりの成約時に作成されるプロジェクト契約にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="7a695-167">When invoice schedules are created in the **Quote** stage, they are copied to the project contract that is created when a project quote is won.</span></span>

## <a name="changes-from-dynamics-365-sales-quote"></a><span data-ttu-id="7a695-168">Dynamics 365 Sales 見積もりからの変更点:</span><span class="sxs-lookup"><span data-stu-id="7a695-168">Changes from Dynamics 365 Sales quote:</span></span>

<span data-ttu-id="7a695-169">Project Operations の見積もりは、Dynamics 365 Sales の見積もりに基づいて構築されています。</span><span class="sxs-lookup"><span data-stu-id="7a695-169">Project Operations quotes are built on the Dynamics 365 Sales quotes.</span></span> <span data-ttu-id="7a695-170">ただし、機能にはいくつかの重要な相違点があることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a695-170">However, there are some important differences in functionality that you should be aware of:</span></span>

- <span data-ttu-id="7a695-171">**変更**および**ライセンス認証**アクションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7a695-171">The **Revise** and **Activate** actions are not supported.</span></span>
- <span data-ttu-id="7a695-172">Project Operations の見積もりには、2つの異なるタイプの品目があります。</span><span class="sxs-lookup"><span data-stu-id="7a695-172">Project Operations quotes have two different types of lines.</span></span> <span data-ttu-id="7a695-173">1 つはプロジェクト用で、もう一方は製品用です。</span><span class="sxs-lookup"><span data-stu-id="7a695-173">One is for projects and the other is for products.</span></span>
- <span data-ttu-id="7a695-174">Project Operations の見積もりには、独自のフォームと UI 要素、業務ルール、プラグインのビジネス ロジック、および販売見積もりとは異なるクライアント側のスクリプトがあります。</span><span class="sxs-lookup"><span data-stu-id="7a695-174">Project Operations quotes have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Sales quotes.</span></span>

<span data-ttu-id="7a695-175">これらの理由から、販売見積もりと Project Operations 見積もりを同じ意味で使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7a695-175">For these reasons, it is not recommended to use a Sales quote and a Project Operations quote interchangeably.</span></span>
