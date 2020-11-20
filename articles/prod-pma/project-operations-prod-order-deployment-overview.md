---
title: 在庫/製造ベース シナリオ展開の概要向け Project Operations
description: このトピックでは、展開の種類、在庫/製造ベースのシナリオ向け Project Operations について説明します。
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7bad4de10a508f0c1aa2cc6bb0c41081f81fb259
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365527"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="08df4-103">在庫/製造ベース シナリオ展開の概要向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="08df4-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="08df4-104">_**適用対象:** 在庫/製造ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="08df4-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="08df4-105">この展開の種類には、プロジェクトベースの企業向けに次の機能があります:</span><span class="sxs-lookup"><span data-stu-id="08df4-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="08df4-106">[WBS (作業分解構造)](work-breakdown-structures.md) を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="08df4-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="08df4-107">プロジェクト用在庫の調達および消費</span><span class="sxs-lookup"><span data-stu-id="08df4-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="08df4-108">Dynamics 365 Finance and Operations アプリで **営業およびマーケティング** モジュールを使用してプロジェクトベースの営業の管理</span><span class="sxs-lookup"><span data-stu-id="08df4-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="08df4-109">Finance and Operations アプリで原価率と請求率の構成を使用したプロジェクトの価格設定と原価計算</span><span class="sxs-lookup"><span data-stu-id="08df4-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="08df4-110">Finance and Operations アプリでプロジェクトのリソース管理</span><span class="sxs-lookup"><span data-stu-id="08df4-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="08df4-111">Finance and Operations アプリでプロジェクトの進捗状況と時間追跡</span><span class="sxs-lookup"><span data-stu-id="08df4-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="08df4-112">OCR 機能を使用した領収書の取り込みによる、プロジェクトおよび非プロジェクト経費の経費管理エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="08df4-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="08df4-113">エンタープライズ クラスの消費税と日付有効為替レート システムを使用した請求</span><span class="sxs-lookup"><span data-stu-id="08df4-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="08df4-114">WIP 会計および見越計上のための構成可能なプロジェクト グループ</span><span class="sxs-lookup"><span data-stu-id="08df4-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="08df4-115">プロジェクトの収益認識</span><span class="sxs-lookup"><span data-stu-id="08df4-115">Project revenue recognition</span></span>

<span data-ttu-id="08df4-116">この展開の種類は、Dynamics 365 Finance と Dynamics 365 Supply Chain Management アプリケーションが提供する機能に拡張機能も提供します。</span><span class="sxs-lookup"><span data-stu-id="08df4-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="08df4-117">次の主要要件を含め、プロジェクト ライフサイクル全体で Dynamics 365 Project Operations を使用するには、この展開の種類を選択します:</span><span class="sxs-lookup"><span data-stu-id="08df4-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="08df4-118">スケジュールと財務のための、内部および請求可能なプロジェクトの在庫品目とジョブ/製造オーダーの原価計算を管理する広範囲なプロジェクト管理システム。</span><span class="sxs-lookup"><span data-stu-id="08df4-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="08df4-119">組織にはすでに Dynamics 365 Finance または Dynamics 365 Supply Chain and Manufacturing apps アプリがあり、プロジェクトベースのトランザクションの統合により、データ アクセスと報告ニーズが簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="08df4-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="08df4-120">プロジェクトおよび非プロジェクト経費を追跡するためのポリシーの実施と償還を含む、完全に機能する経費管理システム。</span><span class="sxs-lookup"><span data-stu-id="08df4-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="08df4-121">プロジェクトの顧客向け請求書を生成するためのエンタープライズ クラスの消費税および為替レート エンジン。</span><span class="sxs-lookup"><span data-stu-id="08df4-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="08df4-122">国際財務報告基準 (IFRS) に準拠したプロジェクト会計および収益認識システム。</span><span class="sxs-lookup"><span data-stu-id="08df4-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>

