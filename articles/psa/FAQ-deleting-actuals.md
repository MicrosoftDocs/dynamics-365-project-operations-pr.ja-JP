---
title: レコードを実績のエンティティから削除できない理由
description: このトピックでは、なぜ実績のエンティティからレコードを削除できないのかを説明します。
author: JPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584418"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>レコードを実績エンティティから削除できない理由

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) では実績を削除することができません。これは、総勘定元帳などの下流システムに財務的な影響を与える取引の事実を示す根拠となるためです。 実績が削除できてしまうと、財務報告取引の整合性が疑われることになりかねません。 監査証跡を設定するには、顧客は仕訳を使用して補償取引を作成する必要があります。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
