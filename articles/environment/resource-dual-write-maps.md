---
title: Project Operations 二重書き込みマッピングのバージョン
description: このトピックは、Dynamics 365 Project Operations に必要となる二重書き込みのマッピングのリストを提供します。
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939004"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations 二重書き込みマッピングのバージョン

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

リソース/非ストックのシナリオに Dynamics 365 Project Operations を使用するには、環境内で二重書き込みマッピングマのセットを実行する必要があります。 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>マッピングの前提条件 : 二重書き込みオーケストレーション ソリューション

次のマッピングは、Project Operations ソリューションに必要となる前提条件です。 次の表にリストされているマッピングと、ご使用の環境で関連するテーブル マッピングを必ず実行してください。

| テーブル マップ | 初期同期 |
| --- | --- |
| 元帳 (msdyn_ledgers) | テーブル マッピングとすべての前提条件の初期同期が必要です。 初期同期のマスターは Finance and Operations アプリです。 |
| 法人 (cdm_companies) | 必須ではありません。 二重書き込みを使用して環境がリンクされると、システムはこのエンティティに自動的にデータを入力します。 |
| 顧客 V3 (accounts) | プロビジョニングには必須ではありません。 |
| ベンダー V2 (msdyn_vendors) | プロビジョニングには必須ではありません。 |

1. マップのリストから、すべての前提条件を満たす元帳 **(msdyn\_ledgers)** マッピングを選択し、**初期同期** チェック ボックスをオンにします。 **初期同期のマスター** フィールドで、**Finance and Operationsアプリ** 元帳マッピングとすべての前提条件マップの両方を選択します。 **実行** を選択します。

![元帳マップの同期](media/DW6.png)

1. 上の表に記載されている残りのすべてのテーブル マッピングについても、同じ手順に従います。 これらのマッピングを実行する際には、**初期同期** のチェック ボックスを選択しないでください。

## <a name="project-operations-dual-write-maps"></a>Project Operations の二重書き込みのマッピング

次のマッピングは、Project Operations ソリューションに必要となる前提条件です。

| **エンティティ マップ** | **最新バージョン** | **初期同期** |
| --- | --- | --- |
| プロジェクト トランザクションの関連付けにおける統合エンティティ (msdyn\_transactionconnections) | 1.0.0.0 | プロビジョニングには必須ではありません。 |
| プロジェクトの契約ヘッダー (受注) | 1.0.0.1 | プロビジョニングには必須ではありません。 |
| プロジェクト 契約品目 (salesorderdetails) | 1.0.0.0 | プロビジョニングには必須ではありません。 |
| プロジェクトの資金源 (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | プロビジョニングには必須ではありません。 |
| Project Operations の統合テーブルによる材料の見積もり (msdyn\_estimatelines) | 1.0.0.0 | プロビジョニングには必須ではありません。 |
| プロジェクトの仮発行請求書 V2 (invoices) | 1.0.0.2 | プロビジョニングには必須ではありません。 |
| Project Operations 統合実績 (msdyn_actuals) | 1.0.0.14 | プロビジョニングには必須ではありません。 |
| Project Operations 統合契約品目のマイルストーン (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | プロビジョニングには必須ではありません。 |
| 経費見積もりに使用する Project Operations 統合エンティティ (msdyn_estimateslines) | 1.0.0.2 | プロビジョニングには必須ではありません。 |
| 時間見積もりに使用する Project Operations 統合エンティティ (msdyn_resourceassignments) | 1.0.0.5 | プロビジョニングには必須ではありません。 |
| Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn_expensecategories) | 1.0.0.2 | プロビジョニングには必須ではありません。 |
| Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn_expenses) | 1.0.0.2 | プロビジョニングには必須ではありません。 |
| Project Operations 統合プロジェクト ベンダー請求書のエクスポート エンティティ (msdyn_projectvendorinvoices) | 1.0.0.0 | プロビジョニングには必須ではありません。 |
| Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ (msdyn_projectvendorinvoicelines) | 1.0.0.0 | プロビジョニングには必須ではありません。 |
| すべての会社のプロジェクトのリソース ロール (bookableresourcecategories) | 1.0.0.1 | プロビジョニング時に Dynamics 365 Dataverse 環境に入力されるプロジェクト マネージャーとチーム メンバーのリソース ロールを同期するためには、テーブル マッピングの初期同期が必要です。 Dataverse は、初期の同期のための主要なソースです。 |
| プロジェクト タスク (msdyn_projecttasks) | 1.0.0.4 | プロビジョニングには必須ではありません。 |
| プロジェクト トランザクション カテゴリ (msdyn_transactioncategories) | 1.0.0.0 | プロビジョニングには必須ではありません。 |
| プロジェクト V2 (msdyn_projects) | 1.0.0.1 | プロビジョニングには必須ではありません。 |

リストされたマッピングを実行するには、次の手順を実行します。

1. **all companies (bookableresourcecategories)** テーブル マッピングのプロジェクト リソース ロールを有効にします。**初期同期のマスター** フィールドで **Common data service** を選択します。 

 ![リソース ロールテーブル マッピングの同期](media/6ResourceInitialSync.jpg)

 マッピングの状態が **実行中** になるまで待機してから次のステップに進みます。

2. 残りの必要なマッピングをすべて選択します。 二重書き込みマッピングのリストでは、右上の検索でキーワード、**プロジェクト** を使ってフィルタリングすることができます。 すべてのマッピングを複数選択して実行できます。 詳細については、[複数のテーブル マッピングを管理する](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps)を参照してください。 関連するエンティティ マッピングも有効にして実行してください。

### <a name="project-operations-dual-write-map-versions"></a>Project Operations 二重書き込みマッピングのバージョン

ご利用の環境では、常に最新バージョンのマッピングを実行してください。 以下の条件に当てはまる場合、一部の機能が正しく動作しない場合があります。

- マッピングがアクティブ化されていません。
- マッピングの最新バージョンがアクティブ化されていません。 
- 関連するテーブル マッピングがアクティブ化されていません。

マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 **テーブル マッピングのバージョン** を選択し、最新のバージョンを選択した後で、選択したバージョンを保存することで、マッピングの新しいバージョンを有効にすることができます。 既成のテーブル マッピングをカスタマイズした場合は、変更を再適用する必要があります。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。