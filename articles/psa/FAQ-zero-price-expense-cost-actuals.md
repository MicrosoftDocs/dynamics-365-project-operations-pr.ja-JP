---
title: 経費実績で価格が既定でゼロになっている理由を教えてください。
description: 経費実績で価格が既定でゼロになっている理由のトラブルシューティング。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146354"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>経費実績で価格が既定でゼロになっている理由を教えてください

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

この FAQ は、トランザクション クラスが経費に設定されていて、トランザクションの種類がコストになっている経費実績に適用されます。

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>経費実績でのコスト レートのトラブルシューティング

関連する経費エントリに移動し、経費入力フィールドの金額があることを確認します。 発生元経費エントリの金額フィールドが入力されていない場合、問題が分離されています。
 
この問題を解決するには、有効な金額を持つ経費エントリを再作成して承認します。
