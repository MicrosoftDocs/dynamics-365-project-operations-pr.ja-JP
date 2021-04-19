---
title: 見積請求書
description: このトピックは、Project Operations における見積請求書の確認に関する情報を提供します。
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b143ba286f25ecb23fea09a85bca06543f7f55ff
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866867"
---
# <a name="proforma-invoices"></a><span data-ttu-id="440a9-103">見積請求書</span><span class="sxs-lookup"><span data-stu-id="440a9-103">Proforma invoices</span></span>

<span data-ttu-id="440a9-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="440a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="440a9-105">見積もり請求は、プロジェクト管理者が顧客に対する請求書を作成する前に、第 2 レベルの承認を提供します。</span><span class="sxs-lookup"><span data-stu-id="440a9-105">Proforma invoicing gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="440a9-106">プロジェクト チーム メンバーが送信する時間、経費、および材料のエントリが承認されると、第 1 レベルの承認が完了します。</span><span class="sxs-lookup"><span data-stu-id="440a9-106">The first level of approval is completed when time, expense, and material entries that project team members submit are approved.</span></span> <span data-ttu-id="440a9-107">確認済みの見積請求書は、Project Operations のプロジェクト会計モジュールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="440a9-107">Confirmed proforma invoices are available in the Project Accounting module of Project Operations.</span></span> <span data-ttu-id="440a9-108">プロジェクトの会計担当者は、消費税、会計、請求書のレイアウトなどの追加の更新を実行できます。</span><span class="sxs-lookup"><span data-stu-id="440a9-108">Project accountants can perform additional updates such as sales tax, accounting, and invoice layout.</span></span>


## <a name="creating-project-invoices"></a><span data-ttu-id="440a9-109">プロジェクトの請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="440a9-109">Creating project invoices</span></span>

<span data-ttu-id="440a9-110">プロジェクトの請求書は 1 つずつ、または一括して作成できます。</span><span class="sxs-lookup"><span data-stu-id="440a9-110">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="440a9-111">手動で作成できます。また、自動実行で生成するように設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="440a9-111">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices"></a><span data-ttu-id="440a9-112">プロジェクトの請求書を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="440a9-112">Manually create project invoices</span></span> 

<span data-ttu-id="440a9-113">**プロジェクト契約** 一覧ページから、プロジェクト契約ごとに個別にプロジェクト請求書を作成することも、複数のプロジェクト契約に対して一括で請求書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="440a9-113">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="440a9-114">特定のプロジェクト契約の請求書を作成するには、このステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="440a9-114">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="440a9-115">**プロジェクト契約** リスト ページで、プロジェクト契約を開き、 **請求書の​​作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-115">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    <span data-ttu-id="440a9-116">ステータスが **請求準備完了** の選択したプロジェクト契約の全トランザクションに対して請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-116">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="440a9-117">これらのトランザクションには、時間、費用、材料、マイルストーン、およびその他の未請求の販売仕訳帳明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="440a9-117">These transactions include time, expenses, materials, milestones, and other unbilled sales journal lines.</span></span>

<span data-ttu-id="440a9-118">一括で請求書を作成するには、次の手順に実行します。</span><span class="sxs-lookup"><span data-stu-id="440a9-118">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="440a9-119">**プロジェクト契約** 一覧ページで、請求書を作成する必要のあるプロジェクト契約を 1 つ以上選択し、 **プロジェクト請求書の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-119">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    <span data-ttu-id="440a9-120">警告メッセージは、請求書が作成される前に遅延が発生する可能性があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="440a9-120">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="440a9-121">プロセスも表示されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-121">The process is also shown.</span></span>

2. <span data-ttu-id="440a9-122">**OK** を選択して、メッセージ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="440a9-122">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="440a9-123">ステータスが **請求準備完了** の契約品目の全トランザクションに対して請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-123">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="440a9-124">これらのトランザクションには、時間、費用、材料、マイルストーン、およびその他の未請求の販売仕訳帳明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="440a9-124">These transactions include time, expenses, materials, milestones, and other unbilled sales journal lines.</span></span>

3. <span data-ttu-id="440a9-125">生成された請求書を表示するには、 **営業** \> **請求先** \> **請求書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="440a9-125">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="440a9-126">プロジェクト契約ごとに 1 つの請求書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-126">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices"></a><span data-ttu-id="440a9-127">プロジェクト請求書の自動作成を設定する</span><span class="sxs-lookup"><span data-stu-id="440a9-127">Set up automated creation of project invoices</span></span> 

<span data-ttu-id="440a9-128">請求書の自動化を実行するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="440a9-128">Follow these steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="440a9-129">**設定** \> **バッチ ジョブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="440a9-129">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="440a9-130">バッチ ジョブを作成し、 **プロジェクト オペレーション請求書の作成** と名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="440a9-130">Create a batch job, and name it **Project Operations Create Invoices**.</span></span> <span data-ttu-id="440a9-131">バッチ ジョブの名前に、「請求書の作成」という語句を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="440a9-131">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="440a9-132">**ジョブの種類** フィールドで、 **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-132">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="440a9-133">既定で、 **頻度 毎日** および **アクティブ** オプションは **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="440a9-133">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="440a9-134">**ワークフローの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-134">Select **Run Workflow**.</span></span> <span data-ttu-id="440a9-135">**レコードの検索** ダイアログ ボックスで、 3 つのワークフローが表示されます:</span><span class="sxs-lookup"><span data-stu-id="440a9-135">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="440a9-136">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="440a9-136">ProcessRunCaller</span></span>
    - <span data-ttu-id="440a9-137">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="440a9-137">ProcessRunner</span></span>
    - <span data-ttu-id="440a9-138">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="440a9-138">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="440a9-139">**ProcessRunCaller** を選択し、そして **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-139">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="440a9-140">次のダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-140">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="440a9-141">**スリープ** ワークフローの後に、 **プロセス** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="440a9-141">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="440a9-142">ステップ 5 で、 **ProcessRunner** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="440a9-142">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="440a9-143">**OK** を選択すると、 **プロセス** ワークフロー の後には、 **スリープ** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="440a9-143">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="440a9-144">**ProcessRunCaller** および **ProcessRunner** ワークフローは、請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="440a9-144">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="440a9-145">**ProcessRunCaller** は **ProcessRunner** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="440a9-145">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="440a9-146">**ProcessRunner** は、実際に請求書を作成するワークフローです。</span><span class="sxs-lookup"><span data-stu-id="440a9-146">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="440a9-147">請求書を作成する必要のあるすべての契約品目を調べ、それらの明細の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="440a9-147">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="440a9-148">契約書を作成する契約品目を決定するために、ジョブは契約品目の請求書の実行日を参照します。</span><span class="sxs-lookup"><span data-stu-id="440a9-148">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="440a9-149">1 つの契約に属する契約品目の請求書実行日が同じ場合、トランザクションは、 2 つの請求明細行を持つ 1 つの請求書に統合されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-149">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="440a9-150">請求書を作成するトランザクションがない場合、ジョブは請求書の作成をスキップします。</span><span class="sxs-lookup"><span data-stu-id="440a9-150">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="440a9-151">**ProcessRunner** の実行が完了すると、 **ProcessRunCaller** を呼び出して、終了時間が指定されてクローズされます。</span><span class="sxs-lookup"><span data-stu-id="440a9-151">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="440a9-152">**ProcessRunCaller** は、指定された終了時刻から24時間実行するタイマーを開始します。</span><span class="sxs-lookup"><span data-stu-id="440a9-152">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="440a9-153">タイマーが終了すると、 **ProcessRunCaller** が閉じられます。</span><span class="sxs-lookup"><span data-stu-id="440a9-153">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="440a9-154">請求書を作成するバッチ処理ジョブは、定期的なジョブです。</span><span class="sxs-lookup"><span data-stu-id="440a9-154">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="440a9-155">このバッチ処理を何度も実行すると、ジョブの複数のインスタンスが作成され、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="440a9-155">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="440a9-156">したがって、バッチ処理は一度だけ実行し、実行が停止した場合のみ、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="440a9-156">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="440a9-157">バッチ請求は、請求スケジュールで構成されたプロジェクト契約明細に対してのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-157">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="440a9-158">固定価格の請求方法の契約品目には、マイルストーンを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="440a9-158">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="440a9-159">時間と材料の請求方法を持つプロジェクト契約品目には、日付ベースの請求スケジュールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="440a9-159">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="440a9-160">これは、プロジェクトベースの契約品目でも同じです。</span><span class="sxs-lookup"><span data-stu-id="440a9-160">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-invoice"></a><span data-ttu-id="440a9-161">請求書の下書きを編集する</span><span class="sxs-lookup"><span data-stu-id="440a9-161">Edit a draft invoice</span></span>

<span data-ttu-id="440a9-162">プロジェクト請求書のドラフトを作成すると、時間、経費、および材料用途のエントリが承認したときに作成された、すべての未請求営業トランザクションが、請求書にプルされます。</span><span class="sxs-lookup"><span data-stu-id="440a9-162">When you create a draft project invoice, all unbilled sales transactions that were created when the time, expense, and material usage entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="440a9-163">請求書がまだドラフト段階である間は、次の調整を行うことができます:</span><span class="sxs-lookup"><span data-stu-id="440a9-163">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="440a9-164">請求明細行の詳細を削除、または編集します。</span><span class="sxs-lookup"><span data-stu-id="440a9-164">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="440a9-165">数量や請求書の種類を編集、調整します。</span><span class="sxs-lookup"><span data-stu-id="440a9-165">Edit and adjust the quantity and billing type.</span></span>

<span data-ttu-id="440a9-166">請求書を確認するには、 **確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="440a9-166">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="440a9-167">確認操作は、一方向の操作です。</span><span class="sxs-lookup"><span data-stu-id="440a9-167">The Confirm action is a one-way action.</span></span> <span data-ttu-id="440a9-168">**確認** を選択すると、システムは請求書を読み取り専用にし、各請求明細行の各請求明細行の詳細から請求済みの売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="440a9-168">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="440a9-169">請求明細行の詳細が未請求売上実績を参照する場合、システムは未請求売上実績も取り消します。</span><span class="sxs-lookup"><span data-stu-id="440a9-169">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="440a9-170">(時間または経費エントリから作成された請求明細行の詳細は、未請求売上実績を参照します)。総勘定元帳統合システムは、この取り消しを使用して、会計目的で進行中のプロジェクト作業 (WIP) を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="440a9-170">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-invoice"></a><span data-ttu-id="440a9-171">確認済みの請求書を修正する</span><span class="sxs-lookup"><span data-stu-id="440a9-171">Correct a confirmed invoice</span></span>

<span data-ttu-id="440a9-172">確認済みの請求書は編集 (修正) できます。</span><span class="sxs-lookup"><span data-stu-id="440a9-172">Confirmed invoices can be edited (corrected).</span></span> <span data-ttu-id="440a9-173">確認済みの請求書を修正すると、新規修正請求書ドラフトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-173">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="440a9-174">元の請求書のすべてのトランザクションと数量を取り消すことを前提としているため、この修正請求書には元の請求書のすべてのトランザクションが含まれ、その数量はすべて 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="440a9-174">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="440a9-175">トランザクションが修正を必要とない場合、その修正請求書のドラフトから削除できます。</span><span class="sxs-lookup"><span data-stu-id="440a9-175">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="440a9-176">部分的な数量を取り消す、または戻り場合は、明細行の詳細の **数量** フィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="440a9-176">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="440a9-177">請求明細行の詳細を開くと、元の請求書の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-177">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="440a9-178">その後、現在の請求書の数量を編集して、元の請求書の数量よりも少なく、または多くすることができます。</span><span class="sxs-lookup"><span data-stu-id="440a9-178">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="440a9-179">修正請求書を確認すると、元の請求済み売上実績が取り消され、新規の請求済み売上実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-179">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="440a9-180">数量が削減された場合、差異により未請求売上実績も作成されます。</span><span class="sxs-lookup"><span data-stu-id="440a9-180">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="440a9-181">例えば、元の請求済み売上が 8 時間分であり、修正された請求明細行の詳細の数量が 6 時間に減少した場合、元の請求売上明細行を戻し、新たに 2 つの実績が作成されます :</span><span class="sxs-lookup"><span data-stu-id="440a9-181">For example, if the original billed sale was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, the original billed sales line is reversed and two new actuals are created:</span></span>

- <span data-ttu-id="440a9-182">6 時間の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="440a9-182">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="440a9-183">残り 2 時間の未請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="440a9-183">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="440a9-184">このトランザクションは、顧客との交渉に応じて後で請求するか、または、請求不可としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="440a9-184">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
