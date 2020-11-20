---
title: 予約と割り当て
description: このトピックでは、リソースの予約とリソースの割り当ての違いについて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130224"
---
# <a name="bookings-vs-assignments"></a>予約と割り当て

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

予約は、プロジェクトに対するリソースの本配賦または仮配賦です。 本予約はリソースのキャパシティを消費します。 予約はチームの組織的なコンセプトを表すため、様々なプロジェクトでリソースをどのように活用するかを理解できるようになっています。 Dynamics 365 Project Operations は、予約をプロジェクト レベルのコンセプトとして捉えています。 

割り当てとは、予約とは異なり、プロジェクト スケジュールの中で、プロジェクトのタスクにリソースを割り当てます。 リソースには名前を付けることも、汎用なものにすることもできます。 

通常、リソースの予約の合計は、1つまたは複数のタスクを横断するリソースの割り当ての合計と同じになります。 ただし、 Project Operations ではこの一致を強制しません。 **調整** ビューでは、リソースの予約と割り当てが一致しない箇所をプロジェクト マネージャに表示します。
