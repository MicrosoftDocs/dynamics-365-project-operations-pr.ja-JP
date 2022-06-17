---
title: スキルと能力の定義
description: この記事では、リソースを評価するための習熟度モデルの設定方法について説明します。
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 707a88b2f72c7324a6954a2e0cdce995b012ff48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915468"
---
# <a name="define-skills-and-proficiencies"></a>スキルと能力の定義

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

スキルは、Dynamics 365 Project Operations と Dynamics 365 Field Service (ある場合) の間で共有されるリソース特性です。 

- プロジェクト オペレーションでスキルのリポジトリを維持するには、**リソース** \> **リソースのスキル** の順に移動します。 

## <a name="use-proficiency-models-to-rate-resources"></a>実力モデルを使用してリソースを評価する

リソースのスキルは能力モデルによって評価されます。 個々の評価が実力モデル内にあります。 

1. 実力モデルを作成するには、**リソース** \>**実力モデル** の順に移動し、**新規** を選択します。
2. 新しい評価モデルでは、最小評価値、最大価値、評価されるエンティティを指定します。
3. **評価値** サブグリッドでは、最小値から最大値まで、さまざまな評価値を定義できます。


これらの評価値は、**リソース要件**、**スケジュール ボード**、および **スケジュール アシスタント** の各種フィルター上で表示されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]