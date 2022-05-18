---
title: 2020 年 12 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオ向け Project Operations の 2020 年 12 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 766e2815d2a07708ace91a0ff5308e0195ff0edc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579864"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 年 12 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

- Dataverse 環境バージョン 4.5.0.134 での Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.15 でのプロジェクト管理と会計

このリリースに更新する方法については、[Finance 環境で Project Operations を更新する](ur5-nonstocked-installation.md)を参照してください。

## <a name="features-included-in-this-release"></a>このリリースが含む機能
このリリースは以下の機能を含みます。

  - [会社間請求](../project-accounting/intercompany-invoicing-overview.md) 
  - [顧客の前払金と着手金](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>リソース非在庫ベースのシナリオ向け Project Operations の更新

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能                    | 照合番号 | 品質更新プログラム                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 請求と価格             | 1986009          | プロジェクトと契約品目のリンクが設定/解除される前に確認する場合は、手動で作成した仕訳帳明細行のパフォーマンスに一貫性がなくなります                     |
| 請求と価格             | 2028174          | 請求明細行詳細の更新は、仕訳帳の修正ロジックに従う必要があります                                                                                  |
| 請求と価格             | 2028315          | 編集できるネストされたグリッドの動作を修正します                                                                                                                        |
| 請求と価格             | 2031070          | 請求明細行修正の詳細の調整は、仕訳帳の修正ロジックに従う必要があります                                                                              |
| 請求と価格             | 2034186          | 契約品目でプロジェクトの更新を可能にする必要があります                                                                                                        |
| 請求と価格             | 2034206          | プロジェクトと契約品目のリンクを解除する際は、実際の取消時に調整ステータスの設定が必要です                                                        |
| 請求と価格             | 2040871          | 経費見積もりグリッドで単位と単位グループのセルについて更新を許可します                                                                                       |
| 請求と価格             | 2053754          | 請求書の編集で作成した実績は、調整ステータスと請求ステータスをマークしません                                                                |
| 請求と価格             | 2057874          | 請求明細行詳細の編集中に作成したトランザクション接続を修正します                                                                                     |
| 請求と価格             | 2057875          | 請求明細行詳細の編集中に作成したトランザクション発生元を修正します                                                                                        |
| 請求と価格           | 2057944          | 請求書修正の請求に対応していない実績に対して、コミット済みとして設定した超過しない状態                                             |
| 請求と価格           | 2066169          | 二重書き込みを使用した統合の場合、未請求販売レコードの会計日を負の値で更新します                                                            |
| 請求と価格           | 2067622          | マイルストーンの生成中は処理中のアイコンを表示します                                                                                                |
| 請求と価格           | 2067624          | マイルストーンの生成時は、契約金額をビジネス推奨としてマークする必要があります                                                                      |
| 請求と価格           | 2086880          | プロジェクト ベースの見積依頼明細行でリボンの **推奨** ボタンを非表示にします                                                                                                |
| 請求と価格           | 2098140          | 統合環境で **請求書の修正** ボタンを表示します                                                                                             |
| 展開と構成  | 2101152          | Power Platform 管理センターで Project Operations テンプレートを使用して作成した新しい環境では、インストール後の操作をすべて実行する必要があります               |
| 営業案件の管理        | 2086601          | 非アクティブ化したロールとカテゴリは、見積依頼明細行と契約品目の課金対象のロールとカテゴリの一覧にコピーできません |
| プロジェクトの計画と追跡 | 1949065          | データの可視性は 200% ズーム時に正しく機能します                                                                                                                   |
| プロジェクトの計画と追跡 | 2046317          | Project Operations でプロジェクトのエンティティ名を変更できます                                                                                   |
| プロジェクトの計画と追跡 | 2057171          | **プロジェクト** ページの **プロジェクト開始日** フィールドが空の場合に表示するエラー メッセージを更新しました                                                           |
| プロジェクトの計画と追跡 | 2057197          | タスク参照を使用した見積行のコピーはサポートしていません                                                                                                     |
| プロジェクトの計画と追跡 | 2060687          | 特定期間の経過後にタイムゾーン警告が非表示になります                                                                                                      |
| リソース管理           | 1832887          | Dataverse や Finance の環境で、繰り返し可能なデータ読み込みを行う際は、既定のリソース カテゴリ ID を静的にする必要があります                                                 |
| 時間と経費              | 2081793          | **経費カテゴリ名** は、財務と運用アプリで **経費カテゴリの説明** フィールドにマッピングする必要があります                                                  |
| 時間と経費              | 2034882          | Dynamics 365 Field Service をインストールすると、**新規** ボタンが時間入力のコマンド バーに 2 回表示されます                                          |
| 時間と経費              | 2056028          | **時間の編集** ページを更新してタイムラインを含めます                                                                                                              |
| 時間と経費              | 1983747          | 時間入力グラフは追加データを示します                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能                        | 照合番号 | 品質更新プログラム                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| プロジェクトの管理と会計 | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | 品目の返品要件に対する調整をブロックしました                                                                                                                                                                                                        |
| プロジェクトの管理と会計 | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | 書式設定したプロジェクトの請求書にフォーム メモが表示されない                                                                                                                                                                                                          |
| プロジェクトの管理と会計 | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | プロジェクト請求書の MEXICO CFDI 33 は、請求提案に基づく支払方法の更新を許可されていません                                                                                                                                                           |
| プロジェクトの管理と会計 | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | 会計日をオープン期間に自動で設定するパラメーターは **統合** 仕訳帳で優先されません                                                                                                                                                             |
| プロジェクトの管理と会計 | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **プロジェクト** 一覧ページに表示されない予測メニュー項目                                                                                                                                                                                                      |
| プロジェクトの管理と会計 | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **プロジェクト ステートメント** > **トランザクションと予測** を開けません                                                                                                                                                                                                      |
| プロジェクトの管理と会計 | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | リソース割り当ての削除と読み取りによって、Finance のプロジェクト予測エントリが 2 倍になります                                                                                                                                                                   |
| プロジェクトの管理と会計 | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | プロジェクトに契約品目が存在しない場合、Dataverse でプロジェクト見積もりを作成できません                                                                                                                                                                 |
| プロジェクトの管理と会計 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 会社基本通貨と取引通貨が異なる場合、伝票の不均衡エラーが原因で消去が失敗します                                                                                                                                            |
| プロジェクトの管理と会計 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | 固定価格プロジェクトで転記済みプロジェクト トランザクションの請求書ステータスに対するフィルターが機能しない                                                                                                                                                            |
| プロジェクトの管理と会計 | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Dataverse でタスクの開始日を更新できません                                                                                                                                                                                                                    |
| プロジェクトの管理と会計 | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | Project Operations 統合シナリオで請求提案明細行を削除できます                                                                                                                                                                                    |
| プロジェクトの管理と会計 | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | Project Operations 統合シナリオで請求提案明細行を削除できます                                                                                                                                                                                    |
| プロジェクトの管理と会計 | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Dataverse 統合がない場合に複数の契約品目機能の有効化を防止する                                                                                                                                                                                        |
| プロジェクトの管理と会計 | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | 取引先企業の請求時 = 損益の場合、表示される請求済み売上の見積もりはゼロ (0) です                                                                                                                                                                          |
| プロジェクトの管理と会計 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | 仕掛品 - 会社間プロジェクトで請求書に売上高を転記すると、予期しない取引先企業が選択されます                                                                                                                                                                           |
| プロジェクトの管理と会計 | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | Project Operations を有効化した状態では見積もり/売上認識を実行できません                                                                                                                                                                         |
| 出張と経費                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | 代理人が入力した経費は、その代理人ではなく経費ユーザーに戻ります                                                                                                                                                                                           |
| 出張と経費                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | 経費報告書ワークフローの代理ユーザーがワークフローを送信する場合、ワークフロー作成者として識別されません                                                                                                                                                             |
| 出張と経費                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | 法人オーバーライドの既定ディメンションが会社間の経費レポートで機能しない                                                                                                                                                                    |
| 出張と経費                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | 日当経費カテゴリの最終日の食費割引計算に関する問題                                                                                                                                                                                    |
| 出張と経費                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | 出張費要求にリンクした経費レポートから経費明細行を削除した後、**出張費要求** ページの **調整額** フィールドが更新されない                                                                                                       |
| 出張と経費                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | ワークフローへの送信後に経費レポートのポリシーを検証しました                                                                                                                                                                                           |
| 出張と経費                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | 入力デリゲートに出張費の領収書が正しく表示されない                                                                                                                                                                                            |
| 出張と経費                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | ユーザー言語の設定が es-MX の場合、従業員ごとの経費タイプに項目ごとの経費を表示しません                                                                                                                         |
| 出張と経費                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | 経費レポートの経費カテゴリに不正なサブカテゴリを入力できます                                                                                                                                                                                       |
| 出張と経費                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | 経費レポートの金額が現金前払い額を超える場合、経費レポートによる現金前払い調整が正常に機能しません                                                                                                           |
| 出張と経費                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | ProjProjectLookup に関連したクエリのパフォーマンス問題。 クエリの実行に長い時間が必要なため顧客がブロックされます。                                                                                                                     |
| 出張と経費                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | **オフセット支払勘定に基づくトランザクションのグループ化を許可する** と **転記時に会計日を修正する** を有効化した転記済みの経費レポートが、**勘定配布** テーブルに会計日をグループ化していないことを示し、消費税レコードに影響を与えます |
| 出張と経費                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | 経費レポート明細行で **受取人払い VAT** を使用する場合、外貨でインポートしたクレジット カード トランザクションが不正なベンダー トランザクションを作成します                                                                                                                     |
| 出張と経費                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | プロジェクト ID をヘッダー レベルで追加すると、会社間の経費レポートを作成できません                                                                                                                                                                 |
| 出張と経費                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | 経費の額が現金前払い額を超える場合に発生する経費支払の問題                                                                                                                                                                          |
| 出張と経費                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | ユーザー ロールを特定の組織に割り当てた場合、会社間の経費レポートでプロジェクト ID 情報が空です                                                                                                                                           |
| 出張と経費                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | 経費レポートの自動転記ワークフローを完了しても請求書が転記されません                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>規制の更新
財務と運用アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、LCS にサインインし、問題検索ツールを使用して、予定されている規制の更新を表示することもできます。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]