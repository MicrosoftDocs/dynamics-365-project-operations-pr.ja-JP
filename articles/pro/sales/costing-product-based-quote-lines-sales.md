---
title: 製品原価計算ベースの見積依頼明細行
description: このトピックでは、製品ベースの見積依頼明細行への原価価格の適用について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118929"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="3a94d-103">製品原価計算ベースの見積依頼明細行</span><span class="sxs-lookup"><span data-stu-id="3a94d-103">Costing product-based quote lines</span></span>

<span data-ttu-id="3a94d-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="3a94d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3a94d-105">Dynamics 365 Project Operations の製品ベースの見積依頼明細行にも **原価価格** フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="3a94d-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="3a94d-106">このフィールドは、見積依頼明細行で製品の原価価格を追跡し、下位の利益性の計算をするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3a94d-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="3a94d-107">カタログ製品に対する製品ベースの見積依頼明細行が作成されると、製品ベースの見積依頼明細行の原価は、製品カタログの **標準のコスト** フィールドで規定値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3a94d-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3a94d-108">製品カタログの標準のコスト フィールドは、組織の基本通貨で設定されます。</span><span class="sxs-lookup"><span data-stu-id="3a94d-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3a94d-109">製品ベースの見積依頼明細行での既定の単位原価は、見積の販売通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="3a94d-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="3a94d-110">製品ベースの見積依頼明細行の単位原価</span><span class="sxs-lookup"><span data-stu-id="3a94d-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="3a94d-111">製品ベースの見積依頼明細行で単位原価を設定する目的は、販売ごとに製品のさまざまなコストを考慮に入れることです。</span><span class="sxs-lookup"><span data-stu-id="3a94d-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="3a94d-112">これは典型的なシナリオではありませんが、最終販売の顧客によっては、製品のコストが納入業者によって割引される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3a94d-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="3a94d-113">たとえば、次のようなものです。</span><span class="sxs-lookup"><span data-stu-id="3a94d-113">For example:</span></span>

<span data-ttu-id="3a94d-114">Fabrikam Robotics は、A Datum Corporation のアセンブリ明細にロボット アームを設置しています。</span><span class="sxs-lookup"><span data-stu-id="3a94d-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="3a94d-115">Fabrikam は設置サービスを提供しますが、ロボット アームは Trey ロボティクスから調達されます。</span><span class="sxs-lookup"><span data-stu-id="3a94d-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="3a94d-116">A Datum Corporation にロボット アームを設置することで、Trey のロボット アームに新しい業界の垂直構造が開かれた場合、Trey はこの取引に対して Fabrikam に特別割引を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="3a94d-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="3a94d-117">この場合、Fabrikam は、Robotic Arms に対する製品ベースの見積依頼明細行を作成し、この見積もりの単位原価あたりの特別な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3a94d-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="3a94d-118">このコストは、Trey Robotic Arms の標準コストとは異なります。</span><span class="sxs-lookup"><span data-stu-id="3a94d-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
