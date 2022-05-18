---
title: 2021 年 9 月の新機能と変更点 - 在庫/製造ベースのシナリオ向け Project Operations
description: このトピックは、在庫/製造ベースのシナリオ向け、 Project Operations の 2021 年 9 月リリースで利用可能な品質更新に関する情報を提供します。
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582026"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>2021 年 9 月の新機能と変更点 - 在庫/製造ベースのシナリオ向け Project Operations

_**適用対象:**  Project Operations (在庫/本番ベースのシナリオ向け)_

このトピックは、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます:

- Dynamics 365 Finance 環境バージョン 10.0.21 でのプロジェクト管理と会計
 
## <a name="quality-updates"></a>品質更新プログラム

| 機能 | 照合番号 | 品質更新プログラム |
|---|---|---|
| プロジェクト管理および会計 | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | 購入マネージャーの役割に 1 つの法人へのアクセスを許可すると、すべての法人のすべてのプロジェクトへのアクセス件も付与される。 |
| プロジェクト管理および会計 | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | 付加価値税 (VAT) の丸め問題は、クレジット ノートが元のプロジェクトの請求書に対して決済される際に発生します。 |
| プロジェクト管理および会計 | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | 予算の検証には、代替のプロジェクト予算を使用します。 |
| プロジェクト管理および会計 | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | プロジェクトの見積書の WBS (作業分解構造)上で、**販売価格時間** の価格グループが計算されない。 |
| プロジェクト管理および会計 | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | **見積もりの計算にプロジェクトの契約通貨を使用する** 機能が有効な場合、見積もりの消去に失敗することがあります。 |
| プロジェクト管理および会計 | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | プロジェクト経費仕訳の消費税グループで使用税を使用した場合、数量による消費税の因数分解が販売価格の金額に加算されます。 |
| プロジェクト管理および会計 | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | 購買発注書の請求書にベンダー留保や前払いを適用した場合、最後の支払いに対して条件付きの税金が正しく計算されない。 |
| プロジェクト管理および会計 | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | 調整トレースは、期首残高仕訳では機能しません。 |
| プロジェクト管理および会計 | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **期間別のプロジェクト予算修正配分** が、すべての予算期間に分割されてしまう。 割り当てが送信されたときに、レコードがクリアされない。 |
| プロジェクト管理および会計 | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | 総勘定元帳への仕掛品 (WIP) の転記額が正しくない。 |
| プロジェクト管理および会計 | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | プロジェクトの時間仕訳の承認が機能しない。 |
| プロジェクト管理および会計 | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | 資金制限がマークされていない場合、プロジェクト調整の販売価格が間接費で更新されない。 |
| プロジェクト管理および会計 | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | 売上テーブルのヘッダーが請求書を発行しており、既存の行の裏付けとなる注文書が確定している場合、品目の要件を作成できない。 |
| プロジェクト管理および会計 | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | 別のプロジェクトにマイルストーンを設定した請求ルールの保持金額が、マイルストーンに選択された対応するプロジェクト ID に転記されない。 代わりに、最初のプロジェクトに転記されてしまう。 |
| プロジェクト管理および会計 | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | 請求書の提案書で **財務ディメンションセット** を選択すると、次のようなエラーが発生します: 「'Dynamics.AX.Application.FormIntControl' のオブジェクトを 'Dynamics.AX.Application.FormStringControl' にキャストできません」 |
| プロジェクト管理および会計 | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **プロジェクトの請求書** レポートは行をスキップします。 |
| プロジェクト管理および会計 | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | 投資プロジェクトのコスト管理を計算すると、エラーが発生する。 |
| プロジェクト管理および会計 | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable-canDeletePostalAddress** メソッドがパフォーマンスの問題を引き起こす。 |
| プロジェクト管理および会計 | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | エラーメッセージは、「予期しないエラー」よりも明確なものでなければなりません |
| プロジェクト管理および会計 | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | プロジェクトの請求書転記バッチジョブが、請求書明細が生成されていなくても請求書案を処理して転記する。 |
| プロジェクト管理および会計 | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | 公共部門のライセンス設定キーをオフにすると、丸めの問題が発生する。 複数のァンディング ソースがある契約のタイムシート時間に、誤った原価または販売価格が生成される。 |
| プロジェクト管理および会計 | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | 販売価格モデルが **寄与率** の場合、請求書を発行したプロジェクト発注書のプロジェクト販売価格が正しく計算されない。 |
| プロジェクト管理および会計 | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | システムが従業員の実効労務単価を計算する際に、その間の稼働日を考慮しない。 |
| プロジェクト管理および会計 | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | 次の検証エラーが原因で、企業間タイムシートに転記エラーが発生する: 「法人に対して取引先が設定されていません」 |
| プロジェクト管理および会計 | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | 転記されたプロジェクトのトランザクション リストに、支出カテゴリーを持つ注文書の説明が取り込まれない。 |
| プロジェクト管理および会計 | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | プロジェクトに計上される品目の仕訳に誤った変換が発生する。 |
| プロジェクト管理および会計 | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | 限度額を超えていても発注書を確認することができてしまう。 |
| プロジェクト管理および会計 | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | プロジェクト ID を選択すると、フリーテキストの **請求書の訂正/取消** フィールドが消える。 |
| プロジェクト管理および会計 | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | 在庫のある品目を含むプロジェクトの受注からプロジェクトの請求書案を転記すると、パフォーマンスの問題が発生する。 |
| プロジェクト管理および会計 | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | 次のようなエラーが発生し、プロジェクトの購入請求書を計上できない: 「関数 AccDistProcessorProjectExtension.createForProjectRevenueLine が不正に呼び出されました」 |
| プロジェクト管理および会計 | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | 複数のサブタスクの実行をサポートするプロジェクト見積もりのバッチジョブの作成を更新します。 |
| プロジェクト管理および会計 | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | ワークフローが **キャンセル** された状態では、タイムシートのステータスを **ドラフト** に更新できない。 |
| プロジェクト管理および会計 | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | 複数の行が存在する場合、クレジット ノートの請求書案で保持金額が計算されない。 |
| プロジェクト管理および会計 | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | 購買発注書から生成された請求書の金額を変更しようとすると、以下のエラーが発生する: 「伝票上のトランザクションが XX/XX/XXXX に従ってバランスが取れていません」。 (会計通貨: 0.00 - 報告通貨: 0.01)。" |
| プロジェクト管理および会計 | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | プロジェクトの請求書案をバッチモードで投稿すると、**GeneralJournalAccountEntry** との結合に起因する、パフォーマンスの問題が発生する。 |
| プロジェクト管理および会計 | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | タイムシートが転記されると、パフォーマンスの問題が発生する。 |
| プロジェクト管理および会計 | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | すべてのタスクが展開された後、または単一のタスクが手動で展開された後に、作業内訳構造のコスト見積もり階層が正しく調整されない。 |
| プロジェクト管理および会計 | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | プロジェクト見積書の Excel テンプレートを **Excelで開く** メニューに追加することができない。 |
| プロジェクト管理および会計 | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | 印刷されたプロジェクトの請求書に、法人の非課税番号が記載されていない。 |
| プロジェクト管理および会計 | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | クレジットの明細に関連してプロジェクトが調整されても、在庫単位のエラーで財務データが更新されない。 |
| プロジェクト管理および会計 | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | KB 461935 を適用した後、連続した数字の配列に切り替えると、見積もりを転記できなくなる。 |
| プロジェクト管理および会計 | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** は、Android 用プロジェクト タイムシート モバイル アプリが応答しなくなる原因となります。 |
| プロジェクト管理および会計 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 請求書の転記による WIP の反転値が、時間入力による元の転記された WIP の値と異なる。 |
| プロジェクト管理および会計 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 適用されたリテイナーのケースでは、プロジェクトの請求書による収入が計上されたときに、伝票上のトランザクションのバランスが正しく取れていない。 |
| プロジェクト管理および会計 | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | **プロジェクトのリソース スケジュールのパフォーマンス向上機能** を有効にすると、リソースの可用性とキャパシティの 10 進数の値が正しく丸められない。 |
| プロジェクト管理および会計 | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | いつ **複数のバッチタスクを使用してプロジェクトの見積もりを作成する** 機能が有効になっている場合、複数のサブタスクを持つバッチでの見積もりの作成は、現在の期間でのみ機能します。 |
| 出張と経費 | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | 出張見積書のポリシーが無視され、ワークフローがエラーなく承認されてしまう。 |
| 出張と経費 | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobile Expense アプリで、経費明細に以下の情報が保存されない:</p><ul><li>プロジェクト ID</li><li>経費が請求可能かどうか</li><li>活動の番号</li></ul> |
| 出張と経費 | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | **添付領収書** フィールドが、経費明細に領収書が添付されていない場合でも **はい** に設定される。 |
| 出張と経費 | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | 支出のカテゴリーを **個人** に変更すると、エラーが発生する。 |
| 出張と経費 | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | クレジットカード決済を個人の経費に分割した後、領収書を添付して親の経費を編集できなくなる。 |
| 出張と経費 | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | プロジェクト ID を持つ企業間取引の費用ポリシーが正しく機能しない。 |
| 出張と経費 | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | 転記された経費報告書の転記日情報が欠落している。 |
| 出張と経費 | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | 経費モバイル アプリで支払い方法の問題が発生する。 |
| 出張と経費 | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | ある作業者のために作成された出張依頼書を、委任日以前の別の作業者の経費報告に使用できてしまう。 |
| 出張と経費 | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | 経費の作成時に、財務ディメンションの値の変更が、**経費管理** ワークスペースの会計分配レベルで正しく更新されない。 |
| 出張と経費 | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | 主な経費明細の承認状況が、明細明細ワークフローの承認票強と同期しない。 |
| 出張と経費 | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | 経費報告書を転記し、税金の回収が有効になっている場合、エラーが発生する。 |
| 出張と経費 | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | 代理人は、退職した従業員の経費書類を削除することはできません。 |
| 出張と経費 | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | 経費明細の削除は予想よりも時間がかかり、パフォーマンスに影響する。 |
| 出張と経費 | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** は、**SourceDocumentLine** のみを削除するため、孤立した **TaxUncommitted** レコードが発生する。 |
| 出張と経費 | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** が **trvExpTrans.ReferenceDataAreaId** を尊重せず、新しい数字の配列を作成する。 |

## <a name="regulatory-updates"></a>規制の更新

財務と運用アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、課題検索ツールを使用して、予定されている規制の更新を確認することもできます。 問題検索では、国や地域、機能の種類、リリースなどで検索することができます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
