---
title: プロジェクトの見積もりと実績の統合
description: このトピックは、プロジェクトの見積もりと実績に向けた Project Operations の二重書き込み統合に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955780"
---
# <a name="project-estimates-and-actuals-integration"></a>プロジェクトの見積もりと実績の統合

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、プロジェクトの見積もりと実績に向けた Project Operations の二重書き込み統合に関する情報を提供します。

## <a name="project-estimates"></a>プロジェクト見積もり

プロジェクトの人件費、経費、材料の見積もりは Microsoft Dataverse で作成、管理され、会計目的で Finance and Operations のアプリに同期されます。 Finance and Operations のアプリでは、作成、更新、削除の操作には対応していません。

見積もりを作成するには、プロジェクトの有効な会計の構成が必要です。 契約品目に関連付けられているプロジェクトには、プロジェクトのコストと収益のプロファイル ルールで定義された有効なプロジェクトのコストと収益のプロファイルが必要です。 詳細については、[請求可能なプロジェクトの会計を構成する](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules) を参照してください。

## <a name="labor-estimates"></a>労働力の見積もり

労働力の見積もりは、プロジェクト マネージャーまたはリソース マネージャーが作成します。これらのマネージャーは、一般的なリソースまたは名前付きリソースもプロジェクト タスクに割り当てます。 リソース割り当てレコードは、Dataverse の **リソースの割り当て** のタブにある **プロジェクトの詳細** のページで確認できます。 Dataverse のリソース割り当てレコードは、**時間見積もりに使用する Project Operations 統合エンティティ (msdyn\_resourceassignments)** を使って Finance and Operations のアプリの時間予測レコードを作成します。

   ![労働力の見積もりを統合する](./Media/DW4LaborEstimates.png)

二重書き込みでは、リソースの割り当てレコードをステージング テーブル (**ProjCDSEstimateHoursImport**) に同期させた後、ビジネス ロジックを使って時間予測レコード (**ProjForecastEmpl**) を作成、更新します。

プロジェクトの会計士は、Finance and Operations アプリで作成された予測時間の記録を次にアクセスして確認します: **プロジェクト管理と会計** > **すべてのプロジェクト** > **計画** > **時間予測**。

## <a name="expense-estimates"></a>経費の見積もり

経費の見積もりは、プロジェクト マネージャーがDataverse の **プロジェクトの詳細** ページの **経費の見積もり** タブで作成します。 経費の見積もり記録は、Dataverse の **見積もり明細** エンティティに保存されます。 これらの見積もりレコードは、トランザクション クラス **費用** を持ち、Finance and Operations アプリの経費予測レコードに **Project Operations の費用見積もりの統合エンティティ (msdyn\_estimatelines)** を使って同期されます。

   ![経費の見積もりを統合する](./Media/DW4ExpenseEstimates.png)

二重書き込みでは、経費の見積もりレコードをステージング テーブル (**ProjCDSEstimateExpenseImport**) に同期させた後、ビジネス ロジックを使って経費予測レコード (**ProjForecastCost**) を作成、更新します。 見積もり明細には、売上の見積もりと原価の見積もりレコードが別々に格納されます。 Finance and Operations アプリのビジネス ロジックは、ステージング テーブルのこの詳細を使用して、ひとつの経費予測レコードを生成します。

プロジェクトの会計士は、Finance and Operations アプリの経費予測レコードを次にアクセスして確認できます: **プロジェクト管理と会計** > **すべてのプロジェクト** > **計画** > **経費予測**。

## <a name="material-estimates"></a>材料の見積もり

材料の見積もりは、プロジェクト マネージャーがDataverse の **プロジェクトの詳細** ページの **材料の見積もり** タブで作成します。 材料の見積もり記録は、Dataverse の **見積もり明細** エンティティに保存されます。 これらの見積もりレコードは、トランザクション クラス **材料** を持ち、Finance and Operations アプリの品目予測レコードに **Project 統合テーブルの素材見積もりの統合エンティティ (msdyn\_estimatelines)** を使って同期されます。

   ![材料の見積もりを統合する](./Media/DW4MaterialEstimates.png)

二重書き込みでは、材料の見積もりレコードをステージング テーブル (**ProjForecastSalesImpor**) に同期させた後、ビジネス ロジックを使って品目予測レコード (**ForecastSales**) を作成、更新します。 見積もり明細には、売上の見積もりと原価の見積もりレコードが別々に格納されます。 Finance and Operations アプリのビジネス ロジックは、ステージング テーブルのこの詳細を使用して、ひとつの品目予測レコードを生成します。

プロジェクトの会計士は、Finance and Operations アプリの品目予測レコードを次にアクセスして確認できます: **プロジェクト管理と会計** > **すべてのプロジェクト** > **計画** > **品目予測**。

## <a name="project-actuals"></a>プロジェクトの実績

プロジェクトの実績は Dataverse で作成されます、これは、時間、費用、材料、請求活動に基づきます。 数量、原価、販売価格、プロジェクトなど、これらの取引のすべてのオペレーション属性がこの Dataverse エンティティに取り込まれます。 詳細については、[実績](../actuals/actuals-overview.md) を参照してください。 実際のレコードは、ダウンストリームの会計のための二重書き込みテーブルマップ **Project Operations 統合実績 (msdyn\_actuals)** を使用して Finance and Operations アプリに同期されます。

   ![実績の統合](./Media/DW4Actuals.png)

**Project Operations 統合の実績** テーブルマップは、属性 **同期のスキップ (内部使用のみ)** が **False** に設定されている Dataverse の **実績** エンティティからのすべてのレコードを同期させます。 この属性値は、レコード作成時に自動的に Dataverse に設定されます。 この属性が **True** に設定されている例:

  - 企業間取引のプロジェクトの原価実績。 詳しくは、[企業間取引を作成する](../project-accounting/create-intercompany-transactions.md)をご覧ください。 システムは企業間のベンダー請求書が転記されたときに、プロジェクトコストの実績を Finance and Operations アプリに再作成するため、これらのレコードはスキップされます。
  - 見積の請求書が確認されたときに作成された負の未請求販売レコードです。 Finance and Operations アプリのプロジェクト補助元帳が請求書発行時に未請求の売上レコードを反転させず、状態を完全請求に変更するため、これらのレコードはスキップされます。

二重書き込みのテーブル マッピングは、実績レコードをステージング テーブル (**ProjCDSActualsImport**) に同期します。 これらのレコードは、定期的なプロセスである  **ステージング テーブルからのインポート** によって、Project Operations の統合仕訳帳明細行やプロジェクト請求書提案明細を作成する際に処理されます。 詳細については、[Project Operations の統合仕訳帳](../project-accounting/project-operations-integration-journal.md)を参照してください。

また、Dataverseは **トランザクション接続** のエンティティにおけるプロジェクトの実際の取引との間のリンクを取得します。 詳細については、[実績を元のレコードにリンクする](../actuals/linkingactuals.md)を参照してください。 実際のトランザクション間のリンクも、二重書き込みのテーブルマッピング **プロジェクト取引の関係性の統合エンティティ (msdyn\_transactionconnections)** を使用して、Finance and Operations アプリに同期されます。 これらのレコードは、定期的なプロセスである **ステージング テーブルからのインポート** で使用され、Project Operations 統合仕訳明細行やプロジェクト請求書提案行を作成する際に使用されます。

Project Operations 統合仕訳帳とプロジェクト請求書の提案書を転記すると、ステージング テーブル **ProjCDSActualsImport** の各レコードが更新されます。 システムは、実績取引に対して以下の会計属性を取得して記録します:

- 会計通貨の金額
- 為替レート
- 伝票番号
- 消費税の金額

**Project Operations 統合実績** テーブル マッピングでは、この情報をもとにそれぞれの実績表を Dataverse に更新します。
