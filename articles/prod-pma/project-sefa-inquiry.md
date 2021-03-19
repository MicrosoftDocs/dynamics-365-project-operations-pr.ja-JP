---
title: 連邦支援金の支出スケジュールに関する照会
description: このトピックでは、連邦支援金の支出スケジュールに関する照会についての情報を提供します。
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288970"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4be7e-103">連邦支援金の支出スケジュールに関する照会</span><span class="sxs-lookup"><span data-stu-id="4be7e-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4be7e-104">行政管理予算局通達 A-133 によると、連邦資金を受け取る機関は、単一監査としても知られる監査要件の対象となります。</span><span class="sxs-lookup"><span data-stu-id="4be7e-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="4be7e-105">この監査プロセスは、連邦支援金の収入と支出を定期的に報告するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4be7e-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="4be7e-106">この単一監査レポートの一部には、連邦支援金の支出スケジュール (SEFA) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4be7e-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="4be7e-107">連邦支援金の支出スケジュールの照会には、連邦国内援助 (CFDA) のタイトルと番号、助成金番号、助成金の年度、資金を提供する連邦機関の名前、パススルー エンティティの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4be7e-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="4be7e-108">この照会は特定の期間に対するものです。</span><span class="sxs-lookup"><span data-stu-id="4be7e-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="4be7e-109">通常、その期間は財務諸表の期間、つまり会計年度と同じになります。</span><span class="sxs-lookup"><span data-stu-id="4be7e-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="4be7e-110">照会には、選択した日付範囲に予測日を持つ助成金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4be7e-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="4be7e-111">照会の **助成金支給機関** 列には、助成金の顧客、またはパススルー助成金に対しては助成金支給機関が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4be7e-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="4be7e-112">助成金がパススルー助成金ではない場合、**パススルー機関** 列は助成金の顧客を表示します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="4be7e-113">助成金がパススルー助成金ではない場合、**パススルー機関** 列は空になります。</span><span class="sxs-lookup"><span data-stu-id="4be7e-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="4be7e-114">CFDA クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="4be7e-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="4be7e-115">連邦支援金の支出スケジュール照会では、CFDA 番号に関連付けることができる CFDA クラスターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4be7e-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="4be7e-116">**プロジェクト管理と会計 \> 設定 \> 助成金 \> 連邦国内援助クラスターのカタログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="4be7e-117">CFDA クラスターを作成するには、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="4be7e-118">クラスター名を入力してください。</span><span class="sxs-lookup"><span data-stu-id="4be7e-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="4be7e-119">**保存** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="4be7e-120">CFDA 番号を設定する</span><span class="sxs-lookup"><span data-stu-id="4be7e-120">Set up CFDA numbers</span></span>

<span data-ttu-id="4be7e-121">助成金に追加して連邦支援金の支出スケジュール照会に含めることができる CFDA 番号を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4be7e-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="4be7e-122">**プロジェクト管理と会計 \> 設定 \> 助成金 \> 連邦国内援助クラスターのカタログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="4be7e-123">CFDA 番号を作成するには、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="4be7e-124">**番号** 列で、CFDA 番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="4be7e-125">**タブ** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="4be7e-126">**説明** 列に、CFDA タイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="4be7e-127">**タブ** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="4be7e-128">オプション: **プログラム クラスター** フィールドに、適切な CFDA クラスターを追加します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="4be7e-129">**保存** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4be7e-130">連邦支援金の支出のスケジュールに関する照会を報告するための助成金を設定する</span><span class="sxs-lookup"><span data-stu-id="4be7e-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="4be7e-131">**プロジェクト管理と会計 \> 助成金 \> 助成金** の順に移動して、既存の助成金を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="4be7e-132">**設定** クイックタブで、**連邦国内援助のカタログ** フィールドに、CFDA 番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4be7e-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="4be7e-133">助成金の CFDA 番号は、レポートする CFDA クラスターを決定します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="4be7e-134">**連絡先情報** クイックタブで、次の手順に従って助成金支給者情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="4be7e-135">**助成金顧客** フィールドに、助成金の責任者である顧客を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="4be7e-136">既存の助成金の場合、この情報はすでに入力されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4be7e-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="4be7e-137">助成金の顧客が資金提供者であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="4be7e-138">助成金顧客が資金提供者である場合は、**パススルー** チェックボックスをクリアのままにします。</span><span class="sxs-lookup"><span data-stu-id="4be7e-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="4be7e-139">別の顧客が資金提供者であり、助成金顧客がお金の支出と追跡を担当している場合は、**パススルー** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="4be7e-140">前の手順で **パススルー** チェックボックスを選択した場合は、**助成金支給機関** フィールドに、助成金を提供した顧客を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="4be7e-141">助成金支給機関と助成金顧客を同じ顧客にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4be7e-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="4be7e-142">パススルー助成金の例は次の通りです。</span><span class="sxs-lookup"><span data-stu-id="4be7e-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="4be7e-143">連邦政府は、州のインフラストラクチャ プロジェクトに資金を提供しました。</span><span class="sxs-lookup"><span data-stu-id="4be7e-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="4be7e-144">連邦政府は州が使うためのお金を支給しました。</span><span class="sxs-lookup"><span data-stu-id="4be7e-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="4be7e-145">この場合、連邦政府が助成金支給機関であり、州が助成金顧客です。</span><span class="sxs-lookup"><span data-stu-id="4be7e-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="4be7e-146">この機能を最初にオンにすると、助成金の既存の番号を使用して、最初の CFDA 番号が入力されます。</span><span class="sxs-lookup"><span data-stu-id="4be7e-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="4be7e-147">助成金の種類に基づいて、SEFA レポートから助成金を除外する</span><span class="sxs-lookup"><span data-stu-id="4be7e-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="4be7e-148">**プロジェクト管理と会計 \> 設定 \> 助成金 \> 助成金の種類** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="4be7e-149">**規定情報** クイックタブで、**連邦支援金の支出スケジュールから除外する** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="4be7e-150">**保存** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4be7e-151">連邦支援金の支出スケジュールに関する照会を実行する</span><span class="sxs-lookup"><span data-stu-id="4be7e-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="4be7e-152">**プロジェクト管理と会計 \> 照会とレポート \> 助成金照会 \> 連邦支援金の支出のスケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="4be7e-153">**パラメーター** セクションで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4be7e-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="4be7e-154">**日付間隔** フィールドで、日付間隔のコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="4be7e-155">または、**開始日** フィールドと **終了日** フィールドで、日付間隔を定義します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="4be7e-156">オプション: 請求されたトランザクションのみを収益として照会に含めるには、**請求された収益のみを含める** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4be7e-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="4be7e-157">列</span><span class="sxs-lookup"><span data-stu-id="4be7e-157">Columns</span></span>

<span data-ttu-id="4be7e-158">連邦支援金の支出のスケジュールに関する照会には、次の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4be7e-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="4be7e-159">連邦国内支援クラスターのカタログ名</span><span class="sxs-lookup"><span data-stu-id="4be7e-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="4be7e-160">助成金支給機関</span><span class="sxs-lookup"><span data-stu-id="4be7e-160">Grantor agency</span></span>
- <span data-ttu-id="4be7e-161">パススルー機関</span><span class="sxs-lookup"><span data-stu-id="4be7e-161">Pass-through agency</span></span>
- <span data-ttu-id="4be7e-162">助成金名</span><span class="sxs-lookup"><span data-stu-id="4be7e-162">Grant name</span></span>
- <span data-ttu-id="4be7e-163">助成金 ID</span><span class="sxs-lookup"><span data-stu-id="4be7e-163">Grant ID</span></span>
- <span data-ttu-id="4be7e-164">助成金申請 ID</span><span class="sxs-lookup"><span data-stu-id="4be7e-164">Grant application ID</span></span>
- <span data-ttu-id="4be7e-165">連邦国内支援クラスターのカタログ</span><span class="sxs-lookup"><span data-stu-id="4be7e-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="4be7e-166">領収書</span><span class="sxs-lookup"><span data-stu-id="4be7e-166">Receipts</span></span>
- <span data-ttu-id="4be7e-167">支出</span><span class="sxs-lookup"><span data-stu-id="4be7e-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]