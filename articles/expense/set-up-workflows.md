---
title: 経費管理のワークフローを設定する
description: ワークフローのプロセスを設定することで、出張ドキュメントや経費ドキュメントをレビューすることができます。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276039"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="43fa5-103">経費管理のワークフローを設定する</span><span class="sxs-lookup"><span data-stu-id="43fa5-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="43fa5-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="43fa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="43fa5-105">ワークフロー プロセスを設定して出張ドキュメントや経費ドキュメントをレビューすることができます。</span><span class="sxs-lookup"><span data-stu-id="43fa5-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="43fa5-106">経費報告書、出張申請書、および現金前払い依頼書のワークフローを定義できます。</span><span class="sxs-lookup"><span data-stu-id="43fa5-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="43fa5-107">ワークフローはビジネスプロセスを表し、システムを介してドキュメントがどのように流れるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="43fa5-108">ワークフローは、誰がタスクを完了しなければならないか、または文書を承認しなければならないかを示します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="43fa5-109">組織でワークフロー システムを使用する利点はいくつか考えられます :</span><span class="sxs-lookup"><span data-stu-id="43fa5-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="43fa5-110">**一貫性のあるプロセス** : 購買依頼や経費報告書など、特定のドキュメントの承認プロセスを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="43fa5-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="43fa5-111">ワークフローシステムを使用することで、一貫性のある効率的な方法で文書を処理し、承認することができます。</span><span class="sxs-lookup"><span data-stu-id="43fa5-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="43fa5-112">**プロセスの可視性** : ワークフロー システムでは、特定のワークフロー インスタンスのステータス、履歴、パフォーマンスの指標を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="43fa5-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="43fa5-113">これにより、効率改善にあたってワークフローに変更を加えるべきかどうかを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="43fa5-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="43fa5-114">**集中管理された作業の一覧** : ユーザーは、集中管理された作業の一覧を表示して、自分に割り当てられたワークフロー タスクや承認を表示します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="43fa5-115">ワークフローのタイプ</span><span class="sxs-lookup"><span data-stu-id="43fa5-115">Workflow types</span></span>

<span data-ttu-id="43fa5-116">次の表は、**経費管理** で作成できるワークフローのタイプの一覧を表わしています。</span><span class="sxs-lookup"><span data-stu-id="43fa5-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="43fa5-117"><strong>型</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="43fa5-118"><strong>このタイプを次に使用する :</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="43fa5-119"><strong>経費精算書の自動承認</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="43fa5-120">経費報告書で使用する承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="43fa5-121"><strong>経費精算書の自動転記</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="43fa5-122">経費報告書で使用する自動転記ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="43fa5-123"><strong>経費の明細品目</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="43fa5-124">経費報告書の明細品目で使用する承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="43fa5-125"><strong>経費明細品目の自動転記</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="43fa5-126">経費報告書の明細品目で使用する自動転記ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="43fa5-127"><strong>出張費要求</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="43fa5-128">出張申請書の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="43fa5-129"><strong>現金前払い申請</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="43fa5-130">現金前払い申請の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="43fa5-131"><strong>VAT 過誤納税の還付</strong></span><span class="sxs-lookup"><span data-stu-id="43fa5-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="43fa5-132">付加価値税 (VAT) の還付に使用する承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="43fa5-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]