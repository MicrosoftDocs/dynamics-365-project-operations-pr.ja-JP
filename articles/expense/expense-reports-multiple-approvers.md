---
title: 経費精算書と複数の承認者
description: このトピックでは、複数の人物による承認を必要とする経費報告書について説明します。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002062"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="bf8e5-103">経費精算書と複数の承認者</span><span class="sxs-lookup"><span data-stu-id="bf8e5-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="bf8e5-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="bf8e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf8e5-105">組織の経費承認ポリシーによっては、送信された経費レポートを複数の人物による承認が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="bf8e5-106">経費精算書の承認ワークフロー プロセスを設定するときに、1 人以上の経費精算書承認者用のタスクまたはステップを含むワークフロー要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="bf8e5-107">たとえば、すべての経費精算書について、精算書を提出した従業員の上司と買掛金勘定コーディネーターの 2 人にそれぞれ承認を要求する場合などです。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="bf8e5-108">経費精算書に複数の承認者を設定する場合は、次の方法でワークフロー要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="bf8e5-109">1 つのステップを持つ承認要素を 1 つ追加する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-109">Add one approval element that has one step.</span></span> <span data-ttu-id="bf8e5-110">たとえば、このステップでは、経費精算書をユーザー グループに割り当て、ユーザー グループのメンバーの 50% がこれを承認する必要があると設定することができます。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="bf8e5-111">複数のステップを含む承認要素を 1 つ追加する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="bf8e5-112">たとえば、承認要素には次のステップが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="bf8e5-113">経費精算書を提出した従業員の上司が精算書を承認する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="bf8e5-114">買掛金勘定の事務員が領収書と経費精算書の品目を確認する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="bf8e5-115">予算の所有者が経費精算書を承認する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="bf8e5-116">それぞれ 1 つのステップを含む複数の承認要素を追加する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="bf8e5-117">たとえば、次の各ステップに個別の承認要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="bf8e5-118">従業員の上司が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="bf8e5-119">予算所有者が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="bf8e5-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]