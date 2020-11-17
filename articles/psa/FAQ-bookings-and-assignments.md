---
title: リソースの予約およびタスク割当への関連付け
description: このトピックでは、名前付きリソース、リソースの登録、およびタスクの割り当てを管理する方法と、それらの相互関係について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079455"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>リソースの予約およびタスク割当への関連付け


名前付きリソースをプロジェクトチームに登録し、プロジェクトタスクを割り当てるには、2つの方法があります:

- リソースはプロジェクトに直接登録し、プロジェクトタスクに割り当てることができます。
- タスクは汎用リソースに割り当てることができます。その後、汎用リソースを検索して指定された実際のリソースと置き換えるために使用されます。 

どちらの場合も、リソースの予約操作ではリソースのキャパシティが確保されます。

プロジェクトを計画しているプロジェクトマネージャーはプロジェクト計画とスケジュールを所有しています。 プロジェクト管理者は、割り当てに標準リソースを使用し、その標準リソースからリソース要求を生成することにより、プロジェクト計画で指定された配分型を使用してプロジェクトにリソースを予約することができます。 リソースをプロジェクトに予約してタスクに割り当てることはできますが、予約の配分型をタスクの配分型に合わせることはできません。 予約はプロジェクトのスケジュールには影響しません。

同じ種類の複数のリソースが同時に作業する必要がある、重複する複数のタスクを持つ複雑なプロジェクトを検討してください。 リソースに、割り当ての集計と異なるコンターが与えられた場合、タスクを変更して予約のコンターを別個のタスクおよびその元のコンターに合わせることは困難です。

次の例では、4 つの一連のタスクの同じリソースが必要とする合計工数は、2 週間にわたる 62 時間であり、特定のコンターがあります。 同じ 2 週だがコンターが異なる 62 時間がリソース Bob に対して予約された場合、要件と予約は一致します。

| **タスクのコンター**    | **合計時間** | 6/4 月 | 6/5 火 | 6/6 水 | 6/7 木 | 6/8 金 | 6/9 土 | 6/10 日 | 6/11 月 | 6/12 火 | 6/13 水 | 6/14 木 | 6/15 金 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| タスク 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| タスク 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| タスク 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| タスク 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **合計**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bob の空き時間
| **リソース予約** | **合計時間** | 6/4 月 | 6/5 火 | 6/6 水 | 6/7 木 | 6/8 金 | 6/9 土 | 6/10 日 | 6/11 月 | 6/12 火 | 6/13 水 | 6/14 木 | 6/15 金 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

ただし、予約された時間コントーを 1 日単位でタスクに割り当てる系統的な方法は存在しません。 プロジェクト管理者がリソースの空き時間に合わせてプロジェクト スケジュールを変更したいと思っている場合、割り当てを削除し、予約コントーに合致するすべてのタスクを変更する必要があります。

組織がプロジェクト管理者とリソース マネージャーの両方にプロジェクト計画タスクを与えた場合、プロジェクト管理者は、必要な作業のコントーを含むスケジュールを設定します。 リソース マネージャーは、プロジェクト マネージャーに知らせずに、実質リソースの予約時に工数コントーを変更することによりスケジュールに影響を与えることはできません。 プロジェクト管理者が要求したものとは別のものをリソース マネージャーが実行しようとする場合、プロジェクト スケジュールで必要な内容に関する取り決めを結ぶ必要があります。

予約と割り当ては密接に連携されていないため、タスクの配分型とは異なる配分型を予約したり、割り当てを変更すると、予約と割り当ての整合性が失われる場合があります。

プロジェクトマネージャーは **調整ビュー** を使用することで、各プロジェクトチームメンバーの登録と割り当てを確認することができます。 このビューでは、チーム メンバーの予約と割り当てが一致しないことを示すために色と網かけが使用されます。 この情報に基づいて、プロジェクト管理者は、割り当てがあるが予約がない場合にリソースの予約を延長したり、リソースが予約されているが割り当てがない予約をキャンセルしたりするために、修正アクションを実行できます。

> [!NOTE]
> 自分で配分型を設定したタスクを移動すると、その配分型は維持されません。 コントーは、プロジェクトのカレンダーに従って、作業時間と祝日の変更に合わせてアカウントに再生成されます。 これは、システムが元の配分型の意図を把握せず、その配分型を新しい期間に保持することが適切かどうかを判断できないためです。 予約と割当は切り離されるため、予約は元の配分型を保持します。 この場合、キャンセルするか再予約して新しい割り当てコントーにする必要があります。
