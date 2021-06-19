---
title: プロジェクトの修正ベース請求書
description: このトピックは、Project Operations におけるプロジェクトベースの修正請求書の作成と確認方法に関する情報を提供します。
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012277"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="90f31-103">プロジェクトの修正ベース請求書</span><span class="sxs-lookup"><span data-stu-id="90f31-103">Corrective project-based invoices</span></span>

<span data-ttu-id="90f31-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="90f31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="90f31-105">確認済みのプロジェクト請求書は、顧客およびプロジェクト マネージャーとの交渉に従って変更、またはクレジットを処理するように修正できます。</span><span class="sxs-lookup"><span data-stu-id="90f31-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="90f31-106">確定した請求書を編集するには、確定した請求書を開き、**この請求書を修正する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90f31-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="90f31-107">この選択は、プロジェクトの請求書が確認されるか、プロジェクトベースの請求書に前払金または着手金、あるいは前払金または着手金の調整が含まれていない限り利用できません。</span><span class="sxs-lookup"><span data-stu-id="90f31-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="90f31-108">確認された請求書から新しいドラフト版の請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="90f31-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="90f31-109">以前に確認された請求書のすべての請求書明細の詳細が新しいドラフトにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="90f31-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="90f31-110">新たに訂正した請求書の明細詳細について、理解しておくべきポイントを以下に挙げます :</span><span class="sxs-lookup"><span data-stu-id="90f31-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="90f31-111">すべての数量がゼロに更新されます。</span><span class="sxs-lookup"><span data-stu-id="90f31-111">All quantities are updated to zero.</span></span> <span data-ttu-id="90f31-112">Dynamics 365 Project Operations は、すべての請求項目が完全に貸方記入されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="90f31-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="90f31-113">必要に応じて、これらの数量を手動で更新して、請求されている数量ではなく、入金されている数量を反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="90f31-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="90f31-114">入力した数量に基づいて、アプリケーションはクレジットされた数量を計算します。</span><span class="sxs-lookup"><span data-stu-id="90f31-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="90f31-115">この金額は、修正した請求書を確認した際に作成される実績に反映されます。</span><span class="sxs-lookup"><span data-stu-id="90f31-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="90f31-116">税額を変更する場合は、控除対象の税額ではなく、正しい税額を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90f31-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="90f31-117">マイルストーンの修正は常に完全なクレジットとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="90f31-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="90f31-118">他のすでに請求された料金の修正である請求書行の明細には、**修正** フィールドが **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="90f31-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="90f31-119">修正済みの明細行を持つ請求書の場合、**修正あり** フィールドが **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="90f31-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="90f31-120">修正請求書が確認されたときに作成された実績</span><span class="sxs-lookup"><span data-stu-id="90f31-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="90f31-121">次の表に、修正請求書が確認されたときに作成される実績を示します。</span><span class="sxs-lookup"><span data-stu-id="90f31-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="90f31-122">
                    <strong>シナリオ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90f31-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="90f31-123">
                    <strong>確認時に作成された実績</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90f31-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="90f31-124">以前に請求された時間トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-125">時間の元の請求書明細詳細の時間と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-126">時間分の元の請求書明細の詳細の時間と金額の新しい未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="90f31-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="90f31-127">時間トランザクションでの部分的なクレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-128">時間分の元の請求書明細の詳細に請求された時間と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-129">編集された請求書明細の詳細に時間と金額を請求する新たな未請求売上実績、これを取り崩して、同等の請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="90f31-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-130">請求書明細の詳細に記載されている修正数値を差し引いた残りの時間と金額を請求する新たな未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="90f31-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="90f31-131">以前に請求された経費トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-132">経費の元となる請求書明細の詳細に記載されている数量と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-133">経費の元となる請求書明細の詳細に記載されている数量と金額に対して、新たに未請求の売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="90f31-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="90f31-134">以前に請求された経費トランザクションの一部のクレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-135">経費の元となる請求書明細の詳細に記載されている数量と金額に対する、請求済みの売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-136">訂正された請求書明細の明細書上の数量と、金額に応じて請求される新たな未請求売上実績、これを取り崩して、これに相当する請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="90f31-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-137">請求書明細の詳細に記載されている修正数値を差し引いた残りの数量と金額を請求する新たな未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="90f31-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="90f31-138">以前に請求された材料トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-139">元の材料の請求行明細の数量と金額に対する請求済みの販売取消。</span><span class="sxs-lookup"><span data-stu-id="90f31-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-140">元の材料の請求行明細の数量と金額に対する新しい未請求の売上実績。</span><span class="sxs-lookup"><span data-stu-id="90f31-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="90f31-141">材料トランザクションの部分的クレジットの請求。</span><span class="sxs-lookup"><span data-stu-id="90f31-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-142">元の材料の請求行明細で請求された数量と金額に対する請求済みの販売取消。</span><span class="sxs-lookup"><span data-stu-id="90f31-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-143">編集された請求書明細の数量と金額、これの取り消し、および同等の請求済み販売実績に対して請求可能な、新しい未請求販売実績。</span><span class="sxs-lookup"><span data-stu-id="90f31-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-144">請求書明細の詳細に記載されている修正数値を差し引いた残りの数量と金額を請求する新たな未請求の売上実績です。</span><span class="sxs-lookup"><span data-stu-id="90f31-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="90f31-145">以前に請求された料金トランザクションの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-146">料金の元となる請求書明細の詳細に記載されている数量と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-147">料金の元となる請求書明細の詳細に記載されている数量と金額に対して、新たに未請求の売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="90f31-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="90f31-148">以前に請求された料金トランザクションの一部のクレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-149">元の請求書明細の詳細に請求された数量と金額を、手数料のために請求された売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-150">訂正・修正された請求書明細の明細書上の数量と、金額に応じて請求される新たな未請求売上実績、これを取り崩して、これに相当する請求売上実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="90f31-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="90f31-151">以前に請求されたマイルストーンの全クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-152">マイルストーンの元の請求書明細詳細の時間と金額の請求済み売上戻入です。</span><span class="sxs-lookup"><span data-stu-id="90f31-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="90f31-153">マイルストーンの請求書ステータスが、<b>顧客請求書転記済み</b>から<b>請求準備完了</b>に更新されます。</span><span class="sxs-lookup"><span data-stu-id="90f31-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="90f31-154">以前に請求されたマイルストーンの一部クレジットを請求します。</span><span class="sxs-lookup"><span data-stu-id="90f31-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="90f31-155">このシナリオはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="90f31-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
