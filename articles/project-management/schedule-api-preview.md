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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>スケジュール API を使用して、スケジューリング エンティティで操作を実行する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

> [!IMPORTANT] 
> このトピックに記載されている機能の一部または全部は、プレビュー リリースの一部として提供されています。 コンテンツおよび機能は変更される場合があります。 

## <a name="scheduling-entities"></a>スケジューリング エンティティ

スケジュール API は、**スケジューリング エンティティ** を使って操作を作成、更新、および削除を実行する機能を提供します。。 これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。 **スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。

次の表は、**スケジューリング エンティティ** の完全なリストです。

| エンティティ名  | エンティティの論理名 |
| --- | --- |
| Project | msdyn_project |
| プロジェクト タスク  | msdyn_projecttask  |
| プロジェクト タスクの依存関係  | msdyn_projecttaskdependency  |
| リソース割り当て | msdyn_resourceassignment |
| プロジェクト バケット  | msdyn_projectbucket |
| プロジェクト チーム メンバー | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet は、スケジュールに影響を与える複数の要求をトランザクション内で処理する必要がある場合に使用できる作業単位パターンです。

## <a name="schedule-apis"></a>スケジュール API

以下は、現在のスケジュール API のリストです。

- **msdyn_CreateProjectV1**: この API を使用してプロジェクトを作成できます。 プロジェクトとデフォルトのプロジェクト バケットがすぐに作成されます。
- **msdyn_CreateTeamMemberV1**: この API を使用して、プロジェクト チーム メンバーを作成できます。 チーム メンバーのレコードはすぐに作成されます。
- **msdyn_CreateOperationSetV1**: この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。
- **msdyn_PSSCreateV1**: この API を使用してエンティティを作成できます。 エンティティは、作成操作をサポートする任意のスケジューリング エンティティにできます。
- **msdyn_PSSUpdateV1**: この API を使用してエンティティを更新できます。 エンティティは、更新操作をサポートする任意のスケジューリング エンティティにできます。
- **msdyn_PSSDeleteV1**: この API を使用してエンティティを削除できます。 エンティティは、削除操作をサポートする任意のスケジューリング エンティティにできます。
- **msdyn_ExecuteOperationSetV1**: この API は、指定された操作セット内のすべての操作を実行するために使用されます。

## <a name="using-schedule-apis-with-operationset"></a>OperationSet と ScheduleAPI の併用

**CreateProjectV1** と **CreateTeamMemberV1** 両方があるレコードは直ちに作成されるため、これらの API は **OperationSet** で直接使用できません。 ただし、API を使用して必要なレコードを作成し、**OperationSet** を作成し、これらの事前に作成されたレコードを **OperationSet** で使用できます。

## <a name="supported-operations"></a>サポートされている操作

| スケジューリング エンティティ | 作成​​ | 更新プログラム | Delete キー | 重要な考慮事項 |
| --- | --- | --- | --- | --- |
プロジェクト タスク | 有効 | 有効 | 有効 | いいえ​​ |
| プロジェクト タスクの依存関係 | 有効 | 有効 | | プロジェクト タスクの依存関係レコードは更新されません。 代わりに、古いレコードを削除して、新しいレコードを作成できます。 |
| リソース割り当て | 有効 | 有効 | | 次のフィールドを使用した操作はサポートされていません: **BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining**、および **PlannedWork**。 リソース割り当てレコードは更新されません。 代わりに、古いレコードを削除して、新しいレコードを作成できます。 |
| プロジェクト バケット | N/A | N/A | N/A | 既定のバケットは、**CreateProjectV1** API を使って作成されます。 |
| プロジェクト チーム メンバー | 有効 | 有効 | 有効 | 作成操作には、**CreateTeamMemberV1** API を使用します。 |
| Project | 有効 | 有効 | N/A | 次のフィールドを使用した操作はサポートされていません: **StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、 **CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart**、および **Duration**。 |

これらの API は、カスタムフィールドを含むエンティティ オブジェクトを使用して呼び出すことができます。

ID プロパティは省略可能です。 提供されている場合、システムはそれを使用しようとし、使用できない場合は例外をスローします。 提供されていない場合は、システムが生成します。

## <a name="limitations-and-known-issues"></a>制限事項と既知の問題
以下は、制限事項と既知の問題のリストです。

- スケジュール API は、**Microsoft Project ライセンスを持つユーザー** のみが使用できます。 次のユーザーは使用できません:
    - アプリケーション ユーザー
    - システム ユーザー
    - 統合ユーザー
    - 必要なライセンスを持っていない他のユーザー
- 各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。
- 各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。
- Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。
- **OperationSet** 障害ステータスと障害ログは現在利用できません。
- スケジュール API はパブリック プレビューにあります。 実稼働環境におけるこれらの API の使用は、Microsoft ではサポートされていません。

## <a name="sample-scenario"></a>シナリオ例

このシナリオでは、プロジェクト、チームメンバー、4 つのタスク、および 2 つのリソース割り当てを作成します。 次に、1 つのタスクを更新し、プロジェクトを更新し、1 つのタスクを削除し、1 つのリソース割り当てを削除して、タスクの依存関係を作成します。

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

## <a name="additional-samples"></a>追加の例

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