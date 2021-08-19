---
title: プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する
description: このトピックでは、プロジェクト スケジュール API を使用するための情報と使用例について解説します。
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 55bd9020275fbb72761b45ba09294f57266b418c0e5b506ba55a2a498aff24e5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008772"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

> [!IMPORTANT] 
> このトピックに記載されている機能の一部または全部は、プレビュー リリースの一部として提供されています。 コンテンツおよび機能は変更される場合があります。 

## <a name="scheduling-entities"></a>スケジューリング エンティティ

プロジェクト スケジュール API では、**スケジュール エンティティ** を使用した作成、更新、削除操作を実行する機能を提供します。 これらのエンティティは、Project for the Web のスケジューリング エンジンを介して管理されます。 **スケジューリング エンティティ** を使用した操作の作成、更新、および削除は、過去の Dynamics 365 Project Operations リリースに限定されていました。

次の表に、プロジェクト スケジュール エンティティの全リストを示します。

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

## <a name="project-schedule-apis"></a>プロジェクト スケジュール API

以下は、現在のプロジェクト スケジュール API のリストです。

- **msdyn_CreateProjectV1**: この API を使用してプロジェクトを作成できます。 プロジェクトとデフォルトのプロジェクト バケットがすぐに作成されます。
- **msdyn_CreateTeamMemberV1**: この API を使用して、プロジェクト チーム メンバーを作成できます。 チーム メンバーのレコードはすぐに作成されます。
- **msdyn_CreateOperationSetV1**: この API を使用して、トランザクション内で実行する必要のあるいくつかの要求をスケジュールできます。
- **msdyn_PSSCreateV1**: この API を使用してエンティティを作成できます。 エンティティは、作成操作をサポートするプロジェクト スケジュール エンティティのいずれかとなります。
- **msdyn_PSSUpdateV1**: この API を使用してエンティティを更新できます。 エンティティは、更新操作をサポートするプロジェクト スケジュール エンティティのいずれかとなります。
- **msdyn_PSSDeleteV1**: この API を使用してエンティティを削除できます。 エンティティには、削除操作をサポートするプロジェクト スケジュール エンティティのいずれかを指定できます。
- **msdyn_ExecuteOperationSetV1**: この API は、指定された操作セット内のすべての操作を実行するために使用されます。

## <a name="using-project-schedule-apis-with-operationset"></a>OperationSet でプロジェクト スケジュール API を使用する

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

## <a name="restricted-fields"></a>制限のあるフィールド

以下の表は、**作成** と **編集** が制限されるフィールドを定義しています。

### <a name="project-task"></a>プロジェクト タスク

| **論理名**                       | **作成可能** | **編集可能**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | いいえ             | いいえ               |
| msdyn_actualcost_base                  | いいえ             | いいえ               |
| msdyn_actualend                        | いいえ             | いいえ               |
| msdyn_actualsales                      | いいえ             | いいえ               |
| msdyn_actualsales_base                 | いいえ             | いいえ               |
| msdyn_actualstart                      | いいえ             | いいえ               |
| msdyn_costatcompleteestimate           | いいえ             | いいえ               |
| msdyn_costatcompleteestimate_base      | いいえ             | いいえ               |
| msdyn_costconsumptionpercentage        | いいえ             | いいえ               |
| msdyn_effortcompleted                  | いいえ             | いいえ               |
| msdyn_effortestimateatcomplete         | いいえ             | いいえ               |
| msdyn_iscritical                       | いいえ             | いいえ               |
| msdyn_iscriticalname                   | いいえ             | いいえ               |
| msdyn_ismanual                         | いいえ             | いいえ               |
| msdyn_ismanualname                     | いいえ             | いいえ               |
| msdyn_ismilestone                      | いいえ             | いいえ               |
| msdyn_ismilestonename                  | いいえ             | いいえ               |
| msdyn_LinkStatus                       | いいえ             | いいえ               |
| msdyn_linkstatusname                   | いいえ             | いいえ               |
| msdyn_msprojectclientid                | いいえ             | いいえ               |
| msdyn_plannedcost                      | いいえ             | いいえ               |
| msdyn_plannedcost_base                 | いいえ             | いいえ               |
| msdyn_plannedsales                     | いいえ             | いいえ               |
| msdyn_plannedsales_base                | いいえ             | いいえ               |
| msdyn_pluginprocessingdata             | いいえ             | いいえ               |
| msdyn_progress                         | いいえ             | いいえ (P4W の場合は"はい") |
| msdyn_remainingcost                    | いいえ             | いいえ               |
| msdyn_remainingcost_base               | いいえ             | いいえ               |
| msdyn_remainingsales                   | いいえ             | いいえ               |
| msdyn_remainingsales_base              | いいえ             | いいえ               |
| msdyn_requestedhours                   | いいえ             | いいえ               |
| msdyn_resourcecategory                 | いいえ             | いいえ               |
| msdyn_resourcecategoryname             | いいえ             | いいえ               |
| msdyn_resourceorganizationalunitid     | いいえ             | いいえ               |
| msdyn_resourceorganizationalunitidname | いいえ             | いいえ               |
| msdyn_salesconsumptionpercentage       | いいえ             | いいえ               |
| msdyn_salesestimateatcomplete          | いいえ             | いいえ               |
| msdyn_salesestimateatcomplete_base     | いいえ             | いいえ               |
| msdyn_salesvariance                    | いいえ             | いいえ               |
| msdyn_salesvariance_base               | いいえ             | いいえ               |
| msdyn_scheduleddurationminutes         | いいえ             | いいえ               |
| msdyn_scheduledend                     | いいえ             | いいえ               |
| msdyn_scheduledstart                   | いいえ             | いいえ               |
| msdyn_schedulevariance                 | いいえ             | いいえ               |
| msdyn_skipupdateestimateline           | いいえ             | いいえ               |
| msdyn_skipupdateestimatelinename       | いいえ             | いいえ               |
| msdyn_summary                          | いいえ             | いいえ               |
| msdyn_varianceofcost                   | いいえ             | いいえ               |
| msdyn_varianceofcost_base              | いいえ             | いいえ               |

### <a name="project-task-dependency"></a>プロジェクト タスクの依存関係

| **論理名**              | **作成可能** | **編集可能** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | いいえ             | いいえ           |
| msdyn_linktypename            | いいえ             | いいえ           |
| msdyn_predecessortask         | はい            | いいえ           |
| msdyn_predecessortaskname     | はい            | いいえ           |
| msdyn_project                 | はい            | いいえ           |
| msdyn_projectname             | はい            | いいえ           |
| msdyn_projecttaskdependencyid | はい            | いいえ           |
| msdyn_successortask           | はい            | いいえ           |
| msdyn_successortaskname       | はい            | いいえ           |

### <a name="resource-assignment"></a>リソース割り当て

| **論理名**             | **作成可能** | **編集可能** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | はい            | いいえ           |
| msdyn_bookableresourceidname | はい            | いいえ           |
| msdyn_bookingstatusid        | いいえ             | いいえ           |
| msdyn_bookingstatusidname    | いいえ             | いいえ           |
| msdyn_committype             | いいえ             | いいえ           |
| msdyn_committypename         | いいえ             | いいえ           |
| msdyn_effort                 | いいえ             | いいえ           |
| msdyn_effortcompleted        | いいえ             | いいえ           |
| msdyn_effortremaining        | いいえ             | いいえ           |
| msdyn_finish                 | いいえ             | いいえ           |
| msdyn_plannedcost            | いいえ             | いいえ           |
| msdyn_plannedcost_base       | いいえ             | いいえ           |
| msdyn_plannedcostcontour     | いいえ             | いいえ           |
| msdyn_plannedsales           | いいえ             | いいえ           |
| msdyn_plannedsales_base      | いいえ             | いいえ           |
| msdyn_plannedsalescontour    | いいえ             | いいえ           |
| msdyn_plannedwork            | いいえ             | いいえ           |
| msdyn_projectid              | はい            | いいえ           |
| msdyn_projectidname          | いいえ             | いいえ           |
| msdyn_projectteamid          | いいえ             | いいえ           |
| msdyn_projectteamidname      | いいえ             | いいえ           |
| msdyn_start                  | いいえ             | いいえ           |
| msdyn_taskid                 | いいえ             | いいえ           |
| msdyn_taskidname             | いいえ             | いいえ           |
| msdyn_userresourceid         | いいえ             | いいえ           |

### <a name="project-team-member"></a>プロジェクト チーム メンバー

| **論理名**                                 | **作成可能** | **編集可能** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | いいえ             | いいえ           |
| msdyn_creategenericteammemberwithrequirementname | いいえ             | いいえ           |
| msdyn_deletestatus                               | いいえ             | いいえ           |
| msdyn_deletestatusname                           | いいえ             | いいえ           |
| msdyn_effort                                     | いいえ             | いいえ           |
| msdyn_effortcompleted                            | いいえ             | いいえ           |
| msdyn_effortremaining                            | いいえ             | いいえ           |
| msdyn_finish                                     | いいえ             | いいえ           |
| msdyn_hardbookedhours                            | いいえ             | いいえ           |
| msdyn_hours                                      | いいえ             | いいえ           |
| msdyn_markedfordeletiontimer                     | いいえ             | いいえ           |
| msdyn_markedfordeletiontimestamp                 | いいえ             | いいえ           |
| msdyn_msprojectclientid                          | いいえ             | いいえ           |
| msdyn_percentage                                 | いいえ             | いいえ           |
| msdyn_requiredhours                              | いいえ             | いいえ           |
| msdyn_softbookedhours                            | いいえ             | いいえ           |
| msdyn_start                                      | いいえ             | いいえ           |

### <a name="project"></a>Project

| **論理名**                       | **作成可能** | **編集可能** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | いいえ             | いいえ           |
| msdyn_actualexpensecost_base           | いいえ             | いいえ           |
| msdyn_actuallaborcost                  | いいえ             | いいえ           |
| msdyn_actuallaborcost_base             | いいえ             | いいえ           |
| msdyn_actualsales                      | いいえ             | いいえ           |
| msdyn_actualsales_base                 | いいえ             | いいえ           |
| msdyn_contractlineproject              | はい            | いいえ           |
| msdyn_contractorganizationalunitid     | はい            | いいえ           |
| msdyn_contractorganizationalunitidname | はい            | いいえ           |
| msdyn_costconsumption                  | いいえ             | いいえ           |
| msdyn_costestimateatcomplete           | いいえ             | いいえ           |
| msdyn_costestimateatcomplete_base      | いいえ             | いいえ           |
| msdyn_costvariance                     | いいえ             | いいえ           |
| msdyn_costvariance_base                | いいえ             | いいえ           |
| msdyn_duration                         | いいえ             | いいえ           |
| msdyn_effort                           | いいえ             | いいえ           |
| msdyn_effortcompleted                  | いいえ             | いいえ           |
| msdyn_effortestimateatcompleteeac      | いいえ             | いいえ           |
| msdyn_effortremaining                  | いいえ             | いいえ           |
| msdyn_finish                           | はい            | はい          |
| msdyn_globalrevisiontoken              | いいえ             | いいえ           |
| msdyn_islinkedtomsprojectclient        | いいえ             | いいえ           |
| msdyn_islinkedtomsprojectclientname    | いいえ             | いいえ           |
| msdyn_linkeddocumenturl                | いいえ             | いいえ           |
| msdyn_msprojectdocument                | いいえ             | いいえ           |
| msdyn_msprojectdocumentname            | いいえ             | いいえ           |
| msdyn_plannedexpensecost               | いいえ             | いいえ           |
| msdyn_plannedexpensecost_base          | いいえ             | いいえ           |
| msdyn_plannedlaborcost                 | いいえ             | いいえ           |
| msdyn_plannedlaborcost_base            | いいえ             | いいえ           |
| msdyn_plannedsales                     | いいえ             | いいえ           |
| msdyn_plannedsales_base                | いいえ             | いいえ           |
| msdyn_progress                         | いいえ             | いいえ           |
| msdyn_remainingcost                    | いいえ             | いいえ           |
| msdyn_remainingcost_base               | いいえ             | いいえ           |
| msdyn_remainingsales                   | いいえ             | いいえ           |
| msdyn_remainingsales_base              | いいえ             | いいえ           |
| msdyn_replaylogheader                  | いいえ             | いいえ           |
| msdyn_salesconsumption                 | いいえ             | いいえ           |
| msdyn_salesestimateatcompleteeac       | いいえ             | いいえ           |
| msdyn_salesestimateatcompleteeac_base  | いいえ             | いいえ           |
| msdyn_salesvariance                    | いいえ             | いいえ           |
| msdyn_salesvariance_base               | いいえ             | いいえ           |
| msdyn_scheduleperformance              | いいえ             | いいえ           |
| msdyn_scheduleperformancename          | いいえ             | いいえ           |
| msdyn_schedulevariance                 | いいえ             | いいえ           |
| msdyn_taskearlieststart                | いいえ             | いいえ           |
| msdyn_teamsize                         | いいえ             | いいえ           |
| msdyn_teamsize_date                    | いいえ             | いいえ           |
| msdyn_teamsize_state                   | いいえ             | いいえ           |
| msdyn_totalactualcost                  | いいえ             | いいえ           |
| msdyn_totalactualcost_base             | いいえ             | いいえ           |
| msdyn_totalplannedcost                 | いいえ             | いいえ           |
| msdyn_totalplannedcost_base            | いいえ             | いいえ           |


## <a name="limitations-and-known-issues"></a>制限事項と既知の問題
以下は、制限事項と既知の問題のリストです。

- プロジェクト スケジュール API は、**Microsoft Project のライセンスを持つユーザー** のみが使用できます。 次のユーザーは使用できません:
    - アプリケーション ユーザー
    - システム ユーザー
    - 統合ユーザー
    - 必要なライセンスを持っていない他のユーザー
- 各 **OperationSet** に割り当てられるのは最大 100 件の操作までです。
- 各ユーザーが持つことができるのは、最大 10 件のオープン **OperationSet** です。
- Project Operations は現在、プロジェクトで最大 500 件の合計タスクをサポートしています。
- **OperationSet** 障害ステータスと障害ログは現在利用できません。
- [プロジェクトとタスクの制限と境界](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>エラー処理

   - 操作セットから生成されたエラーを確認するには、**設定** \> **スケジュールの統合** \> **操作セット** にアクセスしてください。
   - プロジェクト スケジュール サービスから生成されたエラーを確認するには、**設定**\>**スケジュールの統合**\>**PSS エラーログ** にアクセスしてください。

## <a name="sample-scenario"></a>シナリオ例

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

## <a name="additional-samples"></a>追加の例

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
