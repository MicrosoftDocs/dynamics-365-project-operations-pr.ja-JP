---
title: 製品ベースの契約品目の概要 - Lite
description: このトピックでは、製品ベースの契約品目について説明します。
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369742"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="e7a5e-103">製品ベースの契約品目の概要 - Lite</span><span class="sxs-lookup"><span data-stu-id="e7a5e-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="e7a5e-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="e7a5e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7a5e-105">Dynamics 365 Project Operations で製品ベースの契約品目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="e7a5e-106">製品ベースの契約品目は、品目を手動で作成することも、製品カタログの品目にもできます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="e7a5e-107">製品カタログ</span><span class="sxs-lookup"><span data-stu-id="e7a5e-107">Product catalog</span></span>

<span data-ttu-id="e7a5e-108">製品カタログの製品には、既定の出荷単位と出荷単位一覧があります。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="e7a5e-109">複数の製品が同じ属性セットを共有している場合は、それらの属性を持つ製品ファミリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="e7a5e-110">1 つの製品ファミリのすべての製品のは、同じ属性セットを継承します。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="e7a5e-111">たとえば、企業はさまざまな種類のソフトウェアのサブスクリプション ライセンスを販売します。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="e7a5e-112">すべてのサブスクリプション ソフトウェアには、次の 2 つの属性があります:</span><span class="sxs-lookup"><span data-stu-id="e7a5e-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="e7a5e-113">ユーザー数</span><span class="sxs-lookup"><span data-stu-id="e7a5e-113">Number of users</span></span>
- <span data-ttu-id="e7a5e-114">サブスクリプション期間 (月単位)</span><span class="sxs-lookup"><span data-stu-id="e7a5e-114">Subscription duration (in months)</span></span>

<span data-ttu-id="e7a5e-115">このタイプのカタログを維持するには、**サブスクリプション ソフトウェア** という名前の製品ファミリを作成します。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="e7a5e-116">製品ファミリに属性 **ユーザー数** と **サブスクリプション期間** を追加します。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="e7a5e-117">次に、個々の製品を **サブスクリプション ソフトウェア** 製品ファミリに追加します。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="e7a5e-118">プロジェクト契約への製品カタログ品目の追加</span><span class="sxs-lookup"><span data-stu-id="e7a5e-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="e7a5e-119">プロジェクト契約には、プロジェクトベースと製品ベースの 2 種類の品目のセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="e7a5e-120">製品ベースの品目には、契約の製品価格表にあるすべての製品とユニットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="e7a5e-121">契約の製品価格表に含まれていない製品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="e7a5e-122">他の価格表から、または製品カタログから直接製品を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="e7a5e-123">製品を製品カタログから直接選択すると、その製品の既定の価格表が製品の販売価格に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="e7a5e-124">既定の価格表が設定されていない場合、価格は 0 (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="e7a5e-125">契約品目が製品カタログに基づいている場合、品目で販売価格を直接上書きできます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="e7a5e-126">契約品目には 2 つの値を持つ **価格** があります:</span><span class="sxs-lookup"><span data-stu-id="e7a5e-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="e7a5e-127">**価格の上書き**</span><span class="sxs-lookup"><span data-stu-id="e7a5e-127">**Override pricing**</span></span>
- <span data-ttu-id="e7a5e-128">**既定値を使用**</span><span class="sxs-lookup"><span data-stu-id="e7a5e-128">**Use default**</span></span>

<span data-ttu-id="e7a5e-129">**価格** フィールドを **価格の上書き** に設定すると、既定の価格は設定されません。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="e7a5e-130">契約品目に製品の価格を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="e7a5e-131">フィールドを **既定値を使用** に設定すると、既定の販売価格が使用され、フィールドは編集できません。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="e7a5e-132">Project Operations をインストールすると、既定の販売価格が契約の製品ベース品目に入力されます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="e7a5e-133">**価格** フィールドは **価格の上書き** に設定されているため、契約品目の既定価格を編集できます。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="e7a5e-134">これは、Dynamics 365 Sales の製品ベース品目の動作に対する Project Operations 固有の上書きです。</span><span class="sxs-lookup"><span data-stu-id="e7a5e-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]