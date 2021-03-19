---
title: 日当
description: このトピックでは、経費管理で使用される日当ルールについて説明します。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276309"
---
# <a name="per-diems"></a><span data-ttu-id="6f25c-103">日当</span><span class="sxs-lookup"><span data-stu-id="6f25c-103">Per diems</span></span>

<span data-ttu-id="6f25c-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6f25c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="6f25c-105">日当は、出張した作業者に支給される手当です。</span><span class="sxs-lookup"><span data-stu-id="6f25c-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="6f25c-106">経費管理で、さまざまな出張の状況に適合する日当ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="6f25c-107">日当レートは、時期、出張先、または両方を基準にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="6f25c-108">日当ルールを作成する際に、作業者が無料の食事やサービスを受ける場合、日当レートから天引される割合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="6f25c-109">作業者の出張に適用できる日当レートの最小時間数と最大時間数を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="6f25c-110">構成</span><span class="sxs-lookup"><span data-stu-id="6f25c-110">Configuration</span></span> 

1. <span data-ttu-id="6f25c-111">日当の場所を追加するには、**設定** > **計算とコード** > **日当の場所** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f25c-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="6f25c-112">上記で追加した場所ごとに、ホテル、食事、その他の経費の特定の開始日と終了日の間に有効な日当レートと通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f25c-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="6f25c-113">日当レートと通貨は、**設定** > **計算とコード** > **日当** で構成されます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="6f25c-114">**日当の場所** ページで、日当レート層を構成します。</span><span class="sxs-lookup"><span data-stu-id="6f25c-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="6f25c-115">日当レート層を使用すると、ホテル、食事、およびその他の経費の 1 日あたりの手当の割合を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="6f25c-116">朝食、昼食、または夕食の食事の割合の削減を指定するには、**日当** タブの **経費管理パラメーター** ページのフィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="6f25c-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="6f25c-117">日当を使用して経費を提出する</span><span class="sxs-lookup"><span data-stu-id="6f25c-117">Submit expenses using per diem</span></span>
<span data-ttu-id="6f25c-118">日当を利用して経費を提出するには、経費レポートを作成するときの **日当** 経費カテゴリを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f25c-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="6f25c-119">**日当開始日**、**日当終了日**、そして **日当の場所** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f25c-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="6f25c-120">金額は、選択した場所の日当レートに基づいて計算され、食事の削減は、日当レート層に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="6f25c-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]