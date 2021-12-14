---
title: プロジェクト スケジューリング ログ
description: このトピックは、プロジェクト スケジューリング ログを使用して、プロジェクト スケジューリング サービスおよびプロジェクト スケジューリング API に関連するエラーを追跡するのに役立つ情報とサンプルを提供します。
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877633"
---
# <a name="project-scheduling-logs"></a>プロジェクト スケジューリング ログ

_**適用対象:** リソース/非在庫ベースのシナリオの Project Operations、ライト展開 - 見積もり請求の取引_、_Project for the Web_

Microsoft Dynamics 365 Project Operations は [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) をその主要なスケジューリング エンジンとして使用しています。 標準の Microsoft Dataverse Web アプリケーション プログラミング インターフェイス (API) を使用する代わりに、Project Operations は、新しいプロジェクト スケジューリング API を使用して、プロジェクト タスク、リソース割り当て、タスクの依存関係、プロジェクト バケット、プロジェクト チーム メンバーを作成、更新、削除します。 ただし、作成、更新、または削除操作をプログラムで WBS (作業分解構造) エンティティに対して実行すると、エラーが発生する可能性があります。 これらのエラーと操作の履歴を追跡するために、2 つの新しい管理ログ、**操作セット** と **プロジェクト スケジューリング サービス (PSS)** が実装されました。 これらのログにアクセスするには、**設定** \> **スケジュール統合** に移動します。

次の図は、プロジェクト スケジューリング ログのデータ モデルを示しています。

![プロジェクト スケジューリング モードのデータ モデル。](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>操作設定ログ

操作セットログは、プロジェクト、プロジェクトタスク、リソース割り当て、タスクの依存関係、プロジェクト バケット、またはプロジェクト チーム メンバーに対して、1 つまたは複数の作成、更新、または削除操作をバッチで実行するために使用される操作セットの実行を追跡します。 **ステータスでの操作** フィールドには、操作セットの全体的なステータスが表示されます。 操作セットのペイロードの詳細は、関連する操作セットの詳細レコードにキャプチャされます。

### <a name="operation-set"></a>操作セット

次のテーブルは、**操作セット** エンティティに関連したフィールドを示しています。

| スキーマ名            | Description                                                                                                  | 表示名            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | 操作セットが完了または失敗した日時。                                                | CompletedOn            |
| msdyn_correlationid   | 要求の **correlationId** 値。                                                                  | 相関 ID          |
| msdyn_description     | 操作セットの説明。                                                                        | Description            |
| msdyn_executedon      | レコードが実行された日時。                                                                       | 実行日            |
| msdyn_operationsetId  | エンティティ インスタンスの一意識別子。                                                                   | OperationSet           |
| msdyn_Project         | 操作セットに関連するプロジェクト。                                                            | Project                |
| msdyn_projectid       | 要求の **projectId** 値。                                                                      | ProjectId (廃止) |
| msdyn_projectName     | 適用なし。                                                                                              | 適用なし         |
| msdyn_PSSErrorLog     | 操作セットに関連付けられているプロジェクト スケジューリング サービス エラー ログの一意識別子。 | PSS エラー ログ          |
| msdyn_PSSErrorLogName | 適用なし。                                                                                              | 適用なし         |
| msdyn_status          | 操作セットの状態。                                                                             | Status                 |
| msdyn_statusName      | 適用なし。                                                                                              | 適用なし         |
| msdyn_useraadid       | この要求が属するユーザーの Azure Active Directory (Azure AD) オブジェクト ID。                     | UserAADID              |

### <a name="operation-set-detail"></a>操作セットの詳細

次のテーブルは、**操作セットの詳細** エンティティに関連したフィールドを示しています。

| スキーマ名                 | Description                                                                                 | 表示名           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | 要求に対してシリアル化した Dataverse フィールド。                                            | CdsPayload            |
| msdyn_entityname           | この要求のエンティティ名。                                                     | EntityName            |
| msdyn_httpverb             | 要求メソッド。                                                                         | HTTP 動詞 (廃止) |
| msdyn_httpverbName         | 適用なし。                                                                             | 適用なし        |
| msdyn_operationset         | このレコードが属する操作セットの一意識別子。                      | OperationSet          |
| msdyn_operationsetdetailId | エンティティ インスタンスの一意識別子。                                                  | OperationSet の詳細   |
| msdyn_operationsetName     | 適用なし。                                                                             | 適用なし        |
| msdyn_operationtype        | 操作セットの詳細の操作の種類。                                             | OperationType         |
| msdyn_operationtypeName    | 適用なし。                                                                             | 適用なし        |
| msdyn_psspayload           | 要求のシリアル化されたプロジェクト スケジューリング サービス フィールド。                           | PssPayload            |
| msdyn_recordid             | 要求レコードの識別子。                                                       | レコード ID             |
| msdyn_requestnumber        | 要求が受信された順序の識別に使用する自動生成された番号。 | 要求番号        |

## <a name="project-scheduling-service-error-logs"></a>プロジェクト スケジューリング サービスのエラー ログ

プロジェクト スケジューリング サービスのエラーログは、プロジェクト スケジューリング操作を **保存** または **開く** を試行したときに発生するエラーをキャプチャします。 これらのログが生成されるサポートされるシナリオは 3 つあります。

- ユーザーが開始したアクションは重大に失敗します (たとえば、特権がないために割り当てを作成できません)。
- プロジェクト スケジューリング サービスは、エンティティに対してプログラムで作成、更新、削除、またはその他のカスケード操作を実行することはできません。
- レコードを開くことができない場合 (たとえば、プロジェクトを開いたり、チームメンバーの情報を更新したりした場合)、ユーザーにエラーが発生します。

### <a name="project-scheduling-service-log"></a>プロジェクト スケジューリング サービス ログ

次のテーブルは、プロジェクト スケジューリング サービス ログに含まれるフィールドを示しています。

| スキーマ名          | Description                                                                    | 表示名    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | この例外のコール スタック。                                               | コール スタック     |
| msdyn_correlationid | エラーの関連付け ID。                                               | 相関 ID  |
| msdyn_errorcode     | Dataverse エラー コードまたは HTTP エラー コードを格納するために使用されるフィールド。 | エラー コード     |
| msdyn_HelpLink      | 公開ヘルプ ドキュメントへのリンク。                                       | ヘルプのリンク      |
| msdyn_log           | プロジェクト スケジューリング サービスからのログ。                                   | ログ            |
| msdyn_project       | エラー ログに関連付けられたプロジェクト。                             | Project        |
| msdyn_projectName   | 操作セットのペイロードが永続化される場合のプロジェクトの名前。 | 適用なし |
| msdyn_psserrorlogId | エンティティ インスタンスの一意識別子。                                     | PSS エラー ログ  |
| msdyn_SessionId     | プロジェクトのセッション ID。                                                        | セッション ID     |

## <a name="error-log-cleanup"></a>エラー ログのクリーンアップ

規定では、プロジェクト スケジューリング サービスのエラー ログと操作セット ログの両方を 90 日ごとにクリーンアップできます。 90 日経過したすべての失敗レコードは削除されます。 ただし、**プロジェクト パラメータ** ページの **msdyn_StateOperationSetAge** フィールドの値を変更することにより、管理者はクリーンアップ範囲を 1 〜 120 日になるように調整できます。 この値を変更する方法はいくつかあります。

- カスタムページを作成し、**古い操作セットの年齢** フィールドを追加することで、**プロジェクト パラメータ** をカスタマイズします。
- [WebApi ソフトウェア開発キット (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) を使用するクライアント コードを使用します。
- モデル駆動型アプリの Xrm SDK **updateRecord** メソッド (クライアント API リファレンス) を使用する Service SDK コードを使用します。 Power Apps には、**updateRecord** メソッドの説明とサポートされているパラメータが含まれています。

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
