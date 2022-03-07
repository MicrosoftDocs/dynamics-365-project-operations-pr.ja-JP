---
title: プロジェクトの状態について
description: このトピックは、Dynamics 365 Project Operations のプロジェクトに割り当てられたステータスに関する情報を提供します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286479"
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