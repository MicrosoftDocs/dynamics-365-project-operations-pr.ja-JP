---
title: 経費実績で価格が既定でゼロになっている理由を教えてください。
description: 経費実績で価格が既定でゼロになっている理由のトラブルシューティング。
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752848"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>経費実績で価格が既定でゼロになっている理由を教えてください。

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

この FAQ は、トランザクション クラスが経費に設定されていて、トランザクションの種類がコストになっている経費実績に適用されます。

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>経費実績でのコスト レートのトラブルシューティング

関連する経費エントリに移動し、経費入力フィールドの金額があることを確認します。 発生元経費エントリの金額フィールドが入力されていない場合、問題が分離されています。
 
この問題を解決するには、有効な金額を持つ経費エントリを再作成して承認します。
