---
title: スケジュール API を使用して、スケジューリング エンティティで操作を実行する
description: このトピックは、スケジュール API を使用するための情報とサンプルを提供します。
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116803"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="df5e4-103">スケジュール API を使用して、スケジューリング エンティティで操作を実行する</span><span class="sxs-lookup"><span data-stu-id="df5e4-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="df5e4-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="df5e4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="df5e4-105">このトピックに記載されている機能の一部または全部は、プレビュー リリースの一部として提供されています。</span><span class="sxs-lookup"><span data-stu-id="df5e4-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="df5e4-106">コンテンツおよび機能は変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="df5e4-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="df5e4-107">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="df5e4-107">Scheduling entities</span></span>

<span data-ttu-id="df5e4-108">スケジュール API は、**スケジューリング エンティティ** を使って操作を作成、更新、および削除を実行する機能を提供します。。</span><span class="sxs-lookup"><span data-stu-id="df5e4-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="df5e4-109">これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="df5e4-110">**スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。</span><span class="sxs-lookup"><span data-stu-id="df5e4-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="df5e4-111">次の表は、**スケジューリング エンティティ** の完全なリストです。</span><span class="sxs-lookup"><span data-stu-id="df5e4-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="df5e4-112">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="df5e4-112">Entity name</span></span>  | <span data-ttu-id="df5e4-113">エンティティの論理名</span><span class="sxs-lookup"><span data-stu-id="df5e4-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="df5e4-114">Project</span><span class="sxs-lookup"><span data-stu-id="df5e4-114">Project</span></span> | <span data-ttu-id="df5e4-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="df5e4-115">msdyn_project</span></span> |
| <span data-ttu-id="df5e4-116">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="df5e4-116">Project Task</span></span>  | <span data-ttu-id="df5e4-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="df5e4-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="df5e4-118">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="df5e4-118">Project Task Dependency</span></span>  | <span data-ttu-id="df5e4-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="df5e4-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="df5e4-120">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="df5e4-120">Resource Assignment</span></span> | <span data-ttu-id="df5e4-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="df5e4-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="df5e4-122">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="df5e4-122">Project Bucket</span></span>  | <span data-ttu-id="df5e4-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="df5e4-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="df5e4-124">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="df5e4-124">Project Team Member</span></span> | <span data-ttu-id="df5e4-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="df5e4-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="df5e4-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="df5e4-126">OperationSet</span></span>

<span data-ttu-id="df5e4-127">OperationSet は、スケジュールに影響を与える複数の要求をトランザクション内で処理する必要がある場合に使用できる作業単位パターンです。</span><span class="sxs-lookup"><span data-stu-id="df5e4-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="df5e4-128">スケジュール API</span><span class="sxs-lookup"><span data-stu-id="df5e4-128">Schedule APIs</span></span>

<span data-ttu-id="df5e4-129">以下は、現在のスケジュール API のリストです。</span><span class="sxs-lookup"><span data-stu-id="df5e4-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="df5e4-130">**msdyn_CreateProjectV1**: この API を使用してプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="df5e4-131">プロジェクトとデフォルトのプロジェクト バケットがすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="df5e4-132">**msdyn_CreateTeamMemberV1**: この API を使用して、プロジェクト チーム メンバーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="df5e4-133">チーム メンバーのレコードはすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="df5e4-134">**msdyn_CreateOperationSetV1**: この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="df5e4-135">**msdyn_PSSCreateV1**: この API を使用してエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="df5e4-136">エンティティは、作成操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="df5e4-137">**msdyn_PSSUpdateV1**: この API を使用してエンティティを更新できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="df5e4-138">エンティティは、更新操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="df5e4-139">**msdyn_PSSDeleteV1**: この API を使用してエンティティを削除できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="df5e4-140">エンティティは、削除操作をサポートする任意のスケジューリング エンティティにできます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="df5e4-141">**msdyn_ExecuteOperationSetV1**: この API は、指定された操作セット内のすべての操作を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="df5e4-142">OperationSet と ScheduleAPI の併用</span><span class="sxs-lookup"><span data-stu-id="df5e4-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="df5e4-143">**CreateProjectV1** と **CreateTeamMemberV1** 両方があるレコードは直ちに作成されるため、これらの API は **OperationSet** で直接使用できません。</span><span class="sxs-lookup"><span data-stu-id="df5e4-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="df5e4-144">ただし、API を使用して必要なレコードを作成し、**OperationSet** を作成し、これらの事前に作成されたレコードを **OperationSet** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="df5e4-145">サポートされている操作</span><span class="sxs-lookup"><span data-stu-id="df5e4-145">Supported operations</span></span>

| <span data-ttu-id="df5e4-146">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="df5e4-146">Scheduling entity</span></span> | <span data-ttu-id="df5e4-147">作成​​</span><span class="sxs-lookup"><span data-stu-id="df5e4-147">Create</span></span> | <span data-ttu-id="df5e4-148">更新プログラム</span><span class="sxs-lookup"><span data-stu-id="df5e4-148">Update</span></span> | <span data-ttu-id="df5e4-149">Delete キー</span><span class="sxs-lookup"><span data-stu-id="df5e4-149">Delete</span></span> | <span data-ttu-id="df5e4-150">重要な考慮事項</span><span class="sxs-lookup"><span data-stu-id="df5e4-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="df5e4-151">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="df5e4-151">Project task</span></span> | <span data-ttu-id="df5e4-152">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-152">Yes</span></span> | <span data-ttu-id="df5e4-153">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-153">Yes</span></span> | <span data-ttu-id="df5e4-154">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-154">Yes</span></span> | <span data-ttu-id="df5e4-155">いいえ​​</span><span class="sxs-lookup"><span data-stu-id="df5e4-155">None</span></span> |
| <span data-ttu-id="df5e4-156">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="df5e4-156">Project task dependency</span></span> | <span data-ttu-id="df5e4-157">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-157">Yes</span></span> | <span data-ttu-id="df5e4-158">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-158">Yes</span></span> | | <span data-ttu-id="df5e4-159">プロジェクト タスクの依存関係レコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="df5e4-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="df5e4-160">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="df5e4-161">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="df5e4-161">Resource assignment</span></span> | <span data-ttu-id="df5e4-162">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-162">Yes</span></span> | <span data-ttu-id="df5e4-163">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-163">Yes</span></span> | | <span data-ttu-id="df5e4-164">次のフィールドを使用した操作はサポートされていません: **BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining**、および **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="df5e4-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="df5e4-165">リソース割り当てレコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="df5e4-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="df5e4-166">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="df5e4-167">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="df5e4-167">Project bucket</span></span> | <span data-ttu-id="df5e4-168">N/A</span><span class="sxs-lookup"><span data-stu-id="df5e4-168">N/A</span></span> | <span data-ttu-id="df5e4-169">N/A</span><span class="sxs-lookup"><span data-stu-id="df5e4-169">N/A</span></span> | <span data-ttu-id="df5e4-170">N/A</span><span class="sxs-lookup"><span data-stu-id="df5e4-170">N/A</span></span> | <span data-ttu-id="df5e4-171">既定のバケットは、**CreateProjectV1** API を使って作成されます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="df5e4-172">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="df5e4-172">Project team member</span></span> | <span data-ttu-id="df5e4-173">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-173">Yes</span></span> | <span data-ttu-id="df5e4-174">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-174">Yes</span></span> | <span data-ttu-id="df5e4-175">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-175">Yes</span></span> | <span data-ttu-id="df5e4-176">作成操作には、**CreateTeamMemberV1** API を使用します。</span><span class="sxs-lookup"><span data-stu-id="df5e4-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="df5e4-177">Project</span><span class="sxs-lookup"><span data-stu-id="df5e4-177">Project</span></span> | <span data-ttu-id="df5e4-178">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-178">Yes</span></span> | <span data-ttu-id="df5e4-179">有効</span><span class="sxs-lookup"><span data-stu-id="df5e4-179">Yes</span></span> | <span data-ttu-id="df5e4-180">N/A</span><span class="sxs-lookup"><span data-stu-id="df5e4-180">N/A</span></span> | <span data-ttu-id="df5e4-181">次のフィールドを使用した操作はサポートされていません: **StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、 **CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart**、および **Duration**。</span><span class="sxs-lookup"><span data-stu-id="df5e4-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="df5e4-182">これらの API は、カスタムフィールドを含むエンティティ オブジェクトを使用して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="df5e4-183">ID プロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="df5e4-183">The ID property is optional.</span></span> <span data-ttu-id="df5e4-184">提供されている場合、システムはそれを使用しようとし、使用できない場合は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="df5e4-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="df5e4-185">提供されていない場合は、システムが生成します。</span><span class="sxs-lookup"><span data-stu-id="df5e4-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="df5e4-186">制限のあるフィールド</span><span class="sxs-lookup"><span data-stu-id="df5e4-186">Restricted fields</span></span>

<span data-ttu-id="df5e4-187">以下の表は、**作成** と **編集** が制限されるフィールドを定義しています。</span><span class="sxs-lookup"><span data-stu-id="df5e4-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="df5e4-188">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="df5e4-188">Project task</span></span>

| <span data-ttu-id="df5e4-189">**論理名**</span><span class="sxs-lookup"><span data-stu-id="df5e4-189">**Logical name**</span></span>                       | <span data-ttu-id="df5e4-190">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-190">**Can create**</span></span> | <span data-ttu-id="df5e4-191">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="df5e4-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="df5e4-193">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-193">no</span></span>             | <span data-ttu-id="df5e4-194">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-194">no</span></span>               |
| <span data-ttu-id="df5e4-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="df5e4-196">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-196">no</span></span>             | <span data-ttu-id="df5e4-197">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-197">no</span></span>               |
| <span data-ttu-id="df5e4-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="df5e4-198">msdyn_actualend</span></span>                        | <span data-ttu-id="df5e4-199">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-199">no</span></span>             | <span data-ttu-id="df5e4-200">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-200">no</span></span>               |
| <span data-ttu-id="df5e4-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="df5e4-202">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-202">no</span></span>             | <span data-ttu-id="df5e4-203">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-203">no</span></span>               |
| <span data-ttu-id="df5e4-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="df5e4-205">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-205">no</span></span>             | <span data-ttu-id="df5e4-206">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-206">no</span></span>               |
| <span data-ttu-id="df5e4-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="df5e4-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="df5e4-208">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-208">no</span></span>             | <span data-ttu-id="df5e4-209">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-209">no</span></span>               |
| <span data-ttu-id="df5e4-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="df5e4-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="df5e4-211">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-211">no</span></span>             | <span data-ttu-id="df5e4-212">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-212">no</span></span>               |
| <span data-ttu-id="df5e4-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="df5e4-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-214">no</span></span>             | <span data-ttu-id="df5e4-215">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-215">no</span></span>               |
| <span data-ttu-id="df5e4-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="df5e4-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="df5e4-217">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-217">no</span></span>             | <span data-ttu-id="df5e4-218">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-218">no</span></span>               |
| <span data-ttu-id="df5e4-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="df5e4-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="df5e4-220">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-220">no</span></span>             | <span data-ttu-id="df5e4-221">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-221">no</span></span>               |
| <span data-ttu-id="df5e4-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="df5e4-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="df5e4-223">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-223">no</span></span>             | <span data-ttu-id="df5e4-224">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-224">no</span></span>               |
| <span data-ttu-id="df5e4-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="df5e4-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="df5e4-226">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-226">no</span></span>             | <span data-ttu-id="df5e4-227">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-227">no</span></span>               |
| <span data-ttu-id="df5e4-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="df5e4-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="df5e4-229">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-229">no</span></span>             | <span data-ttu-id="df5e4-230">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-230">no</span></span>               |
| <span data-ttu-id="df5e4-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="df5e4-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="df5e4-232">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-232">no</span></span>             | <span data-ttu-id="df5e4-233">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-233">no</span></span>               |
| <span data-ttu-id="df5e4-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="df5e4-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="df5e4-235">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-235">no</span></span>             | <span data-ttu-id="df5e4-236">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-236">no</span></span>               |
| <span data-ttu-id="df5e4-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="df5e4-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="df5e4-238">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-238">no</span></span>             | <span data-ttu-id="df5e4-239">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-239">no</span></span>               |
| <span data-ttu-id="df5e4-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="df5e4-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="df5e4-241">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-241">no</span></span>             | <span data-ttu-id="df5e4-242">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-242">no</span></span>               |
| <span data-ttu-id="df5e4-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="df5e4-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="df5e4-244">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-244">no</span></span>             | <span data-ttu-id="df5e4-245">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-245">no</span></span>               |
| <span data-ttu-id="df5e4-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="df5e4-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="df5e4-247">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-247">no</span></span>             | <span data-ttu-id="df5e4-248">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-248">no</span></span>               |
| <span data-ttu-id="df5e4-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="df5e4-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="df5e4-250">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-250">no</span></span>             | <span data-ttu-id="df5e4-251">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-251">no</span></span>               |
| <span data-ttu-id="df5e4-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="df5e4-253">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-253">no</span></span>             | <span data-ttu-id="df5e4-254">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-254">no</span></span>               |
| <span data-ttu-id="df5e4-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="df5e4-256">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-256">no</span></span>             | <span data-ttu-id="df5e4-257">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-257">no</span></span>               |
| <span data-ttu-id="df5e4-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="df5e4-259">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-259">no</span></span>             | <span data-ttu-id="df5e4-260">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-260">no</span></span>               |
| <span data-ttu-id="df5e4-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="df5e4-262">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-262">no</span></span>             | <span data-ttu-id="df5e4-263">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-263">no</span></span>               |
| <span data-ttu-id="df5e4-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="df5e4-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="df5e4-265">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-265">no</span></span>             | <span data-ttu-id="df5e4-266">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-266">no</span></span>               |
| <span data-ttu-id="df5e4-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="df5e4-267">msdyn_progress</span></span>                         | <span data-ttu-id="df5e4-268">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-268">no</span></span>             | <span data-ttu-id="df5e4-269">いいえ (P4W の場合は"はい")</span><span class="sxs-lookup"><span data-stu-id="df5e4-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="df5e4-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="df5e4-271">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-271">no</span></span>             | <span data-ttu-id="df5e4-272">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-272">no</span></span>               |
| <span data-ttu-id="df5e4-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="df5e4-274">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-274">no</span></span>             | <span data-ttu-id="df5e4-275">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-275">no</span></span>               |
| <span data-ttu-id="df5e4-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="df5e4-277">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-277">no</span></span>             | <span data-ttu-id="df5e4-278">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-278">no</span></span>               |
| <span data-ttu-id="df5e4-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="df5e4-280">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-280">no</span></span>             | <span data-ttu-id="df5e4-281">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-281">no</span></span>               |
| <span data-ttu-id="df5e4-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="df5e4-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="df5e4-283">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-283">no</span></span>             | <span data-ttu-id="df5e4-284">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-284">no</span></span>               |
| <span data-ttu-id="df5e4-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="df5e4-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="df5e4-286">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-286">no</span></span>             | <span data-ttu-id="df5e4-287">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-287">no</span></span>               |
| <span data-ttu-id="df5e4-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="df5e4-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="df5e4-289">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-289">no</span></span>             | <span data-ttu-id="df5e4-290">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-290">no</span></span>               |
| <span data-ttu-id="df5e4-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="df5e4-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="df5e4-292">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-292">no</span></span>             | <span data-ttu-id="df5e4-293">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-293">no</span></span>               |
| <span data-ttu-id="df5e4-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="df5e4-295">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-295">no</span></span>             | <span data-ttu-id="df5e4-296">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-296">no</span></span>               |
| <span data-ttu-id="df5e4-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="df5e4-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="df5e4-298">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-298">no</span></span>             | <span data-ttu-id="df5e4-299">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-299">no</span></span>               |
| <span data-ttu-id="df5e4-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="df5e4-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="df5e4-301">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-301">no</span></span>             | <span data-ttu-id="df5e4-302">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-302">no</span></span>               |
| <span data-ttu-id="df5e4-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="df5e4-304">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-304">no</span></span>             | <span data-ttu-id="df5e4-305">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-305">no</span></span>               |
| <span data-ttu-id="df5e4-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="df5e4-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="df5e4-307">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-307">no</span></span>             | <span data-ttu-id="df5e4-308">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-308">no</span></span>               |
| <span data-ttu-id="df5e4-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="df5e4-310">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-310">no</span></span>             | <span data-ttu-id="df5e4-311">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-311">no</span></span>               |
| <span data-ttu-id="df5e4-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="df5e4-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="df5e4-313">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-313">no</span></span>             | <span data-ttu-id="df5e4-314">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-314">no</span></span>               |
| <span data-ttu-id="df5e4-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="df5e4-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="df5e4-316">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-316">no</span></span>             | <span data-ttu-id="df5e4-317">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-317">no</span></span>               |
| <span data-ttu-id="df5e4-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="df5e4-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="df5e4-319">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-319">no</span></span>             | <span data-ttu-id="df5e4-320">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-320">no</span></span>               |
| <span data-ttu-id="df5e4-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="df5e4-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="df5e4-322">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-322">no</span></span>             | <span data-ttu-id="df5e4-323">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-323">no</span></span>               |
| <span data-ttu-id="df5e4-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="df5e4-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="df5e4-325">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-325">no</span></span>             | <span data-ttu-id="df5e4-326">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-326">no</span></span>               |
| <span data-ttu-id="df5e4-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="df5e4-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="df5e4-328">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-328">no</span></span>             | <span data-ttu-id="df5e4-329">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-329">no</span></span>               |
| <span data-ttu-id="df5e4-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="df5e4-330">msdyn_summary</span></span>                          | <span data-ttu-id="df5e4-331">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-331">no</span></span>             | <span data-ttu-id="df5e4-332">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-332">no</span></span>               |
| <span data-ttu-id="df5e4-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="df5e4-334">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-334">no</span></span>             | <span data-ttu-id="df5e4-335">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-335">no</span></span>               |
| <span data-ttu-id="df5e4-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="df5e4-337">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-337">no</span></span>             | <span data-ttu-id="df5e4-338">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="df5e4-339">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="df5e4-339">Project task dependency</span></span>

| <span data-ttu-id="df5e4-340">**論理名**</span><span class="sxs-lookup"><span data-stu-id="df5e4-340">**Logical name**</span></span>              | <span data-ttu-id="df5e4-341">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-341">**Can create**</span></span> | <span data-ttu-id="df5e4-342">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="df5e4-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="df5e4-343">msdyn_linktype</span></span>                | <span data-ttu-id="df5e4-344">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-344">no</span></span>             | <span data-ttu-id="df5e4-345">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-345">no</span></span>           |
| <span data-ttu-id="df5e4-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="df5e4-346">msdyn_linktypename</span></span>            | <span data-ttu-id="df5e4-347">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-347">no</span></span>             | <span data-ttu-id="df5e4-348">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-348">no</span></span>           |
| <span data-ttu-id="df5e4-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="df5e4-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="df5e4-350">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-350">yes</span></span>            | <span data-ttu-id="df5e4-351">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-351">no</span></span>           |
| <span data-ttu-id="df5e4-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="df5e4-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="df5e4-353">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-353">yes</span></span>            | <span data-ttu-id="df5e4-354">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-354">no</span></span>           |
| <span data-ttu-id="df5e4-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="df5e4-355">msdyn_project</span></span>                 | <span data-ttu-id="df5e4-356">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-356">yes</span></span>            | <span data-ttu-id="df5e4-357">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-357">no</span></span>           |
| <span data-ttu-id="df5e4-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="df5e4-358">msdyn_projectname</span></span>             | <span data-ttu-id="df5e4-359">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-359">yes</span></span>            | <span data-ttu-id="df5e4-360">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-360">no</span></span>           |
| <span data-ttu-id="df5e4-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="df5e4-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="df5e4-362">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-362">yes</span></span>            | <span data-ttu-id="df5e4-363">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-363">no</span></span>           |
| <span data-ttu-id="df5e4-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="df5e4-364">msdyn_successortask</span></span>           | <span data-ttu-id="df5e4-365">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-365">yes</span></span>            | <span data-ttu-id="df5e4-366">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-366">no</span></span>           |
| <span data-ttu-id="df5e4-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="df5e4-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="df5e4-368">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-368">yes</span></span>            | <span data-ttu-id="df5e4-369">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="df5e4-370">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="df5e4-370">Resource assignment</span></span>

| <span data-ttu-id="df5e4-371">**論理名**</span><span class="sxs-lookup"><span data-stu-id="df5e4-371">**Logical name**</span></span>             | <span data-ttu-id="df5e4-372">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-372">**Can create**</span></span> | <span data-ttu-id="df5e4-373">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="df5e4-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="df5e4-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="df5e4-375">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-375">yes</span></span>            | <span data-ttu-id="df5e4-376">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-376">no</span></span>           |
| <span data-ttu-id="df5e4-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="df5e4-378">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-378">yes</span></span>            | <span data-ttu-id="df5e4-379">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-379">no</span></span>           |
| <span data-ttu-id="df5e4-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="df5e4-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="df5e4-381">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-381">no</span></span>             | <span data-ttu-id="df5e4-382">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-382">no</span></span>           |
| <span data-ttu-id="df5e4-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="df5e4-384">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-384">no</span></span>             | <span data-ttu-id="df5e4-385">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-385">no</span></span>           |
| <span data-ttu-id="df5e4-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="df5e4-386">msdyn_committype</span></span>             | <span data-ttu-id="df5e4-387">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-387">no</span></span>             | <span data-ttu-id="df5e4-388">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-388">no</span></span>           |
| <span data-ttu-id="df5e4-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="df5e4-389">msdyn_committypename</span></span>         | <span data-ttu-id="df5e4-390">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-390">no</span></span>             | <span data-ttu-id="df5e4-391">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-391">no</span></span>           |
| <span data-ttu-id="df5e4-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="df5e4-392">msdyn_effort</span></span>                 | <span data-ttu-id="df5e4-393">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-393">no</span></span>             | <span data-ttu-id="df5e4-394">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-394">no</span></span>           |
| <span data-ttu-id="df5e4-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="df5e4-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="df5e4-396">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-396">no</span></span>             | <span data-ttu-id="df5e4-397">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-397">no</span></span>           |
| <span data-ttu-id="df5e4-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="df5e4-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="df5e4-399">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-399">no</span></span>             | <span data-ttu-id="df5e4-400">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-400">no</span></span>           |
| <span data-ttu-id="df5e4-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="df5e4-401">msdyn_finish</span></span>                 | <span data-ttu-id="df5e4-402">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-402">no</span></span>             | <span data-ttu-id="df5e4-403">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-403">no</span></span>           |
| <span data-ttu-id="df5e4-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="df5e4-405">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-405">no</span></span>             | <span data-ttu-id="df5e4-406">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-406">no</span></span>           |
| <span data-ttu-id="df5e4-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="df5e4-408">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-408">no</span></span>             | <span data-ttu-id="df5e4-409">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-409">no</span></span>           |
| <span data-ttu-id="df5e4-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="df5e4-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="df5e4-411">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-411">no</span></span>             | <span data-ttu-id="df5e4-412">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-412">no</span></span>           |
| <span data-ttu-id="df5e4-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="df5e4-414">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-414">no</span></span>             | <span data-ttu-id="df5e4-415">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-415">no</span></span>           |
| <span data-ttu-id="df5e4-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="df5e4-417">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-417">no</span></span>             | <span data-ttu-id="df5e4-418">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-418">no</span></span>           |
| <span data-ttu-id="df5e4-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="df5e4-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="df5e4-420">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-420">no</span></span>             | <span data-ttu-id="df5e4-421">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-421">no</span></span>           |
| <span data-ttu-id="df5e4-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="df5e4-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="df5e4-423">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-423">no</span></span>             | <span data-ttu-id="df5e4-424">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-424">no</span></span>           |
| <span data-ttu-id="df5e4-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="df5e4-425">msdyn_projectid</span></span>              | <span data-ttu-id="df5e4-426">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-426">yes</span></span>            | <span data-ttu-id="df5e4-427">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-427">no</span></span>           |
| <span data-ttu-id="df5e4-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-428">msdyn_projectidname</span></span>          | <span data-ttu-id="df5e4-429">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-429">no</span></span>             | <span data-ttu-id="df5e4-430">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-430">no</span></span>           |
| <span data-ttu-id="df5e4-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="df5e4-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="df5e4-432">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-432">no</span></span>             | <span data-ttu-id="df5e4-433">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-433">no</span></span>           |
| <span data-ttu-id="df5e4-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="df5e4-435">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-435">no</span></span>             | <span data-ttu-id="df5e4-436">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-436">no</span></span>           |
| <span data-ttu-id="df5e4-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="df5e4-437">msdyn_start</span></span>                  | <span data-ttu-id="df5e4-438">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-438">no</span></span>             | <span data-ttu-id="df5e4-439">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-439">no</span></span>           |
| <span data-ttu-id="df5e4-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="df5e4-440">msdyn_taskid</span></span>                 | <span data-ttu-id="df5e4-441">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-441">no</span></span>             | <span data-ttu-id="df5e4-442">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-442">no</span></span>           |
| <span data-ttu-id="df5e4-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-443">msdyn_taskidname</span></span>             | <span data-ttu-id="df5e4-444">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-444">no</span></span>             | <span data-ttu-id="df5e4-445">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-445">no</span></span>           |
| <span data-ttu-id="df5e4-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="df5e4-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="df5e4-447">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-447">no</span></span>             | <span data-ttu-id="df5e4-448">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="df5e4-449">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="df5e4-449">Project team member</span></span>

| <span data-ttu-id="df5e4-450">**論理名**</span><span class="sxs-lookup"><span data-stu-id="df5e4-450">**Logical name**</span></span>                                 | <span data-ttu-id="df5e4-451">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-451">**Can create**</span></span> | <span data-ttu-id="df5e4-452">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="df5e4-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="df5e4-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="df5e4-454">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-454">no</span></span>             | <span data-ttu-id="df5e4-455">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-455">no</span></span>           |
| <span data-ttu-id="df5e4-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="df5e4-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="df5e4-457">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-457">no</span></span>             | <span data-ttu-id="df5e4-458">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-458">no</span></span>           |
| <span data-ttu-id="df5e4-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="df5e4-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="df5e4-460">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-460">no</span></span>             | <span data-ttu-id="df5e4-461">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-461">no</span></span>           |
| <span data-ttu-id="df5e4-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="df5e4-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="df5e4-463">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-463">no</span></span>             | <span data-ttu-id="df5e4-464">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-464">no</span></span>           |
| <span data-ttu-id="df5e4-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="df5e4-465">msdyn_effort</span></span>                                     | <span data-ttu-id="df5e4-466">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-466">no</span></span>             | <span data-ttu-id="df5e4-467">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-467">no</span></span>           |
| <span data-ttu-id="df5e4-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="df5e4-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="df5e4-469">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-469">no</span></span>             | <span data-ttu-id="df5e4-470">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-470">no</span></span>           |
| <span data-ttu-id="df5e4-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="df5e4-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="df5e4-472">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-472">no</span></span>             | <span data-ttu-id="df5e4-473">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-473">no</span></span>           |
| <span data-ttu-id="df5e4-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="df5e4-474">msdyn_finish</span></span>                                     | <span data-ttu-id="df5e4-475">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-475">no</span></span>             | <span data-ttu-id="df5e4-476">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-476">no</span></span>           |
| <span data-ttu-id="df5e4-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="df5e4-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="df5e4-478">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-478">no</span></span>             | <span data-ttu-id="df5e4-479">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-479">no</span></span>           |
| <span data-ttu-id="df5e4-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="df5e4-480">msdyn_hours</span></span>                                      | <span data-ttu-id="df5e4-481">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-481">no</span></span>             | <span data-ttu-id="df5e4-482">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-482">no</span></span>           |
| <span data-ttu-id="df5e4-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="df5e4-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="df5e4-484">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-484">no</span></span>             | <span data-ttu-id="df5e4-485">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-485">no</span></span>           |
| <span data-ttu-id="df5e4-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="df5e4-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="df5e4-487">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-487">no</span></span>             | <span data-ttu-id="df5e4-488">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-488">no</span></span>           |
| <span data-ttu-id="df5e4-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="df5e4-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="df5e4-490">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-490">no</span></span>             | <span data-ttu-id="df5e4-491">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-491">no</span></span>           |
| <span data-ttu-id="df5e4-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="df5e4-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="df5e4-493">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-493">no</span></span>             | <span data-ttu-id="df5e4-494">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-494">no</span></span>           |
| <span data-ttu-id="df5e4-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="df5e4-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="df5e4-496">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-496">no</span></span>             | <span data-ttu-id="df5e4-497">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-497">no</span></span>           |
| <span data-ttu-id="df5e4-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="df5e4-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="df5e4-499">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-499">no</span></span>             | <span data-ttu-id="df5e4-500">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-500">no</span></span>           |
| <span data-ttu-id="df5e4-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="df5e4-501">msdyn_start</span></span>                                      | <span data-ttu-id="df5e4-502">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-502">no</span></span>             | <span data-ttu-id="df5e4-503">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="df5e4-504">Project</span><span class="sxs-lookup"><span data-stu-id="df5e4-504">Project</span></span>

| <span data-ttu-id="df5e4-505">**論理名**</span><span class="sxs-lookup"><span data-stu-id="df5e4-505">**Logical name**</span></span>                       | <span data-ttu-id="df5e4-506">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-506">**Can create**</span></span> | <span data-ttu-id="df5e4-507">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="df5e4-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="df5e4-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="df5e4-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="df5e4-509">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-509">no</span></span>             | <span data-ttu-id="df5e4-510">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-510">no</span></span>           |
| <span data-ttu-id="df5e4-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="df5e4-512">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-512">no</span></span>             | <span data-ttu-id="df5e4-513">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-513">no</span></span>           |
| <span data-ttu-id="df5e4-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="df5e4-515">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-515">no</span></span>             | <span data-ttu-id="df5e4-516">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-516">no</span></span>           |
| <span data-ttu-id="df5e4-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="df5e4-518">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-518">no</span></span>             | <span data-ttu-id="df5e4-519">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-519">no</span></span>           |
| <span data-ttu-id="df5e4-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="df5e4-521">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-521">no</span></span>             | <span data-ttu-id="df5e4-522">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-522">no</span></span>           |
| <span data-ttu-id="df5e4-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="df5e4-524">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-524">no</span></span>             | <span data-ttu-id="df5e4-525">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-525">no</span></span>           |
| <span data-ttu-id="df5e4-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="df5e4-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="df5e4-527">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-527">yes</span></span>            | <span data-ttu-id="df5e4-528">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-528">no</span></span>           |
| <span data-ttu-id="df5e4-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="df5e4-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="df5e4-530">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-530">yes</span></span>            | <span data-ttu-id="df5e4-531">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-531">no</span></span>           |
| <span data-ttu-id="df5e4-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="df5e4-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="df5e4-533">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-533">yes</span></span>            | <span data-ttu-id="df5e4-534">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-534">no</span></span>           |
| <span data-ttu-id="df5e4-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="df5e4-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="df5e4-536">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-536">no</span></span>             | <span data-ttu-id="df5e4-537">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-537">no</span></span>           |
| <span data-ttu-id="df5e4-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="df5e4-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="df5e4-539">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-539">no</span></span>             | <span data-ttu-id="df5e4-540">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-540">no</span></span>           |
| <span data-ttu-id="df5e4-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="df5e4-542">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-542">no</span></span>             | <span data-ttu-id="df5e4-543">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-543">no</span></span>           |
| <span data-ttu-id="df5e4-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="df5e4-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="df5e4-545">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-545">no</span></span>             | <span data-ttu-id="df5e4-546">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-546">no</span></span>           |
| <span data-ttu-id="df5e4-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="df5e4-548">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-548">no</span></span>             | <span data-ttu-id="df5e4-549">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-549">no</span></span>           |
| <span data-ttu-id="df5e4-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="df5e4-550">msdyn_duration</span></span>                         | <span data-ttu-id="df5e4-551">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-551">no</span></span>             | <span data-ttu-id="df5e4-552">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-552">no</span></span>           |
| <span data-ttu-id="df5e4-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="df5e4-553">msdyn_effort</span></span>                           | <span data-ttu-id="df5e4-554">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-554">no</span></span>             | <span data-ttu-id="df5e4-555">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-555">no</span></span>           |
| <span data-ttu-id="df5e4-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="df5e4-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="df5e4-557">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-557">no</span></span>             | <span data-ttu-id="df5e4-558">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-558">no</span></span>           |
| <span data-ttu-id="df5e4-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="df5e4-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="df5e4-560">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-560">no</span></span>             | <span data-ttu-id="df5e4-561">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-561">no</span></span>           |
| <span data-ttu-id="df5e4-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="df5e4-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="df5e4-563">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-563">no</span></span>             | <span data-ttu-id="df5e4-564">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-564">no</span></span>           |
| <span data-ttu-id="df5e4-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="df5e4-565">msdyn_finish</span></span>                           | <span data-ttu-id="df5e4-566">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-566">yes</span></span>            | <span data-ttu-id="df5e4-567">はい</span><span class="sxs-lookup"><span data-stu-id="df5e4-567">yes</span></span>          |
| <span data-ttu-id="df5e4-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="df5e4-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="df5e4-569">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-569">no</span></span>             | <span data-ttu-id="df5e4-570">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-570">no</span></span>           |
| <span data-ttu-id="df5e4-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="df5e4-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="df5e4-572">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-572">no</span></span>             | <span data-ttu-id="df5e4-573">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-573">no</span></span>           |
| <span data-ttu-id="df5e4-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="df5e4-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="df5e4-575">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-575">no</span></span>             | <span data-ttu-id="df5e4-576">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-576">no</span></span>           |
| <span data-ttu-id="df5e4-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="df5e4-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="df5e4-578">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-578">no</span></span>             | <span data-ttu-id="df5e4-579">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-579">no</span></span>           |
| <span data-ttu-id="df5e4-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="df5e4-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="df5e4-581">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-581">no</span></span>             | <span data-ttu-id="df5e4-582">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-582">no</span></span>           |
| <span data-ttu-id="df5e4-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="df5e4-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="df5e4-584">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-584">no</span></span>             | <span data-ttu-id="df5e4-585">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-585">no</span></span>           |
| <span data-ttu-id="df5e4-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="df5e4-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="df5e4-587">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-587">no</span></span>             | <span data-ttu-id="df5e4-588">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-588">no</span></span>           |
| <span data-ttu-id="df5e4-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="df5e4-590">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-590">no</span></span>             | <span data-ttu-id="df5e4-591">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-591">no</span></span>           |
| <span data-ttu-id="df5e4-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="df5e4-593">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-593">no</span></span>             | <span data-ttu-id="df5e4-594">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-594">no</span></span>           |
| <span data-ttu-id="df5e4-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="df5e4-596">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-596">no</span></span>             | <span data-ttu-id="df5e4-597">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-597">no</span></span>           |
| <span data-ttu-id="df5e4-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="df5e4-599">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-599">no</span></span>             | <span data-ttu-id="df5e4-600">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-600">no</span></span>           |
| <span data-ttu-id="df5e4-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="df5e4-602">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-602">no</span></span>             | <span data-ttu-id="df5e4-603">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-603">no</span></span>           |
| <span data-ttu-id="df5e4-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="df5e4-604">msdyn_progress</span></span>                         | <span data-ttu-id="df5e4-605">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-605">no</span></span>             | <span data-ttu-id="df5e4-606">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-606">no</span></span>           |
| <span data-ttu-id="df5e4-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="df5e4-608">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-608">no</span></span>             | <span data-ttu-id="df5e4-609">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-609">no</span></span>           |
| <span data-ttu-id="df5e4-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="df5e4-611">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-611">no</span></span>             | <span data-ttu-id="df5e4-612">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-612">no</span></span>           |
| <span data-ttu-id="df5e4-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="df5e4-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="df5e4-614">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-614">no</span></span>             | <span data-ttu-id="df5e4-615">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-615">no</span></span>           |
| <span data-ttu-id="df5e4-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="df5e4-617">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-617">no</span></span>             | <span data-ttu-id="df5e4-618">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-618">no</span></span>           |
| <span data-ttu-id="df5e4-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="df5e4-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="df5e4-620">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-620">no</span></span>             | <span data-ttu-id="df5e4-621">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-621">no</span></span>           |
| <span data-ttu-id="df5e4-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="df5e4-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="df5e4-623">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-623">no</span></span>             | <span data-ttu-id="df5e4-624">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-624">no</span></span>           |
| <span data-ttu-id="df5e4-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="df5e4-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="df5e4-626">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-626">no</span></span>             | <span data-ttu-id="df5e4-627">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-627">no</span></span>           |
| <span data-ttu-id="df5e4-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="df5e4-629">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-629">no</span></span>             | <span data-ttu-id="df5e4-630">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-630">no</span></span>           |
| <span data-ttu-id="df5e4-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="df5e4-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="df5e4-632">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-632">no</span></span>             | <span data-ttu-id="df5e4-633">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-633">no</span></span>           |
| <span data-ttu-id="df5e4-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="df5e4-635">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-635">no</span></span>             | <span data-ttu-id="df5e4-636">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-636">no</span></span>           |
| <span data-ttu-id="df5e4-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="df5e4-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="df5e4-638">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-638">no</span></span>             | <span data-ttu-id="df5e4-639">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-639">no</span></span>           |
| <span data-ttu-id="df5e4-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="df5e4-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="df5e4-641">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-641">no</span></span>             | <span data-ttu-id="df5e4-642">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-642">no</span></span>           |
| <span data-ttu-id="df5e4-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="df5e4-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="df5e4-644">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-644">no</span></span>             | <span data-ttu-id="df5e4-645">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-645">no</span></span>           |
| <span data-ttu-id="df5e4-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="df5e4-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="df5e4-647">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-647">no</span></span>             | <span data-ttu-id="df5e4-648">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-648">no</span></span>           |
| <span data-ttu-id="df5e4-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="df5e4-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="df5e4-650">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-650">no</span></span>             | <span data-ttu-id="df5e4-651">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-651">no</span></span>           |
| <span data-ttu-id="df5e4-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="df5e4-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="df5e4-653">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-653">no</span></span>             | <span data-ttu-id="df5e4-654">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-654">no</span></span>           |
| <span data-ttu-id="df5e4-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="df5e4-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="df5e4-656">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-656">no</span></span>             | <span data-ttu-id="df5e4-657">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-657">no</span></span>           |
| <span data-ttu-id="df5e4-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="df5e4-659">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-659">no</span></span>             | <span data-ttu-id="df5e4-660">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-660">no</span></span>           |
| <span data-ttu-id="df5e4-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="df5e4-662">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-662">no</span></span>             | <span data-ttu-id="df5e4-663">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-663">no</span></span>           |
| <span data-ttu-id="df5e4-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="df5e4-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="df5e4-665">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-665">no</span></span>             | <span data-ttu-id="df5e4-666">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-666">no</span></span>           |
| <span data-ttu-id="df5e4-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="df5e4-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="df5e4-668">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-668">no</span></span>             | <span data-ttu-id="df5e4-669">いいえ</span><span class="sxs-lookup"><span data-stu-id="df5e4-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="df5e4-670">制限事項と既知の問題</span><span class="sxs-lookup"><span data-stu-id="df5e4-670">Limitations and known issues</span></span>
<span data-ttu-id="df5e4-671">以下は、制限事項と既知の問題のリストです。</span><span class="sxs-lookup"><span data-stu-id="df5e4-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="df5e4-672">スケジュール API は、**Microsoft Project ライセンスを持つユーザー** のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="df5e4-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="df5e4-673">次のユーザーは使用できません:</span><span class="sxs-lookup"><span data-stu-id="df5e4-673">They can't be used by:</span></span>
    - <span data-ttu-id="df5e4-674">アプリケーション ユーザー</span><span class="sxs-lookup"><span data-stu-id="df5e4-674">Application users</span></span>
    - <span data-ttu-id="df5e4-675">システム ユーザー</span><span class="sxs-lookup"><span data-stu-id="df5e4-675">System users</span></span>
    - <span data-ttu-id="df5e4-676">統合ユーザー</span><span class="sxs-lookup"><span data-stu-id="df5e4-676">Integration users</span></span>
    - <span data-ttu-id="df5e4-677">必要なライセンスを持っていない他のユーザー</span><span class="sxs-lookup"><span data-stu-id="df5e4-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="df5e4-678">各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。</span><span class="sxs-lookup"><span data-stu-id="df5e4-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="df5e4-679">各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。</span><span class="sxs-lookup"><span data-stu-id="df5e4-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="df5e4-680">Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="df5e4-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="df5e4-681">**OperationSet** 障害ステータスと障害ログは現在利用できません。</span><span class="sxs-lookup"><span data-stu-id="df5e4-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="df5e4-682">プロジェクトとタスクの制限と境界</span><span class="sxs-lookup"><span data-stu-id="df5e4-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="df5e4-683">エラー処理</span><span class="sxs-lookup"><span data-stu-id="df5e4-683">Error handling</span></span>

   - <span data-ttu-id="df5e4-684">操作セットから生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **操作セット** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="df5e4-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="df5e4-685">Project Scheduling Service で生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **PSS エラーログ** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="df5e4-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="df5e4-686">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="df5e4-686">Sample scenario</span></span>

<span data-ttu-id="df5e4-687">このシナリオでは、プロジェクト、チームメンバー、4 つのタスク、および 2 つのリソース割り当てを作成します。</span><span class="sxs-lookup"><span data-stu-id="df5e4-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="df5e4-688">次に、1 つのタスクを更新し、プロジェクトを更新し、1 つのタスクを削除し、1 つのリソース割り当てを削除して、タスクの依存関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="df5e4-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="df5e4-689">追加の例</span><span class="sxs-lookup"><span data-stu-id="df5e4-689">Additional samples</span></span>

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
