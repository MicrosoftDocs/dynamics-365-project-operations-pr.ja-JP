---
title: 材料の原価率と販売率を設定する
description: この記事では、プロジェクトで使用した資料のコストと販売率を設定する方法について説明します。
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911786"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>材料の原価率と販売率を設定する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations で製品のコストと販売価格を設定できます。 製品のコストと販売価格は 1 つの通貨でのみ表示できます。これは、価格表ヘッダーの通貨である必要があります。

製品のコストと販売率を設定するには、次の手順を実行します。 

1. **販売** > **顧客** > **価格表** に移動して、**新規** を選択して、新しい価格表を作成します。 
2. **価格表品目** のサブグリッド メニューで、**新しい価格表品目** を選択します。 
3. **クイック作成** ページで、新しい価格を作成する製品と単位を入力します。

カタログ アイテムの価格を定義する方法の詳細については、[価格表と価格表項目を使用して製品の価格を定義する](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products)と[通貨と価格の小数精度](/dynamics365/sales/decimal-precision-currency-pricing) をご覧ください。
> [!NOTE]
> Dynamics 365 Project Operations は、Dynamics 365 Sales などの製品のすべての価格設定方法をサポートしているわけではありません。 プロジェクトで使用される製品に対してサポートされている唯一の価格設定方法は *通貨額* です。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
