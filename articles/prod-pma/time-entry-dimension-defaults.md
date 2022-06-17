---
title: プロジェクトの時間入力に財務分析コードを規定として適用する
description: この記事では、財務分析コードが時間エントリに適用される方法について説明します。
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916570"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>プロジェクトの時間入力に財務分析コードを規定として適用する

[!include [banner](../includes/banner.md)]

プロジェクトの時間エントリに財務分析コードを適用するには、分析コードの既定値が以下の順序に基づいていることに注意してください。

1. リソース
2. Project
3. 資金調達ソース

たとえば、既定の分析コードがリソースに指定されている場合、プロジェクトに指定されている既定よりも優先して適用されます。 同様に、既定の分析コードがプロジェクトに指定されている場合、資金源に指定されている既定よりも優先して適用されます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
