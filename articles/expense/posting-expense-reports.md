---
title: 経費精算書の転記
description: このトピックでは、経費精算書を転記する方法について説明します。
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
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
ms.openlocfilehash: 866252c1961f359cecdb729ca909d96bcb03b1f4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079232"
---
# <a name="post-expense-reports"></a><span data-ttu-id="7f804-103">経費精算書の転記</span><span class="sxs-lookup"><span data-stu-id="7f804-103">Post expense reports</span></span>

<span data-ttu-id="7f804-104">経費精算書は、承認されて一般仕訳帳に転送された後、転記することができます。</span><span class="sxs-lookup"><span data-stu-id="7f804-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="7f804-105">経費清算書を転記すると、付加価値税 (VAT) の還付に適用できる経費が特定されます。</span><span class="sxs-lookup"><span data-stu-id="7f804-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="7f804-106">VAT の支払いの確認および還付のタスクは、経費清算書の確認を担当する従業員に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="7f804-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="7f804-107">経費報告書の経費が従業員の採用会社以外の会社に請求される場合は、経費の支払先会社と経費の支払元会社を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f804-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="7f804-108">たとえば、経費清算書を送信した従業員は DAT 社に勤務しているが、DIR 社への経費を請求されたとします。</span><span class="sxs-lookup"><span data-stu-id="7f804-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="7f804-109">この場合、DAT は経費の支払先会社、DIR は経費の支払元会社です。</span><span class="sxs-lookup"><span data-stu-id="7f804-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="7f804-110">これらの仕訳帳明細行を確認した後は、経費明細行を一般会計に転記できます。</span><span class="sxs-lookup"><span data-stu-id="7f804-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="7f804-111">経費清算書を転記するには、 **承認された経費清算書** ページで経費清算書を選択し、アクション ウィンドウで **転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f804-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="7f804-112">同時にリストですべての経費清算書を転記することもできます。</span><span class="sxs-lookup"><span data-stu-id="7f804-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="7f804-113">すべての経費清算書を選択し、 **転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f804-113">Select all the expense reports, and then select **Post**.</span></span>
