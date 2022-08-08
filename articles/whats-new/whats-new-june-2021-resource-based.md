---
title: 2021 年 6 月の新機能 - リソース/非在庫のシナリオ向け Project Operations
description: この記事は、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 6 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028252"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 6 月の新機能 - リソース/非在庫のシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます。

- Dynamics 365 Dataverse 環境バージョン 4.11.0.156 または 4.11.0.164 の Project Operations。
- 財務と運用アプリの環境バージョン 10.0.19 でのプロジェクト管理および会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- [調整シナリオのプロジェクト請求書提案ライン](../invoicing/correct-project-invoice-proposals.md)を削除する機能。
- 項目別の経費明細は、経費レポート: [再考された経費報告書-新機能](../expense/expense-reports-reimagined.md#new-features)のサブカテゴリ名を反映しています。
- 支払い方法は、新規支出を作成する際に、新規支出ペインに表示されます。
- プロジェクト スケジュール API の一般提供。 この新機能により、顧客はプロジェクト タスク、リソースの割り当て、タスクの依存関係、プロジェクト チーム メンバーのレコードに対して、プログラムによる作成、更新、削除の操作を行うことができます。 詳細については、[プロジェクト スケジュール API を使用して、スケジュール設定エンティティで操作を行う](../project-management/schedule-api-preview.md)を参照してください。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 

Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや財務と運用アプリ ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にする必要があります。 最新バージョンのマッピングが有効になっていない場合、一部の機能や性能が正しく動作しないことがあります。 マッピングのアクティブなバージョンは、**バージョン** 列の **二重書き込み** のページで確認できます。 **テーブル マッピングのバージョン** を選択し、最新のバージョンを選択してから、選択したバージョンを保存することで、新しいバージョンのマッピングを有効にすることができます。 既成のテーブル マッピングをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マッピングの起動に問題がある場合は、二重書き込みのトラブルシューティング: [マッピングでのテーブル列が見つからない場合](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)に記載の内容に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求と価格 | 2281417 | 請求書スケジュールによる請求書の自動作成アクションの失敗に関する問題を修正しました。 |
| 請求と価格 | 2287835 | 請求書確認のパフォーマンスが向上しました。 |
| 営業案件管理 | 2222555 | **プロジェクト見積もりからのインポート** を使用する際には、材料見積もりの請求額を見積明細の詳細に正しくコピーする必要があります。 |
| 営業案件管理 | 2223427 | **GenerateRetainersFromRetainerScheduleOptions** のアクションのカスタマイズが許可されるようになりました。 |
| 営業案件管理 | 2277528 | 複数の顧客とのプロジェクト契約明細の請求マイルストーン値の計算を修正しました。 |
| プロジェクトの計画と追跡 | 2226110 | **プロジェクト チーム** グリッドの **要件の生成** 機能で断続的に発生していた問題を修正しました。 |
| プロジェクトの計画と追跡 | 2208109 | ユーザーは、ある通貨でプロジェクトを作成すると、別の通貨で関連するタスクを作成することができない。 |
| プロジェクトの計画と追跡 | 2258228 | スケジュール API を使って **スケジュール** エンティティで変更できるフィールドのリストが更新されました。 |
| プロジェクトの計画と追跡 | 2293989 | **プロジェクト タスク** グリッドには、正しい言語と地域の設定をに渡す必要があります。 |
| リソース管理 | 2220493 | リソース要求が完了したことを迅速に示せるよう、**タスク** グリッドのユーザー エクスペリエンスが修正されました。 |
| リソース管理 | 2330496 | **スケジュール ボード** の読み込みの問題を修正しました。 (品質の更新はバージョン 4.11.0.164 で利用可能です) |
| 時間と経費 | 2194431 | **時間入力** グリッドは、**システム設定** で設定されているように週の始まりに忠実である必要があります。 |
| 時間と経費 | 2277311 | **時間入力** グリッドのセルの値を削除した後、カーソルがグリッド内に残留します。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| プロジェクト管理および会計 | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | Project Operations と統合されている Finance の法人の **プロジェクト管理設定** では、**フォーム ノート** と **フォームの設定** が表示されない。 |
| プロジェクト管理および会計 | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | プロジェクトの請求書伝票の **転記タイプ** = **消費税** では、VAT の既定の説明が空白になっている。 |
| プロジェクト管理および会計 | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | タスクベースの請求書を Dataverse と Project Operations の統合で使用すると、二重のトランザクションが計上される。 |
| プロジェクト管理および会計 | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Project Operations の統合を使用している間、収益認識の完了率が正しくならない。 |
| プロジェクト管理および会計 | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Project Operations の統合シナリオで、保留中のベンダーの請求書に対して収益の発生が 2 倍になっている。 |
| プロジェクト管理および会計 | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | 収益プロファイルのルールが **グループ** 設定に設定されている場合、統合ジャーナルを転記できない。 |
| プロジェクト管理および会計 | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | 複数の単位を含む明細行があるプロジェクトの注文書に対して、購入請求書を計上できない。 |
| プロジェクト管理および会計 | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | プロジェクトの既定の財務財務コードが、プロジェクト **V2** データ エンティティを使用して更新できない。 |
| プロジェクト管理および会計 | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | プロジェクトの見積もりを作成するバッチ処理に時間がかかりすぎる。 |
| プロジェクト管理および会計 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 契約を削除すると、顧客に関連するアドレスも削除される。 |
| 出張と経費 | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | 経費報告書の承認ワークフローの条件が正しく評価されない。 |
| 出張と経費 | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | 経費報告書のポリシーで、プロジェクト ID が正しく評価されない。 |
| 出張と経費 | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | **会社間経費取引のための個人への分割** のアクションが正しく機能しない。 |
| 出張と経費 | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | 特定の出張依頼を削除すると、経費報告書の明細行の正当化が誤って削除される。 これは経費報告書の RecID と出張依頼書の RecID が同じ場合に発生します。 |
| 出張と経費 | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | 経費のモバイルアプリで、経費報告書のポリシーに **プロジェクト ID** フィールドが必要な場合に問題が発生する。 |
| 出張と経費 | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | プロジェクトに関連した会社間の経費が編集できない。 代わりに、「オブジェクト参照がオブジェクトのインスタンスに設定されていません」というエラーメッセージが表示される。 |
| 出張と経費 | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | 経費報告書が計上された後、銀行の補助元帳に誤った通貨と金額が記載さる。 |
| 出張と経費 | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | *クレジットカード取引の削除* の機能が改善されました。  |
| 出張と経費 | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | 法人で異なる報告通貨書が指定されている場合、経費報告書に含まれる消費税が一貫して計算されない。 |
| 出張と経費 | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | 新しい現金の旅費を追加すると、パフォーマンスに影響が出る。 |
| 出張と経費 | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | 経費報告書で、経費ポリシーのルールが適用されない。 |
| 出張と経費 | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | データ管理フレームワークを使って新しい共有カテゴリーをアップロードすると、すべての共有カテゴリーのサブ カテゴリーが削除される。 |
| 出張と経費 | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | 経費明細を作成してからカテゴリを選択すると、「消費税グループDOMと消費税グループSTDの組み合わせは無効です」というエラーメッセージが表示される。 |
| 出張と経費 | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | 経費のモバイル アプリケーションに同期の問題が発生する。 |
