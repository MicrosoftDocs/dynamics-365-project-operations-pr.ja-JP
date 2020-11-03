---
title: スキルと能力の定義
description: このトピックでは、リソースの評価に使用する習熟度モデルの設定方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079212"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="35e58-103">スキルと能力の定義</span><span class="sxs-lookup"><span data-stu-id="35e58-103">Define skills and proficiencies</span></span>

<span data-ttu-id="35e58-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="35e58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="35e58-105">スキルとは、Dynamics 365 プロジェクト オペレーションと Dynamics 365 Field Service (存在する場合) の間で共有されるリソースの特性です。</span><span class="sxs-lookup"><span data-stu-id="35e58-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="35e58-106">プロジェクト オペレーションでスキルのリポジトリを維持するには、 **リソース** \> **リソースのスキル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="35e58-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="35e58-107">実力モデルを使用してリソースを評価する</span><span class="sxs-lookup"><span data-stu-id="35e58-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="35e58-108">リソースのスキルは実力モデルで評価されます。</span><span class="sxs-lookup"><span data-stu-id="35e58-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="35e58-109">個々の評価が実力モデル内にあります。</span><span class="sxs-lookup"><span data-stu-id="35e58-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="35e58-110">実力モデルを作成するには、 **リソース** \>**実力モデル** の順に移動し、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="35e58-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="35e58-111">新規評価モデルでは、最低限評価値、最大評価値、評価されるエンティティを指定します。</span><span class="sxs-lookup"><span data-stu-id="35e58-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="35e58-112">**評価値** サブグリッドで、最小から最大までの異なる評価値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="35e58-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="35e58-113">これらの評価値は、 **リソース要件** 、 **スケジュール ボード** 、および **スケジュール アシスタント** の各種フィルター上で表示されます。</span><span class="sxs-lookup"><span data-stu-id="35e58-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
