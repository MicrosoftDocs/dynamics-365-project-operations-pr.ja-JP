---
title: 製品ベースの営業案件明細行
description: このトピックでは、Project Operations での製品ベースの営業案件明細行の品目について説明します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896242"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="0384d-103">製品ベースの営業案件明細行</span><span class="sxs-lookup"><span data-stu-id="0384d-103">Product-based opportunity lines</span></span>

<span data-ttu-id="0384d-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="0384d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0384d-105">製品ベースの営業案件明細行は、営業案件の品目です。</span><span class="sxs-lookup"><span data-stu-id="0384d-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="0384d-106">これらの明細行は、他の付加価値サービスなしで、最終的な請求書の個別の品目として顧客に配信されます。</span><span class="sxs-lookup"><span data-stu-id="0384d-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="0384d-107">関連する支出と消費は、関連するプロジェクトのタスクでは追跡されません。</span><span class="sxs-lookup"><span data-stu-id="0384d-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="0384d-108">製品ベースの明細行は、カタログ品目またはリスト外製品にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0384d-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="0384d-109">営業案件の製品ベース明細行での機能の大部分は、Dynamics 365 Sales アプリケーションによって提供される機能に従います。</span><span class="sxs-lookup"><span data-stu-id="0384d-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="0384d-110">製品ベースの営業案件明細行の詳細については、[営業案件に製品を追加する](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0384d-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="0384d-111">プロジェクトベースの営業案件に固有の製品ベースの営業案件明細行に関する 1 つの概念は、**顧客予算**です。</span><span class="sxs-lookup"><span data-stu-id="0384d-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="0384d-112">このフィールドを使用して、顧客が品目に快く支払う金額を追跡します。</span><span class="sxs-lookup"><span data-stu-id="0384d-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="0384d-113">営業案件の概要の売上方法が**システムにより計算**に設定されている場合、製品ベースおよびプロジェクトベースの明細行全体の顧客予算値を要約して、売上見込みを計算します。</span><span class="sxs-lookup"><span data-stu-id="0384d-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
