---
title: リソース/非在庫ベース シナリオ展開の概要向け Project Operations
description: このトピックでは、展開の種類、リソース/非在庫ベースのシナリオ向け Project Operations について説明します。
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 770947835af41bd06c02ca08b6ed8e810b9bdcf8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289960"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="79b7e-103">リソース/非在庫ベース シナリオ展開の概要向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="79b7e-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="79b7e-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="79b7e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="79b7e-105">リソース/非在庫ベースのシナリオのための展開タイプ Dynamics 365 Project Operations には、プロジェクトベースの会社に向けに次の機能があります。</span><span class="sxs-lookup"><span data-stu-id="79b7e-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="79b7e-106">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="79b7e-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="79b7e-107">労働力の多面的な価格設定と原価計算</span><span class="sxs-lookup"><span data-stu-id="79b7e-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="79b7e-108">経費カテゴリのカテゴリ ベースの価格設定</span><span class="sxs-lookup"><span data-stu-id="79b7e-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="79b7e-109">Dynamics 365 Sales の機能を使用したプロジェクトベースの営業管理</span><span class="sxs-lookup"><span data-stu-id="79b7e-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="79b7e-110">Dynamics 365 Field Service や Dynamics 365 Customer Service などの他のアプリケーションと統合する Universal Resource Scheduling</span><span class="sxs-lookup"><span data-stu-id="79b7e-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="79b7e-111">プロジェクトの進捗状況と時間追跡</span><span class="sxs-lookup"><span data-stu-id="79b7e-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="79b7e-112">OCR 機能を使用した領収書の取り込みを含む、プロジェクトおよび非プロジェクト経費の基本的かつ完全な経費管理エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="79b7e-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="79b7e-113">見積もりから顧客向けに拡張され、エンタープライズ クラスの消費税と日付有効為替レート システムに裏打ちされた請求書。</span><span class="sxs-lookup"><span data-stu-id="79b7e-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="79b7e-114">構成可能なプロジェクト コスト、収益プロファイル、および仕掛品 (WIP) の会計と見越計上のルール</span><span class="sxs-lookup"><span data-stu-id="79b7e-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="79b7e-115">プロジェクトの収益認識</span><span class="sxs-lookup"><span data-stu-id="79b7e-115">Project revenue recognition</span></span>
- <span data-ttu-id="79b7e-116">Power Platform を使用した拡張性</span><span class="sxs-lookup"><span data-stu-id="79b7e-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="79b7e-117">この展開の種類は、Dynamics 365 Finance と Dynamics 365 Supply Chain Management アプリケーションが提供する機能に拡張機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="79b7e-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="79b7e-118">この展開は、Project Operations が、次の要件を含むプロジェクト ライフサイクル全体を使用することを想定して、選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79b7e-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="79b7e-119">営業アプリケーションの機能を使用して、他の種類の営業でプロジェクトベースの営業を管理する機能。</span><span class="sxs-lookup"><span data-stu-id="79b7e-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="79b7e-120">プロジェクトの営業から会計まで、スケジュールと財務の内部および請求可能なプロジェクトを管理する統合プロジェクト管理システム。</span><span class="sxs-lookup"><span data-stu-id="79b7e-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="79b7e-121">プロジェクトおよび非プロジェクト経費を追跡するためのポリシーの実施と償還を含む経費管理システム。</span><span class="sxs-lookup"><span data-stu-id="79b7e-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="79b7e-122">プロジェクトの顧客向け請求書を生成するために、充実した、エンタープライズ クラスの消費税および為替レート エンジンが必要です。</span><span class="sxs-lookup"><span data-stu-id="79b7e-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="79b7e-123">国際財務報告基準 (IFRS) に準拠したプロジェクト会計および収益認識システム。</span><span class="sxs-lookup"><span data-stu-id="79b7e-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="79b7e-124">Finance または Supply Chain Management アプリケーションとプロジェクトベース トランザクションの統合。</span><span class="sxs-lookup"><span data-stu-id="79b7e-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]