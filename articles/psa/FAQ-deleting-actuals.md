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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127164"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="43246-103">レコードを実績エンティティから削除できない理由</span><span class="sxs-lookup"><span data-stu-id="43246-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="43246-104">Project Service Automation (PSA) では実績を削除することができません。これは、総勘定元帳などの下流システムに財務的な影響を与える取引の事実を示す根拠となるためです。</span><span class="sxs-lookup"><span data-stu-id="43246-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="43246-105">実績が削除できてしまうと、財務報告取引の整合性が疑われることになりかねません。</span><span class="sxs-lookup"><span data-stu-id="43246-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="43246-106">監査証跡を設定するには、顧客は仕訳を使用して補償取引を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43246-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

