---
title: 経費カテゴリの設定
description: このトピックでは、経費報告書の経費カテゴリおよび共有カテゴリを設定する方法について説明します。
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d66df1ffd2be2ff884561010c46cda255a2d2189
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001801"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="da9e5-103">経費カテゴリの設定</span><span class="sxs-lookup"><span data-stu-id="da9e5-103">Set up expense categories</span></span>

<span data-ttu-id="da9e5-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="da9e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="da9e5-105">従業員が経費報告書を作成するとき、記録する各経費は経費カテゴリに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="da9e5-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="da9e5-106">経費カテゴリは、組織内の法人間で共有される共有カテゴリから派生します。</span><span class="sxs-lookup"><span data-stu-id="da9e5-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="da9e5-107">組織の定義方法に応じて、これらの経費カテゴリを他の領域で共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="da9e5-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="da9e5-108">組織の定義および実装チームからのガイダンスに基づいて、経費管理で使用されるカテゴリを経費管理でのみ使用するか、他の領域で共有するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da9e5-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="da9e5-109">これらのカテゴリは、プロジェクト管理と会計および経費管理との間、またはプロジェクト管理と会計および製造の間で共有することができます。</span><span class="sxs-lookup"><span data-stu-id="da9e5-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="da9e5-110">ただし、経費管理と製造の間で共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="da9e5-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="da9e5-111">セットアップ プロセスを開始する前に、各経費カテゴリについて次の決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="da9e5-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="da9e5-112">どのような経費カテゴリか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-112">What is the expense category?</span></span> <span data-ttu-id="da9e5-113">例として、フライト、ホテル、またはマイレージのカテゴリなどがあります。</span><span class="sxs-lookup"><span data-stu-id="da9e5-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="da9e5-114">経費カテゴリは、プロジェクト管理と会計でも使用することができるか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="da9e5-115">可能な場合、次の決定をする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="da9e5-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="da9e5-116">次の経費にどの原価勘定を使用するか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="da9e5-117">原価</span><span class="sxs-lookup"><span data-stu-id="da9e5-117">Cost</span></span>
        - <span data-ttu-id="da9e5-118">給与配賦</span><span class="sxs-lookup"><span data-stu-id="da9e5-118">Payroll allocation</span></span>
        - <span data-ttu-id="da9e5-119">仕掛品コスト値</span><span class="sxs-lookup"><span data-stu-id="da9e5-119">WIP-cost value</span></span>
        - <span data-ttu-id="da9e5-120">コスト項目</span><span class="sxs-lookup"><span data-stu-id="da9e5-120">Cost-item</span></span>
        - <span data-ttu-id="da9e5-121">仕掛品コスト値項目</span><span class="sxs-lookup"><span data-stu-id="da9e5-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="da9e5-122">発生損失</span><span class="sxs-lookup"><span data-stu-id="da9e5-122">Accrued loss</span></span>
        - <span data-ttu-id="da9e5-123">仕掛品発生損失</span><span class="sxs-lookup"><span data-stu-id="da9e5-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="da9e5-124">次の収益要因にどの収益勘定を使用するか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="da9e5-125">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="da9e5-125">Invoiced revenue</span></span>
        - <span data-ttu-id="da9e5-126">未収売上の販売額</span><span class="sxs-lookup"><span data-stu-id="da9e5-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="da9e5-127">仕掛品販売額</span><span class="sxs-lookup"><span data-stu-id="da9e5-127">WIP-sales value</span></span>
        - <span data-ttu-id="da9e5-128">未収収益 - 生産</span><span class="sxs-lookup"><span data-stu-id="da9e5-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="da9e5-129">仕掛品 - 生産</span><span class="sxs-lookup"><span data-stu-id="da9e5-129">WIP-production</span></span>
        - <span data-ttu-id="da9e5-130">未収収益 - 利益</span><span class="sxs-lookup"><span data-stu-id="da9e5-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="da9e5-131">仕掛品利益</span><span class="sxs-lookup"><span data-stu-id="da9e5-131">WIP-profit</span></span>
        - <span data-ttu-id="da9e5-132">未収売上サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="da9e5-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="da9e5-133">仕掛品サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="da9e5-133">WIP-subscription</span></span>

- <span data-ttu-id="da9e5-134">どのような経費の種類か?</span><span class="sxs-lookup"><span data-stu-id="da9e5-134">What is the expense type?</span></span>
- <span data-ttu-id="da9e5-135">経費カテゴリの既定の支払方法はなにか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="da9e5-136">経費カテゴリの経費は項目別にする必要があるか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="da9e5-137">経費カテゴリの既定の主勘定はなにか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="da9e5-138">経費カテゴリの既定の品目消費税グループはなにか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="da9e5-139">経費カテゴリに対して追加の支払方法は許可されているか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="da9e5-140">そうである場合、どのようなものか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-140">If so, what are they?</span></span>
- <span data-ttu-id="da9e5-141">この経費カテゴリにサブカテゴリはあるか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="da9e5-142">サブカテゴリがある場合、次の決定をする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="da9e5-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="da9e5-143">税の回収から除外されているサブカテゴリはあるか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="da9e5-144">サブカテゴリの品目消費税グループはなにか?</span><span class="sxs-lookup"><span data-stu-id="da9e5-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]