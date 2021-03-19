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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285850"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="7dc68-103">経費実績で価格が既定でゼロになっている理由を教えてください</span><span class="sxs-lookup"><span data-stu-id="7dc68-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7dc68-104">この FAQ は、トランザクション クラスが経費に設定されていて、トランザクションの種類がコストになっている経費実績に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7dc68-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="7dc68-105">経費実績でのコスト レートのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="7dc68-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="7dc68-106">関連する経費エントリに移動し、経費入力フィールドの金額があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7dc68-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="7dc68-107">発生元経費エントリの金額フィールドが入力されていない場合、問題が分離されています。</span><span class="sxs-lookup"><span data-stu-id="7dc68-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="7dc68-108">この問題を解決するには、有効な金額を持つ経費エントリを再作成して承認します。</span><span class="sxs-lookup"><span data-stu-id="7dc68-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]