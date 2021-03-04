---
title: 製品ベースの営業案件品目 - Lite
description: このトピックでは、Project Operations での製品ベースの営業案件明細行の品目について説明します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764960"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="5f792-103">製品ベースの営業案件品目 - Lite</span><span class="sxs-lookup"><span data-stu-id="5f792-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="5f792-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="5f792-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5f792-105">製品ベースの営業案件明細行は、営業案件の品目です。</span><span class="sxs-lookup"><span data-stu-id="5f792-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="5f792-106">これらの個別の行項目は、顧客に提供される最終的な請求書に記載されています。</span><span class="sxs-lookup"><span data-stu-id="5f792-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="5f792-107">請求書には、その他の追加サービスは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5f792-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="5f792-108">関連する支出と消費は、関連するプロジェクトのタスクでは追跡されません。</span><span class="sxs-lookup"><span data-stu-id="5f792-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="5f792-109">製品ベースの明細行は、カタログ品目またはリスト外製品にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5f792-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="5f792-110">営業案件の製品ベース明細行での機能の大部分は、Dynamics 365 Sales アプリケーションによって提供される機能に従います。</span><span class="sxs-lookup"><span data-stu-id="5f792-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="5f792-111">製品ベースの営業案件明細行の詳細については、[営業案件に製品を追加する](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f792-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="5f792-112">**顧客の予算** は、プロジェクトベースの営業案件行項目に固有の概念です。</span><span class="sxs-lookup"><span data-stu-id="5f792-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="5f792-113">**顧客の予算** フィールドは、顧客が品目に支払う意思のある金額を追跡します。</span><span class="sxs-lookup"><span data-stu-id="5f792-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="5f792-114">営業案件サマリーの収益方法が **システム計算** の場合、営業案件明細行全体の顧客予算値を集計して、推定収益を計算します。</span><span class="sxs-lookup"><span data-stu-id="5f792-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

