---
title: 経費精算書における複数の承認者
description: このトピックでは、複数の人物による承認を行う経費報告書について説明します。
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005257"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="0ded3-103">経費精算書における複数の承認者</span><span class="sxs-lookup"><span data-stu-id="0ded3-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="0ded3-104">組織の経費承認ポリシーによっては、送信された経費報告書に対して複数の人物による承認が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0ded3-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="0ded3-105">経費報告書承認のワークフロー プロセスを設定する場合、1 つ以上の経費報告書承認者のタスク、またはステップを含むワークフロー要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0ded3-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0ded3-106">たとえば、すべての経費報告書に対して、まず報告書を提出した従業員のマネージャーが承認し、次に買掛金コーディネーターが承認するように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="0ded3-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="0ded3-107">複数の経費報告書承認者を必要とする場合は、以下のいずれかの方法でワークフロー要素を追加できます:</span><span class="sxs-lookup"><span data-stu-id="0ded3-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0ded3-108">1 つのステップを持つ承認要素を 1 つ追加する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-108">Add one approval element that has one step.</span></span> <span data-ttu-id="0ded3-109">たとえば、このステップでは、経費精算書をユーザー グループに割り当て、ユーザー グループのメンバーの 50% がこれを承認する必要があると設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0ded3-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0ded3-110">複数のステップを含む承認要素を 1 つ追加する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0ded3-111">たとえば、承認要素には次のステップが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0ded3-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0ded3-112">経費精算書を提出した従業員の上司が精算書を承認する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0ded3-113">買掛金勘定の事務員が領収書と経費精算書の品目を確認する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0ded3-114">予算の所有者が経費精算書を承認する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0ded3-115">それぞれ 1 つのステップを含む複数の承認要素を追加する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0ded3-116">たとえば、次の各ステップに個別の承認要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0ded3-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0ded3-117">従業員の上司が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0ded3-118">予算所有者が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="0ded3-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]