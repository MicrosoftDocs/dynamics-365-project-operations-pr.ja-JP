---
title: Power Automate でプロジェクト スケジュール API を使用する
description: このトピックは、プロジェクト スケジュール アプリケーション プログラミング インターフェイス (API) を使用するサンプル フローを提供します。
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597712"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Power Automate でプロジェクト スケジュール API を使用する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

このトピックは、Microsoft Power Automate を使用して完全なプロジェクト計画を作成する方法、操作セットを作成する方法、およびエンティティを更新する方法を示すサンプル フローについて説明しています。 この例は、プロジェクト、プロジェクトチームのメンバー、操作セット、プロジェクト タスク、リソースの割り当てを作成する方法を示しています。 このトピックは、エンティティを更新して操作セットを実行する方法についても説明しています。

以下は、このトピックのサンプル フローに記載されているステップの完全なリストです。

1. [PowerApps トリガーを作成する](#1)
2. [プロジェクトの作成](#2)
3. [チーム メンバーの変数を初期化する](#3)
4. [汎用チーム メンバーの作成](#4)
5. [操作セットの作成](#5)
6. [プロジェクト バケットの作成](#6)
7. [リンク状態の変数を初期化する](#7)
8. [タスクの数の変数を初期化する](#8)
9. [プロジェクト タスク ID の変数を初期化する](#9)
10. [終点](#10)
11. [プロジェクト タスクを設定する](#11)
12. [プロジェクト タスクを作成する](#12)
13. [リソース割り当てを作成する](#13)
14. [変数を減らす](#14)
15. [プロジェクト タスクの名前を変更する](#15)
16. [操作セットの実行](#16)

## <a name="assumptions"></a>前提条件

このトピックは、Dataverse プラットフォーム、クラウド フロー、プロジェクト スケジュール アプリケーション プログラミング インターフェイス (API) の基本的な知識がある事を推定しています。 詳細については、このトピックの後にある [参照](#references) セクションをご覧ください。

## <a name="create-a-flow"></a>フローの作成

### <a name="select-an-environment"></a>環境を選択する

自分の環境で、Power Automate フローを作成できます。

1. <https://flow.microsoft.com> に移動し、管理者資格情報を使用してサインインします。
2. 右上隅で、**環境** を選択します。
3. 一覧から、Dynamics 365 Project Operations がインストールされている環境を選択します。

### <a name="create-a-solution"></a>ソリューションの作成

次のステップに従って、[ソリューション対応フロー](/power-automate/overview-solution-flows) を作成します。 ソリューション対応フローを作成することにより、フローをより簡単にエクスポートして後で使用することができます。

1. ナビゲーション ウィンドウで、**ソリューション** を選択します。
2. **ソリューション** ページで、**新しいソリューション** を選択します。
3. **新規ソリューション** ダイアログ ボックスで、必須フィールドを設置して、**作成** を選択します。

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>ステップ 1: PowerApps トリガーを作成する

1. **ソリューション** ページで、作成したマイ自動化ソリューションを選択して、**新規** を選択します。
2. 左ウィンドウで、**クラウド フロー** \> **オートメーション** \> **クラウド フロー** \> **インスタント** を選択します。
3. **フロー名** フィールドで、**API デモ フローのスケジュール** を入力します。
4. **このフローをトリガーする方法を選択** リストで、**Power Apps** を選択します。 Power Apps トリガーを作成する時、ロジックは作成者としてのあなた次第です。 このトピックでは、テストのために入力パラメーターを空白のままにします。
5. **作成** を選択します。

## <a name="step-2-create-a-project"></a><a id="2"></a>手順2 : プロジェクトの作成

これらのステップに従って、サンプル プロジェクトを作成します。

1. 作成したフローで、**新規ステップ** を選択します。

    ![新しいステップを追加します。](media/newstep.png)

2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。

    ![操作の選択](media/chooseactiontab.png)

3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。

![ステップの名前変更](media/renamestep.png)

4. ステップの名前を **タスクの作成** に変更します。
5. **アクション名** フィールドで、**msdyn\_CreateProjectV1** を選択します。
6. **msdyn\_subject** フィールドで、**動的コンテンツを追加する** を選択します。
7. **Expression** タブの機能フィールドで、**プロジェクト名 - utcNow()** を入力します。
8. **OK** を選択します。

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>ステップ 3: チーム メンバーの変数を初期化する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**変数を初期化する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. このステップ **Init チーム メンバー** の名前を変更します。
5. **名前** フィールドで、**TeamMemberAction** と入力します。
6. **タイプ** フィールドで、**文字列** を選択します。
7. **値** フィールドに、**msdyn\_CreateTeamMemberV1** と入力します。

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>ステップ 4: 汎用プロジェクトチームメンバーを作成する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. このステップ **Init チーム メンバー** の名前を変更します。
5. **アクション名** フィールドで、**動的コンテンツ** ダイアログ ボックスで **TeamMemberAction** を選択します。
6. **アクション パラメータ** フィールドに、次のパラメータ情報を入力します。

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    パラメータの説明を以下に示します。

    - **\@\@odata.type** – エンティティ名。 例えば、**"Microsoft.Dynamics.CRM.msdyn\_projectteam"** と入力します。
    - **msdyn\_ projectteamid** – プロジェクト チーム ID の主キー。 この値は、グローバル一意識別子 (GUID) 式です。   この ID は、式タブから生成されます。

    - **msdyn\_project\@odata.bind** – 所有するプロジェクトのプロジェクト ID。 この値は、"プロジェクトの作成" ステップの応答から得られる動的コンテンツになります。 必ずフル パスを入力し、括弧の間に動的コンテンツを追加してください。 引用符が必要です。 例えば、**"/msdyn\_projects(ADD DYNAMIC CONTENT)"** と入力します。
    - **msdyn\_name** – チームメンバーの名前。 たとえば、**"ScheduleAPIDemoTM1"** と入力します。

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>ステップ 5: 操作セットの作成

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **操作セットの作成** の名前を変更します。
5. **アクション名** フィールドで、**msdyn\_CreateOperationSetV1** Dataverse カスタム アクションを選択します。
6. **説明** フィールドに、**ScheduleAPIDemoOperationSet** と入力します。
7. **プロジェクト** フィールドに、**/msdyn\_projects(** と入力します。
8. **動的コンテンツ** ダイアログ ボックスで、**msdyn\_CreateProjectV1Response ProjectId** を選択します。
9. **プロジェクト** フィールドに、**)** と入力します。

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>ステップ 6: プロジェクト バケットを生成する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**新しい行を追加する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **バケットの作成** の名前を変更します。
5. **テーブル名** フィールドで、**プロジェクト バケット** を選択します。
6. **名前** フィールドで、**ScheduleAPIDemoBucket1** と入力します。
7. **プロジェクト** フィールドに対して、**動的コンテンツ** ダイアログボックスで **msdyn\_CreateProjectV1Response ProjectId** を選択します。

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>ステップ 7: リンクの状態の変数を初期化する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**変数を初期化する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **Init linkstatus** の名前を変更します。
5. **名前** フィールドで、**linkstatus** と入力します。
6. **タイプ** フィールドで、**整数** を選択します。
7. **数値** フィールドに、**192350000** と入力します。

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>ステップ 8: タスク数の変数を初期化する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**変数を初期化する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップの名 **タスク数の初期化** の名前を変更します。
5. **名前** フィールドで、**タスク数** と入力します。
6. **タイプ** フィールドで、**整数** を選択します。
7. **数値** フィールドに、**5** と入力します。

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>ステップ 9: プロジェクト タスク ID の変数を初期化する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**変数を初期化する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **Init ProjectTaskID** の名前を変更します。
5. **名前** フィールドで、**タスク数** と入力します。
6. **タイプ** フィールドで、**文字列** を選択します。
7. **値** フィールドに対して、式ビルダーに **guid()** と入力します。

## <a name="step-10-do-until"></a><a id="10"></a>ステップ 10: 終点

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**終点** と入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 条件文の最初の値を **動的コンテンツ** ダイアログ ボックスからの **タスクの数** 変数に設定します。
4. 条件を **以下** にセットします。
5. 条件ステートメントの 2 番目の値を **0** に設定します。

## <a name="step-11-set-a-project-task"></a><a id="11"></a>ステップ 11: プロジェクト タスクを設定する

1. フローで、**新規ステップ** を選択します。
2. **操作の選択** ダイアログ ボックスで、検索フィールドに、**変数を設定** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **プロジェクト タスクの設定** の名前を変更します。
5. **名前** フィールドで **msdyn\_projecttaskid** を入力または選択します。
6. **値** フィールドに対して、式ビルダーに **guid()** と入力します。

## <a name="step-12-create-a-project-task"></a><a id="12"></a>ステップ 12: プロジェクト タスクを生成する

次のステップに従って、現在のプロジェクトと作成したプロジェクトバケットに属する一意の ID を持つプロジェクト タスクを作成します。

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **プロジェクト タスクの作成** の名前を変更します。
5. **アクション名** フィールドで、**msdyn\_PssCreateV1** を選択します。
6. **エンティティ** フィールドに、次のパラメータ情報を入力します。

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    パラメータの説明を以下に示します。

    - **\@\@odata.type** – エンティティ名。 例えば、**"Microsoft.Dynamics.CRM.msdyn\_projecttask"** と入力します。
    - **msdyn\_projecttaskid** – タスクの一意の ID。 この値は **msdyn\_ projecttaskid** からの動的変数に設定する必要があります。
    - **msdyn\_project\@odata.bind** – 所有するプロジェクトのプロジェクト ID。 この値は、"プロジェクトの作成" ステップの応答から得られる動的コンテンツになります。 必ずフル パスを入力し、括弧の間に動的コンテンツを追加してください。 引用符が必要です。 例えば、**"/msdyn\_projects(ADD DYNAMIC CONTENT)"** と入力します。
    - **msdyn\_subject** – 任意のタスク名。
    - **msdyn\_ projectbucket\@ odata.bind** – タスクを含むプロジェクト バケット。 この値は、"バケットの作成" ステップの応答から得られる動的コンテンツになります。 必ずフル パスを入力し、括弧の間に動的コンテンツを追加してください。 引用符が必要です。 例えば、**"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"** と入力します。
    - **msdyn\_start** – 開始日の動的コンテンツ。 たとえば、明日は **"addDays(utcNow(), 1)"** のように表されます。
    - **msdyn\_scheduledstart** – スケジュールされた開始日。 たとえば、明日は **"addDays(utcNow(), 1)"** のように表されます。
    - **msdyn\_scheduleend** – スケジュールされた終了日。 将来の日付を選択します。 たとえば、**"addDays(utcNow(), 5)"** を指定します。
    - **msdyn\_LinkStatus** – リンクのステータス。 たとえば、**"192350000"** と入力します。

7. **OperationSetId** フィールドに対して、**Dynamic content** ダイアログ ボックスで **msdyn\_CreateOperationSetV1Response** を選択します。

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>ステップ 13: リソース割り当てを作成する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. このステップ **割り当ての作成** の名前を変更します。
5. **アクション名** フィールドで、**msdyn\_PssCreateV1** を選択します。
6. **エンティティ** フィールドに、次のパラメータ情報を入力します。

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **OperationSetId** フィールドに対して、**Dynamic content** ダイアログ ボックスで **msdyn\_CreateOperationSetV1Response** を選択します。

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>ステップ 14: 変数を減らす

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**変数を減らす** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. **名前** フィールドで、**タスク数** を選択します。
4. **数値** フィールドに、**1** と入力します。

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>ステップ 15: プロジェクト タスクの名前を変更する

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **プロジェクト タスクの名前を変更する** の名前を変更します。
5. **アクション名** フィールドで、**msdyn\_PssUpdateV1** を選択します。
6. **エンティティ** フィールドに、次のパラメータ情報を入力します。

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **OperationSetId** フィールドに対して、**Dynamic content** ダイアログ ボックスで **msdyn\_CreateOperationSetV1Response** を選択します。

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>ステップ 16: 操作セットの実行

1. フローで、**新規ステップ** を選択します。
2. **操作を選択する** ダイアログ ボックスで、検索フィールドに、**アンバウンド アクションを実行する** を入力します。 次に、**アクション** タブで、結果のリストから操作を選択します。
3. 新規ステップで、省略記号 (**...**) を選択し、次に **名前を変更する** を選択します。
4. ステップ **操作セットの実行** の名前を変更します。
5. **アクション名** フィールドで、**msdyn\_ExecuteOperationSetV1** を選択します。
6. **OperationSetId** フィールドに対して、**動的コンテンツ** ダイアログ ボックスで **msdyn\_CreateOperationSetV1Response OperationSetId** を選択します。

## <a name="references"></a>参照

- [Dataverse でフローを統合する方法の概要 - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する](schedule-api-preview.md)
- [クラウド フローの概要-Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [ソリューション対応フローの概要 - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
