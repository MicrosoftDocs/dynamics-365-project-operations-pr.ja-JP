---
title: 製品原価計算ベースの契約品目
description: このトピックでは、以下について説明します
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079499"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="e16f0-103">製品原価計算ベースの契約品目</span><span class="sxs-lookup"><span data-stu-id="e16f0-103">Costing product-based contract lines</span></span>

<span data-ttu-id="e16f0-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="e16f0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e16f0-105">Dynamics 365 Project Operations の製品ベースの契約ラインには、下流の収益性計算で使用する製品のコスト価格を格納する **原価価格** フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="e16f0-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="e16f0-106">カタログ製品に製品ベースの契約品目を作成した場合、製品ベースの契約品目のコストは、製品カタログの **標準原価** フィールドから既定で作成されます。</span><span class="sxs-lookup"><span data-stu-id="e16f0-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="e16f0-107">製品カタログの **標準原価** フィールドは、組織の基準通貨で設定されています。</span><span class="sxs-lookup"><span data-stu-id="e16f0-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="e16f0-108">単位原価が契約品目で既定になると、契約の販売通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="e16f0-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="e16f0-109">製品ベースの契約品目の単位原価</span><span class="sxs-lookup"><span data-stu-id="e16f0-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="e16f0-110">製品ベースの契約品目に単位原価を持つことで、ユニットの販売ごとに異なる製品コストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e16f0-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="e16f0-111">常に必要というわけではありませんが、サプライヤが顧客に対して製品のコストを割り引く場合がある場合も想定されます。</span><span class="sxs-lookup"><span data-stu-id="e16f0-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="e16f0-112">次のシナリオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e16f0-112">Consider the following scenario:</span></span>

<span data-ttu-id="e16f0-113">Fabrikam Robotics 社は、A Datum Corporation 社の組立ラインにロボット アームを設置しています。</span><span class="sxs-lookup"><span data-stu-id="e16f0-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="e16f0-114">Fabrikam 社は設置サービスを提供していますが、ロボットアームは Trey Research 社から調達しています。</span><span class="sxs-lookup"><span data-stu-id="e16f0-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="e16f0-115">Adatum 社にロボットアームを設置することで、Trey Research 社にとって新たな垂直産業を開くことができれば、Fabrikam 社にこの取引を特別割引で提供することができるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="e16f0-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="e16f0-116">この場合、Fabrikam 社は、ロボット アームの製品ベースの契約品目を作成し、この契約に向けて、Trey Research 社のロボットアームの標準的なコストとは異なる単価を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16f0-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
