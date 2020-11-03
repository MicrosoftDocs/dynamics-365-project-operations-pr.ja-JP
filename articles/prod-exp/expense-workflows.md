---
title: 経費管理のワークフローを設定する
description: ワークフロー プロセスを設定して出張ドキュメントや経費ドキュメントをレビューすることができます。
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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079422"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="7d6b8-103">経費管理のワークフローを設定する</span><span class="sxs-lookup"><span data-stu-id="7d6b8-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d6b8-104">ワークフローのプロセスを設定することで、出張ドキュメントや経費ドキュメントをレビューすることができます。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="7d6b8-105">ワークフローを定義できるドキュメントには、経費報告書、出張依頼書、現金前払い依頼書などがあります。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="7d6b8-106">ワークフローは業務プロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-106">A workflow represents a business process.</span></span> <span data-ttu-id="7d6b8-107">これは、ドキュメントのシステム内のフローを定義し、タスクの完了や承認を行う人物を示すものです。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="7d6b8-108">組織でワークフロー システムを使用する利点はいくつか考えられます :</span><span class="sxs-lookup"><span data-stu-id="7d6b8-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="7d6b8-109">**一貫性のあるプロセス** - 購買要求書や経費報告書など、特定のドキュメントの承認プロセスを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="7d6b8-110">ワークフロー システムを使用することで、一貫性のある効率的な方法でドキュメントを処理し、承認することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="7d6b8-111">プロセスの可視性 — ワークフロー システムでは、特定のワークフロー インスタンスのステータス、履歴、パフォーマンスの指標を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="7d6b8-112">これにより、効率改善にあたってワークフローに変更を加えるべきかどうかを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="7d6b8-113">作業一覧の集中管理 —ユーザーは、集中管理された作業の一覧を表示して、自分に割り当てられたワークフロー タスクや承認を表示します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="7d6b8-114">**作成できるワークフローの種類**</span><span class="sxs-lookup"><span data-stu-id="7d6b8-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="7d6b8-115">次の表は、 **経費** で作成できるワークフロー タイプの一覧を表わしています。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="7d6b8-116"><strong>型</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="7d6b8-117"><strong>このタイプを次に使用する :</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="7d6b8-118"><strong>経費レポート</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="7d6b8-119">経費報告書で使用する承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="7d6b8-120"><strong>経費精算書の自動転記</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="7d6b8-121">経費報告書で使用する自動転記ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="7d6b8-122"><strong>経費の明細品目</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="7d6b8-123">経費報告書の明細品目で使用する承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="7d6b8-124"><strong>経費明細品目の自動転記</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="7d6b8-125">経費報告書の明細品目で使用する自動転記ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="7d6b8-126"><strong>出張費要求</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="7d6b8-127">出張申請書の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="7d6b8-128"><strong>現金前払い申請</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="7d6b8-129">現金前払い申請の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="7d6b8-130"><strong>VAT 過誤納税の還付</strong></span><span class="sxs-lookup"><span data-stu-id="7d6b8-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="7d6b8-131">付加価値税 (VAT) の還付に使用する承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6b8-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

