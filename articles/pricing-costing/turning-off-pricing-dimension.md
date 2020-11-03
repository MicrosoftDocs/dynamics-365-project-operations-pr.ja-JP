---
title: 価格設定ディメンションをオフにする
description: このトピックでは価格ディメンションを無効化する方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a7c91ef70b1dd3697f6a8b5044c6ad4a14c4e74
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079364"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="ae62f-103">価格設定ディメンションをオフにする</span><span class="sxs-lookup"><span data-stu-id="ae62f-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="ae62f-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ae62f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae62f-105">価格設定戦略を数年度ごとにレビューし、更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="ae62f-106">何らかの更新を行うと、既存の価格設定のディメンションを停止して新たに作成しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="ae62f-107">たとえば、以前は、 **ロール** によって価格設定を行っていたとしても、現在は、 **ワーク エクスペリエンス** によって価格設定することを決定しています。</span><span class="sxs-lookup"><span data-stu-id="ae62f-107">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="ae62f-108">この場合、価格設定のディメンションとして、 **ロール** を停止し、 **ワーク エクスペリエンス** を新たな価格設定のディメンションとして作成する必要性が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="ae62f-109">価格設定のディメンションを停止するには、それが標準であるかカスタムであるかにかかわらず、価格設定ディメンションの **コストに適用可能** および **営業に適用可能** フィールドを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae62f-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="ae62f-110">ただし、これを行うと、次のエラーメッセージが表示される場合があります : **関連する価格レコードがある場合、価格ディメンションを更新または削除することはできません。**</span><span class="sxs-lookup"><span data-stu-id="ae62f-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

<span data-ttu-id="ae62f-111">このエラー メッセージは、停止されているディメンションに対して過去に設定済みの価格のレコードが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="ae62f-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="ae62f-112">ディメンションを参照するすべての **ロール価格** および **ロール価格利幅** レコード は、ディメンションの適用領域を **いいえ** に設定する可能性があればその前に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="ae62f-113">このルールは、作成済みの双方の標準価格ディメンションおよび任意のカスタム価格ディメンションに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ae62f-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="ae62f-114">この検証の理由は、それぞれの **ロール価格** レコードは一意のディメンション組み合わせを持つ必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="ae62f-114">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="ae62f-115">たとえば、 **US Cost Rates 2018** と呼ばれる価格表には、次の **ロール価格** 行があります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="ae62f-116">標準タイトル</span><span class="sxs-lookup"><span data-stu-id="ae62f-116">Standard Title</span></span>         | <span data-ttu-id="ae62f-117">組織単位</span><span class="sxs-lookup"><span data-stu-id="ae62f-117">Org Unit</span></span>    |<span data-ttu-id="ae62f-118">出荷単位</span><span class="sxs-lookup"><span data-stu-id="ae62f-118">Unit</span></span>   |<span data-ttu-id="ae62f-119">価格</span><span class="sxs-lookup"><span data-stu-id="ae62f-119">Price</span></span>  |<span data-ttu-id="ae62f-120">[通貨]</span><span class="sxs-lookup"><span data-stu-id="ae62f-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="ae62f-121">システム エンジニア</span><span class="sxs-lookup"><span data-stu-id="ae62f-121">Systems Engineer</span></span>|<span data-ttu-id="ae62f-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ae62f-122">Contoso US</span></span>|<span data-ttu-id="ae62f-123">Hour</span><span class="sxs-lookup"><span data-stu-id="ae62f-123">Hour</span></span>| <span data-ttu-id="ae62f-124">100</span><span class="sxs-lookup"><span data-stu-id="ae62f-124">100</span></span>|<span data-ttu-id="ae62f-125">USD</span><span class="sxs-lookup"><span data-stu-id="ae62f-125">USD</span></span>|
| <span data-ttu-id="ae62f-126">シニア システム エンジニア</span><span class="sxs-lookup"><span data-stu-id="ae62f-126">Senior Systems Engineer</span></span>|<span data-ttu-id="ae62f-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ae62f-127">Contoso US</span></span>|<span data-ttu-id="ae62f-128">Hour</span><span class="sxs-lookup"><span data-stu-id="ae62f-128">Hour</span></span>| <span data-ttu-id="ae62f-129">150</span><span class="sxs-lookup"><span data-stu-id="ae62f-129">150</span></span>| <span data-ttu-id="ae62f-130">USD</span><span class="sxs-lookup"><span data-stu-id="ae62f-130">USD</span></span>|


<span data-ttu-id="ae62f-131">価格設定ディメンションとして **標準タイトル** をオフにして、価格設定エンジンで価格を検索すると、入力コンテキストの **組織単位** 値のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae62f-131">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="ae62f-132">入力コンテキストの **組織単位** が 「Contoso US」であるとすると、その行の両方が一致するため、結果が非確定的になります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="ae62f-133">このシナリオを回避するため、 **ロール価格** レコードを作成する際には、ディメンションの組み合わせが一意であることシステムが検証します。</span><span class="sxs-lookup"><span data-stu-id="ae62f-133">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="ae62f-134">**ロール価格** レコードを作成後にディメンションを停止した場合、この制約に違反する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae62f-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="ae62f-135">したがって、ディメンションを停止する前に必要なことは、ディメンション値が有効になっている **ロール価格** および **ロール価格の利幅** 行をすべて削除することです。</span><span class="sxs-lookup"><span data-stu-id="ae62f-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
