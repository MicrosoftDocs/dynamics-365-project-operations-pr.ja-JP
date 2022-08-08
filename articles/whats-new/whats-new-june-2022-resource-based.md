---
title: 2022 年 6 月の新機能 - リソース/非在庫のシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 6 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031337"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 6 月の新機能 - リソース/非在庫のシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境バージョン 4.43.0.77、または 4.43.0.119 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.27 でのプロジェクト管理と会計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

次のテーブルは、2022 年 6 月にリリースされた Project Operations で変更または追加された二重書き込みマップを表示しています。

| エンティティ マップ | 更新バージョン | Comments |
| --- | --- | --- |
| Project Operations 統合プロジェクト ベンダー請求書のエクスポート エンティティ (msdyn_projectvendorinvoices) | 1.0.0.1 | 従来のフィールドは廃止され、ベンダーの請求書の状態を追跡するために新しいフィールドにマッピングされました。 |

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 外注 | 2708885 | 予約可能なリソースが入力されていない場所で、ユーザーが予約可能なリソース予約ヘッダーレコードを作成したときに表示されるエラーメッセージを修正しました。 |
| プロジェクト計画および追跡 | 2629441 | プロジェクト タスクが更新されたときに無限ループを防ぐのに役立つワークフロー トリガー ロジックを修正しました。 |
| 時間と経費 | 2641209 | 割り当て/予約からのタイム エントリのインポートでは、予約可能なリソース参照を保持する必要があります。 |
| プロジェクト計画および追跡 | 2651148 | プロジェクト ドキュメントのヘッダーを保護する必要があります。|
| プロジェクト計画および追跡 | 2653145 | 名前に無効な文字が含まれるプロジェクト レコードを作成できないようにするための検証が追加されました。 |
| 時間と経費 | 2654710 | **承認** ページのフィルタリングを修正しました。 |
| 請求および価格設定 | 2667805 | 未請求の販売実績が存在しない場合に、請求済みの販売実績が作成されないようにするための検証が追加されました。 |
| 請求および価格設定 | 2668378 | 論理名とフィールド名が入力されていない限り、カスタム価格設定ディメンションが追加されないようにするための検証が追加されました。 |
| 外注 | 2677485 | ベンダーの請求書ラインの二重書き込みマップのターゲット バージョンを更新しました。 |
| 時間と経費 | 2700428 | 承認ロジックを改善して、承認セットの 1 つがシステム ジョブでスタックしている場合でも、プロジェクトの他の承認セットを処理できるように改善されました。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) を参照してください。
