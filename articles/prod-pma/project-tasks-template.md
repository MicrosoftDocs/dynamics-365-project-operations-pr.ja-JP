---
title: Project Service Automation から Finance and Operations へのプロジェクト タスクの直接同期
description: このトピックは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance へプロジェクト タスクを直接同期するために使用されるテンプレートと基礎となるタスクについて説明しています。
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 16cd38f2f190414d7be9c93e8ab90d55006f47e1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009982"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="457ff-103">Project Service Automation から Finance and Operations へのプロジェクト タスクの直接同期</span><span class="sxs-lookup"><span data-stu-id="457ff-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="457ff-104">このトピックは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へプロジェクト タスクを直接同期するために使用されるテンプレートと基礎となるタスクについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="457ff-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="457ff-105">プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="457ff-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="457ff-106">KB 4132657 および KB 4132660 をインストールした後で、Enterprise Edition 7.3.0 を使用している場合は、テンプレートを使用して、プロジェクト タスク、経費トランザクション カテゴリ、時間見積もり、経費見積もり、および実績を統合して機能ロックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="457ff-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="457ff-107">勘定配布をリセットする必要がある場合は、サポート情報 4131710 をインストールすることもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="457ff-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="457ff-108">実績の統合は、バージョン 8.0.1 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="457ff-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="457ff-109">Project Service Automation から Finance へのデータ フロー</span><span class="sxs-lookup"><span data-stu-id="457ff-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="457ff-110">Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="457ff-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="457ff-111">データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト タスクに関するデータ フローが可能になります。</span><span class="sxs-lookup"><span data-stu-id="457ff-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="457ff-112">次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="457ff-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="457ff-113">[![Project Service Automation と Finance の統合用データ フロー](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="457ff-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="457ff-114">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="457ff-114">Template and task</span></span>

<span data-ttu-id="457ff-115">テンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="457ff-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="457ff-116">以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト タスクを同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="457ff-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="457ff-117">**データ統合のテンプレートの名前:** プロジェクト タスク (PSA から Finance and Operation へ)</span><span class="sxs-lookup"><span data-stu-id="457ff-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="457ff-118">**プロジェクトのタスクの名前:** プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="457ff-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="457ff-119">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="457ff-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="457ff-120">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="457ff-120">Entity set</span></span>

| <span data-ttu-id="457ff-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="457ff-121">Project Service Automation</span></span> | <span data-ttu-id="457ff-122">財務</span><span class="sxs-lookup"><span data-stu-id="457ff-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="457ff-123">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="457ff-123">Project Tasks</span></span>              | <span data-ttu-id="457ff-124">プロジェクト タスクの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="457ff-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="457ff-125">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="457ff-125">Entity flow</span></span>

<span data-ttu-id="457ff-126">プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="457ff-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="457ff-127">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="457ff-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="457ff-128">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="457ff-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="457ff-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="457ff-129">Power Query</span></span>

<span data-ttu-id="457ff-130">この条件が満たされている場合、Microsoft Power Query for Excel を使用してデータをフィルター処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="457ff-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="457ff-131">プロジェクト タスクにリソース固有のレコードがあります。</span><span class="sxs-lookup"><span data-stu-id="457ff-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="457ff-132">Power Query を使用する必要がある場合は、このガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="457ff-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="457ff-133">プロジェクト タスク (PSA から Finance and Operation へ) テンプレートには、フィルターを **IsLineTask** から **False** に設定することで、プロジェクト タスクからリソース固有のレコードを除外する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="457ff-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="457ff-134">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="457ff-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="457ff-135">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="457ff-135">Template mapping in Data integration</span></span>

<span data-ttu-id="457ff-136">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="457ff-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="457ff-137">マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="457ff-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="457ff-138">[![テンプレート マッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="457ff-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]