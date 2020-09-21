---
title: '[実績]'
description: このトピックでは、プロジェクトの実績について説明します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752918"
---
# <a name="actuals"></a><span data-ttu-id="16aa2-103">[実績]</span><span class="sxs-lookup"><span data-stu-id="16aa2-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="16aa2-104">実績とはプロジェクトで完了した作業の量です。</span><span class="sxs-lookup"><span data-stu-id="16aa2-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="16aa2-105">プロジェクトの実績はソース ドキュメントまでさかのぼることができます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="16aa2-106">これらのソース ドキュメントには、時間、経費、仕訳入力、そして請求書が含まれます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![プロジェクトの実績をソース ドキュメントまでトレースする方法](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="16aa2-108">時間エントリの送信</span><span class="sxs-lookup"><span data-stu-id="16aa2-108">Submitting a time entry</span></span>

<span data-ttu-id="16aa2-109">PSA では、時間と材料の契約品目にマップされたプロジェクトの時間エントリが送信されると、2 つの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="16aa2-110">1 つはコスト用で、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="16aa2-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="16aa2-111">固定価格の契約品目にマップされたプロジェクトの時間エントリが送信されると、仕訳帳明細行はコストのみで作成されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="16aa2-112">既定の価格を入力するロジックは仕訳帳明細行にあります。</span><span class="sxs-lookup"><span data-stu-id="16aa2-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="16aa2-113">時間エントリのすべてのフィールド値が仕訳帳明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="16aa2-114">これらのフィールドは、トランザクションの日付、プロジェクトがマップされる契約品目、適切な価格表の通貨結果を含みます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="16aa2-115">**役割** や **組織単位** など既定の価格に影響するフィールドにより、適切な価格が既定で仕訳帳明細行に入力されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="16aa2-116">時間エントリのカスタム フィールドを追加してフィールドに値と実績を伝播する場合は、実績エンティティのフィールドを作成して、フィール ドマッピングで時間エントリから実績にフィールドをコピーします。</span><span class="sxs-lookup"><span data-stu-id="16aa2-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="16aa2-117">経費エントリの送信</span><span class="sxs-lookup"><span data-stu-id="16aa2-117">Submitting an expense entry</span></span>

<span data-ttu-id="16aa2-118">PSA では、時間と材料の契約品目にマップされたプロジェクトの経費エントリが送信されると、2 つの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="16aa2-119">1 つはコスト用で、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="16aa2-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="16aa2-120">固定価格の契約品目にマップされたプロジェクトの経費エントリが送信されると、仕訳帳明細行はコストのみで作成されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="16aa2-121">経費の既定価格を入力するロジックは、**経費エントリ** ページで選択した経費カテゴリに基づきます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="16aa2-122">取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="16aa2-123">ただし、価格自体についてユーザーが入力した金額は、既定で原価と販売に関連する経費の仕訳帳明細行に直接設定されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="16aa2-124">PSA の現在のバージョンでは、経費エントリの単位ごとの既定価格のカテゴリ ベースのエントリは使用できません。</span><span class="sxs-lookup"><span data-stu-id="16aa2-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="16aa2-125">ジャーナルを使用してコストを記録する</span><span class="sxs-lookup"><span data-stu-id="16aa2-125">Using journals to record costs</span></span>

<span data-ttu-id="16aa2-126">PSA では仕訳帳を使用して、材料、料金、時間、経費、税のトランザクション クラスでコストや収益を記録できます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="16aa2-127">ジャーナルには、ヘッダー、行、**確認** の操作があります。</span><span class="sxs-lookup"><span data-stu-id="16aa2-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="16aa2-128">以下にジャーナルを使用するシナリオをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="16aa2-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="16aa2-129">プロジェクトで材料の実際のコストと売上を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16aa2-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="16aa2-130">トランザクションの実績を別のシステムから PSA に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16aa2-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="16aa2-131">調達コストや外注コストなど、別のシステムで発生したコストを記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16aa2-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="16aa2-132">プロジェクト イベントに基づく実績を記録する</span><span class="sxs-lookup"><span data-stu-id="16aa2-132">Recording actuals based on project events</span></span>

<span data-ttu-id="16aa2-133">PSA はプロジェクト中に発生する財務取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="16aa2-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="16aa2-134">これらの取引は **実績** として記録されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="16aa2-135">次の表はプロジェクトが時間と材料のプロジェクトであるか、固定価格のプロジェクトであるか、プリセールス段階にあるか、内部プロジェクトであるかに応じて、作成されるさまざまなタイプの実績を示しています。</span><span class="sxs-lookup"><span data-stu-id="16aa2-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="16aa2-136">**リソースはプロジェクトの契約単位と同じ組織単位に属します**</span><span class="sxs-lookup"><span data-stu-id="16aa2-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="16aa2-137">イベント</span><span class="sxs-lookup"><span data-stu-id="16aa2-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="16aa2-138">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="16aa2-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="16aa2-139">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="16aa2-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="16aa2-140">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="16aa2-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="16aa2-141">時間と材料</span><span class="sxs-lookup"><span data-stu-id="16aa2-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="16aa2-142">固定価格</span><span class="sxs-lookup"><span data-stu-id="16aa2-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="16aa2-143">[実績]</span><span class="sxs-lookup"><span data-stu-id="16aa2-143">Actuals</span></span></th>
<th><span data-ttu-id="16aa2-144">取引通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-144">Transaction currency</span></span></th>
<th><span data-ttu-id="16aa2-145">固定価格</span><span class="sxs-lookup"><span data-stu-id="16aa2-145">Fixed price</span></span></th>
<th><span data-ttu-id="16aa2-146">取引通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="16aa2-147">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="16aa2-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="16aa2-148">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="16aa2-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-149">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="16aa2-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="16aa2-150">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="16aa2-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16aa2-151">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="16aa2-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16aa2-152">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-152">Cost actual</span></span></td>
<td><span data-ttu-id="16aa2-153">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-154">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-155">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="16aa2-156">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-157">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-158">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="16aa2-159">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16aa2-160">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16aa2-161">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-161">Cost actual</span></span></td>
<td><span data-ttu-id="16aa2-162">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-163">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-164">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-165">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-166">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-167">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16aa2-168">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-169">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="16aa2-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16aa2-170">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16aa2-171">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="16aa2-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16aa2-172">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16aa2-173">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-174">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-175">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-176">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-177">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-178">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-178">Billed sales</span></span></td>
<td><span data-ttu-id="16aa2-179">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16aa2-180">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="16aa2-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16aa2-181">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16aa2-182">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-183">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-184">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-185">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-186">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-187">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16aa2-188">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-189">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="16aa2-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16aa2-190">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16aa2-191">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16aa2-192">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16aa2-193">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="16aa2-194">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="16aa2-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="16aa2-195">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="16aa2-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="16aa2-196">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-197">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-198">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-199">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-199">Billed sales</span></span></td>
<td><span data-ttu-id="16aa2-200">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16aa2-201">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="16aa2-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16aa2-202">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16aa2-203">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-204">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="16aa2-205">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-206">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="16aa2-207">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="16aa2-208">**リソースがプロジェクトの契約単位と異なる組織単位に属します**</span><span class="sxs-lookup"><span data-stu-id="16aa2-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="16aa2-209">イベント</span><span class="sxs-lookup"><span data-stu-id="16aa2-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="16aa2-210">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="16aa2-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="16aa2-211">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="16aa2-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="16aa2-212">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="16aa2-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="16aa2-213">時間と材料</span><span class="sxs-lookup"><span data-stu-id="16aa2-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="16aa2-214">固定価格</span><span class="sxs-lookup"><span data-stu-id="16aa2-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="16aa2-215">[実績]</span><span class="sxs-lookup"><span data-stu-id="16aa2-215">Actuals</span></span></th>
<th><span data-ttu-id="16aa2-216">取引通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-216">Transaction currency</span></span></th>
<th><span data-ttu-id="16aa2-217">固定価格</span><span class="sxs-lookup"><span data-stu-id="16aa2-217">Fixed price</span></span></th>
<th><span data-ttu-id="16aa2-218">取引通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="16aa2-219">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="16aa2-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="16aa2-220">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="16aa2-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-221">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="16aa2-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="16aa2-222">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="16aa2-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="16aa2-223">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="16aa2-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16aa2-224">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-224">Cost actual</span></span></td>
<td><span data-ttu-id="16aa2-225">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="16aa2-226">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="16aa2-227">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="16aa2-228">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="16aa2-229">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-230">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="16aa2-231">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-232">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="16aa2-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="16aa2-233">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="16aa2-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-234">組織間営業</span><span class="sxs-lookup"><span data-stu-id="16aa2-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="16aa2-235">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="16aa2-236">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16aa2-237">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-237">Cost actual</span></span></td>
<td><span data-ttu-id="16aa2-238">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-239">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-240">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-241">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-242">コストの実績</span><span class="sxs-lookup"><span data-stu-id="16aa2-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-243">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="16aa2-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="16aa2-244">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="16aa2-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-245">組織間営業</span><span class="sxs-lookup"><span data-stu-id="16aa2-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="16aa2-246">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-247">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16aa2-248">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-249">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="16aa2-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16aa2-250">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16aa2-251">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="16aa2-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16aa2-252">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16aa2-253">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-254">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-255">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-256">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="16aa2-257">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-258">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-258">Billed sales</span></span></td>
<td><span data-ttu-id="16aa2-259">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16aa2-260">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="16aa2-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16aa2-261">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16aa2-262">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-263">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-264">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-265">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16aa2-266">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-267">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16aa2-268">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-269">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="16aa2-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16aa2-270">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16aa2-271">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="16aa2-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16aa2-272">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16aa2-273">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="16aa2-274">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="16aa2-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="16aa2-275">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="16aa2-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="16aa2-276">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-277">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="16aa2-278">適用なし</span><span class="sxs-lookup"><span data-stu-id="16aa2-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-279">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-279">Billed sales</span></span></td>
<td><span data-ttu-id="16aa2-280">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16aa2-281">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="16aa2-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16aa2-282">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="16aa2-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16aa2-283">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-284">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="16aa2-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="16aa2-285">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16aa2-286">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="16aa2-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="16aa2-287">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="16aa2-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
