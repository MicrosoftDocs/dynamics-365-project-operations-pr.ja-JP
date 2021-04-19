---
title: スケジュール API を使用して、スケジューリング エンティティで操作を実行する
description: このトピックは、スケジュール API を使用するための情報とサンプルを提供します。
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868135"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="8c646-103">スケジュール API を使用して、スケジューリング エンティティで操作を実行する</span><span class="sxs-lookup"><span data-stu-id="8c646-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="8c646-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="8c646-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8c646-105">このトピックに記載されている機能の一部または全部は、プレビュー リリースの一部として提供されています。</span><span class="sxs-lookup"><span data-stu-id="8c646-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="8c646-106">コンテンツおよび機能は変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8c646-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="8c646-107">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c646-107">Scheduling entities</span></span>

<span data-ttu-id="8c646-108">スケジュール API は、**スケジューリング エンティティ** を使って操作を作成、更新、および削除を実行する機能を提供します。。</span><span class="sxs-lookup"><span data-stu-id="8c646-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="8c646-109">これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。</span><span class="sxs-lookup"><span data-stu-id="8c646-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="8c646-110">**スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。</span><span class="sxs-lookup"><span data-stu-id="8c646-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="8c646-111">次の表は、**スケジューリング エンティティ** の完全なリストです。</span><span class="sxs-lookup"><span data-stu-id="8c646-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="8c646-112">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="8c646-112">Entity name</span></span>  | <span data-ttu-id="8c646-113">エンティティの論理名</span><span class="sxs-lookup"><span data-stu-id="8c646-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="8c646-114">Project</span><span class="sxs-lookup"><span data-stu-id="8c646-114">Project</span></span> | <span data-ttu-id="8c646-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8c646-115">msdyn_project</span></span> |
| <span data-ttu-id="8c646-116">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="8c646-116">Project Task</span></span>  | <span data-ttu-id="8c646-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="8c646-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="8c646-118">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="8c646-118">Project Task Dependency</span></span>  | <span data-ttu-id="8c646-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="8c646-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="8c646-120">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="8c646-120">Resource Assignment</span></span> | <span data-ttu-id="8c646-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="8c646-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="8c646-122">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="8c646-122">Project Bucket</span></span>  | <span data-ttu-id="8c646-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="8c646-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="8c646-124">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="8c646-124">Project Team Member</span></span> | <span data-ttu-id="8c646-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="8c646-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="8c646-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="8c646-126">OperationSet</span></span>

<span data-ttu-id="8c646-127">OperationSet は、スケジュールに影響を与える複数の要求をトランザクション内で処理する必要がある場合に使用できる作業単位パターンです。</span><span class="sxs-lookup"><span data-stu-id="8c646-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="8c646-128">スケジュール API</span><span class="sxs-lookup"><span data-stu-id="8c646-128">Schedule APIs</span></span>

<span data-ttu-id="8c646-129">以下は、現在のスケジュール API のリストです。</span><span class="sxs-lookup"><span data-stu-id="8c646-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="8c646-130">**msdyn_CreateProjectV1**: この API を使用してプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="8c646-131">プロジェクトとデフォルトのプロジェクト バケットがすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="8c646-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="8c646-132">**msdyn_CreateTeamMemberV1**: この API を使用して、プロジェクト チーム メンバーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="8c646-133">チーム メンバーのレコードはすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="8c646-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="8c646-134">**msdyn_CreateOperationSetV1**: この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="8c646-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="8c646-135">**msdyn_PSSCreateV1**: この API を使用してエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="8c646-136">エンティティは、作成操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="8c646-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="8c646-137">**msdyn_PSSUpdateV1**: この API を使用してエンティティを更新できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="8c646-138">エンティティは、更新操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="8c646-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="8c646-139">**msdyn_PSSDeleteV1**: この API を使用してエンティティを削除できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="8c646-140">エンティティは、削除操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="8c646-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="8c646-141">**msdyn_ExecuteOperationSetV1**: この API は、指定された操作セット内のすべての操作を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8c646-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="8c646-142">OperationSet と ScheduleAPI の併用</span><span class="sxs-lookup"><span data-stu-id="8c646-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="8c646-143">**CreateProjectV1** と **CreateTeamMemberV1** 両方があるレコードは直ちに作成されるため、これらの API は **OperationSet** で直接使用できません。</span><span class="sxs-lookup"><span data-stu-id="8c646-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="8c646-144">ただし、API を使用して必要なレコードを作成し、**OperationSet** を作成し、これらの事前に作成されたレコードを **OperationSet** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="8c646-145">サポートされている操作</span><span class="sxs-lookup"><span data-stu-id="8c646-145">Supported operations</span></span>

| <span data-ttu-id="8c646-146">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c646-146">Scheduling entity</span></span> | <span data-ttu-id="8c646-147">作成​​</span><span class="sxs-lookup"><span data-stu-id="8c646-147">Create</span></span> | <span data-ttu-id="8c646-148">更新プログラム</span><span class="sxs-lookup"><span data-stu-id="8c646-148">Update</span></span> | <span data-ttu-id="8c646-149">Delete キー</span><span class="sxs-lookup"><span data-stu-id="8c646-149">Delete</span></span> | <span data-ttu-id="8c646-150">重要な考慮事項</span><span class="sxs-lookup"><span data-stu-id="8c646-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="8c646-151">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="8c646-151">Project task</span></span> | <span data-ttu-id="8c646-152">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-152">Yes</span></span> | <span data-ttu-id="8c646-153">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-153">Yes</span></span> | <span data-ttu-id="8c646-154">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-154">Yes</span></span> | <span data-ttu-id="8c646-155">いいえ​​</span><span class="sxs-lookup"><span data-stu-id="8c646-155">None</span></span> |
| <span data-ttu-id="8c646-156">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="8c646-156">Project task dependency</span></span> | <span data-ttu-id="8c646-157">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-157">Yes</span></span> | <span data-ttu-id="8c646-158">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-158">Yes</span></span> | | <span data-ttu-id="8c646-159">プロジェクト タスクの依存関係レコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="8c646-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="8c646-160">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8c646-161">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="8c646-161">Resource assignment</span></span> | <span data-ttu-id="8c646-162">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-162">Yes</span></span> | <span data-ttu-id="8c646-163">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-163">Yes</span></span> | | <span data-ttu-id="8c646-164">次のフィールドを使用した操作はサポートされていません: **BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining**、および **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="8c646-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="8c646-165">リソース割り当てレコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="8c646-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="8c646-166">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8c646-167">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="8c646-167">Project bucket</span></span> | <span data-ttu-id="8c646-168">N/A</span><span class="sxs-lookup"><span data-stu-id="8c646-168">N/A</span></span> | <span data-ttu-id="8c646-169">N/A</span><span class="sxs-lookup"><span data-stu-id="8c646-169">N/A</span></span> | <span data-ttu-id="8c646-170">N/A</span><span class="sxs-lookup"><span data-stu-id="8c646-170">N/A</span></span> | <span data-ttu-id="8c646-171">既定のバケットは、**CreateProjectV1** API を使って作成されます。</span><span class="sxs-lookup"><span data-stu-id="8c646-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="8c646-172">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="8c646-172">Project team member</span></span> | <span data-ttu-id="8c646-173">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-173">Yes</span></span> | <span data-ttu-id="8c646-174">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-174">Yes</span></span> | <span data-ttu-id="8c646-175">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-175">Yes</span></span> | <span data-ttu-id="8c646-176">作成操作には、**CreateTeamMemberV1** API を使用します。</span><span class="sxs-lookup"><span data-stu-id="8c646-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="8c646-177">Project</span><span class="sxs-lookup"><span data-stu-id="8c646-177">Project</span></span> | <span data-ttu-id="8c646-178">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-178">Yes</span></span> | <span data-ttu-id="8c646-179">有効</span><span class="sxs-lookup"><span data-stu-id="8c646-179">Yes</span></span> | <span data-ttu-id="8c646-180">N/A</span><span class="sxs-lookup"><span data-stu-id="8c646-180">N/A</span></span> | <span data-ttu-id="8c646-181">次のフィールドを使用した操作はサポートされていません: **StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、 **CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart**、および **Duration**。</span><span class="sxs-lookup"><span data-stu-id="8c646-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="8c646-182">これらの API は、カスタムフィールドを含むエンティティ オブジェクトを使用して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8c646-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="8c646-183">ID プロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="8c646-183">The ID property is optional.</span></span> <span data-ttu-id="8c646-184">提供されている場合、システムはそれを使用しようとし、使用できない場合は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="8c646-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="8c646-185">提供されていない場合は、システムが生成します。</span><span class="sxs-lookup"><span data-stu-id="8c646-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="8c646-186">制限事項と既知の問題</span><span class="sxs-lookup"><span data-stu-id="8c646-186">Limitations and known issues</span></span>
<span data-ttu-id="8c646-187">以下は、制限事項と既知の問題のリストです。</span><span class="sxs-lookup"><span data-stu-id="8c646-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="8c646-188">スケジュール API は、**Microsoft Project ライセンスを持つユーザー** のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c646-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="8c646-189">次のユーザーは使用できません:</span><span class="sxs-lookup"><span data-stu-id="8c646-189">They can't be used by:</span></span>
    - <span data-ttu-id="8c646-190">アプリケーション ユーザー</span><span class="sxs-lookup"><span data-stu-id="8c646-190">Application users</span></span>
    - <span data-ttu-id="8c646-191">システム ユーザー</span><span class="sxs-lookup"><span data-stu-id="8c646-191">System users</span></span>
    - <span data-ttu-id="8c646-192">統合ユーザー</span><span class="sxs-lookup"><span data-stu-id="8c646-192">Integration users</span></span>
    - <span data-ttu-id="8c646-193">必要なライセンスを持っていない他のユーザー</span><span class="sxs-lookup"><span data-stu-id="8c646-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="8c646-194">各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。</span><span class="sxs-lookup"><span data-stu-id="8c646-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="8c646-195">各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。</span><span class="sxs-lookup"><span data-stu-id="8c646-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="8c646-196">Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8c646-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="8c646-197">**OperationSet** 障害ステータスと障害ログは現在利用できません。</span><span class="sxs-lookup"><span data-stu-id="8c646-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="8c646-198">スケジュール API はパブリック プレビューにあります。</span><span class="sxs-lookup"><span data-stu-id="8c646-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="8c646-199">実稼働環境におけるこれらの API の使用は、Microsoft ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8c646-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="8c646-200">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="8c646-200">Sample scenario</span></span>

<span data-ttu-id="8c646-201">このシナリオでは、プロジェクト、チームメンバー、4 つのタスク、および 2 つのリソース割り当てを作成します。</span><span class="sxs-lookup"><span data-stu-id="8c646-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="8c646-202">次に、1 つのタスクを更新し、プロジェクトを更新し、1 つのタスクを削除し、1 つのリソース割り当てを削除して、タスクの依存関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="8c646-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="8c646-203">追加の例</span><span class="sxs-lookup"><span data-stu-id="8c646-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
