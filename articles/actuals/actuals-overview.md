---
title: 実績
description: このトピックは、Microsoft Dynamics 365 Project Operations で実績を操作する方法に関する情報を提供します。
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996617"
---
# <a name="actuals"></a><span data-ttu-id="ee90a-103">実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-103">Actuals</span></span> 

<span data-ttu-id="ee90a-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用する Project Operations、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ee90a-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee90a-105">実績は、プロジェクトのレビューおよび承認された財務およびスケジュールの進捗状況を表します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="ee90a-106">これらは、時間、費用、材料使用エントリ、および仕訳入力と請求書の承認の結果として作成されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="ee90a-107">仕訳帳明細行と時間の送信</span><span class="sxs-lookup"><span data-stu-id="ee90a-107">Journal lines and time submission</span></span>

<span data-ttu-id="ee90a-108">時間エントリの詳細については、[時間エントリの概要](../time/time-entry-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee90a-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ee90a-109">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ee90a-109">Time and materials</span></span>

<span data-ttu-id="ee90a-110">送信された時間エントリが、時間と材料の契約品目にマップされているプロジェクトにリンクされている場合、システムは 2 つの仕訳帳明細行を作成します。1 つはコスト用、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="ee90a-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ee90a-111">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-111">Fixed price</span></span>

<span data-ttu-id="ee90a-112">送信されるプロジェクトの時間エントリが固定価格の契約品目にマップされているプロジェクトにリンクされると、システムによってコストの仕訳帳明細行が 1 つ作成されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ee90a-113">既定の価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-113">Default pricing</span></span>

<span data-ttu-id="ee90a-114">既定の価格を作成するロジックは仕訳帳明細行にあります。</span><span class="sxs-lookup"><span data-stu-id="ee90a-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="ee90a-115">時間エントリのフィールド値が仕訳帳明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="ee90a-116">これらの値には、トランザクションの日付、プロジェクトがマップされる契約品目、適切な価格表の通貨結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="ee90a-117">**役割** や **リソース単位** など既定の価格設定に影響するフィールドにより、仕訳帳明細行の適切な価格が決定されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ee90a-118">時間エントリにカスタム フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="ee90a-119">フィールド値を実績に伝播する場合は、**実績** と **仕訳帳明細行** テーブルでフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ee90a-120">カスタム コードを使用し、トランザクション発生元を使って選択したフィールド値を [タイムエントリ] から仕訳帳明細行を介して [実績] に伝達します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ee90a-121">トランザクション発生元と接続の詳細については、[実績を元のレコードにリンクする](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee90a-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="ee90a-122">仕訳帳明細行と基本経費の送信</span><span class="sxs-lookup"><span data-stu-id="ee90a-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="ee90a-123">経費エントリの詳細については、[経費の概要](../expense/expense-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee90a-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ee90a-124">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ee90a-124">Time and materials</span></span>

<span data-ttu-id="ee90a-125">送信される基本経費が、時間と材料の契約品目にマップされているプロジェクトにリンクされている場合、システムは 2 つの仕訳帳明細行を作成します。1 つはコスト用、もう 1 つは未請求販売用です。</span><span class="sxs-lookup"><span data-stu-id="ee90a-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ee90a-126">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-126">Fixed price</span></span>

<span data-ttu-id="ee90a-127">送信済みの基本経費エントリが固定価格の契約品目にマップされたプロジェクトにリンクされている場合、コストの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ee90a-128">既定の価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-128">Default pricing</span></span>

<span data-ttu-id="ee90a-129">経費の既定価格を入力するためのロジックは、経費カテゴリに基づいています。</span><span class="sxs-lookup"><span data-stu-id="ee90a-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="ee90a-130">取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ee90a-131">**トランザクション カテゴリ** や **単位** など既定の価格設定に影響するフィールドにより、仕訳帳明細行の適切な価格が決定されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ee90a-132">ただしこれは、価格表の価格設定方法が **単位当たりの価格** の場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="ee90a-133">価格設定方法が **コスト** または **コストに対する利幅** である場合、経費エントリの作成時に入力された価格がコストに使用され、販売仕訳明細の価格は価格設定方法に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="ee90a-134">経費エントリにカスタム フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="ee90a-135">フィールド値を実績に伝播する場合は、**実績** と **仕訳帳明細行** テーブルでフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ee90a-136">カスタム コードを使用し、トランザクション発生元を使って選択したフィールド値を [タイムエントリ] から仕訳帳明細行を介して [実績] に伝達します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ee90a-137">トランザクション発生元と接続の詳細については、[実績を元のレコードにリンクする](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee90a-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="ee90a-138">仕訳帳明細行と材料用途ログの送信</span><span class="sxs-lookup"><span data-stu-id="ee90a-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="ee90a-139">経費エントリの詳細については、[材料用途ログ](../material/material-usage-log.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee90a-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ee90a-140">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ee90a-140">Time and materials</span></span>

<span data-ttu-id="ee90a-141">送信された資材用途ログ エントリが、時間と資材の仕訳帳明細行にマップされているプロジェクトにリンクされている場合、システムは原価用と未請求販売用 2 つの仕訳明細を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ee90a-142">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-142">Fixed price</span></span>

<span data-ttu-id="ee90a-143">送信済みの資材用途ログ エントリが固定価格の契約品目にマップされたプロジェクトにリンクされている場合、コストの仕訳帳明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ee90a-144">既定の価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-144">Default pricing</span></span>

<span data-ttu-id="ee90a-145">材料のデフォルト価格を入力するためのロジックは、製品とユニットの組み合わせに基づいています。</span><span class="sxs-lookup"><span data-stu-id="ee90a-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="ee90a-146">取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ee90a-147">**製品 ID** や **単位** など既定の価格設定に影響するフィールドにより、仕訳帳明細行の適切な価格が決定されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ee90a-148">ただし、これはカタログ製品でのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-148">However, this only works for catalog products.</span></span> <span data-ttu-id="ee90a-149">書き込み製品の場合、材料使用ログエントリの作成時に入力された価格が、仕訳帳明細行の原価と販売価格に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="ee90a-150">**資材用途ログ** エントリにカスタム フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="ee90a-151">フィールド値を実績に伝播する場合は、**実績** と **仕訳帳明細行** テーブルでフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ee90a-152">カスタム コードを使用し、トランザクション発生元を使って選択したフィールド値を [タイムエントリ] から仕訳帳明細行を介して [実績] に伝達します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ee90a-153">トランザクション発生元と接続の詳細については、[実績を元のレコードにリンクする](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee90a-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="ee90a-154">仕訳帳を使用してコストを記録する</span><span class="sxs-lookup"><span data-stu-id="ee90a-154">Use entry journals to record costs</span></span>

<span data-ttu-id="ee90a-155">仕訳帳を使用して、材料、料金、時間、経費、税のトランザクション クラスでコストや収益を記録できます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ee90a-156">仕訳帳は、次の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="ee90a-157">トランザクションの実績を別のシステムから Microsoft Dynamics 365 Project Operations に移動します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="ee90a-158">別のシステムで発生したコストを記録します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="ee90a-159">これらのコストには、調達コストまたは下請けコストが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee90a-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee90a-160">アプリケーションは、仕訳明細タイプまたは仕訳明細行に入力された関連価格を検証しません。</span><span class="sxs-lookup"><span data-stu-id="ee90a-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ee90a-161">したがって、実績がプロジェクトに与える会計上の影響を十分に認識しているユーザーのみが、仕訳帳を使用して実績を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee90a-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="ee90a-162">この仕訳の種類が影響を与えるため、仕訳帳を作成するためのアクセス権を持つユーザーを慎重に選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee90a-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="ee90a-163">プロジェクト イベントに基づく実績を記録する</span><span class="sxs-lookup"><span data-stu-id="ee90a-163">Record actuals based on project events</span></span>

<span data-ttu-id="ee90a-164">Project Operations はプロジェクト中に発生する財務取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ee90a-165">これらの取引は 実績 として記録されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="ee90a-166">次の表はプロジェクトが時間と材料のプロジェクトであるか、固定価格のプロジェクトであるか、プリセールス段階にあるか、内部プロジェクトであるかに応じて、作成されるさまざまなタイプの実績を示しています。</span><span class="sxs-lookup"><span data-stu-id="ee90a-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="ee90a-167">リソースはプロジェクトの契約単位と同じ組織単位に属します</span><span class="sxs-lookup"><span data-stu-id="ee90a-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ee90a-168">イベント</span><span class="sxs-lookup"><span data-stu-id="ee90a-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ee90a-169">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee90a-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ee90a-170">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee90a-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ee90a-171">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee90a-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ee90a-172">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ee90a-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ee90a-173">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ee90a-174">[実績]</span><span class="sxs-lookup"><span data-stu-id="ee90a-174">Actuals</span></span></th>
<th><span data-ttu-id="ee90a-175">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-175">Transaction currency</span></span></th>
<th><span data-ttu-id="ee90a-176">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-176">Fixed price</span></span></th>
<th><span data-ttu-id="ee90a-177">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee90a-178">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="ee90a-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ee90a-179">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ee90a-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-180">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="ee90a-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ee90a-181">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ee90a-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee90a-182">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="ee90a-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee90a-183">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-183">Cost actual</span></span></td>
<td><span data-ttu-id="ee90a-184">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-185">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-186">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ee90a-187">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-188">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-189">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ee90a-190">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee90a-191">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee90a-192">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-192">Cost actual</span></span></td>
<td><span data-ttu-id="ee90a-193">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-194">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-195">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-196">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-197">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-198">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee90a-199">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-200">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ee90a-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee90a-201">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee90a-202">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="ee90a-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee90a-203">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee90a-204">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-205">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-206">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-207">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-208">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-209">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-209">Billed sales</span></span></td>
<td><span data-ttu-id="ee90a-210">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee90a-211">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee90a-212">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee90a-213">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-214">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-215">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-216">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-217">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-218">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee90a-219">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-220">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ee90a-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee90a-221">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee90a-222">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee90a-223">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee90a-224">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ee90a-225">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="ee90a-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ee90a-226">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="ee90a-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ee90a-227">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-228">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-229">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-230">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-230">Billed sales</span></span></td>
<td><span data-ttu-id="ee90a-231">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee90a-232">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee90a-233">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee90a-234">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-235">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ee90a-236">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-237">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee90a-238">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="ee90a-239">リソースがプロジェクトの契約単位と異なる組織単位に属します</span><span class="sxs-lookup"><span data-stu-id="ee90a-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ee90a-240">イベント</span><span class="sxs-lookup"><span data-stu-id="ee90a-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ee90a-241">請求可能なプロジェクトまたは販売されたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee90a-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ee90a-242">プリセールス段階のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee90a-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ee90a-243">内部プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee90a-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ee90a-244">時間と材料</span><span class="sxs-lookup"><span data-stu-id="ee90a-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ee90a-245">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ee90a-246">[実績]</span><span class="sxs-lookup"><span data-stu-id="ee90a-246">Actuals</span></span></th>
<th><span data-ttu-id="ee90a-247">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-247">Transaction currency</span></span></th>
<th><span data-ttu-id="ee90a-248">固定価格</span><span class="sxs-lookup"><span data-stu-id="ee90a-248">Fixed price</span></span></th>
<th><span data-ttu-id="ee90a-249">取引通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ee90a-250">時間エントリが作成されました。</span><span class="sxs-lookup"><span data-stu-id="ee90a-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ee90a-251">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ee90a-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-252">時間エントリが送信されました。</span><span class="sxs-lookup"><span data-stu-id="ee90a-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ee90a-253">実績エンティティに活動がありません</span><span class="sxs-lookup"><span data-stu-id="ee90a-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ee90a-254">時間が承認され、承認中に請求可能時間の変更や増加はありません。</span><span class="sxs-lookup"><span data-stu-id="ee90a-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee90a-255">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-255">Cost actual</span></span></td>
<td><span data-ttu-id="ee90a-256">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ee90a-257">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ee90a-258">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ee90a-259">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ee90a-260">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-261">未請求の販売実績 – 請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ee90a-262">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-263">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ee90a-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ee90a-264">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ee90a-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-265">組織間営業</span><span class="sxs-lookup"><span data-stu-id="ee90a-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ee90a-266">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ee90a-267">時間が承認され、承認中に請求可能時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ee90a-268">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-268">Cost actual</span></span></td>
<td><span data-ttu-id="ee90a-269">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-270">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-271">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-272">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-273">コストの実績</span><span class="sxs-lookup"><span data-stu-id="ee90a-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-274">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ee90a-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ee90a-275">リソース単位原価</span><span class="sxs-lookup"><span data-stu-id="ee90a-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-276">組織間営業</span><span class="sxs-lookup"><span data-stu-id="ee90a-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ee90a-277">契約単位の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-278">未請求の販売実績 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee90a-279">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-280">未請求の販売実績 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ee90a-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee90a-281">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee90a-282">請求書が確認され、請求可能時間で変更や増加は発生しません。</span><span class="sxs-lookup"><span data-stu-id="ee90a-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee90a-283">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee90a-284">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-285">マイルストーンの請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-286">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-287">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ee90a-288">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-289">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-289">Billed sales</span></span></td>
<td><span data-ttu-id="ee90a-290">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee90a-291">請求書が確認され、請求可能時間に減少します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ee90a-292">未請求の販売取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ee90a-293">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-294">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-295">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-296">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ee90a-297">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-298">請求済み売上 – 新しい数量に対して請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ee90a-299">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-300">請求済み売上 – 差額は請求不可</span><span class="sxs-lookup"><span data-stu-id="ee90a-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee90a-301">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ee90a-302">請求書は修正され、請求可能な数量が増えます。</span><span class="sxs-lookup"><span data-stu-id="ee90a-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee90a-303">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee90a-304">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ee90a-305">マイルストーンの請求された販売の取り消し</span><span class="sxs-lookup"><span data-stu-id="ee90a-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ee90a-306">マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</span><span class="sxs-lookup"><span data-stu-id="ee90a-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ee90a-307">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-308">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ee90a-309">適用なし</span><span class="sxs-lookup"><span data-stu-id="ee90a-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-310">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-310">Billed sales</span></span></td>
<td><span data-ttu-id="ee90a-311">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ee90a-312">請求書は修正され、請求可能な数量が減少します。</span><span class="sxs-lookup"><span data-stu-id="ee90a-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ee90a-313">請求済み売上 – 取消</span><span class="sxs-lookup"><span data-stu-id="ee90a-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ee90a-314">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-315">新しい数量の請求済み売上</span><span class="sxs-lookup"><span data-stu-id="ee90a-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ee90a-316">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ee90a-317">未請求売上 – 差額は請求可能</span><span class="sxs-lookup"><span data-stu-id="ee90a-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ee90a-318">プロジェクト契約の通貨</span><span class="sxs-lookup"><span data-stu-id="ee90a-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
