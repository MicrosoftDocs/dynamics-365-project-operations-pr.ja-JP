---
title: Project Operations の二重書き込みの統合
description: このトピックでは、Project Operations の二重書き込みの統合の概要について説明します。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955664"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="1aace-103">Project Operations の二重書き込みの統合の概要</span><span class="sxs-lookup"><span data-stu-id="1aace-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="1aace-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="1aace-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1aace-105">Project Operations は[二重書き込み機能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)を使って、Microsoft Dataverse と Dynamics 365 Finance の間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="1aace-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="1aace-106">次の図は、この Dataverse と Finance の統合の一環としてデータが同期される様子を示しています。</span><span class="sxs-lookup"><span data-stu-id="1aace-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations データフローの概要](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="1aace-108">Dataverse での Project Operations は、最新のユーザーインターフェース (UI) と、Power Platform の機能を使った簡単なノーコード/ローコードの拡張性を提供します。</span><span class="sxs-lookup"><span data-stu-id="1aace-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="1aace-109">プロジェクト マネージャー、リソース マネージャー、プロジェクト チームのメンバーなどのフロント オフィスのペルソナは、Project Operations on Dataverse で自身の活動を行います。</span><span class="sxs-lookup"><span data-stu-id="1aace-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="1aace-110">Project Operations in Finance は、プロジェクトの会計と収益認識のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="1aace-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="1aace-111">Project Operations は、Finance の財務フレーム ワークに接続して、売上税の計算、為替レート、財務指標の報告などを行います。</span><span class="sxs-lookup"><span data-stu-id="1aace-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="1aace-112">プロジェクト会計士の経験は、主に Finance に基づきます。</span><span class="sxs-lookup"><span data-stu-id="1aace-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="1aace-113">Project Operations の統合は、以下のコンポーネントの統合で構成されています:</span><span class="sxs-lookup"><span data-stu-id="1aace-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="1aace-114">Project Operations のセットアップと構成データの統合</span><span class="sxs-lookup"><span data-stu-id="1aace-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="1aace-115">プロジェクトの見積もりと実績</span><span class="sxs-lookup"><span data-stu-id="1aace-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="1aace-116">プロジェクトの請求書</span><span class="sxs-lookup"><span data-stu-id="1aace-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="1aace-117">経費管理</span><span class="sxs-lookup"><span data-stu-id="1aace-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="1aace-118">ベンダー請求書</span><span class="sxs-lookup"><span data-stu-id="1aace-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
