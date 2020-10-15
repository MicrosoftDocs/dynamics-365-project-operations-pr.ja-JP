---
title: プロジェクトの状態について
description: このトピックでは、Dynamics 365 Project Operations においてプロジェクトに割り当てられた状態ついて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965682"
---
# <a name="understand-project-status"></a>プロジェクトの状態について

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


 **プロジェクト エンティティ**  ページの **状態** セクションに、コストと労力に基づいたプロジェクトの正常性の概要が表示されます。


## <a name="status-summary-fields"></a>ステータス サマリー フィールド

-  **プロジェクト全体のステータス**  フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。 このフィールドは、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。 
-  **コメント**  フィールドでは、プロジェクト マネージャーは状態について特定のコメントを入力することができます。 
-  **状態更新日** フィールドは編集できません。 このフィールドの値は、状態が最後に更新された日時を示すタイムスタンプです。
-  **スケジュール パフォーマンス**  フィールドと **コスト パフォーマンス**  フィールドは追跡グリッドから設定されます。  **工数の追跡**  ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドは **先行**に更新されます。 ルート ノードのスケジュールとコスト差異がマイナスの場合、これらのフィールドは **遅延**に設定されます。
