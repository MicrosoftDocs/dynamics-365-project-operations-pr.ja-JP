---
title: 製品原価計算ベースの契約品目 (ライト)
description: このトピックでは、以下について説明します
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003547"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="fe713-103">製品原価計算ベースの契約品目 (ライト)</span><span class="sxs-lookup"><span data-stu-id="fe713-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="fe713-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="fe713-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fe713-105">Dynamics 365 Project Operations の製品ベースの契約品目には、**原価価格** フィールドが含まれますが、これにはダウンストリームの収益性計算のために製品の原価が保管されます。</span><span class="sxs-lookup"><span data-stu-id="fe713-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="fe713-106">カタログ製品に対して製品ベースの契約品目が作成されると、品目の原価は製品カタログの **標準原価** フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="fe713-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="fe713-107">製品カタログの **標準原価** フィールドは、組織の基準通貨で設定されています。</span><span class="sxs-lookup"><span data-stu-id="fe713-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="fe713-108">単位原価が契約品目で既定になると、契約の販売通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="fe713-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="fe713-109">製品ベースの契約品目の単位原価</span><span class="sxs-lookup"><span data-stu-id="fe713-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="fe713-110">製品ベースの契約品目に単位原価を持つことで、ユニットの販売ごとに異なる製品コストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fe713-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="fe713-111">常に必要というわけではありませんが、サプライヤが顧客に対して製品のコストを割り引く場合がある場合も想定されます。</span><span class="sxs-lookup"><span data-stu-id="fe713-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="fe713-112">次のシナリオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fe713-112">Consider the following scenario:</span></span>

<span data-ttu-id="fe713-113">Fabrikam Robotics 社は、A Datum Corporation 社の組立ラインにロボット アームを設置しています。</span><span class="sxs-lookup"><span data-stu-id="fe713-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="fe713-114">Fabrikam が設置サービスを提供していますが、ロボットアームは Trey Research 社製です。</span><span class="sxs-lookup"><span data-stu-id="fe713-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="fe713-115">Adatum 社にロボットアームを設置することで、Trey Research 社にとって新たな垂直産業を開くことができれば、Fabrikam 社にこの取引を特別割引で提供することができるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="fe713-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="fe713-116">この場合、Fabrikamは、ロボットアームの製品ベースの契約品目を作成します。</span><span class="sxs-lookup"><span data-stu-id="fe713-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="fe713-117">この契約には、単位当たりのコストが入力されます。</span><span class="sxs-lookup"><span data-stu-id="fe713-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="fe713-118">コストが、Trey Research のロボットアームのコストとは異なります。</span><span class="sxs-lookup"><span data-stu-id="fe713-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]