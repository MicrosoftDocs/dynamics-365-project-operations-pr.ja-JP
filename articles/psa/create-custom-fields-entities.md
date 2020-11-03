---
title: カスタム フィールドとエンティティの作成
description: このトピックでは、Power Apps のプラットフォームでオプション セットとエンティティを作成する方法を説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079337"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="19261-103">カスタム フィールドとエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="19261-103">Create custom fields and entities</span></span> 

<span data-ttu-id="19261-104">Power Apps プラットフォームにてカスタム オプション セットまたはエンティティを作成するには以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="19261-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="19261-105">このトピックで扱う手順は Project Service Automation (PSA) のWebインターフェイスを使用して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19261-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19261-106">すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="19261-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="19261-107">この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。</span><span class="sxs-lookup"><span data-stu-id="19261-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="19261-108">必要な変更をすべて行った後、このソリューションを **管理ソリューション** としてエクスポートします。これを別のインスタンスにインポートして価格設定を再利用します。</span><span class="sxs-lookup"><span data-stu-id="19261-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="19261-109">価格設定のディメンションのソリューションにカスタム フィールドとオプション セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="19261-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="19261-110">価格設定のディメンションは、オプション セット、あるいはエンティティである場合があります。</span><span class="sxs-lookup"><span data-stu-id="19261-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="19261-111">いずれも価格設定のソリューションにて作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="19261-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="19261-112">この手順では、エンティティ ベースのディメンションと、オプション セット ベースのディメンションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="19261-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="19261-113">エンティティ ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="19261-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="19261-114">PSA で、 **設定** > **ソリューション** をクリックし、続いて **\<your organization name> 価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="19261-115">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19261-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="19261-116">**新規** をクリックして、 **スタンダード タイトル** と呼ばれる新しいエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="19261-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="19261-117">その他の必要情報を入力し、 **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![スタンダード タイトル エンティティの定義](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="19261-119">オプション セット ベースのディメンション</span><span class="sxs-lookup"><span data-stu-id="19261-119">Option set-based dimensions</span></span> 
<span data-ttu-id="19261-120">2つのオプション セット ベースのディメンションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="19261-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="19261-121">**リソースの作業場所** を使用して、 **ホーム** と **オンサイト** の各作業場所の価格を追跡します。 **リソースの作業時間** に **Regular** and **Overtime** の値を使用して、作業完了時の利幅を適用します。</span><span class="sxs-lookup"><span data-stu-id="19261-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="19261-122">PSAで、 **設定** > **ソリューション** をクリックし、続いて **\<your organization name> 価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="19261-123">ソリューション エクスプローラーの左側のナビゲーションパネルで、  **オプション セット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19261-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="19261-124">**新規** をクリックして新たなオプション セットを作成し、その他の必要な情報を入力し、 **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="19261-125">リソースの作業場所 と呼ばれるオプション セット ベースの 価格設定ディメンション</span><span class="sxs-lookup"><span data-stu-id="19261-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="19261-126">リソースの作業時間 と呼ばれるオプション セット ベースの 価格設定ディメンション</span><span class="sxs-lookup"><span data-stu-id="19261-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="19261-127">エンティティ ベースのディメンションのデータを作成する</span><span class="sxs-lookup"><span data-stu-id="19261-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="19261-128">エンティティ ベースのディメンションのデータは手動での作成、あるいは Microsoft Excel にてインポートやサービス呼び出しを使用して作成することが出来ます。</span><span class="sxs-lookup"><span data-stu-id="19261-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="19261-129">この手順では、エンティティ ベースのディメンションである **スタンダード タイトル** を使用して次の2つのスタンダード タイトルを作成します。 **システム エンジニア** と **シニア システム エンジニア** 。</span><span class="sxs-lookup"><span data-stu-id="19261-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="19261-130">以下の例に示すように、作成するデータが小さい場合は、標準フォームを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="19261-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="19261-131">PSAで、 **高度な検索** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="19261-132">**スタンダード タイトル** エンティティを選択し、 **結果** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="19261-133">**スタンダード タイトル** エンティティのすべての行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="19261-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="19261-134">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-134">Click **New**.</span></span> <span data-ttu-id="19261-135">**名称** フィールドにて 「システムエンジニア」と入力し **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19261-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="19261-136">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="19261-136">Close the form.</span></span> 
4. <span data-ttu-id="19261-137">手順1から3を繰り返し、他のスタンダード タイトル 「シニア システム エンジニア」を作成します。</span><span class="sxs-lookup"><span data-stu-id="19261-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="19261-138">スタンダード タイトル エンティティ のサンプル データ</span><span class="sxs-lookup"><span data-stu-id="19261-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


