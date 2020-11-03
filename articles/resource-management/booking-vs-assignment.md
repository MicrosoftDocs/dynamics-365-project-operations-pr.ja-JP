---
title: 予約と割り当て
description: このトピックでは、リソースの予約とリソースの割り当ての違いについて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079117"
---
# <a name="bookings-vs-assignments"></a>予約と割り当て

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

予約は、プロジェクトに対するリソースの本配賦または仮配賦です。 本予約はリソースのキャパシティを消費します。 

割り当ては、プロジェクト スケジュール内のプロジェクト タスクに対するリソースの割り当てです。 このリソースは、実際のリソースまたは汎用リソースになります。 

理想としては、実際のリソースに対して、予約と割り当ては違いがないことから、これらは一致させる必要があります。 ただし、Microsoft Dynamics Project Operations はこの一致を強制しません。 **調整** ビューでは、リソースの予約と割り当てが一致しない場所のプロジェクト マネージャーが表示されます。
