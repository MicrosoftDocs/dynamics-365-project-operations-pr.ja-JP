---
title: Project Service Automation での 請求
description: このトピックでは、請求に関する情報を提供します。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079332"
---
# <a name="invoicing-in-project-service-automation"></a><span data-ttu-id="f4afa-103">Project Service Automation での 請求</span><span class="sxs-lookup"><span data-stu-id="f4afa-103">Invoicing in Project Service Automation</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f4afa-104">Dynamics 365 Project Service Automation での請求は、プロジェクト管理者が顧客に対する請求書を作成する前に、第 2 レベルの承認を与えるので便利です。</span><span class="sxs-lookup"><span data-stu-id="f4afa-104">Invoicing in Dynamics 365 Project Service Automation is useful because it gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="f4afa-105">プロジェクト チーム メンバーが送信する時間と経費のエントリが承認されると、第 1 レベルの承認が完了します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-105">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="f4afa-106">PSAは、次の理由により、顧客向け請求書を生成するようには設計されていません:</span><span class="sxs-lookup"><span data-stu-id="f4afa-106">PSA isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="f4afa-107">税務情報は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f4afa-107">It doesn't contain tax information.</span></span>
- <span data-ttu-id="f4afa-108">正しく設定された為替レートを使用して、他の通貨を請求通貨に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="f4afa-108">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="f4afa-109">請求書を印刷できるように正しく書式設定できません。</span><span class="sxs-lookup"><span data-stu-id="f4afa-109">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="f4afa-110">代わりに、財務または会計システムを使用して、PSA で生成された請求書候補の情報を使用して顧客向け請求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-110">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from invoice proposals that are generated in PSA.</span></span>

## <a name="creating-project-invoices-in-psa"></a><span data-ttu-id="f4afa-111">PSA でのプロジェクト請求書の作成</span><span class="sxs-lookup"><span data-stu-id="f4afa-111">Creating project invoices in PSA</span></span>

<span data-ttu-id="f4afa-112">プロジェクトの請求書は 1 つずつ、または一括して作成できます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-112">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="f4afa-113">手動で作成できます。また、自動実行で生成するように設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-113">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices-in-psa"></a><span data-ttu-id="f4afa-114">PSA を使用してプロジェクト請求書を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="f4afa-114">Manually create project invoices in PSA</span></span>

<span data-ttu-id="f4afa-115">**プロジェクト契約** 一覧ページから、プロジェクト契約ごとに個別にプロジェクト請求書を作成することも、複数のプロジェクト契約に対して一括で請求書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-115">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="f4afa-116">特定のプロジェクト契約の請求書を作成するには、このステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-116">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="f4afa-117">**プロジェクト契約** リスト ページで、プロジェクト契約を開き、 **請求書の​​作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-117">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    ![特定のプロジェクト契約に対するプロジェクト請求書の作成](media/CreateProjectInvoicesOneByOne.png)

    <span data-ttu-id="f4afa-119">ステータスが **請求準備完了** の選択したプロジェクト契約の全トランザクションに対して請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="f4afa-120">これらのトランザクションには、時間、経費、マイルストーン、製品ベースの契約品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="f4afa-121">一括で請求書を作成するには、次の手順に実行します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="f4afa-122">**プロジェクト契約** 一覧ページで、請求書を作成する必要のあるプロジェクト契約を 1 つ以上選択し、 **プロジェクト請求書の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    ![プロジェクト請求書の一括作成](media/CreateProjectInvoicesBulk.png)

    <span data-ttu-id="f4afa-124">警告メッセージは、請求書が作成される前に遅延が発生する可能性があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-124">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="f4afa-125">プロセスも表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-125">The process is also shown.</span></span>

2. <span data-ttu-id="f4afa-126">**OK** を選択して、メッセージ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-126">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="f4afa-127">ステータスが **請求準備完了** の契約品目の全トランザクションに対して請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-127">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="f4afa-128">これらのトランザクションには、時間、経費、マイルストーン、製品ベースの契約品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-128">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="f4afa-129">生成された請求書を表示するには、 **営業** \> **請求先** \> **請求書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-129">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="f4afa-130">プロジェクト契約ごとに 1 つの請求書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-130">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a><span data-ttu-id="f4afa-131">PSA でプロジェクト請求書の自動作成を設定</span><span class="sxs-lookup"><span data-stu-id="f4afa-131">Set up automated creation of project invoices in PSA</span></span>

<span data-ttu-id="f4afa-132">PSAで実行された自動化請求を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f4afa-132">Follow these steps to configure an automated invoice run in PSA.</span></span>

1. <span data-ttu-id="f4afa-133">**Project Service** \> **設定** \> **バッチ ジョブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-133">Go to **Project Service** \> **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="f4afa-134">一括ジョブを作成して、 **PSA 請求書の作成** と名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-134">Create a batch job, and name it **PSA Create Invoices**.</span></span> <span data-ttu-id="f4afa-135">バッチ ジョブの名前に、「請求書の作成」という語句を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4afa-135">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="f4afa-136">**ジョブの種類** フィールドで、 **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-136">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="f4afa-137">既定で、 **頻度 毎日** および **アクティブ** オプションは **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="f4afa-137">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="f4afa-138">**ワークフローの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-138">Select **Run Workflow**.</span></span> <span data-ttu-id="f4afa-139">**レコードの検索** ダイアログ ボックスで、 3 つのワークフローが表示されます:</span><span class="sxs-lookup"><span data-stu-id="f4afa-139">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="f4afa-140">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="f4afa-140">ProcessRunCaller</span></span>
    - <span data-ttu-id="f4afa-141">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="f4afa-141">ProcessRunner</span></span>
    - <span data-ttu-id="f4afa-142">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="f4afa-142">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="f4afa-143">**ProcessRunCaller** を選択し、そして **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-143">Select **ProcessRunCaller** , and then select **Add**.</span></span>
6. <span data-ttu-id="f4afa-144">次のダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-144">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="f4afa-145">**スリープ** ワークフローの後に、 **プロセス** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-145">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="f4afa-146">ステップ 5 で、 **ProcessRunner** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-146">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="f4afa-147">**OK** を選択すると、 **プロセス** ワークフロー の後には、 **スリープ** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-147">Then, when you select **OK** , a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="f4afa-148">**ProcessRunCaller** および **ProcessRunner** ワークフローは、請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-148">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="f4afa-149">**ProcessRunCaller** は **ProcessRunner** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-149">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="f4afa-150">**ProcessRunner** は、実際に請求書を作成するワークフローです。</span><span class="sxs-lookup"><span data-stu-id="f4afa-150">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="f4afa-151">請求書を作成する必要のあるすべての契約品目を調べ、それらの明細の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-151">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="f4afa-152">契約書を作成する契約品目を決定するために、ジョブは契約品目の請求書の実行日を参照します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-152">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="f4afa-153">1 つの契約に属する契約品目の請求書実行日が同じ場合、トランザクションは、 2 つの請求明細行を持つ 1 つの請求書に統合されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-153">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="f4afa-154">請求書を作成するトランザクションがない場合、ジョブは請求書の作成をスキップします。</span><span class="sxs-lookup"><span data-stu-id="f4afa-154">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="f4afa-155">**ProcessRunner** の実行が完了すると、 **ProcessRunCaller** を呼び出して、終了時間が指定されてクローズされます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-155">After **ProcessRunner** has finished running, it calls **ProcessRunCaller** , provides the end time, and is closed.</span></span> <span data-ttu-id="f4afa-156">**ProcessRunCaller** は、指定された終了時刻から24時間実行するタイマーを開始します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-156">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="f4afa-157">タイマーが終了すると、 **ProcessRunCaller** が閉じられます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-157">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="f4afa-158">請求書を作成するバッチ処理ジョブは、定期的なジョブです。</span><span class="sxs-lookup"><span data-stu-id="f4afa-158">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="f4afa-159">このバッチ処理を何度も実行すると、ジョブの複数のインスタンスが作成され、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-159">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="f4afa-160">したがって、バッチ処理は一度だけ実行し、実行が停止した場合のみ、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4afa-160">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="f4afa-161">Project Service Automation でのバッチ請求は、請求スケジュールによって構成されたプロジェクトの契約品目に対してのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-161">Batch invoicing in Project Service Automation only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="f4afa-162">固定価格の請求方法の契約品目には、マイルストーンを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4afa-162">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="f4afa-163">時間と材料の請求方法を持つプロジェクト契約品目には、日付ベースの請求スケジュールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4afa-163">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="f4afa-164">見積依頼明細行に基づくプロジェクトのコンテキストでの請求頻度の設定に関する情報は、トピック [見積もりと見積依頼明細行](basic-quote-lines.md#invoice-schedule) で提供されています。</span><span class="sxs-lookup"><span data-stu-id="f4afa-164">Information about setting up invoicing frequencies in the context of a project that is based on a quote line, is provided in the topic, [Quotes and quote lines](basic-quote-lines.md#invoice-schedule).</span></span> <span data-ttu-id="f4afa-165">これは、プロジェクトベースの契約品目でも同じです。</span><span class="sxs-lookup"><span data-stu-id="f4afa-165">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-psa-invoice"></a><span data-ttu-id="f4afa-166">PSA 請求書の下書きを編集する</span><span class="sxs-lookup"><span data-stu-id="f4afa-166">Edit a draft PSA invoice</span></span>

<span data-ttu-id="f4afa-167">プロジェクト請求書のドラフトを作成すると、時間と経費のエントリが承認したときに作成された、すべての未請求営業トランザクションが、請求書にプルされます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-167">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="f4afa-168">請求書がまだドラフト段階である間は、次の調整を行うことができます:</span><span class="sxs-lookup"><span data-stu-id="f4afa-168">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="f4afa-169">請求明細行の詳細を削除、または編集します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-169">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="f4afa-170">数量や請求書の種類を編集、調整します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-170">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="f4afa-171">請求書にトランザクションとして直接、時間、経費、手数料を追加します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-171">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="f4afa-172">請求明細行が、これらの取引区分を許可する契約品目にマップされている場合、この機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-172">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="f4afa-173">請求書を確認するには、 **確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-173">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="f4afa-174">確認操作は、一方向の操作です。</span><span class="sxs-lookup"><span data-stu-id="f4afa-174">The Confirm action is a one-way action.</span></span> <span data-ttu-id="f4afa-175">**確認** を選択すると、システムは請求書を読み取り専用にし、各請求明細行の各請求明細行の詳細から請求済みの売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-175">When you select **Confirm** , the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="f4afa-176">請求明細行の詳細が未請求売上実績を参照する場合、システムは未請求売上実績も取り消します。</span><span class="sxs-lookup"><span data-stu-id="f4afa-176">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="f4afa-177">(時間または経費エントリから作成された請求明細行の詳細は、未請求売上実績を参照します)。総勘定元帳統合システムは、この取り消しを使用して、会計目的で進行中のプロジェクト作業 (WIP) を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-177">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-psa-invoice"></a><span data-ttu-id="f4afa-178">確認済みのPSA請求書を修正する</span><span class="sxs-lookup"><span data-stu-id="f4afa-178">Correct a confirmed PSA invoice</span></span>

<span data-ttu-id="f4afa-179">確認済みのPSA請求書は編集 (修正) できます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-179">Confirmed PSA invoices can be edited (corrected).</span></span> <span data-ttu-id="f4afa-180">確認済みの請求書を修正すると、新規修正請求書ドラフトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-180">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="f4afa-181">元の請求書のすべてのトランザクションと数量を取り消すことを前提としているため、この修正請求書には元の請求書のすべてのトランザクションが含まれ、その数量はすべて 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f4afa-181">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="f4afa-182">トランザクションが修正を必要とない場合、その修正請求書のドラフトから削除できます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-182">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="f4afa-183">部分的な数量を取り消す、または戻り場合は、明細行の詳細の **数量** フィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-183">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="f4afa-184">請求明細行の詳細を開くと、元の請求書の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-184">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="f4afa-185">その後、現在の請求書の数量を編集して、元の請求書の数量よりも少なく、または多くすることができます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-185">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="f4afa-186">修正請求書を確認すると、元の請求済み売上実績が取り消され、新規の請求済み売上実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-186">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="f4afa-187">数量が削減された場合、差異により未請求売上実績も作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-187">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="f4afa-188">たとえば、元の請求済み売上が 8 時間で、修正請求明細行の詳細の数量が 6 時間に減少した場合、PSAは元の請求済み売上品目を取り消し、新しい 2 つの実績を作成します:</span><span class="sxs-lookup"><span data-stu-id="f4afa-188">For example, if the original billed sales was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, PSA reverses the original billed sales line and creates two new actuals:</span></span>

- <span data-ttu-id="f4afa-189">6 時間の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="f4afa-189">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="f4afa-190">残り 2 時間の未請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="f4afa-190">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="f4afa-191">このトランザクションは、顧客との交渉に応じて後で請求するか、または、請求不可としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="f4afa-191">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
