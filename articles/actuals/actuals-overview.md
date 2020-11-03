---
title: 実績
description: このトピックでは、Microsoft Dynamics 365 Project Operations における実績の使用方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079258"
---
# <a name="actuals"></a><span data-ttu-id="ff5b8-103">実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-103">Actuals</span></span> 

<span data-ttu-id="ff5b8-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ff5b8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ff5b8-105">実績とはプロジェクトで完了した作業の量です。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="ff5b8-106">それは、時間と経費の入力、および仕訳入力と請求書の結果として作成されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="ff5b8-107">仕訳帳明細行と時間の送信</span><span class="sxs-lookup"><span data-stu-id="ff5b8-107">Journal lines and time submission</span></span>

<span data-ttu-id="ff5b8-108">時間エントリの詳細については、[時間エントリの概要](../time/time-entry-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ff5b8-109">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ff5b8-109">Time and materials</span></span>

<span data-ttu-id="ff5b8-110">送信された時間エントリが、時間と材料の契約品目にマップされているプロジェクトにリンクされている場合、システムは 2 つの仕訳帳明細行を作成します。1 つはコスト用、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ff5b8-111">固定価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-111">Fixed price</span></span>

<span data-ttu-id="ff5b8-112">送信されるプロジェクトの時間エントリが固定価格の契約品目にマップされているプロジェクトにリンクされると、システムによってコストの仕訳帳明細行が 1 つ作成されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ff5b8-113">既定の価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-113">Default pricing</span></span>

<span data-ttu-id="ff5b8-114">既定の価格を作成するロジックは仕訳帳明細行にあります。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="ff5b8-115">時間エントリのフィールド値が仕訳帳明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="ff5b8-116">これらの値には、トランザクションの日付、プロジェクトがマップされる契約品目、適切な価格表の通貨結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="ff5b8-117">**ロール** や **組織単位** など既定の価格に影響するフィールドが、仕訳帳明細行の適切な価格を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ff5b8-118">時間エントリにカスタム フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="ff5b8-119">フィールド値に実績を伝播する場合は、実績エンティティのフィールドを作成して、フィールド マッピングで時間エントリから実績にフィールドをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="ff5b8-120">仕訳帳明細行と基本経費の送信</span><span class="sxs-lookup"><span data-stu-id="ff5b8-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="ff5b8-121">経費エントリの詳細については、[経費の概要](../expense/expense-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ff5b8-122">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ff5b8-122">Time and materials</span></span>

<span data-ttu-id="ff5b8-123">送信される基本経費が、時間と材料の契約品目にマップされているプロジェクトにリンクされている場合、システムは 2 つの仕訳帳明細行を作成します。1 つはコスト用、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ff5b8-124">固定価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-124">Fixed price</span></span>

<span data-ttu-id="ff5b8-125">送信されるプロジェクトの基本経費エントリが固定価格の契約品目にマップされているプロジェクトにリンクされると、システムによってコストの仕訳帳明細行が 1 つ作成されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ff5b8-126">既定の価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-126">Default pricing</span></span>

<span data-ttu-id="ff5b8-127">経費の既定価格を入力するためのロジックは、経費カテゴリに基づいています。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="ff5b8-128">取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ff5b8-129">ただし、既定で価格自体について入力した金額は原価と販売に関連する経費の仕訳帳明細行に直接設定されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="ff5b8-130">経費入力で、単位ごとの既定価格のカテゴリ ベースのエントリは使用できません。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="ff5b8-131">仕訳帳を使用してコストを記録する</span><span class="sxs-lookup"><span data-stu-id="ff5b8-131">Use entry journals to record costs</span></span>

<span data-ttu-id="ff5b8-132">仕訳帳を使用して、材料、料金、時間、経費、税のトランザクション クラスでコストや収益を記録できます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ff5b8-133">仕訳帳は、次の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="ff5b8-134">プロジェクトで材料の実際のコストと売上を記録します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="ff5b8-135">トランザクションの実績を別のシステムから Microsoft Dynamics 365 Project Operations に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="ff5b8-136">別のシステムで発生したコストを記録します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="ff5b8-137">これらのコストには、調達コストまたは下請けコストが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff5b8-138">アプリケーションは、仕訳明細タイプまたは仕訳明細行に入力された関連価格を検証しません。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ff5b8-139">したがって、実績がプロジェクトに与える会計上の影響を十分に認識しているユーザーのみが、仕訳帳を使用して実績を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="ff5b8-140">この仕訳の種類が影響を与えるため、仕訳帳を作成するためのアクセス権を持つユーザーを慎重に選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="ff5b8-141">プロジェクト イベントに基づく実績を記録する</span><span class="sxs-lookup"><span data-stu-id="ff5b8-141">Record actuals based on project events</span></span>

<span data-ttu-id="ff5b8-142">Project Operations はプロジェクト中に発生する財務取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ff5b8-143">これらの取引は 実績 として記録されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="ff5b8-144">次の表はプロジェクトが時間と材料のプロジェクトであるか、固定価格のプロジェクトであるか、プリセールス段階にあるか、内部プロジェクトであるかに応じて、作成されるさまざまなタイプの実績を示しています。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="ff5b8-145">リソースはプロジェクトの契約単位と同じ組織単位に属します</span><span class="sxs-lookup"><span data-stu-id="ff5b8-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ff5b8-146">イベント</span><span class="sxs-lookup"><span data-stu-id="ff5b8-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ff5b8-147">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff5b8-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ff5b8-148">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff5b8-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ff5b8-149">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff5b8-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ff5b8-150">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ff5b8-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ff5b8-151">固定価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ff5b8-152">[実績]</span><span class="sxs-lookup"><span data-stu-id="ff5b8-152">Actuals</span></span></th>
<th><span data-ttu-id="ff5b8-153">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-153">Transaction currency</span></span></th>
<th><span data-ttu-id="ff5b8-154">固定価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-154">Fixed price</span></span></th>
<th><span data-ttu-id="ff5b8-155">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ff5b8-156">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ff5b8-157">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ff5b8-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-158">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ff5b8-159">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ff5b8-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ff5b8-160">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ff5b8-161">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-161">Cost actual</span></span></td>
<td><span data-ttu-id="ff5b8-162">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-163">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-164">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ff5b8-165">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-166">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-167">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ff5b8-168">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ff5b8-169">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ff5b8-170">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-170">Cost actual</span></span></td>
<td><span data-ttu-id="ff5b8-171">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-172">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-173">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-174">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-175">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-176">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ff5b8-177">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-178">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ff5b8-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ff5b8-179">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ff5b8-180">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ff5b8-181">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ff5b8-182">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-183">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-184">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-185">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-186">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-187">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-187">Billed sales</span></span></td>
<td><span data-ttu-id="ff5b8-188">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ff5b8-189">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ff5b8-190">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ff5b8-191">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-192">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-193">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-194">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-195">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-196">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ff5b8-197">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-198">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ff5b8-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ff5b8-199">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ff5b8-200">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ff5b8-201">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ff5b8-202">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ff5b8-203">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="ff5b8-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ff5b8-204">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="ff5b8-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ff5b8-205">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-206">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-207">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-208">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-208">Billed sales</span></span></td>
<td><span data-ttu-id="ff5b8-209">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ff5b8-210">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ff5b8-211">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ff5b8-212">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-213">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ff5b8-214">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-215">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ff5b8-216">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="ff5b8-217">リソースがプロジェクトの契約単位と異なる組織単位に属します</span><span class="sxs-lookup"><span data-stu-id="ff5b8-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ff5b8-218">イベント</span><span class="sxs-lookup"><span data-stu-id="ff5b8-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ff5b8-219">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff5b8-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ff5b8-220">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff5b8-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ff5b8-221">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff5b8-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ff5b8-222">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ff5b8-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ff5b8-223">固定価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ff5b8-224">[実績]</span><span class="sxs-lookup"><span data-stu-id="ff5b8-224">Actuals</span></span></th>
<th><span data-ttu-id="ff5b8-225">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-225">Transaction currency</span></span></th>
<th><span data-ttu-id="ff5b8-226">固定価格</span><span class="sxs-lookup"><span data-stu-id="ff5b8-226">Fixed price</span></span></th>
<th><span data-ttu-id="ff5b8-227">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ff5b8-228">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ff5b8-229">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ff5b8-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-230">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ff5b8-231">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ff5b8-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ff5b8-232">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ff5b8-233">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-233">Cost actual</span></span></td>
<td><span data-ttu-id="ff5b8-234">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ff5b8-235">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ff5b8-236">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ff5b8-237">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ff5b8-238">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-239">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ff5b8-240">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-241">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ff5b8-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ff5b8-242">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ff5b8-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-243">組織間営業</span><span class="sxs-lookup"><span data-stu-id="ff5b8-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ff5b8-244">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ff5b8-245">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ff5b8-246">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-246">Cost actual</span></span></td>
<td><span data-ttu-id="ff5b8-247">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-248">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-249">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-250">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-251">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ff5b8-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-252">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ff5b8-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ff5b8-253">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ff5b8-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-254">組織間営業</span><span class="sxs-lookup"><span data-stu-id="ff5b8-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ff5b8-255">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-256">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ff5b8-257">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-258">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ff5b8-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ff5b8-259">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ff5b8-260">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ff5b8-261">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ff5b8-262">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-263">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-264">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-265">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ff5b8-266">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-267">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-267">Billed sales</span></span></td>
<td><span data-ttu-id="ff5b8-268">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ff5b8-269">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ff5b8-270">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ff5b8-271">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-272">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-273">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-274">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ff5b8-275">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-276">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ff5b8-277">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-278">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ff5b8-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ff5b8-279">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ff5b8-280">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ff5b8-281">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ff5b8-282">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ff5b8-283">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="ff5b8-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ff5b8-284">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="ff5b8-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ff5b8-285">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-286">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ff5b8-287">適用なし</span><span class="sxs-lookup"><span data-stu-id="ff5b8-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-288">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-288">Billed sales</span></span></td>
<td><span data-ttu-id="ff5b8-289">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ff5b8-290">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="ff5b8-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ff5b8-291">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ff5b8-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ff5b8-292">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-293">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ff5b8-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ff5b8-294">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ff5b8-295">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="ff5b8-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ff5b8-296">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ff5b8-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
