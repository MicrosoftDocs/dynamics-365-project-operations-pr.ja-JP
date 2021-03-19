---
title: 以前に承認された時間と経費の入力の取り消しを行う
description: このトピックでは、承認済みの時間と経費の入力を取り消す方法についての情報を提供します。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290860"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="52375-103">以前に承認された時間と経費の入力を取り消しを行う</span><span class="sxs-lookup"><span data-stu-id="52375-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52375-104">Dynamics 365 Project Service Automationの最新バージョンでは、承認者は承認をした時間と経費の入力を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="52375-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="52375-105">以前に承認された時間と経費の入力の取り消しを行う</span><span class="sxs-lookup"><span data-stu-id="52375-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="52375-106">承認済みの時間と経費の入力を取り消すには以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="52375-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="52375-107">**プロジェクト** \> **マイ ワーク** \> **承認** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="52375-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="52375-108">**承認** 一覧のページで、 **過去の承認** へとビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="52375-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="52375-109">これまでに承認した時間、経費エントリの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52375-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="52375-110">一つまたは複数のエントリーを選び、 **承認をキャンセルする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52375-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="52375-111">警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="52375-111">You receive a warning message.</span></span>
4. <span data-ttu-id="52375-112">承認を取り消すには、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52375-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="52375-113">承認済みの時間と経費入力の取り消しについての影響を理解する</span><span class="sxs-lookup"><span data-stu-id="52375-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="52375-114">承認がキャンセルされると、運用上への影響と財務上の影響があります。</span><span class="sxs-lookup"><span data-stu-id="52375-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="52375-115">運用面の影響</span><span class="sxs-lookup"><span data-stu-id="52375-115">Operational impact</span></span>

<span data-ttu-id="52375-116">運用の面では、承認がキャンセルされるとレコードの状態が **下書き** にリセットされ、 **過去の承認** ビューに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="52375-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="52375-117">その代わりに、取り消された承認は **承認待ちの時間エントリ** ビュー、または **承認待ちの経費エントリ** ビューに表示され、時間エントリか経費エントリであるかによって変わります。</span><span class="sxs-lookup"><span data-stu-id="52375-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="52375-118">また、時間エントリや経費エントリの状態が **提出済み** に変更され、これに関連するエントリは、ステータスが **下書き** の承認と一貫性を持ちます。</span><span class="sxs-lookup"><span data-stu-id="52375-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="52375-119">承認者は、 **下書き** 状態となっている承認の一部のフィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="52375-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="52375-120">これらのフィールドには、 **請求の種類** および **時間エントリの請求可能時間** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="52375-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="52375-121">変更を行った後、再度レコードを承認することができます。</span><span class="sxs-lookup"><span data-stu-id="52375-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="52375-122">また、当該エントリを否認することができます。</span><span class="sxs-lookup"><span data-stu-id="52375-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="52375-123">時間エントリを承認を拒否すると、エンティティの状態が **差し戻し** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="52375-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="52375-124">経費エントリの承認を拒否すると、エンティティの状態が **否認** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="52375-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="52375-125">機能的には、差し戻しや否認されたエントリは **下書き** 状態のエントリと同様の動作をします。</span><span class="sxs-lookup"><span data-stu-id="52375-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="52375-126">プロジェクト チーム メンバーは、エントリに必要な変更を加えてから承認に向けて再提出をするか、エントリを完全に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="52375-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="52375-127">財務面での影響</span><span class="sxs-lookup"><span data-stu-id="52375-127">Financial impact</span></span>

<span data-ttu-id="52375-128">承認がキャンセルされると、プロジェクトは財務上の影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="52375-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="52375-129">まず、原価と売上に関連する実績が以下のように更新されます:</span><span class="sxs-lookup"><span data-stu-id="52375-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="52375-130">調整の状態は、 **調整済み** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="52375-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="52375-131">請求の状態は、 **キャンセル** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="52375-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="52375-132">次に、その反対のエントリが実績テーブルに作成されます。</span><span class="sxs-lookup"><span data-stu-id="52375-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="52375-133">反対のエントリを作成するにあたっては、システムが当初の実績からフィールド値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="52375-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="52375-134">コピーがされない値は数量の値のみです。</span><span class="sxs-lookup"><span data-stu-id="52375-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="52375-135">これらの値が逆になります。</span><span class="sxs-lookup"><span data-stu-id="52375-135">These values are reversed instead.</span></span> <span data-ttu-id="52375-136">反転した実績が **コスト** と **未請求の売上** の両方に作成されます。</span><span class="sxs-lookup"><span data-stu-id="52375-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="52375-137">反転した実績の **状態の調整** フィールドは **調整不可** に設定され、請求書の状態は **キャンセル** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="52375-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="52375-138">これらの変更が行われた後は、プロジェクトへの支出として記録された金額およびプロジェクトの収益バックログが、これらの実績が表す金額となります。</span><span class="sxs-lookup"><span data-stu-id="52375-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]