---
title: 製品原価計算ベースの契約品目
description: このトピックでは、以下について説明します
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079499"
---
# <a name="costing-product-based-contract-lines"></a>製品原価計算ベースの契約品目

_**適用対象:** ライト展開 - 見積もり請求の取引_


Dynamics 365 Project Operations の製品ベースの契約ラインには、下流の収益性計算で使用する製品のコスト価格を格納する **原価価格** フィールドがあります。

カタログ製品に製品ベースの契約品目を作成した場合、製品ベースの契約品目のコストは、製品カタログの **標準原価** フィールドから既定で作成されます。 製品カタログの **標準原価** フィールドは、組織の基準通貨で設定されています。 単位原価が契約品目で既定になると、契約の販売通貨に変換されます。

## <a name="unit-cost-on-a-product-based-contract-line"></a>製品ベースの契約品目の単位原価

製品ベースの契約品目に単位原価を持つことで、ユニットの販売ごとに異なる製品コストを設定することができます。 常に必要というわけではありませんが、サプライヤが顧客に対して製品のコストを割り引く場合がある場合も想定されます。 次のシナリオを確認してください。

Fabrikam Robotics 社は、A Datum Corporation 社の組立ラインにロボット アームを設置しています。 Fabrikam 社は設置サービスを提供していますが、ロボットアームは Trey Research 社から調達しています。 Adatum 社にロボットアームを設置することで、Trey Research 社にとって新たな垂直産業を開くことができれば、Fabrikam 社にこの取引を特別割引で提供することができるかもしれません。 この場合、Fabrikam 社は、ロボット アームの製品ベースの契約品目を作成し、この契約に向けて、Trey Research 社のロボットアームの標準的なコストとは異なる単価を入力します。
