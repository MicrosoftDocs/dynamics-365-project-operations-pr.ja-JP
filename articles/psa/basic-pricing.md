---
title: プロジェクトの価格設定
description: このトピックでは、Dynamics 365 Project Service Automation での価格設定の仕組みについて説明します。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2337a1cef55ecc3b7625a0c9a643b9ed8a1d70e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291175"
---
# <a name="project-pricing"></a><span data-ttu-id="84204-103">プロジェクトの価格設定</span><span class="sxs-lookup"><span data-stu-id="84204-103">Project pricing</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="84204-104">Dynamics 365 Project Service Automation は Dynamics 365 Sales の価格表エンティティを拡張します。</span><span class="sxs-lookup"><span data-stu-id="84204-104">Dynamics 365 Project Service Automation extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="84204-105">主要なエンティティ</span><span class="sxs-lookup"><span data-stu-id="84204-105">Key entities</span></span>

<span data-ttu-id="84204-106">価格表には、次の 4 つの異なるエンティティによって提供される情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="84204-106">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="84204-107">**価格表** - このエンティティには、コンテキスト、通貨、日付の有効性、および価格設定時間の時間単位に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="84204-107">**Price List** - This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="84204-108">コンテキストは、価格表が原価率または販売率のどちらを表すかを示します。</span><span class="sxs-lookup"><span data-stu-id="84204-108">Context shows whether the price list is expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="84204-109">**通貨** - このエンティティには、価格表の価格の通貨が格納されます。</span><span class="sxs-lookup"><span data-stu-id="84204-109">**Currency** - This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="84204-110">**日付** - このエンティティは、システムがトランザクションの既定の価格を入力しようとするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="84204-110">**Date** - This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="84204-111">PSA の価格設定は、トランザクションの日付などの日付有効性を持つ価格表を選択します。</span><span class="sxs-lookup"><span data-stu-id="84204-111">PSA pricing selects the price list that has date effectivity that includes the date of the transaction.</span></span> <span data-ttu-id="84204-112">PSA の価格設定が、関連する見積もり、契約、または組織単位に添付されているトランザクションの日付に有効な複数の価格表を見つけた場合、価格は既定にはなりません。</span><span class="sxs-lookup"><span data-stu-id="84204-112">If PSA pricing finds more than one price list that is effective for the transaction date is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="84204-113">**時間** - このエンティティは、日単位または時間単位など、価格が表現される時間の単位を格納します。</span><span class="sxs-lookup"><span data-stu-id="84204-113">**Time** - This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="84204-114">価格表エンティティには、価格を格納する次の 3 つの関連テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="84204-114">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="84204-115">**ロール価格** - このテーブルは、ロールと組織単位の値の組み合わせのレートを格納し、人的リソースのロールベースの価格を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84204-115">**Role Price** - This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="84204-116">**トランザクション カテゴリ価格** - このテーブルはトランザクション カテゴリごとに価格を格納し、経費カテゴリの価格を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84204-116">**Transaction Category Price** - This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="84204-117">**価格表品目** - このテーブルには、カタログ製品の価格が格納されます。</span><span class="sxs-lookup"><span data-stu-id="84204-117">**Price List Items** - This table stores prices for catalog products.</span></span>

> ![価格表を使用した価格の設定](media/basic-guide-12.png)
 
<span data-ttu-id="84204-119">価格表は価格カードです。</span><span class="sxs-lookup"><span data-stu-id="84204-119">The price list is a rate card.</span></span> <span data-ttu-id="84204-120">価格カードは、価格表エンティティと、ロール価格、トランザクション カテゴリ価格、および価格表品目テーブルの関連行の組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="84204-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="84204-121">リソースのロール</span><span class="sxs-lookup"><span data-stu-id="84204-121">Resource roles</span></span>

<span data-ttu-id="84204-122">*リソースのロール* という用語は、プロジェクトで特定のタスク セットを実行するために必要なスキル、コンピテンシー、および認定資格のセットを指します。</span><span class="sxs-lookup"><span data-stu-id="84204-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="84204-123">人的リソース時間は、通常、特定のプロジェクトでリソースが果たすロールに基づいて見積もりされます。</span><span class="sxs-lookup"><span data-stu-id="84204-123">Human resources time is usually quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="84204-124">人的リソース時間については、PSA はリソースのロールに基づいた原価計算と請求をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="84204-124">For human resource time, PSA supports costing and billing that are based on resource role.</span></span> <span data-ttu-id="84204-125">時間は、**時間** 出荷単位一覧の任意の単位で価格設定できます。</span><span class="sxs-lookup"><span data-stu-id="84204-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="84204-126">PSA がインストールされると、**時間** 出荷単位一覧が作成されます。</span><span class="sxs-lookup"><span data-stu-id="84204-126">The **Time** unit group is crated when PSA is installed.</span></span> <span data-ttu-id="84204-127">既定の出荷単位は **時** です。</span><span class="sxs-lookup"><span data-stu-id="84204-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="84204-128">**時間** 出荷単位一覧または **時** 出荷単位の属性を削除、名称変更、または編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="84204-128">You can't delete, rename, or edit the attributes fo teh **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="84204-129">ただし、**時間** 出荷単位一覧に他の出荷単位を追加できます。</span><span class="sxs-lookup"><span data-stu-id="84204-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="84204-130">**時間** 出荷単位一覧または **時** 出荷単位のどちらかを削除しようとすると、PSA ビジネス ロジックでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84204-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the PSA business logic.</span></span>

> ![ロールによる価格の設定](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="84204-132">トランザクション カテゴリと経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="84204-132">Transaction categories and expense categories</span></span>

<span data-ttu-id="84204-133">通常、プロジェクト コンサルタントに発生する旅費およびその他の経費は、顧客に請求されます。</span><span class="sxs-lookup"><span data-stu-id="84204-133">Travel and other expenses that project consultants incur are usually billed to the customer.</span></span> <span data-ttu-id="84204-134">PSA は、価格表を使用することにより、経費カテゴリの価格設定をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="84204-134">PSA supports pricing of expense categories by using price lists.</span></span> <span data-ttu-id="84204-135">経費カテゴリの例には、航空運賃、ホテル、およびレンタカーがあります。</span><span class="sxs-lookup"><span data-stu-id="84204-135">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="84204-136">各価格表の経費の行では、特定の経費カテゴリの価格を指定します。</span><span class="sxs-lookup"><span data-stu-id="84204-136">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="84204-137">経費カテゴリの価格設定について、PSA は次の 3 つの価格設定方法をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="84204-137">For pricing of expense categories, PSA supports the following three pricing methods:</span></span>

- <span data-ttu-id="84204-138">**コスト** - 経費コストは顧客に請求され、利幅は適用されません。</span><span class="sxs-lookup"><span data-stu-id="84204-138">**At cost** - The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="84204-139">**利幅率** - 実際のコストに対する割合が顧客に請求されます。</span><span class="sxs-lookup"><span data-stu-id="84204-139">**Markup percentage** - The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="84204-140">**出荷単位ごとの価格** - 請求価格は、経費カテゴリの各出荷単位に設定されます。</span><span class="sxs-lookup"><span data-stu-id="84204-140">**Price per unit** - A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="84204-141">顧客に請求される金額は、コンサルタントが報告する経費の出荷単位の数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="84204-141">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="84204-142">マイレージは、出荷単位ごとの価格設定方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="84204-142">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="84204-143">たとえば、マイレージの経費カテゴリは、1 日あたり 30 米ドル (USD) または 1 マイルあたり 2 米ドルに設定できます。</span><span class="sxs-lookup"><span data-stu-id="84204-143">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="84204-144">コンサルタントがプロジェクトのマイレージを報告する場合、請求額はコンサルタントが報告したマイル数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="84204-144">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>

> ![経費カテゴリに関する価格の設定](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="84204-146">プロジェクトの販売価格設定と上書き</span><span class="sxs-lookup"><span data-stu-id="84204-146">Project sales pricing and overrides</span></span>

<span data-ttu-id="84204-147">プロジェクトの見積もりと契約において、プロジェクトの価格表には製品の価格表とは異なる上書きパターンがあります。</span><span class="sxs-lookup"><span data-stu-id="84204-147">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="84204-148">製品カタログ ベースの見積依頼明細行では、各見積依頼明細行が正確に 1 つのカタログ品目を指すため、見積依頼明細行で価格をロールおよびカテゴリに直接上書きできます。</span><span class="sxs-lookup"><span data-stu-id="84204-148">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="84204-149">ただし、プロジェクト ベースの見積依頼明細行では、見積依頼明細行で価格をロールおよびカテゴリに直接上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="84204-149">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="84204-150">2 つの異なる上書きパターンをサポートするために、PSA は新しい価格表の関連付けであるプロジェクト価格表を導入しました。</span><span class="sxs-lookup"><span data-stu-id="84204-150">To support the two distinct override patterns, PSA has introduced a new price list association, the project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="84204-151">価格設定を上書きする場合の 2 つの動作には違いがあるため、プロジェクト リソース用とカタログ品目用にそれぞれ価格表を持つことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="84204-151">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="84204-152">次の各エンティティには、プロジェクトの価格設定用に 1 つ以上の関連する販売価格表を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="84204-152">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="84204-153">顧客 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="84204-153">Customer (account)</span></span> 
- <span data-ttu-id="84204-154">営業案件</span><span class="sxs-lookup"><span data-stu-id="84204-154">Opportunity</span></span> 
- <span data-ttu-id="84204-155">見積もり</span><span class="sxs-lookup"><span data-stu-id="84204-155">Quote</span></span> 
- <span data-ttu-id="84204-156">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="84204-156">Project Contract</span></span>

<span data-ttu-id="84204-157">これらのエンティティと価格表の関連付けは、プロジェクト価格表によって示されます。</span><span class="sxs-lookup"><span data-stu-id="84204-157">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="84204-158">顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、1 つ以上の価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="84204-158">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="84204-159">既定のプロジェクト価格表は、顧客レコードに自動的に入力されません。</span><span class="sxs-lookup"><span data-stu-id="84204-159">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="84204-160">ただし、顧客レコードに手動でプロジェクト価格表を添付できます。</span><span class="sxs-lookup"><span data-stu-id="84204-160">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="84204-161">それでも、顧客とのカスタムの価格設定について合意がある場合にのみ、手動でプロジェクト価格表を添付してください。</span><span class="sxs-lookup"><span data-stu-id="84204-161">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="84204-162">プロジェクト価格表が営業エンティティに添付されると、PSA は次の情報を検証します。</span><span class="sxs-lookup"><span data-stu-id="84204-162">When a project price list is attached to a sales entity, PSA validates the following information:</span></span>

- <span data-ttu-id="84204-163">価格表が **営業** コンテキストを持っている。</span><span class="sxs-lookup"><span data-stu-id="84204-163">The price list las a context of **Sales**.</span></span> 
- <span data-ttu-id="84204-164">価格表の通貨が顧客の通貨と一致している。</span><span class="sxs-lookup"><span data-stu-id="84204-164">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="84204-165">プロジェクト契約では、PSA は次の優先順位を使用して、関連するプロジェクト価格表を自動的に設定します。</span><span class="sxs-lookup"><span data-stu-id="84204-165">On a project contract, PSA uses the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="84204-166">見積もり</span><span class="sxs-lookup"><span data-stu-id="84204-166">Quote</span></span>
2. <span data-ttu-id="84204-167">営業案件</span><span class="sxs-lookup"><span data-stu-id="84204-167">Opportunity</span></span>
3. <span data-ttu-id="84204-168">Customer</span><span class="sxs-lookup"><span data-stu-id="84204-168">Customer</span></span> 
4. <span data-ttu-id="84204-169">PSA 用のグローバル設定</span><span class="sxs-lookup"><span data-stu-id="84204-169">Global settings for PSA</span></span>

<span data-ttu-id="84204-170">プロジェクト価格表が既定で入力されると、PSA は通貨が顧客の通貨と一致すること、および入力された既定の価格表が **営業** コンテキストを持っていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="84204-170">When a project price list is entered by default, PSA validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="84204-171">顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、複数のプロジェクト価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="84204-171">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="84204-172">この機能は、長期にわたるプロジェクト契約の日付固有の既定の価格をサポートします。この場合、インフレによって発生する価格更新に対応するため、アカウントに複数の価格表が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="84204-172">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="84204-173">ただし、顧客、営業案件、見積もり、またはプロジェクト契約のエンティティに関連付けられている価格表の日付の有効性が重複していると、既定の価格が正しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="84204-173">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="84204-174">そのため、日付の有効性が重複しているプロジェクト価格表がそれらのエンティティに関連付けられていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84204-174">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="84204-175">取引固有の価格の上書き</span><span class="sxs-lookup"><span data-stu-id="84204-175">Deal-specific price overrides</span></span>

<span data-ttu-id="84204-176">PSA では、見積もりやプロジェクト契約に既定で入力されるプロジェクト価格表で選択した価格の取引固有の上書きを作成できます。</span><span class="sxs-lookup"><span data-stu-id="84204-176">In PSA, you can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="84204-177">既定では、プロジェクト契約は、直接リンクの代わりにマスター販売価格表のコピーを常に取得します。</span><span class="sxs-lookup"><span data-stu-id="84204-177">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="84204-178">この動作は、マスター価格表が変更された場合に、作業指示書 (SOW) についての顧客との価格の合意が変更されないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="84204-178">This behavior helps guarantee that price agreements that are made iwth a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="84204-179">ただし、見積もりではマスター価格表を使用できます。</span><span class="sxs-lookup"><span data-stu-id="84204-179">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="84204-180">または、マスター価格表をコピーして編集し、その見積もりのみに適用されるカスタム価格表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="84204-180">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="84204-181">見積もりに固有の新しい価格表を作成するには、**見積もり** ページで **カスタム価格の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84204-181">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="84204-182">取引固有のプロジェクト価格表は見積もりからのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="84204-182">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="84204-183">カスタム プロジェクト価格表を作成すると、価格表のプロジェクト コンポーネントのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="84204-183">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="84204-184">つまり、見積もりに添付されている既存のプロジェクト価格表のコピーとして作成された新しい価格表であり、この新しい価格表には関連するロール価格とトランザクション カテゴリ価格のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="84204-184">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>

> ![プロジェクト契約のカスタム価格の表示と設定](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a><span data-ttu-id="84204-186">コストの追跡</span><span class="sxs-lookup"><span data-stu-id="84204-186">Tracking costs</span></span>

<span data-ttu-id="84204-187">PSA は、プロジェクトでの人的リソース時間の使用についてのコストを追跡します。</span><span class="sxs-lookup"><span data-stu-id="84204-187">PSA tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="84204-188">また、旅費など、プロジェクト中に発生した他の経費のコストも追跡します。</span><span class="sxs-lookup"><span data-stu-id="84204-188">It also tracks costs for other expenses that are incurrred during hte project, such as travel expenses.</span></span>

<span data-ttu-id="84204-189">請求レートと同様に、人的リソースのコスト レートも価格表を使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="84204-189">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="84204-190">原価表と販売価格表の動作の主な違いは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="84204-190">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="84204-191">リソースのコスト レートは、特定のプロジェクト、契約、または見積もりで上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="84204-191">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="84204-192">ただし、取引の性質に固有の変更が行われた場合、取引ごとに請求レートが上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84204-192">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="84204-193">次の順序は、原価価格表を解決するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84204-193">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="84204-194">組織単位に添付されている原価価格表。</span><span class="sxs-lookup"><span data-stu-id="84204-194">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="84204-195">Project Service のパラメーターに添付されている原価価格表。</span><span class="sxs-lookup"><span data-stu-id="84204-195">The cost price list that is attached to the project service parameters.</span></span> <span data-ttu-id="84204-196">多くの異なる通貨の原価価格表を Project Service のパラメーターに添付できるため、PSA はプロジェクト、契約、または見積もりの契約組織単位の通貨と原価価格表の通貨の間で通貨照合を行います。</span><span class="sxs-lookup"><span data-stu-id="84204-196">Because cost price lists in many different currencies can be attached to project service parameters, PSA does a currency match between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="84204-197">経費については、コスト価格設定方法およびコストに対する利幅価格設定方法は原価価格表には適用されません。</span><span class="sxs-lookup"><span data-stu-id="84204-197">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="84204-198">これらの価格設定方法を原価価格表の行で使用してトランザクション カテゴリ コストを設定しても、システムはそれらを無視し、既定の原価価格は入力されません。</span><span class="sxs-lookup"><span data-stu-id="84204-198">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]