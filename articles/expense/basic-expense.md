---
title: 経費の入力 (ライト)
description: このトピックでは、ライト展開で経費エントリを処理する方法について説明します。
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590952"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="e63f0-103">経費の入力 (ライト)</span><span class="sxs-lookup"><span data-stu-id="e63f0-103">Expense entry (lite)</span></span>

<span data-ttu-id="e63f0-104">_**適用対象:** ライト展開- 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="e63f0-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e63f0-105">ベーシック、またはライトな経費管理は、単純な経費を記録する機能です。</span><span class="sxs-lookup"><span data-stu-id="e63f0-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="e63f0-106">プロジェクトに対する経費を記録することができ、プロジェクトの承認者がそれらを確認して承認します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="e63f0-107">Dynamics 365 Project Operations の経費機能の詳細については [経費の概要](expense-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e63f0-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="e63f0-108">基本経費を取り込む</span><span class="sxs-lookup"><span data-stu-id="e63f0-108">Capture a basic expense</span></span>

<span data-ttu-id="e63f0-109">経費を取り込んで、承認者に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="e63f0-110">**経費** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="e63f0-111">**新規経費** ページで必要な経費情報を入力し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e63f0-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="e63f0-112">基本経費を送信する</span><span class="sxs-lookup"><span data-stu-id="e63f0-112">Submit a basic expense</span></span>

<span data-ttu-id="e63f0-113">すべての経費の取り込みが完了し、承認を受ける準備ができたら、送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e63f0-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="e63f0-114">**経費** に移動し、経費の選択をします。</span><span class="sxs-lookup"><span data-stu-id="e63f0-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="e63f0-115">または、ヘッダーのチェック ボックスを使用してすべての経費を選択します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="e63f0-116">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-116">Select **Submit**.</span></span> <span data-ttu-id="e63f0-117">選択したエントリが処理され、経費承認要求が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="e63f0-118">添付ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="e63f0-118">Add an attachment</span></span>

<span data-ttu-id="e63f0-119">経費に関する文書を承認者にさらに提供する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="e63f0-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="e63f0-120">経費入力のタイムラインで領収書を添付できます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="e63f0-121">**タイムライン** セクションで **編集** を選択し、ペーパークリップ アイコンを選択して領収書を添付します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="e63f0-122">基本経費を取り消す</span><span class="sxs-lookup"><span data-stu-id="e63f0-122">Recall a basic expense</span></span>

<span data-ttu-id="e63f0-123">誤って経費を送信した場合、それを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="e63f0-124">経費エントリを取り消すのに必要な時間は、その承認段階によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e63f0-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="e63f0-125">承認者がまだエントリを承認していない場合、取り消しは即時に実行する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e63f0-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="e63f0-126">ただし、エントリがすでに承認されている場合、承認者は取り消しを承認し、トランザクションを取り消すように求められます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="e63f0-127">**経費** に移動し、次に経費のリストで、取り消す経費を選択します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="e63f0-128">**再呼び出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-128">Select **Recall**.</span></span> <span data-ttu-id="e63f0-129">経費エントリがまだ承認されていない場合、システムはすぐにそれを取り消します。</span><span class="sxs-lookup"><span data-stu-id="e63f0-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="e63f0-130">経費エントリがすでに承認されている場合は、経費を取り消す必要があることを承認者に通知するための取り消し要求が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="e63f0-131">その後、承認者は取り消しを実行できることを確認し、エントリが返されます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="e63f0-132">基本経費を削除する</span><span class="sxs-lookup"><span data-stu-id="e63f0-132">Delete a basic expense</span></span>

<span data-ttu-id="e63f0-133">まだ送信されていない経費は削除できます。</span><span class="sxs-lookup"><span data-stu-id="e63f0-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="e63f0-134">すでに提出されている経費を削除するには、最初にそれを取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e63f0-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="e63f0-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e63f0-135">See also</span></span>

- [<span data-ttu-id="e63f0-136">承認の概要</span><span class="sxs-lookup"><span data-stu-id="e63f0-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
