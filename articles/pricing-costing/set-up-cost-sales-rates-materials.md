---
title: 材料の原価率と販売率を設定する
description: このトピックは、プロジェクトで使用される材料のコストと販売率を設定する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 05abefcec5c64632d00e2317107fe7a84ded4908
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877793"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a><span data-ttu-id="bf2b5-103">材料の原価率と販売率を設定する</span><span class="sxs-lookup"><span data-stu-id="bf2b5-103">Set up cost and sales rates for materials</span></span>

<span data-ttu-id="bf2b5-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="bf2b5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf2b5-105">Dynamics 365 Project Operations で製品のコストと販売価格を設定できます。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-105">You can set up cost and sales prices for products in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="bf2b5-106">製品のコストと販売価格は 1 つの通貨でのみ表示できます。これは、価格表ヘッダーの通貨である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-106">Cost and sales prices for products can only be listed in one currency, which must be the currency on the price list header.</span></span>

<span data-ttu-id="bf2b5-107">製品のコストと販売率を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-107">To set up cost and sales rates for products, complete the following steps.</span></span> 

1. <span data-ttu-id="bf2b5-108">**販売** > **顧客** > **価格表** に移動して、**新規** を選択して、新しい価格表を作成します。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-108">Go to **Sales** > **Customers** > **Price Lists** and select **New** to create a new price list.</span></span> 
2. <span data-ttu-id="bf2b5-109">**価格表品目** のサブグリッド メニューで、**新しい価格表品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-109">On the **Price list items**, on the subgrid menu, select **New price list item**.</span></span> 
3. <span data-ttu-id="bf2b5-110">**クイック作成** ページで、新しい価格を作成する製品と単位を入力します。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-110">On the **Quick Create** page, enter the product and unit that you are creating the new price for.</span></span>

<span data-ttu-id="bf2b5-111">カタログ品目の価格を定義する方法の詳細については、[製品の価格設定](https://docs.microsoft.com/dynamics365/sales-enterprise/create-price-lists-price-list-items-define-pricing-products)と[通貨と価格設定の有効桁数](https://docs.microsoft.com/dynamics365/sales-enterprise/decimal-precision-currency-pricing)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf2b5-111">For more information about how to define prices for catalog items, see [Setup pricing for products](https://docs.microsoft.com/dynamics365/sales-enterprise/create-price-lists-price-list-items-define-pricing-products) and [Decimal precision in currency and pricing](https://docs.microsoft.com/dynamics365/sales-enterprise/decimal-precision-currency-pricing).</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
