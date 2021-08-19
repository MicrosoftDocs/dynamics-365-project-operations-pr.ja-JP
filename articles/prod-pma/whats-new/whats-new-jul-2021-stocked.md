---
title: Project Operations 2021 年 7 月リリースの新機能、変更点 (在庫/本番ベースのシナリオ向け)
description: このトピックでは、2021 年 7 月にリリースされた Project Operations の在庫/本番ベースのシナリオで利用できる品質更新についての情報を提供します。
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992707"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Project Operations 2021 年 7 月リリースの新機能、変更点 (在庫/本番ベースのシナリオ向け)

_**適用対象:**  Project Operations (在庫/本番ベースのシナリオ向け)_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

- Dynamics 365 Finance 環境バージョン 10.0.20 でのプロジェクト管理および会計
 
### <a name="quality-updates"></a>品質更新プログラム
                                                                                                                                                                                  
| 機能                      | 照合番号| 品質更新プログラム                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| プロジェクト管理および会計 | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | 購買請求書からの原価コミットメント レコードは、購買請求書の発行から購買の受注が解除された時点でクリアされます。                                                                           |
| プロジェクト管理および会計 | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | 予算の検証は、購買の依頼で 2 回実施されます。 この重複により、購買依頼を閉じることができず、対応する発注書が作成されません。                                                                                                                        |
| プロジェクト管理および会計 | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | 課金ルールの **請求する割合** は、四捨五入の問題により、完了できませんでした。                                                                              |
| プロジェクト管理および会計 | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | トランザクションを調整する際に、パーセンテージに小数が含まれていると、原価と販売価格が正しく調整されません。                                      |
| プロジェクト管理および会計 | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | 会計ソースのエクスプローラでは、異なるアクティビティを持つ複数のタイムシート明細行に対して、1 つのタイムシート明細行の時間が表示されます。                                      |
| プロジェクト管理および会計 | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | 保存されたビューとタイムシート明細行の詳細をパーソナライズすることにより、タイムシートを開こうとすると、常にリストの最初のタイムシートの詳細が開かれるという問題がありました。  |
| プロジェクト管理および会計 | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | インポートすると、プロジェクトのルート ノードが消え、WBS (作業分解構造) のレコードが削除される。                                                                                             |
| プロジェクト管理および会計 | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | 品目の要求から部分的にアイテムが入出庫されると、システムが間違った予算の消費残高を更新する。 |
| プロジェクト管理および会計 | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | プロジェクトの保持発注書が、**合計** ペインや **保留中の請求書** グリッドに正しく合計が表示されない場合がある。                                                                  |
| プロジェクト管理および会計 | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | 棚卸資産の決算時に、プロジェクト アイテムの原価調整が損益計算書ではなく貸借対照表に計上される。                                                            |
| プロジェクト管理および会計 | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | プロジェクトの計上された取引伝票や見積伝票で、会計の通貨に USD (米国ドル) が使用されている場合でも、金額に CAD (カナダドル) など別の通貨が表示される。              |
| プロジェクト管理および会計 | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | 品目の要件と発注書のあるコミット コストで、一部製品受領と一部請求書発行のある発注書請求書処理が間違っている。       |
| プロジェクト管理および会計 | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | プロジェクト調整で、間接費を使った場合に売上金額が正しく更新されない。                                                                                    |
| プロジェクト管理および会計 | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **タイムシート** テーブルに、**Worker/リソース** ビューとの定義された関連付けが見つからない。                                                                                   |
| プロジェクト管理および会計 | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | 会社間のタイムシートで **アクティビティ番号** をドロップダウン メニューから選択すると、アクティビティ番号フィールドが入力できない。                                                                 |
| プロジェクト管理および会計 | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | 次のページには、パーソナライズされた **目的** や **アクティビティの説明** フィールドを追加することはできません: **プロジェクト転記トランザクション**、**請求書提案の作成**、**請求書提案**。  |
| プロジェクト管理および会計 | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | データ管理 (**ProjSalesItemRequirementEntity**) を使用してアイテムの要件を作成すると、誤った納期管理が行われる。                                              |
| プロジェクト管理および会計 | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Finance でプロジェクト契約 ID を選択すると、Project Operations の統合環境では、既存のプロジェクト契約ではなく、新規レコードを作成するページが開く。                                                                                                                 |
| プロジェクト管理と会計 | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  ラベル、「@SYS4083080」 (「入力された値に対応する一意のワーカー レコードが見つかりません」) がデンマーク語に翻訳されていない。                                |
| プロジェクト管理および会計 | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | **品目の消費税グループ** フィールドが請求書提案で編集できない。                                                                               |
| プロジェクト管理および会計 | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | 確定費用が、損金不算入の税金額で過大計上されてしまう。                                                                                                    |
| プロジェクト管理および会計 | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | 複数のプロジェクトと異なる財務分析コードを持つ企業間のタイムシートを転記すると、総勘定元帳に予期しない値が発生する場合がある。                             |
| プロジェクト管理および会計 | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | 定期的なプロセスである **ステージングからのインポート** が同時に複数回実行されるため、請求書の提案行が重複してしまう。                                      |
| プロジェクト管理および会計 | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | クレジット ノートの請求書案の転記にエラーがあり、伝票上の取引が整合しない。    |
| プロジェクト管理および会計 | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | 保留中のた請求書が解除された後、プロジェクトのコミット済みコストが不正確になる。                                                                             |
| プロジェクト管理と会計 | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | 税額が会社の通貨と異なる通貨である場合、プロジェクトの売上注文にクレジット ノートを作成できない。                                      |
| プロジェクト管理および会計 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 契約を削除すると、顧客に関連するアドレスも削除される。                                                                                     |
| プロジェクト管理および会計 | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | マイナスの時間トランザクションの修正に起因する請求書の提案が転記できない。                                                                    |
| 出張と経費                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | 経費報告書で税金の計算方法が異なる。                                                                                                                  |
| 出張と経費                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | リリース アップデート **DB72_Expense.updateTrvExpTransProjTransId()** が **trvExpTrans.ReferenceDataAreaId** に新しい数列を作成を許可しない。                    |
| 出張と経費                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | 必須項目に、申告額が表示されない。                                                                                                             |
| 出張と経費                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Expense Reimagined のユーザー インターフェースを使って、経費報告書に経費を添付する際のパフォーマンスが向上しています。                                                            |
| 出張と経費                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | 転記された経費報告書が削除可能となっています。                                                                                           |
| 出張と経費                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | 経費ポリシーのメッセージが複数回表示される。                                                                                                       |
| 出張と経費                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | **支払い方法** フィールドが **新しい費用** ペインに含まれている。                                                                                                      |
| 出張と経費                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | **経費ドキュメントの状態をリセットする** ツールで、ワークフローが見つからなかった場合、経費報告書のステータスを **下書き** にリセットするようにしました。 

### <a name="regulatory-updates"></a>規制の更新
Finance and Operations アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、Lifecycle Services (LCS) にログインし、問題検索ツールを使用して、計画されている規制の更新を確認することも可能です。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
