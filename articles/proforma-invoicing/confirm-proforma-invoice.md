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
# <a name="confirm-a-proforma-invoice"></a>見積送り状の確認

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

見積送り状が確認されると、プロジェクト請求書の状態は **確認済み** に更新されます。 請求書が確認されると、読み取り専用になります。 今後、請求書の訂正は、顧客が開始した訂正やクレジットがある場合、または支払い済みとマークされている場合にのみ修正することができます。

次の表は、システムがで作成した実績を表示しています。 これらの実績は、プロジェクトの請求書のドラフトが確定する前に、プロジェクトの請求書案に対して一定の操作を行った場合に作成されます。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>シナリオ</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>確認時に作成された実績</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
請求書のドラフトを編集せずに時間トランザクションの請求書を作成します。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の承認時の時間および金額に対する未請求売上戻し処理。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
当初の時間承認上の時間と金額についての課金売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
数量を減らすために編集されたタイム トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の承認時の時間および金額に対する未請求売上戻し処理。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
残りの時間に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
数量を増やすために編集された時間トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の承認時の時間および金額に対する未請求売上戻し処理。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
請求書のドラフトを編集せずに経費トランザクションの請求書を作成します。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の経費承認上の数量と金額の未請求売上取崩し。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
当初の経費承認上の数量と金額の請求済み売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
数量を減らすために編集された経費トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の経費承認上の数量と金額の未請求売上取崩し。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求売上実績の戻し処理、および同等の請求売上実績。 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
残りの数量に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、未請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
数量を増やすために編集された経費トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の経費承認上の数量と金額の未請求売上取崩し。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未処理の売上実績の戻し処理、および同等の請求売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
料金の請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
当初の仕訳行の料金金額の未請求売上戻し処理。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
当初の料金仕訳明細上の数量と金額の請求済み売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
マイルストーンの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
プロジェクト契約品目の元のマイルストーン上のマイルストーン金額に対する請求済み売上実績。
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]