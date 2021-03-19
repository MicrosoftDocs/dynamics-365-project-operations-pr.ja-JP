---
title: スキルと能力の定義
description: このトピックでは、リソースの評価に使用する習熟度モデルの設定方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279684"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="465d0-103">スキルと能力の定義</span><span class="sxs-lookup"><span data-stu-id="465d0-103">Define skills and proficiencies</span></span>

<span data-ttu-id="465d0-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="465d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="465d0-105">スキルは、Dynamics 365 Project Operations と Dynamics 365 Field Service (ある場合) の間で共有されるリソース特性です。</span><span class="sxs-lookup"><span data-stu-id="465d0-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="465d0-106">プロジェクト オペレーションでスキルのリポジトリを維持するには、**リソース** \> **リソースのスキル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="465d0-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="465d0-107">実力モデルを使用してリソースを評価する</span><span class="sxs-lookup"><span data-stu-id="465d0-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="465d0-108">リソースのスキルは実力モデルで評価されます。</span><span class="sxs-lookup"><span data-stu-id="465d0-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="465d0-109">個々の評価が実力モデル内にあります。</span><span class="sxs-lookup"><span data-stu-id="465d0-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="465d0-110">実力モデルを作成するには、**リソース** \>**実力モデル** の順に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="465d0-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="465d0-111">新しい評価モデルでは、最小評価値、最大価値、評価されるエンティティを指定します。</span><span class="sxs-lookup"><span data-stu-id="465d0-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="465d0-112">**評価値** のサブグリッドで、最小から最大までの異なる評価値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="465d0-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="465d0-113">これらの評価値は、**リソース要件**、**スケジュール ボード**、および **スケジュール アシスタント** の各種フィルター上で表示されます。</span><span class="sxs-lookup"><span data-stu-id="465d0-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]