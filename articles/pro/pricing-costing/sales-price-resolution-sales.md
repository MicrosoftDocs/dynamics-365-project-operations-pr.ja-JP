---
title: プロジェクトの見積もりと実績の販売価格を解決する
description: このトピックは、プロジェクトの見積もりと実績の販売価格がどのように解決されるかについての情報を提供します。
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ac7b8ca7dfc5679b0acb1a984bb7663552d66b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004336"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a><span data-ttu-id="0e90a-103">プロジェクトの見積もりと実績の販売価格を解決する</span><span class="sxs-lookup"><span data-stu-id="0e90a-103">Resolve sales prices for project estimates and actuals</span></span>

<span data-ttu-id="0e90a-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="0e90a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e90a-105">見積りおよび実績の販売価格が Dynamics 365 Project Operations で解決されると、システムは最初に、関連するプロジェクトの見積もりまたは契約の日付と通貨を使用して、販売価格リストを解決します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-105">When sales prices on estimates and actuals are resolved in Dynamics 365 Project Operations, the system first uses the date and currency of the related project quote or contract to resolve the sales price list.</span></span> <span data-ttu-id="0e90a-106">販売価格リストが解決された後、システムは販売または請求レートを解決します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-106">After the sales price list is resolved, the system resolves the sales or bill rate.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="0e90a-107">時間に向けた実際の明細行と見積もり明細行での販売率の解決</span><span class="sxs-lookup"><span data-stu-id="0e90a-107">Resolve sales rates on actual and estimate lines for time</span></span>

<span data-ttu-id="0e90a-108">Project Operations では、時間の見積もり明細行は、時間の見積もり明細行と契約ラインの詳細、およびプロジェクトのリソース割り当てを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-108">In Project Operations, estimate lines for time are used to denote the quote line and contract line details for time and the resource assignments on the project.</span></span>

<span data-ttu-id="0e90a-109">販売の価格表が解決された後、システムは次の手順を実行して、請求レートを規定に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-109">After a price list for sales is resolved, the system completes the following steps to default the bill rate.</span></span>

1. <span data-ttu-id="0e90a-110">原価価格のリストが解決された後、システムは、解決済みの価格表のロール価格明細に対して一致させるために、時間の見積もり明細上の **ロール** フィールドと **リソース単位** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-110">The system uses the **Role** and **Resourcing Unit** fields on the estimate line for time, to match against the role price lines in the resolved price list.</span></span> <span data-ttu-id="0e90a-111">この一致は、請求レートの標準の価格ディメンションが使用されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="0e90a-111">This matching assumes that out-of-box pricing dimensions for bill rates are being used.</span></span> <span data-ttu-id="0e90a-112">**ロール** と **リソース単位** 以外、またはこれらに加えてその他のフィールドに基づいて価格を構成した場合は、それが一致するロールの価格明細行を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-112">If you have configured pricing based on any other fields instead of, or in addition to **Role** and **Resourcing Unit**, then that is the combination that will be used to retrieve a matching role price line.</span></span>
2. <span data-ttu-id="0e90a-113">システムが **ロール** と **リソース単位** の組み合わせの請求レートを持つロール価格明細行ンを検出した場合、それが既定の請求レートとなります。</span><span class="sxs-lookup"><span data-stu-id="0e90a-113">If the system finds a role price line that has a bill rate for the **Role** and **Resourcing Unit** field combination, then that bill rate is defaulted.</span></span>
3. <span data-ttu-id="0e90a-114">システムが **ロール** フィールドと **リソース単位** フィールドの値を一致させることができない場合、一致するロールを持つロール価格明細行を取得しますが、**リソース単位** の null 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-114">If the system is unable to match the **Role** and **Resourcing Unit** field values, then it retrieves role price lines with a matching role but null values of **Resource Unit**.</span></span> <span data-ttu-id="0e90a-115">システムが一致するロールの価格レコードを見つけると、そのレコードから請求レートが規定に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-115">After the system finds a matching role price record, it will default the bill rate from that record.</span></span> <span data-ttu-id="0e90a-116">この一致は、販売価格ディメンションとして、**ロール** 対 **リソース単位** の相対的な優先度に対する標準構成を前提としています。</span><span class="sxs-lookup"><span data-stu-id="0e90a-116">This matching assumes an out-of-the-box configuration for the relative priority of **Role** vs **Resourcing Unit** as a sales pricing dimension.</span></span>

> [!NOTE]
> <span data-ttu-id="0e90a-117">**ロール**、**リソース単位**  の優先順位が異なる構成になっている場合や、優先順位の高い他のディメンジョンがある場合は、それに応じてこの動作が変化します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-117">If you configured a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="0e90a-118">システムは、各価格設定ディメンション値のそれぞれに一致する値を持つロール価格レコードを優先度の高い順に取得し、それらのディメンションの null 値を持つ行が最後に来るようにします。</span><span class="sxs-lookup"><span data-stu-id="0e90a-118">The system retrieves the role price records with matching values of each of the pricing dimension values in the order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="0e90a-119">経費に向けた実際の明細行と見積もり明細行での販売率の解決</span><span class="sxs-lookup"><span data-stu-id="0e90a-119">Resolve sales rates on actual and estimate lines for expense</span></span>

<span data-ttu-id="0e90a-120">Project Operations では、経費の見積もり明細行が、経費の見積もり明細行と契約品目の詳細、およびプロジェクトの経費見積もり明細行を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-120">In Project Operations, estimate lines for expense are used to denote the quote line and contract line details for expenses and the expense estimate lines on the project.</span></span>

<span data-ttu-id="0e90a-121">販売の価格表が解決された後、システムは次の手順を実行して、単位販売価格を規定に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-121">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="0e90a-122">システムは見積り明細行の **カテゴリ** と **単位** フィールドの組み合わせを使用して、解決された価格表のカテゴリ価格明細行と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="0e90a-122">The system uses the **Category** and **Unit** field combination on the estimate line for expense to match against the category price lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="0e90a-123">システムが **カテゴリ** と **単位** フィールドの組み合わせで原価率を持つカテゴリ価格ラインを検出した場合、販売率が既定になります。</span><span class="sxs-lookup"><span data-stu-id="0e90a-123">If the system finds a category price line that has a sales rate for the **Category** and **Unit** field combination, then that sales rate is defaulted.</span></span>
3. <span data-ttu-id="0e90a-124">システムが一致するカテゴリの価格明細行を見つけた場合、価格設定方法を使用して販売価格を規定に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-124">If the system finds a matching category price line, the pricing method may be used to default the sales price.</span></span> <span data-ttu-id="0e90a-125">次の表は、プロジェクト運用における経費価格の規定設定をする動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="0e90a-125">The following table below shows the expense price defaulting behavior in Project Operations.</span></span>

    | <span data-ttu-id="0e90a-126">コンテキスト</span><span class="sxs-lookup"><span data-stu-id="0e90a-126">Context</span></span> | <span data-ttu-id="0e90a-127">価格設定方法</span><span class="sxs-lookup"><span data-stu-id="0e90a-127">Pricing method</span></span> | <span data-ttu-id="0e90a-128">既定の価格</span><span class="sxs-lookup"><span data-stu-id="0e90a-128">Price defaulted</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="0e90a-129">見積もり</span><span class="sxs-lookup"><span data-stu-id="0e90a-129">Estimate</span></span> | <span data-ttu-id="0e90a-130">出荷単位ごとの価格</span><span class="sxs-lookup"><span data-stu-id="0e90a-130">Price per unit</span></span> | <span data-ttu-id="0e90a-131">カテゴリ価格表に基づく</span><span class="sxs-lookup"><span data-stu-id="0e90a-131">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="0e90a-132">コスト</span><span class="sxs-lookup"><span data-stu-id="0e90a-132">At cost</span></span> | <span data-ttu-id="0e90a-133">0.00</span><span class="sxs-lookup"><span data-stu-id="0e90a-133">0.00</span></span> |
    | &nbsp; | <span data-ttu-id="0e90a-134">コストにマークアップ</span><span class="sxs-lookup"><span data-stu-id="0e90a-134">Markup over cost</span></span> | <span data-ttu-id="0e90a-135">0.00</span><span class="sxs-lookup"><span data-stu-id="0e90a-135">0.00</span></span> |
    | <span data-ttu-id="0e90a-136">実績</span><span class="sxs-lookup"><span data-stu-id="0e90a-136">Actual</span></span> | <span data-ttu-id="0e90a-137">出荷単位ごとの価格</span><span class="sxs-lookup"><span data-stu-id="0e90a-137">Price per unit</span></span> | <span data-ttu-id="0e90a-138">カテゴリ価格表に基づく</span><span class="sxs-lookup"><span data-stu-id="0e90a-138">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="0e90a-139">コスト</span><span class="sxs-lookup"><span data-stu-id="0e90a-139">At cost</span></span> | <span data-ttu-id="0e90a-140">実際の関連コストに基づく</span><span class="sxs-lookup"><span data-stu-id="0e90a-140">Based on the related cost actual</span></span> |
    | &nbsp; | <span data-ttu-id="0e90a-141">コストにマークアップ</span><span class="sxs-lookup"><span data-stu-id="0e90a-141">Markup over cost</span></span> | <span data-ttu-id="0e90a-142">カテゴリ価格ラインで定義された利幅を、実際の関連コストの単価に適用します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-142">Apply a markup as defined by the category price line on the unit cost rate of the related cost actual</span></span> |

4. <span data-ttu-id="0e90a-143">システムが **カテゴリ** と **単位** フィールド値と一致することができない場合、販売率は規定でゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="0e90a-143">If the system is unable to match the **Category** and **Unit** field values, the sales rate defaults to zero(0).</span></span>

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="0e90a-144">材料の実績と見積もり行の販売率を解決する</span><span class="sxs-lookup"><span data-stu-id="0e90a-144">Resolving sales rates on actual and estimate lines for Material</span></span>

<span data-ttu-id="0e90a-145">Project Operations で、材料の見積もり行は、材料の見積もり行および契約品目の詳細と、プロジェクトの材料見積もり行を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-145">In Project Operations, estimate lines for material are used to denote the quote line and contract line details for materials and the material estimate lines on the project.</span></span>

<span data-ttu-id="0e90a-146">販売の価格表が解決された後、システムは次の手順を実行して、単位販売価格を規定に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-146">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="0e90a-147">システムは、材料の見積もり行の **製品** と **単位** フィールドの組み合わせを使って、解決された価格表の価格表品目行と照合します。</span><span class="sxs-lookup"><span data-stu-id="0e90a-147">The system uses the **Product** and **Unit** field combination on the estimate line for material to match against the price list item lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="0e90a-148">システムが、**製品** と **単位** フィールドの組み合わせの販売率を持つ価格表アイテム行を見つけ、価格設定方法が **通貨金額** である場合、価格表行で指定された販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e90a-148">If the system finds a price list item line that has a sales rate for the **Product** and **Unit** field combination and the pricing method is **Currency amount**, the sales price that is specified on the price list line is used.</span></span>
3. <span data-ttu-id="0e90a-149">**製品** と **単位** フィールドが一致しない場合、販売率は既定でゼロになります。</span><span class="sxs-lookup"><span data-stu-id="0e90a-149">If the **Product** and **Unit** field values aren't a match, the sales rate defaults to zero.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
