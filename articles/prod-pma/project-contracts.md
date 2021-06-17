---
title: プロジェクト契約
description: このトピックでは、さまざまなタイプのプロジェクトおよび資金調達ソースに対して作成できるプロジェクト契約の例と、契約の管理およびプロジェクト顧客への請求方法を示します。
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999767"
---
# <a name="project-contracts"></a><span data-ttu-id="4ef9f-103">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="4ef9f-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ef9f-104">この記事では、さまざまなタイプのプロジェクトおよび資金調達ソースに対して作成できるプロジェクト契約の例と、契約の管理およびプロジェクト顧客への請求方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="4ef9f-105">プロジェクト契約に対して作成するプロジェクトのタイプによって、プロジェクト顧客への請求方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="4ef9f-106">プロジェクト契約と関連プロジェクトは変更できますが、プロジェクト タイプは変更できません。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="4ef9f-107">プロジェクト契約を使用することにより、一度に 1 つ以上のプロジェクトの請求書を発行できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="4ef9f-108">プロジェクト契約は、プロジェクトの構造のすべての下位プロジェクトで一貫した請求手順を保証するためにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="4ef9f-109">請求されるすべてのプロジェクトは、プロジェクト契約に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="4ef9f-110">プロジェクト契約の設定は、そのプロジェクト契約に関連付けられているすべてのプロジェクトと下位プロジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="4ef9f-111">プロジェクト契約では、1 つ以上の資金調達ソースを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="4ef9f-112">したがって、複数の資金提供者の間で請求を分割し、資金調達ソースが指定された金額を超えて請求されないように資金調達の制限を設定し、経費を請求するための資金調達ルールを構成できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="4ef9f-113">プロジェクト契約の資金調達</span><span class="sxs-lookup"><span data-stu-id="4ef9f-113">Funding for project contracts</span></span>
<span data-ttu-id="4ef9f-114">プロジェクト契約によっては、複数の当事者がプロジェクトの費用の資金調達に共同で責任を負うように指定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="4ef9f-115">次に例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-115">Here are some examples:</span></span>

-   <span data-ttu-id="4ef9f-116">複数の部署を持つ大規模な顧客が、プロジェクトの資金を部署ごとに分割することを要求する。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="4ef9f-117">会社が、大規模プロジェクトのコストを外部組織と共有する。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="4ef9f-118">道路のプロジェクトが 2 つの自治体によって共同出資されている。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="4ef9f-119">1 つの橋のプロジェクトの資金を政府の補助金と一企業で賄っている。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="4ef9f-120">Dynamics 365 Finance では、1 つのトランザクションやプロジェクト全体の請求を複数の顧客、補助金、組織に分けることができます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="4ef9f-121">複数の資金提供者がいるプロジェクトでは、高度な資金調達プロジェクトの資金調達に寄与するすべての当事者を資金調達ソースと呼びます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="4ef9f-122">顧客、組織、補助金を資金調達ソースとして定義すると、1 つ以上の資金調達ルールに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="4ef9f-123">資金調達ルールには、費用をプロジェクトのさまざまな資金調達ソースにどのように配賦するかを決める条件が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="4ef9f-124">購買要求や発注書に表示される在庫品目は分割できないため、配布時にコスト金額を複数の資金調達ソースに分割することはできません。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="4ef9f-125">したがって、在庫払出が転記されるまで、資金調達ソースの値は 0 (ゼロ) のままです。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="4ef9f-126">在庫払出が転記されると、プロジェクトの勘定配賦ルールに従ってコストの金額が配賦されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="4ef9f-127">複数の資金調達ソース間で請求を分割しやすくするために実行できるいくつかの手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="4ef9f-128">プロジェクトに入力されるすべてのトランザクションがプロジェクト契約と同じ販売通貨を使用することを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="4ef9f-129">資金調達ソースがプロジェクトに対して指定された金額以上請求されないように、資金調達の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="4ef9f-130">それぞれの作業者、品目、カテゴリ、カテゴリ グループ、トランザクション タイプ (またはすべてのトランザクション タイプ) に対して、資金調達ルールと資金調達限度を設定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="4ef9f-131">オプションの開始日と終了日を選択して、各資金調達ルールが有効な期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="4ef9f-132">各資金調達ソースが担当する割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="4ef9f-133">資金配賦の計算によって生じる丸め差額を担当する資金調達ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="4ef9f-134">プロジェクトの費用を外部の顧客に請求する方法と内部の組織に請求する方法を決めるルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="4ef9f-135">追加の資金が得られるまで、または費用を内部で負担することを決定するまで、保留中の資金口座にトランザクションを記録します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="4ef9f-136">トランザクションに関連付ける税グループを決定するために、プロジェクトで税グループの割り当てが検索されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="4ef9f-137">プロジェクト レベルで税グループの割り当てが行われていない場合は、プロジェクト契約が検索されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="4ef9f-138">例: 複数の資金調達ソース (シンプル)</span><span class="sxs-lookup"><span data-stu-id="4ef9f-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="4ef9f-139">次の表に、複数の資金調達ソースで資金調達の配賦を管理するシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="4ef9f-140">これらのシナリオは、次の前提に基づいています。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="4ef9f-141">優先度の設定は、他の資金調達ルールの基準が適用される前に資金の配賦に反映されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="4ef9f-142">資金調達ルールが有効な期間を定義する日付範囲は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ef9f-143"><strong>シナリオ</strong></span><span class="sxs-lookup"><span data-stu-id="4ef9f-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="4ef9f-144"><strong>資金調達ソース</strong></span><span class="sxs-lookup"><span data-stu-id="4ef9f-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="4ef9f-145"><strong>配賦率</strong></span><span class="sxs-lookup"><span data-stu-id="4ef9f-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="4ef9f-146"><strong>配賦の優先順位</strong></span><span class="sxs-lookup"><span data-stu-id="4ef9f-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ef9f-147">資金がなくなるまでコストを 1 つの資金調達ソースに割り当て、資金がなくなるまでコストを 2 番目の資金調達ソースに割り当て、最後に残りのコストを 3 番目の資金調達ソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-148">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="4ef9f-149">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="4ef9f-150">資金調達ソース 3</span><span class="sxs-lookup"><span data-stu-id="4ef9f-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-151">100%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-151">100%</span></span></li>
<li><span data-ttu-id="4ef9f-152">100%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-152">100%</span></span></li>
<li><span data-ttu-id="4ef9f-153">100%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-154">1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-154">1</span></span></li>
<li><span data-ttu-id="4ef9f-155">2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-155">2</span></span></li>
<li><span data-ttu-id="4ef9f-156">3</span><span class="sxs-lookup"><span data-stu-id="4ef9f-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ef9f-157">コストの 75% を 1 つの資金調達ソースに割り当て、25% を 2 番目の資金調達ソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4ef9f-158">これらの資金調達ソースのいずれかが使い果たされた場合、残りのコストを 3 番目の資金調達ソースから支払います。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-159">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="4ef9f-160">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="4ef9f-161">資金調達ソース 3</span><span class="sxs-lookup"><span data-stu-id="4ef9f-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-162">75%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-162">75%</span></span></li>
<li><span data-ttu-id="4ef9f-163">25%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-163">25%</span></span></li>
<li><span data-ttu-id="4ef9f-164">100%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-165">1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-165">1</span></span></li>
<li><span data-ttu-id="4ef9f-166">1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-166">1</span></span></li>
<li><span data-ttu-id="4ef9f-167">2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ef9f-168">コストの 75% を 1 つの資金調達ソースに割り当て、25% を 2 番目の資金調達ソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4ef9f-169">これらの資金調達ソースのいずれかが使い果たされた場合、残りのコストを 3 番目と 4 番目の資金調達ソースで分割します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-170">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="4ef9f-171">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="4ef9f-172">資金調達ソース 3</span><span class="sxs-lookup"><span data-stu-id="4ef9f-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="4ef9f-173">資金調達ソース 4</span><span class="sxs-lookup"><span data-stu-id="4ef9f-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-174">75%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-174">75%</span></span></li>
<li><span data-ttu-id="4ef9f-175">25%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-175">25%</span></span></li>
<li><span data-ttu-id="4ef9f-176">50%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-176">50%</span></span></li>
<li><span data-ttu-id="4ef9f-177">50%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-178">1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-178">1</span></span></li>
<li><span data-ttu-id="4ef9f-179">1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-179">1</span></span></li>
<li><span data-ttu-id="4ef9f-180">2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-180">2</span></span></li>
<li><span data-ttu-id="4ef9f-181">2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ef9f-182">コストの最初の 25% を 1 つの資金調達ソースに割り当て、残りを 2 番目の資金調達ソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-183">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="4ef9f-184">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-185">25%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-185">25%</span></span></li>
<li><span data-ttu-id="4ef9f-186">100%</span><span class="sxs-lookup"><span data-stu-id="4ef9f-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4ef9f-187">1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-187">1</span></span></li>
<li><span data-ttu-id="4ef9f-188">2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="4ef9f-189">例: 複数の資金調達ソース (複雑)</span><span class="sxs-lookup"><span data-stu-id="4ef9f-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="4ef9f-190">次の順番で使用する 3 つの資金調達ソースがあります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="4ef9f-191">資金調達ソース 2 と資金調達ソース 3 を、資金調達ソース 2 が資金調達限度に達するまで同じように使用します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="4ef9f-192">資金調達ソース 3 を資金調達限度に達するまで使用します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="4ef9f-193">資金調達ソース 3 が資金調達限度に達したら、資金調達ソース 1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="4ef9f-194">これを実現するには、次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="4ef9f-195">資金調達ソース 2 と資金調達ソース 3 の資金調達限度の金額をそれぞれ設定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="4ef9f-196">次の資金調達ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="4ef9f-197">ルール 1 (優先度 1): トランザクションの 50% を資金調達ソース 2 に配賦し、50% を資金調達ソース 3 に配賦します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="4ef9f-198">ルール 2 (優先度 2): トランザクションの 100% を資金調達ソース 3 に配賦します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="4ef9f-199">ルール 3 (優先度 3): トランザクションの 100% を資金調達ソース 1 に配賦します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="4ef9f-200">この設定は、トランザクションがルールや限度に対して確認され、それらがトランザクションに適用されるかどうかが判断されることによって機能します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="4ef9f-201">トランザクションに特定のルールまたは限度が適用されない場合は、すべてのトランザクションのルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="4ef9f-202">すべてのトランザクションのルールには、すべてのトランザクションが一致します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="4ef9f-203">トランザクションに一致するルールが見つかった場合、そのルールに割り当てられている割合が最初に適用されますが、一致が設定されている制限と照合された後にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="4ef9f-204">制限が満たされ、資金調達ソースの資金が使い果たされた場合、資金調達制限に関連付けられている資金調達ルールは無視され、プログラムは次に適用されるルールをチェックします。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="4ef9f-205">場合によっては、ルールで配賦できるのがトランザクションの一部のみのことがあります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="4ef9f-206">これは、トランザクションに配賦されたときに限度に達した場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="4ef9f-207">この場合、各資金調達ソースに 50% などのルールに従った特定の金額しか配賦されません。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="4ef9f-208">これは、このセクションで先に説明したルール 1 に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="4ef9f-209">残りは、次の優先度のルールに従って配賦されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="4ef9f-210">次の表に、このシナリオの詳しい説明を示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ef9f-211"><strong>フォーカス</strong></span><span class="sxs-lookup"><span data-stu-id="4ef9f-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="4ef9f-212"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="4ef9f-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ef9f-213">資金調達ルール</span><span class="sxs-lookup"><span data-stu-id="4ef9f-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-214">ルール 1 (優先度 1): すべてのトランザクション。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="4ef9f-215">資金調達ソース 2 に 50%、資金調達ソース 3 に 50% を配賦します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="4ef9f-216">ルール 2 (優先度 2): すべてのトランザクション。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="4ef9f-217">資金調達ソース 3 に 100% を配賦します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="4ef9f-218">ルール 3 (優先度 2): すべてのトランザクション。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="4ef9f-219">資金調達ソース 1 に 100% を配賦します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ef9f-220">資金調達限度</span><span class="sxs-lookup"><span data-stu-id="4ef9f-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-221">資金調達ソース 1 の限度 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="4ef9f-222">資金調達ソース 2 の限度 = 500.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="4ef9f-223">資金調達ソース 3 の限度 = 750.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ef9f-224">トランザクション 1</span><span class="sxs-lookup"><span data-stu-id="4ef9f-224">Transaction 1</span></span></td>
<td><span data-ttu-id="4ef9f-225"><strong>トランザクション金額:</strong> 100.00 <strong>資金調達:</strong> トランザクションは、ルール 1 が適用された後に全額支払われるため、ルール 1 に従ってのみ支払われます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="4ef9f-226">このトランザクションは、資金調達ソース 2 と資金調達ソース 3 から均等に資金調達されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="4ef9f-227">資金調達ソース 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="4ef9f-228">資金調達ソース 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ef9f-229">トランザクション 2</span><span class="sxs-lookup"><span data-stu-id="4ef9f-229">Transaction 2</span></span></td>
<td><span data-ttu-id="4ef9f-230"><strong>トランザクション金額:</strong> 5,000.00 <strong>資金調達:</strong> トランザクションは、3 つのルールすべてに従って支払われます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="4ef9f-231"><strong>ルール 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="4ef9f-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="4ef9f-232">資金調達ソース 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="4ef9f-233">資金調達ソース 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="4ef9f-234">
<strong>ルール 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="4ef9f-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="4ef9f-235">資金調達ソース 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="4ef9f-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="4ef9f-236">
<strong>ルール 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="4ef9f-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="4ef9f-237">資金調達ソース 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="4ef9f-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ef9f-238">各資金調達ソースに配賦される資金の合計</span><span class="sxs-lookup"><span data-stu-id="4ef9f-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="4ef9f-239">資金調達ソース 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="4ef9f-240">資金調達ソース 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="4ef9f-241">資金調達ソース 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="4ef9f-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="4ef9f-242">請求ルール</span><span class="sxs-lookup"><span data-stu-id="4ef9f-242">Billing rules</span></span>
<span data-ttu-id="4ef9f-243">顧客とプロジェクト契約を交渉するとき、プロジェクトの作業について顧客に請求する方法と時期を定義します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="4ef9f-244">プロジェクト契約とプロジェクトを設定した後で、プロジェクトの請求ルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="4ef9f-245">請求ルールは、プロジェクト契約で指定されているプロジェクトの契約条件に基づきます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="4ef9f-246">作成できる請求ルールは、請求ルールに関連付けるプロジェクト契約の契約条件やプロジェクト タイプ (時間/実費払いや固定価格など) によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="4ef9f-247">1 つのプロジェクト契約に対して、複数の請求ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="4ef9f-248">また、同じプロジェクト契約に関連付けられていて、同様の請求条件を持つ複数のプロジェクトに請求ルールを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="4ef9f-249">設定できる請求ルールには、次のようなタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="4ef9f-250">**荷渡の単位**: 荷渡の単位が完了したときに顧客に請求します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="4ef9f-251">荷渡の単位は契約で定義します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="4ef9f-252">**進捗状況**: プロジェクトが指定した進捗率に達したときに顧客に請求します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="4ef9f-253">作業の進捗率を自動で計算するように請求ルールを設定するか、作業の進捗率と顧客への請求金額を手動で計算することができます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="4ef9f-254">**マイルストーン**: プロジェクトのマイルストーンに達したときに、マイルストーンまでのすべての金額を顧客に請求します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="4ef9f-255">**手数料**: サービスの費用と管理手数料を顧客に請求します。管理手数料は通常、サービスの費用に料率をかけたものになります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="4ef9f-256">**時間/実費払い**: プロジェクトで使用した時間と材料の価格を顧客に請求します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="4ef9f-257">すべてのタイプの請求ルールで、プロジェクトが合意した段階に達するまで顧客請求書から差し引く留保率を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="4ef9f-258">支払留保率は、プロジェクト契約で指定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="4ef9f-259">この金額は、顧客請求書の明細行の合計額に基づいて計算され、そこから差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="4ef9f-260">**時間/実費払い** と **進捗状況** の請求ルールでは、請求可能カテゴリを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="4ef9f-261">請求可能カテゴリは、顧客請求書に含める必要があるトランザクションを示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="4ef9f-262">顧客に請求する準備ができると、プロジェクトの請求金額が請求ルールに基づいて計算され、プロジェクト請求提案が生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="4ef9f-263">次のセクションでは、プロジェクトの請求ルールを設定および管理する方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="4ef9f-264">例: 出荷された単位数に基づく請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="4ef9f-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="4ef9f-265">組織は、トレーニング セッションごとに 10,000 のコストで顧客の従業員に合計 5 つのトレーニング セッションを提供するという契約を結びます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="4ef9f-266">各トレーニング セッションの後に顧客に請求します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="4ef9f-267">契約の請求ルールを設定するときは、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="4ef9f-268">出荷単位は 1 つのトレーニング セッションです。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="4ef9f-269">単価はトレーニング セッションあたり 10,000 です。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="4ef9f-270">単位の総数は 5 つのトレーニング セッションです。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="4ef9f-271">1 回のトレーニング セッションが完了したら、最初に出荷された単位について 10,000 の請求書を作成し、その請求書を顧客に送信できます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="4ef9f-272">例: 指定されたプロジェクト完了率 (手動計算) に基づく請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="4ef9f-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="4ef9f-273">ソフトウェア コンサルティング会社である組織が、顧客が開発している製品の一部を開発する契約を顧客と締結します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="4ef9f-274">組織は、ソフトウェア コードを 6 か月間にわたって提供することに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="4ef9f-275">顧客は、組織に対して合計 100,000 の作業費を支払うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="4ef9f-276">請求ルールを作成して、契約で指定されたプロジェクト完了率に基づいて顧客に請求します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="4ef9f-277">最初の月の終わりに顧客と会い、完了した作業の割合を決定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="4ef9f-278">顧客と共にプロジェクトをレビューした後、プロジェクトが 15％ 完了したと判断します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="4ef9f-279">15,000 (100,000 の 15%) の請求書を作成し、それを顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="4ef9f-280">例: 指定されたプロジェクト完了率 (自動計算) に基づく請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="4ef9f-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="4ef9f-281">ソフトウェア開発会社である組織が、顧客の給与計算パッケージを 30,000 で開発することに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="4ef9f-282">顧客は、作業の完了率に基づいて組織に支払を行うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="4ef9f-283">プロジェクト コストは 20,000 であると見積もります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="4ef9f-284">プロジェクト契約では、請求プロセスで使用する作業のカテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="4ef9f-285">各カテゴリの完了した作業の割合に対する請求額を自動的に計算する請求ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="4ef9f-286">カテゴリごとに予算を設定します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="4ef9f-287">**開発** – 15,000 のコストと 20,000 の売上</span><span class="sxs-lookup"><span data-stu-id="4ef9f-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="4ef9f-288">**インストール** – 5,000 のコストと 10,000 の売上</span><span class="sxs-lookup"><span data-stu-id="4ef9f-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="4ef9f-289">初めて顧客請求書を作成すると、請求額は次の情報に基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="4ef9f-290">1 か月後、プロジェクトの作業者はプロジェクトのタイムシートを提出します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="4ef9f-291">作業者の時間のコストは、開発で 5,000、インストールで 1,000 です。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="4ef9f-292">開発作業は 33% 完了 (5,000 実績原価 / 15,000 予算原価)、インストール作業は 20% 完了 (1,000 実績原価 / 5,000 予算原価) しています。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="4ef9f-293">請求金額 8,667 が自動的に計算されます (20,000 の 33% + 10,000 の 20%)。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="4ef9f-294">8,667 の請求書を作成し、それを顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="4ef9f-295">例: 合意済のマイルストーンに基づく請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="4ef9f-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="4ef9f-296">経営コンサルティング会社である組織は、顧客が販売を計画している消費者製品の市場調査を行うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="4ef9f-297">顧客は、3 月から 3 か月間サービスを使用することに同意し、組織に 50,000 を支払うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="4ef9f-298">プロジェクトには 3 つのマイルストーンがあります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-298">The project has three milestones:</span></span>

-   <span data-ttu-id="4ef9f-299">マイルストーン 1: 消費者データの収集 – 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4ef9f-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="4ef9f-300">マイルストーン 2: 消費者データの分析 – 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="4ef9f-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="4ef9f-301">マイルストーン 3: 製品の実行可能性提案を提示する – 5 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4ef9f-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="4ef9f-302">顧客は、最初のマイルストーンに10,000、2 番目のマイルストーンに 20,000、3 番目のマイルストーンに 20,000 を支払うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="4ef9f-303">プロジェクト契約を設定すると、完了したマイルストーンに基づいて顧客に請求することに同意したことになります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="4ef9f-304">請求ルールの設定には、次の手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="4ef9f-305">プロジェクト マイルストーンを定義します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-305">Define the project milestones.</span></span>
-   <span data-ttu-id="4ef9f-306">各マイルストーンが完了したときに顧客に請求する金額を定義します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="4ef9f-307">3 月 31 日に最初のマイルストーンが完了したら、マイルストーンを完了済としてマークし、10,000 の請求書を作成して顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="4ef9f-308">マイルストーンを完了済としてマークするまで、マイルストーンの請求書を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="4ef9f-309">例: サービスと管理料金に基づく請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="4ef9f-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="4ef9f-310">経営コンサルティング会社である組織は、顧客である小売企業が開発している製品の実行可能性を評価するために市場調査を行うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="4ef9f-311">契約の条件では、時間と材料に基づいて調査を実施する上位 3 名の経営コンサルタントのサービスを提供することを指定しています。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="4ef9f-312">顧客は 1 時間あたり 100 に加えて、プロジェクトに請求されるコンサルティング時間に対して 10% の管理料金を支払うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4ef9f-313">プロジェクト契約を設定するときに、プロジェクトに請求されるコンサルティング時間に 10％ の管理料金を追加する請求ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4ef9f-314">顧客の請求書を作成すると、顧客には 10％ の管理料金とコンサルティング時間の費用が請求されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="4ef9f-315">たとえば、3 人のコンサルタントがプロジェクトで合計 200 時間働いた場合、次の計算に基づいて 22,000 の請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="4ef9f-316">1 時間あたり 100 で200時間 = 20,000</span><span class="sxs-lookup"><span data-stu-id="4ef9f-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="4ef9f-317">10% の管理料金 = 2,000</span><span class="sxs-lookup"><span data-stu-id="4ef9f-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="4ef9f-318">合計請求金額 = 22,000</span><span class="sxs-lookup"><span data-stu-id="4ef9f-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="4ef9f-319">料金が顧客に課税される場合に、プロジェクト契約で消費税グループを選択すると、消費税グループは料金の請求ルールに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="4ef9f-320">例: 時間と材料の値の請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="4ef9f-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="4ef9f-321">ソフトウェア コンサルティング会社である組織は、次の 6 か月間、顧客向けのソフトウェア開発プロジェクトに取り組むために 5 人の技術コンサルタントを提供することに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="4ef9f-322">顧客は、コンサルティング時間ごとに 150 と事務用品の費用を支払うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="4ef9f-323">組織は毎月末に顧客に請求書を送ります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="4ef9f-324">プロジェクト契約を設定すると、プロジェクトの時間と材料について毎月顧客に請求することに同意したことになります。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="4ef9f-325">次の情報を含む請求ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="4ef9f-326">契約期間は 6 ヶ月です。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-326">The contract period is six months.</span></span>
-   <span data-ttu-id="4ef9f-327">コンサルティング時間は、1 時間あたり 150 の割合で計算されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="4ef9f-328">事務用品は原価で請求され、プロジェクトの総コストは 10,000 を超えてはなりません。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="4ef9f-329">プロジェクト中の各カレンダー月の末に顧客請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="4ef9f-330">最初の 1 か月の間に、プロジェクトのコンサルタントが合計 800 時間を記録しました。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="4ef9f-331">プロジェクトに請求される事務用品のコストは 2,000 です。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="4ef9f-332">したがって、月末に 122,000 の請求書を作成します。これは、1 時間あたり 150 で 800 時間、事務用品には 2,000 を加えたものとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="4ef9f-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]