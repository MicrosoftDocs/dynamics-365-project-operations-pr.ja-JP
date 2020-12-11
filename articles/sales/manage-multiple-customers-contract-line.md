---
title: プロジェクトベースの契約品目の複数の顧客を管理する
description: このトピックは、複数の顧客を含む契約品目および契約で作業する方法について説明します。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 71081775ab45167bc1bff1979f7856a2a2a91385
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181908"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a><span data-ttu-id="6a0dd-103">プロジェクトベースの契約品目の複数の顧客を管理する</span><span class="sxs-lookup"><span data-stu-id="6a0dd-103">Manage multiple customers on project-based contract lines</span></span>

<span data-ttu-id="6a0dd-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="6a0dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a0dd-105">プロジェクトベースの契約品目には、支払いを担当する顧客のリストを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-105">Project-based contract lines can include a list of customers that are responsible for payment.</span></span> <span data-ttu-id="6a0dd-106">プロジェクトベースの契約品目のこの顧客リストは、契約の顧客リストと同一にすることができますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-106">This list of customers on the project-based contract line can be same as the list of customers on the contract but that isn't required.</span></span> <span data-ttu-id="6a0dd-107">プロジェクトの見積が成立し、プロジェクトの契約が作成されると、見積明細の顧客リストが対応する契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-107">When a project quote is won, and a project contract is created, the customer list on the quote line is copied to the corresponding contract line.</span></span> <span data-ttu-id="6a0dd-108">見積もりの顧客は契約にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-108">Customers on the quote are copied to the contract.</span></span>

<span data-ttu-id="6a0dd-109">プロジェクト契約が請求されると、プロジェクト ベースの契約品目の顧客リストが契約の顧客リストよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-109">When the project contract is invoiced, the customer list on project-based contract line takes priority over the customer list on the contract.</span></span> <span data-ttu-id="6a0dd-110">プロジェクト契約の顧客リストは、既定の新しい契約品目にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-110">The customer list on the project contract is only used to default new contract lines.</span></span>

<span data-ttu-id="6a0dd-111">プロジェクト契約の **顧客** タブにあるすべての契約顧客は、プロジェクト契約のために作成された新規契約品目の顧客として既定で契約品目の顧客として表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-111">All contract customers on the **Customers** tab of the project contract default as contract line customers on any new contract lines created for the project contract.</span></span> <span data-ttu-id="6a0dd-112">既存の契約品目は、この後に作成された新しい契約顧客レコードを継承しません。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-112">Any existing contract lines will not inherit the new contract customer records created after them.</span></span>

## <a name="create-update-or-delete-a-contract-line-customer-record"></a><span data-ttu-id="6a0dd-113">契約品目の顧客レコードを作成、更新、または削除する</span><span class="sxs-lookup"><span data-stu-id="6a0dd-113">Create, update, or delete a contract line customer record</span></span>

<span data-ttu-id="6a0dd-114">**プロジェクトベースの契約品目** ページの **契約品目の顧客** タブから、契約ラインの顧客を作成、更新、または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-114">You can create, update, or delete a contract line customer from the **Contract Line Customers** tab on the **Project-based Contract Line** page.</span></span> <span data-ttu-id="6a0dd-115">プロジェクトベースの契約品目に新しい顧客が追加されると、既定の請求分割率がゼロ パーセントの契約顧客として契約全体にも追加されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-115">When a new customer is added on the project-based contract line, they are also added on the overall contract as a contract customer with a default billing split percentage of zero percent.</span></span> <span data-ttu-id="6a0dd-116">契約全体の請求分割率は、新しい契約品目と最終的なプロジェクト契約にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-116">The billing split percentage on the overall contract is copied to new contract lines and to the eventual project contract.</span></span> <span data-ttu-id="6a0dd-117">ただし、契約から請求する場合、使用されるのは契約品目レベルでの請求分割率であり、全体的な契約レベルでの請求分割率ではありません。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-117">However, when invoicing from the contract, it's the billing split percentage at the contract line level that is used and not the billing split percentage at the overall contract level.</span></span> 

<span data-ttu-id="6a0dd-118">以下のフィールドは、プロジェクトベースの契約品目の顧客記録に記載されている項目のうち、作業をする上で覚えておく必要があります :</span><span class="sxs-lookup"><span data-stu-id="6a0dd-118">Below are the fields on the Contract line customer record of a project-based Contract line to keep in mind as you are working with it:</span></span>

| <span data-ttu-id="6a0dd-119">フィールド</span><span class="sxs-lookup"><span data-stu-id="6a0dd-119">Field</span></span> | <span data-ttu-id="6a0dd-120">場所</span><span class="sxs-lookup"><span data-stu-id="6a0dd-120">Location</span></span> | <span data-ttu-id="6a0dd-121">内容</span><span class="sxs-lookup"><span data-stu-id="6a0dd-121">Description</span></span> | <span data-ttu-id="6a0dd-122">下位への影響</span><span class="sxs-lookup"><span data-stu-id="6a0dd-122">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="6a0dd-123">勘定科目</span><span class="sxs-lookup"><span data-stu-id="6a0dd-123">Account</span></span> | <span data-ttu-id="6a0dd-124">**契約品目の顧客** タブの編集可能なグリッドと、契約品目の顧客に向けたメインフォームと簡易作成フォーム</span><span class="sxs-lookup"><span data-stu-id="6a0dd-124">Editable grid on **Contract Line Customers** tab and Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="6a0dd-125">すべてのアクティブな取引先企業。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-125">All active accounts.</span></span> <span data-ttu-id="6a0dd-126">このフィールドは、レコードが作成された後にロックされています。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-126">This field is locked after the record is created.</span></span> <span data-ttu-id="6a0dd-127">フィールドを更新するには、レコードを削除して、新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-127">To update the field, delete the record, and create a new record.</span></span> <span data-ttu-id="6a0dd-128">実績を記録している場合は、実績を含む記録を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-128">If you have recorded any actuals, you can't delete the record.</span></span> <span data-ttu-id="6a0dd-129">ただし、その取引先企業では課金分割率をゼロとしてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-129">However, you can mark the billing split percentage as zero for that account.</span></span> <span data-ttu-id="6a0dd-130">レコードがゼロとマークされている場合、この顧客に帰属または分割されている将来のコストと収益の実績がすべて影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-130">When the record is marked as zero, any future cost and revenue actuals that are attributed or split to this customer are impacted.</span></span> | <span data-ttu-id="6a0dd-131">追加、保存する取引先企業のマスターリストから取引先企業を選んで保存すると、契約品目の顧客も契約顧客として追加されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-131">When you pick an account from the master list of accounts to add and save them, the contract line customer is also added as a contract customer.</span></span> <span data-ttu-id="6a0dd-132">請求書が生成される際には、契約品目の顧客が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-132">Contract line customers are used when invoices are generated.</span></span> |
| <span data-ttu-id="6a0dd-133">請求分割率</span><span class="sxs-lookup"><span data-stu-id="6a0dd-133">Billing split percent</span></span> | <span data-ttu-id="6a0dd-134">**契約品目の顧客** タブの編集可能なグリッドと、契約品目の顧客に向けたメインフォームと簡易作成フォーム</span><span class="sxs-lookup"><span data-stu-id="6a0dd-134">Editable grid on **Contract Line Customers** tab and the Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="6a0dd-135">このフィールドは、この契約品目の顧客に帰属する各未請求の販売トランザクションの割合を表します。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-135">This field represents the percentage of each unbilled sales transaction that will be attributed to this contract line customer.</span></span> | <span data-ttu-id="6a0dd-136">契約品目の顧客と請求分割率は、承認後に実績が作成される際、および請求書が生成される際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-136">Contract line customers and billing split percentages are used when actuals are created after approval and when the invoice is generated.</span></span> |
| <span data-ttu-id="6a0dd-137">上限</span><span class="sxs-lookup"><span data-stu-id="6a0dd-137">Not-to-exceed limit</span></span> | <span data-ttu-id="6a0dd-138">**契約品目の顧客** タブの編集可能なグリッドと、契約品目の顧客に向けたメインフォームと簡易作成フォーム</span><span class="sxs-lookup"><span data-stu-id="6a0dd-138">Editable grid on **Contract Line Customers** tab and Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="6a0dd-139">契約品目についてこの顧客に請求される合計金額に交渉による制限または上限があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-139">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for the contract line.</span></span> | <span data-ttu-id="6a0dd-140">契約品目の顧客の超過しない限度額は、実績を作成して請求書を作成する際に使用します。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-140">The not-to-exceed limit for the contract line customer is used when actuals are created and the invoices are generated.</span></span> |
| <span data-ttu-id="6a0dd-141">所有会社</span><span class="sxs-lookup"><span data-stu-id="6a0dd-141">Owning Company</span></span> | <span data-ttu-id="6a0dd-142">**見積もり品目の顧客** タブの編集可能なグリッドと、見積もり品目の顧客に向けたメインフォームと簡易作成フォーム</span><span class="sxs-lookup"><span data-stu-id="6a0dd-142">Editable grid on the **Quote Line Customers** tab and the Main and Quick Create forms for a quote line customer</span></span> | <span data-ttu-id="6a0dd-143">この顧客が設立された法人です。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-143">The legal entity that this customer is set up in.</span></span> <span data-ttu-id="6a0dd-144">このフィールドは読み取り専用であり、見積もりの所有会社に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-144">This field is read-only and is set to the owning company of the quote.</span></span> <span data-ttu-id="6a0dd-145">**取引先企業** フィールドに追加する顧客のリストは、この所有企業からすでにフィルタリングされてリスト化されています。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-145">The list of customers to add in the **Account** field is already filtered to the list from this owning company.</span></span> | <span data-ttu-id="6a0dd-146">所有会社のコンセプトは、法人のコンセプトと同じです。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-146">The concept of an owning company equates to the concept of a legal entity.</span></span> <span data-ttu-id="6a0dd-147">このプロジェクトから発生するすべての費用と収益は、所有会社の総勘定元帳に計上されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-147">All costs and revenue accruing from this project are accounted for in the General ledger of the owning company.</span></span> |
| <span data-ttu-id="6a0dd-148">丸め</span><span class="sxs-lookup"><span data-stu-id="6a0dd-148">Is Rounding</span></span> | <span data-ttu-id="6a0dd-149">**契約品目の顧客** タブの編集可能なグリッドと、契約品目の顧客に向けたメインフォームと簡易作成フォーム</span><span class="sxs-lookup"><span data-stu-id="6a0dd-149">Editable grid on **Contract Line Customers** tab and Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="6a0dd-150">このフィールドは、この顧客がこのプロジェクトベースの契約品目の既定の丸め顧客であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-150">This field indicates if this customer is a default rounding customer for this project-based contract line.</span></span> | <span data-ttu-id="6a0dd-151">課金分割率に応じた実績を生成する場合、丸め処理の差異が多少発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-151">When you generate an actual according to the billing split percentage, there may be some rounding differences.</span></span> <span data-ttu-id="6a0dd-152">この顧客は、この場合の丸め込みの違いが原因です。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-152">This customer is attributed the rounding differences in this case.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="6a0dd-153">請求分割率の編集</span><span class="sxs-lookup"><span data-stu-id="6a0dd-153">Edit billing split percentages</span></span>

<span data-ttu-id="6a0dd-154">請求分割率はグリッドで編集することができます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-154">Billing split percentages can be edited in the grid.</span></span> <span data-ttu-id="6a0dd-155">請求分割率の合計が 100％ でない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-155">When the billing split percentages don't total 100 percent, an error will occur.</span></span> <span data-ttu-id="6a0dd-156">課金分割率を編集した後、ページを更新してエラーを解消してください。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-156">After you edit the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="6a0dd-157">また、契約品目の顧客サブグリッドで **均等に分配する** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-157">You can also try selecting **Evenly Distribute** on the contract line customer subgrid.</span></span> <span data-ttu-id="6a0dd-158">このアクションは、すべての契約品目の顧客に請求の分割を均等に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-158">This action evenly allocates billing splits to all contract line customers.</span></span> <span data-ttu-id="6a0dd-159">丸め処理の係数がある場合は、丸め顧客に追加されます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-159">If there is any rounding factor, it will be added to the rounding customer.</span></span> <span data-ttu-id="6a0dd-160">1つの契約品目の顧客は、**丸め込み** フラグが **はい** に設定されている状態で、常に **丸め込み** 顧客としてタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="6a0dd-160">One contract line customer is always tagged as the **Rounding** customer with the **Rounding** flag set to **Yes**.</span></span>