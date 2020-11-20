---
title: 請求書の修正
description: このトピックでは、請求書の修正に関する情報を提供します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122394"
---
# <a name="corrected-invoices"></a><span data-ttu-id="ebb02-103">請求書の修正</span><span class="sxs-lookup"><span data-stu-id="ebb02-103">Corrected invoices</span></span>

<span data-ttu-id="ebb02-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ebb02-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ebb02-105">確認済みの請求書は編集可能です。</span><span class="sxs-lookup"><span data-stu-id="ebb02-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="ebb02-106">確認済みの請求書を編集すると、修正請求書のドラフトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="ebb02-107">元の請求書のすべてのトランザクションと数量を取り消すことを前提としているため、この修正請求書には元の請求書のすべてのトランザクションが含まれ、その数量はすべて 0 (ゼロ) となります。</span><span class="sxs-lookup"><span data-stu-id="ebb02-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="ebb02-108">トランザクションが修正を必要とない場合は、その修正請求書をドラフトから削除できます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="ebb02-109">部分的に数量を取り消す、または元に戻す場合は、明細行の詳細の数量フィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="ebb02-110">請求明細行の詳細を開くと、元の請求書の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="ebb02-111">その後、現在の請求書の数量を編集して、元の請求書の数量よりも少なく、または多くすることができます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="ebb02-112">修正請求書を確認すると、元の請求済み売上実績が取り消され、新規の請求済み売上実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="ebb02-113">数量が削減された場合、差異により未請求売上実績も作成されます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="ebb02-114">例えば、元の請求済み売上が 8 時間分であり、修正された請求明細行の詳細の数量が 6 時間に減少した場合、元の請求売上明細行を戻し、新たに 2 つの実績が作成されます :</span><span class="sxs-lookup"><span data-stu-id="ebb02-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="ebb02-115">6 時間の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="ebb02-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="ebb02-116">残り 2 時間の未請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="ebb02-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="ebb02-117">このトランザクションは、顧客との交渉に応じて後で請求するか、または、請求不可としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="ebb02-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
