---
title: プロジェクトの発注書
description: この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。 使用する方法は、発注書の目的、および購入したアイテムがいつ消費されてプロジェクトに請求されるかによって異なります。
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079256"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="9711b-104">プロジェクトの発注書</span><span class="sxs-lookup"><span data-stu-id="9711b-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9711b-105">この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9711b-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="9711b-106">使用する方法は、発注書の目的、および購入したアイテムがいつ消費されてプロジェクトに請求されるかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9711b-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="9711b-107">発注書の作成方法</span><span class="sxs-lookup"><span data-stu-id="9711b-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="9711b-108">次のいずれかの方法を使用してプロジェクト管理と会計で発注書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="9711b-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="9711b-109">発注書の目的は、発注書がいつ消費され、アイテムがいつプロジェクトに請求されるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9711b-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9711b-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="9711b-110">Method</span></span></th>
<th><span data-ttu-id="9711b-111">目的</span><span class="sxs-lookup"><span data-stu-id="9711b-111">Purpose</span></span></th>
<th><span data-ttu-id="9711b-112">品目の消費</span><span class="sxs-lookup"><span data-stu-id="9711b-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9711b-113">プロジェクトから直接発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9711b-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="9711b-114">このメソッドを使用して、プロジェクトで消費するために外部仕入先からアイテムを購入します。</span><span class="sxs-lookup"><span data-stu-id="9711b-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="9711b-115">発注書は 2 日で作成できます。</span><span class="sxs-lookup"><span data-stu-id="9711b-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="9711b-116">プロジェクト自体から。</span><span class="sxs-lookup"><span data-stu-id="9711b-116">From the project itself.</span></span> <span data-ttu-id="9711b-117">この場合、プロジェクトは発注書に対してすでに定義されています。</span><span class="sxs-lookup"><span data-stu-id="9711b-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="9711b-118">プロジェクト発注書に移動して。</span><span class="sxs-lookup"><span data-stu-id="9711b-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="9711b-119">発注書を作成するには、仕入先とプロジェクトの両方を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9711b-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="9711b-120">品目はベンダー請求書が更新されるときに消費されます。</span><span class="sxs-lookup"><span data-stu-id="9711b-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9711b-121">販売注文から発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9711b-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="9711b-122">このメソッドは、プロジェクトから受注を作成する場合、アイテムを購入するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9711b-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="9711b-123">品目は、受注が顧客に請求されるときに消費されます。</span><span class="sxs-lookup"><span data-stu-id="9711b-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9711b-124">品目要件から発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9711b-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="9711b-125">このメソッドは、プロジェクトからアイテム要件を作成する場合、アイテムを購入するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9711b-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="9711b-126">品目は、品目要件梱包明細が更新されるときに消費されます。</span><span class="sxs-lookup"><span data-stu-id="9711b-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="9711b-127">仕入先請求書または梱包明細を更新すると、アイテム要件の梱包明細を更新するように求められます。</span><span class="sxs-lookup"><span data-stu-id="9711b-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="9711b-128">詳細については、[アイテム要件から発注書のアイテムを受け取る](tasks/receive-items-purchase-order-item-requirement.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9711b-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

