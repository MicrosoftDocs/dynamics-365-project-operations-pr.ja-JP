---
title: 製品原価計算ベースの見積依頼明細行
description: このトピックでは、製品ベースの見積依頼明細行への原価価格の適用について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906222"
---
# <a name="costing-product-based-quote-lines"></a>製品原価計算ベースの見積依頼明細行

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


Dynamics 365 Project Operations の製品ベースの見積依頼明細行にも**原価価格**フィールドがあります。 このフィールドは、見積依頼明細行で製品の原価価格を追跡し、下位の利益性の計算をするために使用されます。

カタログ製品に対する製品ベースの見積依頼明細行が作成されると、製品ベースの見積依頼明細行の原価は、製品カタログの**標準のコスト** フィールドで規定値に設定されます。 製品カタログの標準のコスト フィールドは、組織の基本通貨で設定されます。 製品ベースの見積依頼明細行での既定の単位原価は、見積の販売通貨に変換されます。

## <a name="unit-cost-on-a-product-based-quote-line"></a>製品ベースの見積依頼明細行の単位原価

製品ベースの見積依頼明細行で単位原価を設定する目的は、販売ごとに製品のさまざまなコストを考慮に入れることです。 これは典型的なシナリオではありませんが、最終販売の顧客によっては、製品のコストが納入業者によって割引される場合があります。

たとえば、次のようなものです。

Fabrikam Robotics は、A Datum Corporation のアセンブリ明細にロボット アームを設置しています。 Fabrikam は設置サービスを提供しますが、ロボット アームは Trey ロボティクスから調達されます。 A Datum Corporation にロボット アームを設置することで、Trey のロボット アームに新しい業界の垂直構造が開かれた場合、Trey はこの取引に対して Fabrikam に特別割引を提供することができます。

この場合、Fabrikam は、Robotic Arms に対する製品ベースの見積依頼明細行を作成し、この見積もりの単位原価あたりの特別な値を入力します。 このコストは、Trey Robotic Arms の標準コストとは異なります。
