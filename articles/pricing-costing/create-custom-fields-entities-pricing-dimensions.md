---
title: 価格ディメンションとしてカスタム フィールドとエンティティを作成する
description: このトピックは、ユーザー定義のオプションセットまたはエンティティの作成方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130899"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="50eda-103">価格ディメンションとしてカスタム フィールドとエンティティを作成する</span><span class="sxs-lookup"><span data-stu-id="50eda-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="50eda-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="50eda-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50eda-105">ユーザー定義のオプション セットやエンティティを作成するには以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="50eda-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50eda-106">すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="50eda-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="50eda-107">この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。</span><span class="sxs-lookup"><span data-stu-id="50eda-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="50eda-108">必要な変更をすべて行った後、このソリューションを **管理ソリューション** としてエクスポートします。これを別のインスタンスにインポートして価格設定を再利用します。</span><span class="sxs-lookup"><span data-stu-id="50eda-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="50eda-109">価格設定ディメンションのカスタムソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="50eda-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="50eda-110">**設定** > **ソリューション** に移動し、 **新規** を選択して新規ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="50eda-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="50eda-111">**\<your organization name> 価格設定ディメンション** ソリューションの名称を決定し、その他必要な情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="50eda-112">価格設定のディメンションのソリューションにカスタム フィールドとオプション セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50eda-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="50eda-113">価格設定のディメンションは、オプション セット、あるいはエンティティである場合があります。</span><span class="sxs-lookup"><span data-stu-id="50eda-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="50eda-114">いずれも価格設定のソリューションにて作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="50eda-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="50eda-115">この手順では、エンティティ ベースのディメンションと、オプション セット ベースのディメンションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="50eda-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="50eda-116">エンティティ ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="50eda-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="50eda-117">**設定** > **ソリューション** に移動し、続いて **\<your organization name>価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="50eda-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="50eda-118">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="50eda-119">**新規** を選択して、 **スタンダード タイトル** と呼ばれる新しいエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="50eda-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="50eda-120">その他の必要情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="50eda-121">オプション セット ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="50eda-121">Option set-based dimensions</span></span> 
<span data-ttu-id="50eda-122">2つのオプション セット ベースのディメンションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="50eda-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="50eda-123">**リソースの作業場所** を使用して、 **ホーム** と **オンサイト** の各作業場所の価格を追跡します。 **リソースの作業時間** に **Regular** and **Overtime** の値を使用して、作業完了時の利幅を適用します。</span><span class="sxs-lookup"><span data-stu-id="50eda-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="50eda-124">**設定** > **ソリューション** に移動し、**\<your organization name>価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="50eda-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="50eda-125">ソリューション エクスプローラーの左側のナビゲーションパネルで、  **オプション セット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="50eda-126">**新規** を選択して新たなオプション セットを作成し、その他の必要な情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="50eda-127">エンティティ ベースのディメンションのデータを作成する</span><span class="sxs-lookup"><span data-stu-id="50eda-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="50eda-128">エンティティ ベースのディメンションのデータは手動での作成、あるいは Microsoft Excel にてインポートやサービス呼び出しを使用して作成することが出来ます。</span><span class="sxs-lookup"><span data-stu-id="50eda-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="50eda-129">この手順では、エンティティ ベースのディメンションである **スタンダード タイトル** を使用して次の2つのスタンダード タイトルを作成します。 **システム エンジニア** と **シニア システム エンジニア** 。</span><span class="sxs-lookup"><span data-stu-id="50eda-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="50eda-130">以下の例に示すように、作成するデータが小さい場合は、標準フォームを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="50eda-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="50eda-131">**高度な検索** を選択し、エンティティに **スタンダード タイトル** を選択します。続いて **結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="50eda-132">**スタンダード タイトル** エンティティのすべての行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="50eda-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="50eda-133">**新規** を選択し、**名称** フィールドで、 「システムエンジニア」と入力し **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50eda-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="50eda-134">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="50eda-134">Close the form.</span></span> 
4. <span data-ttu-id="50eda-135">手順1から3を繰り返し、他のスタンダード タイトル 「シニア システム エンジニア」を作成します。</span><span class="sxs-lookup"><span data-stu-id="50eda-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="50eda-136">価格設定ディメンション ソリューションにすべての必須エンティティと、関連するコンポーネントを追加する</span><span class="sxs-lookup"><span data-stu-id="50eda-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="50eda-137">価格設定ソリューションには、以下のエンティティを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50eda-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="50eda-138">この手順を使用して、エンティティが新しい価格設定ディメンションを認識できるよう、価格設定ソリューションで重要なスキーマ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="50eda-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="50eda-139">**設定** > **ソリューション** を選択し、**\<your organization name>価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="50eda-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="50eda-140">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50eda-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="50eda-141">**ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:</span><span class="sxs-lookup"><span data-stu-id="50eda-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="50eda-142">実績</span><span class="sxs-lookup"><span data-stu-id="50eda-142">Actual</span></span>
  - <span data-ttu-id="50eda-143">予約可能リソースです</span><span class="sxs-lookup"><span data-stu-id="50eda-143">Bookable Resource</span></span>
  - <span data-ttu-id="50eda-144">見積行</span><span class="sxs-lookup"><span data-stu-id="50eda-144">Estimate Line</span></span>
  - <span data-ttu-id="50eda-145">請求明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="50eda-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="50eda-146">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="50eda-146">Journal Line</span></span>
  - <span data-ttu-id="50eda-147">プロジェクト契約品目の詳細</span><span class="sxs-lookup"><span data-stu-id="50eda-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="50eda-148">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="50eda-148">Project Team Member</span></span>
  - <span data-ttu-id="50eda-149">見積依頼明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="50eda-149">Quote Line Detail</span></span>
  - <span data-ttu-id="50eda-150">ロール価格利幅</span><span class="sxs-lookup"><span data-stu-id="50eda-150">Role Price Markup</span></span>
  - <span data-ttu-id="50eda-151">ロール価格</span><span class="sxs-lookup"><span data-stu-id="50eda-151">Role Price</span></span> 
  - <span data-ttu-id="50eda-152">時間入力</span><span class="sxs-lookup"><span data-stu-id="50eda-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="50eda-153">選択した各エンティティのすべてのフォームとビューが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="50eda-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="50eda-154">上記で選択したエンティティに依存するエンティティを含めるかどうかを確認するダイアログが表示された場合、 **いいえ** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="50eda-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

