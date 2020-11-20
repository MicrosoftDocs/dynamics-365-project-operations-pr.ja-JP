---
title: カタログ製品の原価率と販売率を設定する - Lite
description: このトピックは、製品カタログ内のアイテムのコストと販売率を設定する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176707"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="10395-103">カタログ製品の原価率と販売率を設定する - Lite</span><span class="sxs-lookup"><span data-stu-id="10395-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="10395-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="10395-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="10395-105">Dynamics 365 Project Operations での製品カタログ アイテムの価格設定は、Dynamics 365 Sales の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="10395-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="10395-106">Project Operations のプロジェクトでは製品を見積もったり使用したりできないため、見積もりや契約のプロジェクト価格表に製品カタログの価格を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="10395-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="10395-107">製品カタログの価格は、見積もり、契約、またはアカウントの **製品価格** フィールドに設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="10395-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="10395-108">これらのエンティティのプロジェクト価格表に製品カタログ価格を設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="10395-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="10395-109">プロジェクトの価格表は、Project Operations 専用です。</span><span class="sxs-lookup"><span data-stu-id="10395-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="10395-110">価格表を見積もりから契約にコピーするアプリケーション固有のビジネス ロジックがあります。</span><span class="sxs-lookup"><span data-stu-id="10395-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="10395-111">この結果は、契約に固有のプロジェクトの価格表です。</span><span class="sxs-lookup"><span data-stu-id="10395-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="10395-112">見積もりのプロジェクト価格表が大きくなりすぎると、コピー操作によって見積もりの受注プロセスが遅れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10395-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="10395-113">製品の価格表は、契約のカスタム価格表を作成するためにコピーされません。</span><span class="sxs-lookup"><span data-stu-id="10395-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="10395-114">これは、製品の価格表が見積もり受注プロセスのパフォーマンスに影響を与えないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="10395-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
