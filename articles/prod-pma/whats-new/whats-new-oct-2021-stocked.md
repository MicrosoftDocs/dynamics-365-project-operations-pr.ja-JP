---
title: 2021 年 10 月の新機能と変更点 - 在庫/製造ベースのシナリオ向け Project Operations
description: この記事は、在庫/製造ベースのシナリオ向け、 Project Operations の 2021 年 10 月リリースで利用可能な品質更新に関する情報を提供します。
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029949"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>2021 年 10 月の新機能と変更点 - 在庫/製造ベースのシナリオ向け Project Operations

_**適用対象:**  Project Operations (在庫/本番ベースのシナリオ向け)_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dynamics 365 Finance 環境バージョン 10.0.22 でのプロジェクト管理と会計
 
## <a name="quality-updates"></a>品質更新プログラム

| 機能 | 照合番号 | 品質更新プログラム |
|--------------|------------------|----------------|
| プロジェクト管理および会計 | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | プロジェクトの仕掛品 (WIP) と未収収益の金額が、企業間取引の顧客請求書が計上されたときに正しく取り消されませんでした。 |
| プロジェクト管理および会計 | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **オープンなトランザクションが存在する場合に、プロジェクトの終了を防止する** 機能が動作しない。 |
| プロジェクト管理および会計 | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | フリーテキストの請求書の請求区分で、その機能が有効になっている場合、プロジェクトの寸法が自動的に入力されない。 |
| プロジェクト管理および会計 | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | 企業間ではないシナリオでは、プロジェクトの請求書が計上されたときに、WIPと未収金の金額が正しく取り消されない。 |
| プロジェクト管理および会計 | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Microsoft Excel アドインをプロジェクト経費仕訳に使用し、**オフセット勘定** タイプ フィールドを **プロジェクト** に設定すると、借方と貸方の値が入れ替わります。 |
| プロジェクト管理および会計 | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | 在庫品を含み、**UseTax** をマークしたときに控除対象外の税金額があるプロジェクトの注文書で、プロジェクト取引に計上される金額が過大になる。 |
| プロジェクト管理および会計 | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | システムが、プロジェクトの損益報告書とプロジェクトの WIP 報告書の間で金額を分割します。 |
| プロジェクト管理および会計 | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | 部分的に返品された品目の要件を調整すると、手持ち在庫が正しくなくなります。 |
| プロジェクト管理および会計 | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | リソース名を Microsoft Project で編集すると、Project Operations で重複して表示される。 |
| プロジェクト管理および会計 | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | 買掛金勘定の企業間の保留中のベンダー請求書のコストがある企業間の経費報告が、最初に **プロジェクト WIP コスト** の計上タイプに計上されます。 しかし、処理の過程で、見積関連のコストが、想定していた **企業間コスト** の計上タイプではなく、**プロジェクトのコスト** 計上タイプに計上されてしまいます。 |
| プロジェクト管理および会計 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | ベンダー保持の結果、プロジェクト経費のトランザクションが表示されない。 |
| プロジェクト管理および会計 | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | タイムシートでは、すべての会計上の分配や一般的な仕訳の配分エントリで、取引通貨での取引額を指定された小数点以下の桁数に丸める必要があります。 |
| プロジェクト管理および会計 | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | 計画された注文が確定すると、プロジェクト品目の要件の量が自動的に更新されます。 |
| プロジェクト管理および会計 | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | 発注書の前払い請求書で、伝票番号、トランザクション タイプのベンダー残高、口座番号を取り消せない。 |
| プロジェクト管理および会計 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | ベンダー請求書の統合がオンになっていると、企業間のベンダー請求書が破損する。 |
| プロジェクト管理および会計 | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | プロジェクト経費の仕訳帳を作成すると、原価額が **クレジット** フィールドに表示される。 |
| プロジェクト管理および会計 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | プロジェクトの請求書に記載されている支払条件が、期待通りに機能しない。 |
| プロジェクト管理および会計 | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | タイムシート バウチャーで、連続した番号を設定すると再利用できてしまう場合がある。 |
| プロジェクト管理および会計 | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | フランス: プロジェクト契約の請求書案にある **自動保持量** のロジックと、**手動保持量** のロジックが一致しない。 |
| プロジェクト管理および会計 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | ベンダーの保持が解除されると、伝票の計上に不正な追加行が発生する。 |
| プロジェクト管理および会計 | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **請求書の提案作成** ページで **請求書の日付** フィールドを変更すると、次のエラーが発生することがあります: 「オブジェクト参照がオブジェクトのインスタンスに設定されていません」 |
| プロジェクト管理および会計 | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | **TSLine** のワークフローからタイムシートを承認しようとすると、土日のタイムシートポリシーがある場合にエラーが発生する。 |
| プロジェクト管理および会計 | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | 請求書の合計金額を計算する際に、**請求書のトランザクションサマリー** から期首残高のプロジェクト項目タイプが除外される。 |
| プロジェクト管理および会計 | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | プロジェクトの生産オーダーの消費コストが 0 の場合、見積もりをしようとすると次のようなエラーが発生する: 「ゼロでの除算が実行されました」 |
| プロジェクト管理および会計 | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Android のプロジェクト タイムシート モバイル アプリが反応しなくなる。 この問題は、**TimeEntryDataManager ArgumentNullException** に関連するものです。 |
| プロジェクト管理および会計 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations の統合ジャーナルを転記すると、アカウントにディメンションがないために失敗する。 しかし、ディメンションがないアカウントは、転記先のアカウントではありません。 |
| プロジェクト管理および会計 | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | 検索の **ToDate** フィルターが、**転記コスト** ページの **選択** ダイアログボックスから削除されてもクリアされない。 |
| プロジェクト管理および会計 | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **時間のみ** タイプのプロジェクトで作成されたタイムシートについて、**すべての配布をリセットする** が失敗し、エラーが表示される。 |
| プロジェクト管理および会計 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 保留中のベンダーの請求書で、調達カテゴリがアイテムに割り当てられている場合、**プロジェクト** タブが編集できない。 |
| プロジェクト管理および会計 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Project Operations Dataverse にログインしていない場合、ナビゲーションペインが表示されない。 |
| プロジェクト管理および会計 | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | 企業間のプロジェクト調整トランザクションでは、相手先企業に問題があります。 |
| プロジェクト管理および会計 | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | 総勘定元帳の **注文書の期末処理** で注文書が処理された場合、プロジェクトのコミットされたコストは、間違った数量と原価を計算する。 |
| プロジェクト管理および会計 | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | 品質オーダーを持つプロジェクトの生産注文が完了として報告されると、次のようなエラーが発生する: 「在庫トランザクションでマークされた仮想トランザクションがありません」 |
| プロジェクト管理および会計 | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | プロジェクト関連の買掛金請求書を転記すると、「列挙テキストプロジェクト - 原価 - 明細が存在しません」というエラーが発生する |
| プロジェクト管理および会計 | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | 手動で収益を計上すると間接費が 2 倍になる。 |
| プロジェクト管理および会計 | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | 収益を計上と、WIP の転記でトランザクションが発生しない。 |
| プロジェクト管理および会計 | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | 受信したプロジェクトの発注書が存在する場合に、標準原価項目の保留価格の有効化が失敗する。 |
| プロジェクト管理および会計 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 請求書の転記による WIP の反転値が、時間入力による元の転記された WIP の値と異なる。 |
| プロジェクト管理および会計 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 適用されたリテイナーのケースでプロジェクトの請求書による収益を計上する際に、伝票上のトランザクションのバランスが正しく取れていない。 |
| プロジェクト管理および会計 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 請求書の提案が掲載された後に見積書を作成すると、Project Operations で修正ラインのインポートがブロックされる。 |
| プロジェクト管理および会計 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 完全に請求されたマイルストーンのレコードの修正ができない。 |
| プロジェクト管理および会計 | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | 自動課金を使用している場合、タイムシートの企業間顧客請求書が計上できず、エラーメッセージが表示される。 |
| プロジェクト管理および会計 | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | サブ プロジェクトのアドレスが正しく更新されない。 |
| プロジェクト管理および会計 | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | 品目要求の原価価格が、連結発注の購入価格で更新されてしまう。 |
| プロジェクト管理および会計 | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | 購入価格を更新し、パラメーター **変更管理を有効にする** を有効にすると、計上されたコストが正しくない。 |
| 出張と経費 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | すべてのユーザーの支出が、経費モバイル アプリでカテゴリーを検索すると見ることができる。 |
| 出張と経費 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | クレジットカード取引から作成された経費から、ベンダー取引や消費税取引に誤った金額が計上される。 |
| 出張と経費 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | 経費報告書のページを更新すると、無関係な警告メッセージが表示される。 |
| 出張と経費 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 中間承認者を削除した後にワークフローを介して再送信すると、間違った中間承認者が使用される。 |
| 出張と経費 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | マイルの設定に関連する転記エラーが発生する。 |
| 出張と経費 | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | 企業間取引の経費報告書に添付されていない取引が再追加されたとき、配布では法人が更新されない。 |

### <a name="regulatory-updates"></a>規制の更新

財務と運用アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates)を参照してください。 また、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、課題検索ツールを使用して、予定されている規制の更新を確認することもできます。 問題検索では、国や地域、機能の種類、リリースなどで検索することができます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
