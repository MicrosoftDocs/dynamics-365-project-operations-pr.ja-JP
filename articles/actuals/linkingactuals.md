---
title: 実績を元のレコードにリンクする
description: このトピックは、実績を時間入力、経費入力、材料用途ログなどの元のレコードにリンクする方法を説明しています。
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852595"
---
# <a name="link-actuals-to-original-records"></a>実績を元のレコードにリンクする

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


Dynamics 365 Project Operations で *ビジネス トランザクション* は、エンティティで表現されない抽象的な概念です。 ただし、エンティティの一部の一般的なフィールドとプロセスは、ビジネス トランザクションの概念を使用するように設計されています。 次のエンティティはこの概念を使用します:

- 見積依頼明細行の詳細
- 契約品目の詳細
- 見積もり行
- 仕訳帳明細行
- [実績]

これらのエンティティのうち、**見積品目の詳細**、**契約品目の詳細**、**見積品目** は、プロジェクト ライフサイクルの見積フェーズにマップされます。 **仕訳帳明細行** と **実績エンティティ** は、プロジェクト ライフサイクルの実行フェーズにマップされます。

Project Operations はこれら 5 つのエンティティ レコードをビジネス トランザクションと認識します。 唯一の違いは、見積もりフェーズにマップされたエンティティ レコードが財務予測と見なされることです。一方、実行フェーズにマップされたエンティティ レコードは、すでに発生した財務上の事実と見なされます。

## <a name="concepts-that-are-unique-to-business-transactions"></a>ビジネス トランザクションに固有の概念
以下の概念は、ビジネス トランザクションの概念に固有です:

- トランザクションの種類
- トランザクション クラス
- トランザクション発生元
- トランザクション接続

### <a name="transaction-type"></a>トランザクションの種類

トランザクションの種類は、プロジェクトへの財務的影響のタイミングとコンテキストを表します。 それは、Project Operations がサポートする次の値を持つオプション セットで表されます。

  - 原価
  - プロジェクト契約
  - 未請求売上
  - 請求済み売上
  - 組織間営業
  - リソース単位原価

### <a name="transaction-class"></a>トランザクション クラス

トランザクション クラスは、プロジェクトで発生するさまざまな種類のコストを表します。 それは、Project Operations がサポートする次の値を持つオプション セットで表されます。

  - 時間
  - 経費
  - 材料
  - 料金
  - マイルストーン
  - 税

**マイルストーン** は通常、Project Operations の固定価格請求のビジネス ロジックで使用されます。

### <a name="transaction-origin"></a>トランザクション発生元

**トランザクション発生元** は、各ビジネス トランザクションの起点を格納するエンティティです。 プロジェクトが進行するにつれて、各ビジネス トランザクションは別のビジネス トランザクションを発生させ、それが別のビジネス トランザクションを作成します。 トランザクション発生元エンティティは、レポートと追跡可能性に役立てるため、各トランザクションの発生元に関するデータを格納するように設計されています。 

### <a name="transaction-connection"></a>トランザクション接続

**トランザクション接続** は、コストや関連する販売実績、または請求書の確認や請求書の修正などの請求アクティビティによってトリガーされる取引の取り消しなど、トランザクション接続は 2 つの類似したビジネス トランザクション間の関係を格納するエンティティです。

**トランザクション発生元** と **トランザクション接続** を組み合わせることにより、ビジネス トランザクションと特定のビジネス トランザクションの作成につながったアクションとの関係を追跡できます。

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>例: トランザクションの起点とトランザクション接続との連携

次の例は、Project Operations プロジェクトのライフサイクルにおける時間エントリの一般的な処理を示しています。

> ![Project Service ライフサイクルの処理時間エントリ](media/basic-guide-17.png)
 
1. 時間エントリを送信すると、2 つの仕訳入力が作成されます。1 行は原価用、もう 1 行は未請求販売用です。
2. 時間入力の最終承認により 2 つの実績が作成されます。1 つの実績は原価用、もう 1 つの実績は未請求販売用です。
3. 新しいプロジェクト請求書が作成されると、未請求の販売実績のデータを使用して請求明細行トランザクションが作成されます。 
4. 請求書が確認されると、2つの新しい実績が作成されます。1 つは未請求の販売取り消し実績と、もう 1 つ請求済み販売実績です。

これらの各イベントは、**トランザクション発生元** と **トランザクション接続** エンティティでレコードを作成します。 これらの新しいレコードは、時間入力、仕訳明細、実績、および請求書明細の詳細にわたって作成されたレコード間で関係の履歴を構築するのに役立ちます。

次の表は、ワークフローの **トランザクション発生元** エンティティのレコードを示しています。

| イベント                        | 問い合わせ方法                   | 発生元の種類                       | トランザクション                       | トランザクションの種類         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| 時間エントリの送信        | 時間エントリ レコードの GUID   | 時間エントリ                        | 仕訳帳明細行レコードの GUID (コスト)    | 仕訳帳明細行             |
| 時間エントリ レコードの GUID       | 時間入力               | 仕訳帳明細行レコードの GUID (販売)  | 仕訳帳明細行                      |                          |
| 承認時間                | 仕訳帳明細行レコードの GUID | 仕訳帳明細行                      | 未請求の販売レコードの GUID        | 実績                   |
| 時間エントリ レコードの GUID       | 時間入力               | 未請求の販売レコードの GUID        | 実績                            |                          |
| 仕訳帳明細行レコードの GUID     | 仕訳帳明細行             | コスト実績レコードの GUID           | 実績                            |                          |
| 時間エントリ レコードの GUID       | 時間エントリ               | コスト実績レコードの GUID           | 実績                            |                          |
| 請求書の作成             | 時間エントリ レコードの GUID   | 時間エントリ                        | 請求書明細行トランザクションの GUID     | 請求書明細行トランザクション |
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

次の表は、ワークフローの **トランザクション接続** エンティティのレコードを示しています。

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]