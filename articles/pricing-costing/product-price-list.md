---
title: 製品価格表
description: このトピックでは、プロジェクトの見積もりと契約に使用するカタログ価格の価格リストについて説明します。
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877496"
---
# <a name="product-price-lists"></a><span data-ttu-id="6d481-103">製品価格表</span><span class="sxs-lookup"><span data-stu-id="6d481-103">Product price lists</span></span>

<span data-ttu-id="6d481-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="6d481-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="6d481-105">Project Operations では、**製品価格表** および関連する価格表品目エンティティは、製品ベースの見積もりおよび契約品目で製品の価格を設定する機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6d481-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="6d481-106">プロジェクトで使用される製品の場合、プロジェクト価格表の価格表品目レコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="6d481-107">製品は、製品カタログの既定コストおよび価格表が含まれるように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d481-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="6d481-108">既定のコストおよびリスト価格を設定するには、リスト価格、標準コスト、および現在のコストを使用してください。</span><span class="sxs-lookup"><span data-stu-id="6d481-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="6d481-109">既定のリスト価格は、システムが見積またはプロジェクト契約の製品価格表でその製品の価格表品目を見つけられない場合にのみ、見積依頼明細行またはプロジェクト契約品目で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="6d481-110">製品カタログ品目の原価価格は、見積間で変更できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="6d481-111">コストを正確に追跡しないと、プロジェクト エンゲージメントで運用上の利益を特定できないため、この機能は重要です。</span><span class="sxs-lookup"><span data-stu-id="6d481-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="6d481-112">既定では、製品の標準コストが原価価格として使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="6d481-113">ただし、見積に異なる原価価格がある場合は、既定の原価価格を見積依頼明細行で更新できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="6d481-114">価格表品目</span><span class="sxs-lookup"><span data-stu-id="6d481-114">Price list items</span></span>

<span data-ttu-id="6d481-115">製品カタログの製品をさまざまな価格表に追加できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="6d481-116">製品の価格表明細行は、常に特定の単位を参照します。</span><span class="sxs-lookup"><span data-stu-id="6d481-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="6d481-117">価格表品目の製品の価格設定は、金額として構成できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="6d481-118">または、リスト価格、現在のコスト、または標準コストとして構成できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="6d481-119">価格設定機能は、製品価格が、リスト定価、標準コスト、または現在のコストとして構成されている場合、さまざま丸めオプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6d481-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="6d481-120">複数の価格設定方法と丸めオプションを使用することに加えて、価格表品目に値引き表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6d481-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="6d481-121">既定の製品価格表</span><span class="sxs-lookup"><span data-stu-id="6d481-121">Default product price list</span></span>
<span data-ttu-id="6d481-122">各顧客レコードには、 **既定の価格表** フィールドがあり、顧客の通貨に一致する価格表を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="6d481-123">このフィールドに既定値は自動入力されません。</span><span class="sxs-lookup"><span data-stu-id="6d481-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="6d481-124">特定の顧客に対してカスタム価格契約が存在する場合、このフィールドを使用して、その顧客に価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6d481-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="6d481-125">営業案件、見積もり、およびプロジェクト契約のエンティティでは、次の受注を使用して、既定の製品価格表が入力されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="6d481-126">プロジェクト価格表にも同じ受注が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="6d481-127">見積もり </span><span class="sxs-lookup"><span data-stu-id="6d481-127">Quote</span></span>
2.  <span data-ttu-id="6d481-128">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="6d481-128">Opportunity</span></span>
3.  <span data-ttu-id="6d481-129">顧客</span><span class="sxs-lookup"><span data-stu-id="6d481-129">Customer</span></span>
4.  <span data-ttu-id="6d481-130">グローバル設定</span><span class="sxs-lookup"><span data-stu-id="6d481-130">Global settings</span></span> 

<span data-ttu-id="6d481-131">既定では、見積依頼明細行の **製品** フィールドには、見積の製品価格表内のすべてのアクティブな製品がリストされます。</span><span class="sxs-lookup"><span data-stu-id="6d481-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="6d481-132">製品が非アクティブ化されている場合、またはドラフト製品の場合は、価格表に含まれていてもリストされません。</span><span class="sxs-lookup"><span data-stu-id="6d481-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="6d481-133">製品カタログ品目には、プロジェクト契約で作成された最初の請求書に請求明細行として追加されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="6d481-134">下書き請求書では、それらの請求明細行を削除できます。</span><span class="sxs-lookup"><span data-stu-id="6d481-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="6d481-135">その場合は、明細行は請求書が発行されるまで、または請求書が顧客に送信されるまで、それ以降の請求書に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="6d481-136">製品の請求明細行の部分的な数量を請求することはできません。</span><span class="sxs-lookup"><span data-stu-id="6d481-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="6d481-137">プロジェクト契約の製品明細行が請求されると、実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6d481-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="6d481-138">ただし、それらの実績は関連するプロジェクト エンティティにリンクされていません。</span><span class="sxs-lookup"><span data-stu-id="6d481-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="6d481-139">つまり、製品ベースのプロジェクト契約品目は、プロジェクト ベースの使用から独立しています。</span><span class="sxs-lookup"><span data-stu-id="6d481-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
