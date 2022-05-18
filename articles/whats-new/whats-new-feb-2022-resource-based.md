---
title: 2022 年 2 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオの Project Operations の 2022 年 2 月リリースで利用可能な品質更新に関する情報について説明します。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600840"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 2 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

*適用対象: リソース/非在庫ベースのシナリオ向け Project Operations*

このトピックは、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます:

- Dataverse 環境のバージョン 4.28.0.120 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.24 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

- このリリースの時点で、1 つのプロジェクトに最大 300 人のチーム メンバーを追加できます。 以前は、チーム メンバー数の制限は 150 人でした。 詳細については、[プロジェクトの制限](../project-management/create-wbs.md#project-limitations) を参照してください。

## <a name="project-operations-dual-write-map-updates"></a>Project Operations 二重書き込みマップの更新

次の一覧は、2022 年 2 月にリリースされた Project Operations で変更または追加された二重書き込みマップを表示しています。

| エンティティ マップ | 更新バージョン | Comments |
| --- | --- | --- |
| Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn\_expenses) | 1.0.0.3 | プロジェクト アクティビティの Dataverse への同期に拡張しました。 |

Project Operations の二重書き込みマップの現在の一覧とバージョンについては、[Project Operations 二重書き込みマップ バージョン](../environment/resource-dual-write-maps.md) を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求および価格設定 | 2415109 | **Operations 支払い条件** フィールドの規定値は、プロジェクト契約の顧客レコードと見積もり請求書レコードである必要があります。 |
| 請求および価格設定 | 2497369 | 材料の修正は、**修正** パラメーターの日付値に従う必要があります。 |
| 請求および価格設定 | 2498697 | **時間エントリのリコール** のセキュリティ構成を改善しました。 |
| 請求および価格設定 | 2513824 | リソースベースのシナリオの場合、トランザクション カテゴリ ID は Project Operations で 28 文字を超えてはなりません。 |
| 請求および価格設定 | 2517455 | **請求書行のトランザクションの更新** アクションは、同じ請求書に対してアクションを複数回同時にトリガーできません。 |
| 請求および価格設定 | 2517465 | **請求書行の詳細を非アクティブ化する** アクションはサポートされていないためブロックされています。 |
| 請求および価格設定 | 2556660 | プロジェクト パラメーター レコードに添付されている価格表で実行される日付有効性チェックを修正しました。 |
| 営業案件管理 | 2369202 | 重複している有効日がある価格表を同じプロジェクト契約に添付できることを確認するビジネス ロジックを修正しました。 |
| 営業案件管理 | 2385965 | **保存して閉じる** を選択したときの **プロジェクト契約** ページの **顧客** タブにある動作を修正しました。 |
| 時間と経費 | 2538503 | プロジェクト タスクは、経費レポートが転記された後に **プロジェクト実績** エンティティで使用可能になります。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| プロジェクト管理および会計 | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | 仕入先クレジット メモのインポート中に、エラーが発生します。 エラー メッセージには、「保有額は残りの正味金額を超えることはできません」と記載されています。 |
| プロジェクト管理および会計 | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | 仮発行請求書に、未請求の売上実績である手数料がゼロのトランザクションが含まれている場合、請求は発生しません。 |
| プロジェクト管理および会計 | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | 購入価格を更新し、**変更管理をアクティブ化する** を有効にすると、転記されたコストは正しくなくなります。|
| プロジェクト管理および会計 | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | 固定価格プロジェクトの転記見積もりでは、**見積もり計算で使用するプロジェクト契約通貨を有効にする** 機能が有効になっていても、見積もり伝票に誤った通貨と金額が使用されます。 |
| プロジェクト管理および会計 | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** は、有効化されていない構成キーを持つエンティティの例外をキャッチせずに追跡の変更を有効するために、呼び出しを行わないでください。 |
| プロジェクト管理および会計 | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | 複数の詳細な仕訳帳が転記されてエラーが発生した場合、バッチ ジョブは修正されます。 |
| 出張と経費 | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | 経費報告書の現金前払いに関連する決済の問題が原因で、税額は現金前払いの一部としてカバーされていません。 |
| 出張と経費 | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | 消費税情報は **経費 - 転記されたトランザクション** レポートに含まれていません。 |
| 出張と経費 | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | **領収書が必要な** 経費ポリシー違反は、経費報告書に誤って警告を表示します。 |
| 出張と経費 | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | プロジェクト トランザクションは、トランザクションがマイレージ費用の結果である場合、総売上金額に回収不可能な消費税を含みません。 |
| 出張と経費 | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | 明細行に税がある場合、明細行の日付を変更することはできず、ソース ドキュメントの状態エラーが発生します。 |

## <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Project Operations の削除済みまたは非推奨の機能](removed-depreciated-features-project.md) のトピックでは、Dynamics 365 Project Operations の削除済みまたは非推奨の機能について説明します。

- 削除された機能は製品で使用できなくなりました。
- 非推奨の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

機能が製品から削除される 12 ヶ月前に、非推奨の通知が [Project Operations の削除済みまたは非推奨の機能](removed-depreciated-features-project.md) のトピックに表示されます。

コンパイル時にのみ影響する破壊的変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
