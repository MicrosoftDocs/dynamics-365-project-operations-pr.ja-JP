---
title: 経費報告書の個人的な経費
description: このトピックでは、Microsoft Dynamics 365 Finance で従業者の個人的な経費を処理するための 2 つの方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf6bfc714751fa64914e684f67d37552b2df162e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271404"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="7cffd-103">経費報告書の個人的な経費</span><span class="sxs-lookup"><span data-stu-id="7cffd-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="7cffd-104">出張中に、従業者が会社のクレジットカードに個人的な経費を付けることがあります。</span><span class="sxs-lookup"><span data-stu-id="7cffd-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="7cffd-105">個人的な経費の処理プロセスを定義しないと、従業者が項目別経費報告書を提出したときに、経費報告書の承認プロセスが中断される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7cffd-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="7cffd-106">従業者の個人的な経費を処理する方法には 2 つあります:</span><span class="sxs-lookup"><span data-stu-id="7cffd-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="7cffd-107">**従業員による支払い** – 組織は、会社のクレジット カードの請求書に記載されている個人的な経費を支払いません。</span><span class="sxs-lookup"><span data-stu-id="7cffd-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="7cffd-108">代わりに、会社のクレジットカードに請求された個人的な経費を会社の経費と一緒に表示するレポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cffd-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="7cffd-109">**会社による支払い** – 組織は、会社のクレジットカードの全額を支払い、その後、個人的な経費を従業者の口座から引き落とします。</span><span class="sxs-lookup"><span data-stu-id="7cffd-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="7cffd-110">**経費管理パラメーター** ページで、組織が使用する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="7cffd-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]