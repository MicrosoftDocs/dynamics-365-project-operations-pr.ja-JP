---
title: 2021 年 1 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオ向け Project Operations の 2021 年 1 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958925"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 1 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_


このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

  - Dataverse 環境バージョン 4.6.0.154 での Project Operations
  - Dynamics 365 Finance 環境バージョン 10.0.16 でのプロジェクト管理および会計

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能領域** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| **展開と構成** | 2106818 | ページのカスタマイズに関連する問題を引き起こしていた Web リソースの名前変更を修正しました。 |
| **請求と価格** | 2091908 | Project Operations が Dynamics 365 Field Service と一緒にインストールされている場合の、**請求書** ページの **価格の​​ロック** と **現在の値付けを​​使用** オプションの可視性を修正しました。 |
| **請求と価格** | 2103058 | **プロジェクト合計** タスクを更新して、実際のコストの null 値を処理できるようにしました。 |
| **請求と価格** | 2116100 | **実績の正しいエントリ** 機能で使用されるエラー メッセージを改善しました。 |
| **請求と価格** | 2116129 | **プロジェクト** ページの **見積り** タブで、経費見積もりの可視性を改善しました。 |
| **請求と価格** | 2119112 | 異なる為替レートが使用されている場合の実際の売上と実際のコストの固定集計。 |
| **請求と価格** | 2134705 | **請求書** ページが開き、Field Service がインストールされたときに発生する「未定義のプロパティ **getResourceString** を読み取れません」というエラーを修正しました。 |
| **営業案件管理** | 2022195 | **プロジェクト** ページのタスクベースの請求グリッドに、そのタスクにリンクされた契約または見積もり明細行があることを示すアイコンが含まれます。 |
| **営業案件管理** | 2029135 | ユーザーが前払金額が請求されている確認済みの請求書で請求明細行を開こうとしたときに発生するビジネス プロセス エラーを修正しました。 |
| **営業案件管理** | 2040713 | 契約から請求書を作成し、Field Service がインストールされているときに発生するスクリプト エラーを修正しました。 |
| **プロジェクトの計画と追跡** | 2090202 | **非推奨** として使用されなくなったマーク付きのビジネス ルール。 |
| **時間と経費** | 2091249 | ユーザーが送信済みまたは承認済みの時間エントリでタスクを変更できないよう、コントロールを強化しました。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計

| **機能領域** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| **プロジェクト管理および会計** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | **分割払** ページで、複数の資金源を持つ固定価格プロジェクトの契約金額が正しくありません |
| **プロジェクト管理および会計** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId** プレースホルダーにワークフロー **プロジェクト仮発行請求書をレビューする** のプロジェクト ID が表示されません。 |
| **プロジェクト管理および会計** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | プロジェクト仮発行請求書を転記すると、間違った現金割引日が使用されます。 |
| **プロジェクト管理および会計** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Project Operations でリソース割り当てを削除および読み取ると、Finance のプロジェクト予測エントリが 2 倍になります。 |
| **プロジェクト管理および会計** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Project Operations では、Dataverse でプロジェクトに契約ラインがない状態でプロジェクト見積もりを作成することはできません。 |
| **プロジェクト管理および会計** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | プロジェクト経費トランザクションの財務ディメンションは、関連する伝票および原価が残高に転記されるときの経費清算書の勘定配賦と同期されません。 |
| **プロジェクト管理および会計** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 固定価格プロジェクトで転記済みプロジェクト トランザクションの **請求書ステータス** に対するフィルターが機能しません。 |
| **プロジェクト管理および会計** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | **定期** セクションで、逆見積を除去する機能が動作しません。 |
| **プロジェクト管理および会計** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Project Operations が Dataverse と統合されると、仮発行請求書明細行を削除できます。 |
| **プロジェクト管理および会計** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Dataverse 統合がない場合に、複数の契約品目機能の有効化が防止されます。 |
| **プロジェクト管理および会計** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | 分割払い請求が損益に等しい場合、見積りページの請求済み収益がゼロと表示されます。 |
| **プロジェクト管理および会計** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | 請求書の修正は、統合環境では機能しません。 |
| **プロジェクト管理および会計** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 会社間プロジェクト請求書で仕掛品 - 売上値を転記すると、正しくない取引先企業が選択されます。 |
| **プロジェクト管理および会計** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Project Operations で、Dataverse の見積もりタスクへの依存関係を更新できません。 |
| **プロジェクト管理および会計** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Finance で Project Operations 統合仕訳帳を繰り返し削除すると、データが失われます。 |
| **プロジェクト管理および会計** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | プロジェクト仮発行請求書を転記する際に、「差し引かれた前払請求書が追加されたときに、トランザクション勘定がレポート通貨の勘定と一致しません」というエラーが発生します。 |
| **プロジェクト管理および会計** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations で既定のプロジェクト契約が更新された後、間違ったプロジェクト ID が控除に含まれます。 |
| **プロジェクト管理および会計** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Project Operations が有効になっていると、見積もりと収益認識を完了できません。 |
| **プロジェクト管理および会計** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations では、契約からプロジェクトを削除しても、契約の既定プロジェクトはリセットされません。 |
| **プロジェクト管理および会計** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations では、会社間請求書で、**行を追加** リストに間違った経費明細行が表示されます。 |
| **出張と経費** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | 契約品目に時間設定がないため、経費明細行を転記できません。 |
| **出張と経費** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | プロジェクト/カテゴリの検証が必須の場合、プロジェクトに関連付けられている経費カテゴリは経費清算書に表示されません。 |
| **出張と経費** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 経費清算書が行ごとに転記されても、現金前払い残高は更新されません。 |
| **出張と経費** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | 請求書が 2 つ以上の支払いトランザクションで決済された決済を取り消すと、**支払い情報を更新する** ジョブが失敗します。 |
| **出張と経費** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | 日当経費カテゴリの最終日の食費割引の計算に問題があります。 |
| **出張と経費** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | ユーザーの最初の接続が es-MX 言語であった場合、**従業員ごとの経費タイプ** レポートに項目別の経費が表示されません。 |
| **出張と経費** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | 経費報告請求書のベンダー支払いで、決済転記に間違った決済勘定が使用されます。 |
| **出張と経費** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | **オフセット支払勘定に基づくトランザクションのグループ化を許可する** と **転記時に会計日を修正する** が有効な状態で経費清算書を転記すると、**勘定配賦** テーブルの会計日がグループ化されず消費税レコードに影響を与えます。 |
| **出張と経費** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | 経費で使用チェック ボックスをオフにしてから、再度選択すると、経費サブカテゴリ マッピングが削除されます。 |
| **出張と経費** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | プロジェクト ID をヘッダー レベルで追加すると、会社間の経費清算書を作成できません。 |
| **出張と経費** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | 経費の額が現金前払い額を超える場合に、経費支払の問題が発生します。 |
| **出張と経費** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | ユーザー ロールを特定の組織に割り当てた場合、会社間の経費清算書で **プロジェクト ID** フィールドが空になります。 |
| **出張と経費** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 新しい経費明細行を追加すると、経費カテゴリがロックされます。 |
| **出張と経費** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | すでに分割されている経費清算書の行を明細化すると、買掛金\総勘定元帳の転記が完了しません。 **TRVEXPTRANS.SOURCEDOCUMENTLINE** が重複しているため、会計ソース エクスプローラーも破損します。 |
| **出張と経費** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | **TRVREQUISITIONLINE** テーブルに追加された顧客が重複しているインデックスでは、アップグレード中にエラーが発生します。 |
| **出張と経費** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operations では、Dataverse での会社間タスクの時間を作成または承認できません。 |

## <a name="regulatory-updates"></a>規制の更新

Finance and Operations アプリの規制の更新については、[規制の更新](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、LCS にサインインし、問題検索ツールを使用して、予定されている規制の更新を表示することもできます。 問題検索では、国、機能の種類、リリースで検索できます。
