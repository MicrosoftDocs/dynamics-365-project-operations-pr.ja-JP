---
title: 経費管理の構成
description: この記事では、Microsoft Dynamics 365 Finance で経費管理を構成する前の計画プロセスで考慮すべき事項と行う必要がある決定について説明します。
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079416"
---
# <a name="configure-expense-management"></a><span data-ttu-id="697bc-103">経費管理の構成</span><span class="sxs-lookup"><span data-stu-id="697bc-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="697bc-104">このトピックでは、経費管理を構成する前の計画プロセスで考慮すべき事項と行う必要がある決定について説明します。</span><span class="sxs-lookup"><span data-stu-id="697bc-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="697bc-105">経費管理では、支払い方法、出張申請書、経費報告書、ポリシーなどに関する情報を保存できます。</span><span class="sxs-lookup"><span data-stu-id="697bc-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="697bc-106">経費管理の構成を計画するときに行う決定の多くは、組織の階層と財務構造に基づいているため、これらの領域の計画書を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="697bc-107">会社間経費</span><span class="sxs-lookup"><span data-stu-id="697bc-107">Intercompany expenses</span></span>

<span data-ttu-id="697bc-108">会社間経費を有効にすると、法人および従業員が別の法人に代わって経費を負担し、組織内の雇用法人から支払いを受けることができます。</span><span class="sxs-lookup"><span data-stu-id="697bc-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="697bc-109">たとえば、法人 A の従業員が法人 B のプロジェクトを完了すると、そのプロジェクトには旅費関連の費用が発生するとします。</span><span class="sxs-lookup"><span data-stu-id="697bc-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="697bc-110">会社間経費が有効になっている場合、従業員は経費を法人 B に転記する経費報告書を提出でき、その経費は法人 A が支払う必要があります。組織に複数の法人がない場合は、会社間経費を有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="697bc-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="697bc-111">**決定:** 会社間経費を有効にするか?</span><span class="sxs-lookup"><span data-stu-id="697bc-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="697bc-112">財務管理</span><span class="sxs-lookup"><span data-stu-id="697bc-112">Financial management</span></span>

<span data-ttu-id="697bc-113">経費管理は、組織の財務管理と密に統合されています。</span><span class="sxs-lookup"><span data-stu-id="697bc-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="697bc-114">経費管理の構成の多くは、組織の財務について行った決定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="697bc-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="697bc-115">次のセクションでは、組織の財務上の決定とリーダーシップ チームからのガイダンスに基づいて、計画と決定が必要なさまざまな領域について説明します。</span><span class="sxs-lookup"><span data-stu-id="697bc-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="697bc-116">日当</span><span class="sxs-lookup"><span data-stu-id="697bc-116">Per diems</span></span>

<span data-ttu-id="697bc-117">組織が提供する従業員の日当を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="697bc-118">日当は通常、食事、宿泊、その他の付随的費用などの費用を賄うために使用されるため、組織が提供する日当のルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="697bc-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="697bc-119">日当レートは、時期、出張先、または両方を基準にすることができます。</span><span class="sxs-lookup"><span data-stu-id="697bc-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="697bc-120">日当ルールを定義すると、従業者が無料の食事やサービスを受けた場合に、日当レートから天引される割合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="697bc-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="697bc-121">また、日当レート層を定義して、従業者の出張に適用できる日当レートの最小時間数と最大時間数を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="697bc-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="697bc-122">**決定:**</span><span class="sxs-lookup"><span data-stu-id="697bc-122">**Decisions:**</span></span>

- <span data-ttu-id="697bc-123">初日と最終日の既定の日当ルール:</span><span class="sxs-lookup"><span data-stu-id="697bc-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="697bc-124">従業員が 1 日分請求して日当をもらえる最小時間数は?</span><span class="sxs-lookup"><span data-stu-id="697bc-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="697bc-125">初日と最終日の食事に支給される金額に減額はあるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="697bc-126">減額される場合、減額率は何パーセントか?</span><span class="sxs-lookup"><span data-stu-id="697bc-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="697bc-127">初日と最終日の宿泊に支給される金額に減額はあるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="697bc-128">減額される場合、減額率は何パーセントか?</span><span class="sxs-lookup"><span data-stu-id="697bc-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="697bc-129">初日と最終日に発生するその他の経費に支給される金額に減額はあるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="697bc-130">減額される場合、減額率は何パーセントか?</span><span class="sxs-lookup"><span data-stu-id="697bc-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="697bc-131">既定の日当ルール:</span><span class="sxs-lookup"><span data-stu-id="697bc-131">Default per diem rules:</span></span>

    - <span data-ttu-id="697bc-132">たとえば、食事が無料の場合、1 食あたりの食事手当に減額率があるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="697bc-133">減額される場合、1 食あたりの減額率は何パーセントか?</span><span class="sxs-lookup"><span data-stu-id="697bc-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="697bc-134">食事代の減額は、1 日あたり、1 回の出張あたり、または 1 日あたりの食事回数で計算されるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="697bc-135">日当の金額は、規則的に四捨五入するか、切り上げるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="697bc-136">日当は 24 時間または暦日で計算されるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="697bc-137">場所に基づく日当ルール:</span><span class="sxs-lookup"><span data-stu-id="697bc-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="697bc-138">日当は場所によって異なるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="697bc-139">どのような場所が含まれるのか?</span><span class="sxs-lookup"><span data-stu-id="697bc-139">What locations are included?</span></span>
    - <span data-ttu-id="697bc-140">日当が場所によって異なる場合、場所ごとに、次の種類の費用に対して何パーセントの金額が支給されるか:</span><span class="sxs-lookup"><span data-stu-id="697bc-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="697bc-141">食事</span><span class="sxs-lookup"><span data-stu-id="697bc-141">Meals</span></span>
        - <span data-ttu-id="697bc-142">宿泊</span><span class="sxs-lookup"><span data-stu-id="697bc-142">Hotel</span></span>
        - <span data-ttu-id="697bc-143">その他の経費</span><span class="sxs-lookup"><span data-stu-id="697bc-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="697bc-144">経費管理の仕訳と勘定</span><span class="sxs-lookup"><span data-stu-id="697bc-144">Expense management journals and accounts</span></span>

<span data-ttu-id="697bc-145">経費管理では、複数の仕訳や勘定科目を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="697bc-146">例えば、現金前払いとクレジットカードに同じ口座を使用するかどうかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="697bc-147">**決定:**</span><span class="sxs-lookup"><span data-stu-id="697bc-147">**Decisions:**</span></span>

- <span data-ttu-id="697bc-148">承認済経費報告書が転記される仕訳元帳は?</span><span class="sxs-lookup"><span data-stu-id="697bc-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="697bc-149">現金前払いに使用される口座は?</span><span class="sxs-lookup"><span data-stu-id="697bc-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="697bc-150">現金前払いはすぐに転記するべきか?</span><span class="sxs-lookup"><span data-stu-id="697bc-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="697bc-151">支払方法</span><span class="sxs-lookup"><span data-stu-id="697bc-151">Payment methods</span></span>

<span data-ttu-id="697bc-152">従業員がビジネスのために経費を支出することを許可する場合、従業員が使用できる支払い方法を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="697bc-153">たとえば、従業員が現金や会社のクレジット カードを使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="697bc-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="697bc-154">また、従業員が個人のクレジット カードを使用することを許可し、従業員に払い戻しを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="697bc-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="697bc-155">許可する支払方法ごとに、次の決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="697bc-156">**決定:**</span><span class="sxs-lookup"><span data-stu-id="697bc-156">**Decisions:**</span></span>

- <span data-ttu-id="697bc-157">どのような支払い方法が許可されているか?</span><span class="sxs-lookup"><span data-stu-id="697bc-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="697bc-158">支払い方法の費用は誰が負担するか?</span><span class="sxs-lookup"><span data-stu-id="697bc-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="697bc-159">相手勘定の種類はあるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-159">Is there an offset account type?</span></span> <span data-ttu-id="697bc-160">相手勘定の種類がある場合、それは何か?</span><span class="sxs-lookup"><span data-stu-id="697bc-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="697bc-161">相手勘定がある場合、その勘定は何か?</span><span class="sxs-lookup"><span data-stu-id="697bc-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="697bc-162">支払い方法がクレジット カードの場合、インポートされた取引でのみ使用する必要があるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="697bc-163">経費カテゴリと共有カテゴリ</span><span class="sxs-lookup"><span data-stu-id="697bc-163">Expense categories and shared categories</span></span>

<span data-ttu-id="697bc-164">従業員が経費報告書を作成するとき、記録する各経費は経費カテゴリに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="697bc-165">経費カテゴリは、組織内の法人間で共有される共有カテゴリから派生します。</span><span class="sxs-lookup"><span data-stu-id="697bc-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="697bc-166">これらのカテゴリは、組織の定義方法に応じて、プロジェクト管理と会計で共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="697bc-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="697bc-167">組織の定義および実装チームからのガイダンスに基づいて、経費管理で使用されるカテゴリを経費管理でのみ使用するか、プロジェクト管理と経理および経費管理の間で共有する必要があるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="697bc-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="697bc-168">これらのカテゴリは、プロジェクトと経費あるいはプロジェクトと運用の間で共有できますが、経費と運用の間では共有できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="697bc-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="697bc-169">経費カテゴリごとに次の決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="697bc-170">**決定:**</span><span class="sxs-lookup"><span data-stu-id="697bc-170">**Decisions:**</span></span>

- <span data-ttu-id="697bc-171">どのような経費カテゴリか?</span><span class="sxs-lookup"><span data-stu-id="697bc-171">What is the expense category?</span></span> <span data-ttu-id="697bc-172">例として、フライト、ホテル、またはマイレージのカテゴリなどがあります。</span><span class="sxs-lookup"><span data-stu-id="697bc-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="697bc-173">経費カテゴリは、プロジェクト管理と会計でも使用することができるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="697bc-174">どのような経費の種類か?</span><span class="sxs-lookup"><span data-stu-id="697bc-174">What is the expense type?</span></span>
- <span data-ttu-id="697bc-175">経費カテゴリの既定の支払方法はなにか?</span><span class="sxs-lookup"><span data-stu-id="697bc-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="697bc-176">経費カテゴリの経費は項目別にする必要があるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="697bc-177">経費カテゴリの既定の主勘定はなにか?</span><span class="sxs-lookup"><span data-stu-id="697bc-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="697bc-178">経費カテゴリの既定の品目消費税グループはなにか?</span><span class="sxs-lookup"><span data-stu-id="697bc-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="697bc-179">経費カテゴリに対して追加の支払方法は許可されているか?</span><span class="sxs-lookup"><span data-stu-id="697bc-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="697bc-180">追加の支払い方法が許可されている場合、それらは何か?</span><span class="sxs-lookup"><span data-stu-id="697bc-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="697bc-181">この経費カテゴリにサブカテゴリはあるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="697bc-182">サブカテゴリがある場合、次の決定をする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="697bc-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="697bc-183">税の回収から除外されているサブカテゴリはあるか?</span><span class="sxs-lookup"><span data-stu-id="697bc-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="697bc-184">サブカテゴリの品目消費税グループはなにか?</span><span class="sxs-lookup"><span data-stu-id="697bc-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="697bc-185">経費カテゴリがプロジェクト管理と会計でも使用されている場合は、残りの質問に答えてください。</span><span class="sxs-lookup"><span data-stu-id="697bc-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="697bc-186">それ以外の場合は、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="697bc-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="697bc-187">次の経費にどの原価勘定を使用するか?</span><span class="sxs-lookup"><span data-stu-id="697bc-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="697bc-188">原価</span><span class="sxs-lookup"><span data-stu-id="697bc-188">Cost</span></span>
    - <span data-ttu-id="697bc-189">給与配賦</span><span class="sxs-lookup"><span data-stu-id="697bc-189">Payroll allocation</span></span>
    - <span data-ttu-id="697bc-190">仕掛品コスト値</span><span class="sxs-lookup"><span data-stu-id="697bc-190">WIP-cost value</span></span>
    - <span data-ttu-id="697bc-191">コスト項目</span><span class="sxs-lookup"><span data-stu-id="697bc-191">Cost-item</span></span>
    - <span data-ttu-id="697bc-192">仕掛品コスト値項目</span><span class="sxs-lookup"><span data-stu-id="697bc-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="697bc-193">発生損失</span><span class="sxs-lookup"><span data-stu-id="697bc-193">Accrued loss</span></span>
    - <span data-ttu-id="697bc-194">仕掛品発生損失</span><span class="sxs-lookup"><span data-stu-id="697bc-194">WIP-accrued loss</span></span>

- <span data-ttu-id="697bc-195">次の項目にどの収益勘定を使用するか?</span><span class="sxs-lookup"><span data-stu-id="697bc-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="697bc-196">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="697bc-196">Invoiced revenue</span></span>
    - <span data-ttu-id="697bc-197">未収売上の販売額</span><span class="sxs-lookup"><span data-stu-id="697bc-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="697bc-198">仕掛品販売額</span><span class="sxs-lookup"><span data-stu-id="697bc-198">WIP-sales value</span></span>
    - <span data-ttu-id="697bc-199">未収売上生産</span><span class="sxs-lookup"><span data-stu-id="697bc-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="697bc-200">仕掛品生産</span><span class="sxs-lookup"><span data-stu-id="697bc-200">WIP-production</span></span>
    - <span data-ttu-id="697bc-201">未収売上利益</span><span class="sxs-lookup"><span data-stu-id="697bc-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="697bc-202">仕掛品利益</span><span class="sxs-lookup"><span data-stu-id="697bc-202">WIP-profit</span></span>
    - <span data-ttu-id="697bc-203">未収売上サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="697bc-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="697bc-204">仕掛品サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="697bc-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="697bc-205">税金</span><span class="sxs-lookup"><span data-stu-id="697bc-205">Taxes</span></span>

<span data-ttu-id="697bc-206">経費関連の税金については、経費報告書に何を含めるか、または有効にするかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="697bc-207">**決定:**</span><span class="sxs-lookup"><span data-stu-id="697bc-207">**Decisions:**</span></span>

- <span data-ttu-id="697bc-208">消費税は経費に含まれているのか?</span><span class="sxs-lookup"><span data-stu-id="697bc-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="697bc-209">経費での税金回収は有効にすべきか?</span><span class="sxs-lookup"><span data-stu-id="697bc-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="697bc-210">総勘定元帳を計画していたときに、米国の消費税と使用税のルールを適用することにした場合、経費の税金回収を有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="697bc-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="697bc-211">(米国の消費税と使用税のルールを適用するには、 **消費税課税ルールの適用** オプションを **はい** に設定します。)</span><span class="sxs-lookup"><span data-stu-id="697bc-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="697bc-212">ポリシー</span><span class="sxs-lookup"><span data-stu-id="697bc-212">Policies</span></span>

<span data-ttu-id="697bc-213">経費報告のポリシーを作成することにより、従業員が組織に代わって経費を負担するときに、組織が時間と費用を節約できます。</span><span class="sxs-lookup"><span data-stu-id="697bc-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="697bc-214">ポリシーは、従業員が予算内にとどまり、必要なすべての情報を提供し、必要なときにのみ費用を使うことを保証します。</span><span class="sxs-lookup"><span data-stu-id="697bc-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="697bc-215">作成する経費報告書ポリシーと経費報告書承認ポリシーごとに、次の決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="697bc-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="697bc-216">**決定:**</span><span class="sxs-lookup"><span data-stu-id="697bc-216">**Decisions:**</span></span>

- <span data-ttu-id="697bc-217">ポリシーの名前は?</span><span class="sxs-lookup"><span data-stu-id="697bc-217">What is the name of the policy?</span></span>
- <span data-ttu-id="697bc-218">何のための経費ポリシーか?</span><span class="sxs-lookup"><span data-stu-id="697bc-218">What is the expense policy for?</span></span>
- <span data-ttu-id="697bc-219">以前に会社間経費を有効にすることを決定した場合、このポリシーは組織内のどの会社に適用されるのか?</span><span class="sxs-lookup"><span data-stu-id="697bc-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="697bc-220">ポリシーはいつ発効するのか?</span><span class="sxs-lookup"><span data-stu-id="697bc-220">When does the policy become effective?</span></span>
- <span data-ttu-id="697bc-221">ポリシーの有効期限は?</span><span class="sxs-lookup"><span data-stu-id="697bc-221">When does the policy expire?</span></span>
- <span data-ttu-id="697bc-222">ポリシー ルールとは何か?</span><span class="sxs-lookup"><span data-stu-id="697bc-222">What is the policy rule?</span></span>
- <span data-ttu-id="697bc-223">ポリシー ルールの結果は何か?</span><span class="sxs-lookup"><span data-stu-id="697bc-223">What is the outcome of the policy rule?</span></span>
