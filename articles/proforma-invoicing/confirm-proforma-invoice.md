---
title: プロジェクトの見積もりベース請求の確認
description: このトピックは、見積もりプロジェクトベース請求書の確認に関する情報を提供します。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012142"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="6ab3b-103">プロジェクトの見積もりベース請求の確認</span><span class="sxs-lookup"><span data-stu-id="6ab3b-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="6ab3b-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6ab3b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6ab3b-105">見積送り状が確認されると、プロジェクト請求書の状態は **確認済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="6ab3b-106">請求書が確認されると、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="6ab3b-107">今後、請求書は、顧客が開始した修正または与信がある場合にのみ修正できます。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="6ab3b-108">次の表は、システムがで作成した実績を表示しています。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="6ab3b-109">これらの実績は、プロジェクトの請求書のドラフトが確定する前に、プロジェクトの請求書案に対して一定の操作を行った場合に作成されます。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="6ab3b-110">
                    <strong>シナリオ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ab3b-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="6ab3b-111">
                    <strong>確認時に作成された実績</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ab3b-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-112">前払いまたは保留金の請求</span><span class="sxs-lookup"><span data-stu-id="6ab3b-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-113">前払い金や<strong>留保金</strong>に対して、タイプの課金売上実績、留保金が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-114">調整に使用される着手金または前払金の金額がマイナスの実際の未請求売上。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-115">請求書の留保金や前払い金の調整が完了した後。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-116">調整のために作成された留保金や前払い金の未請求売上の取り崩し。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6ab3b-117">この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-118">この請求書に記載されている金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6ab3b-119">請求書の一部の留保金や前払い金の調整が完了した後。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-120">調整のために作成された留保金や前払い金の未請求売上の取り崩し。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6ab3b-121">この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-122">この請求書に記載されている金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-123">将来の請求書の精算に使用する残額の未請求売上高実績のマイナスの金額。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-124">請求書のドラフトを編集せずに時間トランザクションの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-125">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-126">当初の時間承認上の時間と金額についての課金売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6ab3b-127">数量を減らすために編集されたタイム トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-128">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-129">編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-130">編集された請求書明細の修正された数値、売上実績の取消、および同等の請求済みの実績を差し引いた後の残りの時間と金額については請求不可である新しい未請求の売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-131">数量を増やすために編集された時間トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-132">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-133">編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-134">請求書のドラフトを編集せずに経費トランザクションの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-135">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-136">当初の経費承認上の数量と金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6ab3b-137">数量を減らすために編集された経費トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-138">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-139">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-140">残りの数量に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-141">数量を増やすために編集された経費トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-142">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-143">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求の売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-144">ドラフト請求書を編集しない材料トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-145">元の材料用途承認の数量と金額に対する未請求の販売取消。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-146">元の材料用途承認の数量と金額に対する請求済みの販売実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6ab3b-147">数量を減らすために編集された材料トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-148">元の時間承認の数量と金額に対する未請求の販売取消。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-149">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-150">残りの数量に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-151">数量を増やすために編集された材料トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-152">元の材料用途承認の数量と金額に対する未請求の販売取消。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-153">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ab3b-154">料金の請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-155">当初の仕訳行の料金金額の未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-156">当初の料金仕訳明細上の数量と金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6ab3b-157">マイルストーンの請求。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6ab3b-158">プロジェクト契約品目の元のマイルストーン上のマイルストーン金額に対する請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="6ab3b-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
