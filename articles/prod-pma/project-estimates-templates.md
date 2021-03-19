---
title: Project Service Automation から Finance and Operations へのプロジェクト見積もりの直接同期
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト時間の見積もりおよびプロジェクト経費の見積もりを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289465"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0508e-103">Project Service Automation から Finance and Operations へのプロジェクト見積もりの直接同期</span><span class="sxs-lookup"><span data-stu-id="0508e-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0508e-104">このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト時間の見積もりおよびプロジェクト経費の見積もりを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0508e-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="0508e-105">プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="0508e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="0508e-106">実績の統合は、バージョン 8.0.1 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0508e-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="0508e-107">Project Service Automation から Finance へのデータ フロー</span><span class="sxs-lookup"><span data-stu-id="0508e-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="0508e-108">Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="0508e-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="0508e-109">データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト時間の見積もりおよびプロジェクト経費の見積もりに関するデータのフローが可能になります。</span><span class="sxs-lookup"><span data-stu-id="0508e-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0508e-110">次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0508e-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="0508e-111">[![Finance との Project Service Automation 統合用データ フロー](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="0508e-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="0508e-112">プロジェクト時間の見積もり</span><span class="sxs-lookup"><span data-stu-id="0508e-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="0508e-113">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="0508e-113">Template and tasks</span></span>

<span data-ttu-id="0508e-114">利用可能なテンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0508e-115">以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト時間の見積もりを同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0508e-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="0508e-116">**データ統合のテンプレートの名前:** プロジェクト時間の見積もり (PSA から Finance and Operation へ)</span><span class="sxs-lookup"><span data-stu-id="0508e-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0508e-117">**プロジェクトのタスクの名前:**</span><span class="sxs-lookup"><span data-stu-id="0508e-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="0508e-118">トランザクションの関連付け</span><span class="sxs-lookup"><span data-stu-id="0508e-118">Transaction relationships</span></span>
    - <span data-ttu-id="0508e-119">経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="0508e-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="0508e-120">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="0508e-120">Entity set</span></span>

| <span data-ttu-id="0508e-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0508e-121">Project Service Automation</span></span> | <span data-ttu-id="0508e-122">財務</span><span class="sxs-lookup"><span data-stu-id="0508e-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0508e-123">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="0508e-123">Project tasks</span></span>              | <span data-ttu-id="0508e-124">プロジェクト時間の見積もりの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="0508e-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="0508e-125">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="0508e-125">Entity flow</span></span>

<span data-ttu-id="0508e-126">プロジェクト時間の見積もりは Project Service Automation で管理され、プロジェクト時間の予測として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="0508e-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0508e-127">前提条件</span><span class="sxs-lookup"><span data-stu-id="0508e-127">Prerequisites</span></span>

<span data-ttu-id="0508e-128">プロジェクト時間の見積もりを同期する前に、プロジェクト、プロジェクト タスク、およびプロジェクト経費のトランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0508e-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="0508e-129">Power Query</span></span>

<span data-ttu-id="0508e-130">プロジェクト時間の見積もりテンプレートでは、Microsoft Power Query for Excel を使用して次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="0508e-131">統合が新しい時間予測を作成するときに使用される既定の予測モデル ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="0508e-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="0508e-132">時間予測への統合に失敗するタスクで、リソース固有の任意のレコードを除外します。</span><span class="sxs-lookup"><span data-stu-id="0508e-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="0508e-133">空のトランザクション カテゴリ行をすべて除外します。</span><span class="sxs-lookup"><span data-stu-id="0508e-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="0508e-134">このタスクを完了しないと、時間予測が不正確になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="0508e-135">既定の予測モデル ID の設定</span><span class="sxs-lookup"><span data-stu-id="0508e-135">Set the default forecast model ID</span></span>

<span data-ttu-id="0508e-136">テンプレートで既定の予測モデル ID を更新するには、**マップ** 矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="0508e-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0508e-137">次に、**高度なクエリとフィルター処理** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="0508e-138">既定のプロジェクト時間の見積もり (PSA から Finance and Operation へ) テンプレートを使用している場合は、**適用したステップ** の一覧で **挿入した条件** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="0508e-139">**関数** エントリで、**O\_forecast** を統合で使用する予測モデル ID の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0508e-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="0508e-140">既定のテンプレートには、デモ データからの予測モデル ID があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="0508e-141">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="0508e-142">Power Query で、**条件列の追加** を選択し、**ModelID** などの新しい列の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0508e-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="0508e-143">列の条件を入力します。プロジェクトタスクが null でなければ、\<enter the forecast model ID\> します。それ以外の場合は null です。</span><span class="sxs-lookup"><span data-stu-id="0508e-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="0508e-144">リソース固有のレコードを除外する</span><span class="sxs-lookup"><span data-stu-id="0508e-144">Filter out resource-specific records</span></span>

<span data-ttu-id="0508e-145">プロジェクト時間の見積もり (PSA から Finance and Operation へ) テンプレートには、リソース固有のレコードを削除する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="0508e-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="0508e-146">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="0508e-147">**msdyn\_islinetask** 列でフィルター処理する **高度なクエリとフィルター処理** リンクを選択して、**False** レコードのみが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="0508e-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="0508e-148">空のトランザクション カテゴリ行を除外する</span><span class="sxs-lookup"><span data-stu-id="0508e-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="0508e-149">フィルターを追加して、空のトランザクション カテゴリがある行をすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="0508e-150">既定のテンプレートを使用しているか、または独自のテンプレートを作成しているかどうかに関係なく、このタスクは必要です。</span><span class="sxs-lookup"><span data-stu-id="0508e-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="0508e-151">このフィルターは Project Service Automation から概要行をすべて削除します。これにより、Finance の時間予測が不正確になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="0508e-152">**高度なクエリとフィルー処理** リンクを選択して、**msdyn\_transactioncategory\_value** 列で null レコードを除外します。</span><span class="sxs-lookup"><span data-stu-id="0508e-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0508e-153">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="0508e-153">Template mapping in Data integration</span></span>

<span data-ttu-id="0508e-154">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0508e-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="0508e-155">マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0508e-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0508e-156">[![データ統合におけるテンプレート タスク マッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0508e-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="0508e-157">プロジェクト経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="0508e-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="0508e-158">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="0508e-158">Template and tasks</span></span>

<span data-ttu-id="0508e-159">以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト経費の見積もりを同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0508e-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="0508e-160">**データ統合のテンプレートの名前:** プロジェクト経費の見積もり (PSA から Finance and Operation へ)</span><span class="sxs-lookup"><span data-stu-id="0508e-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0508e-161">**プロジェクトのタスクの名前:**</span><span class="sxs-lookup"><span data-stu-id="0508e-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="0508e-162">トランザクションの関連付け</span><span class="sxs-lookup"><span data-stu-id="0508e-162">Transaction relationships</span></span> 
    - <span data-ttu-id="0508e-163">経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="0508e-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="0508e-164">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="0508e-164">Entity set</span></span>

| <span data-ttu-id="0508e-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0508e-165">Project Service Automation</span></span> | <span data-ttu-id="0508e-166">財務</span><span class="sxs-lookup"><span data-stu-id="0508e-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="0508e-167">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="0508e-167">Transaction Connections</span></span>    | <span data-ttu-id="0508e-168">プロジェクト トランザクションの関連性における統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="0508e-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="0508e-169">見積行</span><span class="sxs-lookup"><span data-stu-id="0508e-169">Estimate Lines</span></span>             | <span data-ttu-id="0508e-170">プロジェクト経費の見積もりの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="0508e-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="0508e-171">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="0508e-171">Entity flow</span></span>

<span data-ttu-id="0508e-172">プロジェクト経費の見積もりは Project Service Automation で管理され、プロジェクト経費の予測として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="0508e-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0508e-173">前提条件</span><span class="sxs-lookup"><span data-stu-id="0508e-173">Prerequisites</span></span>

<span data-ttu-id="0508e-174">プロジェクト経費の見積もりを同期する前に、プロジェクト、プロジェクト タスク、およびプロジェクト経費のトランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0508e-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="0508e-175">Power Query</span></span>

<span data-ttu-id="0508e-176">プロジェクト経費の見積もりテンプレートでは、Power Query を使用して次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="0508e-177">経費見積行レコードのみを含めるようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="0508e-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="0508e-178">統合が新しい時間予測を作成するときに使用される既定の予測モデル ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="0508e-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="0508e-179">請求タイプを変換します。</span><span class="sxs-lookup"><span data-stu-id="0508e-179">Transform the billing types.</span></span>
- <span data-ttu-id="0508e-180">トランザクション タイプを変換します。</span><span class="sxs-lookup"><span data-stu-id="0508e-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="0508e-181">経費見積品目のみを含めるようにフィルター処理します</span><span class="sxs-lookup"><span data-stu-id="0508e-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="0508e-182">プロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートには、統合に経費品目のみを含む既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="0508e-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="0508e-183">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="0508e-184">**トランザクションの関連付け** タスクを選択してから、**マップ** 矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="0508e-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0508e-185">**高度なクエリとフィルター処理** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="0508e-186">**msdyn\_transactiontype1** 列をフィルター処理して、**msdyn\_estimateline** のみが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="0508e-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="0508e-187">既定の予測モデル ID の設定</span><span class="sxs-lookup"><span data-stu-id="0508e-187">Set the default forecast model ID</span></span>

<span data-ttu-id="0508e-188">テンプレートで既定の予測モデル ID を更新するには、**経費の見積もり** タスクを選択してから、**マップ** 矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="0508e-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0508e-189">**高度なクエリとフィルター処理** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="0508e-190">既定のプロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートを使用している場合は、Power Query で、**適用したステップ** セクションから最初に **挿入した条件** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="0508e-191">**関数** エントリで、**O\_forecast** を統合で使用する予測モデル ID の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0508e-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="0508e-192">既定のテンプレートには、デモ データからの予測モデル ID があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="0508e-193">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="0508e-194">Power Query で、**条件列の追加** を選択し、**ModelID** などの新しい列の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0508e-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="0508e-195">列の条件を入力します。見積り行 IDが null でなければ、\<enter the forecast model ID\> します。それ以外の場合は null です。</span><span class="sxs-lookup"><span data-stu-id="0508e-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="0508e-196">請求タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="0508e-196">Transform the billing types</span></span>

<span data-ttu-id="0508e-197">プロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートには、統合中に Project Service Automation から受け取る請求タイプを変換するために使用する条件列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0508e-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="0508e-198">独自のテンプレートを作成する場合は、この条件列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="0508e-199">**高度なクエリとフィルター処理** リンクを選択してから、**条件列の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="0508e-200">**BillingType** などの新しい列の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0508e-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="0508e-201">次に以下の条件を入力します:</span><span class="sxs-lookup"><span data-stu-id="0508e-201">Then enter the following condition:</span></span>

<span data-ttu-id="0508e-202">**msdyn\_billingtype** = 192350000 の場合、**NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="0508e-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="0508e-203">**msdyn\_billingtype** = 192350001 の場合、**請求可能**</span><span class="sxs-lookup"><span data-stu-id="0508e-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="0508e-204">**msdyn\_billingtype** = 192350002 の場合、**無料**</span><span class="sxs-lookup"><span data-stu-id="0508e-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="0508e-205">それ以外は **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="0508e-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="0508e-206">トランザクション タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="0508e-206">Transform the transaction types</span></span>

<span data-ttu-id="0508e-207">プロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートには、統合中に Project Service Automation から受け取るトランザクション タイプを変換するために使用する条件列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0508e-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="0508e-208">独自のテンプレートを作成する場合は、この条件列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0508e-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="0508e-209">**高度なクエリとフィルター処理** リンクを選択してから、**条件列の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0508e-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="0508e-210">**TransactionType** などの新しい列の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0508e-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="0508e-211">次に以下の条件を入力します:</span><span class="sxs-lookup"><span data-stu-id="0508e-211">Then enter the following condition:</span></span>

<span data-ttu-id="0508e-212">**msdyn\_transactiontypecode** = 192350000 の場合、**コスト**</span><span class="sxs-lookup"><span data-stu-id="0508e-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="0508e-213">**msdyn\_transactiontypecode** = 192350005 の場合、**営業**</span><span class="sxs-lookup"><span data-stu-id="0508e-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="0508e-214">それ以外は **null**</span><span class="sxs-lookup"><span data-stu-id="0508e-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0508e-215">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="0508e-215">Template mapping in Data integration</span></span>

<span data-ttu-id="0508e-216">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0508e-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="0508e-217">マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0508e-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0508e-218">[![経費見積もりトランザクションのテンプレートマッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0508e-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="0508e-219">[![経費見積もりのテンプレートマッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0508e-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]