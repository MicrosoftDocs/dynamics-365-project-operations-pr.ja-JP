---
title: スキルと能力の定義
description: このトピックでは、リソースの評価に使用する習熟度モデルの設定方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897637"
---
# <a name="define-skills-and-proficiencies"></a>スキルと能力の定義

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

スキルとは、Dynamics 365 プロジェクト オペレーションと Dynamics 365 Field Service (存在する場合) の間で共有されるリソースの特性です。 

- プロジェクト オペレーションでスキルのリポジトリを維持するには、**リソース** \> **リソースのスキル**の順に移動します。 

## <a name="use-proficiency-models-to-rate-resources"></a>実力モデルを使用してリソースを評価する

リソースのスキルは実力モデルで評価されます。 個々の評価が実力モデル内にあります。 

1. 実力モデルを作成するには、**リソース** \>**実力モデル**の順に移動し、**新規**を選択します。
2. 新規評価モデルでは、最低限評価値、最大評価値、評価されるエンティティを指定します。
3. **評価値**サブグリッドで、最小から最大までの異なる評価値を定義できます。


これらの評価値は、**リソース要件**、**スケジュール ボード**、および**スケジュール アシスタント**の各種フィルター上で表示されます。
