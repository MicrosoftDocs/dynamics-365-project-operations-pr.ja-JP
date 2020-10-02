---
title: 手動で見積もり請求書を作成する
description: このトピックでは、見積もり請求書の作成について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896112"
---
# <a name="create-a-manual-proforma-invoice"></a><span data-ttu-id="7f5d9-103">手動で見積もり請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="7f5d9-103">Create a manual proforma invoice</span></span>

<span data-ttu-id="7f5d9-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="7f5d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7f5d9-105">請求書を作成することで、プロジェクト マネージャーは、顧客に向けた請求書を作成する前に、2段階の承認を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-105">Invoicing gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="7f5d9-106">プロジェクト チーム メンバーが送信する時間と経費のエントリが承認されると、第 1 レベルの承認が完了します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-106">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="7f5d9-107">Dynamics 365 プロジェクト オペレーションでは、次の理由により、顧客向けの請求書を生成するように設計されていません :</span><span class="sxs-lookup"><span data-stu-id="7f5d9-107">Dynamics 365 Project Operations isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="7f5d9-108">税務情報は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-108">It doesn't contain tax information.</span></span>
- <span data-ttu-id="7f5d9-109">正しく設定された為替レートを使用して、他の通貨を請求通貨に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-109">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="7f5d9-110">請求書を印刷できるように正しく書式設定できません。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-110">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="7f5d9-111">代わりに、財務または会計システムを使用して、生成された請求書提案書の情報を使用した顧客向けの請求書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-111">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from generated invoice proposals.</span></span>

## <a name="creating-project-invoices"></a><span data-ttu-id="7f5d9-112">プロジェクトの請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="7f5d9-112">Creating project invoices</span></span>

<span data-ttu-id="7f5d9-113">プロジェクトの請求書は 1 つずつ、または一括して作成できます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-113">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="7f5d9-114">手動で作成できます。また、自動実行で生成するように設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-114">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices"></a><span data-ttu-id="7f5d9-115">プロジェクトの請求書を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="7f5d9-115">Manually create project invoices</span></span> 

<span data-ttu-id="7f5d9-116">**プロジェクト契約** 一覧ページから、プロジェクト契約ごとに個別にプロジェクト請求書を作成することも、複数のプロジェクト契約に対して一括で請求書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-116">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="7f5d9-117">特定のプロジェクト契約の請求書を作成するには、このステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-117">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="7f5d9-118">**プロジェクト契約** リスト ページで、プロジェクト契約を開き、 **請求書の​​作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-118">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    <span data-ttu-id="7f5d9-119">ステータスが **請求準備完了** の選択したプロジェクト契約の全トランザクションに対して請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="7f5d9-120">これらのトランザクションには、時間、経費、マイルストーン、製品ベースの契約品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="7f5d9-121">一括で請求書を作成するには、次の手順に実行します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="7f5d9-122">**プロジェクト契約** 一覧ページで、請求書を作成する必要のあるプロジェクト契約を 1 つ以上選択し、 **プロジェクト請求書の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    <span data-ttu-id="7f5d9-123">警告メッセージは、請求書が作成される前に遅延が発生する可能性があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-123">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="7f5d9-124">プロセスも表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-124">The process is also shown.</span></span>

2. <span data-ttu-id="7f5d9-125">**OK** を選択して、メッセージ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-125">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="7f5d9-126">ステータスが **請求準備完了** の契約品目の全トランザクションに対して請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-126">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="7f5d9-127">これらのトランザクションには、時間、経費、マイルストーン、製品ベースの契約品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-127">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="7f5d9-128">生成された請求書を表示するには、 **営業** \> **請求先** \> **請求書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-128">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="7f5d9-129">プロジェクト契約ごとに 1 つの請求書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-129">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices"></a><span data-ttu-id="7f5d9-130">プロジェクト請求書の自動作成を設定する</span><span class="sxs-lookup"><span data-stu-id="7f5d9-130">Set up automated creation of project invoices</span></span> 

<span data-ttu-id="7f5d9-131">請求書の自動化を実行するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-131">Follow these steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="7f5d9-132">**設定** \> **バッチ ジョブ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-132">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="7f5d9-133">バッチ ジョブを作成し、 **プロジェクト オペレーション請求書の作成** と名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-133">Create a batch job, and name it **Project Operations Create Invoices**.</span></span> <span data-ttu-id="7f5d9-134">バッチ ジョブの名前に、「請求書の作成」という語句を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-134">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="7f5d9-135">**ジョブの種類** フィールドで、 **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-135">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="7f5d9-136">既定で、 **頻度 毎日** および **アクティブ** オプションは **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-136">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="7f5d9-137">**ワークフローの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-137">Select **Run Workflow**.</span></span> <span data-ttu-id="7f5d9-138">**レコードの検索** ダイアログ ボックスで、 3 つのワークフローが表示されます:</span><span class="sxs-lookup"><span data-stu-id="7f5d9-138">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="7f5d9-139">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="7f5d9-139">ProcessRunCaller</span></span>
    - <span data-ttu-id="7f5d9-140">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="7f5d9-140">ProcessRunner</span></span>
    - <span data-ttu-id="7f5d9-141">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="7f5d9-141">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="7f5d9-142">**ProcessRunCaller** を選択し、そして **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-142">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="7f5d9-143">次のダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-143">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="7f5d9-144">**スリープ** ワークフローの後に、 **プロセス** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-144">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="7f5d9-145">ステップ 5 で、 **ProcessRunner** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-145">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="7f5d9-146">**OK** を選択すると、 **プロセス** ワークフロー の後には、 **スリープ** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-146">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="7f5d9-147">**ProcessRunCaller** および **ProcessRunner** ワークフローは、請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-147">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="7f5d9-148">**ProcessRunCaller** は **ProcessRunner** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-148">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="7f5d9-149">**ProcessRunner** は、実際に請求書を作成するワークフローです。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-149">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="7f5d9-150">請求書を作成する必要のあるすべての契約品目を調べ、それらの明細の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-150">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="7f5d9-151">契約書を作成する契約品目を決定するために、ジョブは契約品目の請求書の実行日を参照します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-151">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="7f5d9-152">1 つの契約に属する契約品目の請求書実行日が同じ場合、トランザクションは、 2 つの請求明細行を持つ 1 つの請求書に統合されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-152">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="7f5d9-153">請求書を作成するトランザクションがない場合、ジョブは請求書の作成をスキップします。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-153">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="7f5d9-154">**ProcessRunner** の実行が完了すると、 **ProcessRunCaller** を呼び出して、終了時間が指定されてクローズされます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-154">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="7f5d9-155">**ProcessRunCaller** は、指定された終了時刻から24時間実行するタイマーを開始します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-155">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="7f5d9-156">タイマーが終了すると、 **ProcessRunCaller** が閉じられます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-156">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="7f5d9-157">請求書を作成するバッチ処理ジョブは、定期的なジョブです。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-157">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="7f5d9-158">このバッチ処理を何度も実行すると、ジョブの複数のインスタンスが作成され、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-158">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="7f5d9-159">したがって、バッチ処理は一度だけ実行し、実行が停止した場合のみ、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-159">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="7f5d9-160">バッチ請求は、請求スケジュールで構成されたプロジェクト契約明細に対してのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-160">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="7f5d9-161">固定価格の請求方法の契約品目には、マイルストーンを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-161">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="7f5d9-162">時間と材料の請求方法を持つプロジェクト契約品目には、日付ベースの請求スケジュールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-162">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="7f5d9-163">これは、プロジェクトベースの契約品目でも同じです。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-163">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-invoice"></a><span data-ttu-id="7f5d9-164">請求書の下書きを編集する</span><span class="sxs-lookup"><span data-stu-id="7f5d9-164">Edit a draft invoice</span></span>

<span data-ttu-id="7f5d9-165">プロジェクト請求書のドラフトを作成すると、時間と経費のエントリが承認したときに作成された、すべての未請求営業トランザクションが、請求書にプルされます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-165">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="7f5d9-166">請求書がまだドラフト段階である間は、次の調整を行うことができます:</span><span class="sxs-lookup"><span data-stu-id="7f5d9-166">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="7f5d9-167">請求明細行の詳細を削除、または編集します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-167">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="7f5d9-168">数量や請求書の種類を編集、調整します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-168">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="7f5d9-169">請求書にトランザクションとして直接、時間、経費、手数料を追加します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-169">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="7f5d9-170">請求明細行が、これらの取引区分を許可する契約品目にマップされている場合、この機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-170">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="7f5d9-171">請求書を確認するには、 **確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-171">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="7f5d9-172">確認操作は、一方向の操作です。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-172">The Confirm action is a one-way action.</span></span> <span data-ttu-id="7f5d9-173">**確認** を選択すると、システムは請求書を読み取り専用にし、各請求明細行の各請求明細行の詳細から請求済みの売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-173">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="7f5d9-174">請求明細行の詳細が未請求売上実績を参照する場合、システムは未請求売上実績も取り消します。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-174">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="7f5d9-175">(時間または経費エントリから作成された請求明細行の詳細は、未請求売上実績を参照します)。総勘定元帳統合システムは、この取り消しを使用して、会計目的で進行中のプロジェクト作業 (WIP) を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-175">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-invoice"></a><span data-ttu-id="7f5d9-176">確認済みの請求書を修正する</span><span class="sxs-lookup"><span data-stu-id="7f5d9-176">Correct a confirmed invoice</span></span>

<span data-ttu-id="7f5d9-177">確認済みの請求書は編集 (修正) できます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-177">Confirmed invoices can be edited (corrected).</span></span> <span data-ttu-id="7f5d9-178">確認済みの請求書を修正すると、新規修正請求書ドラフトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-178">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="7f5d9-179">元の請求書のすべてのトランザクションと数量を取り消すことを前提としているため、この修正請求書には元の請求書のすべてのトランザクションが含まれ、その数量はすべて 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-179">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="7f5d9-180">トランザクションが修正を必要とない場合、その修正請求書のドラフトから削除できます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-180">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="7f5d9-181">部分的な数量を取り消す、または戻り場合は、明細行の詳細の **数量** フィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-181">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="7f5d9-182">請求明細行の詳細を開くと、元の請求書の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-182">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="7f5d9-183">その後、現在の請求書の数量を編集して、元の請求書の数量よりも少なく、または多くすることができます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-183">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="7f5d9-184">修正請求書を確認すると、元の請求済み売上実績が取り消され、新規の請求済み売上実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-184">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="7f5d9-185">数量が削減された場合、差異により未請求売上実績も作成されます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-185">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="7f5d9-186">例えば、元の請求済み売上が 8 時間分であり、修正された請求明細行の詳細の数量が 6 時間に減少した場合、元の請求売上明細行を戻し、新たに 2 つの実績が作成されます :</span><span class="sxs-lookup"><span data-stu-id="7f5d9-186">For example, if the original billed sale was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, the original billed sales line is reversed and two new actuals are created:</span></span>

- <span data-ttu-id="7f5d9-187">6 時間の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-187">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="7f5d9-188">残り 2 時間の未請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-188">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="7f5d9-189">このトランザクションは、顧客との交渉に応じて後で請求するか、または、請求不可としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="7f5d9-189">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
