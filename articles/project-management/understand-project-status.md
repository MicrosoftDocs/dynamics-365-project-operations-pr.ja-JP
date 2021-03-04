---
title: プロジェクトの状態について
description: このトピックでは、Dynamics 365 Project Operations においてプロジェクトに割り当てられた状態ついて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127299"
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