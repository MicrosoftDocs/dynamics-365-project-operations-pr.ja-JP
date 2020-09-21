---
title: カスタム フィールドとエンティティの作成
description: このトピックでは、Power Apps のプラットフォームでオプション セットとエンティティを作成する方法を説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752921"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="6df43-103">カスタム フィールドとエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="6df43-103">Create custom fields and entities</span></span> 

<span data-ttu-id="6df43-104">Power Apps プラットフォームにてカスタム オプション セットまたはエンティティを作成するには以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="6df43-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="6df43-105">このトピックで扱う手順は Project Service Automation (PSA) のWebインターフェイスを使用して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df43-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6df43-106">すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="6df43-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="6df43-107">この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。</span><span class="sxs-lookup"><span data-stu-id="6df43-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="6df43-108">必要な変更をすべて行った後、このソリューションを **管理ソリューション** としてエクスポートします。これを別のインスタンスにインポートして価格設定を再利用します。</span><span class="sxs-lookup"><span data-stu-id="6df43-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="6df43-109">価格設定ディメンションのカスタムソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="6df43-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="6df43-110">PSAで、 **構成** > **ソリューション**とクリックし、 **新規** をクリックして新規ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6df43-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="6df43-111">ソリューションの名称を設定します。 **\<自社の名称> 価格設定ディメンション**、その他必要な情報を入力し、 **保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![価格設定ディメンションのカスタムソリューションを作成する](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="6df43-113">価格設定のディメンションのソリューションにカスタム フィールドとオプション セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="6df43-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="6df43-114">価格設定のディメンションは、オプション セット、あるいはエンティティである場合があります。</span><span class="sxs-lookup"><span data-stu-id="6df43-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="6df43-115">いずれも価格設定のソリューションにて作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df43-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="6df43-116">この手順では、エンティティ ベースのディメンションと、オプション セット ベースのディメンションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6df43-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="6df43-117">エンティティ ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="6df43-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="6df43-118">PSAで、 **構成** > **ソリューション**をクリックし、  **\<自社の名称 > 価格設定ディメンション**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="6df43-119">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **エンティティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6df43-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="6df43-120">**新規** をクリックして、 **スタンダード タイトル**と呼ばれる新しいエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="6df43-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="6df43-121">その他の必要情報を入力し、 **保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![スタンダード タイトル エンティティの定義](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="6df43-123">オプション セット ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="6df43-123">Option set-based dimensions</span></span> 
<span data-ttu-id="6df43-124">2つのオプション セット ベースのディメンションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6df43-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="6df43-125">**リソースの作業場所** を使用して、 **ホーム** と **オンサイト** の各作業場所の価格を追跡します。 **リソースの作業時間** に **Regular** and **Overtime** の値を使用して、作業完了時の利幅を適用します。</span><span class="sxs-lookup"><span data-stu-id="6df43-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="6df43-126">PSAで、 **構成** > **ソリューション**をクリックし、  **\<自社の名称> 価格設定ディメンション**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="6df43-127">ソリューション エクスプローラーの左側のナビゲーションパネルで、  **オプション セット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6df43-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="6df43-128">**新規** をクリックして新たなオプション セットを作成し、その他の必要な情報を入力し、 **保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="6df43-129">リソースの作業場所 と呼ばれるオプション セット ベースの 価格設定ディメンション</span><span class="sxs-lookup"><span data-stu-id="6df43-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="6df43-130">リソースの作業時間 と呼ばれるオプション セット ベースの 価格設定ディメンション</span><span class="sxs-lookup"><span data-stu-id="6df43-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="6df43-131">エンティティ ベースのディメンションのデータを作成する</span><span class="sxs-lookup"><span data-stu-id="6df43-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="6df43-132">エンティティ ベースのディメンションのデータは手動での作成、あるいは Microsoft Excel にてインポートやサービス呼び出しを使用して作成することが出来ます。</span><span class="sxs-lookup"><span data-stu-id="6df43-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="6df43-133">この手順では、エンティティ ベースのディメンションである **スタンダード タイトル**を使用して次の2つのスタンダード タイトルを作成します。 **システム エンジニア** と **シニア システム エンジニア** 。</span><span class="sxs-lookup"><span data-stu-id="6df43-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="6df43-134">以下の例に示すように、作成するデータが小さい場合は、標準フォームを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6df43-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="6df43-135">PSAで、 **高度な検索** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="6df43-136">**スタンダード タイトル** エンティティを選択し、 **結果** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="6df43-137">**スタンダード タイトル** エンティティのすべての行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6df43-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="6df43-138">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-138">Click **New**.</span></span> <span data-ttu-id="6df43-139">**名称** フィールドにて 「システムエンジニア」と入力し **保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="6df43-140">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6df43-140">Close the form.</span></span> 
4. <span data-ttu-id="6df43-141">手順1から3を繰り返し、他のスタンダード タイトル 「シニア システム エンジニア」を作成します。</span><span class="sxs-lookup"><span data-stu-id="6df43-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="6df43-142">スタンダード タイトル エンティティ のサンプル データ</span><span class="sxs-lookup"><span data-stu-id="6df43-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="6df43-143">価格設定ディメンション ソリューションにすべての必須PSA エンティティと、関連するコンポーネントを追加する</span><span class="sxs-lookup"><span data-stu-id="6df43-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="6df43-144">価格設定ソリューションには、以下の Project Service エンティティを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df43-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="6df43-145">この手順を使用して、エンティティが新しい価格設定ディメンションを認識できるよう、価格設定ソリューションで重要なスキーマ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="6df43-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="6df43-146">PSAで、 **構成** > **ソリューション**をクリックし、  **\<自社の名称 > 価格設定ディメンション**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="6df43-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="6df43-147">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6df43-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="6df43-148">**ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:</span><span class="sxs-lookup"><span data-stu-id="6df43-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="6df43-149">実績</span><span class="sxs-lookup"><span data-stu-id="6df43-149">Actual</span></span>
- <span data-ttu-id="6df43-150">予約可能リソースです</span><span class="sxs-lookup"><span data-stu-id="6df43-150">Bookable Resource</span></span>
- <span data-ttu-id="6df43-151">見積行</span><span class="sxs-lookup"><span data-stu-id="6df43-151">Estimate Line</span></span>
- <span data-ttu-id="6df43-152">請求明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="6df43-152">Invoice Line Detail</span></span>
- <span data-ttu-id="6df43-153">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="6df43-153">Journal Line</span></span>
- <span data-ttu-id="6df43-154">プロジェクト契約品目の詳細</span><span class="sxs-lookup"><span data-stu-id="6df43-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="6df43-155">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="6df43-155">Project Team Member</span></span>
- <span data-ttu-id="6df43-156">見積依頼明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="6df43-156">Quote Line Detail</span></span>
- <span data-ttu-id="6df43-157">ロール価格利幅</span><span class="sxs-lookup"><span data-stu-id="6df43-157">Role Price Markup</span></span>
- <span data-ttu-id="6df43-158">ロール価格</span><span class="sxs-lookup"><span data-stu-id="6df43-158">Role Price</span></span> 
- <span data-ttu-id="6df43-159">時間入力</span><span class="sxs-lookup"><span data-stu-id="6df43-159">Time Entry</span></span> 

> ![価格設定ディメンション ソリューションに既存のエンティティを追加します。](media/Existing-entities-to-PD-solution.png)

> ![ソリューション コンポーネントの選択](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="6df43-162">選択した各エンティティのすべてのフォームとビューが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6df43-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="6df43-163">上記で選択したエンティティに依存するエンティティを含めるかどうかを確認するダイアログが表示された場合、 **いいえ**をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="6df43-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![すべての関連コンポーネントを含めない](media/Do-not-include-required.png)


