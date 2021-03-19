---
title: 時間コスト実績で価格が既定でゼロになっている理由を教えてください。
description: 時間コスト実績で価格が既定でゼロになっている理由のトラブルシューティング。
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
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285804"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="fc18c-103">時間コスト実績で価格が既定でゼロになっている理由を教えてください。</span><span class="sxs-lookup"><span data-stu-id="fc18c-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fc18c-104">この FAQ は、トランザクション クラスが時間に設定されていて、トランザクションの種類がコストになっている実績に適用されます。</span><span class="sxs-lookup"><span data-stu-id="fc18c-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="fc18c-105">次の 3 つのチェックでは、時間コスト実績で価格が既定で 0 になっている理由をトラブルシューティングできます。</span><span class="sxs-lookup"><span data-stu-id="fc18c-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="fc18c-106">チェック 1: プロジェクトのコスト価格表を特定する</span><span class="sxs-lookup"><span data-stu-id="fc18c-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="fc18c-107">実績のプロジェクト フィールドからプロジェクトを検索し、プロジェクト ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="fc18c-108">フィールドで契約単位リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc18c-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="fc18c-109">[契約単位] ページで、契約単位の [原価価格表] グリッドに価格表があるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="fc18c-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="fc18c-110">複数の価格表がある場合は、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="fc18c-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="fc18c-111">Project Service は、組織単位につき 1 つの価格表のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc18c-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="fc18c-112">組織単位の [原価価格表] グリッドで添付されている価格表が 1 つになるまで、このエンティティからすべての価格表を削除します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="fc18c-113">組織単位に添付されている価格表がない場合、組織単位の通貨を書き留めます。</span><span class="sxs-lookup"><span data-stu-id="fc18c-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="fc18c-114">[Project Service]、[パラメーター] の順に移動し、[価格表] タブを開きます。コンテキストが [コスト] に設定され、組織単位の通貨と一致する通貨を持つ価格表がないかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="fc18c-115">その条件をに一致する価格表がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="fc18c-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="fc18c-116">コンテキストが [コスト] に設定され、組織単位の通貨に一致する通貨を持つ価格表が少なくとも 1 つあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="fc18c-117">その条件に一致する価格表が複数ある場合、このドキュメントを読み続けてさらにチェックを行います。</span><span class="sxs-lookup"><span data-stu-id="fc18c-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="fc18c-118">チェック 2: 上記で特定した価格表のうち、時間コスト実績の特定の日付で有効なものがあるか</span><span class="sxs-lookup"><span data-stu-id="fc18c-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="fc18c-119">Project Service で既定の価格として価格表を考慮に入れる場合、価格表が時間コスト実績の日付に適用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc18c-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="fc18c-120">上で識別した価格表が適用されるかどうかを確認するには、次の点をチェックします。</span><span class="sxs-lookup"><span data-stu-id="fc18c-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="fc18c-121">添付された価格表の全般タブの開始日と終了日が空でないかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="fc18c-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="fc18c-122">上で識別した価格表の開始日と終了日が空の場合、問題を分離しています。</span><span class="sxs-lookup"><span data-stu-id="fc18c-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="fc18c-123">時間コスト実績で開始日フィールドを書き留め、特定されたいずれかの価格表がその日付に適用されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="fc18c-124">たとえば、時間コスト実績の日付は、価格表の開始日と終了日の間に収まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc18c-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="fc18c-125">時間コスト実績の日付をカバーする価格表がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="fc18c-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="fc18c-126">価格表の開始日と終了日を変更し、価格表が時間コスト実績の日付をカバーするようにします。</span><span class="sxs-lookup"><span data-stu-id="fc18c-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="fc18c-127">時間コスト実績の日付をカバーする価格表が複数ある場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="fc18c-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="fc18c-128">これは、時間コスト実績の日付をカバーする価格表が 1 つだけになるように、価格表の開始日と終了日を編集することで修正できます。</span><span class="sxs-lookup"><span data-stu-id="fc18c-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="fc18c-129">時間コスト実績の日付をカバーする価格表が 1 つだけの場合、ドキュメントの次のチェックに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="fc18c-130">必要な修正を加え終わったら、時間エントリを再作成して承認し、時間コスト実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="fc18c-131">チェック 3: 時間コスト実績の価格ディメンションの価格表に価格はあるか</span><span class="sxs-lookup"><span data-stu-id="fc18c-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="fc18c-132">チェック 1 とチェック 2 を正常に完了した場合、時間コスト実績の日付に適用される価格表は 1 つだけになっているはずです。</span><span class="sxs-lookup"><span data-stu-id="fc18c-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="fc18c-133">この価格表を開いて [ロール価格] タブに移動します。時間コスト実績で価格ディメンションのグリッドに行があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="fc18c-134">時間コスト実績の価格ディメンションのロール価格グリッドに行がない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="fc18c-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="fc18c-135">時間コスト実績の価格ディメンションのロール価格グリッドに行を作成します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="fc18c-136">これが終わったら、時間エントリを再作成して承認し、時間コスト実績に有効な価格が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc18c-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="fc18c-137">上の 3 つのチェックが終わった後に時間コスト実績に有効な価格がまだ表示されない場合、サポート チケットを登録してください。</span><span class="sxs-lookup"><span data-stu-id="fc18c-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]