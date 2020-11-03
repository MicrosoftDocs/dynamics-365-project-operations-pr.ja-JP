---
title: 製品カタログの価格
description: このトピックでは、 Dynamics 365 Project Service Automation で製品カタログの価格がどのように機能するかについて説明します (PSA)。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: e6d9266cfee996b68608c99f77d1b0c053985b3d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079299"
---
# <a name="product-catalog-pricing"></a><span data-ttu-id="9dcee-103">製品カタログの価格</span><span class="sxs-lookup"><span data-stu-id="9dcee-103">Product catalog pricing</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="9dcee-104">価格表および価格表品目エンティティは、製品カタログの価格をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9dcee-104">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="9dcee-105">ほとんどの場合、この機能は、プロジェクト見積およびプロジェクト契約のカタログ ベースの明細行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-105">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="9dcee-106">プロジェクト ベースの明細行の場合、契約は受注後の取引を表します。</span><span class="sxs-lookup"><span data-stu-id="9dcee-106">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="9dcee-107">通常、交渉のプロセスが受注に先行するため、見積もりに添付された価格は常にそのまま新しい価格表にコピーされ、契約に添付されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-107">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="9dcee-108">この新しい価格表は、契約の範囲外では変更できません。</span><span class="sxs-lookup"><span data-stu-id="9dcee-108">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="9dcee-109">この制限は、マスター価格表で発生する価格変更から、交渉され価格カードを保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-109">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="9dcee-110">製品は、製品カタログの既定コストおよび価格表が含まれるように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dcee-110">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="9dcee-111">既定のコストおよびリスト価格を設定するには、リスト価格、標準コスト、および現在のコストを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dcee-111">You must use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="9dcee-112">既定のリスト価格は、システムが見積またはプロジェクト契約の製品価格表でその製品の価格表品目を見つけられない場合にのみ、見積依頼明細行またはプロジェクト契約品目で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-112">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="9dcee-113">製品カタログ品目の原価価格は、見積間で変更できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-113">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="9dcee-114">コストを正確に追跡しないと、プロジェクト エンゲージメントで運用上の利益を特定できないため、この機能は重要です。</span><span class="sxs-lookup"><span data-stu-id="9dcee-114">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="9dcee-115">既定では、製品の標準コストが原価価格として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-115">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="9dcee-116">ただし、見積に異なる原価価格がある場合は、既定の原価価格を見積依頼明細行で更新できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-116">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="9dcee-117">価格表品目</span><span class="sxs-lookup"><span data-stu-id="9dcee-117">Price list items</span></span>

<span data-ttu-id="9dcee-118">製品カタログの製品をさまざまな価格表に追加できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-118">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="9dcee-119">製品の価格表明細行は、常に特定の単位を参照します。</span><span class="sxs-lookup"><span data-stu-id="9dcee-119">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="9dcee-120">価格表品目の製品の価格設定は、金額として構成できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-120">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="9dcee-121">または、リスト価格、現在のコスト、または標準コストとして構成できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-121">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="9dcee-122">PSAは、価格が、リスト定価、標準コスト、または現在のコストとして構成されている場合、さまざま丸めオプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9dcee-122">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="9dcee-123">複数の価格設定方法と丸めオプションを使用することに加えて、価格表品目に値引き表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-123">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

> ![カタログの製品をさまざまな価格表に追加する](media/basic-guide-16.png)

<span data-ttu-id="9dcee-125">**プロジェクト見積もり** ページで **カスタム価格の作成** を選択して、見積の新しいカスタム価格表を作成すると、PSAは価格表のコピーを作成し、新しい価格表のヘッダーの **エンティティ** フィールドは **営業エンティティ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, PSA makes a copy of the price list, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="9dcee-126">新しい価格表の名前には、見積名とタイムスタンプが追加されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="9dcee-127">カスタム ワークフローで新しい価格表の名前と見積の名前を使用して、カスタム価格を使用する見積の追加レビューと承認をトリガーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="9dcee-128">既定の製品価格表</span><span class="sxs-lookup"><span data-stu-id="9dcee-128">Default product price list</span></span>
<span data-ttu-id="9dcee-129">各顧客レコードには、 **既定の価格表** フィールドがあり、顧客の通貨に一致する価格表を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="9dcee-130">PSAでは、このフィールドに既定値は、自動的に入力されません。</span><span class="sxs-lookup"><span data-stu-id="9dcee-130">In PSA, a default value isn't automatically entered in this field.</span></span> <span data-ttu-id="9dcee-131">特定の顧客に対してカスタム価格契約が存在する場合、このフィールドを使用して、その顧客に価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="9dcee-132">営業案件、見積もり、およびプロジェクト契約のエンティティでは、次の受注を使用して、既定の製品価格表が入力されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="9dcee-133">プロジェクト価格表にも同じ受注が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="9dcee-134">見積もり</span><span class="sxs-lookup"><span data-stu-id="9dcee-134">Quote</span></span>
2.  <span data-ttu-id="9dcee-135">営業案件</span><span class="sxs-lookup"><span data-stu-id="9dcee-135">Opportunity</span></span>
3.  <span data-ttu-id="9dcee-136">Customer</span><span class="sxs-lookup"><span data-stu-id="9dcee-136">Customer</span></span>
4.  <span data-ttu-id="9dcee-137">PSA 用のグローバル設定</span><span class="sxs-lookup"><span data-stu-id="9dcee-137">Global settings for PSA</span></span>

<span data-ttu-id="9dcee-138">既定では、見積依頼明細行の **製品** フィールドには、見積の製品価格表内のすべてのアクティブな製品がリストされます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="9dcee-139">製品が非アクティブ化されている場合、またはドラフト製品の場合は、価格表に含まれていてもリストされません。</span><span class="sxs-lookup"><span data-stu-id="9dcee-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="9dcee-140">製品カタログ品目には、プロジェクト契約で作成された最初の請求書に請求明細行として追加されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="9dcee-141">下書き請求書では、それらの請求明細行を削除できます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="9dcee-142">その場合は、明細行は請求書が発行されるまで、または請求書が顧客に送信されるまで、それ以降の請求書に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="9dcee-143">PSAでは、製品の請求明細行の部分的な数量を請求することはできません。</span><span class="sxs-lookup"><span data-stu-id="9dcee-143">In PSA, you can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="9dcee-144">プロジェクト契約の製品明細行が請求されると、実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="9dcee-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="9dcee-145">ただし、それらの実績は関連するプロジェクト エンティティにリンクされていません。</span><span class="sxs-lookup"><span data-stu-id="9dcee-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="9dcee-146">つまり、製品ベースのプロジェクト契約品目は、プロジェクト ベースの使用から独立しています。</span><span class="sxs-lookup"><span data-stu-id="9dcee-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="9dcee-147">PSAは、プロジェクトの物的消費を追跡しません。</span><span class="sxs-lookup"><span data-stu-id="9dcee-147">PSA doesn't track material consumption on projects.</span></span>
