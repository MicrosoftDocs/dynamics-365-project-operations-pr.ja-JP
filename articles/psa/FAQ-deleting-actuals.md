---
title: レコードを実績のエンティティから削除できない理由
description: この記事では、実績のエンティティからレコードを削除できない理由について説明します。
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
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925586"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>レコードを実績エンティティから削除できない理由

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) では実績を削除することができません。これは、総勘定元帳などの下流システムに財務的な影響を与える取引の事実を示す根拠となるためです。 実績が削除できてしまうと、財務報告取引の整合性が疑われることになりかねません。 監査証跡を設定するには、顧客は仕訳を使用して補償取引を作成する必要があります。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
