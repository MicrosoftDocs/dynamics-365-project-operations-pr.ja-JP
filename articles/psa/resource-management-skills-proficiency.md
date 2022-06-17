---
title: スキルおよび実力モデル
description: この記事では、スキルと実力モデルを使用する方法について説明します。
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 27a9668c3a0d6a2323fb4797a29f6c7d3d146c57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925310"
---
# <a name="skills-and-proficiency-models"></a>スキルおよび実力モデル

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

スキルは、Dynamics 365 Project Service Automation と Dynamics 365 Field Service (ある場合) の間で共有されるリソース特性です。 

Project Service Automation でスキルのリポジトリを維持するには、**リソース** \> **リソースのスキル** の順に移動します。 

> ![リソースのスキル。](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>能力モデルを使用したリソースの評価

リソースのスキルは能力モデルによって評価されます。 個々の評価が実力モデル内にあります。 

1. 実力モデルを作成するには、**リソース** \>**実力モデル** の順に移動し、**新規** を選択します。
2. 新しい評価モデルでは、最小評価値、最大価値、評価されるエンティティを指定します。
3. **評価値** サブグリッドでは、最小値から最大値まで、さまざまな評価値を定義できます。

> ![定義された最小評価値と最高評価値。](media/Resource-Management-image85.png)

これらの評価値は、**リソース要件**、**スケジュール ボー**、および **スケジュール アシスタント** フィルターで表示されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
