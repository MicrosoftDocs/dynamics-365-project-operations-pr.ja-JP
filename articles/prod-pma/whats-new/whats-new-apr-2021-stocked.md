---
title: 2021 年 4 月の最新情報または変更事項 - 在庫/製造ベースのシナリオ向け Project Operations
description: このトピックは、在庫/製造ベースのシナリオ向け Project Operations の 2021 年 4 月リリースで利用可能な品質アップデートに関する情報を提供します。
author: andchoi
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 42b4da3a77d56891454d094cd771575ff9bff081
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589616"
---
# <a name="whats-new-or-changed-in-project-operations-april-2021-for-stockedproduction-based-scenarios"></a>2021 年 4 月の最新情報または変更事項 - 在庫/製造ベースのシナリオ向け Project Operations

_**適用対象:** 在庫/製造ベースのシナリオ向け Project Operations_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

- Dynamics 365 Finance 環境バージョン 10.0.18 でのプロジェクト管理と会計
 
### <a name="quality-updates"></a>品質更新プログラム
                                                                                                                                                                                  
| 機能                      | 照合番号| 品質更新プログラム                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| プロジェクト管理および会計 | [534393](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534393) | **プロジェクトの並べ替え** グリッドでエラーが発生します。                                                                                                                                                      |
| プロジェクト管理および会計 | [542850](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542850) | プロジェクトの発注書で単価や数量を修正すると、コミットされた金額が過大になってしまう。                                                                                    |
| プロジェクト管理および会計 | [543645](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543645) | **ProjParameters** 変数は宣言されているが、使用前にレコードバッファが割り当てられない。                                                                                     |
| プロジェクト管理および会計 | [543674](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543674) | **ResRollup** テーブルが削除されると、**すべての企業にプロジェクト リソースを投入する** バッチジョブが実行される。                                                                          |
| プロジェクト管理および会計 | [544417](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544417) | **受注明細 V2** エンティティを使用している購買オーダーの **プロジェクト販売価格** フィールドを更新すると、問題が発生する。                                                                           |
| プロジェクト管理および会計 | [547652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547652) | ID 番号によっては、サブ プロジェクトを作成できない場合がある。   「Function Global:: int642int が誤って呼び出されました」 というエラーが発生する。                                         |
| プロジェクト管理および会計 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 調達先のカテゴリーと品目が同一の発注書を請求書に記載すると、顧客に誤った勘定科目が届く。                                                                      |
| プロジェクト管理および会計 | [509920](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509920) | 間接費を含むプロジェクトのトランザクションを、請求可能から請求不可能に調整し、再び請求可能に戻すと、WIP が正しく削除されない。                                       |
| プロジェクト管理および会計 | [511274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511274) | 売上明細書でリテンション期間と合計割引を使用すると、請求書の金額が正しくない。                                                                                          |
| プロジェクト管理および会計 | [511315](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511315) | 別のトランザクション タイプを選択しても、明細のアドレス名が変更されない。                                                                           |
| プロジェクト管理および会計 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 部分的の製品の受領と部分的の請求書の発行を伴う発注書の請求プロセスにおいて、品目の要件と発注書を持つコミットされたコストが正しくない。                       |
| プロジェクト管理および会計 | [524226](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524226) | プロジェクトの財務分析コードが変更された場合、発注書ヘッダーにその変更が反映されない。                                                                                                  |
| プロジェクト管理および会計 | [524979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524979) | 生成された **固定価格のプロジェク** トレポートが空白になっている。                                                                                                         |
| プロジェクト管理および会計 | [529445](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529445) | **請求額の受領時に支払う** ページでベンダーの請求書を確認した際に、請求書がプロジェクト ID の参照を選択していない。                                                                          |
| プロジェクト管理および会計 | [529982](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529982) | **人事マネージャー** ロールで 1 つの法人に対するアクセスが制限されているユーザーの場合、カテゴリが正しく既定として設定されていないため、タイムシートの入力が正しく行われない。                                         |
| プロジェクト管理および会計 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 元のプロジェクトの日付が調整に考慮されていないため、**新しいプロジェクトの日付に調整日を使用する** フィールドが **いいえ** に設定されているとエラーが発生する。                                             |
| プロジェクト管理および会計 | [530788](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530788) | バッチを使用してプロジェクトの見積もりを計算すると、結果が正しくない。                                                                                                         |
| プロジェクト管理および会計 | [530834](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530834) | プロジェクト契約上の支出額と、プロジェクト上の当座預金額が一致していない。                                                                             |
| プロジェクト管理および会計 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | プロジェクト会計担当者とプロジェクト マネージャーの役割で、承認グループが設定された時間仕訳を作成できない。                                                                                 |
| プロジェクト管理および会計 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Microsoft Excel のインポートした経費仕訳帳を転記できない。                                                                                                                                       |
| プロジェクト管理および会計 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | ベンダーの請求書や経費報告書など、会社間シナリオからのベンダー トランザクション取消が許可できてしまう。                                                                     |
| プロジェクト管理および会計 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | プロジェクトの調整で、間接費で売上金額が正しく更新されない。                                                                                                    |
| プロジェクト管理および会計 | [534869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534869) | 固定価格のプロジェクト請求書のクレジット ノートが作成され、その請求ルールに納品単位が使用されている場合、リリースされた単位を再請求に利用できない。 |
| プロジェクト管理および会計 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 通貨が異なるプロジェクト契約では、項目仕訳や請求書案で会計通貨が正しく計算されない。                                                   |
| プロジェクト管理および会計 | [537158](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537158) | 購買発注明細のプロジェクトを変更して、品目の要求を転送できる。                                                                                                                          |
| プロジェクト管理および会計 | [540603](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540603) | 予測からプロジェクト予算にインポートすると、金額が正しくない。                                                                                                                    |
| プロジェクト管理および会計 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5406222) | 請求可能な取引から請求不可能な取引に調整する際に、総勘定元帳のエントリが作成されない。                                                                                            |
| プロジェクト管理および会計 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 機能キー **プロジェクトベンダーの請求書保持期間のコスト計算機能の有効化** がオンになっている場合、プロジェクト取引は 「請求額の受領後の支払い」 で作成されません。                  |
| プロジェクト管理および会計 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **仮発行請求書の作成** ページに複数の問題がある。                                                                                                                             |
| プロジェクト管理および会計 | [543390](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543390) | **すべてのプロジェクト** ページに新しい言語コードのリストが表示されない。                                                                                                            |
| プロジェクト管理および会計 | [543803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543803) | 予算を 2 回以上修正した場合、プロジェクト予算残高の未承認予算額が正しくない。                                                                |
| プロジェクト管理および会計 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations と統合されている Finance の法人で **購入契約** ページが表示されない。                                                                               |
| プロジェクト管理および会計 | [545456](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545456) | 正しい伝票の日付がプロジェクト時間の仕訳行にアップロードされない。                                                                                                            |
| プロジェクト管理および会計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | リソース ベースのシナリオの Project Operations では、統合エラーのために見積を成約に変換できない。                                                                      |
| プロジェクト管理および会計 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations, では、契約品目とトランザクションタイプの重複をチェックするため、契約品目とプロジェクト ID の関連付けを作成しようとすると、エラーメッセージが表示されます。                        |
| プロジェクト管理および会計 | [546949](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546949) | **ProjValEmplProjSetup** テーブルに 14,000 を超えるレコードがある場合、**リソース/プロジェクト検証グループ** ページのパフォーマンスの問題が発生する。                                                                     |
| プロジェクト管理および会計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** は、資金調達ソースとなる請求書の宛先を別の顧客から設定することができてしまう。                                                                                   |
| プロジェクト管理および会計 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 10.0.15 へのアップデート後は、ページ上のリソースの標準ルックアップが使用できなくなる。                                                                                          |
| プロジェクト管理および会計 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 発注書請求書伝票の元帳勘定と転記タイプがサービス項目と一致していない。 プロジェクト グループが **残高** に設定されており、元帳の勘定科目が間違っている。                   |
| プロジェクト管理および会計 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | 保留中のベンダーの請求書について、**親アクティビティの選択をブロックする** が **いいえ** に設定されているにもかかわらず、アクティビティ番号が表示されない。                                            |
| プロジェクト管理および会計 | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | ナビゲーション パスに **プロジェクト** > **予算** > **改訂** > **新規** > **インポート** を使用すると、システムがすべてのプロジェクトに対してプロジェクト予算の修正を作成してしまう。                                                            |
| プロジェクト管理および会計 | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) | 異なる取引通貨と会計通貨で取引を調整すると、誤った転記と総勘定元帳の入力が発生する。                                                                        |
| プロジェクト管理および会計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | トランザクションの転記請求書を作成する際に、分析コードが含まれない。                                                                                                   |
| プロジェクト管理および会計 | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | 保留中のベンダー請求書の作成時に **PurchTotals.purchNewTotalAmount()** メソッドが呼び出されるが、この請求書は発注書とリンクしていないため、パフォーマンスに問題がある。                    |
| 出張と経費                | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | マイルの設定に関する転記エラーが発生する。                                                                                                                                          |
| 出張と経費                | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | 外貨建ての経費処理を **個人に分割** できない。                                                                                                         |
| 出張と経費                | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | **代行** がリソースとして設定されているかどうかを問わず、経費カテゴリーのドロップダウン メニューに誤ったカテゴリーが表示される。                                         |
| 出張と経費                | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | リソース/カテゴリーの検証エラーが発生し、会社間取引の経費レポートを保存できない。                                                                                             |
| 出張と経費                | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 経費報告書の転記でのマイレージ率の計算が間違っていると、行が分割されてしまう。                                                                                                        |
| 出張と経費                | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 消費税が含まれていて、支払い方法のオフセット勘定タイプが **作業者** の場合、会社間の経費報告書を転記できない。                                                   |
| 出張と経費                | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | **TrvRequisitionLine** データのエンティティと、そのエンティティに関連付けられた一意のインデックスの変更がロールバックされる。                                                                                            |
| 出張と経費                | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 経費報告書の特定の箇所にログを追加し、ソース ドキュメント ラインの作成と更新をサポートします。                                                                                           |
| 出張と経費                | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 販売先の法人に売上税が計上されている場合、会社間のシナリオでは、間違った補助元帳仕訳が表示される。                                              |
| 出張と経費                | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations で、Dataverse から削除されても Finance からは経費の見積もりが削除されない。                                                                                         |
| 出張と経費                | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 経費カテゴリが非プロジェクト カテゴリの場合、**経費** ページで選択された財務ディメンションは経費報告書にコピーされない。                                          |

### <a name="regulatory-updates"></a>規制の更新
財務と運用アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、LCS にサインインし、問題検索ツールを使用して、予定されている規制の更新を表示することもできます。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
