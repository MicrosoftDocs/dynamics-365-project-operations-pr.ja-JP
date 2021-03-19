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
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279144"
---
# <a name="submit-a-resource-request"></a>リソース要求の送信

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

リソース要求として生成されたリソース要件を送信できます。 要求の達成のため、要求はリソース マネージャーに送信されます。

1. Dynamics 365 Project Operations の **プロジェクト** ページで、**チーム** タブを選択して、予約可能なリソースの一覧を表示します。 
2. 一覧からリソース要件を持つ汎用リソースを選択し、**要求を送信する** をクリックします。

汎用要求チーム メンバーの要求の状態が **送信済み** に変更されます。

要求が満たされた後、リソース マネージャーが名前付きのリソースで要求を処理すると、汎用リソースが名前付きのリソースで置き換えられます。 それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合、汎用リソースはチームに残り、要求の状態が **レビューが必要** に変更されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]