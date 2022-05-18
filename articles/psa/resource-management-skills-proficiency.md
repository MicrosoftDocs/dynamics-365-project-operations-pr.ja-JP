---
title: スキルおよび実力モデル
description: このトピックでは、スキルと実力モデルを使用する方法を説明します。
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
ms.openlocfilehash: d46382939e22c1ee1d9f5517798aabb3520ae3bd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599874"
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
