---
title: 製品ベースの見積依頼明細行に対してユーザーごと、月ごとなどの複雑な出荷単位を管理する (ライト)
description: このトピックは、製品ベースの見積依頼明細行の複雑な出荷単位の管理について説明します。
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175582"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="cc3ea-103">製品ベースの見積依頼明細行に対してユーザーごと、月ごとなどの複雑な出荷単位を管理する (ライト)</span><span class="sxs-lookup"><span data-stu-id="cc3ea-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="cc3ea-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="cc3ea-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc3ea-105">Dynamics 365 Project Operations は、数量係数を使用して、サブスクリプション ベースの製品の販売をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="cc3ea-106">サブスクリプション ベース製品の場合、見積もりまたはプロジェクト契約品目の数量はユーザー月数で表されます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="cc3ea-107">通常は、サブスクリプション ソフトウェア の価格は、ユーザーごとの月額として、カタログに保存されます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="cc3ea-108">営業プロセスの間、見積依頼明細行の価格は通常、IT 販売代理店が交渉および割引した、ユーザーごと、月ごとの価格です。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="cc3ea-109">各取引には、異なる数のユーザーと異なる数のサブスクリプション月があります。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="cc3ea-110">見積依頼明細行の計算に使用される数量は、ユーザーの数とサブスクリプション月数の積です。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="cc3ea-111">この種類の営業をサポートするために、Project Operations は数量係数の概念を導入しました。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="cc3ea-112">数量係数は、Dynamics 365の製品属性に依存します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="cc3ea-113">製品の特定のプロパティを設定すると、Project Operations では、サブセットまたはすべてのプロパティに数量係数としてフラグを立てることができます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="cc3ea-114">数値データ型を持つ数値プロパティ、または製品プロパティのみが、数量係数としてフラグが立てられていることが Project Operations によって検証されます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="cc3ea-115">数量係数のある製品を見積依頼明細行に追加すると、**数量** フィールドは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="cc3ea-116">数量係数である製品プロパティの値を入力すると、Project Operations は見積依頼明細行の数量を計算します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="cc3ea-117">たとえば、Dynamics 365 Sales には、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="cc3ea-118">**ユーザー数** : ユーザー数</span><span class="sxs-lookup"><span data-stu-id="cc3ea-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="cc3ea-119">**月数** : サブスクリプションの月数</span><span class="sxs-lookup"><span data-stu-id="cc3ea-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="cc3ea-120">**製品 SKU**</span><span class="sxs-lookup"><span data-stu-id="cc3ea-120">**Product SKU**</span></span>

<span data-ttu-id="cc3ea-121">製品品目のプロパティを編集することにより、**ユーザー数** と **月数** プロパティに数量係数としてフラグを立てることができます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="cc3ea-122">製品プロパティから数量係数を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="cc3ea-123">Project Operations の左側のナビゲーション ウィンドウで、**営業** > **製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="cc3ea-124">数量係数を構成する必要がある製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="cc3ea-125">製品にプロパティがすでに構成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="cc3ea-126">製品の **プロジェクト情報** ページで、**数量係数** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="cc3ea-127">サブグリッドで、**+ 新しいフィールド計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="cc3ea-128">数量係数の名前を入力し、フィールド計算にマップするプロパティ値を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="cc3ea-129">フォームを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-129">Save and close the form.</span></span> <span data-ttu-id="cc3ea-130">製品ベースの見積依頼明細行の数量を計算するために使用するすべてのプロパティについて、これらの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="cc3ea-131">製品の製品ベースの見積依頼明細行を作成すると、見積依頼明細行の数量がロックされます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="cc3ea-132">数量は、その見積依頼明細行に入力したプロパティ値の積として計算されます。</span><span class="sxs-lookup"><span data-stu-id="cc3ea-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
