---
title: 製品原価計算ベースの契約品目 (ライト)
description: このトピックでは、以下について説明します
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273699"
---
# <a name="cost-product-based-contract-lines---lite"></a>製品原価計算ベースの契約品目 (ライト)

_**適用対象:** ライト展開 - 見積もり請求の取引_


Dynamics 365 Project Operations の製品ベースの契約品目には、**原価価格** フィールドが含まれますが、これにはダウンストリームの収益性計算のために製品の原価が保管されます。

カタログ製品に対して製品ベースの契約品目が作成されると、品目の原価は製品カタログの **標準原価** フィールドから取得されます。 製品カタログの **標準原価** フィールドは、組織の基準通貨で設定されています。 単位原価が契約品目で既定になると、契約の販売通貨に変換されます。

## <a name="unit-cost-on-a-product-based-contract-line"></a>製品ベースの契約品目の単位原価

製品ベースの契約品目に単位原価を持つことで、ユニットの販売ごとに異なる製品コストを設定することができます。 常に必要というわけではありませんが、サプライヤが顧客に対して製品のコストを割り引く場合がある場合も想定されます。 次のシナリオを確認してください。

Fabrikam Robotics 社は、A Datum Corporation 社の組立ラインにロボット アームを設置しています。 Fabrikam が設置サービスを提供していますが、ロボットアームは Trey Research 社製です。 Adatum 社にロボットアームを設置することで、Trey Research 社にとって新たな垂直産業を開くことができれば、Fabrikam 社にこの取引を特別割引で提供することができるかもしれません。 この場合、Fabrikamは、ロボットアームの製品ベースの契約品目を作成します。 この契約には、単位当たりのコストが入力されます。 コストが、Trey Research のロボットアームのコストとは異なります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]