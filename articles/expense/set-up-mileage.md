---
title: マイレージ レートの階層を使用したマイレージの設定
description: このトピックでは、マイレージ レートとマイレージ レートの階層について説明します。
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083677"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a><span data-ttu-id="60505-103">マイレージ レートの階層を使用したマイレージの設定</span><span class="sxs-lookup"><span data-stu-id="60505-103">Set up mileage using mileage rate tiers</span></span>

<span data-ttu-id="60505-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="60505-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="60505-105">経費が報告され、選択した経費カテゴリが **マイレージ** の場合、その経費明細行の金額は、*マイレージあたりのレート* 金額に従って計算されます。</span><span class="sxs-lookup"><span data-stu-id="60505-105">When an expense is reported and the selected expense category is **Mileage**, the amount for that expense line is calculated according to the *rate per mileage* amount.</span></span> <span data-ttu-id="60505-106">この金額は、定義されたマイレージの階層を使用するか、マイレージ レートの階層が設定されていない場合は、標準のマイレージ レートに従って決定されます。</span><span class="sxs-lookup"><span data-stu-id="60505-106">This amount is determined by using defined mileage tiers or, if no mileage rate tiers are set up, by following a standard rate of mileage.</span></span> 

<span data-ttu-id="60505-107">マイレージ レートの階層は、**経費管理** > **設定** > **全般** > **経費カテゴリ** > **マイレージ** > **カテゴリの設定** に移動することで設定できます。</span><span class="sxs-lookup"><span data-stu-id="60505-107">Mileage rate tiers can be set up by going to **Expense Management** > **Setup** > **General** > **Expense categories** > **Mileage** > **Category setup**.</span></span>

<span data-ttu-id="60505-108">10.0.18 にアップグレードした後、組織でマイレージの経費カテゴリを使用している場合は、以下の設計変更を確認した後、マイレージ機能を有効にすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="60505-108">After you upgrade to 10.0.18, if your organization uses the mileage expense category, consider enabling the mileage feature after reviewing the design changes below.</span></span> 

<span data-ttu-id="60505-109">マイレージ レート階層の新しい設計は、**数量** フィールドの値の処理方法に影響します。</span><span class="sxs-lookup"><span data-stu-id="60505-109">The new design of mileage rate tiers impacts how the value in the **Quantity** field is processed.</span></span> <span data-ttu-id="60505-110">10.0.18 のリリース以前は、**数量** フィールドの値が下限と見なされていました。</span><span class="sxs-lookup"><span data-stu-id="60505-110">Prior to the release of 10.0.18, the value in the **Quantity** field was considered to be the lower limit.</span></span> <span data-ttu-id="60505-111">累積がその値を超えた場合、対応するレートが使用されました。</span><span class="sxs-lookup"><span data-stu-id="60505-111">When accumulation crossed that value, the corresponding rate was used.</span></span>  <span data-ttu-id="60505-112">10.0.18 では、**数量** フィールドの値が上限と見なされます。</span><span class="sxs-lookup"><span data-stu-id="60505-112">As of 10.0.18, the value in the **Quantity** field is considered the upper limit.</span></span> <span data-ttu-id="60505-113">マイレージの累積が **数量** フィールドの値未満の場合、対応するレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60505-113">The corresponding rate is used when mileage accumulation is less than the value in the **Quantity** field.</span></span>  <span data-ttu-id="60505-114">マイレージの階層の新モデルは、マイレージの階層間の一貫性と使いやすさの向上に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="60505-114">The new model for mileage tiers helps with consistency across mileage tiers and better usability.</span></span>   

<span data-ttu-id="60505-115">承認されたすべての経費精算書は、転記時に新しい設計に従って再計算されます。</span><span class="sxs-lookup"><span data-stu-id="60505-115">All approved expense reports will be recalculated during posting according to the new design.</span></span>

## <a name="example"></a><span data-ttu-id="60505-116">例</span><span class="sxs-lookup"><span data-stu-id="60505-116">Example</span></span>
 
### <a name="before-version-10018"></a><span data-ttu-id="60505-117">バージョン 10.0.18 より前</span><span class="sxs-lookup"><span data-stu-id="60505-117">Before version 10.0.18</span></span>
<span data-ttu-id="60505-118">2 つのマイレージ レート階層では、各階層の **数量** フィールドは、マイレージの下限を表します。</span><span class="sxs-lookup"><span data-stu-id="60505-118">With two mileage rate tiers, the **Quantity** field in each tier represents the lower mileage limit.</span></span> <span data-ttu-id="60505-119">現在、階層 1 の値はゼロ (0) でレートは 0.45、階層 2 の値は1000 でレートは 0.25 です。</span><span class="sxs-lookup"><span data-stu-id="60505-119">Currently, tier one has a value of zero (0) and a rate of 0.45, and tier two has a value of 1000 and a rate of 0.25.</span></span> <span data-ttu-id="60505-120">累積したマイルまたはキロメートルがフィールドの値を超える場合、関連するレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60505-120">If the accumulated miles or kilometers crosses the value in the field, the related rate is used.</span></span> <span data-ttu-id="60505-121">数量がゼロの明細行がない場合、システムは経費管理で定義されたマイレージ レートを使用します。</span><span class="sxs-lookup"><span data-stu-id="60505-121">If there's no line with zero quantity, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="60505-122">従業員が 1,500 マイルの経費報告書を提出した場合、転記された経費報告書の 2 つのマイレージ行は、1000 (レート 0.45) + 500 (レート 0.25) = 575.00 になります。</span><span class="sxs-lookup"><span data-stu-id="60505-122">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575.00.</span></span>

### <a name="after-version-10018"></a><span data-ttu-id="60505-123">バージョン 10.0.18 以降</span><span class="sxs-lookup"><span data-stu-id="60505-123">After version 10.0.18</span></span>
<span data-ttu-id="60505-124">10.0.18 では、各階層の **数量** フィールドは、階層の上限を表します。</span><span class="sxs-lookup"><span data-stu-id="60505-124">In 10.0.18, the **Quantity** field in each tier represents the upper limit of the tier.</span></span> <span data-ttu-id="60505-125">現在、階層 1 の値は 999 でレートは 0.45、階層 2 の値は 999,999,999.00 でレートは 0.25 です。</span><span class="sxs-lookup"><span data-stu-id="60505-125">Currently, tier one has a value of 999 and a rate of 0.45, and tier two has a value of 999,999,999.00 and a rate of 0.25.</span></span> <span data-ttu-id="60505-126">累積したマイルまたはキロメートルが **数量** フィールドの値を超える場合、関連するレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60505-126">If the accumulated miles or kilometers crosses the value in the **Quantity** field, the related rate is used.</span></span> <span data-ttu-id="60505-127">すべての上限を超えると、システムは経費管理で定義されたマイレージ レートを使用します。</span><span class="sxs-lookup"><span data-stu-id="60505-127">If all upper limits are exceeded, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="60505-128">同じシナリオを正しく計算するには、階層設定を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60505-128">To correctly calculate the same scenario, the tier set up must be changed.</span></span> <span data-ttu-id="60505-129">階層 1 の **数量** フィールドの値は 999.00 で、層 2 の値は 999,999,999.00 です。</span><span class="sxs-lookup"><span data-stu-id="60505-129">The **Quantity** field in tier one has a value of 999.00 and a value of 999,999,999.00 in tier two.</span></span> <span data-ttu-id="60505-130">従業員が階層 1 でマイルまたはキロメートルの合計数を超えた場合、システムは経費管理で定義されたマイレージ レートを使用します。</span><span class="sxs-lookup"><span data-stu-id="60505-130">If an employee exceeds the total quantity of miles or kilometers in tier one, the system uses the rate of mileage that is defined in Expense management.</span></span> 
  
<span data-ttu-id="60505-131">従業員が 1,500 マイルの経費報告書を提出した場合、転記された経費報告書の 2 つのマイレージ行は、1000 (レート 0.45) + 500 (レート 0.25) = 575 になります</span><span class="sxs-lookup"><span data-stu-id="60505-131">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575</span></span>

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a><span data-ttu-id="60505-132">同一レートの複数のマイレージ階層に対するマイレージ数計算を有効にする機能</span><span class="sxs-lookup"><span data-stu-id="60505-132">Enable the Mileage amount calculation for multiple mileage tiers with same rate feature</span></span>

<span data-ttu-id="60505-133">**同一レートの複数のマイレージ階層に対するマイレージ数計算** 機能は、マイレージ レート計算を改善します。</span><span class="sxs-lookup"><span data-stu-id="60505-133">The **Mileage amount calculation for multiple mileage tiers with same rate** feature improves mileage rate calculation.</span></span> <span data-ttu-id="60505-134">この機能を有効するには、以下の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="60505-134">Complete the following steps to enable this feature.</span></span>

1. <span data-ttu-id="60505-135">**ワークスペース** > **機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="60505-135">Go to **Workspaces** > **Feature Management**.</span></span> 
2. <span data-ttu-id="60505-136">一覧で **同一レートの複数のマイレージ階層に対するマイレージ数計算** を見つけて選択し、**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="60505-136">In the list, locate and select **Mileage amount calculation for multiple mileage tiers with same rate**, and then select **Enable now**.</span></span>

<span data-ttu-id="60505-137">この機能を有効にした後、マイレージ階層をリセットして、**数量** フィールドの値を正しく反映します。</span><span class="sxs-lookup"><span data-stu-id="60505-137">After you enable the feature, reset the mileage tiers to correctly reflect the value of the **Quantity** field.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
