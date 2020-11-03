---
title: レポート作成ホーム ページ
description: このトピックでは、 Dynamics 365 Project Service Automation でのレポート作成に関する情報へのリンクを提供します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079495"
---
# <a name="reporting-home-page"></a><span data-ttu-id="58586-103">レポート作成ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="58586-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="58586-104">Microsoft Dynamics 365 Project Service Automation を使うことで、プロジェクトベースの組織は事業の操作を効率的に管理することができます。</span><span class="sxs-lookup"><span data-stu-id="58586-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="58586-105">どのプロジェクトでも、チーム メンバーは、営業案件、見積もり、および作業の計画の管理、プロジェクトのリソース、計画に従った作業の管理、作業の請求書、そしてプロジェクトを完了するために作業を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58586-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="58586-106">操作でレポート機能は、組織の正常性を判断し、必要な修正措置を講じるための重要な鍵となります。</span><span class="sxs-lookup"><span data-stu-id="58586-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="58586-107">PSA はすべてのレポート作成で、Microsoft Dynamics 365 のレポート作成メソッドと技術を使用しています。</span><span class="sxs-lookup"><span data-stu-id="58586-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="58586-108">レポートのオプションの詳細については、[Dynamics 365 Customer Engagement (on-premises)のレポート作成ガイド、バージョン9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58586-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="58586-109">レポート ウィザード</span><span class="sxs-lookup"><span data-stu-id="58586-109">Report Wizard</span></span>

<span data-ttu-id="58586-110">レポート ウィザードでは、開発者以外の人が簡単なレポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="58586-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="58586-111">アプリが既存のプラットフォーム上に構築されていることから、この体験は、[レポート ウィザードを使用したレポートの作成、または編集](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard)で文書化された体験と同じです。</span><span class="sxs-lookup"><span data-stu-id="58586-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="58586-112">ただし、Project Service Automation 固有のエンティティを使用します。</span><span class="sxs-lookup"><span data-stu-id="58586-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="58586-113">カスタム SQL Server Reporting Service のレポート</span><span class="sxs-lookup"><span data-stu-id="58586-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="58586-114">あなたのビジネスがレポート ウィザードを使用して作成することができない特定のレポートを必要とする場合は、カスタム レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="58586-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="58586-115">Microsoft Visual Studio と、適切な Microsoft SQL Server Data Tools と Report Authoring Extension がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="58586-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="58586-116">ツール、およびバージョンの詳細については、[SQL Server Data Tools を使用したレポート作成環境](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58586-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="58586-117">カスタム レポートの作成方法に関しては、[SQL Server Data Tools を使用して新規レポートを作成する](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58586-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="58586-118">Power BI インサイト アプリケーション</span><span class="sxs-lookup"><span data-stu-id="58586-118">Power BI insights apps</span></span>

<span data-ttu-id="58586-119">Microsoft Power BI と Dynamics 365 を合わせて、インサイト アプリの形式であなたのデータと作業するためのパワフルな方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="58586-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="58586-120">インサイト アプリの可用性については、[Power BI インサイト アプリ ページ](https://powerbi.microsoft.com/power-bi-insights-apps/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58586-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="58586-121">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="58586-121">Additional resources</span></span>
<span data-ttu-id="58586-122">PSA でのレポート作成については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58586-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="58586-123">Project Service のデータ モデルでの作業</span><span class="sxs-lookup"><span data-stu-id="58586-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="58586-124">ダッシュボード</span><span class="sxs-lookup"><span data-stu-id="58586-124">Dashboards</span></span>](reports-dashboards.md)

