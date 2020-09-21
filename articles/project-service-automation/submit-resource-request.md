---
title: リソース要求を送信します
description: このトピックでは、プロジェクト リソースの要求を送信する方法について説明します。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752901"
---
# <a name="submit-a-resource-request"></a>リソース要求を送信します

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

リソース要求として生成されたリソース要件を送信できます。 要求は、実行する場合はリソース マネージャーに送信されます。

1. Project Service Automation (PSA) の **プロジェクト** ページで、 **チーム** タブをクリックして一覧の予約可能リソースを表示します。 
2. 一覧からリソース要件を持つ汎用リソースを選択して、**要求を送信する**をクリックします。

![リソース要求を送信する](media/RM-how-to-18.png)

汎用要求チーム メンバーの要求の状態が **送信済み**に変更されます。

リソース マネージャーによって要求が満たされた後、名前付きリソースの予約を使用してリソース マネージャーが要求を満たすと、汎用リソースは名前付きリソースに置き換えられます。 それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合は汎用リソースはチームに残り、要求の状態が **レビューが必要**に変更されます。
