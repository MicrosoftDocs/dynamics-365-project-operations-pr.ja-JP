---
title: 製品ベースの見積依頼明細行
description: このトピックでは、製品ベースの見積依頼明細行について説明します。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151259"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="cfb41-103">製品ベースの見積依頼明細行</span><span class="sxs-lookup"><span data-stu-id="cfb41-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="cfb41-104">Dynamics 365 Project Service Automation で製品ベースの見積依頼明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="cfb41-105">製品ベースの見積依頼明細行は、「書き込み」行にすることも、製品カタログの品目にもできます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="cfb41-106">製品カタログ</span><span class="sxs-lookup"><span data-stu-id="cfb41-106">Product catalog</span></span>

<span data-ttu-id="cfb41-107">Dynamics 365 製品カタログの製品には、既定の出荷単位と出荷単位一覧があります。</span><span class="sxs-lookup"><span data-stu-id="cfb41-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="cfb41-108">複数の製品が同じ属性セットを共有している場合は、それらの属性を持つ製品ファミリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="cfb41-109">1 つの製品ファミリのすべての製品のは、同じ属性セットを継承します。</span><span class="sxs-lookup"><span data-stu-id="cfb41-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="cfb41-110">たとえば、企業はさまざまなソフトウェアのサブスクリプション ライセンスを販売します。</span><span class="sxs-lookup"><span data-stu-id="cfb41-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="cfb41-111">すべてのサブスクリプション ソフトウェアには、次の 2 つの属性があります:</span><span class="sxs-lookup"><span data-stu-id="cfb41-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="cfb41-112">ユーザー数</span><span class="sxs-lookup"><span data-stu-id="cfb41-112">Number of users</span></span> 
- <span data-ttu-id="cfb41-113">サブスクリプション期間 (月単位)</span><span class="sxs-lookup"><span data-stu-id="cfb41-113">Subscription duration (in months)</span></span>

<span data-ttu-id="cfb41-114">この種類のカタログを維持する良い方法は、 **サブスクリプション ソフトウェア** いう名前で、 **ユーザー数** および **サブスクリプション期間** を属性として持つ製品ファミリを作成することです。</span><span class="sxs-lookup"><span data-stu-id="cfb41-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="cfb41-115">その後、 **Dynamics 365 Sales** や **Dynamics 365 Field Service** などの個々の製品を **サブスクリプション ソフトウェア** 製品ファミリに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="cfb41-116">見積依頼明細行への製品カタログ品目の追加</span><span class="sxs-lookup"><span data-stu-id="cfb41-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="cfb41-117">プロジェクト見積、およびプロジェクト契約ページには、プロジェクトベース品目および製品ベース品目の 2 つの品目の種類のセクションがあります: 。</span><span class="sxs-lookup"><span data-stu-id="cfb41-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="cfb41-118">製品ベース品目には、Dynamics 365を使用して、製品カタログから品目を見積もりに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="cfb41-119">見積品目またはプロジェクト契約品目のドロップダウン リストには、見積またはプロジェクト契約に添付されている製品価格表のすべての製品および単位が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="cfb41-120">見積の製品価格表の一部ではない製品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="cfb41-121">また、別の価格表から製品を選択することも、製品カタログから製品を直接選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="cfb41-122">製品を製品カタログから直接選択すると、その製品の既定の価格表を使用して、製品の販売価格が取得されます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="cfb41-123">既定の価格表が設定されていない場合、価格は 0 (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="cfb41-124">見積品目が製品カタログに基づいている場合、見積依頼明細行で販売価格を直接上書きできます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="cfb41-125">Dynamics 365の見積依頼明細行に **価格設定** フィールドがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cfb41-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="cfb41-126">次の 2 つの値を使用できます:</span><span class="sxs-lookup"><span data-stu-id="cfb41-126">Two values are available:</span></span>

- <span data-ttu-id="cfb41-127">価格の上書き</span><span class="sxs-lookup"><span data-stu-id="cfb41-127">Override pricing</span></span>  
- <span data-ttu-id="cfb41-128">既定値を使用</span><span class="sxs-lookup"><span data-stu-id="cfb41-128">Use default</span></span>

<span data-ttu-id="cfb41-129">このフィールドを **価格の上書き** に設定すると、Dynamics 365では、既定の価格を設定しません。</span><span class="sxs-lookup"><span data-stu-id="cfb41-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="cfb41-130">見積依頼明細行に製品価格を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfb41-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="cfb41-131">このフィールドを **既定値を使用** に設定すると、Dynamics 365では既定の販売価格を使用し、フィールドを編集できないようにロックします。</span><span class="sxs-lookup"><span data-stu-id="cfb41-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="cfb41-132">PSAをインストールすると、既定の販売価格が見積の製品ベース行に入力されます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="cfb41-133">**価格設定** フィールドは **価格の上書き** に設定されているため、見積依頼明細行の既定価格を編集できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![価格の上書きの設定](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="cfb41-135">製品の数量係数</span><span class="sxs-lookup"><span data-stu-id="cfb41-135">Quantity factors for products</span></span>

<span data-ttu-id="cfb41-136">PSAは、数量係数を使用して、サブスクリプション ベースの製品の販売をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cfb41-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="cfb41-137">サブスクリプション ベース製品の場合、見積またはプロジェクト契約品目の数量はユーザー月数で表されます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="cfb41-138">通常は、サブスクリプション ソフトウェア の価格は、ユーザーごとの月額として、カタログに保存されます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="cfb41-139">ただし、代わりに別の時間の説明を使用できます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="cfb41-140">営業プロセスの間、見積依頼明細行の価格は通常、IT 販売代理店が交渉および割引した、ユーザーごと、月ごとの価格です。</span><span class="sxs-lookup"><span data-stu-id="cfb41-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="cfb41-141">各取引には、異なる数のユーザーと異なる数のサブスクリプション月があります。</span><span class="sxs-lookup"><span data-stu-id="cfb41-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="cfb41-142">見積依頼明細行の金額の計算に使用される数量は、ユーザーの数とサブスクリプション月数の積です。</span><span class="sxs-lookup"><span data-stu-id="cfb41-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="cfb41-143">この種類の営業をサポートするために、PSAは数量係数の概念を導入しました。</span><span class="sxs-lookup"><span data-stu-id="cfb41-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="cfb41-144">数量係数は、Dynamics 365の製品属性に依存します。</span><span class="sxs-lookup"><span data-stu-id="cfb41-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="cfb41-145">製品の特定のプロパティを設定すると、PSAでは、それらのプロパティのサブセットまたはすべてのプロパティに数量係数としてフラグを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="cfb41-146">PSAでは、数値データ型を持つ数値プロパティまたは製品プロパティのみが、数量係数としてフラグ付けされていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="cfb41-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="cfb41-147">数量係数が設定されている製品が見積依頼明細行に追加されると、見積依頼明細行の **数量** フィールドは、読み取り専用フィールドになります。</span><span class="sxs-lookup"><span data-stu-id="cfb41-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="cfb41-148">数量係数である製品プロパティの値を入力すると、PSAは、見積依頼明細行の数量を計します。</span><span class="sxs-lookup"><span data-stu-id="cfb41-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="cfb41-149">たとえば、Dynamics 365には、次のプロパティがあります:</span><span class="sxs-lookup"><span data-stu-id="cfb41-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="cfb41-150">**ユーザー数** - ユーザー数</span><span class="sxs-lookup"><span data-stu-id="cfb41-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="cfb41-151">**月数** - サブスクリプション月数</span><span class="sxs-lookup"><span data-stu-id="cfb41-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="cfb41-152">**製品 SKU**</span><span class="sxs-lookup"><span data-stu-id="cfb41-152">**Product SKU**</span></span> 

<span data-ttu-id="cfb41-153">製品品目のプロパティを編集することにより、 **ユーザー数** と **月数** プロパティに数量係数としてフラグを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="cfb41-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![ユーザー数と月数に品質係数としてフラグを付ける](media/basic-guide-11.png)
 
