---
title: 価格ディメンションとしてカスタム フィールドとエンティティを作成する
description: このトピックは、ユーザー定義のオプションセットまたはエンティティの作成方法について説明します。
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642819"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="ebb55-103">価格ディメンションとしてカスタム フィールドとエンティティを作成する</span><span class="sxs-lookup"><span data-stu-id="ebb55-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="ebb55-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ebb55-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ebb55-105">価格ディメンションとして使用するカスタム オプション セットやエンティティを作成する場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="ebb55-106">詳細は [価格ディメンションの概要](pricing-dimensions-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebb55-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="ebb55-107">すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="ebb55-108">この重要なベスト プラクティスは、今後必要に応じて変更を更新や削除する柔軟性を与えます。</span><span class="sxs-lookup"><span data-stu-id="ebb55-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="ebb55-109">これは作業の再利用にも役立ち、こうした変更を別のインスタンスに簡単に移植できます。必要な変更をすべて行った後で、このソリューションを **マネージド ソリューション** としてエクスポートし、他のインスタンスにインポートすることで価格を再利用します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="ebb55-110">価格設定のディメンションのソリューションにカスタム フィールドとオプション セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="ebb55-111">価格設定のディメンションは、オプション セット、あるいはエンティティである場合があります。</span><span class="sxs-lookup"><span data-stu-id="ebb55-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="ebb55-112">いずれも価格設定のソリューションにて作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebb55-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="ebb55-113">この手順では、エンティティ ベースのディメンションと、オプション セット ベースのディメンションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="ebb55-114">エンティティ ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="ebb55-114">Entity-based dimensions</span></span>
<span data-ttu-id="ebb55-115">エンティティ ベースのディメンションを作成する際は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ebb55-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="ebb55-116">**設定** > **ソリューション** に移動し、続いて **\<your organization name>価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="ebb55-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="ebb55-117">ソリューション エクスプローラーの左側のナビゲーション ウィンドウで **エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="ebb55-118">**新規** を選択して、 **スタンダード タイトル** と呼ばれる新しいエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="ebb55-119">その他の必要情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![スタンダード タイトル エンティティの定義](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="ebb55-121">オプション セット ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="ebb55-121">Option set-based dimensions</span></span> 
<span data-ttu-id="ebb55-122">2つのオプション セット ベースのディメンションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ebb55-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="ebb55-123">**リソースの作業場所** を使用して **ホーム** ロケーション作業と **現場** 作業の価格を追跡します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="ebb55-124">作業の完了時にマークアップを適用する場合は、**標準** と **残業** の値で **リソースの作業時間** を使用します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="ebb55-125">次の図は **リソースの作業場所** ディメンションのビューを示します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![リソースの作業場所 と呼ばれるオプション セット ベースの 価格設定ディメンション](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="ebb55-127">次の図は **リソースの作業時間** ディメンションのビューを示します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![リソースの作業時間 と呼ばれるオプション セット ベースの 価格設定ディメンション](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="ebb55-129">**設定** > **ソリューション** に移動し、**\<your organization name>価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="ebb55-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ebb55-130">ソリューション エクスプローラーの左側のナビゲーション ウィンドウで **オプション セット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="ebb55-131">**新規** を選択して新たなオプション セットを作成し、その他の必要な情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="ebb55-132">エンティティ ベースのディメンションのデータを作成する</span><span class="sxs-lookup"><span data-stu-id="ebb55-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="ebb55-133">エンティティ ベースのディメンションのデータは手動での作成、あるいは Microsoft Excel にてインポートやサービス呼び出しを使用して作成することが出来ます。</span><span class="sxs-lookup"><span data-stu-id="ebb55-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="ebb55-134">この手順では、エンティティ ベースのディメンションである **スタンダード タイトル** を使用して次の2つのスタンダード タイトルを作成します。 **システム エンジニア** と **シニア システム エンジニア** 。</span><span class="sxs-lookup"><span data-stu-id="ebb55-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="ebb55-135">以下の例に示すように、作成するデータが小さい場合は、標準フォームを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ebb55-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="ebb55-136">**高度な検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="ebb55-137">**スタンダード タイトル** エンティティを選択してから **結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="ebb55-138">**スタンダード タイトル** エンティティのすべての行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebb55-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="ebb55-139">**新規** を選択し、**名称** フィールドで、 「システムエンジニア」と入力し **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ebb55-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="ebb55-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ebb55-140">Close the page.</span></span> 
5. <span data-ttu-id="ebb55-141">手順1から3を繰り返し、他のスタンダード タイトル 「シニア システム エンジニア」を作成します。</span><span class="sxs-lookup"><span data-stu-id="ebb55-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![スタンダード タイトル エンティティのサンプル データ](media/ST-data.png)
