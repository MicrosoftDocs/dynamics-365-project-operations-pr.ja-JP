---
title: 営業価格表の設定
description: このトピックでは、プロジェクトの価格に使用する営業価格表についての説明をします。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004897"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="e1a07-103">営業価格表の設定</span><span class="sxs-lookup"><span data-stu-id="e1a07-103">Set up a sales price list</span></span>

<span data-ttu-id="e1a07-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="e1a07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1a07-105">プロジェクトの見積もりと契約において、プロジェクトの価格表には製品の価格表とは異なる上書きパターンがあります。</span><span class="sxs-lookup"><span data-stu-id="e1a07-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="e1a07-106">製品カタログ ベースの見積依頼明細行では、各見積依頼明細行が正確に 1 つのカタログ品目を指すため、見積依頼明細行で価格をロールおよびカテゴリに直接上書きできます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="e1a07-107">ただし、プロジェクト ベースの見積依頼明細行では、見積依頼明細行で価格をロールおよびカテゴリに直接上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e1a07-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="e1a07-108">プロジェクト価格表を使用して、2つの異なる指定パターンを操作できます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="e1a07-109">価格設定を上書きする場合の 2 つの動作には違いがあるため、プロジェクト リソース用とカタログ品目用にそれぞれ価格表を持つことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e1a07-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="e1a07-110">次の各エンティティには、プロジェクトの価格設定用に 1 つ以上の関連する販売価格表を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="e1a07-111">顧客 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="e1a07-111">Customer (account)</span></span> 
- <span data-ttu-id="e1a07-112">営業案件</span><span class="sxs-lookup"><span data-stu-id="e1a07-112">Opportunity</span></span> 
- <span data-ttu-id="e1a07-113">見積もり</span><span class="sxs-lookup"><span data-stu-id="e1a07-113">Quote</span></span> 
- <span data-ttu-id="e1a07-114">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="e1a07-114">Project Contract</span></span>

<span data-ttu-id="e1a07-115">これらのエンティティと価格表の関連付けは、プロジェクト価格表によって示されます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="e1a07-116">顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、1 つ以上の価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="e1a07-117">既定のプロジェクト価格表は、顧客レコードに自動的に入力されません。</span><span class="sxs-lookup"><span data-stu-id="e1a07-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="e1a07-118">ただし、顧客レコードに手動でプロジェクト価格表を添付できます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="e1a07-119">それでも、顧客とのカスタムの価格設定について合意がある場合にのみ、手動でプロジェクト価格表を添付してください。</span><span class="sxs-lookup"><span data-stu-id="e1a07-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="e1a07-120">プロジェクト価格表が営業エンティティに添付されると、次の情報を検証します :</span><span class="sxs-lookup"><span data-stu-id="e1a07-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="e1a07-121">価格表が **営業** のコンテキストを保有している。</span><span class="sxs-lookup"><span data-stu-id="e1a07-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="e1a07-122">価格表の通貨が顧客の通貨と一致している。</span><span class="sxs-lookup"><span data-stu-id="e1a07-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="e1a07-123">プロジェクト契約では、次の優先順位を使用して、関連するプロジェクト価格表を自動的に設定します。</span><span class="sxs-lookup"><span data-stu-id="e1a07-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="e1a07-124">見積もり </span><span class="sxs-lookup"><span data-stu-id="e1a07-124">Quote</span></span>
2. <span data-ttu-id="e1a07-125">営業案件​​</span><span class="sxs-lookup"><span data-stu-id="e1a07-125">Opportunity</span></span>
3. <span data-ttu-id="e1a07-126">顧客</span><span class="sxs-lookup"><span data-stu-id="e1a07-126">Customer</span></span> 
4. <span data-ttu-id="e1a07-127">グローバル設定</span><span class="sxs-lookup"><span data-stu-id="e1a07-127">Global settings</span></span> 

<span data-ttu-id="e1a07-128">既定のプロジェクト価格表が入力されると、システムは通貨が顧客の通貨と一致すること、および入力された既定の価格表が **営業** コンテキストを保有していることを検証します。</span><span class="sxs-lookup"><span data-stu-id="e1a07-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="e1a07-129">顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、複数のプロジェクト価格表を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e1a07-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="e1a07-130">この機能は、長期にわたるプロジェクト契約の日付固有の既定の価格をサポートします。この場合、インフレによって発生する価格更新に対応するため、アカウントに複数の価格表が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e1a07-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="e1a07-131">ただし、顧客、営業案件、見積もり、またはプロジェクト契約のエンティティに関連付けられている価格表の日付の有効性が重複していると、既定の価格が正しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e1a07-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="e1a07-132">そのため、日付の有効性が重複しているプロジェクト価格表がそれらのエンティティに関連付けられていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1a07-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]