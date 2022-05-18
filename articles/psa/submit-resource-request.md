---
title: リソース要求を送信する
description: このトピックでは、プロジェクト リソースの要求を送信する方法について説明します。
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d22f52771f55a551416d1ba2f7105d59d7b912f0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577472"
---
# <a name="submitting-a-resource-request"></a>リソース要求を送信する

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

リソース要求として生成されたリソース要件を送信できます。 要求は、実行する場合はリソース マネージャーに送信されます。

1. Project Service Automation (PSA) の **プロジェクト** ページで、 **チーム** タブをクリックして一覧の予約可能リソースを表示します。 
2. 一覧からリソース要件を持つ汎用リソースを選択して、**要求を送信する** をクリックします。

![リソース要求を送信する。](media/RM-how-to-18.png)

汎用的なチーム メンバーの要求ステータスが **送信済** に変わります。

リソース マネージャーによって要求が満たされた後、名前付きリソースの予約を使用してリソース マネージャーが要求を満たすと、汎用リソースは名前付きリソースに置き換えられます。 それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合は汎用リソースはチームに残り、要求の状態が **レビューが必要** に変更されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
