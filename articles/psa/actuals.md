---
title: 実績の概要
description: このトピックでは、プロジェクトの実績について説明します。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014662"
---
# <a name="actuals-overview"></a><span data-ttu-id="64ce9-103">実績の概要</span><span class="sxs-lookup"><span data-stu-id="64ce9-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="64ce9-104">実績とはプロジェクトで完了した作業の量です。</span><span class="sxs-lookup"><span data-stu-id="64ce9-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="64ce9-105">プロジェクトの実績はソース ドキュメントまでさかのぼることができます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="64ce9-106">これらのソース ドキュメントには、時間、経費、仕訳入力、そして請求書が含まれます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![プロジェクトの実績をソース ドキュメントまでトレースする方法](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="64ce9-108">時間エントリの送信</span><span class="sxs-lookup"><span data-stu-id="64ce9-108">Submitting a time entry</span></span>

<span data-ttu-id="64ce9-109">PSA では、時間と材料の契約品目にマップされたプロジェクトの時間エントリが送信されると、2 つの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="64ce9-110">1 つはコスト用で、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="64ce9-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="64ce9-111">固定価格の契約品目にマップされたプロジェクトの時間エントリが送信されると、仕訳帳明細行はコストのみで作成されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="64ce9-112">既定の価格を入力するロジックは仕訳帳明細行にあります。</span><span class="sxs-lookup"><span data-stu-id="64ce9-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="64ce9-113">時間エントリのすべてのフィールド値が仕訳帳明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="64ce9-114">これらのフィールドは、トランザクションの日付、プロジェクトがマップされる契約品目、適切な価格表の通貨結果を含みます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="64ce9-115">**役割** や **組織単位** など既定の価格に影響するフィールドにより、適切な価格が既定で仕訳帳明細行に入力されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="64ce9-116">時間エントリのカスタム フィールドを追加してフィールドに値と実績を伝播する場合は、実績エンティティのフィールドを作成して、フィール ドマッピングで時間エントリから実績にフィールドをコピーします。</span><span class="sxs-lookup"><span data-stu-id="64ce9-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="64ce9-117">経費エントリの送信</span><span class="sxs-lookup"><span data-stu-id="64ce9-117">Submitting an expense entry</span></span>

<span data-ttu-id="64ce9-118">PSA では、時間と材料の契約品目にマップされたプロジェクトの経費エントリが送信されると、2 つの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="64ce9-119">1 つはコスト用で、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="64ce9-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="64ce9-120">固定価格の契約品目にマップされたプロジェクトの経費エントリが送信されると、仕訳帳明細行はコストのみで作成されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="64ce9-121">経費の既定価格を入力するロジックは、**経費エントリ** ページで選択した経費カテゴリに基づきます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="64ce9-122">取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="64ce9-123">ただし、価格自体についてユーザーが入力した金額は、既定で原価と販売に関連する経費の仕訳帳明細行に直接設定されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="64ce9-124">PSA の現在のバージョンでは、経費エントリの単位ごとの既定価格のカテゴリ ベースのエントリは使用できません。</span><span class="sxs-lookup"><span data-stu-id="64ce9-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="64ce9-125">エントリ ジャーナルを使用してコストを記録する</span><span class="sxs-lookup"><span data-stu-id="64ce9-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="64ce9-126">PSA ではエントリ ジャーナルを使用して、材料、料金、時間、経費、税のトランザクション クラスでコストや収益を記録できます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="64ce9-127">ジャーナルには、ヘッダー、行、**確認** の操作があります。</span><span class="sxs-lookup"><span data-stu-id="64ce9-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="64ce9-128">以下にジャーナルを使用するシナリオをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="64ce9-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="64ce9-129">プロジェクトで材料の実際のコストと売上を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64ce9-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="64ce9-130">トランザクションの実績を別のシステムから PSA に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64ce9-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="64ce9-131">調達コストや外注コストなど、別のシステムで発生したコストを記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64ce9-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64ce9-132">エントリ ジャーナルを使用して実績を作成するのは、実績がプロジェクトに与える会計上の影響を完全に認識しているユーザーだけが行ってください。</span><span class="sxs-lookup"><span data-stu-id="64ce9-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="64ce9-133">これは、アプリケーションが仕訳帳明細行タイプ、または仕訳帳明細行に入力された関連する価格を検証しないためです。</span><span class="sxs-lookup"><span data-stu-id="64ce9-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="64ce9-134">この仕訳タイプの影響があるため、誰がエントリ ジャーナルを作成するためのアクセス権を与えられるかについて十分な注意を払ってください。</span><span class="sxs-lookup"><span data-stu-id="64ce9-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="64ce9-135">プロジェクト イベントに基づく実績を記録する</span><span class="sxs-lookup"><span data-stu-id="64ce9-135">Recording actuals based on project events</span></span>

<span data-ttu-id="64ce9-136">PSA はプロジェクト中に発生する財務取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="64ce9-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="64ce9-137">これらの取引は **実績** として記録されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="64ce9-138">次の表はプロジェクトが時間と材料のプロジェクトであるか、固定価格のプロジェクトであるか、プリセールス段階にあるか、内部プロジェクトであるかに応じて、作成されるさまざまなタイプの実績を示しています。</span><span class="sxs-lookup"><span data-stu-id="64ce9-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="64ce9-139">**リソースはプロジェクトの契約単位と同じ組織単位に属します**</span><span class="sxs-lookup"><span data-stu-id="64ce9-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="64ce9-140">イベント</span><span class="sxs-lookup"><span data-stu-id="64ce9-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="64ce9-141">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="64ce9-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="64ce9-142">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="64ce9-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="64ce9-143">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="64ce9-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="64ce9-144">時間と材料</span><span class="sxs-lookup"><span data-stu-id="64ce9-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="64ce9-145">固定価格</span><span class="sxs-lookup"><span data-stu-id="64ce9-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64ce9-146">[実績]</span><span class="sxs-lookup"><span data-stu-id="64ce9-146">Actuals</span></span></th>
<th><span data-ttu-id="64ce9-147">取引通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-147">Transaction currency</span></span></th>
<th><span data-ttu-id="64ce9-148">固定価格</span><span class="sxs-lookup"><span data-stu-id="64ce9-148">Fixed price</span></span></th>
<th><span data-ttu-id="64ce9-149">取引通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64ce9-150">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="64ce9-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="64ce9-151">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="64ce9-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-152">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="64ce9-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="64ce9-153">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="64ce9-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64ce9-154">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="64ce9-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64ce9-155">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-155">Cost actual</span></span></td>
<td><span data-ttu-id="64ce9-156">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-157">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-158">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="64ce9-159">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-160">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-161">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="64ce9-162">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64ce9-163">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64ce9-164">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-164">Cost actual</span></span></td>
<td><span data-ttu-id="64ce9-165">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-166">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-167">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-168">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-169">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-170">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64ce9-171">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-172">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="64ce9-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64ce9-173">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64ce9-174">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="64ce9-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64ce9-175">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64ce9-176">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-177">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-178">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-179">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-180">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-181">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-181">Billed sales</span></span></td>
<td><span data-ttu-id="64ce9-182">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64ce9-183">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="64ce9-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64ce9-184">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64ce9-185">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-186">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-187">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-188">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-189">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-190">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64ce9-191">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-192">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="64ce9-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64ce9-193">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64ce9-194">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64ce9-195">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64ce9-196">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="64ce9-197">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="64ce9-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="64ce9-198">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="64ce9-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="64ce9-199">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-200">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-201">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-202">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-202">Billed sales</span></span></td>
<td><span data-ttu-id="64ce9-203">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64ce9-204">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="64ce9-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64ce9-205">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64ce9-206">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-207">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="64ce9-208">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-209">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="64ce9-210">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64ce9-211">**リソースがプロジェクトの契約単位と異なる組織単位に属します**</span><span class="sxs-lookup"><span data-stu-id="64ce9-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="64ce9-212">イベント</span><span class="sxs-lookup"><span data-stu-id="64ce9-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="64ce9-213">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="64ce9-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="64ce9-214">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="64ce9-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="64ce9-215">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="64ce9-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="64ce9-216">時間と材料</span><span class="sxs-lookup"><span data-stu-id="64ce9-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="64ce9-217">固定価格</span><span class="sxs-lookup"><span data-stu-id="64ce9-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64ce9-218">[実績]</span><span class="sxs-lookup"><span data-stu-id="64ce9-218">Actuals</span></span></th>
<th><span data-ttu-id="64ce9-219">取引通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-219">Transaction currency</span></span></th>
<th><span data-ttu-id="64ce9-220">固定価格</span><span class="sxs-lookup"><span data-stu-id="64ce9-220">Fixed price</span></span></th>
<th><span data-ttu-id="64ce9-221">取引通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64ce9-222">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="64ce9-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="64ce9-223">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="64ce9-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-224">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="64ce9-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="64ce9-225">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="64ce9-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="64ce9-226">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="64ce9-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64ce9-227">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-227">Cost actual</span></span></td>
<td><span data-ttu-id="64ce9-228">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="64ce9-229">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="64ce9-230">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="64ce9-231">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="64ce9-232">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-233">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="64ce9-234">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-235">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="64ce9-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="64ce9-236">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="64ce9-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-237">組織間営業</span><span class="sxs-lookup"><span data-stu-id="64ce9-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="64ce9-238">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="64ce9-239">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64ce9-240">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-240">Cost actual</span></span></td>
<td><span data-ttu-id="64ce9-241">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-242">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-243">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-244">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-245">コストの実績</span><span class="sxs-lookup"><span data-stu-id="64ce9-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-246">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="64ce9-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="64ce9-247">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="64ce9-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-248">組織間営業</span><span class="sxs-lookup"><span data-stu-id="64ce9-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="64ce9-249">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-250">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64ce9-251">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-252">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="64ce9-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64ce9-253">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64ce9-254">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="64ce9-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64ce9-255">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64ce9-256">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-257">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-258">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-259">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="64ce9-260">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-261">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-261">Billed sales</span></span></td>
<td><span data-ttu-id="64ce9-262">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64ce9-263">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="64ce9-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64ce9-264">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64ce9-265">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-266">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-267">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-268">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64ce9-269">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-270">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64ce9-271">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-272">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="64ce9-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64ce9-273">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64ce9-274">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="64ce9-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64ce9-275">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64ce9-276">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="64ce9-277">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="64ce9-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="64ce9-278">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="64ce9-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="64ce9-279">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-280">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="64ce9-281">適用なし</span><span class="sxs-lookup"><span data-stu-id="64ce9-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-282">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-282">Billed sales</span></span></td>
<td><span data-ttu-id="64ce9-283">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64ce9-284">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="64ce9-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64ce9-285">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="64ce9-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64ce9-286">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-287">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="64ce9-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="64ce9-288">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64ce9-289">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="64ce9-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="64ce9-290">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="64ce9-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]