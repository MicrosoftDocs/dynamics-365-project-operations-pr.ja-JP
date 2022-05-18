---
title: プロジェクトの時間入力に財務分析コードを規定として適用する
description: このトピックでは、財務分析コードが時間エントリに適用される方法について説明します。
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597942"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>プロジェクトの時間入力に財務分析コードを規定として適用する

[!include [banner](../includes/banner.md)]

プロジェクトの時間エントリに財務分析コードを適用するには、分析コードの既定値が以下の順序に基づいていることに注意してください。

1. リソース
2. Project
3. 資金調達ソース

たとえば、既定の分析コードがリソースに指定されている場合、プロジェクトに指定されている既定よりも優先して適用されます。 同様に、既定の分析コードがプロジェクトに指定されている場合、資金源に指定されている既定よりも優先して適用されます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
