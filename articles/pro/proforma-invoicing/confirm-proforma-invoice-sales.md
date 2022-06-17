---
title: プロジェクトの見積もり請求の確認
description: この記事では、Project Operations でプロフォーマ プロジェクト ベースの請求書を確認する方法について説明します。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922228"
---
# <a name="confirm-a-proforma-project-invoice"></a>プロジェクトの見積もり請求の確認 

_**適用対象:** ライト展開 - 見積もり請求の取引_


見積送り状が確認されると、プロジェクト請求書の状態は **確認済み** に更新されます。 請求書が確認されると、読み取り専用になります。 今後、請求書は、顧客が開始した修正または与信がある場合にのみ修正できます。

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
ドラフト請求書を編集しない材料トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
元の材料用途承認の数量と金額に対する未請求の販売取消。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
元の材料用途承認の数量と金額に対する請求済みの販売実績。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
数量を減らすために編集された材料トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
元の時間承認の数量と金額に対する未請求の販売取消。
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
数量を増やすために編集された材料トランザクションの請求。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
元の材料用途承認の数量と金額に対する未請求の販売取消。
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
