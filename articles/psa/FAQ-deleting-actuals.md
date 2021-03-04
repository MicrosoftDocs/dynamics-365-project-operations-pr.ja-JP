---
title: レコードを実績のエンティティから削除できない理由
description: このトピックでは、なぜ実績のエンティティからレコードを削除できないのかを説明します。
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148964"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="ff6b9-103">レコードを実績エンティティから削除できない理由</span><span class="sxs-lookup"><span data-stu-id="ff6b9-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ff6b9-104">Project Service Automation (PSA) では実績を削除することができません。これは、総勘定元帳などの下流システムに財務的な影響を与える取引の事実を示す根拠となるためです。</span><span class="sxs-lookup"><span data-stu-id="ff6b9-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="ff6b9-105">実績が削除できてしまうと、財務報告取引の整合性が疑われることになりかねません。</span><span class="sxs-lookup"><span data-stu-id="ff6b9-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="ff6b9-106">監査証跡を設定するには、顧客は仕訳を使用して補償取引を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff6b9-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

