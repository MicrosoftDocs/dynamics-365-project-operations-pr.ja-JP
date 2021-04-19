---
title: プロジェクトのリソース時間の財務見積もり
description: このトピックは、時間の財務見積もりがどのように計算されるかについての情報を提供します。
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91156c5cf79af8c66c12b84a6d2b17aa7fe09ed1
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701832"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a><span data-ttu-id="1f568-103">プロジェクトのリソース時間の財務見積もり</span><span class="sxs-lookup"><span data-stu-id="1f568-103">Financial estimates for resource time on projects</span></span>

<span data-ttu-id="1f568-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1f568-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f568-105">時間の財務見積もりは、次の 3 つの要因に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-105">Financial estimates for time are calculated based on three factors:</span></span> 

- <span data-ttu-id="1f568-106">プロジェクト計画の各リーフ ノード タスクに割り当てられた一般的なチーム メンバーまたは名前の付いた各チーム メンバーのタイプ。</span><span class="sxs-lookup"><span data-stu-id="1f568-106">The type of generic or named team member assigned to each leaf node task on the project plan.</span></span> 
- <span data-ttu-id="1f568-107">仕事の種類または複雑さ。</span><span class="sxs-lookup"><span data-stu-id="1f568-107">The type or complexity of work.</span></span>
- <span data-ttu-id="1f568-108">タスクへのリソースの割り当てのための工数の広がり。</span><span class="sxs-lookup"><span data-stu-id="1f568-108">The spread of effort for the resource's assignment on the task.</span></span> 

<span data-ttu-id="1f568-109">最初の 2 つの要因は、リソースの割り当ての単価または請求レートに影響します。</span><span class="sxs-lookup"><span data-stu-id="1f568-109">The first two factors influence the unit cost or bill rate of a resource's assignment.</span></span> <span data-ttu-id="1f568-110">リソース割り当ての単価または請求レートは、割り当てられたリソースの属性によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-110">The unit cost or bill rate of a resource assignment is determined by the attributes of the resource assigned.</span></span> <span data-ttu-id="1f568-111">これらの属性には、リソースが属する組織単位とリソースの標準的な役割が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1f568-111">These attributes include the organizational unit to which the resource belongs and the standard role of the resource.</span></span> <span data-ttu-id="1f568-112">また、標準のタイトルや経験レベルなど、リソースのビジネスに関連するカスタム属性を追加して、割り当ての単価や請求レートに影響を及ぼすこともできます。</span><span class="sxs-lookup"><span data-stu-id="1f568-112">You can also add custom attributes relevant to your business for the resource, like standard title or experience level, and have them influence the unit cost or bill rate of the assignment.</span></span>
<span data-ttu-id="1f568-113">リソースの属性に加えて、タスクなど作業の属性も、割り当ての単位請求レートまたはコスト率に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1f568-113">In addition to the attributes of the resource, attributes of work, such as the task, can also influence the unit bill rate or cost rate of the assignment.</span></span> <span data-ttu-id="1f568-114">たとえば、特定のタスクがより複雑な場合、それらの特定のタスクへのリソースの割り当ては、それほど複雑でないタスクよりも高い単位原価または請求率をもたらします。</span><span class="sxs-lookup"><span data-stu-id="1f568-114">For example, when certain tasks are more complex, the resource's assignment to those specific tasks result in a higher unit cost or bill rate than tasks that are less complex.</span></span>   

<span data-ttu-id="1f568-115">3 番目の要素は、そのレートでの時間数を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f568-115">The third factor provides the quantity of hours at that rate.</span></span> <span data-ttu-id="1f568-116">タスクが 2 つの価格期間をカバーしている場合、そのタスクのリソース割り当ての最初の部分のコストと価格は、タスクの 2 番目の部分とは異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1f568-116">In cases where a task covers two price periods, it is likely that the first part of the resource assignment for that task is costed and priced differently than the second portion of the task.</span></span> <span data-ttu-id="1f568-117">各リソース割り当ての工数の見積もりは、1 日あたりの工数の毎日の分布とともに保存される複雑な値です。</span><span class="sxs-lookup"><span data-stu-id="1f568-117">The effort estimate on each resource assignment is a complex value stored with the daily distribution of effort per day.</span></span>

<span data-ttu-id="1f568-118">作業とリソースのカスタム属性を価格設定と原価計算のディメンションとして設定する方法の詳細については、[価格ディメンションの概要](../pricing-costing/pricing-dimensions-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f568-118">For detailed instructions about how to set up custom attributes of work and resources as pricing and costing dimensions, see [Pricing Dimensions overview](../pricing-costing/pricing-dimensions-overview.md).</span></span>

<span data-ttu-id="1f568-119">各リソース割り当ての財務見積もりは、**割り当てのレート/時間に時間数を掛けて** 計算されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-119">The financial estimate on each resource assignment is calculated as **rate/hr for the assignment multiplied by the number of hours.**</span></span>  <span data-ttu-id="1f568-120">工数の見積もりと同様に、各リソース割り当てのコストと収益の財務見積もりは、1 日あたりの金額の日次分布とともに保存される複雑な値です。</span><span class="sxs-lookup"><span data-stu-id="1f568-120">Similar to the effort estimate, the financial estimate for cost and revenue for each resource assignment is a complex value stored with the daily distribution of monetary amount per day.</span></span> 

## <a name="summarizing-financial-estimates-for-time"></a><span data-ttu-id="1f568-121">時間の財務見積もりの集計</span><span class="sxs-lookup"><span data-stu-id="1f568-121">Summarizing financial estimates for time</span></span>
<span data-ttu-id="1f568-122">リーフ ノード タスクの時間の財務見積もりは、そのタスクのすべてのリソース割り当ての財務見積もりの合計です。</span><span class="sxs-lookup"><span data-stu-id="1f568-122">A financial estimate for time on a leaf node task is the sum of the financial estimates on all resource assignments for that task.</span></span>

<span data-ttu-id="1f568-123">サマリーまたは親タスクの時間の財務見積もりは、そのすべての子タスクの財務見積もりの合計です。</span><span class="sxs-lookup"><span data-stu-id="1f568-123">A financial estimate for time on a summary or parent task is the sum of the financial estimates on all of its child tasks.</span></span> <span data-ttu-id="1f568-124">これは、プロジェクトの見積もり労務コストです。</span><span class="sxs-lookup"><span data-stu-id="1f568-124">This is the estimated labor cost on the project.</span></span> 

![リソースの見積もり](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="1f568-126">既定の原価価格と原価通貨</span><span class="sxs-lookup"><span data-stu-id="1f568-126">Default cost price and cost currency</span></span>

<span data-ttu-id="1f568-127">既定の原価は、プロジェクトの契約単位に添付されている価格表から取得されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-127">The default cost price comes from the price lists attached to the contracting unit of the project.</span></span> <span data-ttu-id="1f568-128">プロジェクトの原価通貨は、常にプロジェクトの契約単位の通貨です。</span><span class="sxs-lookup"><span data-stu-id="1f568-128">The cost currency of a project is always the currency of the contracting unit of the project.</span></span> <span data-ttu-id="1f568-129">リソース割り当てでは、コストの財務見積もりはプロジェクトのコスト通貨で保存されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-129">On a resource assignment, the financial estimate for cost is stored in the cost currency of the project.</span></span> <span data-ttu-id="1f568-130">価格表で原価率が設定されている通貨は、プロジェクトの原価通貨と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1f568-130">Sometimes, the currency in which the cost rate is set up in the price list is different from the project's cost currency.</span></span> <span data-ttu-id="1f568-131">このような場合、アプリケーションは、原価が設定されている通貨をプロジェクトの通貨に変換します。</span><span class="sxs-lookup"><span data-stu-id="1f568-131">In these cases, the application converts the currency in which the cost price is set up for the currency of the project.</span></span> <span data-ttu-id="1f568-132">**見積り** グリッドでは、すべてのコスト見積もりが表示され、プロジェクトのコスト通貨で集計されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-132">On the **Estimates** grid, all cost estimates are displayed and summarized in the project's cost currency.</span></span> 

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="1f568-133">既定の請求レートと販売通貨</span><span class="sxs-lookup"><span data-stu-id="1f568-133">Default bill rate and sales currency</span></span>

<span data-ttu-id="1f568-134">既定の販売価格は、トランザクションが成立した場合は関連するプロジェクト契約に添付されたプロジェクト価格表から、トランザクションがまだ販売前の段階にある場合は関連するプロジェクトの見積もりから取得されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-134">The default sales price comes from the project price lists attached to the related project contract if the deal is won, or from the related project quote if the deal is still in the pre-sales stage.</span></span> <span data-ttu-id="1f568-135">プロジェクトの販売通貨は、常にプロジェクトの見積もりまたはプロジェクト契約の通貨です。</span><span class="sxs-lookup"><span data-stu-id="1f568-135">The sales currency of the project is always the currency of the project quote or the project contract.</span></span> <span data-ttu-id="1f568-136">リソース割り当てでは、売上の財務見積もりはプロジェクトの販売通貨で保存されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-136">On a resource assignment, the financial estimate for sales is stored in the sales currency of the project.</span></span> <span data-ttu-id="1f568-137">コストとは異なり、価格表に設定されている販売価格が’プロジェクトの販売通貨と異なることはありません。</span><span class="sxs-lookup"><span data-stu-id="1f568-137">Unlike cost, the sales price that is set up in the price list can never be different from the project's sales currency.</span></span> <span data-ttu-id="1f568-138">通貨換算が必要なシナリオはありません。</span><span class="sxs-lookup"><span data-stu-id="1f568-138">There is no scenario where currency conversion is needed.</span></span> <span data-ttu-id="1f568-139">**見積り** グリッドでは、すべての売上見積もりが表示され、プロジェクトの販売通貨で集計されます。</span><span class="sxs-lookup"><span data-stu-id="1f568-139">On the **Estimates** grid, all sales estimates are displayed and summarized in the project's sales currency.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
