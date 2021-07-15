---
title: プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する
description: このトピックでは、プロジェクト スケジュール API を使用するための情報と使用例について解説します。
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293233"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="5af3a-103">プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する</span><span class="sxs-lookup"><span data-stu-id="5af3a-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="5af3a-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="5af3a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="5af3a-105">このトピックに記載されている機能の一部または全部は、プレビュー リリースの一部として提供されています。</span><span class="sxs-lookup"><span data-stu-id="5af3a-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="5af3a-106">コンテンツおよび機能は変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5af3a-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="5af3a-107">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="5af3a-107">Scheduling entities</span></span>

<span data-ttu-id="5af3a-108">プロジェクト スケジュール API では、**スケジュール エンティティ** を使用した作成、更新、削除操作を実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="5af3a-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="5af3a-109">これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="5af3a-110">**スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。</span><span class="sxs-lookup"><span data-stu-id="5af3a-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="5af3a-111">次の表に、プロジェクト スケジュール エンティティの全リストを示します。</span><span class="sxs-lookup"><span data-stu-id="5af3a-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="5af3a-112">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="5af3a-112">Entity name</span></span>  | <span data-ttu-id="5af3a-113">エンティティの論理名</span><span class="sxs-lookup"><span data-stu-id="5af3a-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="5af3a-114">Project</span><span class="sxs-lookup"><span data-stu-id="5af3a-114">Project</span></span> | <span data-ttu-id="5af3a-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5af3a-115">msdyn_project</span></span> |
| <span data-ttu-id="5af3a-116">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="5af3a-116">Project Task</span></span>  | <span data-ttu-id="5af3a-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="5af3a-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="5af3a-118">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="5af3a-118">Project Task Dependency</span></span>  | <span data-ttu-id="5af3a-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="5af3a-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="5af3a-120">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="5af3a-120">Resource Assignment</span></span> | <span data-ttu-id="5af3a-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="5af3a-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="5af3a-122">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="5af3a-122">Project Bucket</span></span>  | <span data-ttu-id="5af3a-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="5af3a-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="5af3a-124">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="5af3a-124">Project Team Member</span></span> | <span data-ttu-id="5af3a-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="5af3a-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="5af3a-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="5af3a-126">OperationSet</span></span>

<span data-ttu-id="5af3a-127">OperationSet は、スケジュールに影響を与える複数の要求をトランザクション内で処理する必要がある場合に使用できる作業単位パターンです。</span><span class="sxs-lookup"><span data-stu-id="5af3a-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="5af3a-128">プロジェクト スケジュール API</span><span class="sxs-lookup"><span data-stu-id="5af3a-128">Project schedule APIs</span></span>

<span data-ttu-id="5af3a-129">以下は、現在のプロジェクト スケジュール API のリストです。</span><span class="sxs-lookup"><span data-stu-id="5af3a-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="5af3a-130">**msdyn_CreateProjectV1**: この API を使用してプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="5af3a-131">プロジェクトとデフォルトのプロジェクト バケットがすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="5af3a-132">**msdyn_CreateTeamMemberV1**: この API を使用して、プロジェクト チーム メンバーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="5af3a-133">チーム メンバーのレコードはすぐに作成されます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="5af3a-134">**msdyn_CreateOperationSetV1**: この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="5af3a-135">**msdyn_PSSCreateV1**: この API を使用してエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="5af3a-136">エンティティは、作成操作をサポートするプロジェクト スケジュール エンティティのいずれかとなります。</span><span class="sxs-lookup"><span data-stu-id="5af3a-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="5af3a-137">**msdyn_PSSUpdateV1**: この API を使用してエンティティを更新できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="5af3a-138">エンティティは、更新操作をサポートするプロジェクト スケジュール エンティティのいずれかとなります。</span><span class="sxs-lookup"><span data-stu-id="5af3a-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="5af3a-139">**msdyn_PSSDeleteV1**: この API を使用してエンティティを削除できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="5af3a-140">エンティティには、削除操作をサポートするプロジェクト スケジュール エンティティのいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="5af3a-141">**msdyn_ExecuteOperationSetV1**: この API は、指定された操作セット内のすべての操作を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="5af3a-142">OperationSet でプロジェクト スケジュール API を使用する</span><span class="sxs-lookup"><span data-stu-id="5af3a-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="5af3a-143">**CreateProjectV1** と **CreateTeamMemberV1** 両方があるレコードは直ちに作成されるため、これらの API は **OperationSet** で直接使用できません。</span><span class="sxs-lookup"><span data-stu-id="5af3a-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="5af3a-144">ただし、API を使用して必要なレコードを作成し、**OperationSet** を作成し、これらの事前に作成されたレコードを **OperationSet** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="5af3a-145">サポートされている操作</span><span class="sxs-lookup"><span data-stu-id="5af3a-145">Supported operations</span></span>

| <span data-ttu-id="5af3a-146">スケジューリング エンティティ</span><span class="sxs-lookup"><span data-stu-id="5af3a-146">Scheduling entity</span></span> | <span data-ttu-id="5af3a-147">作成​​</span><span class="sxs-lookup"><span data-stu-id="5af3a-147">Create</span></span> | <span data-ttu-id="5af3a-148">更新プログラム</span><span class="sxs-lookup"><span data-stu-id="5af3a-148">Update</span></span> | <span data-ttu-id="5af3a-149">Delete キー</span><span class="sxs-lookup"><span data-stu-id="5af3a-149">Delete</span></span> | <span data-ttu-id="5af3a-150">重要な考慮事項</span><span class="sxs-lookup"><span data-stu-id="5af3a-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="5af3a-151">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="5af3a-151">Project task</span></span> | <span data-ttu-id="5af3a-152">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-152">Yes</span></span> | <span data-ttu-id="5af3a-153">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-153">Yes</span></span> | <span data-ttu-id="5af3a-154">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-154">Yes</span></span> | <span data-ttu-id="5af3a-155">いいえ​​</span><span class="sxs-lookup"><span data-stu-id="5af3a-155">None</span></span> |
| <span data-ttu-id="5af3a-156">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="5af3a-156">Project task dependency</span></span> | <span data-ttu-id="5af3a-157">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-157">Yes</span></span> | <span data-ttu-id="5af3a-158">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-158">Yes</span></span> | | <span data-ttu-id="5af3a-159">プロジェクト タスクの依存関係レコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="5af3a-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="5af3a-160">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5af3a-161">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="5af3a-161">Resource assignment</span></span> | <span data-ttu-id="5af3a-162">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-162">Yes</span></span> | <span data-ttu-id="5af3a-163">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-163">Yes</span></span> | | <span data-ttu-id="5af3a-164">次のフィールドを使用した操作はサポートされていません: **BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining**、および **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="5af3a-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="5af3a-165">リソース割り当てレコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="5af3a-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="5af3a-166">代わりに、古いレコードを削除して、新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5af3a-167">プロジェクト バケット</span><span class="sxs-lookup"><span data-stu-id="5af3a-167">Project bucket</span></span> | <span data-ttu-id="5af3a-168">N/A</span><span class="sxs-lookup"><span data-stu-id="5af3a-168">N/A</span></span> | <span data-ttu-id="5af3a-169">N/A</span><span class="sxs-lookup"><span data-stu-id="5af3a-169">N/A</span></span> | <span data-ttu-id="5af3a-170">N/A</span><span class="sxs-lookup"><span data-stu-id="5af3a-170">N/A</span></span> | <span data-ttu-id="5af3a-171">既定のバケットは、**CreateProjectV1** API を使って作成されます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="5af3a-172">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="5af3a-172">Project team member</span></span> | <span data-ttu-id="5af3a-173">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-173">Yes</span></span> | <span data-ttu-id="5af3a-174">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-174">Yes</span></span> | <span data-ttu-id="5af3a-175">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-175">Yes</span></span> | <span data-ttu-id="5af3a-176">作成操作には、**CreateTeamMemberV1** API を使用します。</span><span class="sxs-lookup"><span data-stu-id="5af3a-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="5af3a-177">Project</span><span class="sxs-lookup"><span data-stu-id="5af3a-177">Project</span></span> | <span data-ttu-id="5af3a-178">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-178">Yes</span></span> | <span data-ttu-id="5af3a-179">有効</span><span class="sxs-lookup"><span data-stu-id="5af3a-179">Yes</span></span> | <span data-ttu-id="5af3a-180">N/A</span><span class="sxs-lookup"><span data-stu-id="5af3a-180">N/A</span></span> | <span data-ttu-id="5af3a-181">次のフィールドを使用した操作はサポートされていません: **StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、 **CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart**、および **Duration**。</span><span class="sxs-lookup"><span data-stu-id="5af3a-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="5af3a-182">これらの API は、カスタムフィールドを含むエンティティ オブジェクトを使用して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="5af3a-183">ID プロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5af3a-183">The ID property is optional.</span></span> <span data-ttu-id="5af3a-184">提供されている場合、システムはそれを使用しようとし、使用できない場合は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5af3a-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="5af3a-185">提供されていない場合は、システムが生成します。</span><span class="sxs-lookup"><span data-stu-id="5af3a-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="5af3a-186">制限のあるフィールド</span><span class="sxs-lookup"><span data-stu-id="5af3a-186">Restricted fields</span></span>

<span data-ttu-id="5af3a-187">以下の表は、**作成** と **編集** が制限されるフィールドを定義しています。</span><span class="sxs-lookup"><span data-stu-id="5af3a-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="5af3a-188">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="5af3a-188">Project task</span></span>

| <span data-ttu-id="5af3a-189">**論理名**</span><span class="sxs-lookup"><span data-stu-id="5af3a-189">**Logical name**</span></span>                       | <span data-ttu-id="5af3a-190">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-190">**Can create**</span></span> | <span data-ttu-id="5af3a-191">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="5af3a-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="5af3a-193">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-193">no</span></span>             | <span data-ttu-id="5af3a-194">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-194">no</span></span>               |
| <span data-ttu-id="5af3a-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="5af3a-196">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-196">no</span></span>             | <span data-ttu-id="5af3a-197">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-197">no</span></span>               |
| <span data-ttu-id="5af3a-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="5af3a-198">msdyn_actualend</span></span>                        | <span data-ttu-id="5af3a-199">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-199">no</span></span>             | <span data-ttu-id="5af3a-200">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-200">no</span></span>               |
| <span data-ttu-id="5af3a-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="5af3a-202">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-202">no</span></span>             | <span data-ttu-id="5af3a-203">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-203">no</span></span>               |
| <span data-ttu-id="5af3a-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5af3a-205">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-205">no</span></span>             | <span data-ttu-id="5af3a-206">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-206">no</span></span>               |
| <span data-ttu-id="5af3a-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="5af3a-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="5af3a-208">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-208">no</span></span>             | <span data-ttu-id="5af3a-209">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-209">no</span></span>               |
| <span data-ttu-id="5af3a-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="5af3a-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="5af3a-211">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-211">no</span></span>             | <span data-ttu-id="5af3a-212">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-212">no</span></span>               |
| <span data-ttu-id="5af3a-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="5af3a-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-214">no</span></span>             | <span data-ttu-id="5af3a-215">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-215">no</span></span>               |
| <span data-ttu-id="5af3a-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5af3a-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="5af3a-217">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-217">no</span></span>             | <span data-ttu-id="5af3a-218">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-218">no</span></span>               |
| <span data-ttu-id="5af3a-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5af3a-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5af3a-220">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-220">no</span></span>             | <span data-ttu-id="5af3a-221">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-221">no</span></span>               |
| <span data-ttu-id="5af3a-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5af3a-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="5af3a-223">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-223">no</span></span>             | <span data-ttu-id="5af3a-224">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-224">no</span></span>               |
| <span data-ttu-id="5af3a-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="5af3a-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="5af3a-226">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-226">no</span></span>             | <span data-ttu-id="5af3a-227">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-227">no</span></span>               |
| <span data-ttu-id="5af3a-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="5af3a-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="5af3a-229">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-229">no</span></span>             | <span data-ttu-id="5af3a-230">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-230">no</span></span>               |
| <span data-ttu-id="5af3a-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="5af3a-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="5af3a-232">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-232">no</span></span>             | <span data-ttu-id="5af3a-233">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-233">no</span></span>               |
| <span data-ttu-id="5af3a-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="5af3a-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="5af3a-235">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-235">no</span></span>             | <span data-ttu-id="5af3a-236">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-236">no</span></span>               |
| <span data-ttu-id="5af3a-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="5af3a-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="5af3a-238">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-238">no</span></span>             | <span data-ttu-id="5af3a-239">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-239">no</span></span>               |
| <span data-ttu-id="5af3a-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="5af3a-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="5af3a-241">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-241">no</span></span>             | <span data-ttu-id="5af3a-242">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-242">no</span></span>               |
| <span data-ttu-id="5af3a-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="5af3a-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="5af3a-244">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-244">no</span></span>             | <span data-ttu-id="5af3a-245">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-245">no</span></span>               |
| <span data-ttu-id="5af3a-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="5af3a-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="5af3a-247">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-247">no</span></span>             | <span data-ttu-id="5af3a-248">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-248">no</span></span>               |
| <span data-ttu-id="5af3a-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5af3a-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="5af3a-250">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-250">no</span></span>             | <span data-ttu-id="5af3a-251">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-251">no</span></span>               |
| <span data-ttu-id="5af3a-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="5af3a-253">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-253">no</span></span>             | <span data-ttu-id="5af3a-254">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-254">no</span></span>               |
| <span data-ttu-id="5af3a-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="5af3a-256">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-256">no</span></span>             | <span data-ttu-id="5af3a-257">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-257">no</span></span>               |
| <span data-ttu-id="5af3a-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5af3a-259">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-259">no</span></span>             | <span data-ttu-id="5af3a-260">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-260">no</span></span>               |
| <span data-ttu-id="5af3a-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5af3a-262">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-262">no</span></span>             | <span data-ttu-id="5af3a-263">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-263">no</span></span>               |
| <span data-ttu-id="5af3a-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="5af3a-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="5af3a-265">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-265">no</span></span>             | <span data-ttu-id="5af3a-266">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-266">no</span></span>               |
| <span data-ttu-id="5af3a-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5af3a-267">msdyn_progress</span></span>                         | <span data-ttu-id="5af3a-268">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-268">no</span></span>             | <span data-ttu-id="5af3a-269">いいえ (P4W の場合は"はい")</span><span class="sxs-lookup"><span data-stu-id="5af3a-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="5af3a-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5af3a-271">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-271">no</span></span>             | <span data-ttu-id="5af3a-272">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-272">no</span></span>               |
| <span data-ttu-id="5af3a-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5af3a-274">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-274">no</span></span>             | <span data-ttu-id="5af3a-275">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-275">no</span></span>               |
| <span data-ttu-id="5af3a-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5af3a-277">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-277">no</span></span>             | <span data-ttu-id="5af3a-278">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-278">no</span></span>               |
| <span data-ttu-id="5af3a-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5af3a-280">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-280">no</span></span>             | <span data-ttu-id="5af3a-281">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-281">no</span></span>               |
| <span data-ttu-id="5af3a-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="5af3a-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="5af3a-283">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-283">no</span></span>             | <span data-ttu-id="5af3a-284">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-284">no</span></span>               |
| <span data-ttu-id="5af3a-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="5af3a-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="5af3a-286">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-286">no</span></span>             | <span data-ttu-id="5af3a-287">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-287">no</span></span>               |
| <span data-ttu-id="5af3a-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="5af3a-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="5af3a-289">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-289">no</span></span>             | <span data-ttu-id="5af3a-290">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-290">no</span></span>               |
| <span data-ttu-id="5af3a-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5af3a-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="5af3a-292">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-292">no</span></span>             | <span data-ttu-id="5af3a-293">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-293">no</span></span>               |
| <span data-ttu-id="5af3a-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="5af3a-295">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-295">no</span></span>             | <span data-ttu-id="5af3a-296">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-296">no</span></span>               |
| <span data-ttu-id="5af3a-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5af3a-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="5af3a-298">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-298">no</span></span>             | <span data-ttu-id="5af3a-299">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-299">no</span></span>               |
| <span data-ttu-id="5af3a-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5af3a-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="5af3a-301">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-301">no</span></span>             | <span data-ttu-id="5af3a-302">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-302">no</span></span>               |
| <span data-ttu-id="5af3a-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="5af3a-304">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-304">no</span></span>             | <span data-ttu-id="5af3a-305">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-305">no</span></span>               |
| <span data-ttu-id="5af3a-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5af3a-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5af3a-307">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-307">no</span></span>             | <span data-ttu-id="5af3a-308">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-308">no</span></span>               |
| <span data-ttu-id="5af3a-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5af3a-310">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-310">no</span></span>             | <span data-ttu-id="5af3a-311">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-311">no</span></span>               |
| <span data-ttu-id="5af3a-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="5af3a-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="5af3a-313">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-313">no</span></span>             | <span data-ttu-id="5af3a-314">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-314">no</span></span>               |
| <span data-ttu-id="5af3a-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="5af3a-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="5af3a-316">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-316">no</span></span>             | <span data-ttu-id="5af3a-317">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-317">no</span></span>               |
| <span data-ttu-id="5af3a-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="5af3a-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="5af3a-319">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-319">no</span></span>             | <span data-ttu-id="5af3a-320">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-320">no</span></span>               |
| <span data-ttu-id="5af3a-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5af3a-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5af3a-322">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-322">no</span></span>             | <span data-ttu-id="5af3a-323">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-323">no</span></span>               |
| <span data-ttu-id="5af3a-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="5af3a-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="5af3a-325">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-325">no</span></span>             | <span data-ttu-id="5af3a-326">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-326">no</span></span>               |
| <span data-ttu-id="5af3a-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="5af3a-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="5af3a-328">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-328">no</span></span>             | <span data-ttu-id="5af3a-329">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-329">no</span></span>               |
| <span data-ttu-id="5af3a-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="5af3a-330">msdyn_summary</span></span>                          | <span data-ttu-id="5af3a-331">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-331">no</span></span>             | <span data-ttu-id="5af3a-332">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-332">no</span></span>               |
| <span data-ttu-id="5af3a-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="5af3a-334">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-334">no</span></span>             | <span data-ttu-id="5af3a-335">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-335">no</span></span>               |
| <span data-ttu-id="5af3a-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="5af3a-337">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-337">no</span></span>             | <span data-ttu-id="5af3a-338">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="5af3a-339">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="5af3a-339">Project task dependency</span></span>

| <span data-ttu-id="5af3a-340">**論理名**</span><span class="sxs-lookup"><span data-stu-id="5af3a-340">**Logical name**</span></span>              | <span data-ttu-id="5af3a-341">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-341">**Can create**</span></span> | <span data-ttu-id="5af3a-342">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="5af3a-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="5af3a-343">msdyn_linktype</span></span>                | <span data-ttu-id="5af3a-344">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-344">no</span></span>             | <span data-ttu-id="5af3a-345">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-345">no</span></span>           |
| <span data-ttu-id="5af3a-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="5af3a-346">msdyn_linktypename</span></span>            | <span data-ttu-id="5af3a-347">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-347">no</span></span>             | <span data-ttu-id="5af3a-348">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-348">no</span></span>           |
| <span data-ttu-id="5af3a-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="5af3a-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="5af3a-350">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-350">yes</span></span>            | <span data-ttu-id="5af3a-351">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-351">no</span></span>           |
| <span data-ttu-id="5af3a-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="5af3a-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="5af3a-353">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-353">yes</span></span>            | <span data-ttu-id="5af3a-354">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-354">no</span></span>           |
| <span data-ttu-id="5af3a-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5af3a-355">msdyn_project</span></span>                 | <span data-ttu-id="5af3a-356">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-356">yes</span></span>            | <span data-ttu-id="5af3a-357">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-357">no</span></span>           |
| <span data-ttu-id="5af3a-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="5af3a-358">msdyn_projectname</span></span>             | <span data-ttu-id="5af3a-359">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-359">yes</span></span>            | <span data-ttu-id="5af3a-360">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-360">no</span></span>           |
| <span data-ttu-id="5af3a-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="5af3a-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="5af3a-362">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-362">yes</span></span>            | <span data-ttu-id="5af3a-363">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-363">no</span></span>           |
| <span data-ttu-id="5af3a-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="5af3a-364">msdyn_successortask</span></span>           | <span data-ttu-id="5af3a-365">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-365">yes</span></span>            | <span data-ttu-id="5af3a-366">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-366">no</span></span>           |
| <span data-ttu-id="5af3a-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="5af3a-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="5af3a-368">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-368">yes</span></span>            | <span data-ttu-id="5af3a-369">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="5af3a-370">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="5af3a-370">Resource assignment</span></span>

| <span data-ttu-id="5af3a-371">**論理名**</span><span class="sxs-lookup"><span data-stu-id="5af3a-371">**Logical name**</span></span>             | <span data-ttu-id="5af3a-372">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-372">**Can create**</span></span> | <span data-ttu-id="5af3a-373">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="5af3a-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="5af3a-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="5af3a-375">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-375">yes</span></span>            | <span data-ttu-id="5af3a-376">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-376">no</span></span>           |
| <span data-ttu-id="5af3a-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="5af3a-378">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-378">yes</span></span>            | <span data-ttu-id="5af3a-379">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-379">no</span></span>           |
| <span data-ttu-id="5af3a-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="5af3a-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="5af3a-381">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-381">no</span></span>             | <span data-ttu-id="5af3a-382">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-382">no</span></span>           |
| <span data-ttu-id="5af3a-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="5af3a-384">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-384">no</span></span>             | <span data-ttu-id="5af3a-385">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-385">no</span></span>           |
| <span data-ttu-id="5af3a-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="5af3a-386">msdyn_committype</span></span>             | <span data-ttu-id="5af3a-387">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-387">no</span></span>             | <span data-ttu-id="5af3a-388">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-388">no</span></span>           |
| <span data-ttu-id="5af3a-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="5af3a-389">msdyn_committypename</span></span>         | <span data-ttu-id="5af3a-390">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-390">no</span></span>             | <span data-ttu-id="5af3a-391">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-391">no</span></span>           |
| <span data-ttu-id="5af3a-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5af3a-392">msdyn_effort</span></span>                 | <span data-ttu-id="5af3a-393">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-393">no</span></span>             | <span data-ttu-id="5af3a-394">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-394">no</span></span>           |
| <span data-ttu-id="5af3a-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5af3a-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="5af3a-396">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-396">no</span></span>             | <span data-ttu-id="5af3a-397">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-397">no</span></span>           |
| <span data-ttu-id="5af3a-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5af3a-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="5af3a-399">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-399">no</span></span>             | <span data-ttu-id="5af3a-400">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-400">no</span></span>           |
| <span data-ttu-id="5af3a-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5af3a-401">msdyn_finish</span></span>                 | <span data-ttu-id="5af3a-402">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-402">no</span></span>             | <span data-ttu-id="5af3a-403">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-403">no</span></span>           |
| <span data-ttu-id="5af3a-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="5af3a-405">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-405">no</span></span>             | <span data-ttu-id="5af3a-406">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-406">no</span></span>           |
| <span data-ttu-id="5af3a-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="5af3a-408">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-408">no</span></span>             | <span data-ttu-id="5af3a-409">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-409">no</span></span>           |
| <span data-ttu-id="5af3a-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="5af3a-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="5af3a-411">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-411">no</span></span>             | <span data-ttu-id="5af3a-412">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-412">no</span></span>           |
| <span data-ttu-id="5af3a-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="5af3a-414">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-414">no</span></span>             | <span data-ttu-id="5af3a-415">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-415">no</span></span>           |
| <span data-ttu-id="5af3a-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="5af3a-417">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-417">no</span></span>             | <span data-ttu-id="5af3a-418">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-418">no</span></span>           |
| <span data-ttu-id="5af3a-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="5af3a-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="5af3a-420">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-420">no</span></span>             | <span data-ttu-id="5af3a-421">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-421">no</span></span>           |
| <span data-ttu-id="5af3a-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="5af3a-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="5af3a-423">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-423">no</span></span>             | <span data-ttu-id="5af3a-424">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-424">no</span></span>           |
| <span data-ttu-id="5af3a-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="5af3a-425">msdyn_projectid</span></span>              | <span data-ttu-id="5af3a-426">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-426">yes</span></span>            | <span data-ttu-id="5af3a-427">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-427">no</span></span>           |
| <span data-ttu-id="5af3a-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-428">msdyn_projectidname</span></span>          | <span data-ttu-id="5af3a-429">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-429">no</span></span>             | <span data-ttu-id="5af3a-430">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-430">no</span></span>           |
| <span data-ttu-id="5af3a-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="5af3a-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="5af3a-432">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-432">no</span></span>             | <span data-ttu-id="5af3a-433">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-433">no</span></span>           |
| <span data-ttu-id="5af3a-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="5af3a-435">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-435">no</span></span>             | <span data-ttu-id="5af3a-436">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-436">no</span></span>           |
| <span data-ttu-id="5af3a-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5af3a-437">msdyn_start</span></span>                  | <span data-ttu-id="5af3a-438">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-438">no</span></span>             | <span data-ttu-id="5af3a-439">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-439">no</span></span>           |
| <span data-ttu-id="5af3a-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="5af3a-440">msdyn_taskid</span></span>                 | <span data-ttu-id="5af3a-441">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-441">no</span></span>             | <span data-ttu-id="5af3a-442">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-442">no</span></span>           |
| <span data-ttu-id="5af3a-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-443">msdyn_taskidname</span></span>             | <span data-ttu-id="5af3a-444">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-444">no</span></span>             | <span data-ttu-id="5af3a-445">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-445">no</span></span>           |
| <span data-ttu-id="5af3a-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="5af3a-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="5af3a-447">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-447">no</span></span>             | <span data-ttu-id="5af3a-448">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="5af3a-449">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="5af3a-449">Project team member</span></span>

| <span data-ttu-id="5af3a-450">**論理名**</span><span class="sxs-lookup"><span data-stu-id="5af3a-450">**Logical name**</span></span>                                 | <span data-ttu-id="5af3a-451">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-451">**Can create**</span></span> | <span data-ttu-id="5af3a-452">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="5af3a-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="5af3a-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="5af3a-454">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-454">no</span></span>             | <span data-ttu-id="5af3a-455">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-455">no</span></span>           |
| <span data-ttu-id="5af3a-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="5af3a-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="5af3a-457">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-457">no</span></span>             | <span data-ttu-id="5af3a-458">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-458">no</span></span>           |
| <span data-ttu-id="5af3a-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="5af3a-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="5af3a-460">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-460">no</span></span>             | <span data-ttu-id="5af3a-461">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-461">no</span></span>           |
| <span data-ttu-id="5af3a-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="5af3a-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="5af3a-463">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-463">no</span></span>             | <span data-ttu-id="5af3a-464">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-464">no</span></span>           |
| <span data-ttu-id="5af3a-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5af3a-465">msdyn_effort</span></span>                                     | <span data-ttu-id="5af3a-466">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-466">no</span></span>             | <span data-ttu-id="5af3a-467">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-467">no</span></span>           |
| <span data-ttu-id="5af3a-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5af3a-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="5af3a-469">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-469">no</span></span>             | <span data-ttu-id="5af3a-470">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-470">no</span></span>           |
| <span data-ttu-id="5af3a-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5af3a-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="5af3a-472">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-472">no</span></span>             | <span data-ttu-id="5af3a-473">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-473">no</span></span>           |
| <span data-ttu-id="5af3a-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5af3a-474">msdyn_finish</span></span>                                     | <span data-ttu-id="5af3a-475">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-475">no</span></span>             | <span data-ttu-id="5af3a-476">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-476">no</span></span>           |
| <span data-ttu-id="5af3a-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="5af3a-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="5af3a-478">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-478">no</span></span>             | <span data-ttu-id="5af3a-479">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-479">no</span></span>           |
| <span data-ttu-id="5af3a-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="5af3a-480">msdyn_hours</span></span>                                      | <span data-ttu-id="5af3a-481">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-481">no</span></span>             | <span data-ttu-id="5af3a-482">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-482">no</span></span>           |
| <span data-ttu-id="5af3a-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="5af3a-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="5af3a-484">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-484">no</span></span>             | <span data-ttu-id="5af3a-485">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-485">no</span></span>           |
| <span data-ttu-id="5af3a-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="5af3a-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="5af3a-487">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-487">no</span></span>             | <span data-ttu-id="5af3a-488">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-488">no</span></span>           |
| <span data-ttu-id="5af3a-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5af3a-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="5af3a-490">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-490">no</span></span>             | <span data-ttu-id="5af3a-491">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-491">no</span></span>           |
| <span data-ttu-id="5af3a-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="5af3a-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="5af3a-493">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-493">no</span></span>             | <span data-ttu-id="5af3a-494">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-494">no</span></span>           |
| <span data-ttu-id="5af3a-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="5af3a-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="5af3a-496">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-496">no</span></span>             | <span data-ttu-id="5af3a-497">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-497">no</span></span>           |
| <span data-ttu-id="5af3a-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="5af3a-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="5af3a-499">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-499">no</span></span>             | <span data-ttu-id="5af3a-500">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-500">no</span></span>           |
| <span data-ttu-id="5af3a-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5af3a-501">msdyn_start</span></span>                                      | <span data-ttu-id="5af3a-502">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-502">no</span></span>             | <span data-ttu-id="5af3a-503">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="5af3a-504">Project</span><span class="sxs-lookup"><span data-stu-id="5af3a-504">Project</span></span>

| <span data-ttu-id="5af3a-505">**論理名**</span><span class="sxs-lookup"><span data-stu-id="5af3a-505">**Logical name**</span></span>                       | <span data-ttu-id="5af3a-506">**作成可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-506">**Can create**</span></span> | <span data-ttu-id="5af3a-507">**編集可能**</span><span class="sxs-lookup"><span data-stu-id="5af3a-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="5af3a-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="5af3a-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="5af3a-509">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-509">no</span></span>             | <span data-ttu-id="5af3a-510">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-510">no</span></span>           |
| <span data-ttu-id="5af3a-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="5af3a-512">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-512">no</span></span>             | <span data-ttu-id="5af3a-513">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-513">no</span></span>           |
| <span data-ttu-id="5af3a-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="5af3a-515">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-515">no</span></span>             | <span data-ttu-id="5af3a-516">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-516">no</span></span>           |
| <span data-ttu-id="5af3a-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="5af3a-518">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-518">no</span></span>             | <span data-ttu-id="5af3a-519">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-519">no</span></span>           |
| <span data-ttu-id="5af3a-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="5af3a-521">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-521">no</span></span>             | <span data-ttu-id="5af3a-522">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-522">no</span></span>           |
| <span data-ttu-id="5af3a-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5af3a-524">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-524">no</span></span>             | <span data-ttu-id="5af3a-525">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-525">no</span></span>           |
| <span data-ttu-id="5af3a-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="5af3a-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="5af3a-527">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-527">yes</span></span>            | <span data-ttu-id="5af3a-528">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-528">no</span></span>           |
| <span data-ttu-id="5af3a-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5af3a-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="5af3a-530">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-530">yes</span></span>            | <span data-ttu-id="5af3a-531">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-531">no</span></span>           |
| <span data-ttu-id="5af3a-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5af3a-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="5af3a-533">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-533">yes</span></span>            | <span data-ttu-id="5af3a-534">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-534">no</span></span>           |
| <span data-ttu-id="5af3a-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="5af3a-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="5af3a-536">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-536">no</span></span>             | <span data-ttu-id="5af3a-537">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-537">no</span></span>           |
| <span data-ttu-id="5af3a-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5af3a-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="5af3a-539">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-539">no</span></span>             | <span data-ttu-id="5af3a-540">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-540">no</span></span>           |
| <span data-ttu-id="5af3a-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="5af3a-542">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-542">no</span></span>             | <span data-ttu-id="5af3a-543">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-543">no</span></span>           |
| <span data-ttu-id="5af3a-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="5af3a-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="5af3a-545">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-545">no</span></span>             | <span data-ttu-id="5af3a-546">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-546">no</span></span>           |
| <span data-ttu-id="5af3a-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="5af3a-548">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-548">no</span></span>             | <span data-ttu-id="5af3a-549">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-549">no</span></span>           |
| <span data-ttu-id="5af3a-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="5af3a-550">msdyn_duration</span></span>                         | <span data-ttu-id="5af3a-551">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-551">no</span></span>             | <span data-ttu-id="5af3a-552">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-552">no</span></span>           |
| <span data-ttu-id="5af3a-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5af3a-553">msdyn_effort</span></span>                           | <span data-ttu-id="5af3a-554">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-554">no</span></span>             | <span data-ttu-id="5af3a-555">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-555">no</span></span>           |
| <span data-ttu-id="5af3a-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5af3a-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5af3a-557">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-557">no</span></span>             | <span data-ttu-id="5af3a-558">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-558">no</span></span>           |
| <span data-ttu-id="5af3a-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5af3a-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="5af3a-560">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-560">no</span></span>             | <span data-ttu-id="5af3a-561">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-561">no</span></span>           |
| <span data-ttu-id="5af3a-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5af3a-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="5af3a-563">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-563">no</span></span>             | <span data-ttu-id="5af3a-564">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-564">no</span></span>           |
| <span data-ttu-id="5af3a-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5af3a-565">msdyn_finish</span></span>                           | <span data-ttu-id="5af3a-566">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-566">yes</span></span>            | <span data-ttu-id="5af3a-567">はい</span><span class="sxs-lookup"><span data-stu-id="5af3a-567">yes</span></span>          |
| <span data-ttu-id="5af3a-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="5af3a-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="5af3a-569">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-569">no</span></span>             | <span data-ttu-id="5af3a-570">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-570">no</span></span>           |
| <span data-ttu-id="5af3a-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="5af3a-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="5af3a-572">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-572">no</span></span>             | <span data-ttu-id="5af3a-573">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-573">no</span></span>           |
| <span data-ttu-id="5af3a-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="5af3a-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="5af3a-575">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-575">no</span></span>             | <span data-ttu-id="5af3a-576">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-576">no</span></span>           |
| <span data-ttu-id="5af3a-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="5af3a-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="5af3a-578">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-578">no</span></span>             | <span data-ttu-id="5af3a-579">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-579">no</span></span>           |
| <span data-ttu-id="5af3a-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="5af3a-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="5af3a-581">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-581">no</span></span>             | <span data-ttu-id="5af3a-582">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-582">no</span></span>           |
| <span data-ttu-id="5af3a-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="5af3a-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="5af3a-584">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-584">no</span></span>             | <span data-ttu-id="5af3a-585">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-585">no</span></span>           |
| <span data-ttu-id="5af3a-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="5af3a-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="5af3a-587">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-587">no</span></span>             | <span data-ttu-id="5af3a-588">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-588">no</span></span>           |
| <span data-ttu-id="5af3a-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="5af3a-590">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-590">no</span></span>             | <span data-ttu-id="5af3a-591">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-591">no</span></span>           |
| <span data-ttu-id="5af3a-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="5af3a-593">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-593">no</span></span>             | <span data-ttu-id="5af3a-594">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-594">no</span></span>           |
| <span data-ttu-id="5af3a-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="5af3a-596">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-596">no</span></span>             | <span data-ttu-id="5af3a-597">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-597">no</span></span>           |
| <span data-ttu-id="5af3a-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5af3a-599">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-599">no</span></span>             | <span data-ttu-id="5af3a-600">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-600">no</span></span>           |
| <span data-ttu-id="5af3a-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5af3a-602">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-602">no</span></span>             | <span data-ttu-id="5af3a-603">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-603">no</span></span>           |
| <span data-ttu-id="5af3a-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5af3a-604">msdyn_progress</span></span>                         | <span data-ttu-id="5af3a-605">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-605">no</span></span>             | <span data-ttu-id="5af3a-606">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-606">no</span></span>           |
| <span data-ttu-id="5af3a-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5af3a-608">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-608">no</span></span>             | <span data-ttu-id="5af3a-609">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-609">no</span></span>           |
| <span data-ttu-id="5af3a-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5af3a-611">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-611">no</span></span>             | <span data-ttu-id="5af3a-612">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-612">no</span></span>           |
| <span data-ttu-id="5af3a-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5af3a-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5af3a-614">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-614">no</span></span>             | <span data-ttu-id="5af3a-615">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-615">no</span></span>           |
| <span data-ttu-id="5af3a-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5af3a-617">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-617">no</span></span>             | <span data-ttu-id="5af3a-618">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-618">no</span></span>           |
| <span data-ttu-id="5af3a-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="5af3a-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="5af3a-620">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-620">no</span></span>             | <span data-ttu-id="5af3a-621">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-621">no</span></span>           |
| <span data-ttu-id="5af3a-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="5af3a-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="5af3a-623">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-623">no</span></span>             | <span data-ttu-id="5af3a-624">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-624">no</span></span>           |
| <span data-ttu-id="5af3a-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5af3a-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="5af3a-626">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-626">no</span></span>             | <span data-ttu-id="5af3a-627">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-627">no</span></span>           |
| <span data-ttu-id="5af3a-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="5af3a-629">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-629">no</span></span>             | <span data-ttu-id="5af3a-630">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-630">no</span></span>           |
| <span data-ttu-id="5af3a-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5af3a-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5af3a-632">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-632">no</span></span>             | <span data-ttu-id="5af3a-633">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-633">no</span></span>           |
| <span data-ttu-id="5af3a-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5af3a-635">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-635">no</span></span>             | <span data-ttu-id="5af3a-636">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-636">no</span></span>           |
| <span data-ttu-id="5af3a-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="5af3a-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="5af3a-638">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-638">no</span></span>             | <span data-ttu-id="5af3a-639">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-639">no</span></span>           |
| <span data-ttu-id="5af3a-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="5af3a-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="5af3a-641">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-641">no</span></span>             | <span data-ttu-id="5af3a-642">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-642">no</span></span>           |
| <span data-ttu-id="5af3a-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5af3a-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5af3a-644">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-644">no</span></span>             | <span data-ttu-id="5af3a-645">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-645">no</span></span>           |
| <span data-ttu-id="5af3a-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="5af3a-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="5af3a-647">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-647">no</span></span>             | <span data-ttu-id="5af3a-648">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-648">no</span></span>           |
| <span data-ttu-id="5af3a-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="5af3a-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="5af3a-650">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-650">no</span></span>             | <span data-ttu-id="5af3a-651">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-651">no</span></span>           |
| <span data-ttu-id="5af3a-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="5af3a-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="5af3a-653">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-653">no</span></span>             | <span data-ttu-id="5af3a-654">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-654">no</span></span>           |
| <span data-ttu-id="5af3a-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="5af3a-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="5af3a-656">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-656">no</span></span>             | <span data-ttu-id="5af3a-657">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-657">no</span></span>           |
| <span data-ttu-id="5af3a-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="5af3a-659">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-659">no</span></span>             | <span data-ttu-id="5af3a-660">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-660">no</span></span>           |
| <span data-ttu-id="5af3a-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="5af3a-662">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-662">no</span></span>             | <span data-ttu-id="5af3a-663">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-663">no</span></span>           |
| <span data-ttu-id="5af3a-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="5af3a-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="5af3a-665">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-665">no</span></span>             | <span data-ttu-id="5af3a-666">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-666">no</span></span>           |
| <span data-ttu-id="5af3a-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5af3a-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="5af3a-668">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-668">no</span></span>             | <span data-ttu-id="5af3a-669">いいえ</span><span class="sxs-lookup"><span data-stu-id="5af3a-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="5af3a-670">制限事項と既知の問題</span><span class="sxs-lookup"><span data-stu-id="5af3a-670">Limitations and known issues</span></span>
<span data-ttu-id="5af3a-671">以下は、制限事項と既知の問題のリストです。</span><span class="sxs-lookup"><span data-stu-id="5af3a-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="5af3a-672">プロジェクト スケジュール API は、**Microsoft Project のライセンスを持つユーザー** のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="5af3a-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="5af3a-673">次のユーザーは使用できません:</span><span class="sxs-lookup"><span data-stu-id="5af3a-673">They can't be used by:</span></span>
    - <span data-ttu-id="5af3a-674">アプリケーション ユーザー</span><span class="sxs-lookup"><span data-stu-id="5af3a-674">Application users</span></span>
    - <span data-ttu-id="5af3a-675">システム ユーザー</span><span class="sxs-lookup"><span data-stu-id="5af3a-675">System users</span></span>
    - <span data-ttu-id="5af3a-676">統合ユーザー</span><span class="sxs-lookup"><span data-stu-id="5af3a-676">Integration users</span></span>
    - <span data-ttu-id="5af3a-677">必要なライセンスを持っていない他のユーザー</span><span class="sxs-lookup"><span data-stu-id="5af3a-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="5af3a-678">各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。</span><span class="sxs-lookup"><span data-stu-id="5af3a-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="5af3a-679">各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。</span><span class="sxs-lookup"><span data-stu-id="5af3a-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="5af3a-680">Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5af3a-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="5af3a-681">**OperationSet** 障害ステータスと障害ログは現在利用できません。</span><span class="sxs-lookup"><span data-stu-id="5af3a-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="5af3a-682">プロジェクトとタスクの制限と境界</span><span class="sxs-lookup"><span data-stu-id="5af3a-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="5af3a-683">エラー処理</span><span class="sxs-lookup"><span data-stu-id="5af3a-683">Error handling</span></span>

   - <span data-ttu-id="5af3a-684">操作セットから生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **操作セット** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="5af3a-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="5af3a-685">プロジェクト スケジュール サービスから生成されたエラーを確認するには、**設定**\>**スケジュールの統合**\>**PSS エラーログ** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="5af3a-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="5af3a-686">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="5af3a-686">Sample scenario</span></span>

<span data-ttu-id="5af3a-687">このシナリオでは、プロジェクト、チームメンバー、4 つのタスク、および 2 つのリソース割り当てを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af3a-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="5af3a-688">次に、1 つのタスクを更新し、プロジェクトを更新し、1 つのタスクを削除し、1 つのリソース割り当てを削除して、タスクの依存関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="5af3a-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="5af3a-689">追加の例</span><span class="sxs-lookup"><span data-stu-id="5af3a-689">Additional samples</span></span>

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
