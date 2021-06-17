---
title: プロジェクトの修正ベース請求書の作成
description: このトピックは、Project Operations における修正請求書の確認に関する情報を提供します。
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001625"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="a2f64-103">プロジェクトの修正ベース請求書の作成</span><span class="sxs-lookup"><span data-stu-id="a2f64-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="a2f64-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a2f64-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a2f64-105">確認済みのプロジェクト請求書は、顧客およびプロジェクト マネージャーとの交渉に従って変更、またはクレジットを処理するように修正できます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="a2f64-106">確定した請求書を編集するには、確定した請求書を開き、**この請求書を修正する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a2f64-107">この選択は、プロジェクトの請求書が確定していない場合は利用できません。</span><span class="sxs-lookup"><span data-stu-id="a2f64-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="a2f64-108">確認された請求書から新しいドラフト版の請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="a2f64-109">以前に確認された請求書のすべての請求書明細の詳細が新しいドラフトにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="a2f64-110">以下は、新しく修正された請求書の明細の情報を理解するのに役立ついくつかの重要なポイントです。</span><span class="sxs-lookup"><span data-stu-id="a2f64-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="a2f64-111">すべての数量がゼロに更新されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-111">All quantities are updated to zero.</span></span> <span data-ttu-id="a2f64-112">これは、すべての請求項目が完全に貸方記入されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="a2f64-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="a2f64-113">必要に応じて、これらの数量を手動で更新して、請求されている数量ではなく、入金されている数量を反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="a2f64-114">入力した数量に基づいて、アプリケーションはクレジットされた数量を計算します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="a2f64-115">この金額は、修正した請求書を確認した際に作成される実績に反映されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="a2f64-116">税額を変更する場合は、控除対象の税額ではなく、正しい税額を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2f64-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="a2f64-117">マイルストーンの修正は常に完全なクレジットとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="a2f64-118">顧客が誤った金額で請求された場合、留保金や立替金の金額を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="a2f64-119">留保金や立替金の調整については、以前に確認された請求書の料金との調整に誤った金額が使用されていた場合に修正することができます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2f64-120">他のすでに請求された料金の修正である請求書行の明細には、**修正** フィールドが **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a2f64-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="a2f64-121">請求書明細の詳細を修正した請求書には、**訂正あり** というフィールドがあり、ここも **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a2f64-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="a2f64-122">修正請求書の確認時に作成された実績</span><span class="sxs-lookup"><span data-stu-id="a2f64-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="a2f64-123">次の表に、修正請求書が確認されたときに作成される実績を示します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="a2f64-124">
                    <strong>シナリオ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2f64-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="a2f64-125">
                    <strong>確認時に作成された実績</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2f64-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="a2f64-126">請求書の前払いや留保金の修正を確認します。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2f64-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-127">調整のために作成された留保金や前払い金の未請求売上の取り崩し。</span><span class="sxs-lookup"><span data-stu-id="a2f64-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="a2f64-128">この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。</span><span class="sxs-lookup"><span data-stu-id="a2f64-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-129">請求売上の割戻実績は、元の請求売上を取り崩すために、留保金や前払い金に計上されている金額に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-130">留保金や前払い金の修正請求書明細の修正金額に対して、新たに請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-131">留保金や前払い金の修正請求書明細のマイナス額の未請求売上実績で、調整のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="a2f64-132">以前に調整された留保金や前払い金の修正を確認します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-133">調整のために作成された留保金や前払い金の未請求売上の取り崩し。</span><span class="sxs-lookup"><span data-stu-id="a2f64-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="a2f64-134">この金額は正の値であり、前回の調整が発生した際に作成された負の値を相殺することを意味します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-135">前回の請求書に記載されている金額の請求済み売上戻入実績。</span><span class="sxs-lookup"><span data-stu-id="a2f64-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-136">訂正後の請求書に適用される、訂正後の留保金に対する新たな請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="a2f64-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-137">未請求の売上実績で、補正後の残余の留保金や前払い金をマイナスにしたもので、後の請求書の精算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a2f64-138">以前に請求された時間トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-139">時間の元の請求書明細詳細の時間と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-140">時間分の元の請求書明細の詳細の時間と金額の新しい未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a2f64-141">時間トランザクションでの部分的なクレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-142">時間分の元の請求書明細の詳細に請求された時間と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-143">編集された請求書明細の詳細に時間と金額を請求する新たな未請求売上実績、これを取り崩して、同等の請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-144">請求書明細の詳細に記載されている修正数値を差し引いた残りの時間と金額を請求する新たな未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a2f64-145">以前に請求された経費トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-146">経費の元となる請求書明細の詳細に記載されている数量と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-147">経費の元となる請求書明細の詳細に記載されている数量と金額に対して、新たに未請求の売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a2f64-148">以前に請求された経費トランザクションの一部のクレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-149">経費の元となる請求書明細の詳細に記載されている数量と金額に対する、請求済みの売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-150">訂正された請求書明細の明細書上の数量と、金額に応じて請求される新たな未請求売上実績、これを取り崩して、これに相当する請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-151">請求書明細の詳細に記載されている修正数値を差し引いた残りの数量と金額を請求する新たな未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a2f64-152">以前に請求された料金トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-153">料金の元となる請求書明細の詳細に記載されている数量と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-154">料金の元となる請求書明細の詳細に記載されている数量と金額に対して、新たに未請求の売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a2f64-155">以前に請求された料金トランザクションの一部のクレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-156">元の請求書明細の詳細に請求された数量と金額を、手数料のために請求された売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-157">訂正・修正された請求書明細の明細書上の数量と、金額に応じて請求される新たな未請求売上実績、これを取り崩して、これに相当する請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a2f64-158">以前に請求されたマイルストーンの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-159">マイルストーンの元の請求書明細詳細の時間と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="a2f64-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="a2f64-160">マイルストーンの請求書ステータスが、<b>顧客請求書転記済み</b>から<b>請求準備完了</b>に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a2f64-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a2f64-161">以前に請求されたマイルストーンの一部クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="a2f64-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a2f64-162">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="a2f64-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
