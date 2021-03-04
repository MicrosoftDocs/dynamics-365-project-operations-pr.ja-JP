---
title: 実績の概要
description: このトピックでは、プロジェクトの実績について説明します。
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146129"
---
# <a name="actuals-overview"></a><span data-ttu-id="76f6d-103">実績の概要</span><span class="sxs-lookup"><span data-stu-id="76f6d-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76f6d-104">実績とはプロジェクトで完了した作業の量です。</span><span class="sxs-lookup"><span data-stu-id="76f6d-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="76f6d-105">プロジェクトの実績はソース ドキュメントまでさかのぼることができます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="76f6d-106">これらのソース ドキュメントには、時間、経費、仕訳入力、そして請求書が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![プロジェクトの実績をソース ドキュメントまでトレースする方法](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="76f6d-108">時間エントリの送信</span><span class="sxs-lookup"><span data-stu-id="76f6d-108">Submitting a time entry</span></span>

<span data-ttu-id="76f6d-109">PSA では、時間と材料の契約品目にマップされたプロジェクトの時間エントリが送信されると、2 つの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="76f6d-110">1 つはコスト用で、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="76f6d-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="76f6d-111">固定価格の契約品目にマップされたプロジェクトの時間エントリが送信されると、仕訳帳明細行はコストのみで作成されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="76f6d-112">既定の価格を入力するロジックは仕訳帳明細行にあります。</span><span class="sxs-lookup"><span data-stu-id="76f6d-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="76f6d-113">時間エントリのすべてのフィールド値が仕訳帳明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="76f6d-114">これらのフィールドは、トランザクションの日付、プロジェクトがマップされる契約品目、適切な価格表の通貨結果を含みます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="76f6d-115">**役割** や **組織単位** など既定の価格に影響するフィールドにより、適切な価格が既定で仕訳帳明細行に入力されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="76f6d-116">時間エントリのカスタム フィールドを追加してフィールドに値と実績を伝播する場合は、実績エンティティのフィールドを作成して、フィール ドマッピングで時間エントリから実績にフィールドをコピーします。</span><span class="sxs-lookup"><span data-stu-id="76f6d-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="76f6d-117">経費エントリの送信</span><span class="sxs-lookup"><span data-stu-id="76f6d-117">Submitting an expense entry</span></span>

<span data-ttu-id="76f6d-118">PSA では、時間と材料の契約品目にマップされたプロジェクトの経費エントリが送信されると、2 つの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="76f6d-119">1 つはコスト用で、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="76f6d-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="76f6d-120">固定価格の契約品目にマップされたプロジェクトの経費エントリが送信されると、仕訳帳明細行はコストのみで作成されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="76f6d-121">経費の既定価格を入力するロジックは、**経費エントリ** ページで選択した経費カテゴリに基づきます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="76f6d-122">取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="76f6d-123">ただし、価格自体についてユーザーが入力した金額は、既定で原価と販売に関連する経費の仕訳帳明細行に直接設定されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="76f6d-124">PSA の現在のバージョンでは、経費エントリの単位ごとの既定価格のカテゴリ ベースのエントリは使用できません。</span><span class="sxs-lookup"><span data-stu-id="76f6d-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="76f6d-125">エントリ ジャーナルを使用してコストを記録する</span><span class="sxs-lookup"><span data-stu-id="76f6d-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="76f6d-126">PSA ではエントリ ジャーナルを使用して、材料、料金、時間、経費、税のトランザクション クラスでコストや収益を記録できます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="76f6d-127">ジャーナルには、ヘッダー、行、**確認** の操作があります。</span><span class="sxs-lookup"><span data-stu-id="76f6d-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="76f6d-128">以下にジャーナルを使用するシナリオをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="76f6d-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="76f6d-129">プロジェクトで材料の実際のコストと売上を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76f6d-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="76f6d-130">トランザクションの実績を別のシステムから PSA に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76f6d-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="76f6d-131">調達コストや外注コストなど、別のシステムで発生したコストを記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76f6d-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76f6d-132">エントリ ジャーナルを使用して実績を作成するのは、実績がプロジェクトに与える会計上の影響を完全に認識しているユーザーだけが行ってください。</span><span class="sxs-lookup"><span data-stu-id="76f6d-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="76f6d-133">これは、アプリケーションが仕訳帳明細行タイプ、または仕訳帳明細行に入力された関連する価格を検証しないためです。</span><span class="sxs-lookup"><span data-stu-id="76f6d-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="76f6d-134">この仕訳タイプの影響があるため、誰がエントリ ジャーナルを作成するためのアクセス権を与えられるかについて十分な注意を払ってください。</span><span class="sxs-lookup"><span data-stu-id="76f6d-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="76f6d-135">プロジェクト イベントに基づく実績を記録する</span><span class="sxs-lookup"><span data-stu-id="76f6d-135">Recording actuals based on project events</span></span>

<span data-ttu-id="76f6d-136">PSA はプロジェクト中に発生する財務取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="76f6d-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="76f6d-137">これらの取引は **実績** として記録されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="76f6d-138">次の表はプロジェクトが時間と材料のプロジェクトであるか、固定価格のプロジェクトであるか、プリセールス段階にあるか、内部プロジェクトであるかに応じて、作成されるさまざまなタイプの実績を示しています。</span><span class="sxs-lookup"><span data-stu-id="76f6d-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="76f6d-139">**リソースはプロジェクトの契約単位と同じ組織単位に属します**</span><span class="sxs-lookup"><span data-stu-id="76f6d-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="76f6d-140">イベント</span><span class="sxs-lookup"><span data-stu-id="76f6d-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="76f6d-141">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="76f6d-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="76f6d-142">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="76f6d-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="76f6d-143">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="76f6d-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="76f6d-144">時間と材料</span><span class="sxs-lookup"><span data-stu-id="76f6d-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="76f6d-145">固定価格</span><span class="sxs-lookup"><span data-stu-id="76f6d-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="76f6d-146">[実績]</span><span class="sxs-lookup"><span data-stu-id="76f6d-146">Actuals</span></span></th>
<th><span data-ttu-id="76f6d-147">取引通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-147">Transaction currency</span></span></th>
<th><span data-ttu-id="76f6d-148">固定価格</span><span class="sxs-lookup"><span data-stu-id="76f6d-148">Fixed price</span></span></th>
<th><span data-ttu-id="76f6d-149">取引通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76f6d-150">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="76f6d-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="76f6d-151">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="76f6d-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-152">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="76f6d-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="76f6d-153">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="76f6d-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76f6d-154">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="76f6d-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76f6d-155">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-155">Cost actual</span></span></td>
<td><span data-ttu-id="76f6d-156">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-157">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-158">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="76f6d-159">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-160">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-161">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="76f6d-162">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76f6d-163">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76f6d-164">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-164">Cost actual</span></span></td>
<td><span data-ttu-id="76f6d-165">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-166">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-167">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-168">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-169">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-170">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76f6d-171">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-172">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="76f6d-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76f6d-173">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76f6d-174">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="76f6d-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76f6d-175">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76f6d-176">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-177">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-178">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-179">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-180">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-181">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-181">Billed sales</span></span></td>
<td><span data-ttu-id="76f6d-182">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76f6d-183">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="76f6d-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76f6d-184">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76f6d-185">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-186">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-187">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-188">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-189">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-190">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76f6d-191">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-192">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="76f6d-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76f6d-193">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76f6d-194">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76f6d-195">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76f6d-196">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="76f6d-197">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="76f6d-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="76f6d-198">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="76f6d-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="76f6d-199">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-200">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-201">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-202">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-202">Billed sales</span></span></td>
<td><span data-ttu-id="76f6d-203">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76f6d-204">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="76f6d-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76f6d-205">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76f6d-206">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-207">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="76f6d-208">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-209">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="76f6d-210">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76f6d-211">**リソースがプロジェクトの契約単位と異なる組織単位に属します**</span><span class="sxs-lookup"><span data-stu-id="76f6d-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="76f6d-212">イベント</span><span class="sxs-lookup"><span data-stu-id="76f6d-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="76f6d-213">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="76f6d-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="76f6d-214">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="76f6d-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="76f6d-215">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="76f6d-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="76f6d-216">時間と材料</span><span class="sxs-lookup"><span data-stu-id="76f6d-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="76f6d-217">固定価格</span><span class="sxs-lookup"><span data-stu-id="76f6d-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="76f6d-218">[実績]</span><span class="sxs-lookup"><span data-stu-id="76f6d-218">Actuals</span></span></th>
<th><span data-ttu-id="76f6d-219">取引通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-219">Transaction currency</span></span></th>
<th><span data-ttu-id="76f6d-220">固定価格</span><span class="sxs-lookup"><span data-stu-id="76f6d-220">Fixed price</span></span></th>
<th><span data-ttu-id="76f6d-221">取引通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76f6d-222">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="76f6d-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="76f6d-223">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="76f6d-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-224">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="76f6d-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="76f6d-225">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="76f6d-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="76f6d-226">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="76f6d-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76f6d-227">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-227">Cost actual</span></span></td>
<td><span data-ttu-id="76f6d-228">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="76f6d-229">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="76f6d-230">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="76f6d-231">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="76f6d-232">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-233">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="76f6d-234">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-235">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="76f6d-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="76f6d-236">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="76f6d-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-237">組織間営業</span><span class="sxs-lookup"><span data-stu-id="76f6d-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="76f6d-238">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="76f6d-239">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76f6d-240">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-240">Cost actual</span></span></td>
<td><span data-ttu-id="76f6d-241">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-242">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-243">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-244">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-245">コストの実績</span><span class="sxs-lookup"><span data-stu-id="76f6d-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-246">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="76f6d-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="76f6d-247">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="76f6d-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-248">組織間営業</span><span class="sxs-lookup"><span data-stu-id="76f6d-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="76f6d-249">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-250">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76f6d-251">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-252">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="76f6d-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76f6d-253">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76f6d-254">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="76f6d-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76f6d-255">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76f6d-256">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-257">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-258">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-259">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="76f6d-260">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-261">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-261">Billed sales</span></span></td>
<td><span data-ttu-id="76f6d-262">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76f6d-263">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="76f6d-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76f6d-264">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76f6d-265">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-266">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-267">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-268">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76f6d-269">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-270">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76f6d-271">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-272">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="76f6d-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76f6d-273">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76f6d-274">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="76f6d-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76f6d-275">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76f6d-276">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="76f6d-277">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="76f6d-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="76f6d-278">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="76f6d-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="76f6d-279">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-280">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="76f6d-281">適用なし</span><span class="sxs-lookup"><span data-stu-id="76f6d-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-282">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-282">Billed sales</span></span></td>
<td><span data-ttu-id="76f6d-283">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76f6d-284">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="76f6d-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76f6d-285">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="76f6d-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76f6d-286">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-287">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="76f6d-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="76f6d-288">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76f6d-289">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="76f6d-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="76f6d-290">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="76f6d-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
