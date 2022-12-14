---
title: 原価率から販売価格を算出する通貨換算の設定
description: この記事では、原価取引から売上取引を生成する際に、Microsoft Dynamics 365 Project Operations で使用される通貨変換の動作を構成する方法について説明します。
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816670"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>原価率から販売価格を算出する通貨換算の設定

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Microsoft Dynamics 365 Project Operations では、経費区分の売上価格を数値で設定することも、発生した原価をもとに計算するように設定することも可能です。

発生したコストに基づいて計算されるように設定されている場合、次のオプションを使用できます:

- コスト
- コストに対するマークアップ率

プロジェクト契約の販売通貨と異なる通貨で費用原価が発生するシナリオでは、費用原価に基づく販売価格を算出するために通貨換算が必要となります。

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>ネイティブの Dataverse 為替レートを使用した通貨変換動作

既定では、Project Operations は Dataverse の Currency テーブルに保存されている通貨為替レートを使用します。 原価から販売価格を計算するためにネイティブの為替レートを使用するよう、Project Operations を構成するには、以下の手順に従います。

1. **Project Operations \> 設定 \> パラメータ** ーに移動します。
1. **プロジェクト パラメータ** の詳細ページを開きます。
1. **通貨換算ロジック** フィールドを空白の値に設定します。

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>財務と運用アプリからの為替レートを使用する通貨換算動作

Dataverse にネイティブで用意されている Currency テーブルの為替レートは、日付が有効ではありません。 したがって、コスト レートから販売価格を計算するための要件に合わせて、常にスケーリングされるとは限りません。

財務と運用環境の為替レートを利用して、原価通貨の原価率から販売通貨の販売価格を計算することができます。 この通貨換算動作を構成するには、次の手順に従います。

1. **プロジェクト パラメーター** ページで、**通貨換算ロジック** フィールドを追加します。 その後、カスタマイズを保存して公開します。
1. **Project Operations \> 設定 \> パラメータ** ーに移動します。
1. **プロジェクト パラメータ** の詳細ページを開きます。 
1. **通貨の変換動作**  フィールドを  **デフォルトへのフォールバックで拡張** に設定します。
1. **デュアル書き込みアプリ ユーザー** のセキュリティ ロール **グローバル読み取り** 権限を次のテーブルに付与します:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. 財務と運用環境で、初期同期を使用して次の二重書き込みマップを実行します。

    - 為替レート タイプ (msdyn\_exchangeratetypes)
    - 為替レートの通貨ペア (msdyn\_currencyexchangeratepairs)
    - CDS 為替レート (msdyn\_currencyexchangerates)

これらの変更が完了した後、二重書き込みにより、財務と運用環境の為替レートが Dataverse で利用できるようになります。 Project Operations は、これらの為替レートを使用して、コスト レートを契約の販売通貨に変換します。

> [!NOTE]
> この通貨換算動作は、原価率からの販売価格の計算にのみ適用されます。 基本通貨の値を一般的に計算するためには使用されません。 この手順を完了するかどうかに関係なく、基本通貨の値は常に現地の Dataverse 為替レートを使用します。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
