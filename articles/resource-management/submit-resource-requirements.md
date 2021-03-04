---
title: リソース要求の送信
description: リソース要求として生成されたリソース要件を送信できます。 要求は、実行する場合はリソース マネージャーに送信されます。
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128829"
---
# <a name="submit-a-resource-request"></a>リソース要求の送信

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

リソース要求として生成されたリソース要件を送信できます。 要求は、実行する場合はリソース マネージャーに送信されます。

1. Dynamics 365 Project Operations の **プロジェクト** ページで、**チーム** タブを選択して、予約可能なリソースの一覧を表示します。 
2. 一覧からリソース要件を持つ汎用リソースを選択し、**要求を送信する** をクリックします。

汎用要求チーム メンバーの要求の状態が **送信済み** に変更されます。

要求が満たされた後、名前付きリソースの予約によりリソース マネージャーが要求を満たすと、汎用リソースは名前付きリソースに置き換えられます。 それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合、汎用リソースはチームに残り、要求の状態が **レビューが必要** に変更されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]