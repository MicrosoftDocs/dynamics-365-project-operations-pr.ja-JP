---
title: 提案されたプロジェクト リソースを承認または拒否する
description: このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
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
ms.openlocfilehash: 4c10c55961c74c2dc53fabd1d041a935ca9a4870
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079432"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a>提案されたプロジェクト リソースを承認または拒否する

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。

リソース マネージャーがプロジェクトの汎用リソース要求を満たすために名前付きリソースを提案すると、汎用チーム メンバーの **要求の状態** フィールドが **レビューが必要** に更新されます。 要求が承認や拒否のためにプロジェクト マネージャーに送信されます。

![提案がある汎用チーム メンバー](media/RM-how-to-19.png)

**プロジェクト チーム メンバー** ページの **提案されたリソース** タブのグリッドには、提案されたリソースの現在の予約が表示されます。 提案が承認された後、グリッドはその予約を反映して更新されます。 

提案されたリソースを承認してチームでそのリソースを予約するには **提案の承認** をクリックします。  
提案を拒否するには **リソースの拒否** をクリックします。

![リソース提案の承認](media/RM-how-to-20.png) 

名前付きリソースで汎用リソース要求を直接満たすのと同様に、汎用リソースは置き換えられ、割り当てられたタスクは名前付きチーム メンバーで更新されます。
