---
title: 製品ベースの見積依頼明細行の概要 - Lite
description: このトピックでは、製品ベースの見積依頼明細行の使用方法について説明します。
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178194"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="ba15f-103">製品ベースの見積依頼明細行の概要 - Lite</span><span class="sxs-lookup"><span data-stu-id="ba15f-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="ba15f-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="ba15f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba15f-105">Dynamics 365 Project Operations で製品ベースの見積依頼明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="ba15f-106">製品ベースの見積依頼明細行は、手動で追加することも、製品カタログの品目にもできます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="ba15f-107">製品カタログ</span><span class="sxs-lookup"><span data-stu-id="ba15f-107">Product catalog</span></span>

<span data-ttu-id="ba15f-108">製品カタログの各製品には、既定の出荷単位と出荷単位一覧があります。</span><span class="sxs-lookup"><span data-stu-id="ba15f-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="ba15f-109">複数の製品が同じ属性セットを共有している場合は、それらの属性を共有する製品ファミリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="ba15f-110">たとえば、企業はさまざまな種類のソフトウェアのサブスクリプション ライセンスを販売します。</span><span class="sxs-lookup"><span data-stu-id="ba15f-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="ba15f-111">すべてのサブスクリプション ソフトウェアには、次の 2 つの属性があります:</span><span class="sxs-lookup"><span data-stu-id="ba15f-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="ba15f-112">ユーザー数</span><span class="sxs-lookup"><span data-stu-id="ba15f-112">Number of users</span></span>
- <span data-ttu-id="ba15f-113">月単位のサブスクリプション期間</span><span class="sxs-lookup"><span data-stu-id="ba15f-113">A subscription duration measured in months</span></span>

<span data-ttu-id="ba15f-114">この種類のカタログを維持するには、**サブスクリプション ソフトウェア** いう名前の製品ファミリを作成し、ユーザー数とサブスクリプション期間を属性として追加します。</span><span class="sxs-lookup"><span data-stu-id="ba15f-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="ba15f-115">次に、**サブスクリプション ソフトウェア** 製品ファミリに個々の製品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="ba15f-116">プロジェクト見積もりへの製品カタログ品目の追加</span><span class="sxs-lookup"><span data-stu-id="ba15f-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="ba15f-117">**プロジェクト見積もり** および **プロジェクト契約** ページには、プロジェクト ベース品目および製品ベース品目のセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="ba15f-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="ba15f-118">製品ベース品目の場合、見積依頼明細行またはプロジェクト契約品目のドロップダウン リストには、製品価格表のすべての製品および単位が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="ba15f-119">製品価格表の一部ではない製品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="ba15f-120">また、別の価格表から、または直接製品カタログから、製品を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="ba15f-121">製品を製品カタログから直接選択すると、その製品の既定の価格表を使用して、製品の販売価格が取得されます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="ba15f-122">既定の価格表が設定されていない場合、価格はゼロ (0) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="ba15f-123">見積依頼明細行が製品カタログに基づいている場合は、見積依頼明細行で販売価格を直接上書きできます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="ba15f-124">2 つの使用可能な値を持つ **価格設定** フィールドの見積依頼明細行:</span><span class="sxs-lookup"><span data-stu-id="ba15f-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="ba15f-125">**価格の上書き**</span><span class="sxs-lookup"><span data-stu-id="ba15f-125">**Override Pricing**</span></span>
- <span data-ttu-id="ba15f-126">**既定値を使用する**</span><span class="sxs-lookup"><span data-stu-id="ba15f-126">**Use Default**</span></span>

<span data-ttu-id="ba15f-127">**価格の上書き** を選択すると、既定価格は設定されません。</span><span class="sxs-lookup"><span data-stu-id="ba15f-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="ba15f-128">代わりに、見積依頼明細行に製品価格を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba15f-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="ba15f-129">**既定値を使用** を選択すると、既定の販売価格が使用され、フィールドは編集用にロックされます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="ba15f-130">既定の販売価格が見積の製品ベース品目に入力されます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="ba15f-131">**価格設定** フィールドは **価格の上書き** に設定されているため、見積依頼明細行の既定価格を編集できます。</span><span class="sxs-lookup"><span data-stu-id="ba15f-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="ba15f-132">これは、Dynamics 365 Sales の製品ベース品目の動作に対する Project Operations 固有の上書きです。</span><span class="sxs-lookup"><span data-stu-id="ba15f-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
