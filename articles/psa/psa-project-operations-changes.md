---
title: Project Service Automation から Project Operations への機能変更
description: このトピックでは、Project Service Automation から Dynamics 365 Project Operations への機能変更の概要について説明します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595412"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Project Service Automation から Project Operations への機能変更

Dynamics 365 Project Service Automation から Dynamics 365 Project Operations Lite へのアップグレードは、3 つのフェーズで行われます。 このトピックでは、アップグレードの完了時に期待できる主な変更について説明します。

| アップグレードの出荷 | フェーズ 1 <br>(2022 年 1 月) | フェーズ 2 <br>(2022 年 4 月のサイクル) | フェーズ 3  |
|------------------|------------------------|---------------------------|---------------------------|
| プロジェクトの作業分解構造 (WBS) に依存しません。 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBSは、現在サポートされている Project Operations の制限に含まれています。 | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client のサポートを含む、現在サポートされている Project Operations の制限外の WBS。 | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>プロジェクト管理

ユーザー エクスペリエンスの最も重要な変更は、プロジェクト計画の領域になります。 Project Operations では、[Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) によって提供されるスケジュール機能を活用することにより、作業分解構造 (WBS) を管理するための新しい最新のエクスペリエンスを採用しています。

## <a name="differences-in-the-scheduling-experience"></a>スケジュール エクスペリエンスの違い

次の表は、Project Service Automation と Project Operations のスケジュールの違いをまとめたものです。

|  スケジューリング     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| プロジェクト テンプレート - プロジェクトの作成時にプロジェクト テンプレートを定義および適用する機能  |  &nbsp;    | :heavy_check_mark: |
| プロジェクト作業分解構造 (WBS) とデスクトップ クライアントの統合   |    &nbsp;  | :heavy_check_mark: |
| 制約 - 以後に開始、以後に終了  | :heavy_check_mark: |   &nbsp;  |
| マイルストーン - 期間がゼロのタスク   | :heavy_check_mark:  |  &nbsp;  |
| リソース主導タスクでは、割り当てられたリソースの利用状況を考慮する   | :heavy_check_mark: |  &nbsp;    |
| 時間フェーズ編集 - 計画を編集し、日単位で作業する   |   &nbsp;  | :heavy_check_mark: |
| 自動/手動スケジュール - プロジェクト スケジュール エンジンを使用して、タスクを自動または手動でスケジュールする |  &nbsp; | :heavy_check_mark:  |
| ユーザー インターフェイスで大規模なプロジェクトを直接編集: 編集可能な計画のサイズに制限はありません  | 500 タスクの制限  | :heavy_check_mark:       |
| 完了率 - タスクの進行状況をマークする   | :heavy_check_mark:  |  &nbsp;  |
| [プロジェクト スケジュール モード](../project-management/scheduling-modes.md) - プロジェクトを固定単位、固定工数、または固定期間として定義する | :heavy_check_mark: | &nbsp; |
| タイムライン - タイムライン ビューを作成およびカスタマイズして、スケジュールの詳細を視覚化し、関係者と通信する。 | :heavy_check_mark:  | &nbsp; |
| 工数主導のタスク - 工数主導としてタスクをスケジュールするためのスケジュール エンジン サポート  | :heavy_check_mark:  | &nbsp; |
| **タスク情報** ダイアログ ボックス - ダイアログ ボックスを使用してタスクの詳細を保存する | :heavy_check_mark:  |  &nbsp;  |
| ドラッグ アンド ドロップ - タスクを複数選択し、WBS 上の位置を変更する | :heavy_check_mark: | &nbsp;  |
| 柔軟な永続ビュー - タスク属性のより詳細なビューを定義する   | :heavy_check_mark:  | &nbsp; |
| WBS の並べ替えとフィルター  | :heavy_check_mark:  | &nbsp; |
| ウォーターフォール以外のプロジェクト デリバリー用のボード ビュー  | :heavy_check_mark:   | &nbsp; |
| タイムライン ビュー - WBSの視覚化と編集に使用される対話型ガント チャート   | :heavy_check_mark:  | &nbsp; |
| キーボード ショートカット - インデントや挿入などの一般的な操作にキーボード ショートカットを使用する  | :heavy_check_mark:  |  &nbsp; |
| 複数レベルの元に戻す - what-if 分析を実行して、一連の操作全体を元に戻して再適用することにより、変更の影響を完全に把握する | :heavy_check_mark: | &nbsp; |
| 切り取り/コピー/貼り付け - アプリケーション間でスケジュールの詳細をコピーして貼り付けることにより、スケジュール開発で共同作業する  | :heavy_check_mark: | &nbsp; |
| タスク チェックリスト - 最大 20 個のチェックリスト項目をタスクに追加する   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>プロジェクト計画

Project Operations の **プロジェクト** ページには、Project Service Automation の **プロジェクト** ページと比べてかなりの数の違いがあります。

次のアクションは、フェーズ 1 アップグレードの一部として **プロジェクト** ページから削除されました:

  - **MS Project で開く**
  - **テンプレートの作成**
  - **MS Project からリンク解除する**

Project Operations の **プロジェクト** ページには、次の新しいタブが含まれています。

- **材料の見積もり**
- **タスクの請求の設定**

**ステータス** タブが削除され、**ステータス** フィールドがプロジェクトのスケジュール モードの **概要** タブに表示されるようになりました。

   ![プロジェクト ページを更新します。](media/projectform.png)

**スケジュール** タブは **タスク** タブに名称変更され、Project for the Web による新しいプロジェクト計画エクスペリエンスを提供します。

   ![新しいプロジェクト タスク タブ。](media/tasktab.png)

## <a name="scheduling-modes"></a>スケジュール モード

Project Operations は、新しい機能 [スケジュール モード](../project-management/scheduling-modes.md) を導入しました。 既存のすべての Project Service Automation プロジェクトは、デフォルトで Project Operations の **固定期間** に設定されます。 ただし、新しいプロジェクトのデフォルトは、**設定** > **パラメーター** > **パラメーター** > **スケジュール モード** に移動することで管理できます。

   ![スケジュール モードのプロジェクト パラメーター設定。](media/projectparameter.png)

## <a name="project-planning-limits"></a>プロジェクト計画の制限

Project Operations は、すべてのプロジェクト スケジュール操作を Project for the Web に依存しています。 Project for the Web は、次の表の制限を使用して WBS (作業分解構造) を管理します。

| **フィールド**                                          | **限度**             |
|----------------------------------------------------|-----------------------|
| プロジェクトの最大合計タスク                  | 500                   |
| プロジェクトの最大合計期間               | 3650 日 (10 年)  |
| プロジェクトの最大総リソース              | 300                   |
| プロジェクトの最大総リンク数 (後継のみ) | 600                   |
| 1 つのプロジェクトにおけるカスタム フィールドの最大合計数          | 10                    |
| 最大階層レベル                            | 10 レベル             |
| 最大リンク数 (後続 + 先行)            | 20                    |
| リーフ タスクの最大期間                      | 1250 日             |
| サマリー タスクの最大期間                 | 3650 日 (10 年)  |
| タスクに割り当てられる最大リソース               | 20 リソース          |
| タスクでサポートされている日付範囲                    | 2000/1/1 - 2149/12/31 |
| チェックリスト項目                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>プロジェクト計画の拡張と開発

Project Operations にアップグレード後、プロジェクト スケジュール API を使用して、次のエンティティで作成、更新、および削除の操作を実行する必要があります:

|   Entity name           |   エンティティの論理名       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| プロジェクト タスク            | msdyn_projecttask           |
| プロジェクト タスクの依存関係 | msdyn_projecttaskdependency |
| リソース割り当て     | msdyn_resourceassignment    |
| プロジェクト バケット          | msdyn_projectbucket         |
| プロジェクト チーム メンバー     | msdyn_projectteam           |

現在、これらのエンティティを含むカスタマイズがある場合は、実装ガイダンスの [プロジェクト スケジュール API を使用して、スケジュール設定エンティティで操作を行う](../project-management/schedule-api-preview.md) を参照してください。

## <a name="data-model-changes"></a>データ モデルの変更

アップグレード フェーズ 1 の一環として、データ モデルに変更があります。 これらの変更は、主に既存エンティティに対するフィールドの変更です。 フェーズ 1 では、エンティティ、**msydn_project** と **msdyn_projectteam** はカスタマイズのリファクタリングです。 

> [!IMPORTANT]
> このセクションは、今後のアップグレード フェーズが完了すると、追加エンティティで更新されます。

次のフィールドは新しいフィールドに置き換えられました。

|   Entity          |   旧論理名   |   新論理名    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

次のフィールドが追加されました。

|   Entity          |   論理名                               |   説明設定 |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | プロジェクトの手数料売上実績を集計して表示します。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_actualmaterialcost                     | プロジェクトの材料コスト実績を集計して表示します。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_actualmaterialsales                    | プロジェクトの材料売上実績を集計して表示します。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | このプロジェクトに関連付けられた契約品目。 |
| msdyn_project     | msdyn_copyprojectcorrelationid               | これは内部システム フィールドで、関連付け識別子に関連する **プロジェクトのコピー** に使用されます。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_copyprojectsessionid                   | これは内部システム フィールドで、セッション識別子に関連する **プロジェクトのコピー** に使用されます。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_globalrevisiontoken                    | プロジェクト スケジュール サービスからの最終同期 xRM グローバル リビジョン トークン。 |
| msdyn_project     | msdyn_msprojectdocument                      | プロジェクトに属する Microsoft Project ドキュメント。 |
| msdyn_project     | msdyn_plannedmaterialcost                    | プロジェクトの材料コスト計画の集計。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_plannedmaterialsales                   | プロジェクトの材料売上計画の集計。 Project Service Automation でのみ使用可能。 |
| msdyn_project     | msdyn_program                                | このプロジェクトが関連付けられているプログラムです。 |
| msdyn_project     | msdyn_quotelineproject                       | このプロジェクトに関連付けられた見積依頼明細行。 |
| msdyn_project     | msdyn_replaylogheader                        | 再生ログのヘッダー。 |
| msdyn_project     | msdyn_schedulemode                           | プロジェクトのすべてのタスクに使用する既定のスケジュール モード。  |
| msdyn_project     | msdyn_taskearlieststart                      | プロジェクト内のすべてのタスクの最も早い開始日です。  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | このプロジェクト チーム メンバーのコピー元であるプロジェクト チーム メンバー。 |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | 新しく作成された汎用チーム メンバーのリソース要件を作成するかどうかを指定します。  |
| msdyn_projectteam | msdyn_deletestatus                           | プロジェクト スケジュール サービスに削除要求が送信されたかどうか、および想定される時間枠内で応答が正常に返信されたかどうかを追跡するためのチーム メンバーの削除状態。 |
| msdyn_projectteam | msdyn_effortcompleted                        | 割り当てに対してチーム メンバーが達成した工数を追跡します。 |
| msdyn_projectteam | msdyn_effortremaining                        | 割り当てに対してチーム メンバーがまだ完了していない工数を追跡します。 |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | チーム メンバーがプロジェクト スケジュール サービスに削除要求を送信してから、チーム メンバーが Microsoft Dataverse で実際に削除されるまでの待機期間。|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | チーム メンバーの削除要求がプロジェクト スケジュール サービスに送信されたときに記録されるタイムスタンプ。 |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | このプロジェクト チーム メンバーのコピー元であるプロジェクト チーム メンバーを表示します。  |

## <a name="project-templates"></a>プロジェクト テンプレート

Project Operations は、プロジェクト テンプレートをサポートしていません。 ただし、[プロジェクト コピー API](../project-management/dev-copy-project.md) を使用してコア機能の多くを複製することができます。

## <a name="desktop-add-in-support"></a>デスクトップ アドインのサポート

Microsoft Project Desktop アドインのサポートは、アップグレードの最初の 2 つのフェーズでは利用できません。 フェーズ 3 で、現在サポートされている Project for the Web の制限を超えるプロジェクトをお持ちのお客様は、デスクトップ アドインを使用できるようになります。

## <a name="editing-resource-assignment-contours"></a>リソース割り当て配分型の編集

リソース割り当て配分型を編集する機能は、アップグレードのフェーズ 2 が利用可能になったときに利用できます。

## <a name="billing-and-pricing"></a>請求および価格設定

Project Operations に次の新機能が追加されました。 これらの機能は本質的に付加的であり、Project Service Automation データ モデルに影響を与えません。

- [プロジェクトやプロジェクトのタスクにおける資材の使用状況の記録](../material/material-usage-log.md)
- [外注管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [前払いおよび着手金ベースの契約](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [上限と検証へのコンタクト](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [タスクベースの請求](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>非推奨のコンポーネント

次の表に、アップグレード後に非推奨コンポーネント ソリューションに移動されるすべての非推奨フィールドを示します。 詳細およびソリューションへのリンクについては、[Dynamics 365 Project Service Automation 3x から Project Operations 4x への非推奨コンポーネント](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution) を参照してください。

### <a name="invoicedetail"></a>invoicedetail

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| フィールド                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

