---
title: 製品原価計算ベースの見積依頼明細行
description: この記事では、製品ベースの見積ラインに原価を適用する方法について説明します。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825617"
---
# <a name="costing-product-based-quote-lines"></a>製品原価計算ベースの見積依頼明細行

_**適用対象:** ライト展開 - 見積もり請求の取引_


Dynamics 365 Project Operations の製品ベースの見積もり行にも **原価** フィールドがあります。 このフィールドは、見積依頼明細行で製品の原価価格を追跡し、下位の利益性の計算をするために使用されます。

カタログ製品に対する製品ベースの見積依頼明細行が作成されると、製品ベースの見積依頼明細行の原価は、製品カタログの **標準のコスト** フィールドで規定値に設定されます。 製品カタログの標準のコスト フィールドは、組織の基本通貨で設定されます。 製品ベースの見積依頼明細行での既定の単位原価は、見積の販売通貨に変換されます。

## <a name="unit-cost-on-a-product-based-quote-line"></a>製品ベースの見積依頼明細行の単位原価

製品ベースの見積依頼明細行で単位原価を設定する目的は、販売ごとに製品のさまざまなコストを考慮に入れることです。 これは典型的なシナリオではありませんが、最終販売の顧客によっては、製品のコストが納入業者によって割引される場合があります。

たとえば、次のようなものです。

Fabrikam Robotics は、A Datum Corporation のアセンブリ明細にロボット アームを設置しています。 Fabrikam は設置サービスを提供しますが、ロボット アームは Trey ロボティクスから調達されます。 A Datum Corporation にロボット アームを設置することで、Trey のロボット アームに新しい業界の垂直構造が開かれた場合、Trey はこの取引に対して Fabrikam に特別割引を提供することができます。

この場合、Fabrikam は、Robotic Arms に対する製品ベースの見積依頼明細行を作成し、この見積もりの単位原価あたりの特別な値を入力します。 このコストは、Trey Robotic Arms の標準コストとは異なります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
