---
title: 承認済みの時間または経費エントリの取り消し
description: このトピックでは、前に承認済みの時間と経費の入力を取り消す方法について説明します。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1a199985099745b2e62b844ef748ea2031054458
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283464"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="e48e1-103">承認済みの時間または経費エントリの取り消し</span><span class="sxs-lookup"><span data-stu-id="e48e1-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e48e1-104">プロジェクト チーム メンバーまたは時間エントリを提出するその他の人は、既に承認された時間や経費のエントリを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="e48e1-105">承認済みの時間や経費のエントリを取り消すためのプロセスには二つの手順があります:</span><span class="sxs-lookup"><span data-stu-id="e48e1-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="e48e1-106">提出者が取り消しを要求する。</span><span class="sxs-lookup"><span data-stu-id="e48e1-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="e48e1-107">承認者が取り消しを承認する。</span><span class="sxs-lookup"><span data-stu-id="e48e1-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="e48e1-108">取り消しの要求</span><span class="sxs-lookup"><span data-stu-id="e48e1-108">Request a recall</span></span>

<span data-ttu-id="e48e1-109">承認済みの時間や経費のエントリを取り消す要求をおこなうには以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="e48e1-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="e48e1-110">時間エントリについては、**プロジェクト** \> **自分の作業** \> **時間エントリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="e48e1-111">-または-</span><span class="sxs-lookup"><span data-stu-id="e48e1-111">–or–</span></span>

    <span data-ttu-id="e48e1-112">経費エントリについては、**プロジェクト** \> **自分の作業** \> **経費** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="e48e1-113">時間エントリの場合は、特定のプロジェクト タスクとの組み合わせ対してすべての時間エントリを選択します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="e48e1-114">または、グリッドで、特定プロジェクトの特定の日付の時間に対して個々のセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="e48e1-115">-または-</span><span class="sxs-lookup"><span data-stu-id="e48e1-115">–or–</span></span>

    <span data-ttu-id="e48e1-116">経費エントリについては、取り消す経費エントリの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="e48e1-117">**再呼び出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-117">Select **Recall**.</span></span> <span data-ttu-id="e48e1-118">確認ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="e48e1-119">選択した時間や経費エントリが既に承認されている場合は、取り消しの理由を入力するよう要求されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="e48e1-120">取り消しの理由を入力してから、操作を確認するには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="e48e1-121">エントリを承認する人にシステムから取り消しの要求が送信されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="e48e1-122">承認済みの時間エントリや経費エントリは取り消し可能ですが、承認された時間や経費がすでに顧客に請求済みの場合は、取り消し要求は作成できません。</span><span class="sxs-lookup"><span data-stu-id="e48e1-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="e48e1-123">取り消し要求の作成を試みているユーザーは、既に請求済みなのでこの時間または経費は取り消しできないことを示すメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="e48e1-124">取り消し要求の承認または拒否</span><span class="sxs-lookup"><span data-stu-id="e48e1-124">Approve or reject a recall request</span></span>

<span data-ttu-id="e48e1-125">次の手順に従って、取り消し要求を承認または拒否します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="e48e1-126">**プロジェクト** \> **マイ ワーク** \> **承認** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="e48e1-127">**承認** リストページで、**承認の取り消し要求** へとビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="e48e1-128">提出された取り消し要求の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="e48e1-129">一つまたは複数のエントリを選び、**承認** または **拒否** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="e48e1-130">**承認** を選択した場合、承認の影響に関する警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="e48e1-131">**OK** を選択して操作を確定します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="e48e1-132">取り消し要求が承認されました</span><span class="sxs-lookup"><span data-stu-id="e48e1-132">The recall request is approved.</span></span>

    <span data-ttu-id="e48e1-133">-または-</span><span class="sxs-lookup"><span data-stu-id="e48e1-133">–or–</span></span>

    <span data-ttu-id="e48e1-134">**拒否** を選択した場合、その取り消し要求は拒否されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="e48e1-135">取り消しが要求された際、取り消しが承認された際、システムはその時間エントリや経費エントリで請求が起きていないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="e48e1-136">エントリが既に請求済み、または下書きの請求書の状態にある場合、このエントリは既に請求済みなので時間や経費は承認することができないことを示すエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="e48e1-137">取り消し要求の影響</span><span class="sxs-lookup"><span data-stu-id="e48e1-137">Impact of a recall request</span></span>

<span data-ttu-id="e48e1-138">承認が取り消されると、運用上の影響と財務上の影響の両方があります。</span><span class="sxs-lookup"><span data-stu-id="e48e1-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="e48e1-139">運用面での影響</span><span class="sxs-lookup"><span data-stu-id="e48e1-139">Operational impact</span></span>

<span data-ttu-id="e48e1-140">取り消し要求が承認された場合、承認レコードは、**拒否済** としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="e48e1-141">このエントリの状態は、それが時間エントリか経費エントリかによって、**返却済** または **拒否済** へ変更されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="e48e1-142">プロジェクト チームのメンバは、エントリを表示して編集した後、エントリを再送信する、またはエントリを完全に削除できます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="e48e1-143">取り消し要求が拒否された場合、そのエントリの状態は **承認済** のままとなり、プロジェクトのプロジェクト チーム メンバーや承認者はそのエントリを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="e48e1-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="e48e1-144">財務面での影響</span><span class="sxs-lookup"><span data-stu-id="e48e1-144">Financial impact</span></span>

<span data-ttu-id="e48e1-145">取り消し要求が承認された場合、コストや営業の対応する実績が以下のように更新されます:</span><span class="sxs-lookup"><span data-stu-id="e48e1-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="e48e1-146">**精算状態** フィールドは **調整済** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="e48e1-147">**請求状態** フィールドは **キャンセル済** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="e48e1-148">次に、その反対のエントリが実績テーブルに作成されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="e48e1-149">反対のエントリを作成するにあたっては、システムが当初の実績からフィールド値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="e48e1-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="e48e1-150">コピーがされない値は数量の値のみです。</span><span class="sxs-lookup"><span data-stu-id="e48e1-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="e48e1-151">これらの値が逆になります。</span><span class="sxs-lookup"><span data-stu-id="e48e1-151">These values are reversed instead.</span></span> <span data-ttu-id="e48e1-152">反転した実績が **コスト** と **未請求の売上** の両方に作成されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="e48e1-153">反転した実績の **精算状態** フィールドは、**調整不能** に設定され、**請求状態** フィールドは **キャンセル済** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e48e1-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="e48e1-154">これらの変更が原因となり、プロジェクトの記録された支出と売り上げのバックログは、これらの実績を表す金額には相当しなくなります。</span><span class="sxs-lookup"><span data-stu-id="e48e1-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="e48e1-155">取り消し要求が拒否された場合、プロジェクトの財政面への影響はありません。</span><span class="sxs-lookup"><span data-stu-id="e48e1-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="e48e1-156">時間エントリ レコードへの変更</span><span class="sxs-lookup"><span data-stu-id="e48e1-156">Changes to time entry records</span></span>

<span data-ttu-id="e48e1-157">次の図は承認済みの時間エントリが取り消された場合に発生する変更を示します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![時間エントリ状態の切り替え](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="e48e1-159">経費エントリ レコードへの変更</span><span class="sxs-lookup"><span data-stu-id="e48e1-159">Changes to expense entry records</span></span>

<span data-ttu-id="e48e1-160">次の図は承認済みの経費エントリが取り消された場合に発生する変更を示します。</span><span class="sxs-lookup"><span data-stu-id="e48e1-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![経費エントリ状態の切り替え](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]