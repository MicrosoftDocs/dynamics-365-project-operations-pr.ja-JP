---
title: 経費売上実績で価格が既定でゼロになっている理由を教えてください。
description: 次の 3 つのチェックでは、経費売上実績で価格が既定で 0 になっている理由をトラブルシューティングできます。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 8c2270b07b6f8765a6ec1f506fe1767a1841950b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122079"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a><span data-ttu-id="dee36-103">経費売上実績で価格が既定でゼロになっている理由を教えてください。</span><span class="sxs-lookup"><span data-stu-id="dee36-103">Why is the price defaulting to zero on expense sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dee36-104">この FAQ は、トランザクション クラスが経費に設定されていて、トランザクションの種類が未請求売上になっている経費実績に適用されます。</span><span class="sxs-lookup"><span data-stu-id="dee36-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="dee36-105">次の 3 つのチェックでは、経費売上実績で価格 (請求レート) が既定で 0 になっている理由をトラブルシューティングできます。</span><span class="sxs-lookup"><span data-stu-id="dee36-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on expense sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-project"></a><span data-ttu-id="dee36-106">チェック 1: プロジェクトの販売価格表を特定する</span><span class="sxs-lookup"><span data-stu-id="dee36-106">Check 1: Identify the sales price list for project</span></span>

<span data-ttu-id="dee36-107">実績のプロジェクト フィールドからプロジェクトを検索し、プロジェクト ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="dee36-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="dee36-108">次に、[営業] タブに移動します。[プロジェクト契約品目] グリッドで、[プロジェクト契約] フィールドのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee36-108">Then go to the Sales tab. On the Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="dee36-109">[プロジェクト契約] ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="dee36-109">The Project Contract page will open.</span></span> <span data-ttu-id="dee36-110">[プロジェクト契約] ページで、[プロジェクト価格表] タブに移動します。少なくとも 1 つの価格表が添付されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span>

<span data-ttu-id="dee36-111">プロジェクト契約の [プロジェクト価格表] グリッドに添付された価格表がない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dee36-111">If there is no price list attached in the Project Price Lists grid of the Project Contract do the following:</span></span>

- <span data-ttu-id="dee36-112">[プロジェクト価格表] グリッドに価格表を添付します。</span><span class="sxs-lookup"><span data-stu-id="dee36-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="dee36-113">ここで添付できる価格表では、コンテキスト フィールドが [営業] が設定されていて、価格表の通貨フィールドがプロジェクト契約の金額フィールドに一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="dee36-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="dee36-114">必要な修正を加えたら、経費エントリを再作成して承認し、未請求営業実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-114">Once you’ve made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>
- <span data-ttu-id="dee36-115">プロジェクト契約の [プロジェクト価格表] グリッドに 1 つ以上の価格表が貼付されている場合、チェック 2 に移動します。</span><span class="sxs-lookup"><span data-stu-id="dee36-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, go to Check 2.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a><span data-ttu-id="dee36-116">チェック 2: 上記で特定した価格表のうち、経費実績の特定の日付で有効なものがあるか</span><span class="sxs-lookup"><span data-stu-id="dee36-116">Check 2: Are any of the price lists identified above valid for the specific date of the expense actual?</span></span>

<span data-ttu-id="dee36-117">Project Service で既定の価格として価格表を考慮に入れる場合、価格表が経費売上実績の日付に適用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="dee36-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the expense sales actual.</span></span> <span data-ttu-id="dee36-118">上で識別した価格表が適用されるかどうかを確認するには、次の点をチェックします。</span><span class="sxs-lookup"><span data-stu-id="dee36-118">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="dee36-119">まず、添付された価格表の全般タブの開始日と終了日が空でないかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="dee36-119">Start by checking if start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="dee36-120">上で識別した価格表の開始日と終了日が空の場合、問題を分離しています。</span><span class="sxs-lookup"><span data-stu-id="dee36-120">If the start and end dates on the price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="dee36-121">経費売上実績で開始日フィールドを書き留め、特定されたいずれかの価格表がその日付に適用されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-121">Make a note of the start date field on your expense sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="dee36-122">たとえば、経費実績の日付は、価格表の開始日と終了日の間に収まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dee36-122">For example, the date of the expense actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="dee36-123">経費売上実績の日付をカバーする価格表がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="dee36-123">If there is no price list that covers that date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="dee36-124">価格表の開始日と終了日を変更し、価格表が経費実績の日付をカバーするようにします。</span><span class="sxs-lookup"><span data-stu-id="dee36-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="dee36-125">経費売上実績の日付をカバーする価格表が複数ある場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="dee36-125">If there is more than one price list that covers the date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="dee36-126">これは、経費実績の日付をカバーする価格表が 1 つだけになるように、価格表の開始日と終了日を編集することで修正できます。</span><span class="sxs-lookup"><span data-stu-id="dee36-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="dee36-127">経費実績の日付をカバーする価格表が 1 つだけの場合は、チェック 3 に移動します。</span><span class="sxs-lookup"><span data-stu-id="dee36-127">If there is only one price list that covers that date of the expense actual, move to Check 3.</span></span>
<span data-ttu-id="dee36-128">必要な修正を加え終わったら、経費エントリを再作成して承認し、未請求営業実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-128">Once you’ve done made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a><span data-ttu-id="dee36-129">チェック 3: 適用されるプロジェクト価格表の経費カテゴリには有効な価格があるか</span><span class="sxs-lookup"><span data-stu-id="dee36-129">Check 3: Is there a valid price for the expense category in the applicable project price list?</span></span> 

<span data-ttu-id="dee36-130">チェック 1 とチェック 2 を正常に完了した場合、経費売上実績の日付に適用されるプロジェクト価格表は 1 つだけになっているはずです。</span><span class="sxs-lookup"><span data-stu-id="dee36-130">If you have successfully completed Check 1 and Check 2, you should now have only one project price list that is applicable for the date of the expense sales actual.</span></span> <span data-ttu-id="dee36-131">このプロジェクト価格表を開いて [価格カテゴリ] タブに移動します。経費実績で特定の経費カテゴリのグリッドに行があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-131">Open this Project Price List and go to the Category Prices tab. Make sure that there is a row in the grid for the specific expense category on the Expense actual.</span></span>
 
- <span data-ttu-id="dee36-132">行がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="dee36-132">If there is no row, then you have isolated the problem.</span></span> <span data-ttu-id="dee36-133">経費実績のカテゴリのカテゴリ価格グリッドに行を作成します。</span><span class="sxs-lookup"><span data-stu-id="dee36-133">Create a row in the Category price grid for the category on your expense actual.</span></span> <span data-ttu-id="dee36-134">これが終わったら、経費エントリを再作成して承認し、未請求営業実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-134">Once this is done, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 
- <span data-ttu-id="dee36-135">カテゴリ価格グリッド内に経費カテゴリの行がある場合、有効な価格があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-135">If there is a row for the expense category in the category prices grid, check if it has a valid price.</span></span>

<span data-ttu-id="dee36-136">有効な価格について理解するには、次の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="dee36-136">To understand what a valid price is, use these methods:</span></span>

- <span data-ttu-id="dee36-137">カテゴリ価格行の価格設定方法フィールドが [コスト] に設定されている場合、経費売上実績の単位価格の既定値は経費エントリの値になります。</span><span class="sxs-lookup"><span data-stu-id="dee36-137">If the Pricing Method field on the Category price line is set to At Cost, then the unit rate on your Expense sales actual will be defaulted to the value in the Expense entry.</span></span>
- <span data-ttu-id="dee36-138">カテゴリ価格行の価格設定方法フィールドが [利幅率] に設定されている場合、[パーセント] フィールドが有効な値に設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-138">If the Pricing Method field on the Category price line is set to Markup Percentage, then check if the Percent field is set to a valid value.</span></span> <span data-ttu-id="dee36-139">経費売上実績の単位価格は、この利幅率を経費エントリの価格に適用することにより既定が設定されます。</span><span class="sxs-lookup"><span data-stu-id="dee36-139">The unit rate on your Expense sales actual is defaulted by applying this markup percent to the price in the Expense entry.</span></span>
- <span data-ttu-id="dee36-140">カテゴリ価格行の価格設定方法フィールドが [出荷単位ごとの価格] に設定されている場合、[価格] フィールドが有効な値に設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-140">If the Pricing Method field on the Category price line is set to Price per Unit, then check if the Price field is set to a valid value.</span></span> <span data-ttu-id="dee36-141">経費売上実績の単位価格の既定値は、価格フィールドで指定された固定金額に設定されます。</span><span class="sxs-lookup"><span data-stu-id="dee36-141">The unit rate on your Expense sales actual will be defaulted to the currency amount specified in the Price field.</span></span>

<span data-ttu-id="dee36-142">経費カテゴリの価格設定が有効でない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="dee36-142">If the price setup for the expense category isn't valid, then you have isolated the problem.</span></span> <span data-ttu-id="dee36-143">解決策は、上記のルールに従って経費カテゴリの有効な価格を持つカテゴリ価格行を編集することです。</span><span class="sxs-lookup"><span data-stu-id="dee36-143">The solution is to edit the category price line with a valid price for the expense category in accordance with the rules above.</span></span> <span data-ttu-id="dee36-144">それが終わったら、経費エントリを再作成して承認し、未請求営業実績に有効な価格があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee36-144">Once you’ve done that, recreate an expense entry, approve it, and then check that the unbilled sales actual gets a valid price.</span></span>

<span data-ttu-id="dee36-145">上の 3 つのチェックが終わった後に経費売上実績に有効な価格がまだ表示されない場合、サポート チケットを登録してください。</span><span class="sxs-lookup"><span data-stu-id="dee36-145">If you still don't see a valid price on your expense sales actual after doing the three checks above, please log a support ticket.</span></span>


