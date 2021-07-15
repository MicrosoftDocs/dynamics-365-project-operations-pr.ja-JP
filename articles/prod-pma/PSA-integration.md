---
title: Project Service Automation の概要
description: このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance への統合ソリューションについて説明します。
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369625"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="d88c7-103">Project Service Automation の概要</span><span class="sxs-lookup"><span data-stu-id="d88c7-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d88c7-104">Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Dynamics 365 Finance および Dynamics 365 Project Service Automation のインスタンス間で、Common Data Service を経由してデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="d88c7-105">データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance への、プロジェクト、プロジェクト契約、プロジェクト契約品目、プロジェクト契約品目のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間の見積もり、および経費の見積もりのフローを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d88c7-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="d88c7-106">バージョン 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="d88c7-107">その後、固定価格プロジェクトを統合できます。</span><span class="sxs-lookup"><span data-stu-id="d88c7-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="d88c7-108">バージョン 7.3.0 を使用していて、Project Service Automation から料金のトランザクションを引き継いでいる場合、プロジェクト請求書にこれらの料金を含めるために、KB 4345320 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="d88c7-109">バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、費用の見積もり、および機能のロックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d88c7-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="d88c7-110">バージョン 8.0.1 以降を使用している場合は、実績を同期することができます。</span><span class="sxs-lookup"><span data-stu-id="d88c7-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="d88c7-111">Project Service Automation Finance を統合する前に、Project Service Automation 統合パラメーターを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="d88c7-112">詳細については、[Project Service Automation 統合パラメーター](PSA-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d88c7-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="d88c7-113">この統合ソリューションにより、次のシナリオで直接同期が可能になります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="d88c7-114">Project Service Automation でプロジェクト契約を維持して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-115">Project Service Automation でプロジェクトを作成して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-116">Project Service Automation でプロジェクト契約品目を維持して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-117">Project Service Automation でプロジェクト契約品目のマイルストーンを維持して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-118">Project Service Automation でプロジェクト タスクを維持して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-119">Finance で経費トランザクション カテゴリを維持して、Finance から Project Service Automation に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="d88c7-120">Project Service Automation でプロジェクト時間の見積もりを作成して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-121">Project Service Automation でプロジェクト経費の見積もりを作成して、Project Service Automation から Finance に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="d88c7-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d88c7-122">Project Service Automation でプロジェクト時間、費用、料金の実績を作成し、Project Service Automation 統合ジャーナルでプロジェクト トランザクションを作成して、Finance に転記できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d88c7-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="d88c7-123">データの同期</span><span class="sxs-lookup"><span data-stu-id="d88c7-123">Data synchronization</span></span>

<span data-ttu-id="d88c7-124">次の図は、Project Service Automation と Finance の統合の一部としてデータを同期する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d88c7-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="d88c7-125">現在利用できないテンプレートもあります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-125">Not all templates are currently available.</span></span> <span data-ttu-id="d88c7-126">テンプレートは完成次第リリースされます。</span><span class="sxs-lookup"><span data-stu-id="d88c7-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="d88c7-127">[![Project Service Automation と Finance の統合](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="d88c7-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="d88c7-128">Finance のシステム要件</span><span class="sxs-lookup"><span data-stu-id="d88c7-128">System requirements for Finance</span></span>

<span data-ttu-id="d88c7-129">Project Service Automation から Finance への統合ソリューションを使用するには、Enterprise Edition 7.3 と Platform update 12 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="d88c7-130">Project Service Automation のシステム要件</span><span class="sxs-lookup"><span data-stu-id="d88c7-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="d88c7-131">Project Service Automation から Finance への統合ソリューションを使用するには、次のコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d88c7-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="d88c7-132">Dynamics 365 Project Service Automation バージョン 9.0.0.0 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="d88c7-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="d88c7-133">Dynamics 365 Sales の見込顧客の現金化、バージョン 1.14.0.0 (v14) 以降</span><span class="sxs-lookup"><span data-stu-id="d88c7-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="d88c7-134">Dynamics 365 Project Service Automation の Project Service Automation から Finance へのソリューション バージョン 1.0.0.0 以降</span><span class="sxs-lookup"><span data-stu-id="d88c7-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="d88c7-135">Project Service Automation インスタンスに、Project Service Automation から Finance への統合ソリューションをインストールする</span><span class="sxs-lookup"><span data-stu-id="d88c7-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="d88c7-136">[Microsoft ダウンロード センター](https://www.microsoft.com/download/details.aspx?id=57016)から Project Service Automation から Finance への統合ソリューションをダウンロードして、ソリューションに含まれる指示に従います。</span><span class="sxs-lookup"><span data-stu-id="d88c7-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]