---
title: カタログ製品の原価率と販売率を設定する - Lite
description: このトピックは、製品カタログ内のアイテムのコストと販売率を設定する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274464"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="73742-103">カタログ製品の原価率と販売率を設定する - Lite</span><span class="sxs-lookup"><span data-stu-id="73742-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="73742-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="73742-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="73742-105">Dynamics 365 Project Operations で製品カタログ アイテムの価格設定を行う方法は、Dynamics 365 Sales と同じです。</span><span class="sxs-lookup"><span data-stu-id="73742-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="73742-106">Project Operations では、製品を見積もったりプロジェクトで使用したりすることはできないため、見積もりや契約のために製品カタログの価格をプロジェクトの価格表に設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="73742-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="73742-107">見積もり、契約の **製品価格** フィールドを使うか、製品カタログの価格を設定します。</span><span class="sxs-lookup"><span data-stu-id="73742-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="73742-108">プロジェクト価格表に製品カタログの価格を設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="73742-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="73742-109">プロジェクトの価格表は、Project Operations 専用です。</span><span class="sxs-lookup"><span data-stu-id="73742-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="73742-110">アプリケーション固有のビジネス ロジックは、価格表を見積もりから契約にコピーします。</span><span class="sxs-lookup"><span data-stu-id="73742-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="73742-111">この結果は、契約に固有のプロジェクトの価格表です。</span><span class="sxs-lookup"><span data-stu-id="73742-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="73742-112">見積もりのプロジェクト価格表が大きくなりすぎると、コピー操作によって見積もりの受注プロセスが遅れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="73742-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="73742-113">製品の価格表は、契約のカスタム価格表を作成するためにコピーされません。</span><span class="sxs-lookup"><span data-stu-id="73742-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="73742-114">コピーが含まれないため、見積もりプロセスのパフォーマンスに影響はありません。</span><span class="sxs-lookup"><span data-stu-id="73742-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]