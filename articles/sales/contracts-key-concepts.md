---
title: プロジェクト契約 - 重要な概念
description: このトピックでは、Dynamics Project Operations における主要な概念について解説します。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24b3fcd74e4167ba419e12c890a119d22c54c99a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175537"
---
# <a name="project-contracts---key-concepts"></a><span data-ttu-id="d6e58-103">プロジェクト契約 - 重要な概念</span><span class="sxs-lookup"><span data-stu-id="d6e58-103">Project contracts - Key concepts</span></span>

<span data-ttu-id="d6e58-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d6e58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d6e58-105">このトピックでは、Dynamics 365 Project Operations でプロジェクト契約を使い始める前に知っておくべき重要な概念について解説します :</span><span class="sxs-lookup"><span data-stu-id="d6e58-105">This topic provides the key concepts to be aware of before you begin using Project contracts in Dynamics 365 Project Operations:</span></span>

## <a name="owning-company"></a><span data-ttu-id="d6e58-106">所有会社</span><span class="sxs-lookup"><span data-stu-id="d6e58-106">Owning Company</span></span>

<span data-ttu-id="d6e58-107">所有会社は、Dynamics 365 Finance に由来する Project Operations 向けの **プロジェクト管理および会計** モジュールの法人格です。</span><span class="sxs-lookup"><span data-stu-id="d6e58-107">The owning company is the legal entity from the **Project management and accounting** module for Project Operations from Dynamics 365 Finance.</span></span> <span data-ttu-id="d6e58-108">所有会社は、取引から発生する費用や収益を計上する法人を表します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-108">The owning company represents the legal entity that will account for the cost and revenue that accrues from a deal.</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="d6e58-109">契約単位</span><span class="sxs-lookup"><span data-stu-id="d6e58-109">Contracting Unit</span></span>

<span data-ttu-id="d6e58-110">契約単位は、プロジェクトの実施を所有する部門または業務を表します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-110">The contracting unit represents the division or practice that owns the delivery of the project.</span></span> <span data-ttu-id="d6e58-111">各契約単位ごとにリソース コストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-111">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="d6e58-112">リソースのコストを指定すると、リソースごとに異なるコスト レートを設定することも可能です。</span><span class="sxs-lookup"><span data-stu-id="d6e58-112">When you specify the resource cost for a resource, you will also be able to set up different cost rates for resources.</span></span> <span data-ttu-id="d6e58-113">この契約部門は、企業内の他の部門または慣行からこれらのリソースを借用しています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-113">This contracting unit borrows these resources from other division or practices within the enterprise.</span></span> <span data-ttu-id="d6e58-114">リソースのコスト レートは、移転価格、リソース借入、為替価格。</span><span class="sxs-lookup"><span data-stu-id="d6e58-114">The cost rates for the resources are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="d6e58-115">他の部門からリソースを借りるためにコスト レートを設定する場合は、貸出部門の通貨を使用します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-115">When you set up the cost rates to borrow resources from other divisions, use the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="d6e58-116">原価の通貨</span><span class="sxs-lookup"><span data-stu-id="d6e58-116">Cost Currency</span></span>

<span data-ttu-id="d6e58-117">コスト通貨とは、画面上でコストが報告される通貨のことです。</span><span class="sxs-lookup"><span data-stu-id="d6e58-117">Cost currency is the currency in which costs are reported on screen.</span></span> <span data-ttu-id="d6e58-118">この通貨は、契約書やプロジェクトの **契約単位** フィールドに添付されている通貨から派生しています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-118">This currency is derived from the currency attached to the **Contracting Unit** field on the contract and the project.</span></span> <span data-ttu-id="d6e58-119">コストは、プロジェクトに対して任意の通貨で記録できます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-119">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="d6e58-120">ただし、画面に表示されている場合は、コストを計上した通貨からプロジェクトのコスト通貨への換算があります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-120">However, there is currency conversion from the currency the costs were recorded in, to the cost currency of the project when shown on the screen.</span></span>

<span data-ttu-id="d6e58-121">Common Data Service (CDS) プラット フォームの為替レートは日付を有効化できないため、為替レートを更新すると、画面上のコストの合計が時間の経過とともに変化する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-121">Because the exchange rates in the Common Data Service (CDS) platform can't be date effective, the on-screen totals for cost may change over time if you update the currency exchange rates.</span></span> <span data-ttu-id="d6e58-122">ただし、データベースに記録されているコストは、発生した通貨で保存されているため、変更されません。</span><span class="sxs-lookup"><span data-stu-id="d6e58-122">However, costs as recorded in the database remain unchanged because the amounts are stored in the currency that were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="d6e58-123">販売通貨</span><span class="sxs-lookup"><span data-stu-id="d6e58-123">Sales Currency</span></span>

<span data-ttu-id="d6e58-124">Project Operations の販売通貨は、推定および販売実績額が記録および表示される通貨です。</span><span class="sxs-lookup"><span data-stu-id="d6e58-124">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="d6e58-125">また、販売通貨は、取引の際に顧客に請求される通貨でもあります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-125">Sales currency is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="d6e58-126">プロジェクト契約では、販売通貨は顧客または取引先企業レコードから既定で設定され、契約作成時に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-126">On a project contract, the sales currency defaults from the customer or account record and can be changed during when the contract is created.</span></span> <span data-ttu-id="d6e58-127">落札された見積もりをクローズすることで契約が作成されると、契約の通貨は見積もりの通貨から既定に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-127">When a contract is created by closing a quote as won, the currency on the contract is defaulted from the currency on the quote.</span></span>

<span data-ttu-id="d6e58-128">プロジェクト契約を最初から作成する場合、**販売通貨** フィールドは編集できません。</span><span class="sxs-lookup"><span data-stu-id="d6e58-128">When you create a project contract from scratch, the **Sales Currency** field can't be edited.</span></span> <span data-ttu-id="d6e58-129">既定では、製品およびプロジェクトの価格リストは、契約上のこの通貨に基づいています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-129">Product and project price lists default based on this currency on the contract.</span></span>

<span data-ttu-id="d6e58-130">原価とは異なり、販売額は販売通貨でのみ記録可能となっています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-130">Unlike costs, sales values can only be recorded in the sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="d6e58-131">請求方法</span><span class="sxs-lookup"><span data-stu-id="d6e58-131">Billing Method</span></span>

<span data-ttu-id="d6e58-132">プロジェクトの契約モデルには、一般的に定額制と消費ベースの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-132">There are typically two types of contracting models for projects, fixed fee and consumption-based.</span></span> <span data-ttu-id="d6e58-133">これらのモデルは、2 つの可能値を持つ課金方法として、Project Operations で表現されます :</span><span class="sxs-lookup"><span data-stu-id="d6e58-133">These models are represented in Project Operations as billing methods with two possible values:</span></span>

- <span data-ttu-id="d6e58-134">時間と材料 : 発生した各コストを対応する収益に裏付けされた消費ベースの契約モデル。</span><span class="sxs-lookup"><span data-stu-id="d6e58-134">Time and Material: A consumption-based contracting model where each incurred cost is backed by corresponding revenue.</span></span> <span data-ttu-id="d6e58-135">見積もりや費用が増えると、それに応じた見積額や実売額も増加します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-135">As you estimate or incur more costs, the corresponding estimated and actual sales also increase.</span></span> <span data-ttu-id="d6e58-136">この請求方法を持つ契約品目について、実際の収益を相殺する超過しない限度額を指定します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-136">Specify not-to-exceed limits on contract lines that have this billing method, which caps off the actual revenue.</span></span> <span data-ttu-id="d6e58-137">売上見込みは、上限を超えないことによる影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="d6e58-137">Estimated revenue isn't impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="d6e58-138">固定価格: これは、販売額が発生したコストに依存しないことを示す固定料金契約モデルです。</span><span class="sxs-lookup"><span data-stu-id="d6e58-138">Fixed Price: A fixed fee contracting model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="d6e58-139">販売額は固定されいるため、見積もりや追加のコストが発生しても変化しません。</span><span class="sxs-lookup"><span data-stu-id="d6e58-139">The sales value is fixed and doesn't change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="d6e58-140">プロジェクト価格表</span><span class="sxs-lookup"><span data-stu-id="d6e58-140">Project Price lists</span></span>

<span data-ttu-id="d6e58-141">プロジェクト価格表は、時間、費用、その他のプロジェクト関連コンポーネントのコスト レートではなく、既定の価格として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-141">Project price lists are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="d6e58-142">複数の価格表が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-142">There can be multiple prices lists.</span></span> <span data-ttu-id="d6e58-143">各価格表には、プロジェクト契約ごとに有効期限が設定されています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-143">Each price list has its own date effectivity for each project contract.</span></span> <span data-ttu-id="d6e58-144">プロジェクト価格表での重複する日付の有効性は、Project Operations では対応していません。</span><span class="sxs-lookup"><span data-stu-id="d6e58-144">Overlapping date-effectivity on project price lists isn't supported in Project Operations.</span></span>

<span data-ttu-id="d6e58-145">プロジェクト見積もりを獲得してプロジェクト契約を作成すると、プロジェクトの価格表が契約名と日付を含めてコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-145">When a project contract is created by winning a project quote, project price lists are copied with the contract name and date included.</span></span> <span data-ttu-id="d6e58-146">この情報をコピーすると、このプロジェクト契約のプロジェクト コンポーネントのカスタム価格が構成されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-146">Copying this information constitutes custom pricing for project components on this project contract.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="d6e58-147">トランザクション クラス</span><span class="sxs-lookup"><span data-stu-id="d6e58-147">Transaction Classes</span></span>

<span data-ttu-id="d6e58-148">Project Operations は、次の 4 種類のトランザクション クラスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-148">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="d6e58-149">時間</span><span class="sxs-lookup"><span data-stu-id="d6e58-149">Time</span></span>
- <span data-ttu-id="d6e58-150">経費</span><span class="sxs-lookup"><span data-stu-id="d6e58-150">Expense</span></span>
- <span data-ttu-id="d6e58-151">材料</span><span class="sxs-lookup"><span data-stu-id="d6e58-151">Material</span></span>
- <span data-ttu-id="d6e58-152">料金</span><span class="sxs-lookup"><span data-stu-id="d6e58-152">Fee</span></span>

<span data-ttu-id="d6e58-153">コストと販売額は、時間、経費、および材料のトランザクション クラスで見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-153">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="d6e58-154">手数料は、売上のみのトランザクション クラスです。</span><span class="sxs-lookup"><span data-stu-id="d6e58-154">Fee is a revenue-only transaction class.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="d6e58-155">作業エンティティと請求エンティティ</span><span class="sxs-lookup"><span data-stu-id="d6e58-155">Work entities and Billing entities</span></span>

<span data-ttu-id="d6e58-156">作業を表すエンティティは、プロジェクトとタスクです。</span><span class="sxs-lookup"><span data-stu-id="d6e58-156">Entities that represent work are projects and tasks.</span></span> <span data-ttu-id="d6e58-157">請求を表すエンティティは、契約品目です。</span><span class="sxs-lookup"><span data-stu-id="d6e58-157">Entities that represent billing aspects are contract lines.</span></span> <span data-ttu-id="d6e58-158">異なる作業エンティティを契約品目に関連付けることで、請求オプションに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-158">You can tie different work entities to billing options by tying them to contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="d6e58-159">複数の顧客との取引</span><span class="sxs-lookup"><span data-stu-id="d6e58-159">Multi-customer deals</span></span>

<span data-ttu-id="d6e58-160">複数の顧客との取引では、複数の顧客が取引上の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-160">Multi- customer deals have more than one customer to invoice on a deal.</span></span> <span data-ttu-id="d6e58-161">一般的な例は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="d6e58-161">Common examples of this include:</span></span>

- <span data-ttu-id="d6e58-162">OEM 企業とそのパートナー : パートナーや再販業者は、付加価値のあるサービスで製品を販売しており、通常は顧客との特定の取引を伴います。</span><span class="sxs-lookup"><span data-stu-id="d6e58-162">OEM Enterprises and their partners: Partners and resellers sell a product with some value-added services, typically involving a particular deal with a customer.</span></span> <span data-ttu-id="d6e58-163">OEMは、プロジェクトの一部に資金を提供することを提案します。</span><span class="sxs-lookup"><span data-stu-id="d6e58-163">The OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="d6e58-164">公的機関のプロジェクト: 地方自治体の複数の部署がプロジェクトに資金を提供することに同意し、以前に合意された分割に従って請求されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-164">Public sector projects: Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="d6e58-165">例えば、学区と地方自治体がプール建設のための資金提供に合意したとします。</span><span class="sxs-lookup"><span data-stu-id="d6e58-165">For example, s school district and the local government agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="d6e58-166">請求書スケジュール</span><span class="sxs-lookup"><span data-stu-id="d6e58-166">Invoice Schedules</span></span>

<span data-ttu-id="d6e58-167">請求書のスケジュールは各契約品目に固有であり、自動請求が機能するために必要となります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-167">Invoice schedules are specific to each contract line and are required for automatic invoicing to work.</span></span> <span data-ttu-id="d6e58-168">請求書のスケジュールは、特定の開始日と終了日、および請求頻度に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-168">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="d6e58-169">スケジュールは、請求書の自動作成処理が設定されている場合、契約ステージで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-169">The schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="d6e58-170">見積書からプロジェクト契約書を作成すると、見積書からプロジェクト契約書に請求書スケジュールがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-170">When a project contract is created from a quote, the invoice schedule is copied to the project contract from the quote.</span></span>

## <a name="changes-from-dynamics-365-sales-orders"></a><span data-ttu-id="d6e58-171">Dynamics 365 Sales Orders からの変更点</span><span class="sxs-lookup"><span data-stu-id="d6e58-171">Changes from Dynamics 365 Sales Orders</span></span>

<span data-ttu-id="d6e58-172">Project Operations の契約は、Dynamics 365 Sales の注文に基づいて構築されます。</span><span class="sxs-lookup"><span data-stu-id="d6e58-172">Contracts in Project Operations are built on Orders in Dynamics 365 Sales.</span></span> <span data-ttu-id="d6e58-173">しかし、重要な偏差や機能の違いがあります。</span><span class="sxs-lookup"><span data-stu-id="d6e58-173">However, there are important deviations and differences in functionality.</span></span> <span data-ttu-id="d6e58-174">契約には、独自のフォームや UI 要素、ビジネス ルール、プラグイン内のビジネス ロジック、クライアント サイドのスクリプトがあり、受注書とは異なる独自のものとなっています。</span><span class="sxs-lookup"><span data-stu-id="d6e58-174">Contracts have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Orders.</span></span> <span data-ttu-id="d6e58-175">これらの理由から、販売注文と Project Operations 契約を区別なく使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d6e58-175">For these reasons, don't use a Sales order and Project Operations contract interchangeably.</span></span>
