---
title: Project Operations における商取引
description: この記事は、Microsoft Dynamics 365 Project Operations のビジネスト ランザクションのコンセプトの概要について説明します。
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923286"
---
# <a name="business-transactions-in-project-operations"></a>Project Operations における商取引

_**適用対象 :** リソース/非在庫ベースのシナリオに使用する Project Operations、見積請求に対応する小規模のデプロイ_

Microsoft Dynamics 365 Project Operations で *ビジネス トランザクション* は、どのエンティティでも表現されない抽象的な概念です。 ただし、エンティティの一部の一般的なフィールドとプロセスは、ビジネス トランザクションの概念を使用するように設計されています。 次のエンティティはこの抽象化を使用します:

- 見積依頼明細行の詳細
- 契約品目の詳細
- 見積もり行
- 仕訳帳明細行
- [実績]

これらのエンティティのうち、見積品目の詳細、契約品目の詳細、見積品目は、プロジェクト ライフサイクルの *見積フェーズ* にマッピングされます。 仕訳帳明細行と実績エンティティは、プロジェクト ライフサイクルの *実行フェーズ* にマッピングされます。

Project Operations はこれら 5 つのエンティティ レコードをビジネス トランザクションとして扱います。 見積段階にマッピングされるエンティティ (見積明細、契約明細、見積明細) のレコードは *財務予測* とみなされ、実行段階にマッピングされるエンティティ、仕訳明細、実績のレコードは既に発生した *財務上の事実* と見なされます。

詳細については、[見積もり](../project-management/estimating-projects-overview.md) と [実績](actuals-overview.md) を参照してください。

## <a name="concepts-that-are-unique-to-business-transactions"></a>ビジネス トランザクションに固有の概念

以下の概念は、ビジネス トランザクションの概念に固有です:

- トランザクションの種類
- トランザクション クラス
- トランザクション発生元
- トランザクション接続

### <a name="transaction-type"></a>トランザクションの種類

トランザクションの種類は、プロジェクトへの財務的影響のタイミングとコンテキストを表します。 Project Operations でサポートされている以下の値を持つオプションセットで定義されています:

- 原価
- プロジェクト契約
- 未請求売上
- 請求済み売上
- 組織間営業
- リソース単位原価

### <a name="transaction-class"></a>トランザクション クラス

トランザクション クラスは、プロジェクトで発生するさまざまな種類のコストを表します。 Project Operations でサポートされている以下の値を持つオプションセットで定義されています:

- 時間
- 経費
- 材料
- 料金
- マイルストーン
- 税

> [!NOTE]
> **マイルストーン** の値は通常、Project Operations の固定価格請求のビジネス ロジックで使用されます。

### <a name="transaction-origin"></a>トランザクション発生元

トランザクション オリジンは、レポートとトレーサビリティを支援するために、各ビジネストランザクションのオリジンを格納するエンティティです。 プロジェクトが実行されると、それぞれのビジネス トランザクションが別のビジネス トランザクションを作成し、続いて別のビジネスト ランザクションを作成します。

### <a name="transaction-connection"></a>トランザクション接続

コストや関連する販売実績、または請求書の確認や請求書の修正などの請求アクティビティによってトリガーされる取引の取り消しなど、トランザクション接続は 2 つの類似したビジネス トランザクション間の関係を格納するエンティティです。

トランザクションの起点とトランザクションの接続エンティティを組み合わせると、ビジネス トランザクションと特定のビジネストランザクションを作成する原因となったアクション間の関係を追跡することができます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
