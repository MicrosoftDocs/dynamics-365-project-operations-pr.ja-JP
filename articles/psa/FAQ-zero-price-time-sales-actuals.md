---
title: 時間売上実績で価格が既定でゼロになっている理由を教えてください。
description: 時間売上実績で価格が既定でゼロになっている理由のトラブルシューティング。
author: rumant
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
ms.openlocfilehash: e32b4c8113afdc18d9b220b1a8daf5007be93ac8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011647"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a><span data-ttu-id="99ca2-103">時間売上実績で価格が既定でゼロになっている理由を教えてください。</span><span class="sxs-lookup"><span data-stu-id="99ca2-103">Why is price defaulting to zero on time sales actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="99ca2-104">この FAQ は、トランザクション クラスが時間に設定されていて、トランザクションの種類が未請求売上になっている実績に適用されます。</span><span class="sxs-lookup"><span data-stu-id="99ca2-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="99ca2-105">次の 3 つのチェックでは、時間売上実績で価格 (請求レート) が既定で 0 になっている理由をトラブルシューティングできます。</span><span class="sxs-lookup"><span data-stu-id="99ca2-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on time sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a><span data-ttu-id="99ca2-106">チェック 1: プロジェクトの販売価格表を特定する</span><span class="sxs-lookup"><span data-stu-id="99ca2-106">Check 1: Identify the sales price list for the project</span></span>

<span data-ttu-id="99ca2-107">実績のプロジェクト フィールドからプロジェクトを検索し、プロジェクト ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="99ca2-108">次に、[営業] タブに移動し、[プロジェクト契約品目] グリッドで、[プロジェクト契約] フィールドのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="99ca2-108">Then go to the Sales tab and on Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="99ca2-109">[プロジェクト契約] ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="99ca2-109">The project Contract page will open.</span></span> <span data-ttu-id="99ca2-110">[プロジェクト契約] ページで、[プロジェクト価格表] タブに移動します。少なくとも 1 つの価格表が添付されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span> <span data-ttu-id="99ca2-111">プロジェクト契約の [プロジェクト価格表] グリッドに添付された価格表がない場合は、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="99ca2-111">If there is no price list attached in the Project Price Lists grid of the Project Contract you have isolated the problem.</span></span> <span data-ttu-id="99ca2-112">[プロジェクト価格表] グリッドに価格表を添付します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="99ca2-113">ここで添付できる価格表では、コンテキスト フィールドが [営業] が設定されていて、価格表の通貨フィールドがプロジェクト契約の金額フィールドに一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="99ca2-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="99ca2-114">必要な修正を加え終わったら、時間エントリを再作成して承認し、未請求営業実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-114">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 

<span data-ttu-id="99ca2-115">プロジェクト契約の [プロジェクト価格表] グリッドに 1 つ以上の価格表が貼付されている場合、ドキュメントの次のチェックに移動します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, proceed to the next check in the document.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a><span data-ttu-id="99ca2-116">チェック 2: 上記で特定した価格表のうち、時間売上実績の特定の日付で有効なものがあるか</span><span class="sxs-lookup"><span data-stu-id="99ca2-116">Check 2: Are any of the price lists identified above valid for the specific date of the time sales actual?</span></span>

<span data-ttu-id="99ca2-117">Project Service で既定の価格として価格表を考慮に入れる場合、価格表が時間売上実績の日付に適用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="99ca2-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time sales actual.</span></span> <span data-ttu-id="99ca2-118">上で識別した価格表が適用されるかどうかを確認するには、次の点をチェックします。</span><span class="sxs-lookup"><span data-stu-id="99ca2-118">Check the following to see if the price list(s) identified above are applicable:</span></span>
- <span data-ttu-id="99ca2-119">添付された価格表の全般タブの開始日と終了日が空でないかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="99ca2-119">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="99ca2-120">上で識別した価格表の開始日と終了日が空の場合、問題を分離しています。</span><span class="sxs-lookup"><span data-stu-id="99ca2-120">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="99ca2-121">時間売上実績で開始日フィールドを書き留め、特定されたいずれかの価格表がその日付に適用されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-121">Make a note of the start date field on your time sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="99ca2-122">たとえば、時間売上実績の日付は、価格表の開始日と終了日の間に収まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="99ca2-122">For example, the date of the time sales actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="99ca2-123">時間売上実績の日付をカバーする価格表がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="99ca2-123">If there is no price list that covers that date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="99ca2-124">価格表の開始日と終了日を変更し、価格表が時間売上実績の日付をカバーするようにします。</span><span class="sxs-lookup"><span data-stu-id="99ca2-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="99ca2-125">時間売上実績の日付をカバーする価格表が複数ある場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="99ca2-125">If there is more than one price list that covers the date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="99ca2-126">これは、時間売上実績の日付をカバーする価格表が 1 つだけになるように、価格表の開始日と終了日を編集することで修正できます。</span><span class="sxs-lookup"><span data-stu-id="99ca2-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="99ca2-127">時間売上実績の日付をカバーする価格表が 1 つだけの場合は、チェック 3 に移動します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-127">If there is only one price list that covers that date of the time sales actual, go to Check 3.</span></span>
<span data-ttu-id="99ca2-128">必要な修正を加え終わったら、時間エントリを再作成して承認し、時間売上実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-128">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a><span data-ttu-id="99ca2-129">チェック 3: 時間売上実績の価格ディメンションの価格表に価格はあるか</span><span class="sxs-lookup"><span data-stu-id="99ca2-129">Check 3: Is there a price in the price list for the pricing dimensions on the time sales actual?</span></span>

<span data-ttu-id="99ca2-130">チェック 1 とチェック 2 を正常に完了した場合、時間売上実績の日付に適用される価格表は 1 つだけになっているはずです。</span><span class="sxs-lookup"><span data-stu-id="99ca2-130">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time sales actual.</span></span> <span data-ttu-id="99ca2-131">この価格表を開いて [ロール価格] タブに移動します。時間売上実績で価格ディメンションのグリッドに行があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-131">Open this Price List and navigate to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the Time sales actual.</span></span>

<span data-ttu-id="99ca2-132">時間売上実績の価格ディメンションのロール価格グリッドに行がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="99ca2-132">If there is no row in the role price grid for the pricing dimensions on the time sales actual, then you have isolated the problem.</span></span> <span data-ttu-id="99ca2-133">時間売上実績の価格ディメンションのロール価格グリッドに行を作成します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-133">Create a row in the Role prices grid for the pricing dimensions on your time sales actual.</span></span> <span data-ttu-id="99ca2-134">これが終わったら、時間エントリを再作成して承認し、時間売上実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99ca2-134">Once this is done, recreate time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

<span data-ttu-id="99ca2-135">上の 3 つのチェックに従った後に時間売上実績に有効な価格がまだ表示されない場合、サポート チケットを登録してください。</span><span class="sxs-lookup"><span data-stu-id="99ca2-135">If you still don't see a valid price on your time sales actual after following the three checks above, please log a support ticket.</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]