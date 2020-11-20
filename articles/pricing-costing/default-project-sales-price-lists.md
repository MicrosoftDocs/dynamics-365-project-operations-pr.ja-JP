---
title: 既定の価格表
description: このトピックでは、Project Operations における既定の価格表と原価価格表について説明します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd29a3fc9c873d46dd66a05ad100c7515177d6cd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130944"
---
# <a name="default-price-lists"></a><span data-ttu-id="12f04-103">既定の価格表</span><span class="sxs-lookup"><span data-stu-id="12f04-103">Default price lists</span></span>

<span data-ttu-id="12f04-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="12f04-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="sales-price-lists"></a><span data-ttu-id="12f04-105">販売価格表</span><span class="sxs-lookup"><span data-stu-id="12f04-105">Sales price lists</span></span>

<span data-ttu-id="12f04-106">Dynamics 365 Project Operations のすべてのプロジェクト見積もりと契約には、既定の販売価格表が含まれています。</span><span class="sxs-lookup"><span data-stu-id="12f04-106">Every project quote and contract in Dynamics 365 Project Operations contains a default sales price list.</span></span> 

### <a name="price-list-default-on-project-quotes"></a><span data-ttu-id="12f04-107">プロジェクトの既定の見積もり価格表</span><span class="sxs-lookup"><span data-stu-id="12f04-107">Price list default on project quotes</span></span>
<span data-ttu-id="12f04-108">システムは、プロジェクト見積書の既定の価格表を決定するにあたって、以下のプロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="12f04-108">The system completes the following process to determine which price list to default on a project quote:</span></span>

1. <span data-ttu-id="12f04-109">システムは、アカウントのプロジェクト価格表に添付されている価格表を確認します。</span><span class="sxs-lookup"><span data-stu-id="12f04-109">The system looks at the price lists that are attached to the account's project price lists.</span></span> 
2. <span data-ttu-id="12f04-110">取引先企業のレコードにプロジェクト価格表が添付されている場合、システムは、プロジェクトの見積書の通貨と一致するプロジェクト パラメータに添付されている販売価格表を探します。</span><span class="sxs-lookup"><span data-stu-id="12f04-110">If there are project price lists attached to the account record, the system looks at the sales price lists attached to the project parameters that match the currency of the project quote.</span></span>
3. <span data-ttu-id="12f04-111">続いて、システムは、プロジェクトの見積書の日付範囲と一致する価格表の日付効果を確認します。</span><span class="sxs-lookup"><span data-stu-id="12f04-111">Next, the system checks the date effectivity of the price lists that match the date range of the project quote.</span></span> <span data-ttu-id="12f04-112">具体的には、見積もりが作成された日付です。</span><span class="sxs-lookup"><span data-stu-id="12f04-112">Specifically, the date the quote was created.</span></span>
4. <span data-ttu-id="12f04-113">プロジェクト見積もりの日付に有効な価格表が複数ある場合、すべての価格表はプロジェクトの見積書に既定となります。</span><span class="sxs-lookup"><span data-stu-id="12f04-113">If there are multiple price lists that are effective for the date of the project quote, all of the price lists default on the project quote.</span></span>
5. <span data-ttu-id="12f04-114">プロジェクト見積書の日付に有効な価格表がない場合、プロジェクト見積書には既定のプロジェクト価格表はありません。</span><span class="sxs-lookup"><span data-stu-id="12f04-114">If no price lists in effect for the date of the project quote, there's no default project price list on the project quote.</span></span> <span data-ttu-id="12f04-115">プロジェクトの見積もりに警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="12f04-115">A warning message will occur on the project quote.</span></span> <span data-ttu-id="12f04-116">メッセージには、プロジェクトの価格表が添付されていないため、プロジェクト上の実際の見積もりは価格が付かないことが表示されています。</span><span class="sxs-lookup"><span data-stu-id="12f04-116">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

### <a name="price-list-default-on-project-contracts"></a><span data-ttu-id="12f04-117">プロジェクト契約の既定の価格表</span><span class="sxs-lookup"><span data-stu-id="12f04-117">Price list default on project contracts</span></span> 
<span data-ttu-id="12f04-118">システムは、プロジェクト契約の既定の価格表を決定するにあたって、以下のプロセスを完了します :</span><span class="sxs-lookup"><span data-stu-id="12f04-118">The system completes the following process to determine which price list to default on a project contract:</span></span>

1. <span data-ttu-id="12f04-119">見積書から契約書を作成した場合は、見積書に記載されているプロジェクト価格表を別途コピーしてプロジェクト契約書に添付します。</span><span class="sxs-lookup"><span data-stu-id="12f04-119">If the contract is created from a quote, the project price lists on the quote are copied over separately and attached to the project contract.</span></span>
2. <span data-ttu-id="12f04-120">ゼロから契約書を作成した場合、システムはその取引先企業のプロジェクト価格表に添付されている価格表を参照します。</span><span class="sxs-lookup"><span data-stu-id="12f04-120">If the contract is created from scratch, the system looks at the price lists that are attached to the project price lists of the account.</span></span> <span data-ttu-id="12f04-121">取引先企業のレコードにプロジェクトの価格表が添付されていない場合、システムは、プロジェクト契約の通貨と一致するプロジェクト パラメータに添付された販売価格表を探します。</span><span class="sxs-lookup"><span data-stu-id="12f04-121">If there aren't project price lists attached to the account record, the system looks for sales price lists attached to the project parameters that match the currency of the project contract.</span></span>
4. <span data-ttu-id="12f04-122">続いて、プロジェクト契約の日付範囲と一致する価格表の日付の有効性をチェックします。</span><span class="sxs-lookup"><span data-stu-id="12f04-122">Next, the system checks the date effectivity of the price lists that match the date range of the project contract.</span></span> <span data-ttu-id="12f04-123">具体的には、契約が作成された日付です。</span><span class="sxs-lookup"><span data-stu-id="12f04-123">Specifically, the date the contract was created.</span></span>
5. <span data-ttu-id="12f04-124">契約日に有効な価格表が複数ある場合は、すべての価格表が契約上で既定となります。</span><span class="sxs-lookup"><span data-stu-id="12f04-124">If there are multiple price lists that are effective for the date of the contract, all of the price lists default on the contract.</span></span>
6. <span data-ttu-id="12f04-125">契約日に有効な価格表がない場合、プロジェクトの価格表が既定となる契約はありません。</span><span class="sxs-lookup"><span data-stu-id="12f04-125">If there are no price lists in effect for the date of the contract, no project price lists default to the contract.</span></span> <span data-ttu-id="12f04-126">プロジェクト契約書に警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="12f04-126">A warning message will occur on the project contract.</span></span> <span data-ttu-id="12f04-127">メッセージには、プロジェクトの価格表が添付されていないため、プロジェクト上の実際の見積もりは価格が付かないことが表示されています。</span><span class="sxs-lookup"><span data-stu-id="12f04-127">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

## <a name="cost-price-lists"></a><span data-ttu-id="12f04-128">原価価格表</span><span class="sxs-lookup"><span data-stu-id="12f04-128">Cost price lists</span></span>

<span data-ttu-id="12f04-129">原価価格表は、Project Operations のどのエンティティにも既定とはなりません。</span><span class="sxs-lookup"><span data-stu-id="12f04-129">Cost price lists don't default to any entity in Project Operations.</span></span> <span data-ttu-id="12f04-130">プロジェクトコストに使用する原価価格表の決定は、常にその瞬間に行われます。</span><span class="sxs-lookup"><span data-stu-id="12f04-130">Determining the cost price list to use for project costs is always done in the moment.</span></span> <span data-ttu-id="12f04-131">システムは、プロジェクトコストの既定の価格表を決定するにあたって、以下のプロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="12f04-131">The system completes the following process to determine which price list to use for project costs:</span></span>

1. <span data-ttu-id="12f04-132">システムは最初に、プロジェクトの契約組織単位に添付されている価格表を調べます。</span><span class="sxs-lookup"><span data-stu-id="12f04-132">The system first looks at the price lists that are attached to the contracting organization unit of the project.</span></span>
2. <span data-ttu-id="12f04-133">次に、入庫見積もりの日付や実際の明細と一致する価格表の日付効果を見ていきます。</span><span class="sxs-lookup"><span data-stu-id="12f04-133">The system then looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> <span data-ttu-id="12f04-134">この状況では、*見積もりライン* とは、プロジェクト・オペレーションにおける見積もりの 3 つのコンテクストのすべてを指します :</span><span class="sxs-lookup"><span data-stu-id="12f04-134">In this situation, *estimate line* refers to all three contexts of estimation in Project Operations:</span></span>

    - <span data-ttu-id="12f04-135">プロジェクト見積もり明細</span><span class="sxs-lookup"><span data-stu-id="12f04-135">Project estimate line</span></span>
    - <span data-ttu-id="12f04-136">見積依頼明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="12f04-136">Quote line detail</span></span>
    - <span data-ttu-id="12f04-137">契約品目の詳細</span><span class="sxs-lookup"><span data-stu-id="12f04-137">Contract line detail</span></span>
  
3. <span data-ttu-id="12f04-138">入力された見積もりや実績の日付に有効な価格表が複数ある場合は、直近に作成された価格表が選択されます。</span><span class="sxs-lookup"><span data-stu-id="12f04-138">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
4. <span data-ttu-id="12f04-139">プロジェクトの契約組織ユニットに添付されている価格表がない場合、プロジェクトの通貨と一致するプロジェクトのパラメータに添付されている原価価格表を検索します。</span><span class="sxs-lookup"><span data-stu-id="12f04-139">If there no price lists attached to the contracting organization unit of the project, the system looks at cost price lists attached to project parameters that match the currency of the project.</span></span>
5. <span data-ttu-id="12f04-140">次に、入力された見積もりまたは実際の明細の日付と一致する価格表の日付の有効性を調べます。</span><span class="sxs-lookup"><span data-stu-id="12f04-140">Next the system looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> 
6. <span data-ttu-id="12f04-141">入力された見積もりや実績の日付に有効な価格表が複数ある場合は、直近に作成された価格表が選択されます。</span><span class="sxs-lookup"><span data-stu-id="12f04-141">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
7. <span data-ttu-id="12f04-142">通貨と有効日が一致する原価価格表がプロジェクト パラメータに添付されていない場合は、入力された見積もりまたは実際の明細で原価率が既定でゼロ (0) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="12f04-142">If there are no cost price lists attached to the project parameters that match the currency and effective date, the system defaults the cost rate to zero (0) on the incoming estimate or actual line.</span></span>
