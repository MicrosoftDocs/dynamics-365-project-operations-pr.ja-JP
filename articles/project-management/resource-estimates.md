---
title: リソースの見積もり
description: このトピックは、Project Operations でリソースの見積もりを計算する方法について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286524"
---
# <a name="resource-estimates"></a>リソースの見積もり

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

リソースの見積もりは、適用可能な価格設定のディメンションとともに、作業分解構造で定義された時間フェーズの作業から得られます。 通常、計算は **各ロールのレート/時間 x 時間** です。 各リソースの時間フェーズの作業は、リソース割り当てレコードに保存されます。 価格設定は、事前定義された価格表に保存されます。 単位換算は、該当する価格表に基づいて適用されます。

![リソースの見積もり](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>既定の原価価格と原価通貨

原価は組織単位から既定設定されます。

## <a name="default-bill-rate-and-sales-currency"></a>既定の請求レートと販売通貨

販売価格は取引ごとに 1 回適用されます。 販売価格表の既定の階層は次のとおりです。

1. 組織全体
2. 顧客
3. 見積もり/契約


[!INCLUDE[footer-include](../includes/footer-banner.md)]