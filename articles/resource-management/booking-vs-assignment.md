---
title: 予約と割り当て
description: この記事では、リソースの予約とリソースの割り当ての違いについて説明します。
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918594"
---
# <a name="bookings-vs-assignments"></a>予約と割り当て

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

予約は、プロジェクトに対するリソースの本配賦または仮配賦です。 本予約は、リソースの能力を消費します。 予約はチームの組織的な概念を表し、リソースがさまざまなプロジェクトにまたがってどのように関与するのか理解できます。 Dynamics 365 Project Operations は、予約をプロジェクト レベルの概念として扱います。 

割り当ては予約と異なり、プロジェクト スケジュールのプロジェクト タスクに対してリソースを確保することです。 リソースには名前を付けることも、汎用なものにすることもできます。  リソース要件がプロジェクト タスクの割り当てから導き出される場合、Project Operations は、リソース割り当ての工数コントーを使用して、リソース要件の詳細のコントーを作成します。 ただし、リソース割り当てへの参照は維持されません。 リソース要件から導き出された予約を更新しても、リソース割り当ては更新されません。

通常、予約されたリソースの合計は、1 つまたは複数のタスクへのリソースの割り当ての合計と等しくなります。 ただし、 Project Operations ではこの一致を強制しません。 **調整** ビューでは、リソースの予約と割り当てが一致しない箇所をプロジェクト マネージャに表示します。




[!INCLUDE[footer-include](../includes/footer-banner.md)]