---
title: 経費管理のワークフロー
description: このトピックは、Microsoft Dynamics 365 Finance のワークフロー システムを使用して、経費管理で経費報告書のレビュープロセスを設定する方法について解説します。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271674"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="bc757-103">経費管理のワークフロー</span><span class="sxs-lookup"><span data-stu-id="bc757-103">Expense management workflow</span></span>

<span data-ttu-id="bc757-104">このトピックは、経費管理で経費報告書のレビュープロセスを設定する方法について解説します。</span><span class="sxs-lookup"><span data-stu-id="bc757-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="bc757-105">次の基準を使用して、経費報告書の承認者を決定するワークフローを設定することができます :</span><span class="sxs-lookup"><span data-stu-id="bc757-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="bc757-106">従業員のレポート階層と事前定義された承認制限</span><span class="sxs-lookup"><span data-stu-id="bc757-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="bc757-107">暫定承認者と最終承認者をサポートする複数レベルの承認</span><span class="sxs-lookup"><span data-stu-id="bc757-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="bc757-108">財務的側面とプロジェクトの責任</span><span class="sxs-lookup"><span data-stu-id="bc757-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="bc757-109">特定のユーザー、またはユーザー グループへの割り当て</span><span class="sxs-lookup"><span data-stu-id="bc757-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="bc757-110">ワークフローの承認は、経費報告書、出張の要求、仮払金、付加価値税 (VAT) の精算に使用できます。</span><span class="sxs-lookup"><span data-stu-id="bc757-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="bc757-111">**例**</span><span class="sxs-lookup"><span data-stu-id="bc757-111">**Example**</span></span>

<span data-ttu-id="bc757-112">次のプロセスは、経費報告書の経費管理ワークフローの例です。</span><span class="sxs-lookup"><span data-stu-id="bc757-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="bc757-113">従業員が経費報告書を作成して保存します。</span><span class="sxs-lookup"><span data-stu-id="bc757-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="bc757-114">従業員の経費報告書を提出して承認を待機します。</span><span class="sxs-lookup"><span data-stu-id="bc757-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="bc757-115">承認者は、ワークフローの設定時に定義されたルールに基づいて識別されます。</span><span class="sxs-lookup"><span data-stu-id="bc757-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="bc757-116">承認者は、経費報告書の承認準備が整った旨の通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="bc757-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="bc757-117">承認者は経費報告書を確認し、次の条件が満たされていることを確認します :</span><span class="sxs-lookup"><span data-stu-id="bc757-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="bc757-118">経費は経費方針に違反していないこと。</span><span class="sxs-lookup"><span data-stu-id="bc757-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="bc757-119">経費が本心に違反している場合、承認者は経費レポートに正当な業務上の理由が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc757-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="bc757-120">経費報告書には電子領収書が添付されています。</span><span class="sxs-lookup"><span data-stu-id="bc757-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="bc757-121">承認者が経費報告書を承認します。</span><span class="sxs-lookup"><span data-stu-id="bc757-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="bc757-122">経費報告書は、買掛金コーディネーターに割り当てられて転記されます。</span><span class="sxs-lookup"><span data-stu-id="bc757-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="bc757-123">自動転記の構成に応じて、次のいずれかの手順が発生します :</span><span class="sxs-lookup"><span data-stu-id="bc757-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="bc757-124">自動転記が設定されている場合、経費報告書支払い処理が行われ、経費報告書のステータスが更新されます。</span><span class="sxs-lookup"><span data-stu-id="bc757-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="bc757-125">自動転記が構成されていない場合、買掛金コーディネーターは、すべての領収書の原本が提出されているかどうか、領収書が経費報告書の経費と一致しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc757-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="bc757-126">経費報告書に入力されているすべての税コードが正しいことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc757-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="bc757-127">これらの要件を確認後、経費報告書が転記されます。</span><span class="sxs-lookup"><span data-stu-id="bc757-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="bc757-128">経費報告書が転記された後、経費報告書の支払いが承認され、従業員に精算されます。</span><span class="sxs-lookup"><span data-stu-id="bc757-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]