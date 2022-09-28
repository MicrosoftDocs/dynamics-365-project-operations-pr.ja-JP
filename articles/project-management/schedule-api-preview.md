---
title: プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する
description: この記事では、プロジェクト スケジュール API を使用するための情報とサンプルを提供します。
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541130"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


**スケジューリング エンティティ**

プロジェクト スケジュール API では、**スケジュール エンティティ** を使用した作成、更新、削除操作を実行する機能を提供します。 これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。 **スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。

次の表に、プロジェクト スケジュール エンティティの全リストを示します。

| **エンティティ名**         | **エンティティの論理名**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| プロジェクト タスク            | msdyn_projecttask           |
| プロジェクト タスクの依存関係 | msdyn_projecttaskdependency |
| リソース割り当て     | msdyn_resourceassignment    |
| プロジェクト バケット          | msdyn_projectbucket         |
| プロジェクト チーム メンバー     | msdyn_projectteam           |
| プロジェクト チェックリスト      | msdyn_projectchecklist      |
| プロジェクト ラベル           | msdyn_projectlabel          |
| プロジェクト タスクとラベルの関連付け   | +msdyn_projecttasktolabel    |
| プロジェクト スプリント          | msdyn_projectsprint         |

**OperationSet**

OperationSet は、スケジュールに影響を与える複数の要求をトランザクション内で処理する必要がある場合に使用できる作業単位パターンです。

**プロジェクト スケジュール API**

以下は、現在のプロジェクト スケジュール API のリストです。

| **API**                                 | 説明設定                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | この API は、プロジェクトを作成するために使用されます。 プロジェクトと規定のプロジェクト バケットがすぐに作成されます。                         |
| **msdyn_CreateTeamMemberV1**            | この API はプロジェクト チーム メンバーを作成するために使用されます。 チーム メンバーのレコードはすぐに作成されます。                                  |
| **msdyn_CreateOperationSetV1**          | この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。                                        |
| **msdyn_PssCreateV1**                   | この API は、エンティティを作成するために使用されます。 エンティティは、作成操作をサポートするプロジェクト スケジュール エンティティのいずれかとなります。 |
| **msdyn_PssUpdateV1**                   | この API は、エンティティを更新するために使用されます。 エンティティは、更新の操作をサポートするいずれかのプロジェクト スケジューリング エンティティの場合がある  |
| **msdyn_PssDeleteV1**                   | この API は、エンティティを削除するために使用されます。 エンティティには、削除操作をサポートするプロジェクト スケジュール エンティティのいずれかを指定できます。 |
| **msdyn_ExecuteOperationSetV1**         | この API を使用して、指定された操作セット内ですべての操作を実行します。                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | この API は、リソース割り当ての計画された作業輪郭を更新するために使用されます。                                                        |



**OperationSet でプロジェクト スケジュール API を使用する**

**CreateProjectV1** と **CreateTeamMemberV1** 両方があるレコードは直ちに作成されるため、これらの API は **OperationSet** で直接使用できません。 ただし、API を使用して必要なレコードを作成し、**OperationSet** を作成し、これらの事前に作成されたレコードを **OperationSet** で使用できます。

**サポートされている操作**

| **スケジューリング エンティティ**   | **作成** | **更新プログラム** | **Delete** | **重要な考慮事項**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| プロジェクト タスク            | 有効        | 有効        | 有効        | **Progress**、**EffortCompleted**、および **EffortRemaining** のフィールドは、Project for the Web で編集できますが、Project Operations では編集できません。                                                                                                                                                                                             |
| プロジェクト タスクの依存関係 | イエス        | 番号         | イエス        | プロジェクト タスクの依存関係レコードは更新されません。 代わりに、古いレコードを削除して、新しいレコードを作成できます。                                                                                                                                                                                                                                 |
| リソース割り当て     | イエス        | イエス\*      | イエス        | 次のフィールドを使用した操作はサポートされていません: **BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining**、および **PlannedWork**。 リソース割り当てレコードは更新されません。 代わりに、古いレコードを削除して、新しいレコードを作成できます。 リソース割り当て配分型を更新するために、別の API が提供されています。 |
| プロジェクト バケット          | イエス        | イエス        | イエス        | 規定のバケットは、**CreateProjectV1** APIを使用して作成されます。 プロジェクト バケットの作成と削除のサポートは、アップデート リリース 16 で追加されました。                                                                                                                                                                                                   |
| プロジェクト チーム メンバー     | 有効        | 有効        | 有効        | 作成操作には、**CreateTeamMemberV1** API を使用します。                                                                                                                                                                                                                                                                                           |
| Project                 | 有効        | 有効        |            | 次のフィールドを使用した操作はサポートされていません: **StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、 **CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart**、および **Duration**。                                                                                       |
| プロジェクト チェックリスト      | イエス        | イエス        | イエス        |                                                                                                                                                                                                                                                                                                                                                         |
| プロジェクト ラベル           | 番号         | イエス        | 番号         | ラベル名は変更できます。 この機能は、Project for the Web でのみ利用可能                                                                                                                                                                                                                                                                      |
| プロジェクト タスクとラベルの関連付け   | イエス        | 番号         | イエス        | この機能は、Project for the Web でのみ利用可能                                                                                                                                                                                                                                                                                                  |
| プロジェクト スプリント          | イエス        | イエス        | イエス        | **開始** フィールドは、**終了** フィールドより前の日付である必要があります。 同じプロジェクトのスプリントが重複することはできません。 この機能は、Project for the Web でのみ利用可能                                                                                                                                                                    |




ID プロパティは省略可能です。 提供されている場合、システムはそれを使用しようとし、使用できない場合は例外をスローします。 提供されていない場合は、システムが生成します。

**制限事項と既知の問題**

以下は、制限事項と既知の問題のリストです。

-   プロジェクト スケジュール API は、**Microsoft Project のライセンスを持つユーザー** のみが使用できます。 次のユーザーは使用できません:
    -   アプリケーション ユーザー
    -   システム ユーザー
    -   統合ユーザー
    -   必要なライセンスを持っていない他のユーザー
-   各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。
-   各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。
-   Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。
-   リソース割り当て配分型の各更新オペレーションは、1 つのオペレーションとしてカウントされます。
-   更新された配分型の各リストには、最大 100 のタイム スライスを含めることができます。
-   **OperationSet** 障害ステータスと障害ログは現在利用できません。
-   プロジェクトごとに最大 400 のスプリントがあります。
-   [プロジェクトとタスクの制限と境界](/project-for-the-web/project-for-the-web-limits-and-boundaries)。
-   ラベルは現在、Project for the Web でのみ利用可能です。

**エラー処理**

-   操作セットから生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **操作セット** にアクセスしてください。
-   プロジェクト スケジュール サービスから生成されたエラーを確認するには、**設定**\>**スケジュールの統合**\>**PSS エラーログ** にアクセスしてください。

**リソース割り当て配分型の編集**

エンティティを更新する他のすべてのプロジェクト スケジューリング API とは異なり、リソース割り当て配分型 API は、1 つのエンティティ、msydn_resourceassignment の 1 つのフィールド msdyn_plannedwork の更新のみを担当します。

指定されたスケジュール モードは次のとおりです。

-   **固定単位**
-   プロジェクト カレンダーは9時から5時で、月曜日、火曜日、木曜日、金曜日 (水曜日は休み)
-   リソース カレンダーは月曜から金曜の 9 時から 1 時まで (PST)

この課題は 1 週間、1 日 4 時間です。 これは、リソース カレンダーが 9時から 1 時まで (PST) (1 日 4 時間) であるためです。

| &nbsp;     | Task | Start Date | 終了日付  | 品質 | 2022/6/13 | 2022/6/14 | 2022/6/15 | 2022/6/16 | 2022/6/17 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 ワーカー |  T1  | 2022/6/13  | 2022/6/17 | 20       | 4         | 4         | 4         | 4         | 4         |

たとえば、ワーカーが今週 1 日 3 時間だけ働くようにし、1 時間は他のタスクに使用できるようにする場合です。

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours のサンプル ペイロード

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

これは、Update Contour Schedule API が実行された後の割り当てです。

| &nbsp;     | Task | Start Date | 終了日付  | 品質 | 2022/6/13 | 2022/6/14 | 2022/6/15 | 2022/6/16 | 2022/6/17 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 ワーカー | T1   | 2022/6/13  | 2022/6/17 | 15       | 3         | 3         | 3         | 3         | 3         |


**シナリオ例**

このシナリオでは、プロジェクト、チームメンバー、4 つのタスク、および 2 つのリソース割り当てを作成します。 次に、1 つのタスクを更新し、プロジェクトを更新し、1 つのタスクを削除し、1 つのリソース割り当てを削除して、タスクの依存関係を作成します。

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

** 追加の例

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
