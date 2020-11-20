---
title: 製品ベースの契約品目の複雑な出荷単位の管理 (ライト)
description: このトピックは、サブスクリプション ベースの製品の販売のサポートに関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177382"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="9c0c9-103">製品ベースの契約品目の複雑な出荷単位の管理 (ライト)</span><span class="sxs-lookup"><span data-stu-id="9c0c9-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="9c0c9-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="9c0c9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c0c9-105">Dynamics 365 Project Operations は、数量係数を使用して、サブスクリプション ベースの製品の販売をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="9c0c9-106">サブスクリプション ベース製品の場合、契約またはプロジェクト契約品目の数量はユーザーの月数で表されます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="9c0c9-107">サブスクリプション ソフトウェアの価格は、ユーザーごとの価格、月ごとの価格としてカタログに格納されています。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="9c0c9-108">営業プロセスの間、契約依頼明細行の価格は通常、販売代理店が交渉および割引した、ユーザーごと、月ごとの価格です。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="9c0c9-109">各取引には、異なる数のユーザーと異なる数のサブスクリプション月があります。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="9c0c9-110">契約品目の金額を計算する際に使用する数量は、利用者数と契約月数の積となります。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="9c0c9-111">このような営業をサポートするために、Project Operations では *数量係数* の概念に対応しています。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="9c0c9-112">数量係数は、製品の属性に依存します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="9c0c9-113">製品の特定のプロパティを設定すると、それらのプロパティのサブセット、またはすべてのプロパティに数量係数としてフラグを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="9c0c9-114">数値データ型を持つ数値プロパティ、または製品プロパティのみが、数量係数としてフラグが立てられていることが Project Operations によって検証されます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="9c0c9-115">数量係数が設定されている商品が契約品目に追加されると、**数量** フィールドは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="9c0c9-116">数量係数である製品プロパティの値を入力すると、Project Operationsは、契約品目の数量を計算します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="9c0c9-117">たとえば、Dynamics 365 Sales には、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="9c0c9-118">**ユーザー数** : ユーザーの数です。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="9c0c9-119">**月数** : サブスクリプションの月数です。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="9c0c9-120">**製品 SKU** : 製品の最小管理単位 (SKU) です。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="9c0c9-121">製品品目のプロパティを編集することにより、 **ユーザー数** と **月数** プロパティに数量係数としてフラグを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="9c0c9-122">製品プロパティから数量係数を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="9c0c9-123">**Project Operations** で、**販売-製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="9c0c9-124">数量係数の設定が必要な製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="9c0c9-125">製品にプロパティがすでに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="9c0c9-126">**プロジェクト情報** ページで、**数量係数** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="9c0c9-127">サブグリッドで、**+ 新しいフィールド計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="9c0c9-128">**数量係数** の名前を入力し、フィールド計算にマッピングするプロパティの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="9c0c9-129">フォームを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-129">Save and close the form.</span></span>
7. <span data-ttu-id="9c0c9-130">製品ベースの契約品目の数量を構成するすべてのプロパティに対して、手順 2 から 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="9c0c9-131">数量係数が設定されている場合、ユーザーがこの製品の契約品目を作成すると、契約品目の数量がロックされます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="9c0c9-132">数量は、その契約品目のプロパティ値の積として計算されます。</span><span class="sxs-lookup"><span data-stu-id="9c0c9-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
