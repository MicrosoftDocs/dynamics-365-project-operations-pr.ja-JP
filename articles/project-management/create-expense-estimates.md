---
title: 経費の見積もり
description: このトピックでは、プロジェクトベースの経費の定義または見積もりについて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908296"
---
# <a name="expense-estimates"></a><span data-ttu-id="44610-103">経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="44610-103">Expense estimates</span></span>
<span data-ttu-id="44610-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="44610-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44610-105">Dynamics 365 Project Operations を使用すると、リソースベースの見積もりを定義すると共に、プロジェクト マネージャーは各プロジェクトのプロジェクトベースの経費を定義できます。</span><span class="sxs-lookup"><span data-stu-id="44610-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="44610-106">各経費項目は、特定のプロジェクト タスクまたは経費カテゴリに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="44610-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="44610-107">経費カテゴリは通常、組織レベルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="44610-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="44610-108">各経費カテゴリの価格設定は通常、次の階層で定義されます:</span><span class="sxs-lookup"><span data-stu-id="44610-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="44610-109">組織全体</span><span class="sxs-lookup"><span data-stu-id="44610-109">Organization</span></span>
- <span data-ttu-id="44610-110">顧客</span><span class="sxs-lookup"><span data-stu-id="44610-110">Customer</span></span>
- <span data-ttu-id="44610-111">見積もり/契約</span><span class="sxs-lookup"><span data-stu-id="44610-111">Quote/contract</span></span>

<span data-ttu-id="44610-112">プロジェクト経費を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="44610-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="44610-113">**プロジェクト**に移動し、作業するプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="44610-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="44610-114">**プロジェクトの見積もり**タブを選択して、プロジェクト経費のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="44610-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="44610-115">**新規経費**を選択して、経費を追加します。</span><span class="sxs-lookup"><span data-stu-id="44610-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="44610-116">または、削除する経費を選択してから、**経費の削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="44610-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="44610-117">次の属性は、経費明細行品目ごとに定義されています:</span><span class="sxs-lookup"><span data-stu-id="44610-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="44610-118">**カテゴリ**: プロジェクトで発生するすべての経費を説明するために使用される一般的なグループ化。</span><span class="sxs-lookup"><span data-stu-id="44610-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="44610-119">**開始日**: 経費が発生すると予測される日付。</span><span class="sxs-lookup"><span data-stu-id="44610-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="44610-120">**数量**: 特定のカテゴリの経費項目の予測値。</span><span class="sxs-lookup"><span data-stu-id="44610-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="44610-121">**単位原価価格**: 経費のコストの計算に使用される単価。</span><span class="sxs-lookup"><span data-stu-id="44610-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="44610-122">**単位販売価格**: 経費の販売価格の計算に使用される単価。</span><span class="sxs-lookup"><span data-stu-id="44610-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

