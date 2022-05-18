---
title: エンゲージメントのプリセールス段階における実績の影響
description: このトピックでは、Microsoft Dynamics 365 Project Operations でエンゲージメントがプリセールス段階にあるときの、さまざまなイベントでの Actuals テーブルへの影響について説明します。
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
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577242"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>エンゲージメントのプリセールス段階における実績の影響

_**適用対象 :** リソース/非在庫ベースのシナリオに使用する Project Operations、見積請求に対応する小規模のデプロイ_

以下の表は、プロジェクト エンゲージメントのプリセールス段階における様々なイベントで発生する様々な種類のトランザクションの実績を示しています。

| イベント | コストの実績 | 例 |
|---|---|---|
| 時間が作成されました。 | 該当なし | <p>1 時間当たり 100 米国ドル (USD100) のコストレートを持つ Fabrikam US の組織ユニットのボブ コザックは、"Arm Installation at Adatum (Adatum でのアームの設置作業)" というプロジェクトに取り組んでいます。 このプロジェクトは、契約品目上の固定価格課金方式にマッピングされています。 これがボブ コザックが入力したサンプル時間です:</p><p>ボブ コザック - 8 時間</p> |
| 時間が提出されました。 | 該当なし | 時間入力の費用仕訳帳明細行が作成されます。 既定のコスト率は、仕訳入力に入力されます。 |
| 時間入力は承認される前にリコールされます。 | 該当なし | |
| 時間が承認されました。 | 費用の実績が作成されました。 | <p>新しい実績が作成されました:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li></ul> |
| 時間の承認がキャンセルされました。 | <p>元の原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** である取消原価実績が作成されます。</p> | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li></ul> |
| 時間入力は承認された後にリコールされます。 | <p>元の原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** である取消原価実績が作成されます。</p> | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li></ul> |
| 見積もりを獲得し、契約書を作成します。 | <p>古い原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** となっている取消原価実績が作成されます。</p><p>契約上のルールを再評価した上で、新たなコスト実績を作成します。</p> | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li></ul><p>見積もりを獲得し、契約を作成する際に、再評価された財務上の影響について作成される新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li><li>**実際の未請求売上:** ボブコザック、8時間、1,600 米国ドル</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]