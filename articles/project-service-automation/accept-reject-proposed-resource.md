---
title: 提案されたプロジェクト リソースを承認または拒否する
description: このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 8270b895-b103-4ca4-984f-ed577bbf4057
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 005c6d364dcc7127a2cd8023f125f15f67c1a9ce
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752879"
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
