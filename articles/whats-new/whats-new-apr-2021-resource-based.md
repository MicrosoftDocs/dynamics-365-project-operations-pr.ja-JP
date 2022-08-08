---
title: 2021 年 4 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 4 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 490b7aa38bfdfbcdce21a21e582296e4ce15aeeb
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029260"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 4 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます。

- Dataverse 環境バージョン 4.9.0.221 での Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.17 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- プロジェクト用の非在庫材料。 主要機能には次のようなものがあります。
  - プロジェクトの販売サイクル中の非在庫材料の見積もりと価格設定。 詳細については、[カタログ製品の原価率と販売率を設定する (ライト)](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md)を参照してください。
  - プロジェクトの実施中に非在庫材料の使用を追跡します。 詳細については、[プロジェクトおよびプロジェクト タスクでの材料用途を記録する](../material/material-usage-log.md)を参照してください。
  - 使用済みの非在庫材料原価の請求。 詳細については、[請求バックログの管理](../proforma-invoicing/manage-billing-backlog.md)を参照してください。
  - この機能の構成方法については、[在庫のない品目と保留中のベンダー請求書を構成する](../procurement/configure-materials-nonstocked.md) を参照してください
- タスクベースの請求: プロジェクト タスクをプロジェクト契約品目に関連付ける機能が追加されました。これにより、プロジェクト タスクに、契約品目と同じ請求方法、請求頻度、および顧客が適用されます。 この関連付けにより、プロジェクト タスクでこの設定に従って、正確な請求、会計、収益の見積もり、および認識が徹底されます。
- Dynamics 365 Dataverse の新しい API では、**スケジューリング エンティティ** を使った操作の作成、行進、削除が可能です。 詳細については、[スケジュール API を使用して、スケジューリング エンティティで操作を実行する](../project-management/schedule-api-preview.md)を参照してください。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

次のリストは、Project Operations 2021 年 4 月リリースで変更または追加された二重書き込みのマッピングです。

| **エンティティ マップ** | **更新バージョン** | **コメント** |
| --- | --- | --- |
| Project Operations 統合実績 (msdyn\_actuals) | 1.0.0.14 | 材料プロジェクトの実績を同期するよう、マッピングが変更されました。 |
| Project Operations の費用見積もりの統合エンティティ (msdyn\_estimateslines) | 1.0.0.2 | タスクベースの請求をサポートするため、プロジェクト契約品目の同期を財務と運用アプリに追加しました。 |
| 時間見積もりに使用する Project Operations 統合エンティティ (msdyn\_resourceassignments) | 1.0.0.5 | タスクベースの請求をサポートするため、プロジェクト契約品目の同期を財務と運用アプリに追加しました。 |
| Project Operations の統合テーブルによる材料の見積もり (msdyn\_estimatelines) | 1.0.0.0 | 材料の見積もりを Dataverse から財務と運用アプリに同期する新しいテーブル マップ。 |
| Project Operations 統合プロジェクト ベンダー請求書のエクスポート エンティティ (msdyn\_projectvendorinvoices) | 1.0.0.0 | 仕入先請求書のヘッダーを財務と運用アプリから Dataverse に同期する新しいテーブル マップ。 |
| Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | 仕入先請求書行を財務と運用アプリから Dataverse に同期する新しいテーブル マップ。 |

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや財務と運用ソリューション バージョンを更新する際に、関連するすべてのテーブル マッピングを有効にする必要があります。 最新バージョンのマッピングが有効になっていない場合、一部の機能や性能が正しく動作しないことがあります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 **テーブル マッピングのバージョン** を選択し、最新のバージョンを選択した後で、選択したバージョンを保存することで、マッピングの新しいバージョンを有効にすることができます。 既成のテーブル マッピングをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの起動に問題がある場合は、「二重書き込みのトラブルシューティング」の [マッピング上にテーブルの列が表示されない問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) のセクションを参照してください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-in-dynamics-365-dataverse"></a>Dynamics 365 Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求および価格設定 | 2124532 | 元の請求書に着手金額または適用された着手金額が存在する場合、**請求書の修正** ボタンが見積もり請求書に表示されます。 このボタンは、Finance バージョン 10.0.19 以降の環境でのみ表示されます。 |
| 請求および価格設定 | 2224568 | 請求書確認プラグインの呼び出しを含むカスタマイズを可能にするロジックが追加されました。 |
| 請求および価格設定 | 2101098 | 既定フィールドのロジックを見積もり請求に改善しました: **請求先住所**、**請求先氏名**、および **支払い条件** が、対応するプロジェクト契約の顧客レコードからの既定値となりました。 |
| 請求および価格設定 | 2021413 | **タスク** エンティティの **実際のコスト** と **売上** フィールドが更新され、タスクの未請求および請求済みの経費からの売上値が含まれるようになりました。 |
| 請求および価格設定 | 2182110 | プロジェクト契約をコピーするとき、契約品目 ID は、それが一意であることを保証するために、コピー先プロジェクト契約で再生成されます。 |
| 営業案件管理 | 2186741 | **発生元** フィールドと **トランザクション タイプ** を確認するために追加された検証は、既存の見積もり行の詳細で更新できません。 |
| 営業案件管理 | 2191353 | マイルストーンは、時間と材料の契約品目で作成してはなりません。 |
| 営業案件管理 | 2216956 | **価格の更新** の問題を修正しました。 |
| 計画と追跡 | 2182979 | プロジェクト コピー機能が改善され、経費見積もり行が元のプロジェクトから確実にコピーされるようになりました。 |
| 計画と追跡 | 2184144 | プロジェクト コピー機能が改善され、リソース位置名が元のプロジェクトから確実にコピーされるようになりました。 |
| 計画と追跡 | 2184799 | プロジェクトのコピー: コピーの進行中に推定開始日を変更できないように、制御を強化しました。 |
| 計画と追跡 | 2185134 | プロジェクトのコピー: コピー先プロジェクトの推定開始日は、今日の日付に設定されます。 |
| 計画と追跡 | 2196373 | プロジェクトのコピー: プロジェクト マネージャーとチーム メンバーのレコードがプロジェクト チームで重複していないことを確認します。 |
| 計画と追跡 | 2211833 | プロジェクトのコピー: リソースの割り当ては、ソース プロジェクト タスクからコピー先プロジェクトにコピーされます。 |
| 計画と追跡 | 2186541 | リソース別にグループ化する場合の **見積り** グリッドの問題を修正しました。 |
| 計画と追跡 | 2166906 | タスクのトランザクション カテゴリを **リソースの割り当て** エンティティにコピーする必要があります。 |
| リソース管理 | 2125362 | 時間ベースの割り当て方法を使用して一般的なチーム メンバーを作成する際の問題を修正しました。 |
| 時間と経費 | 2113603 | **時間入力** ページから属性を削除する際のカスタマイズ関連の問題を修正しました。 システムは、スクリプトを使用して属性にアクセスする前に、属性がページに存在するかどうかを確認するようになりました。 |
| 時間と経費 | 2204377 | 時間入力中に **週のコピー** を選択すると、コピーされたタイムシートが自動的に表示されます。 |
| 時間と経費 | 2209059 | **ステータス** フィールドを、Dynamics 365 Field Service 時間入力向けに編集できます。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| プロジェクト管理および会計 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | **定期** セクションで、逆見積を除去する機能が動作しません。  |
| プロジェクト管理および会計 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **会計調整** 機能は、**手動入力を許可しない** が選択された元帳勘定では問題が発生します。 |
| プロジェクト管理および会計 | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | 着手金額または適用された着手金額を含む修正請求書を処理するためのビジネス ロジックが追加されました。 |
| プロジェクト管理および会計 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 仕掛品 - 会社間プロジェクトで請求書に売上高を転記すると、予期しない取引先企業が選択されます。 |
| プロジェクト管理および会計 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations で着手金額を使用する場合、前払いの請求後に契約の既定プロジェクトを変更すると、控除額に問題が発生します。 |
| プロジェクト管理および会計 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations では、必要に応じて契約からプロジェクトを削除すると、契約の既定プロジェクトがリセットされます。 |
| プロジェクト管理および会計 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations では、会社間請求書の **行を追加** リストに間違った経費明細行が表示されます。 |
| プロジェクト管理および会計 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations では、Project Operations と統合されている Finance 法人で **購入契約** ページが表示されません。 |
| プロジェクト管理および会計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse 統合エラーが原因で、Project Operations で見積もりを成約に変換できません。 |
| プロジェクト管理および会計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** は、別の顧客からの資金調達ソースの請求書住所を設定できます。  |
| プロジェクト管理および会計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Project Operations では、トランザクションの転記請求書を作成するときにディメンションが選択されません。 |
| 出張と経費 | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 承認されて行ごとに転記された場合、経費報告書の現金前払い残高は更新されません。 |
| 出張と経費 | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | 項目別の会社間経費報告書の税金が正しく計算されていません。 |
| 出張と経費 | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | プロジェクトに関連する追加のフィールドは、刷新された **会社間経費報告** ページに表示されます。 |
| 出張と経費 | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | 経費報告書のヘッダー領収書に誤ったエラー メッセージが表示されます。 |
| 出張と経費 | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | 売上税が転記先の法人に転記されている場合、会社間シナリオで経費報告書が誤って転記されます。 |
| 出張と経費 | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | レポート送信日が、承認された経費報告書に印刷されません。 |
| 出張と経費 | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | **承認日** と **拒否日** フィールドは、経費が承認された後に自動入力されません。 |
| 出張と経費 | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | ある労働者用に作成された出張依頼書は、別の労働者の経費報告書に使用できます。 |
| 出張と経費 | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 新しい経費明細を追加する際、経費カテゴリがロックされています。 |
| 出張と経費 | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | すでに分割された経費報告書の行を明細化すると、買掛金\総勘定元帳の伝票の転記が不完全になり、**TRVEXPTRANS.SOURCEDOCUMENTLINE** が重複しているため、会計ソース エクスプローラーが破損します。 |
| 出張と経費 | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | 出張費要求ポリシーが想定どおりに機能しません。 |
| 出張と経費 | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | 仕入先勘定名は、経費報告書に対して転記されたプロジェクト トランザクションには表示されません。 |
| 出張と経費 | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operations では、会社間プロジェクトのタスクで時間を承認することはできません。 |
| 出張と経費 | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | 現金前払い返金カテゴリは、転記時に現金前払い残高を更新しません。 |
| 出張と経費 | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | インポートされたクレジット カード トランザクションを使用して外貨で作成され、プロジェクトに関連付けられている経費報告書では、販売価格が正しく計算されていません。 |
| 出張と経費 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | **TrvRequisitionLine** データ エンティティと関連する一意のインデックスをロールバックしました。 |
| 出張と経費 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | **SOURCEDOCUMENTLINE** 世代ににインストルメンテーションを追加しました。 |
| 出張と経費 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 売上税が転記先の法人に転記されている場合、会社間シナリオで正しくない補助元帳仕訳が表示されます。 |
| 出張と経費 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations では、Dataverse から経費見積もりを削除しても、Finance から削除されません。 |
| 出張と経費 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 経費カテゴリが非プロジェクト カテゴリの場合、**経費** ページで選択された財務ディメンションは経費報告書にコピーされません。 |
