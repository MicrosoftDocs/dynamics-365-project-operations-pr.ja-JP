---
title: 2021 年 11 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックは、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 11 月リリースで利用可能な品質更新に関する情報を提供します。
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942891"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 11 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

*適用対象: リソース/非在庫ベースのシナリオ向け Project Operations*

このトピックは、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます:

- Dataverse 環境のバージョン 4.26.0.145、4.26.0.148、4.26.0.150、4.26.0.155 の Project Operations
- Dynamics 365 Finance 環境でのプロジェクト管理と会計 バージョン 10.0.22

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- プロジェクト スケジューリング アプリケーション プログラミング インターフェイス (API) は、プロジェクト バケットを作成および削除する機能をサポートするようになりました。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](/dynamics365/project-operations/environment/resource-dual-write-maps)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-in-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求と価格 | 2240080 | **支払い条件** フィールドは、見積もり送り状で複製してはなりません。 |
| 請求と価格 | 2358236 | 請求書の修正では、ゼロ価格の行がある修正を許可する必要がある。 |
| リソース管理 | 2410072 | プロジェクト マネージャーとしてタスクに割り当てられたリソースのセットアップができるようになる。 |
| 請求と価格 | 2430234 | コスト パフォーマンス計算の問題を修正。 |
| 時間と経費 | 2436978 | hh:mm 形式で時間を入力できるようになる。 |
| 請求と価格 | 2448623 | 価格表が組織単位に関連付けられた後に更新できるようになる。 |
| 時間と経費 | 2460396 | セルをクリアして、時間エントリを削除できるようになる。 |
| 請求と価格 | 2467386 | タスクが落札見積もりに関連付けられている場合でも、タスクのあるプロジェクトを削除できるようになる。 |
| 時間と経費 | 2461744 | **失敗した承認** ビューには、**提出済み** ステージのプロジェクト承認のみが含まれる。 |
| 時間と経費 | 2464082 | 対象ステータスが一致したら、プロジェクト承認から承認セットへのリンクを削除する。 |
| 時間と経費 | 2468108 | スケジュール ジョブは承認セットの **処理** ステータスを設定すべきではない。 |
| 時間と経費 | 2471503 | 7 日経過した承認セットを削除する。 |
| 請求と価格 | 2480687 | 見積もり明細のマイルストーンを作成するときに、見積もり明細の参照を削除すべきではない。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| プロジェクト管理および会計 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | プロジェクト費用トランザクションで保持されているベンダーの金額は、トランザクション リストに表示されない。 |
| プロジェクト管理および会計 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | ベンダー請求書の統合がオンになっていると、企業間のベンダー請求書が破損する。 |
| プロジェクト管理および会計 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | プロジェクトの請求書に記載されている支払条件が、期待通りに機能しない。 |
| プロジェクト管理および会計 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | ベンダーの保持が解除されると、伝票の計上に不正確な追加行が発生する。 |
| プロジェクト管理および会計 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations の統合ジャーナルが転記されると、転記先でないアカウントにディメンションがないため失敗する。 |
| プロジェクト管理および会計 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 保留中のベンダーの請求書で、調達カテゴリがアイテムに割り当てられている場合、**プロジェクト** タブが編集できない。 |
| プロジェクト管理および会計 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Project Operations Dataverse にログインしていない場合、ナビゲーションペインが表示されない。 |
| プロジェクト管理および会計 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 適用されたリテイナー ケースでプロジェクトの請求書から収益を転記する際、伝票上のトランザクションのバランスが正しく取れていないため問題が発生する。 |
| プロジェクト管理および会計 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 請求書提案を転記した後に見積を作成すると、修正明細のインポートがブロックされる。 |
| プロジェクト管理および会計 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 完全に請求されたマイルストーンのレコードの修正ができない。 |
| 出張と経費 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | すべての経費レポートが、経費モバイル アプリでカテゴリーを検索する時に表示される。 |
| 出張と経費 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | クレジット カード取引から作成された経費から、ベンダー取引や消費税取引に誤った金額が計上される。 |
| 出張と経費 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | **経費レポート** ページを更新すると、無関係な警告が表示される。 |
| 出張と経費 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 中間承認者を削除した後にワークフローを介して経費レポートを再送信すると、間違った中間承認者が使用される。 |
| 出張と経費 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | マイルの設定に関連する転記エラーが発生する。 |
