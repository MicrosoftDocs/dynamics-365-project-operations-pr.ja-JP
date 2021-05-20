---
title: スケジュール API を使用して、スケジューリング エンティティで操作を実行する
description: このトピックは、スケジュール API を使用するための情報とサンプルを提供します。
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950810"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="a31cb-103">スケジュール API を使用して、スケジューリング エンティティで操作を実行する</span><span class="sxs-lookup"><span data-stu-id="a31cb-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="a31cb-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="a31cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a31cb-105">このトピックに記載されている機能の一部または全部は、プレビュー リリースの一部として提供されています。</span><span class="sxs-lookup"><span data-stu-id="a31cb-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="a31cb-106">コンテンツおよび機能は変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a31cb-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="a31cb-107">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="a31cb-107">Scheduling entities</span></span>

<span data-ttu-id="a31cb-108">スケジュール API は、**スケジューリング エンティティ** を使って操作を作成、更新、および削除を実行する機能を提供します。。</span><span class="sxs-lookup"><span data-stu-id="a31cb-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="a31cb-109">これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="a31cb-110">**スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。</span><span class="sxs-lookup"><span data-stu-id="a31cb-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="a31cb-111">次の表は、**スケジューリング エンティティ** の完全なリストです。</span><span class="sxs-lookup"><span data-stu-id="a31cb-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="a31cb-112">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="a31cb-112">Entity name</span></span>  | <span data-ttu-id="a31cb-113">エンティティの論理名</span><span class="sxs-lookup"><span data-stu-id="a31cb-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="a31cb-114">Project</span><span class="sxs-lookup"><span data-stu-id="a31cb-114">Project</span></span> | <span data-ttu-id="a31cb-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a31cb-115">msdyn_project</span></span> |
| <span data-ttu-id="a31cb-116">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a31cb-116">Project Task</span></span>  | <span data-ttu-id="a31cb-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="a31cb-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="a31cb-118">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="a31cb-118">Project Task Dependency</span></span>  | <span data-ttu-id="a31cb-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="a31cb-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="a31cb-120">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="a31cb-120">Resource Assignment</span></span> | <span data-ttu-id="a31cb-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="a31cb-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="a31cb-122">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="a31cb-122">Project Bucket</span></span>  | <span data-ttu-id="a31cb-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="a31cb-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="a31cb-124">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="a31cb-124">Project Team Member</span></span> | <span data-ttu-id="a31cb-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="a31cb-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="a31cb-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="a31cb-126">OperationSet</span></span>

<span data-ttu-id="a31cb-127">OperationSet は、スケジュールに影響を与える複数の要求をトランザクション内で処理する必要がある場合に使用できる作業単位パターンです。</span><span class="sxs-lookup"><span data-stu-id="a31cb-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="a31cb-128">スケジュール API</span><span class="sxs-lookup"><span data-stu-id="a31cb-128">Schedule APIs</span></span>

<span data-ttu-id="a31cb-129">以下は、現在のスケジュール API のリストです。</span><span class="sxs-lookup"><span data-stu-id="a31cb-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="a31cb-130">**msdyn_CreateProjectV1**: この API を使用してプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="a31cb-131">プロジェクトとデフォルトのプロジェクト バケットがすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="a31cb-132">**msdyn_CreateTeamMemberV1**: この API を使用して、プロジェクト チーム メンバーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="a31cb-133">チーム メンバーのレコードはすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="a31cb-134">**msdyn_CreateOperationSetV1**: この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="a31cb-135">**msdyn_PSSCreateV1**: この API を使用してエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="a31cb-136">エンティティは、作成操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="a31cb-137">**msdyn_PSSUpdateV1**: この API を使用してエンティティを更新できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="a31cb-138">エンティティは、更新操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="a31cb-139">**msdyn_PSSDeleteV1**: この API を使用してエンティティを削除できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="a31cb-140">エンティティは、削除操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="a31cb-141">**msdyn_ExecuteOperationSetV1**: この API は、指定された操作セット内のすべての操作を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="a31cb-142">OperationSet と ScheduleAPI の併用</span><span class="sxs-lookup"><span data-stu-id="a31cb-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="a31cb-143">**CreateProjectV1** と **CreateTeamMemberV1** 両方があるレコードは直ちに作成されるため、これらの API は **OperationSet** で直接使用できません。</span><span class="sxs-lookup"><span data-stu-id="a31cb-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="a31cb-144">ただし、API を使用して必要なレコードを作成し、**OperationSet** を作成し、これらの事前に作成されたレコードを **OperationSet** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="a31cb-145">サポートされている操作</span><span class="sxs-lookup"><span data-stu-id="a31cb-145">Supported operations</span></span>

| <span data-ttu-id="a31cb-146">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="a31cb-146">Scheduling entity</span></span> | <span data-ttu-id="a31cb-147">作成​​</span><span class="sxs-lookup"><span data-stu-id="a31cb-147">Create</span></span> | <span data-ttu-id="a31cb-148">更新プログラム</span><span class="sxs-lookup"><span data-stu-id="a31cb-148">Update</span></span> | <span data-ttu-id="a31cb-149">Delete キー</span><span class="sxs-lookup"><span data-stu-id="a31cb-149">Delete</span></span> | <span data-ttu-id="a31cb-150">重要な考慮事項</span><span class="sxs-lookup"><span data-stu-id="a31cb-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="a31cb-151">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a31cb-151">Project task</span></span> | <span data-ttu-id="a31cb-152">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-152">Yes</span></span> | <span data-ttu-id="a31cb-153">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-153">Yes</span></span> | <span data-ttu-id="a31cb-154">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-154">Yes</span></span> | <span data-ttu-id="a31cb-155">いいえ​​</span><span class="sxs-lookup"><span data-stu-id="a31cb-155">None</span></span> |
| <span data-ttu-id="a31cb-156">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="a31cb-156">Project task dependency</span></span> | <span data-ttu-id="a31cb-157">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-157">Yes</span></span> | <span data-ttu-id="a31cb-158">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-158">Yes</span></span> | | <span data-ttu-id="a31cb-159">プロジェクト タスクの依存関係レコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="a31cb-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="a31cb-160">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a31cb-161">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="a31cb-161">Resource assignment</span></span> | <span data-ttu-id="a31cb-162">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-162">Yes</span></span> | <span data-ttu-id="a31cb-163">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-163">Yes</span></span> | | <span data-ttu-id="a31cb-164">次のフィールドを使用した操作はサポートされていません: **BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining**、および **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="a31cb-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="a31cb-165">リソース割り当てレコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="a31cb-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="a31cb-166">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a31cb-167">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="a31cb-167">Project bucket</span></span> | <span data-ttu-id="a31cb-168">N/A</span><span class="sxs-lookup"><span data-stu-id="a31cb-168">N/A</span></span> | <span data-ttu-id="a31cb-169">N/A</span><span class="sxs-lookup"><span data-stu-id="a31cb-169">N/A</span></span> | <span data-ttu-id="a31cb-170">N/A</span><span class="sxs-lookup"><span data-stu-id="a31cb-170">N/A</span></span> | <span data-ttu-id="a31cb-171">既定のバケットは、**CreateProjectV1** API を使って作成されます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="a31cb-172">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="a31cb-172">Project team member</span></span> | <span data-ttu-id="a31cb-173">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-173">Yes</span></span> | <span data-ttu-id="a31cb-174">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-174">Yes</span></span> | <span data-ttu-id="a31cb-175">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-175">Yes</span></span> | <span data-ttu-id="a31cb-176">作成操作には、**CreateTeamMemberV1** API を使用します。</span><span class="sxs-lookup"><span data-stu-id="a31cb-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="a31cb-177">Project</span><span class="sxs-lookup"><span data-stu-id="a31cb-177">Project</span></span> | <span data-ttu-id="a31cb-178">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-178">Yes</span></span> | <span data-ttu-id="a31cb-179">有効</span><span class="sxs-lookup"><span data-stu-id="a31cb-179">Yes</span></span> | <span data-ttu-id="a31cb-180">N/A</span><span class="sxs-lookup"><span data-stu-id="a31cb-180">N/A</span></span> | <span data-ttu-id="a31cb-181">次のフィールドを使用した操作はサポートされていません: **StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、 **CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart**、および **Duration**。</span><span class="sxs-lookup"><span data-stu-id="a31cb-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="a31cb-182">これらの API は、カスタムフィールドを含むエンティティ オブジェクトを使用して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="a31cb-183">ID プロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="a31cb-183">The ID property is optional.</span></span> <span data-ttu-id="a31cb-184">提供されている場合、システムはそれを使用しようとし、使用できない場合は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a31cb-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="a31cb-185">提供されていない場合は、システムが生成します。</span><span class="sxs-lookup"><span data-stu-id="a31cb-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="a31cb-186">制限のあるフィールド</span><span class="sxs-lookup"><span data-stu-id="a31cb-186">Restricted fields</span></span>

<span data-ttu-id="a31cb-187">以下の表は、**作成** と **編集** が制限されるフィールドを定義しています。</span><span class="sxs-lookup"><span data-stu-id="a31cb-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="a31cb-188">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a31cb-188">Project task</span></span>

| <span data-ttu-id="a31cb-189">**論理名**</span><span class="sxs-lookup"><span data-stu-id="a31cb-189">**Logical name**</span></span>                       | <span data-ttu-id="a31cb-190">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-190">**Can create**</span></span> | <span data-ttu-id="a31cb-191">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="a31cb-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="a31cb-193">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-193">no</span></span>             | <span data-ttu-id="a31cb-194">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-194">no</span></span>               |
| <span data-ttu-id="a31cb-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="a31cb-196">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-196">no</span></span>             | <span data-ttu-id="a31cb-197">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-197">no</span></span>               |
| <span data-ttu-id="a31cb-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="a31cb-198">msdyn_actualend</span></span>                        | <span data-ttu-id="a31cb-199">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-199">no</span></span>             | <span data-ttu-id="a31cb-200">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-200">no</span></span>               |
| <span data-ttu-id="a31cb-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="a31cb-202">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-202">no</span></span>             | <span data-ttu-id="a31cb-203">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-203">no</span></span>               |
| <span data-ttu-id="a31cb-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="a31cb-205">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-205">no</span></span>             | <span data-ttu-id="a31cb-206">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-206">no</span></span>               |
| <span data-ttu-id="a31cb-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="a31cb-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="a31cb-208">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-208">no</span></span>             | <span data-ttu-id="a31cb-209">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-209">no</span></span>               |
| <span data-ttu-id="a31cb-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="a31cb-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="a31cb-211">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-211">no</span></span>             | <span data-ttu-id="a31cb-212">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-212">no</span></span>               |
| <span data-ttu-id="a31cb-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="a31cb-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-214">no</span></span>             | <span data-ttu-id="a31cb-215">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-215">no</span></span>               |
| <span data-ttu-id="a31cb-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="a31cb-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="a31cb-217">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-217">no</span></span>             | <span data-ttu-id="a31cb-218">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-218">no</span></span>               |
| <span data-ttu-id="a31cb-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a31cb-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="a31cb-220">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-220">no</span></span>             | <span data-ttu-id="a31cb-221">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-221">no</span></span>               |
| <span data-ttu-id="a31cb-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a31cb-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="a31cb-223">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-223">no</span></span>             | <span data-ttu-id="a31cb-224">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-224">no</span></span>               |
| <span data-ttu-id="a31cb-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="a31cb-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="a31cb-226">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-226">no</span></span>             | <span data-ttu-id="a31cb-227">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-227">no</span></span>               |
| <span data-ttu-id="a31cb-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="a31cb-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="a31cb-229">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-229">no</span></span>             | <span data-ttu-id="a31cb-230">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-230">no</span></span>               |
| <span data-ttu-id="a31cb-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="a31cb-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="a31cb-232">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-232">no</span></span>             | <span data-ttu-id="a31cb-233">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-233">no</span></span>               |
| <span data-ttu-id="a31cb-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="a31cb-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="a31cb-235">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-235">no</span></span>             | <span data-ttu-id="a31cb-236">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-236">no</span></span>               |
| <span data-ttu-id="a31cb-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="a31cb-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="a31cb-238">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-238">no</span></span>             | <span data-ttu-id="a31cb-239">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-239">no</span></span>               |
| <span data-ttu-id="a31cb-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="a31cb-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="a31cb-241">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-241">no</span></span>             | <span data-ttu-id="a31cb-242">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-242">no</span></span>               |
| <span data-ttu-id="a31cb-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="a31cb-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="a31cb-244">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-244">no</span></span>             | <span data-ttu-id="a31cb-245">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-245">no</span></span>               |
| <span data-ttu-id="a31cb-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="a31cb-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="a31cb-247">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-247">no</span></span>             | <span data-ttu-id="a31cb-248">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-248">no</span></span>               |
| <span data-ttu-id="a31cb-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="a31cb-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="a31cb-250">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-250">no</span></span>             | <span data-ttu-id="a31cb-251">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-251">no</span></span>               |
| <span data-ttu-id="a31cb-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="a31cb-253">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-253">no</span></span>             | <span data-ttu-id="a31cb-254">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-254">no</span></span>               |
| <span data-ttu-id="a31cb-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="a31cb-256">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-256">no</span></span>             | <span data-ttu-id="a31cb-257">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-257">no</span></span>               |
| <span data-ttu-id="a31cb-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="a31cb-259">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-259">no</span></span>             | <span data-ttu-id="a31cb-260">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-260">no</span></span>               |
| <span data-ttu-id="a31cb-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="a31cb-262">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-262">no</span></span>             | <span data-ttu-id="a31cb-263">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-263">no</span></span>               |
| <span data-ttu-id="a31cb-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="a31cb-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="a31cb-265">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-265">no</span></span>             | <span data-ttu-id="a31cb-266">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-266">no</span></span>               |
| <span data-ttu-id="a31cb-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="a31cb-267">msdyn_progress</span></span>                         | <span data-ttu-id="a31cb-268">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-268">no</span></span>             | <span data-ttu-id="a31cb-269">いいえ (P4W の場合は"はい")</span><span class="sxs-lookup"><span data-stu-id="a31cb-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="a31cb-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="a31cb-271">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-271">no</span></span>             | <span data-ttu-id="a31cb-272">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-272">no</span></span>               |
| <span data-ttu-id="a31cb-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="a31cb-274">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-274">no</span></span>             | <span data-ttu-id="a31cb-275">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-275">no</span></span>               |
| <span data-ttu-id="a31cb-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="a31cb-277">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-277">no</span></span>             | <span data-ttu-id="a31cb-278">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-278">no</span></span>               |
| <span data-ttu-id="a31cb-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="a31cb-280">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-280">no</span></span>             | <span data-ttu-id="a31cb-281">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-281">no</span></span>               |
| <span data-ttu-id="a31cb-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="a31cb-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="a31cb-283">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-283">no</span></span>             | <span data-ttu-id="a31cb-284">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-284">no</span></span>               |
| <span data-ttu-id="a31cb-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a31cb-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="a31cb-286">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-286">no</span></span>             | <span data-ttu-id="a31cb-287">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-287">no</span></span>               |
| <span data-ttu-id="a31cb-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="a31cb-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="a31cb-289">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-289">no</span></span>             | <span data-ttu-id="a31cb-290">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-290">no</span></span>               |
| <span data-ttu-id="a31cb-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="a31cb-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="a31cb-292">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-292">no</span></span>             | <span data-ttu-id="a31cb-293">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-293">no</span></span>               |
| <span data-ttu-id="a31cb-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="a31cb-295">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-295">no</span></span>             | <span data-ttu-id="a31cb-296">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-296">no</span></span>               |
| <span data-ttu-id="a31cb-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="a31cb-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="a31cb-298">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-298">no</span></span>             | <span data-ttu-id="a31cb-299">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-299">no</span></span>               |
| <span data-ttu-id="a31cb-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a31cb-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="a31cb-301">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-301">no</span></span>             | <span data-ttu-id="a31cb-302">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-302">no</span></span>               |
| <span data-ttu-id="a31cb-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="a31cb-304">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-304">no</span></span>             | <span data-ttu-id="a31cb-305">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-305">no</span></span>               |
| <span data-ttu-id="a31cb-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="a31cb-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="a31cb-307">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-307">no</span></span>             | <span data-ttu-id="a31cb-308">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-308">no</span></span>               |
| <span data-ttu-id="a31cb-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="a31cb-310">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-310">no</span></span>             | <span data-ttu-id="a31cb-311">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-311">no</span></span>               |
| <span data-ttu-id="a31cb-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="a31cb-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="a31cb-313">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-313">no</span></span>             | <span data-ttu-id="a31cb-314">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-314">no</span></span>               |
| <span data-ttu-id="a31cb-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="a31cb-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="a31cb-316">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-316">no</span></span>             | <span data-ttu-id="a31cb-317">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-317">no</span></span>               |
| <span data-ttu-id="a31cb-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="a31cb-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="a31cb-319">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-319">no</span></span>             | <span data-ttu-id="a31cb-320">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-320">no</span></span>               |
| <span data-ttu-id="a31cb-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="a31cb-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="a31cb-322">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-322">no</span></span>             | <span data-ttu-id="a31cb-323">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-323">no</span></span>               |
| <span data-ttu-id="a31cb-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="a31cb-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="a31cb-325">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-325">no</span></span>             | <span data-ttu-id="a31cb-326">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-326">no</span></span>               |
| <span data-ttu-id="a31cb-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="a31cb-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="a31cb-328">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-328">no</span></span>             | <span data-ttu-id="a31cb-329">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-329">no</span></span>               |
| <span data-ttu-id="a31cb-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="a31cb-330">msdyn_summary</span></span>                          | <span data-ttu-id="a31cb-331">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-331">no</span></span>             | <span data-ttu-id="a31cb-332">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-332">no</span></span>               |
| <span data-ttu-id="a31cb-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="a31cb-334">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-334">no</span></span>             | <span data-ttu-id="a31cb-335">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-335">no</span></span>               |
| <span data-ttu-id="a31cb-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="a31cb-337">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-337">no</span></span>             | <span data-ttu-id="a31cb-338">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="a31cb-339">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="a31cb-339">Project task dependency</span></span>

| <span data-ttu-id="a31cb-340">**論理名**</span><span class="sxs-lookup"><span data-stu-id="a31cb-340">**Logical name**</span></span>              | <span data-ttu-id="a31cb-341">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-341">**Can create**</span></span> | <span data-ttu-id="a31cb-342">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="a31cb-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="a31cb-343">msdyn_linktype</span></span>                | <span data-ttu-id="a31cb-344">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-344">no</span></span>             | <span data-ttu-id="a31cb-345">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-345">no</span></span>           |
| <span data-ttu-id="a31cb-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="a31cb-346">msdyn_linktypename</span></span>            | <span data-ttu-id="a31cb-347">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-347">no</span></span>             | <span data-ttu-id="a31cb-348">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-348">no</span></span>           |
| <span data-ttu-id="a31cb-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="a31cb-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="a31cb-350">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-350">yes</span></span>            | <span data-ttu-id="a31cb-351">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-351">no</span></span>           |
| <span data-ttu-id="a31cb-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="a31cb-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="a31cb-353">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-353">yes</span></span>            | <span data-ttu-id="a31cb-354">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-354">no</span></span>           |
| <span data-ttu-id="a31cb-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a31cb-355">msdyn_project</span></span>                 | <span data-ttu-id="a31cb-356">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-356">yes</span></span>            | <span data-ttu-id="a31cb-357">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-357">no</span></span>           |
| <span data-ttu-id="a31cb-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="a31cb-358">msdyn_projectname</span></span>             | <span data-ttu-id="a31cb-359">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-359">yes</span></span>            | <span data-ttu-id="a31cb-360">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-360">no</span></span>           |
| <span data-ttu-id="a31cb-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="a31cb-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="a31cb-362">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-362">yes</span></span>            | <span data-ttu-id="a31cb-363">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-363">no</span></span>           |
| <span data-ttu-id="a31cb-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="a31cb-364">msdyn_successortask</span></span>           | <span data-ttu-id="a31cb-365">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-365">yes</span></span>            | <span data-ttu-id="a31cb-366">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-366">no</span></span>           |
| <span data-ttu-id="a31cb-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="a31cb-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="a31cb-368">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-368">yes</span></span>            | <span data-ttu-id="a31cb-369">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="a31cb-370">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="a31cb-370">Resource assignment</span></span>

| <span data-ttu-id="a31cb-371">**論理名**</span><span class="sxs-lookup"><span data-stu-id="a31cb-371">**Logical name**</span></span>             | <span data-ttu-id="a31cb-372">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-372">**Can create**</span></span> | <span data-ttu-id="a31cb-373">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="a31cb-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="a31cb-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="a31cb-375">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-375">yes</span></span>            | <span data-ttu-id="a31cb-376">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-376">no</span></span>           |
| <span data-ttu-id="a31cb-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="a31cb-378">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-378">yes</span></span>            | <span data-ttu-id="a31cb-379">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-379">no</span></span>           |
| <span data-ttu-id="a31cb-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="a31cb-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="a31cb-381">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-381">no</span></span>             | <span data-ttu-id="a31cb-382">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-382">no</span></span>           |
| <span data-ttu-id="a31cb-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="a31cb-384">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-384">no</span></span>             | <span data-ttu-id="a31cb-385">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-385">no</span></span>           |
| <span data-ttu-id="a31cb-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="a31cb-386">msdyn_committype</span></span>             | <span data-ttu-id="a31cb-387">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-387">no</span></span>             | <span data-ttu-id="a31cb-388">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-388">no</span></span>           |
| <span data-ttu-id="a31cb-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="a31cb-389">msdyn_committypename</span></span>         | <span data-ttu-id="a31cb-390">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-390">no</span></span>             | <span data-ttu-id="a31cb-391">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-391">no</span></span>           |
| <span data-ttu-id="a31cb-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a31cb-392">msdyn_effort</span></span>                 | <span data-ttu-id="a31cb-393">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-393">no</span></span>             | <span data-ttu-id="a31cb-394">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-394">no</span></span>           |
| <span data-ttu-id="a31cb-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a31cb-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="a31cb-396">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-396">no</span></span>             | <span data-ttu-id="a31cb-397">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-397">no</span></span>           |
| <span data-ttu-id="a31cb-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a31cb-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="a31cb-399">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-399">no</span></span>             | <span data-ttu-id="a31cb-400">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-400">no</span></span>           |
| <span data-ttu-id="a31cb-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a31cb-401">msdyn_finish</span></span>                 | <span data-ttu-id="a31cb-402">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-402">no</span></span>             | <span data-ttu-id="a31cb-403">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-403">no</span></span>           |
| <span data-ttu-id="a31cb-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="a31cb-405">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-405">no</span></span>             | <span data-ttu-id="a31cb-406">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-406">no</span></span>           |
| <span data-ttu-id="a31cb-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="a31cb-408">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-408">no</span></span>             | <span data-ttu-id="a31cb-409">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-409">no</span></span>           |
| <span data-ttu-id="a31cb-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="a31cb-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="a31cb-411">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-411">no</span></span>             | <span data-ttu-id="a31cb-412">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-412">no</span></span>           |
| <span data-ttu-id="a31cb-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="a31cb-414">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-414">no</span></span>             | <span data-ttu-id="a31cb-415">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-415">no</span></span>           |
| <span data-ttu-id="a31cb-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="a31cb-417">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-417">no</span></span>             | <span data-ttu-id="a31cb-418">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-418">no</span></span>           |
| <span data-ttu-id="a31cb-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="a31cb-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="a31cb-420">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-420">no</span></span>             | <span data-ttu-id="a31cb-421">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-421">no</span></span>           |
| <span data-ttu-id="a31cb-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="a31cb-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="a31cb-423">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-423">no</span></span>             | <span data-ttu-id="a31cb-424">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-424">no</span></span>           |
| <span data-ttu-id="a31cb-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="a31cb-425">msdyn_projectid</span></span>              | <span data-ttu-id="a31cb-426">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-426">yes</span></span>            | <span data-ttu-id="a31cb-427">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-427">no</span></span>           |
| <span data-ttu-id="a31cb-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-428">msdyn_projectidname</span></span>          | <span data-ttu-id="a31cb-429">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-429">no</span></span>             | <span data-ttu-id="a31cb-430">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-430">no</span></span>           |
| <span data-ttu-id="a31cb-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="a31cb-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="a31cb-432">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-432">no</span></span>             | <span data-ttu-id="a31cb-433">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-433">no</span></span>           |
| <span data-ttu-id="a31cb-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="a31cb-435">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-435">no</span></span>             | <span data-ttu-id="a31cb-436">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-436">no</span></span>           |
| <span data-ttu-id="a31cb-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="a31cb-437">msdyn_start</span></span>                  | <span data-ttu-id="a31cb-438">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-438">no</span></span>             | <span data-ttu-id="a31cb-439">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-439">no</span></span>           |
| <span data-ttu-id="a31cb-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="a31cb-440">msdyn_taskid</span></span>                 | <span data-ttu-id="a31cb-441">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-441">no</span></span>             | <span data-ttu-id="a31cb-442">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-442">no</span></span>           |
| <span data-ttu-id="a31cb-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-443">msdyn_taskidname</span></span>             | <span data-ttu-id="a31cb-444">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-444">no</span></span>             | <span data-ttu-id="a31cb-445">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-445">no</span></span>           |
| <span data-ttu-id="a31cb-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="a31cb-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="a31cb-447">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-447">no</span></span>             | <span data-ttu-id="a31cb-448">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="a31cb-449">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="a31cb-449">Project team member</span></span>

| <span data-ttu-id="a31cb-450">**論理名**</span><span class="sxs-lookup"><span data-stu-id="a31cb-450">**Logical name**</span></span>                                 | <span data-ttu-id="a31cb-451">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-451">**Can create**</span></span> | <span data-ttu-id="a31cb-452">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="a31cb-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="a31cb-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="a31cb-454">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-454">no</span></span>             | <span data-ttu-id="a31cb-455">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-455">no</span></span>           |
| <span data-ttu-id="a31cb-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="a31cb-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="a31cb-457">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-457">no</span></span>             | <span data-ttu-id="a31cb-458">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-458">no</span></span>           |
| <span data-ttu-id="a31cb-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="a31cb-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="a31cb-460">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-460">no</span></span>             | <span data-ttu-id="a31cb-461">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-461">no</span></span>           |
| <span data-ttu-id="a31cb-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="a31cb-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="a31cb-463">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-463">no</span></span>             | <span data-ttu-id="a31cb-464">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-464">no</span></span>           |
| <span data-ttu-id="a31cb-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a31cb-465">msdyn_effort</span></span>                                     | <span data-ttu-id="a31cb-466">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-466">no</span></span>             | <span data-ttu-id="a31cb-467">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-467">no</span></span>           |
| <span data-ttu-id="a31cb-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a31cb-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="a31cb-469">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-469">no</span></span>             | <span data-ttu-id="a31cb-470">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-470">no</span></span>           |
| <span data-ttu-id="a31cb-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a31cb-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="a31cb-472">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-472">no</span></span>             | <span data-ttu-id="a31cb-473">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-473">no</span></span>           |
| <span data-ttu-id="a31cb-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a31cb-474">msdyn_finish</span></span>                                     | <span data-ttu-id="a31cb-475">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-475">no</span></span>             | <span data-ttu-id="a31cb-476">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-476">no</span></span>           |
| <span data-ttu-id="a31cb-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="a31cb-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="a31cb-478">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-478">no</span></span>             | <span data-ttu-id="a31cb-479">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-479">no</span></span>           |
| <span data-ttu-id="a31cb-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="a31cb-480">msdyn_hours</span></span>                                      | <span data-ttu-id="a31cb-481">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-481">no</span></span>             | <span data-ttu-id="a31cb-482">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-482">no</span></span>           |
| <span data-ttu-id="a31cb-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="a31cb-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="a31cb-484">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-484">no</span></span>             | <span data-ttu-id="a31cb-485">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-485">no</span></span>           |
| <span data-ttu-id="a31cb-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="a31cb-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="a31cb-487">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-487">no</span></span>             | <span data-ttu-id="a31cb-488">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-488">no</span></span>           |
| <span data-ttu-id="a31cb-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="a31cb-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="a31cb-490">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-490">no</span></span>             | <span data-ttu-id="a31cb-491">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-491">no</span></span>           |
| <span data-ttu-id="a31cb-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="a31cb-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="a31cb-493">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-493">no</span></span>             | <span data-ttu-id="a31cb-494">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-494">no</span></span>           |
| <span data-ttu-id="a31cb-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="a31cb-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="a31cb-496">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-496">no</span></span>             | <span data-ttu-id="a31cb-497">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-497">no</span></span>           |
| <span data-ttu-id="a31cb-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="a31cb-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="a31cb-499">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-499">no</span></span>             | <span data-ttu-id="a31cb-500">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-500">no</span></span>           |
| <span data-ttu-id="a31cb-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="a31cb-501">msdyn_start</span></span>                                      | <span data-ttu-id="a31cb-502">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-502">no</span></span>             | <span data-ttu-id="a31cb-503">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="a31cb-504">Project</span><span class="sxs-lookup"><span data-stu-id="a31cb-504">Project</span></span>

| <span data-ttu-id="a31cb-505">**論理名**</span><span class="sxs-lookup"><span data-stu-id="a31cb-505">**Logical name**</span></span>                       | <span data-ttu-id="a31cb-506">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-506">**Can create**</span></span> | <span data-ttu-id="a31cb-507">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="a31cb-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="a31cb-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="a31cb-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="a31cb-509">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-509">no</span></span>             | <span data-ttu-id="a31cb-510">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-510">no</span></span>           |
| <span data-ttu-id="a31cb-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="a31cb-512">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-512">no</span></span>             | <span data-ttu-id="a31cb-513">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-513">no</span></span>           |
| <span data-ttu-id="a31cb-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="a31cb-515">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-515">no</span></span>             | <span data-ttu-id="a31cb-516">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-516">no</span></span>           |
| <span data-ttu-id="a31cb-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="a31cb-518">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-518">no</span></span>             | <span data-ttu-id="a31cb-519">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-519">no</span></span>           |
| <span data-ttu-id="a31cb-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="a31cb-521">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-521">no</span></span>             | <span data-ttu-id="a31cb-522">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-522">no</span></span>           |
| <span data-ttu-id="a31cb-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="a31cb-524">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-524">no</span></span>             | <span data-ttu-id="a31cb-525">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-525">no</span></span>           |
| <span data-ttu-id="a31cb-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="a31cb-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="a31cb-527">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-527">yes</span></span>            | <span data-ttu-id="a31cb-528">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-528">no</span></span>           |
| <span data-ttu-id="a31cb-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="a31cb-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="a31cb-530">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-530">yes</span></span>            | <span data-ttu-id="a31cb-531">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-531">no</span></span>           |
| <span data-ttu-id="a31cb-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="a31cb-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="a31cb-533">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-533">yes</span></span>            | <span data-ttu-id="a31cb-534">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-534">no</span></span>           |
| <span data-ttu-id="a31cb-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="a31cb-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="a31cb-536">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-536">no</span></span>             | <span data-ttu-id="a31cb-537">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-537">no</span></span>           |
| <span data-ttu-id="a31cb-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a31cb-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="a31cb-539">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-539">no</span></span>             | <span data-ttu-id="a31cb-540">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-540">no</span></span>           |
| <span data-ttu-id="a31cb-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="a31cb-542">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-542">no</span></span>             | <span data-ttu-id="a31cb-543">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-543">no</span></span>           |
| <span data-ttu-id="a31cb-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="a31cb-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="a31cb-545">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-545">no</span></span>             | <span data-ttu-id="a31cb-546">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-546">no</span></span>           |
| <span data-ttu-id="a31cb-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="a31cb-548">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-548">no</span></span>             | <span data-ttu-id="a31cb-549">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-549">no</span></span>           |
| <span data-ttu-id="a31cb-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="a31cb-550">msdyn_duration</span></span>                         | <span data-ttu-id="a31cb-551">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-551">no</span></span>             | <span data-ttu-id="a31cb-552">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-552">no</span></span>           |
| <span data-ttu-id="a31cb-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a31cb-553">msdyn_effort</span></span>                           | <span data-ttu-id="a31cb-554">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-554">no</span></span>             | <span data-ttu-id="a31cb-555">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-555">no</span></span>           |
| <span data-ttu-id="a31cb-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a31cb-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="a31cb-557">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-557">no</span></span>             | <span data-ttu-id="a31cb-558">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-558">no</span></span>           |
| <span data-ttu-id="a31cb-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="a31cb-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="a31cb-560">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-560">no</span></span>             | <span data-ttu-id="a31cb-561">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-561">no</span></span>           |
| <span data-ttu-id="a31cb-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a31cb-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="a31cb-563">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-563">no</span></span>             | <span data-ttu-id="a31cb-564">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-564">no</span></span>           |
| <span data-ttu-id="a31cb-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a31cb-565">msdyn_finish</span></span>                           | <span data-ttu-id="a31cb-566">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-566">yes</span></span>            | <span data-ttu-id="a31cb-567">はい</span><span class="sxs-lookup"><span data-stu-id="a31cb-567">yes</span></span>          |
| <span data-ttu-id="a31cb-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="a31cb-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="a31cb-569">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-569">no</span></span>             | <span data-ttu-id="a31cb-570">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-570">no</span></span>           |
| <span data-ttu-id="a31cb-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="a31cb-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="a31cb-572">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-572">no</span></span>             | <span data-ttu-id="a31cb-573">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-573">no</span></span>           |
| <span data-ttu-id="a31cb-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="a31cb-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="a31cb-575">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-575">no</span></span>             | <span data-ttu-id="a31cb-576">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-576">no</span></span>           |
| <span data-ttu-id="a31cb-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="a31cb-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="a31cb-578">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-578">no</span></span>             | <span data-ttu-id="a31cb-579">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-579">no</span></span>           |
| <span data-ttu-id="a31cb-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="a31cb-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="a31cb-581">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-581">no</span></span>             | <span data-ttu-id="a31cb-582">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-582">no</span></span>           |
| <span data-ttu-id="a31cb-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="a31cb-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="a31cb-584">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-584">no</span></span>             | <span data-ttu-id="a31cb-585">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-585">no</span></span>           |
| <span data-ttu-id="a31cb-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="a31cb-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="a31cb-587">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-587">no</span></span>             | <span data-ttu-id="a31cb-588">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-588">no</span></span>           |
| <span data-ttu-id="a31cb-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="a31cb-590">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-590">no</span></span>             | <span data-ttu-id="a31cb-591">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-591">no</span></span>           |
| <span data-ttu-id="a31cb-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="a31cb-593">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-593">no</span></span>             | <span data-ttu-id="a31cb-594">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-594">no</span></span>           |
| <span data-ttu-id="a31cb-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="a31cb-596">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-596">no</span></span>             | <span data-ttu-id="a31cb-597">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-597">no</span></span>           |
| <span data-ttu-id="a31cb-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="a31cb-599">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-599">no</span></span>             | <span data-ttu-id="a31cb-600">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-600">no</span></span>           |
| <span data-ttu-id="a31cb-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="a31cb-602">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-602">no</span></span>             | <span data-ttu-id="a31cb-603">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-603">no</span></span>           |
| <span data-ttu-id="a31cb-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="a31cb-604">msdyn_progress</span></span>                         | <span data-ttu-id="a31cb-605">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-605">no</span></span>             | <span data-ttu-id="a31cb-606">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-606">no</span></span>           |
| <span data-ttu-id="a31cb-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="a31cb-608">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-608">no</span></span>             | <span data-ttu-id="a31cb-609">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-609">no</span></span>           |
| <span data-ttu-id="a31cb-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="a31cb-611">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-611">no</span></span>             | <span data-ttu-id="a31cb-612">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-612">no</span></span>           |
| <span data-ttu-id="a31cb-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a31cb-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="a31cb-614">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-614">no</span></span>             | <span data-ttu-id="a31cb-615">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-615">no</span></span>           |
| <span data-ttu-id="a31cb-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="a31cb-617">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-617">no</span></span>             | <span data-ttu-id="a31cb-618">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-618">no</span></span>           |
| <span data-ttu-id="a31cb-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="a31cb-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="a31cb-620">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-620">no</span></span>             | <span data-ttu-id="a31cb-621">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-621">no</span></span>           |
| <span data-ttu-id="a31cb-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="a31cb-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="a31cb-623">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-623">no</span></span>             | <span data-ttu-id="a31cb-624">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-624">no</span></span>           |
| <span data-ttu-id="a31cb-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="a31cb-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="a31cb-626">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-626">no</span></span>             | <span data-ttu-id="a31cb-627">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-627">no</span></span>           |
| <span data-ttu-id="a31cb-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="a31cb-629">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-629">no</span></span>             | <span data-ttu-id="a31cb-630">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-630">no</span></span>           |
| <span data-ttu-id="a31cb-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="a31cb-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="a31cb-632">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-632">no</span></span>             | <span data-ttu-id="a31cb-633">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-633">no</span></span>           |
| <span data-ttu-id="a31cb-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="a31cb-635">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-635">no</span></span>             | <span data-ttu-id="a31cb-636">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-636">no</span></span>           |
| <span data-ttu-id="a31cb-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="a31cb-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="a31cb-638">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-638">no</span></span>             | <span data-ttu-id="a31cb-639">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-639">no</span></span>           |
| <span data-ttu-id="a31cb-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="a31cb-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="a31cb-641">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-641">no</span></span>             | <span data-ttu-id="a31cb-642">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-642">no</span></span>           |
| <span data-ttu-id="a31cb-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="a31cb-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="a31cb-644">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-644">no</span></span>             | <span data-ttu-id="a31cb-645">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-645">no</span></span>           |
| <span data-ttu-id="a31cb-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="a31cb-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="a31cb-647">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-647">no</span></span>             | <span data-ttu-id="a31cb-648">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-648">no</span></span>           |
| <span data-ttu-id="a31cb-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="a31cb-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="a31cb-650">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-650">no</span></span>             | <span data-ttu-id="a31cb-651">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-651">no</span></span>           |
| <span data-ttu-id="a31cb-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="a31cb-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="a31cb-653">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-653">no</span></span>             | <span data-ttu-id="a31cb-654">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-654">no</span></span>           |
| <span data-ttu-id="a31cb-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="a31cb-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="a31cb-656">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-656">no</span></span>             | <span data-ttu-id="a31cb-657">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-657">no</span></span>           |
| <span data-ttu-id="a31cb-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="a31cb-659">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-659">no</span></span>             | <span data-ttu-id="a31cb-660">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-660">no</span></span>           |
| <span data-ttu-id="a31cb-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="a31cb-662">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-662">no</span></span>             | <span data-ttu-id="a31cb-663">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-663">no</span></span>           |
| <span data-ttu-id="a31cb-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="a31cb-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="a31cb-665">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-665">no</span></span>             | <span data-ttu-id="a31cb-666">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-666">no</span></span>           |
| <span data-ttu-id="a31cb-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a31cb-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="a31cb-668">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-668">no</span></span>             | <span data-ttu-id="a31cb-669">いいえ</span><span class="sxs-lookup"><span data-stu-id="a31cb-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="a31cb-670">制限事項と既知の問題</span><span class="sxs-lookup"><span data-stu-id="a31cb-670">Limitations and known issues</span></span>
<span data-ttu-id="a31cb-671">以下は、制限事項と既知の問題のリストです。</span><span class="sxs-lookup"><span data-stu-id="a31cb-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="a31cb-672">スケジュール API は、**Microsoft Project ライセンスを持つユーザー** のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="a31cb-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="a31cb-673">次のユーザーは使用できません:</span><span class="sxs-lookup"><span data-stu-id="a31cb-673">They can't be used by:</span></span>
    - <span data-ttu-id="a31cb-674">アプリケーション ユーザー</span><span class="sxs-lookup"><span data-stu-id="a31cb-674">Application users</span></span>
    - <span data-ttu-id="a31cb-675">システム ユーザー</span><span class="sxs-lookup"><span data-stu-id="a31cb-675">System users</span></span>
    - <span data-ttu-id="a31cb-676">統合ユーザー</span><span class="sxs-lookup"><span data-stu-id="a31cb-676">Integration users</span></span>
    - <span data-ttu-id="a31cb-677">必要なライセンスを持っていない他のユーザー</span><span class="sxs-lookup"><span data-stu-id="a31cb-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="a31cb-678">各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。</span><span class="sxs-lookup"><span data-stu-id="a31cb-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="a31cb-679">各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。</span><span class="sxs-lookup"><span data-stu-id="a31cb-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="a31cb-680">Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a31cb-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="a31cb-681">**OperationSet** 障害ステータスと障害ログは現在利用できません。</span><span class="sxs-lookup"><span data-stu-id="a31cb-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="a31cb-682">スケジュール API はパブリック プレビューにあります。</span><span class="sxs-lookup"><span data-stu-id="a31cb-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="a31cb-683">実稼働環境におけるこれらの API の使用は、Microsoft ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a31cb-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="a31cb-684">プロジェクトとタスクの制限と境界</span><span class="sxs-lookup"><span data-stu-id="a31cb-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="a31cb-685">エラー処理</span><span class="sxs-lookup"><span data-stu-id="a31cb-685">Error handling</span></span>

   - <span data-ttu-id="a31cb-686">操作セットから生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **操作セット** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="a31cb-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="a31cb-687">Project Scheduling Service で生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **PSS エラーログ** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="a31cb-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="a31cb-688">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="a31cb-688">Sample scenario</span></span>

<span data-ttu-id="a31cb-689">このシナリオでは、プロジェクト、チームメンバー、4 つのタスク、および 2 つのリソース割り当てを作成します。</span><span class="sxs-lookup"><span data-stu-id="a31cb-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="a31cb-690">次に、1 つのタスクを更新し、プロジェクトを更新し、1 つのタスクを削除し、1 つのリソース割り当てを削除して、タスクの依存関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="a31cb-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="a31cb-691">追加の例</span><span class="sxs-lookup"><span data-stu-id="a31cb-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
