---
title: プロジェクトの状態について
description: この記事では、Dynamics 365 Project Operations でプロジェクトに割り当てられた状態について説明します。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923608"
---
# <a name="understand-project-status"></a>プロジェクトの状態について

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


**プロジェクト エンティティ** ページの **状態** セクションには、コストと労力に基づいたプロジェクトの正常性の概要が表示されます。


## <a name="status-summary-fields"></a>ステータス サマリー フィールド

- **プロジェクト全体のステータス** フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。 このフィールドは、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。 
- **コメント** フィールドでは、プロジェクト マネージャーはステータスについて特定のコメントを入力することができます。 
- **状態更新日** フィールドは編集できません。 このフィールドの値は、状態が最後に更新された日時を示すタイムスタンプです。
- **スケジュール効率** フィールドと **コスト効率** フィールドは追跡グリッドから設定されます。 **工数の追跡** ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドは **先行** に更新されます。 ルート ノードのスケジュールとコスト差異がマイナスの場合、これらのフィールドは **遅延** に設定されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]