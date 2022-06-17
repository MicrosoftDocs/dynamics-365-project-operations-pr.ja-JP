---
title: 内部プロジェクトにおける実績の影響
description: この記事では、Microsoft Dynamics 365 Project Operations の内部プロジェクトのさまざまなイベントでの Actuals テーブルへの影響に関する情報を提供します。
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921354"
---
# <a name="actuals-impact-for-an-internal-project"></a>内部プロジェクトにおける実績の影響

_**適用対象 :** リソース/非在庫ベースのシナリオに使用する Project Operations、見積請求に対応する小規模のデプロイ_

以下の表は、内部プロジェクト エンゲージメントにおいて様々なイベントで発生する様々な種類のトランザクションの実績を示しています。

| イベント | コストの実績 | 例 |
|---|---|---|
| 時間が作成されました。 | 該当なし | <p>1 時間当たり 100 米国ドル (USD100) のコストレートを持つ Fabrikam US の組織ユニットのボブ コザックは、"Arm Installation at Adatum (Adatum でのアームの設置作業)" というプロジェクトに取り組んでいます。 このプロジェクトは、契約品目上の固定価格課金方式にマッピングされています。 これがボブ コザックが入力したサンプル時間です:</p><p>ボブ コザック - 8 時間</p> |
| 時間が提出されました。 | 該当なし | 時間入力の費用仕訳帳明細行が作成されます。 既定のコスト率は、仕訳入力に入力されます。 |
| 時間入力は承認される前にリコールされます。 | 該当なし | |
| 時間が承認されました。 | 費用の実績が作成されました。 | <p>新しい実績が作成されました:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル</li></ul> |
| 時間の承認はキャンセルされます。 | <p>元の原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** である取消原価実績が作成されます。</p> | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li></ul> |
| 時間入力は承認された後にリコールされます。 | <p>元の原価実績の調整ステータスが **調整済み** に更新されます。</p><p>調整ステータスが **調整不能** である取消原価実績が作成されます。</p> | <p>更新される既存の実績:</p><ul><li>**実際の費用:** ボブ コザック、8時間、800 米国ドル、*調整済み*</li></ul><p>以前の財務務上の影響を取り消すために作成された新しい実績:</p><ul><li>**実際の費用:** ボブ コザック、(8時間)、800 米国ドル、*調整不能*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
