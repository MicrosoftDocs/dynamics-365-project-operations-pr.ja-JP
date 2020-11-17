---
title: ビジネス トランザクション
description: このトピックでは、ビジネス トランザクションに関する情報を提供します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d82f5d75de69b32b39c9a55d77287c0719930eb4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079390"
---
# <a name="business-transactions"></a>ビジネス トランザクション

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation で *ビジネス トランザクション* は、どのエンティティでも表現されない抽象的な概念です。 ただし、エンティティの一部の一般的なフィールドとプロセスは、ビジネス トランザクションの概念を使用するように設計されています。 次のエンティティはこの抽象化を使用します:

- 見積依頼明細行の詳細
- 契約品目の詳細
- 見積もり行
- 仕訳帳明細行
- [実績]

これらのエンティティのうち、見積品目の詳細、契約品目の詳細、見積品目は、プロジェクト ライフサイクルの見積フェーズにマップされます。 仕訳帳明細行と実績エンティティは、プロジェクト ライフサイクルの実行フェーズにマップされます。

PSA はこれら 5 つのエンティティ レコードをビジネス トランザクションとして扱います。 唯一の違いは、見積もりフェーズにマップされたエンティティ レコードが財務予測と見なされることです。一方、実行フェーズにマップされたエンティティ レコードは、すでに発生した財務上の事実と見なされます。

詳細については、[見積もり](estimates.md) と [実績](actuals.md) を参照してください。

## <a name="concepts-that-are-unique-to-business-transactions"></a>ビジネス トランザクションに固有の概念
以下の概念は、ビジネス トランザクションの概念に固有です:

- トランザクションの種類
- トランザクション クラス
- トランザクション発生元
- トランザクション接続

### <a name="transaction-type"></a>トランザクションの種類

トランザクションの種類は、プロジェクトへの財務的影響のタイミングとコンテキストを表します。 これは PSA がサポートする次の値を持つオプション セットで表されます。
- コスト
- プロジェクト契約
- 未請求売上
- 請求済み売上
- 組織間営業
- リソース単位原価

### <a name="transaction-class"></a>トランザクション クラス

トランザクション クラスは、プロジェクトで発生するさまざまな種類のコストを表します。 これは PSA がサポートする次の値を持つオプション セットで表されます。

- Time
- 経費
- 材料
- 料金
- マイルストーン
- 税額

**マイルストーン** の値は通常、PSA の固定価格請求のビジネス ロジックで使用されます。

### <a name="transaction-origin"></a>トランザクション発生元

トランザクションの起点は、各ビジネス トランザクションの起点を格納するエンティティです。 プロジェクトの実行が開始されると、各ビジネス トランザクションは別のビジネス トランザクションを生成し、順次ビジネス トランザクションが作成されていきます。 トランザクションの起点エンティティは、各トランザクションの起点に関するデータを格納し、レポート作成と追跡可能性を容易にするよう設計されています。 

### <a name="transaction-connection"></a>トランザクション接続

コストや関連する販売実績、または請求書の確認や請求書の修正などの請求アクティビティによってトリガーされる取引の取り消しなど、トランザクション接続は 2 つの類似したビジネス トランザクション間の関係を格納するエンティティです。

トランザクションの起点とトランザクション接続を組み合わせることにより、ビジネス トランザクションと特定のビジネス トランザクションの作成につながったアクションとの関係を追跡できます。

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>例: トランザクションの起点とトランザクション接続との連携

次の例は、PSA プロジェクトのライフサイクルにおける時間エントリの一般的な処理を示しています。

> ![Project Service ライフサイクルの処理時間エントリ](media/basic-guide-17.png)
 
1. 時間エントリを送信すると、2 つの仕訳入力が作成されます。1 つはコスト用、もう 1 つは未請求販売用です。
2. 時間入力の最終承認により 2 つの実績が作成されます。1 つはコスト用、もう 1 つは未請求販売用です。
3. ユーザーがプロジェクト請求書を作成すると、未請求の販売実績のデータを使用して請求明細行トランザクションが作成されます。 
4. 請求書が確認されると、2つの新しい実績が作成されます。1 つは未請求の販売取り消しと、もう 1 つ請求済み販売実績です。

これらの各イベントは、トランザクション起点のレコードの作成をトリガーします。そしてトランザクション接続エンティティは、時間エントリ、仕訳帳明細行、実績、請求書明細行の詳細にわたって作成されたこれらのレコード間の関係の追跡を構築するのに役立ちます。

次の表は、前述のワークフローのトランザクション起点エンティティのレコードを示しています。

| イベント                        | 発生元                   | 発生元の種類                       | トランザクション                       | トランザクションの種類         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| 時間エントリの送信        | 時間エントリ レコードの GUID   | 時間入力                        | 仕訳帳明細行レコードの GUID (コスト)    | 仕訳帳明細行             |
| 時間エントリ レコードの GUID       | 時間入力               | 仕訳帳明細行レコードの GUID (販売)  | 仕訳帳明細行                      |                          |
| 承認時間                | 仕訳帳明細行レコードの GUID | 仕訳帳明細行                      | 未請求の販売レコードの GUID        | 実績                   |
| 時間エントリ レコードの GUID       | 時間入力               | 未請求の販売レコードの GUID        | 実績                            |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | コスト実績レコードの GUID           | 実績                            |                          |
| 時間エントリ レコードの GUID       | 時間入力               | コスト実績レコードの GUID           | 実績                            |                          |
| 請求書の作成             | 時間エントリ レコードの GUID   | 時間入力                        | 請求書明細行トランザクションの GUID     | 請求書明細行トランザクション |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | 請求書明細行トランザクションの GUID     | 請求書明細行トランザクション          |                          |
| 請求書の確認         | 請求書明細行の GUID        | 請求明細行                      | 請求済み販売レコードの GUID          | 実績                   |
| 請求書の GUID                 | 請求書                  | 請求済み販売レコードの GUID          | 実績                            |                          |
| 請求明細行の詳細の GUID     | 請求明細行の詳細      | 請求済み販売レコードの GUID          | 実績                            |                          |
| 時間エントリ レコードの GUID       | 時間入力               | 請求済み販売レコードの GUID          | 実績                            |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | 請求済み販売レコードの GUID          | 実績                            |                          |
| 時間エントリ レコードの GUID       | 時間入力               | 未請求の販売取消の GUID      | 実績                            |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | 未請求の販売取消の GUID      | 実績                            |                          |
| 下書きの請求書修正     | 古い ILD GUID             | 請求書明細行トランザクション          | 修正 ILD GUID               | 請求書明細行トランザクション |
| 古い IL GUID                  | 請求明細行             | 修正 ILD GUID               | 請求書明細行トランザクション          |                          |
| 古い請求書の GUID             | 請求書                  | 修正 ILD GUID               | 請求書明細行トランザクション          |                          |
| 時間エントリ レコードの GUID       | 時間入力               | 修正 ILD GUID               | 請求書明細行トランザクション          |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | 修正 ILD GUID               | 請求書明細行トランザクション          |                          |
| 確認済みの請求書修正 | 古い ILD GUID             | 請求書明細行トランザクション          | 請求済み販売実績の逆仕訳の GUID | 実績                   |
| 古い IL GUID                  | 請求明細行             | 請求済み販売実績の逆仕訳の GUID | 実績                            |                          |
| 古い請求書の GUID             | 請求書                  | 請求済み販売実績の逆仕訳の GUID | 実績                            |                          |
| 時間エントリ レコードの GUID       | 時間入力               | 請求済み販売実績の逆仕訳の GUID | 実績                            |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | 請求済み販売実績の逆仕訳の GUID | 実績                            |                          |
| 古い ILD GUID                 | 請求書明細行トランザクション | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 古い IL GUID                  | 請求明細行             | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 古い請求書の GUID             | 請求書                  | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 時間エントリ レコードの GUID       | 時間入力               | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 修正 ILD GUID          | 請求書明細行トランザクション | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 修正 IL GUID           | 請求明細行             | 新しい未請求の販売実績の GUID    | 実績                            |                          |
| 請求書の修正の GUID      | 請求書                  | 新しい未請求の販売実績の GUID    | 実績                            |                          |

次の表は、前述のワークフローのトランザクション接続エンティティのレコードを示しています。

| イベント                          | トランザクション 1                 | トランザクション 1 のロール | トランザクション 1 の種類           | トランザクション 2                | トランザクション 2 のロール | トランザクション 2 の種類 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| 時間エントリの送信          | 仕訳帳明細行 (販売) の GUID     | 未請求売上     | msdyn_journalline            | 仕訳帳明細行 (コスト) GUID     | コスト               | msdyn_journalline  |
| 承認時間                  | 未請求の実績 (販売) の GUID  | 未請求売上     | msdyn_actual                 | コスト実績 (コスト) の GUID       | コスト               | msdyn_actual       |
| 請求書の作成               | 請求明細行の詳細の GUID      | 請求済み売上       | msdyn_invoicelinetransaction | 未請求の販売実績の GUID   | 未請求売上     | msdyn_actual       |
| 請求書の確認           | 実績の逆仕訳の GUID         | 逆仕訳          | msdyn_actual                 | 元の未請求販売の GUID | 元の画像サイズ           | msdyn_actual       |
| 請求済み販売の GUID              | 請求済み売上                  | msdyn_actual       | 未請求の販売実績の GUID   | 未請求売上               | msdyn_actual       |                    |
| 下書きの請求書修正       | 請求書明細行トランザクションの GUID | 置換          | msdyn_invoicelinetransaction | 請求済み販売の GUID            | 元の画像サイズ           | msdyn_actual       |
| 請求書修正の確認     | 請求済みの販売取消の GUID    | 逆仕訳          | msdyn_actual                 | 請求済み販売の GUID            | 元の画像サイズ           | msdyn_actual       |
| 新しい未請求の販売実績の GUID | 置換                     | msdyn_actual       | 請求済み販売の GUID            | 元の画像サイズ                     | msdyn_actual       |                    |