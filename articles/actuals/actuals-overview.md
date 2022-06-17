---
title: 実績
description: この記事では、Microsoft Dynamics 365 Project Operations で実績を操作する方法について説明します。
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924804"
---
# <a name="actuals"></a>実績

_**適用対象 :** リソース/非在庫ベースのシナリオに使用する Project Operations、見積請求に対応する小規模のデプロイ_

実績は、プロジェクトのレビューおよび承認された財務およびスケジュールの進捗状況を表します。 時間、経費、材料使用量の入力、仕訳、請求書の承認時に作成されます。

> [!IMPORTANT]
> 実績を編集したり、システムから削除したりしないでください。 財務の完全性および他の財務および会計システムとの統合に悪影響が及ぶ可能性があります。 Microsoft Dynamics 365 Project Operations では、実績の取り消しや置き換えを利用して、プロジェクトのビジネス プロセスのライフサイクルのさまざまなポイントで実績を編集することができます。

## <a name="recording-actuals-based-on-project-events"></a>プロジェクト イベントに基づく実績を記録する

Project Operations は、プロジェクト エンゲージメントのライフサイクルの中で発生する金融取引を実績として記録します。 ライフサイクルの各イベントにおける実績の作成は、プロジェクト契約が時間、材料課金モデルか固定価格課金モデルか、またプリ セールスの段階か社内プロジェクトかによって異なります。

以下の記事では、さまざまなバリエーションのイベントにおける Actuals テーブルへの影響について説明します:

- [時間と材料のエンゲージメントにおける実際の影響](ActualsonTM.md)
- [固定価格エンゲージメントにおける実績の影響](ActualonFP.md)
- [エンゲージメントのプリセールス段階における実績の影響](ActualonPreSales.md)
- [内部プロジェクトにおける実績の影響](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
