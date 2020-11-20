---
title: 見積もり請求の確認 (ライト)
description: このトピックでは、Project Operations で見積送り状を確認する方法について解説します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176527"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="88bce-103">見積もり請求の確認 (ライト)</span><span class="sxs-lookup"><span data-stu-id="88bce-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="88bce-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="88bce-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="88bce-105">見積送り状が確認されると、プロジェクト請求書の状態は **確認済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="88bce-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="88bce-106">請求書が確認されると、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="88bce-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="88bce-107">今後、請求書の訂正は、顧客が開始した訂正やクレジットがある場合、または請求書が支払い済みとマークされている場合にのみ修正することができます。</span><span class="sxs-lookup"><span data-stu-id="88bce-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="88bce-108">次の表は、システムがで作成した実績を表示しています。</span><span class="sxs-lookup"><span data-stu-id="88bce-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="88bce-109">これらの実績は、プロジェクトの請求書のドラフトが確定する前に、プロジェクトの請求書案に対して一定の操作を行った場合に作成されます。</span><span class="sxs-lookup"><span data-stu-id="88bce-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="88bce-110">
                    <strong>シナリオ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88bce-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="88bce-111">
                    <strong>確認時に作成された実績</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88bce-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-112">前払いまたは保留金の請求</span><span class="sxs-lookup"><span data-stu-id="88bce-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-113">前払い金や<strong>留保金</strong>に対して、タイプの課金売上実績、留保金が作成されます。</span><span class="sxs-lookup"><span data-stu-id="88bce-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-114">留保金や前払い金のマイナス額の未請求売上実績で、調整のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="88bce-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-115">請求書の留保金や前払い金の調整が完了した後。</span><span class="sxs-lookup"><span data-stu-id="88bce-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-116">調整のために作成された留保金や前払い金の未請求売上の取り崩し。</span><span class="sxs-lookup"><span data-stu-id="88bce-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="88bce-117">この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。</span><span class="sxs-lookup"><span data-stu-id="88bce-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-118">この請求書に記載されている金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="88bce-119">請求書の一部の留保金や前払い金の調整が完了した後。</span><span class="sxs-lookup"><span data-stu-id="88bce-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-120">調整のために作成された留保金や前払い金の未請求売上の取り崩し。</span><span class="sxs-lookup"><span data-stu-id="88bce-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="88bce-121">この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。</span><span class="sxs-lookup"><span data-stu-id="88bce-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-122">この請求書に記載されている金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-123">将来の請求書の精算に使用する残額の未請求売上高実績のマイナスの金額。</span><span class="sxs-lookup"><span data-stu-id="88bce-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-124">請求書のドラフトを編集せずに時間トランザクションの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="88bce-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-125">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="88bce-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-126">当初の時間承認上の時間と金額についての課金売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="88bce-127">数量を減らすために編集されたタイム トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="88bce-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-128">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="88bce-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-129">編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-130">残りの時間に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。</span><span class="sxs-lookup"><span data-stu-id="88bce-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-131">数量を増やすために編集された時間トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="88bce-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-132">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="88bce-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-133">編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-134">請求書のドラフトを編集せずに経費トランザクションの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="88bce-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-135">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="88bce-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-136">当初の経費承認上の数量と金額の請求済み売上実績</span><span class="sxs-lookup"><span data-stu-id="88bce-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="88bce-137">数量を減らすために編集された経費トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="88bce-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-138">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="88bce-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-139">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-140">残りの数量に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。</span><span class="sxs-lookup"><span data-stu-id="88bce-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-141">数量を増やすために編集された経費トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="88bce-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-142">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="88bce-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-143">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求の売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88bce-144">料金の請求。</span><span class="sxs-lookup"><span data-stu-id="88bce-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-145">当初の仕訳行の料金金額の未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="88bce-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-146">当初の料金仕訳明細上の数量と金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="88bce-147">マイルストーンの請求。</span><span class="sxs-lookup"><span data-stu-id="88bce-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-148">プロジェクト契約品目の元のマイルストーン上のマイルストーン金額に対する請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="88bce-149">製品ベースの契約品目を請求する。</span><span class="sxs-lookup"><span data-stu-id="88bce-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="88bce-150">製品ベースの契約品目に由来する数量と金額で、製品明細の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="88bce-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
