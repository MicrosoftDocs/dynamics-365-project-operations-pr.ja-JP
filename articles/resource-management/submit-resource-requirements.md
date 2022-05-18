---
title: リソース要求の送信
description: リソース要求として生成されたリソース要件を送信できます。 要求は、実行する場合はリソース マネージャーに送信されます。
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 583524ccf33f2dc42ee6beba7e00cc5fd74819d4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598678"
---
# <a name="submit-a-resource-request"></a>リソース要求の送信

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

リソース要求として生成されたリソース要件を送信できます。 要求の達成のため、要求はリソース マネージャーに送信されます。

1. Dynamics 365 Project Operations の **プロジェクト** ページで、**チーム** タブを選択して、予約可能なリソースの一覧を表示します。 
2. 一覧からリソース要件を持つ汎用リソースを選択し、**要求を送信する** をクリックします。

汎用要求チーム メンバーの要求の状態が **送信済み** に変更されます。

要求が満たされた後、リソース マネージャーが名前付きのリソースで要求を処理すると、汎用リソースが名前付きのリソースで置き換えられます。 それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合、汎用リソースはチームに残り、要求の状態が **レビューが必要** に変更されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]