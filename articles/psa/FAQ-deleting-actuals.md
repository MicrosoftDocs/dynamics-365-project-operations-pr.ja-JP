---
title: レコードを実績のエンティティから削除できない理由
description: このトピックでは、なぜ実績のエンティティからレコードを削除できないのかを説明します。
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079394"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>レコードを実績エンティティから削除できない理由

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) では実績を削除することができません。これは、総勘定元帳などの下流システムに財務的な影響を与える取引の事実を示す根拠となるためです。 実績が削除できてしまうと、財務報告取引の整合性が疑われることになりかねません。 監査証跡を設定するには、顧客は仕訳を使用して補償取引を作成する必要があります。

