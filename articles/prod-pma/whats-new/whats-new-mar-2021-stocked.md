---
title: 2021 年 3 月の最新情報または変更事項 - 在庫/製造ベースのシナリオ向け Project Operations
description: この記事は、在庫 / 製造ベースのシナリオの Project Operations の 2021 年 3 月リリースで利用可能な品質更新について説明します。
author: andchoi
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: fffa9d70574c8c91b63ceb5055af64a49c9d398b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911326"
---
# <a name="whats-new-or-changed-in-project-operations-march-2021-for-stockedproduction-based-scenarios"></a>2021 年 3 月の最新情報または変更事項 - 在庫/製造ベースのシナリオ向け Project Operations

_**適用対象:** 在庫/製造ベースのシナリオ向け Project Operations_

この記事は、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます。

- Dynamics 365 Finance 環境バージョン 10.0.17 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能
このリリースは以下の機能を含みます。

  - [プロジェクトの仮発行請求書のパフォーマンス](../project-invoice-proposal-performance.md)
 
### <a name="quality-updates"></a>品質更新プログラム

| 機能                        | 照合番号 | 品質更新プログラム                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| プロジェクト管理および会計 | [420064](https://fix.lcs.dynamics.com/Issue/Details/?bugId=420064) | マイナスの転記済みプロジェクト トランザクションは、在庫が再計算された後は更新されません。                                                                                                                      |
| プロジェクト管理および会計 | [438692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=438692) | 資金調達ソースに割り当てられたトランザクションまたは請求書がない場合は、資金調達ソースを削除できるはずです。                                                                                                           |
| プロジェクト管理および会計 | [439470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=439470) | 実際の見積もりトランザクションには、前の期間の経費および項目のトランザクションは表示されません。                                                                                                       |
| プロジェクト管理および会計 | [452710](https://fix.lcs.dynamics.com/Issue/Details/?bugId=452710) | プロジェクト品目要件の梱包明細の元帳記述値が正しくありません。                                                                                                              |
| プロジェクト管理および会計 | [455602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=455602) | 仕訳がプロジェクトに対して転記される場合、財務ディメンションは従業員と伝票の項目から選択されません。                                                                               |
| プロジェクト管理および会計 | [472988](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472988) | プロジェクト請求書合計で明細正味金額が更新されると、転記されたトランザクションの調整済み金額が販売金額に入力されます。                                                                               |
| プロジェクト管理および会計 | [477969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477969) | **支払時にベンダー請求書を支払う** ページのベンダー請求書行を確認する際、請求書がプロジェクト ID 参照を選択しません。                                                                                                   |
| プロジェクト管理および会計 | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 複数の資金調達ソースを持つ固定価格プロジェクトの **分割払** ページで、契約金額が間違っています。                                                                                                  |
| プロジェクト管理および会計 | [481443](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481443) | 固定価格プロジェクトの未収収益は、消去が転記された後も調整されません。                                                                                                                                |
| プロジェクト管理および会計 | [483209](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483209) | プロジェクトの受注書が仮発行請求書を通じて請求される場合、信用状ステータスが更新されません。                                                                                                  |
| プロジェクト管理および会計 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 発注書が請求され、請求書に調達カテゴリと品目が含まれている場合、顧客が間違ったアカウント情報を受け取ります。                                                                                              |
| プロジェクト管理および会計 | [484817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484817) | 定期的なバッチ ジョブを通じて生成されたプロジェクト仮発行請求書には、金額がゼロの重複トランザクションがあります。                                                                                                  |
| プロジェクト管理および会計 | [486817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486817) | プロジェクトの損益レポートの実行中にエラー制限チェックを削除します。                                                                                                                                  |
| プロジェクト管理および会計 | [488076](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488076) | **時間と材料のプロジェクトコード** で **郵送費** の機能を使用する際、会社間再請求で転記された費用は、使用時に損益エントリを表示しません。                                                         |
| プロジェクト管理および会計 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 固定価格プロジェクトの転記済みプロジェクト トランザクションの **請求書ステータス** フィルターが機能ません。                                                                                                   |
| プロジェクト管理および会計 | [488783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488783) | 代理人レコードが重複しているため、タイムシート エントリが重複します。                                                                                                                                           |
| プロジェクト管理および会計 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 逆見積もりの削除が **定期的** で機能しない。                                                                                                                                                 |
| プロジェクト管理および会計 | [498010](https://fix.lcs.dynamics.com/Issue/Details/?bugId=498010) | 範囲が追加されたとき、**プロジェクト管理と会計** モジュールの **トランザクションを調整する** オプションから適切なデータを選択できません。 **追加** フィルタが無視されます。                      |
| プロジェクト管理および会計 | [508494](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508494) | ジョブを記録した後、製造指示のステータスをリセットできません。                                                                                                              |
| プロジェクト管理および会計 | [509716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509716) | Project からの自動予約と生産可能在庫 (CTP) のある品目が予約されません。                                                                                                                      |
| プロジェクト管理および会計 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **会計調整** 機能は、**手動入力を許可しない** が選択された元帳勘定では問題が発生します。                                                                     |
| プロジェクト管理および会計 | [510079](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510079) | 見積もりが削除されたとき、プロジェクト明細書の **未収収益 - 販売額** フィールドに値が表示されてはいけません。                                                                                 |
| プロジェクト管理および会計 | [510607](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510607) | 役割の価格設定を使用したプロジェクト調整では、コストと販売価格が正しくありません。                                                                                                                        |
| プロジェクト管理および会計 | [10728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=10728) | Project Operations では、部分的に着手金を修正した後、着手金修正請求書が機能しません。                                                                                                                   |
| プロジェクト管理および会計 | [510743](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510743) | **リンクを削除** オプションは、会社間発注をキャンセルする場合にのみ有効にする必要があります。                                                                                                                                          |
| プロジェクト管理および会計 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 仕掛品 - 会社間プロジェクトで請求書に売上高を転記すると、予期しない取引先企業が選択されます。                                                                                                                  |
| プロジェクト管理および会計 | [514432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514432) | 仮発行請求書に訂正票用に選択された行が含まれている場合、請求ルールからの料金は再計算されません。                                                                                            |
| プロジェクト管理および会計 | [515820](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515820) | 連邦補助金の支出に関するお問い合わせのスケジュールには、プロジェクトの仮発行請求書が経費トランザクションに対して実行されていない場合、領収書の金額が表示されます。                                               |
| プロジェクト管理および会計 | [516301](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516301) | **残高** プロジェクト グループを持つサービス品目のプロジェクト明細書で、仕掛品 - コストが正しくありません。                                                                                               |
| プロジェクト管理および会計 | [516553](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516553) | プロジェクトに関連付けられている自由テキストの請求書を修正することはできません。                                                                                                                                                  |
| プロジェクト管理および会計 | [517074](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517074) | プロジェクト トランザクションを販売価格ゼロに調整すると、請求書ステータスが **請求不可** である請求書で調整された新しいトランザクションが作成さえｒます。                                                               |
| プロジェクト管理および会計 | [517414](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517414) | 複数の行を同時に調整している場合、プロジェクト調整の転記中に問題が発生します。                                                                                                                               |
| プロジェクト管理および会計 | [518001](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518001) | 梱包伝票の転記後に製品原価と品目所要量が変更された場合、調整が誤った原価額で転記されます。                                                                   |
| プロジェクト管理および会計 | [518092](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518092) | 直接配送発注の財務ディメンションが正しくないため、受注の財務ディメンションに置き換えられました。                                                              |
| プロジェクト管理および会計 | [518605](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518605) | 負の数量のプロジェクト仕訳行では、予測数量がゼロの場合、予測が更新されません。                                                                                        |
| プロジェクト管理および会計 | [518657](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518657) | Microsoft Excel を使用してアイテム要件をインポートすると、受領日エラーが発生します。                                                                                                                                                    |
| プロジェクト管理および会計 | [519200](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519200) | 請求書が転記されても、ベンダー請求書トランザクションへのプロジェクト品目トランザクション参照は更新されません。                                                                                               |
| プロジェクト管理および会計 | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | プロジェクトの仮発行請求書を転記すると、「事前請求書の控除が追加されたときに、報告通貨建てのトランザクション残高が正しくない」というエラーが発生する場合があります。                                                                    |
| プロジェクト管理および会計 | [520268](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520268) | プロジェクト レイアウトを使用する場合、プロジェクト ID とプロジェクト名は **ベンダーの支払いリテンション期間** レポートに自動入力されません。                                                                                              |
| プロジェクト管理および会計 | [520872](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | データ エンティティを介してプロジェクトが作成された場合、元帳転記の並べ替えの優先度が正しくありません。                                                                                                                      |
| プロジェクト管理および会計 | [521150](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521150) | ベンダー留保のある発注書に基づいて生成された転記済みプロジェクト トランザクションの原価金額が正しくありません。 これにより、プロジェクト明細書および固定価格プロジェクトのコスト管理で誤った値が生成されます。 |
| プロジェクト管理および会計 | [521374](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521374) | プロジェクトの販売見積で、ヘッダーが更新されたときに単価を誤って更新されます。                                                                                                                    |
| プロジェクト管理および会計 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations で着手金額を使用する場合、前払いの請求後に契約の既定プロジェクトを変更すると、後に控除額に問題が発生します。                                                                        |
| プロジェクト管理および会計 | [521857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521857) | ベンダーの請求書とプロジェクトの販売価格の請求日を更新することが変更されました。                                                                                                                                  |
| プロジェクト管理および会計 | [522897](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 為替レートが異なる会社間取引を調整すると、問題が発生します。                                                                                                                |
| プロジェクト管理および会計 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 品目要件と発注書の確定済みコストは、部分的な製品の受領と部分的な請求を伴う発注書の請求プロセスにおいて正しくありません。                                                |
| プロジェクト管理および会計 | [523960](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523960) | 見積もりが為替レートで取り消されると、誤った値が発生します。                                                                                                                                             |
| プロジェクト管理および会計 | [524242](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524242) | 時間単位の工数は、タスク レベルの WBS (作業分解構造) テンプレートで自動的にクリアされます。                                                                                                                         |
| プロジェクト管理および会計 | [524911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524911) | 見積もりのステータスを **失注** に更新すると、ステータスが **作成済み** または **送信済み** である、開始した全見積もりのステータスも **失注** に更新されます。                 |
| プロジェクト管理および会計 | [525182](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525182) | 納期が将来の場合、売上請求書は仮発行請求書に表示されません。                                                                                                                  |
| プロジェクト管理および会計 | [526180](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526180) | **プロジェクト品目仕訳行明細** エンティティのビジネス ロジックに変更があります。                                                                                                                                          |
| プロジェクト管理および会計 | [526522](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526522) | 会社間顧客請求書の未収収益が、タイムシートおよび外貨の再評価と一致しません。                                                                                 |
| プロジェクト管理および会計 | [526650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526650) | プロジェクト発注書行の納品リマインダーがプロジェクト購買依頼またはプロジェクトから作成された後、確定済み原価が誤って計算されます。                    |
| プロジェクト管理および会計 | [526812](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526812) | プロジェクトを調整すると、「在庫単位で財務データが更新されていません」というエラーが発生する場合があります。                                                                                                             |
| プロジェクト管理および会計 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations では、必要に応じて契約からプロジェクトを削除すると、契約の既定プロジェクトがリセットされます。                                                                                       |
| プロジェクト管理および会計 | [527945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527945) | 使用税を適用した場合、プロジェクトの費用の販売価格が間違っています。                                                                                                                                         |
| プロジェクト管理および会計 | [528020](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528020) | プロジェクト発注書の行が追加の請求書で更新されると、プロジェクト品目要件に誤った数量が転記されます。                                                                                                 |
| プロジェクト管理および会計 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations では、会社間請求書の **行を追加** リストに間違った経費明細行が表示されます。                                                                                                |
| プロジェクト管理および会計 | [529887](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529887) | 請求書登録と請求書承認を使用してトランザクションが転記されると、**プロジェクト転記トランザクション** ページでは **ベンダー勘定** のフィールドが空白です。                                                                  |
| プロジェクト管理および会計 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 元のプロジェクトの日付は調整で考慮されないため、**新しいプロジェクトの日付として調整日を使用する** が **いいえ** に設定されている場合、エラーが発生します。                                                                     |
| プロジェクト管理および会計 | [530241](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530241) | トランザクション通貨が会社通貨と異なる場合、プロジェクトに関連する一般仕訳帳および経費仕訳帳の販売価格が誤って計算されます。                                     |
| プロジェクト管理および会計 | [530658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530658) | プロジェクト発注書の部分請求書の伝票には、販売トランザクションが表示されません。                                                                                                                          |
| プロジェクト管理および会計 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | プロジェクト会計担当者とプロジェクト マネージャーの役割では、承認グループが設定された時間仕訳を作成できません。                                                                                                         |
| プロジェクト管理および会計 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Microsoft Excel を使ってインポートされた経費報告書は転記できません。                                                                                                                                                              |
| プロジェクト管理および会計 | [532106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532106) | **メッセージ** フィールドがアクティブではないため、タイムシート ポリシーを作成できません。                                                                                                                               |
| プロジェクト管理および会計 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 会社間シナリオで仕入先取引取消が許可されるという問題が発生します。 これは、ベンダー請求書と経費報告書の両方に当てはまります。                                                                                 |
| プロジェクト管理および会計 | [532692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532692) | 承認されたタイムシートの配布はリセットできません。                                                                                                                                                     |
| プロジェクト管理および会計 | [532843](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532843) | 時間仕訳と品目仕訳の為替レートで見積もりを取り消すと、誤った値が発生します。                                                                                                                  |
| プロジェクト管理および会計 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | プロジェクト調整では、間接費で売上金額が正しく更新されません。                                                                                                                              |
| プロジェクト管理および会計 | [534597](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534597) | 時間仕訳を転記すると、「ディメンション値が指定されていません」というエラー メッセージが表示されます。                                                                                                                                  |
| プロジェクト管理および会計 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 通貨が異なるプロジェクト契約では、伝票の会計通貨が正しく計算されません。                                                                                              |
| プロジェクト管理および会計 | [535652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535652) | 会社間タイムシート仕掛品転記に対して、間違った販売仕掛品勘定が使用されます。                                                                                                                                     |
| プロジェクト管理および会計 | [536536](https://fix.lcs.dynamics.com/Issue/Details/?bugId=536536) | 割引が適用され、倉庫が更新されると、プロジェクトの見積もりで価格が誤って計算されます。                                                                                                       |
| プロジェクト管理および会計 | [537905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537905) | プロジェクト トランザクションで品目原価調整が使用された後に再計算を実行すると、「エラーのため再計算が一時停止されています」というエラー メッセージが表示されます。                                                               |
| プロジェクト管理および会計 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540622) | 収益の発生時に取引を請求可能から請求不可に調整すると、総勘定元帳のエントリが作成されません。                                                                                              |
| プロジェクト管理および会計 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | プロジェクト ベンダー請求書保持機能である **コスト額の計算を有効にする** がオンの場合、**ProjTrans** が pay-when-paid (支払留保) では作成されません。                                             |
| プロジェクト管理および会計 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **仮発行請求書の作成** ページには複数の問題があります。                                                                                                                                                     |
| プロジェクト管理および会計 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations では、Project Operations と統合されている Finance 法人で **購入契約** ページが表示されません。                                                                                             |
| プロジェクト管理および会計 | [544132](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544132) | 高度な仕訳は、**会計日を次のオープン期間に自動設定** オプションがオンになっていても、決算日を使用してクローズ期間に転記することはできません。                                                |
| プロジェクト管理および会計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse 統合エラーが原因で、Project Operations で見積もりを成約に変換できません。                                                                                                                                       |
| プロジェクト管理および会計 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations では、重複する契約品目とトランザクション タイプがチェックされているため、契約品目をプロジェクト ID に関連付けようとするとエラー メッセージが表示されます。                                                |
| プロジェクト管理および会計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** は、別の顧客からの資金調達ソースの請求書住所を設定できます。                                                                                                             |
| プロジェクト管理および会計 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 10.0.15 アップデート後は、ページ上のリソースの標準ルックアップが使用できなくなります。                                                                                                                    |
| プロジェクト管理および会計 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | プロジェクト グループが **残高** に設定されている場合、総勘定元帳の元帳勘定と転記タイプが正しくなく、非在庫サービス品目の発注伝票の転記タイプが正しくありません。。                                 |
| プロジェクト管理および会計 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | **親アクティビティの選択をブロックする** が「いいえ」に設定されているのに、保留中のベンダー請求書の活動番号は表示されません。                                                                    |
| プロジェクト管理および会計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Project Operations では、トランザクションの転記請求書を作成するときにディメンションが選択されません。                                                                                                                   |
| プロジェクト管理および会計 | [442814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=442814) | プロジェクト管理と会計では、転送価格の優先順位が会社間タイムシートに正確に反映されていません。                                                                            |
| プロジェクト管理および会計 | [533530](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533530) | レガシーの WBS (作業分解構造) クラス メソッドである **ProjWBSUpdateController:: updateOutlineNumbersAndPublishInPreOrder** が非推奨となりました。                                                                                                   |

### <a name="regulatory-updates"></a>規制の更新
財務と運用アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、LCS にサインインし、問題検索ツールを使用して、予定されている規制の更新を表示することもできます。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
