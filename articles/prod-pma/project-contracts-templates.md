---
title: プロジェクト契約とプロジェクトを、Project Service Automation から Finance に直接同期します
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト契約およびプロジェクトを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。
author: Yowelle
ms.date: 12/17/2020
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 2f5fa0143c903f08b3937426805cb43d5d6109e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999812"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a><span data-ttu-id="05df2-103">プロジェクト契約とプロジェクトを、Project Service Automation から Finance に直接同期します</span><span class="sxs-lookup"><span data-stu-id="05df2-103">Synchronize project contracts and projects directly from Project Service Automation to Finance</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="05df2-104">このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト契約およびプロジェクトを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="05df2-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="05df2-105">Enterprise Edition 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="05df2-106">Project Service Automation から Finance へのデータ フロー</span><span class="sxs-lookup"><span data-stu-id="05df2-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="05df2-107">Project Service Automation から Finance への統合ソリューションを使用する前に、Dynamics 365 のデータ統合機能に精通している必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="05df2-108">Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="05df2-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="05df2-109">データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト契約、プロジェクト、プロジェクト契約品目、およびプロジェクト契約品目のマイルストーンについてのデータのフローが可能になります。</span><span class="sxs-lookup"><span data-stu-id="05df2-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="05df2-110">次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="05df2-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="05df2-111">[![Finance との Project Service Automation 統合用データ フロー](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="05df2-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="05df2-112">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="05df2-112">Templates and tasks</span></span>

<span data-ttu-id="05df2-113">利用可能なテンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="05df2-113">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="05df2-114">以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へのプロジェクト契約およびプロジェクトを同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="05df2-115">Dynamics 365 Project Service Automation v2.x との統合</span><span class="sxs-lookup"><span data-stu-id="05df2-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="05df2-116">**データ統合におけるテンプレートの名前:** プロジェクトと契約 (Project Service Automation から Finance)</span><span class="sxs-lookup"><span data-stu-id="05df2-116">**Name of the template in Data integration:** Projects and contracts (Project Service Automation to Finance)</span></span>
- <span data-ttu-id="05df2-117">**プロジェクトのタスクの名前:**</span><span class="sxs-lookup"><span data-stu-id="05df2-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="05df2-118">プロジェクト契約 Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-118">Project contracts Project Service Automation to Finance</span></span>
    - <span data-ttu-id="05df2-119">プロジェクト Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-119">Projects Project Service Automation to Finance</span></span>
    - <span data-ttu-id="05df2-120">プロジェクト契約品目 Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-120">Project contract lines Project Service Automation to Finance</span></span>
    - <span data-ttu-id="05df2-121">プロジェクト契約品目マイルストーン Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-121">Project contract line milestones Project Service Automation to Finance</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="05df2-122">Dynamics 365 Project Service Automation v3.x との統合</span><span class="sxs-lookup"><span data-stu-id="05df2-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="05df2-123">Project Service Automation にはスキーマの変更があり、プロジェクト契約品目のマイルストーン テンプレートに影響します。ProjectService Automation v3.x を Dynamics 365 と統合するには、テンプレートの v2 バージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="05df2-124">**データ統合におけるテンプレートの名前:** プロジェクトと契約 (Project Service Automation 3.x から Finance) - v2</span><span class="sxs-lookup"><span data-stu-id="05df2-124">**Name of the template in Data integration:** Projects and Contracts (Project Service Automation 3.x to Finance) - v2</span></span>
- <span data-ttu-id="05df2-125">**プロジェクトのタスクの名前:**</span><span class="sxs-lookup"><span data-stu-id="05df2-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="05df2-126">プロジェクト契約 Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-126">Project contracts Project Service Automation to Finance</span></span>
    - <span data-ttu-id="05df2-127">プロジェクト Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-127">Projects Project Service Automation to Finance</span></span>
    - <span data-ttu-id="05df2-128">プロジェクト契約品目 Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-128">Project contract lines Project Service Automation to Finance</span></span>
    - <span data-ttu-id="05df2-129">プロジェクト契約品目マイルストーン Project Service Automation から Finance</span><span class="sxs-lookup"><span data-stu-id="05df2-129">Project contract line milestones Project Service Automation to Finance</span></span>

<span data-ttu-id="05df2-130">プロジェクト契約およびプロジェクトの同期を行う前に、アカウントを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="05df2-131">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="05df2-131">Entity set</span></span>

| <span data-ttu-id="05df2-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="05df2-132">Project Service Automation</span></span>       | <span data-ttu-id="05df2-133">財務</span><span class="sxs-lookup"><span data-stu-id="05df2-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="05df2-134">受注</span><span class="sxs-lookup"><span data-stu-id="05df2-134">Orders</span></span>                           | <span data-ttu-id="05df2-135">プロジェク契約の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="05df2-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="05df2-136">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="05df2-136">Projects</span></span>                         | <span data-ttu-id="05df2-137">プロジェクトの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="05df2-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="05df2-138">受注明細行</span><span class="sxs-lookup"><span data-stu-id="05df2-138">Order lines</span></span>                      | <span data-ttu-id="05df2-139">プロジェク契約品目の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="05df2-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="05df2-140">プロジェクト契約品目のマイルストーン</span><span class="sxs-lookup"><span data-stu-id="05df2-140">Project contract line milestones</span></span> | <span data-ttu-id="05df2-141">プロジェク契約品目のマイルストーンの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="05df2-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="05df2-142">エンティティ フロー</span><span class="sxs-lookup"><span data-stu-id="05df2-142">Entity flow</span></span>

<span data-ttu-id="05df2-143">プロジェクト契約は Project Service Automation で管理され、プロジェクト契約として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="05df2-144">統合テンプレートの一部として、プロジェクト契約の統合ソースを Finance で設定できます。</span><span class="sxs-lookup"><span data-stu-id="05df2-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="05df2-145">時間と材料および固定価格のプロジェクトは、Project Service Automation で管理され、プロジェクトとして Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-145">Time and material and fixed-price projects are managed in Project Service Automation and synchronized to Finance as projects.</span></span> <span data-ttu-id="05df2-146">テンプレート統合の一部として、Finance でプロジェクトの統合ソースを設定できます。</span><span class="sxs-lookup"><span data-stu-id="05df2-146">As part of the template integration, you can set the integration source for the project in Finance.</span></span> <span data-ttu-id="05df2-147">現在、時間と材料および固定価格のプロジェクトのみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="05df2-147">Currently, only time and material and fixed-price projects are supported.</span></span>


<span data-ttu-id="05df2-148">プロジェクト契約品目は Project Service Automation で管理され、プロジェクト契約の請求ルールとして Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-148">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="05df2-149">請求方法が既定のプロジェクト タイプと異なる場合、同期により、契約品目プロジェクトとプロジェクト グループのプロジェクト タイプが更新されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-149">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="05df2-150">プロジェクト契約品目のマイルストーンは Project Service Automation で管理され、プロジェクト契約の請求ルール マイルストーンとして Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-150">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="05df2-151">Project Service Automation から Finance への統合ソリューション</span><span class="sxs-lookup"><span data-stu-id="05df2-151">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="05df2-152">**プロジェクト契約 ID** フィールドは、**プロジェクト契約** ページで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="05df2-152">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="05df2-153">このフィールドは、統合をサポートするための自然で一意のキーになっています。</span><span class="sxs-lookup"><span data-stu-id="05df2-153">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="05df2-154">新しいプロジェクト契約が作成されると、**プロジェクト契約 ID** 値がまだ存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-154">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="05df2-155">値は **ORD** から成り、番号順序が増分し、その後に 6 文字の接尾辞が続きます。</span><span class="sxs-lookup"><span data-stu-id="05df2-155">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="05df2-156">次に例を示します: **ORD-01022-Z4M9Q0**。</span><span class="sxs-lookup"><span data-stu-id="05df2-156">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="05df2-157">**プロジェクト番号** フィールドは、**プロジェクト** ページで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="05df2-157">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="05df2-158">このフィールドは、統合をサポートするための自然で一意のキーになっています。</span><span class="sxs-lookup"><span data-stu-id="05df2-158">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="05df2-159">新しいプロジェクトが作成されると、**プロジェクト番号** 値がまだ存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-159">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="05df2-160">値は **PRJ** から成り、番号順序が増分し、その後に 6 文字の接尾辞が続きます。</span><span class="sxs-lookup"><span data-stu-id="05df2-160">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="05df2-161">次に例を示します: **PRJ-01049-CCNID0**。</span><span class="sxs-lookup"><span data-stu-id="05df2-161">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="05df2-162">Project Service Automation から Finance への統合ソリューションが適用されると、アップグレード スクリプトにより、既存のプロジェクト契約の **プロジェクト契約 ID** フィールド、および Project Service Automation の既存のプロジェクトの **プロジェクト番号** フィールドが設定されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-162">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="05df2-163">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="05df2-163">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="05df2-164">プロジェクト契約およびプロジェクトの同期を行う前に、アカウントを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-164">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="05df2-165">接続設定で、**msdyn\_organizationalunits** から **msdyn\_name\[名前\]** への統合キー フィールドのマッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="05df2-165">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="05df2-166">最初にプロジェクトを接続設定に追加する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="05df2-166">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="05df2-167">詳細については、[アプリ用 Common Data Service へのデータの統合](/powerapps/administrator/data-integrator)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05df2-167">For more information, see [Integrate data into Common Data Service for Apps](/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="05df2-168">接続設定で、**msdyn\_projects** から **msdynce\_projectnumber\[プロジェクト番号\]** への統合キー フィールドのマッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="05df2-168">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="05df2-169">最初にプロジェクトを接続設定に追加する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="05df2-169">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="05df2-170">詳細については、[アプリ用 Common Data Service へのデータの統合](/powerapps/administrator/data-integrator)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05df2-170">For more information, see [Integrate data into Common Data Service for Apps](/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="05df2-171">プロジェクト契約およびプロジェクトの **SourceDataID** は、別の値に更新したり、マッピングから削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="05df2-171">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="05df2-172">既定のテンプレート値は **Project Service Automation** です。</span><span class="sxs-lookup"><span data-stu-id="05df2-172">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="05df2-173">**PaymentTerms** マッピングは、Finance の有効な支払条件を反映するように更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-173">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="05df2-174">プロジェクト タスクからマッピングを削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="05df2-174">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="05df2-175">既定値マップには、デモ データの既定値があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-175">The default value map has default values for demo data.</span></span> <span data-ttu-id="05df2-176">次の表は、Project Service Automation の値を示します。</span><span class="sxs-lookup"><span data-stu-id="05df2-176">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="05df2-177">Value</span><span class="sxs-lookup"><span data-stu-id="05df2-177">Value</span></span> | <span data-ttu-id="05df2-178">内容</span><span class="sxs-lookup"><span data-stu-id="05df2-178">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="05df2-179">1</span><span class="sxs-lookup"><span data-stu-id="05df2-179">1</span></span>     | <span data-ttu-id="05df2-180">支払期限 30 日以内</span><span class="sxs-lookup"><span data-stu-id="05df2-180">Net 30</span></span>        |
    | <span data-ttu-id="05df2-181">2</span><span class="sxs-lookup"><span data-stu-id="05df2-181">2</span></span>     | <span data-ttu-id="05df2-182">10 日以内支払割引 2%、支払期限 30 日以内</span><span class="sxs-lookup"><span data-stu-id="05df2-182">2% 10, Net 30</span></span> |
    | <span data-ttu-id="05df2-183">3</span><span class="sxs-lookup"><span data-stu-id="05df2-183">3</span></span>     | <span data-ttu-id="05df2-184">支払期限 45 日以内</span><span class="sxs-lookup"><span data-stu-id="05df2-184">Net 45</span></span>        |
    | <span data-ttu-id="05df2-185">4</span><span class="sxs-lookup"><span data-stu-id="05df2-185">4</span></span>     | <span data-ttu-id="05df2-186">支払期限 60 日以内</span><span class="sxs-lookup"><span data-stu-id="05df2-186">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="05df2-187">Power Query</span><span class="sxs-lookup"><span data-stu-id="05df2-187">Power Query</span></span>

<span data-ttu-id="05df2-188">次の条件が満たされている場合は、Microsoft Power Query for Excel を使用して、データをフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="05df2-188">Use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="05df2-189">Dynamics 365 Sales に受注があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-189">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="05df2-190">Project Service Automation に複数の組織単位があり、これらの組織単位は Finance の複数の法人にマップされます。</span><span class="sxs-lookup"><span data-stu-id="05df2-190">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="05df2-191">Power Query を使用する必要がある場合は、これらのガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="05df2-191">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="05df2-192">プロジェクトと契約 (PSA から Finance and Operation) テンプレートには既定のフィルターがあり、**作業項目 (msdyn\_ordertype = 192350001)** タイプの受注のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="05df2-192">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="05df2-193">このフィルターは、プロジェクト契約が Finance の受注に対して作成されないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="05df2-193">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="05df2-194">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05df2-194">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="05df2-195">統合接続セットの法人に同期する必要がある契約組織のみを含む Power Query フィルターを作成します。</span><span class="sxs-lookup"><span data-stu-id="05df2-195">Create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="05df2-196">たとえば、契約組織単位が Contoso US のプロジェクト契約は USSI の法人格に同期しますが、契約組織単位が Contoso グローバル のプロジェクト契約は USMF の法人に同期します。</span><span class="sxs-lookup"><span data-stu-id="05df2-196">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="05df2-197">このフィルターをタスク マッピングに追加しない場合、契約組織単位に関係なく、すべてのプロジェクト契約が接続設定に定義されている法人に同期されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-197">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="05df2-198">データ統合におけるテンプレート マッピング</span><span class="sxs-lookup"><span data-stu-id="05df2-198">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="05df2-199">**CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、 **AddressLine2**、**AddressState**、および **AddressZipCode** フィールドは、プロジェクト契約の既定マッピングには含まれません。</span><span class="sxs-lookup"><span data-stu-id="05df2-199">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="05df2-200">このデータをプロジェクト契約で同期する必要がある場合は、マッピングを追加できます。</span><span class="sxs-lookup"><span data-stu-id="05df2-200">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="05df2-201">**Description**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber**、および **ProjectType** フィールドは、プロジェクトの既定マッピングには含まれません。</span><span class="sxs-lookup"><span data-stu-id="05df2-201">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="05df2-202">このデータをプロジェクトで同期する必要がある場合は、マッピングを追加できます。</span><span class="sxs-lookup"><span data-stu-id="05df2-202">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="05df2-203">次の図は、データ統合のテンプレート タスク マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="05df2-203">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="05df2-204">マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="05df2-204">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="05df2-205">[![プロジェクト契約テンプレート マッピング](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="05df2-205">[![Project contract template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="05df2-206">[![プロジェクト テンプレート マッピング](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="05df2-206">[![Project template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="05df2-207">[![プロジェクト契約品目テンプレート マッピング](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="05df2-207">[![Project contract lines template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="05df2-208">[![プロジェクト契約品目マイルストーンのテンプレート マッピング](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="05df2-208">[![Project contract line milestone template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="05df2-209">プロジェクトおよび契約におけるプロジェクト契約品目のマイルストーン マッピング (PSA 3.x から Dynamics へ) - v2 テンプレート:</span><span class="sxs-lookup"><span data-stu-id="05df2-209">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="05df2-210">[![バージョン 2 テンプレートを使用したプロジェクト契約品目マイルストーン マッピング](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="05df2-210">[![Project contract line milestone mapping with version two template](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]