---
title: スキルおよび実力モデル
description: このトピックでは、スキルと実力モデルを使用する方法を説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079488"
---
# <a name="skills-and-proficiency-models"></a>スキルおよび実力モデル

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

スキルは、Dynamics 365 Project Service Automation と Dynamics 365 Field Service (ある場合) の間で共有されるリソース特性です。 

Project Service Automation でスキルのリポジトリを維持するには、 **リソース** \> **リソースのスキル** の順に移動します。 

> ![リソースのスキル](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>実力モデルを使用してリソースを評価する

リソースのスキルは実力モデルで評価されます。 個々の評価が実力モデル内にあります。 

1. 実力モデルを作成するには、 **リソース** \>**実力モデル** の順に移動し、 **新規** を選択します。
2. 新規評価モデルでは、最低限評価値、最大評価値、評価されるエンティティを指定します。
3. **評価値** サブグリッドで、最小から最大までの異なる評価値を定義できます。

> ![定義された最小評価値と最高評価値](media/Resource-Management-image85.png)

これらの評価値は、 **リソース要件** 、 **スケジュール ボード** 、および **スケジュール アシスタント** の各種フィルター上で表示されます。
