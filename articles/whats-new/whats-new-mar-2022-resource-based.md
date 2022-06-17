---
title: 2022 年 3 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオの Project Operations の 2022 年 3 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910912"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 3 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

*適用対象: リソース/非在庫ベースのシナリオ向け Project Operations*

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.30.0.99 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.25 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

日当は、新しく再考された最新の経費ワークスペースでサポートされるようになりました。 この機能を有効にすると、日当を使用する企業のユーザーが、日当経費の提出や払い戻しを簡単に実行することができます。 詳細については、[日当経費](../expense/per-diem-expenses.md) を参照してください。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

次の一覧は、2022 年 3 月にリリースされた Project Operations で変更または追加された二重書き込みマップを表示しています。

| **エンティティ マップ** | **更新バージョン** | **コメント** |
| --- | --- | --- |
| Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ msdyn\_projectvendorinvoicelines | 1.0.0.3 | Dataverse の請求書行エンティティに合わせてマッピングが更新されました。 <br>マッピング バージョン 1.0.0.4 をアクティブ化しないでください。 次回の月次更新では、Finance 環境バージョン 10.0.26 と組み合わせて使用できるようになります。 |

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 時間と経費 | 2388011 | 一括承認時に、時間入力の送信者に拒否コメントを表示します。 |
| プロジェクト計画および追跡 | 2495294 | プロジェクトの詳細は、**タスクの詳細** ページで編集することができません。 |
| 請求および価格設定 | 2499605 | 見積もりマイルストーンで作成された契約マイルストーンは、誤って読み取り専用としてマークされています。 |
| プロジェクト計画および追跡 | 2506050 | 保存する変更がない場合、操作セットは 1 時間保留のままになります。 その後、セットは誤って **失敗** とマークされますが、すぐに完了する必要があります。 |
| 請求および価格設定 | 2507401 | キャッシュが正しくないため、既定の契約単位がプロジェクトに誤って入力されています。 |
| 請求および価格設定 | 2541660 | 二重書き込みの **受注作成の検証** は、プロジェクトベースの受注のみが対象です。 |
| 請求および価格設定 | 2552745 | 分割請求ルールを設定した顧客間で税金が分割されることはありません。 |
| 請求および価格設定 | 2558859 | 価格ディメンションが設定されている場合のエラー メッセージが改善されました。 |
| 請求および価格設定 | 2558933 | **msdyn\_project** が価格ディメンションとして追加された場合、**プロジェクトの見積もりからのインポート** は失敗します。 |
| 請求および価格設定 | 2559101 | プロジェクト パラメータの削除はブロックされず、問題が発生します。 |
| 営業案件管理 | 2570390 | 二重書き込みプラグインは、アカウントの種類が正しくない場合でも、見積もり、注文、および営業案件のアカウントの種類を強制的に **顧客** に設定します。 |
| 請求および価格設定 | 2586097 | プロジェクトがプロジェクト契約品目から削除されても、分割請求コストの実績は取り消されません。 |
| 請求および価格設定 | 2589619 | リスト外資料に対する税金は、未請求の営業実績と請求書に反映されます。 |
| 営業案件管理 | 2594015 | **Net60** 支払い条件のある顧客に見積もりを獲得としてクローズすることはできません。 |
| プロジェクト計画および追跡 | 2595841 | Project for the Web では、新しいリソース要求を作成する際に、**msdyn\_ actualstart** の不在に関するエラー メッセージがユーザーに送信されます。 |
| 時間と経費 | 2602511 | 時間エントリの **拒否者** フィールドに、拒否者という名前を付けられたユーザーの代わりに **システム** が表示されます。 |
| 時間と経費 | 2602528 | プロジェクト承認者は、承認者としてリストされていないプロジェクトの時間を承認できます。 |
| 請求および価格設定 | 2608550 | 元の請求書に変更がなくても、修正請求書を確認できます。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| プロジェクト管理および会計 | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | **カテゴリ ID** フィールドで許容される長さに関して、Finance と Project Operations の間で不一致があります。 |
| プロジェクト管理および会計 | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | **分割払い請求書発行** フィールドが **利益と損失** に設定され、**完了率** の原則が使用されている場合、固定価格のプロジェクトは除外できません。 |
| プロジェクト管理および会計 | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Project Operations 統合の仕訳帳の経費行のプロジェクト設定から、誤った既定の消費税グループが入力されています。 |
| プロジェクト管理および会計 | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Project Operations との統合展開では、プロジェクトの仮発行請求書のヘッダー ディメンションを編集することはできません。 |
| プロジェクト管理および会計 | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | 会社間の仕入先請求書は、Dataverse と統合しません。 |
| プロジェクト管理および会計 | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | 顧客残高通貨と報告通貨に不一致があります。 |
| プロジェクト管理および会計 | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | 顧客がすべての請求書を保留にしている場合でも、プロジェクト請求書を転記することができます。 |
| プロジェクト管理および会計 | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | **ヘッダー** と **行** ビューのあるプロジェクトの仮発行請求書に **すべての行を削除する** ボタンがありません。 |
| プロジェクト管理および会計 | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | 仕入先請求書を転記すると、次のエラーが発生します。「請求書の会計日は、関連する発注書と同じ会計年度である必要があります。 発注書の年末処理を実行するか、日付を現在の会計年度に変更してください。」 |
| 出張と経費 | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | プロジェクトのコミット済みコストは、出張費要求のコミット済みコストがリリースされた後はリリースされません。 |
| 出張と経費 | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | 経費報告書を提出すると、次のエラーが発生します:「スタック トレース: 会社が存在しません」 |
| 出張と経費 | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | **仕訳帳のアクティビティを要求する** パラメーターがプロジェクトで選択されている場合は、既定の **プロジェクト ID** は経費報告書に入力されません。 |
| 出張と経費 | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | **経費の転記** ボタンは、リソース/非在庫のシナリオの Project Operations では正しく機能しません。 |
| 出張と経費 | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | 乗客を含むマイレージ経費報告書の **1 マイルあたりのレート** でエラーが発生しました。 |
| 出張と経費 | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | 2 つの異なる車両が **マイレージ レート層** の経費カテゴリで使用されている場合、従業員の経費マイレージ レートが正しく合計されません。 |
| 出張と経費 | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | 出張費要求の **プロジェクト** フィールドの検索は、プロジェクトの正しいリストを返しません。 |
| 出張と経費 | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **レビュー中のマイレージ** に、経費報告書に関する警告が表示されます。 |
| 出張と経費 | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | 受領する経費 OCR サービスの URL に問題があるため、光学式文字認識 (OCR) サービスが機能しません。 |
| 出張と経費 | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **定期的な経費を迅速に明細化する** 機能が有効になっている場合、**明細化** ページを開く度に経費報告書の明細行の金額が変更します。 |
| 出張と経費 | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | 中間リストに複数の承認者がいる場合、経費報告書を削除することはできません。 |

## <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Project Operations の削除済みまたは非推奨の機能](removed-depreciated-features-project.md) の記事では、Dynamics 365 Project Operations の削除済みまたは非推奨の機能について説明します。

- 削除された機能は製品で使用できなくなりました。
- 非推奨の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

機能が製品から削除される 12 ヶ月前に、非推奨の通知が [Project Operations の削除済みまたは非推奨の機能](removed-depreciated-features-project.md) の記事に表示されます。

コンパイル時にのみ影響する破壊的変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
