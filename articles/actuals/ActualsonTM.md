---
title: 時間と材料のエンゲージメントにおける実際の影響
description: このトピックでは、Microsoft Dynamics 365 Project Operations の時間と材料のエンゲージメントのライフサイクルにおける様々なイベントでの Actuals テーブルへの影響について説明します。
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a4ea3f9cf74d8a67447571001b75065b8cde5c00
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580830"
---
# <a name="actuals-impact-in-a-time-and-materials-engagement"></a>時間と材料のエンゲージメントにおける実際の影響

_**適用対象 :** リソース/非在庫ベースのシナリオに使用する Project Operations、見積請求に対応する小規模のデプロイ_

以下の表は、時間と材料のエンゲージメントにおいて様々なイベントで発生する様々な種類のトランザクションの実績を示しています。

| イベント | コストの実績 | 未請求売上の実績 | 請求済み営業の実績 | 例 |
|---|---|---|---|---|
| 時間が作成されました。 | 該当なし | 該当なし | 該当なし | <p>1 時間当たり 100 米国ドル (USD100) のコストレートを持つ Fabrikam US の組織ユニットのボブ コザックは、"Arm Installation at Adatum (Adatum でのアームの設置作業)" というプロジェクトに取り組んでいます。 このプロジェクトでは、彼の契約請求レートは 1 時間あたり 200 米国ドルです。 これがボブ コザックが入力したサンプル時間です:</p><p>ボブ コザック、8 時間</p> |
| 時間が提出されました。 | 該当なし | 該当なし | 該当なし | 時間入力のために、コスト仕訳帳明細行と未請求売上仕訳帳が作成されます。 仕訳入力には、既定の価格と原価率が入力されています。 |
| 時間入力は承認される前にリコールされます。 | 該当なし | 該当なし | 該当なし | |
| 承認された時間: 提出された時間は請求可能な時間と同じです。 | 費用の実績が作成されました。 | 未請求の営業実績が作成されます。 | 該当なし | <p>新しい実績が作成されました:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブコザック、8時間、1,600 米国ドル</li></ul> |
| 承認された時間: 請求可能な時間は、提出された時間より短くなります。 | 費用の実績が作成されました。 | <p>2 つの未請求売上実績が作成されます:</p><ul><li>請求可能な時間帯の未請求の営業実績</li><li>残量に応じた非課金の未請求の営業実績</li></ul> | 該当なし | <p>新しい実績が作成されました:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブ コザック、6 時間、1,200 米国ドル、*請求可能*</li><li>**実際の未請求売上:** ボブ コザック、2 時間、400 米国ドル、*請求不可能*</li></ul> |
| 承認された時間: 請求可能な時間は、提出された時間より長くなります。 | 費用の実績が作成されました。 | 未請求の営業実績が作成されます。 | 該当なし | <p>新しい実績が作成されました:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブ コザック、10 時間、2,000 米国ドル</li></ul> |
| 時間の承認がキャンセルされました。 | <p>元の原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** である取消原価実績が作成されます。</p> | <p>元の未請求営業実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** の取消未請求の売上実績が作成されます。</p> | 該当なし | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li><li>**実際の未請求売上:** ボブ コザック、(8時間)、(1,600 米国ドル)、*調整不能*</li></ul> |
| 時間入力は承認された後にリコールされます。 | <p>元の原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** である取消原価実績が作成されます。</p> | <p>元の未請求営業実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** の取消未請求の売上実績が作成されます。</p> | 該当なし | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li><li>**実際の未請求売上:** ボブ コザック、(8時間)、(1,600 米国ドル)、*調整不能*</li></ul> |
| 契約が確認されました。 | <p>古い原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** となっている取消原価実績が作成されます。</p><p>契約上のルールを再評価した上で、新たなコスト実績を作成します。</p> | <p>古いの未請求営業実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** の取消未請求の売上実績が作成されます。</p><p>契約上のルールを見直した上で、新たに未請求の売上実績を作成します。</p> | 該当なし | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li><li>**実際の未請求売上:** ボブ コザック、(8時間)、(1,600 米国ドル)、*調整不能*</li></ul><p>再評価された財務上の影響に対して作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブコザック、8時間、1,600 米国ドル</li></ul> |
| 請求書が作成されます。 | 該当なし | 該当なし | 該当なし | |
| 請求書が確認されます。 請求書行明細の数量は、未請求売上実績の数量から変更されません。 | 該当なし | <p>古い未請求売上実績の請求書ステータスが更新されます。</p><p>調整ステータスが **調整不能** の取消未請求の売上実績が作成されます。 | 請求済みの営業実績が作成されます。 | <p>変更されない既存の実際:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li></ul><p>更新される既存の実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*顧客の請求書が転記されました*</li></ul>財務上の作業中 (WIP) 処理を取り消すために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)</li></ul><p>請求された売上値を記録するために作成される新しい実績:</p><ul><li>**実際の請求済み売上:** ボブ コザック、8 時間、1,600 米国ドル</li></ul> |
| 請求書明細の数量が未請求売上実績の数量から減らした後に、請求書が確定します。 | 該当なし | <p>元の未請求営業実績の調整ステータスが **調整済み** に更新されます。</p><p>取消未請求販売実績は、元の未請求販売実績に対して作成されます。 調整状態は **調整不能** となります。</p><p>2 つの新規未請求売上実績が作成されます:</p><ul><li>請求可能な時間帯の未請求の営業実績</li><li>残量に応じた非課金の未請求の営業実績</li></ul><p>取消未請求販売実績は、2 つの新規未請求販売実績に対して作成されます。</p> | <p>2 つの請求済売上実績が作成されます:</p><ul><li>請求可能な時間帯の請求済みの営業実績</li><li>残量に応じた非課金の請求済みの営業実績</li></ul> | <p>変更されない既存の実際:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li></ul><p>更新される既存の実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*調整済み*</li></ul><p>以前の財務務上 WIP を取り消すために作成された新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(8時間)、(1,600 米国ドル)、*調整不能*</li></ul><p>更新された営業の WIP を記録するために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、6 時間、1,200 米国ドル、*請求可能*</li><li>**実際の未請求売上:** ボブ コザック、2 時間、400 米国ドル、*請求不可能*</li></ul><p>更新された営業の WIP を取り消しするために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(6 時間)、(1,200 米国ドル)、*請求可能*</li><li>**実際の未請求売上:** ボブ コザック、(2 時間)、(400 米国ドル)、*請求不可能*</li></ul><p>請求された売上値を記録するために作成される新しい実績:</p><ul><li>**実際の請求済売上:** ボブ コザック、6 時間、1,200 米国ドル、*請求可能*</li><li>**実際の請求済み売上:** ボブ コザック、2 時間、400 米国ドル、*請求不可能*</li></ul> |
| 請求書明細の数量が未請求売上実績の数量から増量した後に、請求書が確定します。 | 該当なし | <p>元の未請求営業実績の調整ステータスが **調整済み** に更新されます。</p><p>取消未請求販売実績は、元の未請求販売実績に対して作成されます。 調整状態は **調整不能** となります。</p><p>新しい数量に対して、新しい未請求売上実績が作成されます。</p><p>取消未請求販売実績は、新規未請求販売実績に対して作成されます。</p> | 新しい数量に対して、請求済み売上実績が作成されます。 | <p>変更されない既存の実際:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li></ul><p>更新される既存の実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*調整済み*</li></ul><p>以前の財務務上 WIP を取り消すために作成された新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(8時間)、(1,600 米国ドル)、*調整不能*</li></ul><p>更新された営業の WIP を記録するために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、10 時間、2,000 米国ドル、*請求可能*</li></ul><p>更新された営業の WIP を取り消すために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(10 時間)、(2,000 米国ドル)、*請求可能*、*請求不可能*</li></ul><p>請求された売上値を記録するために作成される新しい実績:</p><ul><li>**実際の請求済売上:** ボブ コザック、10 時間、2,000 米国ドル、*請求可能*</li></ul> |
| 請求書は修正され、請求可能な数量または価格が減少します。 | 該当なし | <p>2 つの未請求売上実績が作成されます:</p><ul><li>修正請求書の数量の実際の請求可能な未請求売上</li><li>残量に応じた非課金の請求可能な営業実績</li></ul><p>取消未請求販売実績は、2 つの新規未請求販売実績に対して作成されます。</p> | <p>取消請求済売上実績が作成されます:</p><p>新しい数量に対して、新しい請求済み売上実績が作成されます。 | <p>変更されない既存の実際:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*顧客の請求書が転記されました*</li><li>**実際の未請求売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)</li></ul><p>更新される既存の実績:</p><ul><li>**実際の請求済み売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)、*調整済み*</li></ul><p>以前の売上値を取り消しするために作成される新しい実績:</p><ul><li>**実際の請求済み売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)、*調整不能*</li></ul><p>修正された営業の WIP を記録するために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、6 時間、1,200 米国ドル、*請求可能*、*顧客の請求書が転記されました*</li><li>**実際の未請求売上:** ボブ コザック、2 時間、400 米国ドル、*請求可能*</li></ul><p>修正された営業の WIP を取り消すために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(6 時間)、(1,200 米国ドル)、*請求可能*、*請求不可能*</li></ul><p>修正された売上値を記録するために作成される新しい実績:</p><ul><li>**実際の請求済売上:** ボブ コザック、6 時間、1,200 米国ドル、*請求可能*</li></ul> |
| 請求書は修正され、請求可能な数量または価格が増額します。 | 該当なし | <p>新しい数量に対して、新しい未請求売上実績が作成されます。</p> <p>取消未請求販売実績は、新規未請求販売実績に対して作成されます。</p> | <p>取消請求済売上実績が作成されます:</p>新しい数量に対して、新しい請求済み売上実績が作成されます。</p> | <p>変更されない既存の実際:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブ コザック、8時間、1,600 米国ドル、*顧客の請求書が転記されました*</li><li>**実際の未請求売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)</li></ul><p>更新される既存の実績:</p><ul><li>**実際の請求済み売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)、*調整済み*</li></ul><p>以前の売上値を取り消しするために作成される新しい実績:</p><ul><li>**実際の請求済み売上:** ボブ コザック、(8 時間)、(1,600 米国ドル)、*調整不能*</li></ul><p>修正された営業の WIP を記録するために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、10 時間、2,000 米国ドル、*請求可能*、*顧客の請求書が転記されました*</li></ul><p>修正された営業の WIP を取り消すために作成される新しい実績:</p><ul><li>**実際の未請求売上:** ボブ コザック、(10 時間)、(2,000 米国ドル)、*請求可能*</li></ul><p>修正された売上値を記録するために作成される新しい実績:</p><ul><li>**実際の請求済売上:** ボブ コザック、10 時間、2,000 米国ドル、*請求可能*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]