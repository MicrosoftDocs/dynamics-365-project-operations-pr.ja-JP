---
title: リソースの見積もり
description: このトピックは、Project Operations でリソースの見積もりを計算する方法について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079188"
---
# <a name="resource-estimates"></a><span data-ttu-id="f94ea-103">リソースの見積もり</span><span class="sxs-lookup"><span data-stu-id="f94ea-103">Resource estimates</span></span>

<span data-ttu-id="f94ea-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="f94ea-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f94ea-105">リソースの見積もりは、適用可能な価格設定のディメンションとともに、作業分解構造で定義された時間フェーズの作業から得られます。</span><span class="sxs-lookup"><span data-stu-id="f94ea-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="f94ea-106">通常、計算は **各ロールのレート/時間 x 時間** です。</span><span class="sxs-lookup"><span data-stu-id="f94ea-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="f94ea-107">各リソースの時間フェーズの作業は、リソース割り当てレコードに保存されます。</span><span class="sxs-lookup"><span data-stu-id="f94ea-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="f94ea-108">価格設定は、事前定義された価格表に保存されます。</span><span class="sxs-lookup"><span data-stu-id="f94ea-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="f94ea-109">単位換算は、該当する価格表に基づいて適用されます。</span><span class="sxs-lookup"><span data-stu-id="f94ea-109">Unit conversion is applied based on the applicable price list.</span></span>

![リソースの見積もり](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="f94ea-111">既定の原価価格と原価通貨</span><span class="sxs-lookup"><span data-stu-id="f94ea-111">Default cost price and cost currency</span></span>

<span data-ttu-id="f94ea-112">原価は組織単位から既定設定されます。</span><span class="sxs-lookup"><span data-stu-id="f94ea-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="f94ea-113">既定の請求レートと販売通貨</span><span class="sxs-lookup"><span data-stu-id="f94ea-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="f94ea-114">販売価格は取引ごとに 1 回適用されます。</span><span class="sxs-lookup"><span data-stu-id="f94ea-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="f94ea-115">販売価格表の既定の階層は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f94ea-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="f94ea-116">組織全体</span><span class="sxs-lookup"><span data-stu-id="f94ea-116">Organization</span></span>
2. <span data-ttu-id="f94ea-117">顧客</span><span class="sxs-lookup"><span data-stu-id="f94ea-117">Customer</span></span>
3. <span data-ttu-id="f94ea-118">見積もり/契約</span><span class="sxs-lookup"><span data-stu-id="f94ea-118">Quote/contract</span></span>
