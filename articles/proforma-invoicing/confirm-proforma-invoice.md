---
title: 見積送り状の確認
description: このトピックでは、見積送り状の確認について説明します。
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287874"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="2e0c1-103">見積送り状の確認</span><span class="sxs-lookup"><span data-stu-id="2e0c1-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="2e0c1-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2e0c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2e0c1-105">見積送り状が確認されると、プロジェクト請求書の状態は **確認済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="2e0c1-106">請求書が確認されると、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="2e0c1-107">今後、請求書の訂正は、顧客が開始した訂正やクレジットがある場合、または支払い済みとマークされている場合にのみ修正することができます。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="2e0c1-108">次の表は、システムがで作成した実績を表示しています。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="2e0c1-109">これらの実績は、プロジェクトの請求書のドラフトが確定する前に、プロジェクトの請求書案に対して一定の操作を行った場合に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="2e0c1-110">
                    <strong>シナリオ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e0c1-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="2e0c1-111">
                    <strong>確認時に作成された実績</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e0c1-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e0c1-112">請求書のドラフトを編集せずに時間トランザクションの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-113">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-114">当初の時間承認上の時間と金額についての課金売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2e0c1-115">数量を減らすために編集されたタイム トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-116">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-117">編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-118">残りの時間に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e0c1-119">数量を増やすために編集された時間トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-120">当初の承認時の時間および金額に対する未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-121">編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e0c1-122">請求書のドラフトを編集せずに経費トランザクションの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-123">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-124">当初の経費承認上の数量と金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2e0c1-125">数量を減らすために編集された経費トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-126">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-127">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-128">残りの数量に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e0c1-129">数量を増やすために編集された経費トランザクションの請求。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-130">当初の経費承認上の数量と金額の未請求売上取崩し。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-131">編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未処理の売上実績の戻し処理、および同等の請求売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e0c1-132">料金の請求。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-133">当初の仕訳行の料金金額の未請求売上戻し処理。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-134">当初の料金仕訳明細上の数量と金額の請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2e0c1-135">マイルストーンの請求。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2e0c1-136">プロジェクト契約品目の元のマイルストーン上のマイルストーン金額に対する請求済み売上実績。</span><span class="sxs-lookup"><span data-stu-id="2e0c1-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]