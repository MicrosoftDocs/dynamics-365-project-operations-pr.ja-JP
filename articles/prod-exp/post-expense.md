---
title: 経費精算書を転記する
description: このトピックでは、総勘定元帳に経費精算書を転記する方法について説明します。
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24dd945ea7ea73b37806e209a90d5301ac09d956
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005797"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="3caaf-103">経費精算書を転記する</span><span class="sxs-lookup"><span data-stu-id="3caaf-103">Post an expense report</span></span>

<span data-ttu-id="3caaf-104">経費精算書は、承認されて一般仕訳帳に転送された後、総勘定元帳に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="3caaf-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="3caaf-105">経費清算書を転記すると、付加価値税 (VAT) の還付に適用できる経費が特定されます。</span><span class="sxs-lookup"><span data-stu-id="3caaf-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="3caaf-106">VAT の支払いの確認および還付のタスクは、経費清算書の確認を担当する従業員に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3caaf-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="3caaf-107">経費精算書の経費が従業員を雇用している会社以外の会社に請求される場合は、経費の支払先会社と経費の支払元会社を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3caaf-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="3caaf-108">たとえば、経費清算書を送信した従業員は DAT 社に勤務しているが、DIR 社への経費を請求されたとします。</span><span class="sxs-lookup"><span data-stu-id="3caaf-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="3caaf-109">この場合、DAT は経費の支払先会社、DIR は経費の支払元会社です。</span><span class="sxs-lookup"><span data-stu-id="3caaf-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="3caaf-110">これらの仕訳帳明細行を確認した後は、経費明細行を一般会計に転記できます。</span><span class="sxs-lookup"><span data-stu-id="3caaf-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="3caaf-111">経費清算書を転記するには、**承認された経費清算書** ページで経費清算書を選択し、アクション ウィンドウで **転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3caaf-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="3caaf-112">同時にリストですべての経費清算書を転記することもできます。</span><span class="sxs-lookup"><span data-stu-id="3caaf-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="3caaf-113">すべての経費清算書を選択し、**転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3caaf-113">Select all the expense reports, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]