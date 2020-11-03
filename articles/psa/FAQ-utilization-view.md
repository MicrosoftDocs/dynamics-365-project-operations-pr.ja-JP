---
title: リソースの稼働率を表示する
description: このトピックでは、リソースの稼働率ビューについて説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079290"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="ae4d7-103">リソースの稼働率を表示する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="ae4d7-104">**Project Service リソースの稼働率** ページの **稼働率ビュー** では、それぞれの予約可能リソースの稼働率を表示します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="ae4d7-105">このビューはスケジュール ボードに基づいているため、共通する機能があります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![稼働率ビューのスクリーンショット](media/FAQ-utilization-1.png)
 

<span data-ttu-id="ae4d7-107">請求可能稼働率の計算のしくみは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="ae4d7-108">稼働率 = (実際に割当可能な時間) / (リソース キャパシティ)</span><span class="sxs-lookup"><span data-stu-id="ae4d7-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="ae4d7-109">セルには、選択した期間 (日、週、または月) で按分計算された稼働率を表します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="ae4d7-110">各セルの色は、ターゲットの請求可能稼働率と比べた、リソースの請求可能稼働率が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="ae4d7-111">ターゲット稼働率は、リソースのデフォルトの役割または個々のリソース自体に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="ae4d7-112">この計算では、まずターゲットの個人を調べ、次にリソースの既定のロールを調べます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="ae4d7-113">リソースにターゲットを設定する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-113">Set target on a resource</span></span>

1. <span data-ttu-id="ae4d7-114">**リソース** \> **リソース** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="ae4d7-115">リソースを選択してレコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="ae4d7-116">**Project Service** タブでは、リソースの目標稼働率を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![[Project Service] タブを使用してターゲット稼働率を設定するスクリーンショット](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="ae4d7-118">ロールの目標稼働率を設定する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="ae4d7-119">**リソース** \> **リソースのロール** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="ae4d7-120">ロールを選択してレコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="ae4d7-121">ロールのターゲット稼働率を設定します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-121">Set the target utilization for the role.</span></span>

> ![[リソースのロール] を使用してターゲット稼働率を設定するスクリーンショット](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="ae4d7-123">リソースの可能稼働率を計算する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="ae4d7-124">リソースの可能稼働率を計算するには、いくつかの前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="ae4d7-125">個々のリソースの既定ロールを設定する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-125">Set default role for individual resource</span></span>

<span data-ttu-id="ae4d7-126">まず、目標稼働率がそれぞれのリソース、またはリソースのロールで設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="ae4d7-127">ターゲットのリソース ロールを使用する場合、個別のリソースには既定のロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="ae4d7-128">これを設定するには、 **リソース** \> **リソース** へと移動します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="ae4d7-129">リソースを選択してから、レコードを開き、 **Project Service** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="ae4d7-130">**リソース ロール** グリッドにて、リソースに1つのロールが設定されていて、 **これを既定とする** が **はい** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="ae4d7-131">リソースのロールに対する請求の種類を変更する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-131">Change billing type for resource role</span></span>

<span data-ttu-id="ae4d7-132">リソースロールの請求の種類は、 **請求可能** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="ae4d7-133">**リソース** \> **リソースのロール** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="ae4d7-134">更新を行うレコードを開き、請求種類の既定値を **請求可能** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="ae4d7-135">リソースロールの作業時間を設定する</span><span class="sxs-lookup"><span data-stu-id="ae4d7-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="ae4d7-136">キャパシティ計算のため、リソースは作業時間を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="ae4d7-137">**リソース** \> **リソース** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="ae4d7-138">リソースを選択してレコードを開き、 **作業時間の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="ae4d7-139">**リソースの一覧** ビューから **作業時間テンプレート** を適用することで、リソースの一覧を一括更新することができます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="ae4d7-140">割り当て可能な実際の時間に関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ae4d7-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="ae4d7-141">割り当て可能な実績時間は、 **実績** エンティティから提供されます。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="ae4d7-142">請求タイプが **請求可能** となる実績が計算に含まれているため、実績が請求可能なプロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="ae4d7-143">請求可能稼働率が表示されない場合、以下の点をチェックすると役立つことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="ae4d7-144">リソースのキャパシティに作業時間が定義されている。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="ae4d7-145">リソースには、個別に定義されたターゲット稼働率があるか、既定のロールが割り当てられている。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="ae4d7-146">ロールにはターゲット稼働率が定義されている。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="ae4d7-147">実績の請求タイプは、稼働状況計算の対象となる期間に対して **請求可能** となります。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="ae4d7-148">請求タイプに請求可能以外の実績が表示されている場合は、以下を確認してください。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="ae4d7-149">実績で使用されるロールの既定の請求の種類が請求可能以外になっている。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="ae4d7-150">プロジェクトを支えるプロジェクト契約品目のロールが請求不可に設定されている。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="ae4d7-151">プロジェクトに関連する契約品目がない。</span><span class="sxs-lookup"><span data-stu-id="ae4d7-151">The project does not have an associated contract line.</span></span>

