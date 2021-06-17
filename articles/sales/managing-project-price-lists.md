---
title: 見積もりのプロジェクト価格表を管理する
description: このトピックでは、プロジェクトの価格表エンティティについての説明をします。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: da349924488fb62dc0b0bd8eaf4c48b02aa16d09
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996257"
---
# <a name="manage-project-price-lists-on-a-quote"></a><span data-ttu-id="d177c-103">見積もりのプロジェクト価格表を管理する</span><span class="sxs-lookup"><span data-stu-id="d177c-103">Manage project price lists on a quote</span></span>

<span data-ttu-id="d177c-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d177c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d177c-105">Dynamics 365 Project Operations は Dynamics 365 Sales の価格表エンティティを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d177c-105">Dynamics 365 Project Operations extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="d177c-106">主要なエンティティ</span><span class="sxs-lookup"><span data-stu-id="d177c-106">Key entities</span></span>

<span data-ttu-id="d177c-107">価格表には、次の 4 つの異なるエンティティによって提供される情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d177c-107">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="d177c-108">**価格表** : このエンティティには、コンテキスト、通貨、日付の有効性、および価格設定時間の時間単位に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-108">**Price List**: This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="d177c-109">コンテキストは、価格表が原価率または販売率のどちらを表すかを表わします。</span><span class="sxs-lookup"><span data-stu-id="d177c-109">Context shows whether the price list expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="d177c-110">**通貨** : このエンティティには、価格表の価格の通貨が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-110">**Currency**:  This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="d177c-111">**日付** : このエンティティは、システムがトランザクションの既定の価格を入力しようとするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-111">**Date**: This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="d177c-112">価格表は、トランザクションの日付などの日付有効性を持つ価格表を選択します。</span><span class="sxs-lookup"><span data-stu-id="d177c-112">A price list that has date effectivity that includes the date of the transaction is selected.</span></span> <span data-ttu-id="d177c-113">取引日に有効な価格表がひとつ以上あり、関連する見積書、契約書、組織単位に添付されている場合は、価格は既定にはなりません。</span><span class="sxs-lookup"><span data-stu-id="d177c-113">If  more than one price list is found that is effective for the transaction date and is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="d177c-114">**時間** : このエンティティは、日単位または時間単位など、価格が表現される時間の単位を格納します。</span><span class="sxs-lookup"><span data-stu-id="d177c-114">**Time**: This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="d177c-115">価格表エンティティには、価格を格納する次の 3 つの関連テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="d177c-115">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="d177c-116">**ロール価格** : このテーブルは、ロールと組織単位の値の組み合わせのレートを格納し、人的リソースのロールに基づいたの価格を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-116">**Role Price**: This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="d177c-117">**トランザクション カテゴリ価格** : このテーブルはトランザクション カテゴリごとに価格を格納し、経費カテゴリの価格を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-117">**Transaction Category Price**: This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="d177c-118">**価格表品目** : このテーブルには、カタログ製品の価格が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-118">**Price List Items**: This table stores prices for catalog products.</span></span>
 
<span data-ttu-id="d177c-119">価格表は価格カードです。</span><span class="sxs-lookup"><span data-stu-id="d177c-119">The price list is a rate card.</span></span> <span data-ttu-id="d177c-120">価格カードは、価格表エンティティと、ロール価格、トランザクション カテゴリ価格、および価格表品目テーブルの関連行の組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="d177c-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="d177c-121">リソースのロール</span><span class="sxs-lookup"><span data-stu-id="d177c-121">Resource roles</span></span>

<span data-ttu-id="d177c-122">*リソースのロール* という用語は、プロジェクトで特定のタスク セットを実行するために必要なスキル、コンピテンシー、および認定資格のセットを指します。</span><span class="sxs-lookup"><span data-stu-id="d177c-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="d177c-123">人的リソース時間は、特定のプロジェクトでリソースが果たすロールに基づいて見積もりされます。</span><span class="sxs-lookup"><span data-stu-id="d177c-123">Human resources time is quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="d177c-124">人的リソースの時間については、リソースのロールに基づいた原価計算と請求に対応しています。</span><span class="sxs-lookup"><span data-stu-id="d177c-124">For human resource time, costing and billing is based on resource role.</span></span> <span data-ttu-id="d177c-125">時間は、**時間** 出荷単位一覧の任意の単位で価格設定できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="d177c-126">**時間** の出荷単位は、プロジェクト オペレーションをインストールすると作成されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-126">The **Time** unit group is created when you install Project Operations.</span></span> <span data-ttu-id="d177c-127">既定の出荷単位は **時** です。</span><span class="sxs-lookup"><span data-stu-id="d177c-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="d177c-128">**時間** 出荷単位一覧、または **Hour (時)** 出荷グループの属性を削除、名称変更、または編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="d177c-128">You can't delete, rename, or edit the attributes fo the **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="d177c-129">ただし、**時間** 出荷単位一覧に他の出荷単位を追加できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="d177c-130">**時間** 出荷単位一覧、または **Hour (時)** 出荷単位のどちらかを削除しようとすると、ビジネス ロジックでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d177c-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the business logic.</span></span>
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="d177c-131">トランザクション カテゴリと経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d177c-131">Transaction categories and expense categories</span></span>

<span data-ttu-id="d177c-132">プロジェクト コンサルタントに発生する旅費およびその他の経費は、顧客に請求されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-132">Travel and other expenses that project consultants incur are billed to the customer.</span></span> <span data-ttu-id="d177c-133">経費カテゴリの価格設定は、価格表を利用することで完了します。</span><span class="sxs-lookup"><span data-stu-id="d177c-133">Pricing of expense categories is completed by using price lists.</span></span> <span data-ttu-id="d177c-134">経費カテゴリの例には、航空運賃、ホテル、およびレンタカーがあります。</span><span class="sxs-lookup"><span data-stu-id="d177c-134">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="d177c-135">各価格表の経費の行では、特定の経費カテゴリの価格を指定します。</span><span class="sxs-lookup"><span data-stu-id="d177c-135">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="d177c-136">経費カテゴリの価格設定には、次の 3 つの方法が使用されます :</span><span class="sxs-lookup"><span data-stu-id="d177c-136">The following three methods are used to price expense categories:</span></span>

- <span data-ttu-id="d177c-137">**コスト** : 経費コストは顧客に請求され、利幅は適用されません。</span><span class="sxs-lookup"><span data-stu-id="d177c-137">**At cost**: The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="d177c-138">**利幅率** : 実際のコストに対する割合が顧客に請求されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-138">**Markup percentage**: The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="d177c-139">**出荷単位ごとの価格** : 請求価格は、経費カテゴリの各出荷単位に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-139">**Price per unit**: A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="d177c-140">顧客に請求される金額は、コンサルタントが報告する経費の出荷単位の数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-140">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="d177c-141">マイレージは、出荷単位ごとの価格設定方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="d177c-141">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="d177c-142">たとえば、マイレージの経費カテゴリは、1 日あたり 30 米ドル (USD) または 1 マイルあたり 2 米ドルに設定できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-142">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="d177c-143">コンサルタントがプロジェクトのマイレージを報告する場合、請求額はコンサルタントが報告したマイル数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-143">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="d177c-144">プロジェクトの販売価格設定と上書き</span><span class="sxs-lookup"><span data-stu-id="d177c-144">Project sales pricing and overrides</span></span>

<span data-ttu-id="d177c-145">プロジェクトの見積もりと契約において、プロジェクトの価格表には製品の価格表とは異なる上書きパターンがあります。</span><span class="sxs-lookup"><span data-stu-id="d177c-145">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="d177c-146">製品カタログ ベースの見積依頼明細行では、各見積依頼明細行が正確に 1 つのカタログ品目を指すため、見積依頼明細行で価格をロールおよびカテゴリに直接上書きできます。</span><span class="sxs-lookup"><span data-stu-id="d177c-146">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="d177c-147">ただし、プロジェクト ベースの見積依頼明細行では、見積依頼明細行で価格をロールおよびカテゴリに直接上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d177c-147">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="d177c-148">プロジェクト価格表を使用して、2つの異なる指定パターンに対応できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-148">Use the project price list to support the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="d177c-149">価格設定を上書きする場合の 2 つの動作には違いがあるため、プロジェクト リソース用とカタログ品目用にそれぞれ価格表を持つことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d177c-149">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="d177c-150">次の各エンティティには、プロジェクトの価格設定用に 1 つ以上の関連する販売価格表を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="d177c-150">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="d177c-151">顧客 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="d177c-151">Customer (account)</span></span> 
- <span data-ttu-id="d177c-152">営業案件</span><span class="sxs-lookup"><span data-stu-id="d177c-152">Opportunity</span></span> 
- <span data-ttu-id="d177c-153">見積もり</span><span class="sxs-lookup"><span data-stu-id="d177c-153">Quote</span></span> 
- <span data-ttu-id="d177c-154">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="d177c-154">Project Contract</span></span>

<span data-ttu-id="d177c-155">これらのエンティティと価格表の関連付けは、プロジェクト価格表によって示されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-155">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="d177c-156">顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、1 つ以上の価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d177c-156">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="d177c-157">既定のプロジェクト価格表は、顧客レコードに自動的に入力されません。</span><span class="sxs-lookup"><span data-stu-id="d177c-157">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="d177c-158">ただし、顧客レコードに手動でプロジェクト価格表を添付できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-158">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="d177c-159">それでも、顧客とのカスタムの価格設定について合意がある場合にのみ、手動でプロジェクト価格表を添付してください。</span><span class="sxs-lookup"><span data-stu-id="d177c-159">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="d177c-160">プロジェクト価格表が営業エンティティに添付されると、次の情報を検証します :</span><span class="sxs-lookup"><span data-stu-id="d177c-160">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="d177c-161">価格表が **営業** のコンテキストを保有している。</span><span class="sxs-lookup"><span data-stu-id="d177c-161">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="d177c-162">価格表の通貨が顧客の通貨と一致している。</span><span class="sxs-lookup"><span data-stu-id="d177c-162">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="d177c-163">プロジェクト契約では、次の優先順位を使用して、関連するプロジェクト価格表を自動的に設定します :</span><span class="sxs-lookup"><span data-stu-id="d177c-163">On a project contract, the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="d177c-164">見積もり </span><span class="sxs-lookup"><span data-stu-id="d177c-164">Quote</span></span>
2. <span data-ttu-id="d177c-165">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="d177c-165">Opportunity</span></span>
3. <span data-ttu-id="d177c-166">顧客</span><span class="sxs-lookup"><span data-stu-id="d177c-166">Customer</span></span> 
4. <span data-ttu-id="d177c-167">グローバル設定</span><span class="sxs-lookup"><span data-stu-id="d177c-167">Global settings</span></span> 

<span data-ttu-id="d177c-168">既定のプロジェクト価格表が入力されると、システムは通貨が顧客の通貨と一致すること、および入力された既定の価格表が **営業** コンテキストを保有していることを検証します。</span><span class="sxs-lookup"><span data-stu-id="d177c-168">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="d177c-169">顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、複数のプロジェクト価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d177c-169">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="d177c-170">この機能は、長期にわたるプロジェクト契約の日付固有の既定の価格をサポートします。この場合、インフレによって発生する価格更新に対応するため、アカウントに複数の価格表が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d177c-170">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="d177c-171">ただし、顧客、営業案件、見積もり、またはプロジェクト契約のエンティティに関連付けられている価格表の日付の有効性が重複していると、既定の価格が正しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d177c-171">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="d177c-172">そのため、日付の有効性が重複しているプロジェクト価格表がそれらのエンティティに関連付けられていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d177c-172">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="d177c-173">取引固有の価格の上書き</span><span class="sxs-lookup"><span data-stu-id="d177c-173">Deal-specific price overrides</span></span>

<span data-ttu-id="d177c-174">見積もりやプロジェクト契約に既定で入力されるプロジェクト価格表で選択した価格の取引固有の上書きを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-174">You can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="d177c-175">既定では、プロジェクト契約は、直接リンクの代わりにマスター販売価格表のコピーを常に取得します。</span><span class="sxs-lookup"><span data-stu-id="d177c-175">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="d177c-176">この動作は、マスター価格表が変更された場合に、作業指示書 (SOW) についての顧客との価格合意が変更されないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d177c-176">This behavior helps guarantee that price agreements that are made with a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="d177c-177">ただし、見積もりではマスター価格表を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-177">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="d177c-178">または、マスター価格表をコピーして編集し、その見積もりのみに適用されるカスタム価格表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d177c-178">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="d177c-179">見積もりに固有の新しい価格表を作成するには、**見積もり** ページで **カスタム価格の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d177c-179">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="d177c-180">取引固有のプロジェクト価格表は見積もりからのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d177c-180">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="d177c-181">カスタム プロジェクト価格表を作成すると、価格表のプロジェクト コンポーネントのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d177c-181">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="d177c-182">つまり、見積もりに添付されている既存のプロジェクト価格表のコピーとして作成された新しい価格表であり、この新しい価格表には関連するロール価格とトランザクション カテゴリ価格のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d177c-182">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>
  
## <a name="tracking-costs"></a><span data-ttu-id="d177c-183">コストの追跡</span><span class="sxs-lookup"><span data-stu-id="d177c-183">Tracking costs</span></span>

<span data-ttu-id="d177c-184">プロジェクト オペレーションは、プロジェクトでの人的リソース時間の使用についてのコストを追跡します。</span><span class="sxs-lookup"><span data-stu-id="d177c-184">Project Operations tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="d177c-185">また、旅費などのプロジェクト中に発生したその他の経費のコストも追跡します。</span><span class="sxs-lookup"><span data-stu-id="d177c-185">It also tracks costs for other expenses that are incurred during the project, such as travel expenses.</span></span>

<span data-ttu-id="d177c-186">請求レートと同様に、人的リソースのコスト レートも価格表を使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-186">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="d177c-187">原価表と販売価格表の動作の主な違いは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d177c-187">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="d177c-188">リソースのコスト レートは、特定のプロジェクト、契約、または見積もりで上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d177c-188">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="d177c-189">ただし、取引の性質に固有の変更が行われた場合、取引ごとに請求レートが上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d177c-189">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="d177c-190">次の順序は、原価価格表を解決するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d177c-190">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="d177c-191">組織単位に添付されている原価価格表。</span><span class="sxs-lookup"><span data-stu-id="d177c-191">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="d177c-192">プロジェクト オペレーションのパラメーターに添付されている原価価格表。</span><span class="sxs-lookup"><span data-stu-id="d177c-192">The cost price list that is attached to the Project Operations parameters.</span></span> <span data-ttu-id="d177c-193">多くの異なる通貨の原価価格表をプロジェクト サービスのパラメーターに添付できるため、プロジェクト、契約、または見積もりの契約組織単位の通貨と原価価格表の通貨の間で通貨照合を完了します。</span><span class="sxs-lookup"><span data-stu-id="d177c-193">Because cost price lists in many different currencies can be attached to the parameters, a currency match is completed between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="d177c-194">経費については、コスト価格設定方法およびコストに対する利幅価格設定方法は原価価格表には適用されません。</span><span class="sxs-lookup"><span data-stu-id="d177c-194">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="d177c-195">これらの価格設定方法を原価価格表の行で使用してトランザクション カテゴリ コストを設定しても、システムはそれらを無視し、既定の原価価格は入力されません。</span><span class="sxs-lookup"><span data-stu-id="d177c-195">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]