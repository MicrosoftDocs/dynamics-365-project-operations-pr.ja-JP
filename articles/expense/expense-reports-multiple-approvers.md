---
title: 経費精算書と複数の承認者
description: このトピックでは、複数の人物による承認を必要とする経費報告書について説明します。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079271"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="1d6a4-103">経費精算書と複数の承認者</span><span class="sxs-lookup"><span data-stu-id="1d6a4-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="1d6a4-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1d6a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d6a4-105">組織の経費承認ポリシーによっては、送信された経費レポートを複数の人物による承認が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="1d6a4-106">経費報告書承認のワークフロー プロセスを設定する場合、1 つ以上の経費報告書承認者のタスク、またはステップを含むワークフロー要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="1d6a4-107">たとえば、すべての経費報告書に対して、報告書を提出した従業員の上司と買掛金コーディネーターの 2 人の別々の人物による承認が必要となる要件を設定するとします。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="1d6a4-108">複数の経費報告書承認者を必要とする場合は、以下のいずれかの方法でワークフロー要素を追加できます:</span><span class="sxs-lookup"><span data-stu-id="1d6a4-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="1d6a4-109">1 つの承認段階を持つ、 1 つの承認要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-109">Add one approval element that has one step.</span></span> <span data-ttu-id="1d6a4-110">たとえば、このステップでは、経費報告書をユーザー グループに割り当て、ユーザー グループのメンバーの 50％ の承認を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="1d6a4-111">複数の承認段階を持つ 1 つの承認要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="1d6a4-112">たとえば、承認要素には次のステップがあります :</span><span class="sxs-lookup"><span data-stu-id="1d6a4-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="1d6a4-113">経費報告書を提出した従業員の上司が承認する。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="1d6a4-114">買掛金担当者が領収書と経費精算書を確認する。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="1d6a4-115">予算所有者が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="1d6a4-116">それぞれが 1 つの承認段階を持つ複数の承認要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="1d6a4-117">たとえば、次の手順ごとに個別の承認要素を追加することができます :</span><span class="sxs-lookup"><span data-stu-id="1d6a4-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="1d6a4-118">従業員の上司が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="1d6a4-119">予算所有者が経費報告書を承認する。</span><span class="sxs-lookup"><span data-stu-id="1d6a4-119">The budget owner approves the expense report.</span></span>
