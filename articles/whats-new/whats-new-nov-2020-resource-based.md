---
title: 2020 年 11 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオ向け Project Operations の 2020 年 11 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367272"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 年 11 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

- CDS 環境バージョン 4.4.0.70 での Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.14 でのプロジェクト管理および会計

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>リソース非在庫ベースのシナリオ向け Project Operations の更新

### <a name="project-operations-on-cds"></a>CDS での Project Operations

| 機能                 | 照合番号 | 品質更新プログラム                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  営業案件管理       | 2036993          | 見積行とリソース割り当て契約品目は、見積依頼明細行の種類が **すべてのタスク** である場合に、受注見積もりで更新されます。                                                 |
| 請求および価格設定          | 2070392          | **請求書トランザクションの更新** が選択されるたびに、請求書のプロジェクト契約品目が増加します。                                                                         |
| プロジェクト計画             | 2043336          | プロジェクト チーム メンバー レコードを削除できません。                                                                                                                                  |
| プロジェクト計画             | 2046013          | ロード中と時間フェーズ種類の変更時の見積もりタグ列の矛盾した動作。                                                                                   |
| プロジェクト計画             | 2046647          | プロジェクト チーム メンバーからリソース要件が生成されると、開始時間と終了時間が 1 時間ずれます。                                                                      |
| プロジェクト計画             | 2053879          | (今後の CDS ロールアウトごとに)   PublishUnassignedAssignments は、「ConditionOperator.In に渡された値が空です」 というエラーが発生すると、タスクの保存の試行を中断します。                       |
| プロジェクト計画             | 2055501          | **プロジェクトの開始日** を空のままにすると、スケジュールに失敗します。                                                                                                      |
| プロジェクト計画             | 2066817          | **タスク** タブでユーザー ピッカーを使用して、汎用リソースを作成することはできません。                                                                                                   |
| プロジェクト計画             | 2067034          | **詳細の表示** ボタンは **タスクの詳細** ページで利用できません。                                                                                                       |
| リソース管理          | 2046667          | すべてのリソースが満たされた後でも、汎用チーム メンバーは削除されません。                                                                                                    |
| 時間と簡易経費入力 | 2047499          | 時間エントリ ページの **新規** ボタンをクリックすると、**新しい電子メール署名** ページが開きます。                                                                                               |
| 時間と簡易経費入力 | 2059859          | 経費エントリを作成すると、予期しないポップアップが開きます。                                                                                                                         |
| その他                        | 2044181          | (発注書のアンインストール)   msdyn_ProjectServiceCore_Patch および msdyn Project Service のコア ソリューションをアンインストールしようとすると、「レコードは利用できません」 というエラーが発生します。  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計

| 機能        | 照合番号 | 品質更新プログラム                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 売上認識 | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | 契約が外貨を使用し、完了方法に作業進捗率を使用している場合、プロジェクト見積もりの達成率が正しくありません。                     |
| 売上認識 | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | **実績コスト** 完成度メソッドで見積もりを転記できません。                                                                                                    |
| 売上認識 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 会社基本通貨と取引通貨が異なる場合、伝票の不均衡エラーが原因で消去が失敗します。                                              |
| 経費管理  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | 管理者以外のユーザーの場合、**プロジェクト ID** と **経費カテゴリ** などの経費明細行列の検索値が、データ コネクタ フレームに正しく表示されません。 |
| 経費管理  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | 明細行プロパティの既定は、経費カテゴリには表示されません。                                                                                                         |
| 経費管理  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | 経費統合には、経費精算書から明細行プロパティを含める必要があります。                                                                                             |
| 請求           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | FD の組み合わせが検証されなかったことを示すエラー メッセージが原因で、プロジェクトの仮発行請求書を投稿できません。                                                    |
| 請求           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | **請求書** 詳細ページからのトランザクションを表示できません。                                                                                                              |
| 請求           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | 仮発行請求書の明細行は削除できます。                                                                                                                                  |
| プロジェクト会計  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **予測** メニュー項目は、**プロジェクト** 一覧ページに表示されません。                                                                                                   |
| プロジェクト会計  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **プロジェクト ステートメント**   > **トランザクションと予測** を開けません。                                                                                                       |
| プロジェクト会計  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **会計の調整** が、請求済みのプロジェクト トランザクションに対して有効になっていません。                                                                                                  |
| プロジェクト会計  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | **統合** 仕訳帳の転記時に、会計の詳細は **ProjCDSActualsImport** テーブルに含まれません。                                                  |
| プロジェクト会計  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | リソース割り当てを削除して再追加すると、プロジェクト予測エントリが 2 倍になります。                                                                            |
| プロジェクト会計  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | プロジェクト ID リンクを選択しても、CDS ディープ リンク URL は開きません。                                                                                                         |
| プロジェクト会計  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | CDS でタスクの開始日を更新できません。                                                                                                                           |
| プロジェクト会計  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | この機能を有効にすると、CDS 統合なしに複数の契約品目は不可能です。                                                                                   |

### <a name="regulatory-updates"></a>規制の更新
Finance and Operations アプリの規制の更新については、[規制の更新](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates) を参照してください。 また、LCS にサインインし、問題検索ツールを使用して、予定されている規制の更新を表示することもできます。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]