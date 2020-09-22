---
title: 人件費と経費の標準原価を構成する
description: このトピックでは、プロジェクトの人件費と経費の標準原価を設定する方法について説明します。
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752947"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="4a70c-103">人件費と経費の標準原価を構成する</span><span class="sxs-lookup"><span data-stu-id="4a70c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a70c-104">このトピックでは、プロジェクトの人件費と経費の標準原価を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="4a70c-105">このタスクでは、USSI データセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4a70c-106">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 原価価格 (時間)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="4a70c-107">**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a70c-107">Select **New**.</span></span>
3. <span data-ttu-id="4a70c-108">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="4a70c-109">**原価価格**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="4a70c-110">プロジェクト カテゴリに対して標準原価価格を設定するか、または作業者番号、プロジェクト番号、カテゴリ、日付、またはこれらの任意の組み合わせごとに原価価格を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4a70c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="4a70c-111">適用される原価価格は、詳細レベルが最大の原価価格です。</span><span class="sxs-lookup"><span data-stu-id="4a70c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="4a70c-112">**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-112">Select **Save**.</span></span>
6. <span data-ttu-id="4a70c-113">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 販売価格 (時間)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="4a70c-114">**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a70c-114">Select **New**.</span></span>
8. <span data-ttu-id="4a70c-115">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="4a70c-116">**有効**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="4a70c-117">**価格**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="4a70c-118">時間トランザクションまたはプロジェクト カテゴリに対して標準販売価格を設定できます。</span><span class="sxs-lookup"><span data-stu-id="4a70c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="4a70c-119">作業者番号、プロジェクト番号、カテゴリ、トランザクションの日付、またはこれらの任意の組み合わせごとに販売価格を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="4a70c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="4a70c-120">作業者が時間仕訳帳にトランザクションを入力するときに適用される実際の販売価格は、詳細レベルの最大の販売価格です。</span><span class="sxs-lookup"><span data-stu-id="4a70c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4a70c-121">たとえば、一般的な販売価格と作業者固有の販売価格の両方が設定されている場合、作業者固有の販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a70c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="4a70c-122">**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-122">Select **Save**.</span></span>
12. <span data-ttu-id="4a70c-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4a70c-123">Close the page.</span></span>
13. <span data-ttu-id="4a70c-124">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 原価価格 (経費)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="4a70c-125">**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a70c-125">Select **New**.</span></span>
15. <span data-ttu-id="4a70c-126">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="4a70c-127">**原価価格**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="4a70c-128">複数のフィールドに入力できますが、これはレコードを保存するのに最低限必要なものです。</span><span class="sxs-lookup"><span data-stu-id="4a70c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="4a70c-129">**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-129">Select **Save**.</span></span>
18. <span data-ttu-id="4a70c-130">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 販売価格 (経費)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="4a70c-131">**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a70c-131">Select **New**.</span></span>
20. <span data-ttu-id="4a70c-132">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="4a70c-133">**有効**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="4a70c-134">**価格**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="4a70c-135">作業者が経費仕訳帳にトランザクションを入力するときに適用される実際の販売価格は、詳細レベルの最大の販売価格です。</span><span class="sxs-lookup"><span data-stu-id="4a70c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4a70c-136">たとえば、一般的な価格と作業者固有の販売価格の両方が設定されている場合、作業者固有の販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a70c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="4a70c-137">**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a70c-137">Select **Save**.</span></span>

