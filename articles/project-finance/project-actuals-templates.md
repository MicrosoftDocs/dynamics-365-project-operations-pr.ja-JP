---
title: Finance and Operations に転記するため、プロジェクトの実績を Project Service Automation から直接プロジェクト総合ジャーナルへ同期する
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Finance and Operations へプロジェクトの実績を直接同期するために、使用されるテンプレートと基礎となるタスクについて説明しています。
author: KimANelson
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
ms.assetid: 02ae4986-8e7b-4abe-97d3-cff0904d84de
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7e5aff102226e5eac2ba3de17407eaa4461cd1ac
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752882"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="39e1e-103">Finance and Operations に転記するため、プロジェクトの実績を Project Service Automation から直接プロジェクト総合ジャーナルへ同期する</span><span class="sxs-lookup"><span data-stu-id="39e1e-103">Synchronize project actuals directly from Project Service Automation to the project integration journal for posting in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39e1e-104">このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へプロジェクトの実績を直接同期するために、使用されるテンプレートと基礎となるタスクについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

<span data-ttu-id="39e1e-105">テンプレートは、Project Service Automation からのトランザクションを Finance のステージング テーブルに同期します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-105">The template synchronizes transactions from Project Service Automation into a staging table in Finance.</span></span> <span data-ttu-id="39e1e-106">同期が完了すると、ステージング テーブルから統合ジャーナルにデータをインポートする**必要**があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-106">After synchronization is completed, you **must** import the data from the staging table into the integration journal.</span></span>

> [!NOTE]
> - <span data-ttu-id="39e1e-107">プロジェクト実績の統合は、バージョン 8.0.1 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-107">Project actuals integration is available starting in version 8.0.1.</span></span>
> - <span data-ttu-id="39e1e-108">KB 4132657 および KB 4132660 をインストールした後で、Enterprise Edition 7.3.0 を使用している場合は、テンプレートを使用してプロジェクト タスク、経費トランザクション カテゴリ、時間見積もり、経費見積もり、および実績を統合して機能ロックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-108">If you're using Enterprise edition 7.3.0 after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="39e1e-109">勘定配布をリセットする必要がある場合は、サポート情報 4131710 をインストールすることもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="39e1e-109">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="39e1e-110">バージョン 7.3.0 を使用していて、Project Service Automation から料金のトランザクションを引き継いでいる場合、プロジェクト請求書にこれらの料金を含めるために、KB 4345320 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-110">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="39e1e-111">Project Service Automation にて、時間または費用トランザクションに消費税額を入力する場合は、Project Service Automation Update 7 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-111">If you're entering sales tax amounts on time or expense transactions in Project Service Automation, you must install Project Service Automation Update 7.</span></span> <span data-ttu-id="39e1e-112">そうでない場合、税の実績は関連する時間または費用の実績にリンクされず、Finance に同期されません。</span><span class="sxs-lookup"><span data-stu-id="39e1e-112">Otherwise, the tax actuals won't be linked to the associated time or expense actuals, and they won't be synchronized to Finance.</span></span> <span data-ttu-id="39e1e-113">詳細については Support にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="39e1e-113">For more information, contact Support.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="39e1e-114">Project Service Automation から Finance へのデータ フロー</span><span class="sxs-lookup"><span data-stu-id="39e1e-114">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="39e1e-115">Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-115">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="39e1e-116">データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクトの実績に関するデータ フローが可能になります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-116">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance.</span></span>

<span data-ttu-id="39e1e-117">次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-117">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="39e1e-118">[![Finance and Operations との Project Service Automation 統合用データ フロー](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="39e1e-118">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>

## <a name="project-actuals-from-project-service-automation"></a><span data-ttu-id="39e1e-119">Project Service Automation からのプロジェクトの実績</span><span class="sxs-lookup"><span data-stu-id="39e1e-119">Project actuals from Project Service Automation</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="39e1e-120">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="39e1e-120">Template and tasks</span></span>

<span data-ttu-id="39e1e-121">利用可能なテンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト**を選択してから、右上隅で**新しいプロジェクト**を選択して公開テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-121">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="39e1e-122">以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクトの実績を同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-122">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="39e1e-123">**データ統合のテンプレート名:** プロジェクトの実績 (PSA から Fin および Ops へ)</span><span class="sxs-lookup"><span data-stu-id="39e1e-123">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="39e1e-124">**プロジェクトのタスクの名前:**</span><span class="sxs-lookup"><span data-stu-id="39e1e-124">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="39e1e-125">実績</span><span class="sxs-lookup"><span data-stu-id="39e1e-125">Actuals</span></span>
    - <span data-ttu-id="39e1e-126">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="39e1e-126">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="39e1e-127">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="39e1e-127">Entity set</span></span>

| <span data-ttu-id="39e1e-128">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39e1e-128">Project Service Automation</span></span> | <span data-ttu-id="39e1e-129">財務</span><span class="sxs-lookup"><span data-stu-id="39e1e-129">Finance</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="39e1e-130">実績</span><span class="sxs-lookup"><span data-stu-id="39e1e-130">Actuals</span></span>                    | <span data-ttu-id="39e1e-131">プロジェク実績の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="39e1e-131">Integration entity for project actuals</span></span>                   |
| <span data-ttu-id="39e1e-132">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="39e1e-132">Transaction Connections</span></span>    | <span data-ttu-id="39e1e-133">プロジェクト トランザクションの関連性における統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="39e1e-133">Integration entity for project transaction relationships</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="39e1e-134">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="39e1e-134">Entity flow</span></span>

<span data-ttu-id="39e1e-135">プロジェクトの実績は、Project Service Automation で管理され、Finance のプロジェクト統合ジャーナルに同期されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-135">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="39e1e-136">会計は、デフォルトの財務分析コードと転記設定に基づいて適用されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-136">The accounting will be applied based on default financial dimensions and the posting setup.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="39e1e-137">前提条件</span><span class="sxs-lookup"><span data-stu-id="39e1e-137">Prerequisites</span></span>

<span data-ttu-id="39e1e-138">実績の同期を行う前に、Project Service Automation 統合パラメーターを構成し、プロジェクト、プロジェクト タスク、およびプロジェクト費用トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-138">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="39e1e-139">Power Query</span><span class="sxs-lookup"><span data-stu-id="39e1e-139">Power Query</span></span>

<span data-ttu-id="39e1e-140">プロジェクトの実績テンプレートでは、Microsoft Power Query for Excel を使用して次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-140">In the project actuals template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="39e1e-141">Project Service Automation のトランザクション タイプを、Finance の正しいトランザクション タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-141">Transform the transaction type in Project Service Automation to the correct transaction type in Finance.</span></span> <span data-ttu-id="39e1e-142">この変換は、プロジェクト実績 (PSA から Fin および Ops へ) テンプレートですでに定義されています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-142">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span>
- <span data-ttu-id="39e1e-143">Project Service Automation の請求タイプを、Finance の正しい請求タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-143">Transform the billing type in Project Service Automation to the correct billing type in Finance.</span></span> <span data-ttu-id="39e1e-144">この変換は、プロジェクト実績 (PSA から Fin および Ops へ) テンプレートですでに定義されています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-144">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="39e1e-145">次に、請求タイプは明細行プロパティにマップされ、**Project Service Automation 統合パラメーター**ページの設定に基づきます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-145">The billing type is then mapped to the line property, based on the configuration on the **Project Service Automation integration parameters** page.</span></span>
- <span data-ttu-id="39e1e-146">このテンプレートと同期する必要がある特定のリソース組織単位にフィルターします。</span><span class="sxs-lookup"><span data-stu-id="39e1e-146">Filter to specific resource organizational units that must be synchronized with this template.</span></span>
- <span data-ttu-id="39e1e-147">会社間の時間または会社間の費用の実績が Finance に同期される場合は、契約組織単位を Finance の正しい法人に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-147">If intercompany time or intercompany expense actuals will be synchronized to Finance, you must transform the contract organizational unit to the correct legal entity in Finance.</span></span> <span data-ttu-id="39e1e-148">プロジェクト実績 (PSA から Fin および Ops へ) テンプレートでは、条件付きの列がデモ データに基づいて定義されています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-148">In the Project actuals (PSA to Fin and Ops) template, a conditional column is defined based on demo data.</span></span> <span data-ttu-id="39e1e-149">最後に挿入された条件付き列を正しい法人に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-149">You must update the last inserted conditional column to the correct legal entities.</span></span> <span data-ttu-id="39e1e-150">そうしないと、統合エラーが発生するか、または誤った実際のトランザクションが Finance にインポートされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-150">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>
- <span data-ttu-id="39e1e-151">会社間の時間または会社間の費用の実績が Finance に同期されない場合は、最後に挿入された条件付き列をテンプレートから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-151">If intercompany time or intercompany expense actuals won't be synchronized to Finance, you must delete the last inserted conditional column from your template.</span></span> <span data-ttu-id="39e1e-152">そうしないと、統合エラーが発生するか、または誤った実際のトランザクションが Finance にインポートされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-152">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>

#### <a name="contract-organizational-unit"></a><span data-ttu-id="39e1e-153">契約組織の単位</span><span class="sxs-lookup"><span data-stu-id="39e1e-153">Contract organizational unit</span></span>
<span data-ttu-id="39e1e-154">テンプレートで挿入された条件付き列を更新するには、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-154">To update the inserted conditional column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="39e1e-155">**高度なクエリとフィルター処理**リンクを選択し、Power Query を開きます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-155">Select the **Advanced Query and Filtering** link to open Power Query.</span></span>

- <span data-ttu-id="39e1e-156">既定のプロジェクト実績 (PSA から Fin と Ops へ) テンプレートを使用している場合は、Power Query で、**適用したステップ**セクションから最後に**挿入した条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-156">If you're using the default Project actuals (PSA to Fin and Ops) template, in Power Query, select the last **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="39e1e-157">**関数**エントリで、**USSI** を統合で使用する法人名に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-157">In the **Function** entry, replace **USSI** with the name of the legal entity that should be used with the integration.</span></span> <span data-ttu-id="39e1e-158">必要に応じて、条件を**関数**にエントリに追加し、**USMF** から正しい法人に**他の**条件を更新します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-158">Add additional conditions to the **Function** entry as you require, and update the **else** condition from **USMF** to the correct legal entity.</span></span>
- <span data-ttu-id="39e1e-159">新しいテンプレートを作成する場合は、会社間の時間と費用をサポートするために列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-159">If you're creating a new template, you must add the column to support intercompany time and expenses.</span></span> <span data-ttu-id="39e1e-160">**条件列の追加**を選択し、**LegalEntity** などの列の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-160">Select **Add Conditional Column**, and enter a name for the column, such as **LegalEntity**.</span></span> <span data-ttu-id="39e1e-161">**msdyn\_contractorganizationalunitid.msdyn\_name** が \<organizational unit\> の場合は、 \<enter the legal entity\>、それ以外は null、と列の条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-161">Enter a condition for the column, where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="39e1e-162">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="39e1e-162">Template mapping in Data integration</span></span>

<span data-ttu-id="39e1e-163">次の図は、データ統合のテンプレート タスク マッピングの一例を示しています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-163">The following illustrations show an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="39e1e-164">マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-164">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="39e1e-165">[![テンプレート マッピング](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="39e1e-165">[![Template mapping](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="39e1e-166">[![テンプレート マッピング](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="39e1e-166">[![Template mapping](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a><span data-ttu-id="39e1e-167">Project Service Automation からの統合後のステージング テーブルからのインポート</span><span class="sxs-lookup"><span data-stu-id="39e1e-167">Import from staging table after integration from Project Service Automation</span></span>

<span data-ttu-id="39e1e-168">ステージング テーブルからの定期的なインポート プロセスは、Project Service Automation から Finance への実績の同期後に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-168">The Import from staging table periodic process must be run after the synchronization of actuals from Project Service Automation to Finance.</span></span> <span data-ttu-id="39e1e-169">このプロセスでは、プロジェクト トランザクションがステージング テーブルから Project Service Automation 統合ジャーナルにインポートされます。ここで、アカウンティングが適用され、インポートされたトランザクションを転記できます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-169">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="39e1e-170">このプロセスはバッチ モードで実行することをお勧めします。オプションで、定期バッチとして実行するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-170">We recommend that you run this process in batch mode; it can optionally be set up to run as a recurring batch.</span></span>

## <a name="update-actuals-from-finance"></a><span data-ttu-id="39e1e-171">Finance からの実績を更新</span><span class="sxs-lookup"><span data-stu-id="39e1e-171">Update actuals from Finance</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="39e1e-172">テンプレートとタスク</span><span class="sxs-lookup"><span data-stu-id="39e1e-172">Template and tasks</span></span>

<span data-ttu-id="39e1e-173">次のテンプレートと基になるタスクを使用して、転記されたプロジェクト トランザクションのバウチャー番号と売上税を、Finance から Project Service Automation に同期します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-173">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="39e1e-174">**データ統合のテンプレート名:** プロジェクト実績の更新 (Fin Ops から PSA へ)</span><span class="sxs-lookup"><span data-stu-id="39e1e-174">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
- <span data-ttu-id="39e1e-175">**プロジェクトのタスクの名前:**</span><span class="sxs-lookup"><span data-stu-id="39e1e-175">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="39e1e-176">実績</span><span class="sxs-lookup"><span data-stu-id="39e1e-176">Actuals</span></span> 
    - <span data-ttu-id="39e1e-177">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="39e1e-177">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="39e1e-178">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="39e1e-178">Entity set</span></span>

| <span data-ttu-id="39e1e-179">財務</span><span class="sxs-lookup"><span data-stu-id="39e1e-179">Finance</span></span>                                                  | <span data-ttu-id="39e1e-180">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39e1e-180">Project Service Automation</span></span> |
|----------------------------------------------------------|----------------------------|
| <span data-ttu-id="39e1e-181">プロジェク実績の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="39e1e-181">Integration entity for project actuals</span></span>                   | <span data-ttu-id="39e1e-182">実績</span><span class="sxs-lookup"><span data-stu-id="39e1e-182">Actuals</span></span>                    |
| <span data-ttu-id="39e1e-183">プロジェクト トランザクションの関連性における統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="39e1e-183">Integration entity for project transaction relationships</span></span> | <span data-ttu-id="39e1e-184">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="39e1e-184">Transaction Connections</span></span>    |

### <a name="entity-flow"></a><span data-ttu-id="39e1e-185">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="39e1e-185">Entity flow</span></span>

<span data-ttu-id="39e1e-186">プロジェクトの実績は、Project Service Automation で管理され、Finance のプロジェクト統合ジャーナルに同期されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-186">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="39e1e-187">実績が Finance に転記された後、Project Service Automation にて、Finance からのバウチャー番号を使い更新されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-187">After actuals are posted in Finance, they are updated in Project Service Automation with the voucher number from Finance.</span></span> <span data-ttu-id="39e1e-188">売上税が Finance に追加された場合、新しい税の実績が Project Service Automation で作成されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-188">If sales taxes were added in Finance, new tax actuals are created in Project Service Automation.</span></span>

### <a name="power-query"></a><span data-ttu-id="39e1e-189">Power Query</span><span class="sxs-lookup"><span data-stu-id="39e1e-189">Power Query</span></span>

<span data-ttu-id="39e1e-190">プロジェクト実績の更新テンプレートでは、Power Query を使用して次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e1e-190">In the project actuals update template, you must use Power Query to complete these tasks:</span></span>

- <span data-ttu-id="39e1e-191">Finance のトランザクション タイプを、Project Service Automation で正しいトランザクション タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-191">Transform the transaction type in Finance to the correct transaction type in Project Service Automation.</span></span> <span data-ttu-id="39e1e-192">この変換は、プロジェクト実績の更新 (Fin Ops から PSA へ) テンプレートですでに定義されています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-192">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>
- <span data-ttu-id="39e1e-193">Finance の請求タイプを、Project Service Automation の正しい請求タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="39e1e-193">Transform the billing type in Finance to the correct billing type in Project Service Automation.</span></span> <span data-ttu-id="39e1e-194">この変換は、プロジェクト実績の更新 (Fin Ops から PSA へ) テンプレートですでに定義されています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-194">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="39e1e-195">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="39e1e-195">Template mapping in Data integration</span></span>

<span data-ttu-id="39e1e-196">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="39e1e-196">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="39e1e-197">マッピングには、Finance から Project Service Automation に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="39e1e-197">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="39e1e-198">[![テンプレート マッピング](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="39e1e-198">[![Template mapping](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="39e1e-199">[![テンプレート マッピング](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="39e1e-199">[![Template mapping](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>
