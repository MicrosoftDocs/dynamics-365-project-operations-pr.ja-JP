---
title: Project Operations の二重書き込みの統合
description: このトピックでは、Project Operations の二重書き込みの統合の概要について説明します。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998687"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="89291-103">Project Operations の二重書き込みの統合の概要</span><span class="sxs-lookup"><span data-stu-id="89291-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="89291-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="89291-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="89291-105">Project Operations は[二重書き込み機能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)を使って、Microsoft Dataverse と Dynamics 365 Finance の間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="89291-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="89291-106">次の図は、この Dataverse と Finance の統合の一環としてデータが同期される様子を示しています。</span><span class="sxs-lookup"><span data-stu-id="89291-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations データフローの概要](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="89291-108">Dataverse での Project Operations は、最新のユーザーインターフェース (UI) と、Power Platform の機能を使った簡単なノーコード/ローコードの拡張性を提供します。</span><span class="sxs-lookup"><span data-stu-id="89291-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="89291-109">プロジェクト マネージャー、リソース マネージャー、プロジェクト チームのメンバーなどのフロント オフィスのペルソナは、Project Operations on Dataverse で自身の活動を行います。</span><span class="sxs-lookup"><span data-stu-id="89291-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="89291-110">Project Operations in Finance は、プロジェクトの会計と収益認識のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="89291-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="89291-111">Project Operations は、Finance の財務フレーム ワークに接続して、売上税の計算、為替レート、財務指標の報告などを行います。</span><span class="sxs-lookup"><span data-stu-id="89291-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="89291-112">プロジェクト会計士の経験は、主に Finance に基づきます。</span><span class="sxs-lookup"><span data-stu-id="89291-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="89291-113">Project Operations の統合は、以下のコンポーネントの統合で構成されています:</span><span class="sxs-lookup"><span data-stu-id="89291-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="89291-114">Project Operations のセットアップと構成データの統合</span><span class="sxs-lookup"><span data-stu-id="89291-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="89291-115">プロジェクトの見積もりと実績</span><span class="sxs-lookup"><span data-stu-id="89291-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="89291-116">プロジェクトの請求書</span><span class="sxs-lookup"><span data-stu-id="89291-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="89291-117">経費管理</span><span class="sxs-lookup"><span data-stu-id="89291-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="89291-118">ベンダー請求書</span><span class="sxs-lookup"><span data-stu-id="89291-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
