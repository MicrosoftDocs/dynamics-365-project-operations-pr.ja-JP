---
title: 見積もり請求の確認
description: このトピックでは、Project Operations で見積送り状を確認する方法について解説します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079176"
---
# <a name="confirming-a-proforma-invoice"></a>見積もり請求の確認

_**適用対象:** ライト展開 - 見積もり請求の取引_


見積送り状が確認されると、プロジェクト請求書の状態は **確認済み** に更新されます。 請求書が確認されると、読み取り専用になります。 今後、請求書の訂正は、顧客が開始した訂正やクレジットがある場合、または請求書が支払い済みとマークされている場合にのみ修正することができます。

次の表は、システムがで作成した実績を表示しています。 これらの実績は、プロジェクトの請求書のドラフトが確定する前に、プロジェクトの請求書案に対して一定の操作を行った場合に作成されます。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>シナリオ</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>確認時に作成された実績</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
前払いまたは保留金の請求 </p>
            </td>
            <td width="408" valign="top">
                <p>
前払い金や<strong>留保金</strong>に対して、タイプの課金売上実績、留保金が作成されます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
留保金や前払い金のマイナス額の未請求売上実績で、調整のために使用されます。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
請求書の留保金や前払い金の調整が完了した後。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
調整のために作成された留保金や前払い金の未請求売上の取り崩し。 この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
この請求書に記載されている金額の請求済み売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
請求書の一部の留保金や前払い金の調整が完了した後。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
調整のために作成された留保金や前払い金の未請求売上の取り崩し。 この金額は、前払いや留保金が請求されたときに発生したマイナスを相殺する意味があるので、プラスになります。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
この請求書に記載されている金額の請求済み売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
将来の請求書の精算に使用する残額の未請求売上高実績のマイナスの金額。
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
編集された請求書の詳細の時間と金額に対して課金される新たな未請求売上実績、請求売上実績の戻し処理、および同等の請求売上実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
残りの時間に課金されない新規未課金販売実績と、編集した請求書の明細書に記載されている修正後の数値を差し引いた金額、請求売上高実績の取崩し、およびそれに準ずる請求売上高実績の計上値。
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
当初の経費承認上の数量と金額の請求済み売上実績 </p>
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
編集された請求書ライン詳細上の数量と金額に応じて課金される新たな未請求売上実績、未請求の売上実績の戻し処理、および同等の請求売上実績。 
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
        <tr>
            <td width="216" valign="top">
                <p>
製品ベースの契約品目を請求する。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
製品ベースの契約品目に由来する数量と金額で、製品明細の請求済み売上実績。
                </p>
            </td>
        </tr>
    </tbody>
</table>