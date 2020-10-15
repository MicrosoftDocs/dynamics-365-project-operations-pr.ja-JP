---
title: 営業案件からプロジェクトの見積もりを作成する
description: このトピックは、営業案件からプロジェクトの見積もりを作成するための情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898538"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="cd6f9-103">営業案件からプロジェクトの見積もりを作成する</span><span class="sxs-lookup"><span data-stu-id="cd6f9-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="cd6f9-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="cd6f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cd6f9-105">見積もりは、次の方法でプロジェクトの営業案件から作成できます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="cd6f9-106">**プロジェクトの営業案件**ページで、**見積もり**タブを選択</span><span class="sxs-lookup"><span data-stu-id="cd6f9-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="cd6f9-107">営業案件の販売プロセス フローを選択</span><span class="sxs-lookup"><span data-stu-id="cd6f9-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="cd6f9-108">既存の見積もりで営業案件の参照を更新する</span><span class="sxs-lookup"><span data-stu-id="cd6f9-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="cd6f9-109">Project Opportunity ページの見積もりタブを選択</span><span class="sxs-lookup"><span data-stu-id="cd6f9-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="cd6f9-110">営業案件からプロジェクト見積もりを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="cd6f9-111">**プロジェクトの営業案件**ページを開き、**見積もり**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="cd6f9-112">**見積もり**サブグリッドで、**+** を選択して営業案件に基づき新しいプロジェクトの見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="cd6f9-113">すべての営業案件品目および関連するプロジェクトの価格表は、営業案件から新しい見積りにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="cd6f9-114">営業案件の販売プロセス フローを選択</span><span class="sxs-lookup"><span data-stu-id="cd6f9-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="cd6f9-115">営業案件のプロセス フローから見積もりを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="cd6f9-116">営業案件の販売プロセス フローから、営業案件を開きます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="cd6f9-117">**見積もり**ステージを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="cd6f9-118">**次へ**を選択して、**+ 作成**を選び新しい見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="cd6f9-119">この新しい見積りの**概要**タブの情報のほとんどは、営業案件からデフォルト設定されます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="cd6f9-120">不足している必要な情報を入力するか、または必要に応じて**概要**タブでデフォルト値を更新、</span><span class="sxs-lookup"><span data-stu-id="cd6f9-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="cd6f9-121">**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-121">Select **Save**.</span></span> <span data-ttu-id="cd6f9-122">新しい見積もりが作成され、営業案件に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="cd6f9-123">**営業案件**ページの**見積もり**タブで、見積り情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="cd6f9-124">営業案件の販売プロセスは、次の段階**提案**に進みます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="cd6f9-125">既存の見積もりで営業案件の参照を更新する</span><span class="sxs-lookup"><span data-stu-id="cd6f9-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="cd6f9-126">既存の見積もりは、営業案件にリンクできます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="cd6f9-127">次の手順を実行して、既存の見積もりの営業案件を更新します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="cd6f9-128">**見積もり**ページを開き、**概要**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="cd6f9-129">**営業案件**フィールドで、見積もりにリンクする営業案件を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="cd6f9-130">営業案件の**見積もり**グリッドで見積りを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="cd6f9-131">営業案件の販売プロセスを使用して、営業案件が次の段階、**提案**へ移動できます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="cd6f9-132">営業案件をこのステージに移動すると、この営業案件に関連付けられている見積もりのリストから、この見積もりを選択できます。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="cd6f9-133">この見積もりを選択すると、それで進めていることを示します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="cd6f9-134">営業案件に関連する他のすべての見積もりは、いずれかが勝つまで引き続き利用可能でアクティブです。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="cd6f9-135">販売プロセスを前のステージ**見積もり**に戻すことができ、先に進むために別の見積もりを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd6f9-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
