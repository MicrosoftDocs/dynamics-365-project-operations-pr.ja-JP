---
title: リソース管理に関するよくある質問
description: このトピックでは、リソース管理についてのよくある質問への回答を提供します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079479"
---
# <a name="resource-management-faq"></a>リソース管理に関するよくある質問

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>チーム メンバーとリソース要件の違いは何ですか。

プロジェクト チーム メンバーは、タスクが割り当てられたり、予約または超過予約されたり、承認者として設定することができます。 リソース要件は、要求の下書きメモとして、プロジェクト チーム メンバーなしでも存在することができます。 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>提案された時間と仮予約された時間の違いは何ですか。

提案された時間と仮予約された時間は表示形式が異なります。 提案された時間は、リソース要求を使用して要求を開始したリソース マネージャーのみに表示されます。 仮予約された時間は、スケジュール ボードにアクセスできるすべてのユーザーに表示されます。

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>チーム上でリソースに仮予約された時間はどうしたら見れますか？

仮予約は、リソース要件を予約した際に予約することができます。 プロジェクト チームで仮予約されたリソースは、時間が仮予約されたチーム メンバーとして表示されます。 これらはスケジュール ボード上でも表示されます。

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>予約したリソースに対して、必要な時間を変更し、1 日の開始および終了はどのようにおこないますか。

リソースを予約した後、 **予約の維持** を選択して、必要な変更をおこないます。

## <a name="what-resources-types-does-project-service-automation-support"></a>Project Service Automation ではどのような種類のリソースをサポートしますか？

**ユーザー** および **取引先担当者** が Dynamics 365 Project Service Automation でサポートされている唯一のリソースの種類です。 その他の種類 ( **備品** 、 **グループ** など) のリソースも作成可能ですが、これはエンド ツー エンドでの使用はサポートされていません。

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>割り当てと予約の違いは何ですか。

割り当ては、プロジェクト スケジュール内のプロジェクト タスクに対するリソースの割り当てです。 このリソースは、実際のリソースまたは汎用リソースのいずれかになります。 予約は、プロジェクトに対するリソースの本配賦または仮配賦です。 本予約はリソースのキャパシティを消費します。 理想としては、実際のリソースに対して、予約と割り当ては違いがないことから、これらは一致させる必要があります。 ただし、PSA はこの一致を強制しません。 調整ビューでは、リソースの予約と割り当てが一致しない場所のプロジェクト マネージャーが表示されます。
