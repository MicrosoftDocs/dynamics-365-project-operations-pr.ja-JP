---
title: スキルおよび実力モデル
description: このトピックでは、スキルと実力モデルを使用する方法を説明します。
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124194"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="cc16a-103">スキルおよび実力モデル</span><span class="sxs-lookup"><span data-stu-id="cc16a-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cc16a-104">スキルは、Dynamics 365 Project Service Automation と Dynamics 365 Field Service (ある場合) の間で共有されるリソース特性です。</span><span class="sxs-lookup"><span data-stu-id="cc16a-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="cc16a-105">Project Service Automation でスキルのリポジトリを維持するには、**リソース** \> **リソースのスキル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc16a-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![リソースのスキル](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="cc16a-107">実力モデルを使用してリソースを評価する</span><span class="sxs-lookup"><span data-stu-id="cc16a-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="cc16a-108">リソースのスキルは実力モデルで評価されます。</span><span class="sxs-lookup"><span data-stu-id="cc16a-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="cc16a-109">個々の評価が実力モデル内にあります。</span><span class="sxs-lookup"><span data-stu-id="cc16a-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="cc16a-110">実力モデルを作成するには、**リソース** \>**実力モデル** の順に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc16a-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="cc16a-111">新しい評価モデルでは、最小評価値、最大価値、評価されるエンティティを指定します。</span><span class="sxs-lookup"><span data-stu-id="cc16a-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="cc16a-112">**評価値** のサブグリッドで、最小から最大までの異なる評価値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="cc16a-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![定義された最小評価値と最高評価値](media/Resource-Management-image85.png)

<span data-ttu-id="cc16a-114">これらの評価値は、**リソース要件**、**スケジュール ボード**、および **スケジュール アシスタント** の各種フィルター上で表示されます。</span><span class="sxs-lookup"><span data-stu-id="cc16a-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
