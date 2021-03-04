---
title: 経費精算書における複数の承認者
description: このトピックでは、複数の人物による承認を行う経費報告書について説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960613"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="68e1e-103">経費精算書における複数の承認者</span><span class="sxs-lookup"><span data-stu-id="68e1e-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="68e1e-104">組織の経費承認ポリシーによっては、送信された経費報告書に対して複数の人物による承認が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="68e1e-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="68e1e-105">経費報告書承認のワークフロー プロセスを設定する場合、1 つ以上の経費報告書承認者のタスク、またはステップを含むワークフロー要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="68e1e-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="68e1e-106">たとえば、すべての経費報告書に対して、まず報告書を提出した従業員のマネージャーが承認し、次に買掛金コーディネーターが承認するように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="68e1e-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="68e1e-107">複数の経費報告書承認者を必要とする場合は、以下のいずれかの方法でワークフロー要素を追加できます:</span><span class="sxs-lookup"><span data-stu-id="68e1e-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="68e1e-108">1 つの承認段階を持つ、 1 つの承認要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="68e1e-108">Add one approval element that has one step.</span></span> <span data-ttu-id="68e1e-109">たとえば、このステップでは、経費報告書をユーザー グループに割り当て、ユーザー グループのメンバーの 50％ の承認を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="68e1e-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="68e1e-110">複数の承認段階を持つ 1 つの承認要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="68e1e-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="68e1e-111">たとえば、承認要素には次のステップがあります :</span><span class="sxs-lookup"><span data-stu-id="68e1e-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="68e1e-112">経費報告書を提出した従業員の上司が承認する。</span><span class="sxs-lookup"><span data-stu-id="68e1e-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="68e1e-113">買掛金担当者が領収書と経費精算書を確認する。</span><span class="sxs-lookup"><span data-stu-id="68e1e-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="68e1e-114">予算所有者が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="68e1e-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="68e1e-115">それぞれが 1 つの承認段階を持つ複数の承認要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="68e1e-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="68e1e-116">たとえば、次の手順ごとに個別の承認要素を追加することができます :</span><span class="sxs-lookup"><span data-stu-id="68e1e-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="68e1e-117">従業員の上司が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="68e1e-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="68e1e-118">予算所有者が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="68e1e-118">The budget owner approves the expense report.</span></span>
