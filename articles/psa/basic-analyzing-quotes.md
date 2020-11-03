---
title: プロジェクトの見積もりの分析
description: このトピックでは、プロジェクトの見積もりの分析に関する情報を提供します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079384"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="f2974-103">プロジェクトの見積もりの分析</span><span class="sxs-lookup"><span data-stu-id="f2974-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f2974-104">Dynamics 365 Project Service Automation はプロジェクトの見積もりを分析して、収益性を予測します。</span><span class="sxs-lookup"><span data-stu-id="f2974-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="f2974-105">また、納期、完了日、予算に関する顧客の要求に、見積りがどの程度合致しているか分析します。</span><span class="sxs-lookup"><span data-stu-id="f2974-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="f2974-106">利益性分析</span><span class="sxs-lookup"><span data-stu-id="f2974-106">Profitability analysis</span></span>

<span data-ttu-id="f2974-107">Project Service Automation は、粗利と調整後の粗利を使用して収益性を分析します。</span><span class="sxs-lookup"><span data-stu-id="f2974-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="f2974-108">粗利は次の式を使用して計算します。</span><span class="sxs-lookup"><span data-stu-id="f2974-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="f2974-109">調整後の粗利は次の式を使用して計算します。</span><span class="sxs-lookup"><span data-stu-id="f2974-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="f2974-110">粗利と調整後の粗利の値が大幅に異なる場合、見積もり中の作業の多くは非請求に分類されます。</span><span class="sxs-lookup"><span data-stu-id="f2974-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="f2974-111">顧客の要求の分析</span><span class="sxs-lookup"><span data-stu-id="f2974-111">Analysis of customer expectations</span></span>

<span data-ttu-id="f2974-112">次のフィールドに値を入力すると、見積もりを分析してスケジュールと予算に関する顧客の要求に関するチャートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="f2974-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="f2974-113">見積もりヘッダーの **配送指定日** フィールド。</span><span class="sxs-lookup"><span data-stu-id="f2974-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="f2974-114">(プロジェクト ベースの行と製品ベースの行に対する) 各見積もり行の **顧客予算** フィールド。</span><span class="sxs-lookup"><span data-stu-id="f2974-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="f2974-115">スケジュールに関する顧客要求の分析は、見積もりラインの詳細の最新の終了日を、見積もり内のすべての見積もりラインにわたって要求された納期と比較することで行われます。</span><span class="sxs-lookup"><span data-stu-id="f2974-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="f2974-116">予算に関する顧客要求の分析は、顧客の総予算の合計をすべての見積もり行の見積もり金額と比較することで行われます。</span><span class="sxs-lookup"><span data-stu-id="f2974-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
