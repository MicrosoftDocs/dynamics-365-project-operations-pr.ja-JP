---
title: プロジェクト経費カテゴリを Finance and Operations と Project Service Automation 間で同期する
description: このトピックは、Microsoft Dynamics 365 Finance と Dynamics 365 Project Service Automation 間でプロジェクト経費カテゴリを直接同期するために使用されるテンプレートおよび基礎となるタスクについて説明しています。
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079407"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="6c611-103">プロジェクト経費カテゴリを Finance and Operations と Project Service Automation 間で同期する</span><span class="sxs-lookup"><span data-stu-id="6c611-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6c611-104">このトピックは、Dynamics 365 Finance と Dynamics 365 Project Service Automation 間でプロジェクト経費カテゴリを直接同期するために、使用されるテンプレートおよび基礎となるタスクについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="6c611-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="6c611-105">プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6c611-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="6c611-106">実績の統合は、バージョン 8.0.1 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c611-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="6c611-107">KB 4132657 および KB 4132660 をインストールした後で、Enterprise Edition 7.3.0 を使用している場合は、テンプレートを使用して、プロジェクト タスク、経費トランザクション カテゴリ、時間見積もり、経費見積もり、および実績を統合して機能ロックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6c611-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="6c611-108">勘定配布をリセットする必要がある場合は、サポート情報 4131710 をインストールすることもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6c611-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="6c611-109">Project Service Automation と Finance のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="6c611-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="6c611-110">Project Service Automation と Finance の統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="6c611-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="6c611-111">データ統合機能で使用可能な統合テンプレートを使用すると、Finance と Project Service Automation 間のプロジェクト経費トランザクションに関するデータのフローが可能になります。</span><span class="sxs-lookup"><span data-stu-id="6c611-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="6c611-112">プロジェクト経費カテゴリが Finance で習得されている場合、統合フローは最初 Finance から Project Service Automation までです。</span><span class="sxs-lookup"><span data-stu-id="6c611-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="6c611-113">そして、プロジェクト経費カテゴリの統合 ID が Project Service Automation から Finance へ同期によって更新されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="6c611-114">プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初 Project Service Automation から Finance までです。</span><span class="sxs-lookup"><span data-stu-id="6c611-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="6c611-115">プロジェクト カテゴリは、Project Service Automation から同期する前に、Finance で既に構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="6c611-116">その後、Finance から Project Service Automation に戻り同期を実行し、Project Service Automation から Finance に再度同期します。</span><span class="sxs-lookup"><span data-stu-id="6c611-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="6c611-117">このようにして、カテゴリがリンクされ、重複が作成されないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6c611-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="6c611-118">通常、プロジェクト経費カテゴリは Finance で習得されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="6c611-119">ただし、そうでない場合、または経費カテゴリが既に Project Service Automation で作成されている場合は、最初にプロジェクト経費トランザクション カテゴリ (PSA から Fin および Ops へ) テンプレートを使用して同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="6c611-120">そして、プロジェクト経費トランザクション カテゴリ (Fin および Ops から PSA へ) テンプレートを使用して同期します。</span><span class="sxs-lookup"><span data-stu-id="6c611-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="6c611-121">その後、もう一度 Project Service Automation から Finance へ同期を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="6c611-122">最初に Project Service Automation から同期する場合、同期を実行する前に、Finance で次の要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="6c611-123">Project Service Automation で設定されているプロジェクト カテゴリと一致する共有カテゴリが存在し、 **プロジェクト** と **経費** の両方で有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="6c611-124">統合する必要がある Finance の法人ごとに、次のプロジェクト カテゴリが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="6c611-125">**プロジェクト カテゴリー** は存在します。</span><span class="sxs-lookup"><span data-stu-id="6c611-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="6c611-126">**経費での使用** が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="6c611-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="6c611-127">**ジャーナルでアクティブ** が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="6c611-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="6c611-128">**トランザクション タイプ** が **経費** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="6c611-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="6c611-129">次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6c611-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="6c611-130">[![Finance を使用した Project Service Automation 統合用データ フロー](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="6c611-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="6c611-131">プロジェクト経費カテゴリを Finance と Project Service Automation 間で同期</span><span class="sxs-lookup"><span data-stu-id="6c611-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="6c611-132">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="6c611-132">Template and task</span></span>

<span data-ttu-id="6c611-133">テンプレートにアクセスするには、Microsoft Power Apps 管理センターで、 **プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c611-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6c611-134">以下のテンプレートおよび基礎となるタスクは、Finance から Project Service Automation へプロジェクト経費カテゴリを同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="6c611-135">**データ統合のテンプレートの名前:** プロジェクト経費カテゴリ (Fin と Ops から PSA へ)</span><span class="sxs-lookup"><span data-stu-id="6c611-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="6c611-136">**プロジェクトのタスク名:** カテゴリを PSA に同期</span><span class="sxs-lookup"><span data-stu-id="6c611-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="6c611-137">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="6c611-137">Entity set</span></span>

| <span data-ttu-id="6c611-138">財務</span><span class="sxs-lookup"><span data-stu-id="6c611-138">Finance</span></span>                           | <span data-ttu-id="6c611-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6c611-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="6c611-140">カテゴリの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="6c611-140">Integration entity for categories</span></span> | <span data-ttu-id="6c611-141">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="6c611-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="6c611-142">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="6c611-142">Entity flow</span></span>

<span data-ttu-id="6c611-143">プロジェクト経費カテゴリは Finance で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="6c611-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="6c611-144">Power Query</span></span>

<span data-ttu-id="6c611-145">Project Service Automation に同期する場合は、Microsoft Power Query for Excel を使用して、トランザクション カテゴリに請求タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="6c611-146">プロジェクト経費のトランザクション カテゴリ (Fin と Ops から PSA へ) テンプレートは、デフォルトの列とマッピングを提供します。</span><span class="sxs-lookup"><span data-stu-id="6c611-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="6c611-147">独自のテンプレートを作成する場合は、Power Query に条件列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c611-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="6c611-148">次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c611-148">Follow these steps.</span></span>

1. <span data-ttu-id="6c611-149">矢印をクリックして、プロジェクト経費トランザクション カテゴリ (Fin と Ops から PSA へ) テンプレートで、プロジェクト経費カテゴリ タスクのマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="6c611-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="6c611-150">**高度なクエリとフィルター処理** リンクをクリックして、Power Query を開きます。</span><span class="sxs-lookup"><span data-stu-id="6c611-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="6c611-151">**条件付き列を追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c611-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="6c611-152">**BillingType** などの新しい列の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c611-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="6c611-153">次の条件を入力します: **CATEGORYID が null と等しくない場合は 19235001、そうでない場合は null** 。</span><span class="sxs-lookup"><span data-stu-id="6c611-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="6c611-154">列で **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c611-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="6c611-155">この新しい列をマッピング ページに必ずマッピングしてください。</span><span class="sxs-lookup"><span data-stu-id="6c611-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="6c611-156">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c611-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="6c611-157">マッピングには、Finance から Project Service Automation に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="6c611-158">[![プロジェクト経費カテゴリから Project Service Automation へのテンプレート マッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6c611-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="6c611-159">プロジェクト経費カテゴリを Project Service Automation から Finance へ同期</span><span class="sxs-lookup"><span data-stu-id="6c611-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="6c611-160">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="6c611-160">Template and task</span></span>

<span data-ttu-id="6c611-161">以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト経費カテゴリを同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="6c611-162">**データ統合のテンプレートの名前:** プロジェクト経費カテゴリ (PSA から Fin と Ops へ)</span><span class="sxs-lookup"><span data-stu-id="6c611-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="6c611-163">**プロジェクトのタスク名:** カテゴリを Fin Ops に同期</span><span class="sxs-lookup"><span data-stu-id="6c611-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="6c611-164">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="6c611-164">Entity set</span></span>

| <span data-ttu-id="6c611-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6c611-165">Project Service Automation</span></span> | <span data-ttu-id="6c611-166">財務</span><span class="sxs-lookup"><span data-stu-id="6c611-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="6c611-167">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="6c611-167">Transaction categories</span></span>     | <span data-ttu-id="6c611-168">カテゴリの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="6c611-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="6c611-169">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="6c611-169">Entity flow</span></span>

<span data-ttu-id="6c611-170">プロジェクト経費カテゴリは Finance で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="6c611-171">Finance に戻った同期により、Project Service Automation からの統合 ID で Finance のプロジェクト カテゴリを更新されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6c611-172">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="6c611-172">Template mapping in Data integration</span></span>

<span data-ttu-id="6c611-173">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c611-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="6c611-174">マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c611-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="6c611-175">[![Project Service Automation から Finance へのテンプレート マッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6c611-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
