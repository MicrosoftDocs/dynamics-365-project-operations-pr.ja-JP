---
title: Project Service Automation の予約割り当て方法
description: このトピックでは、予約の割り当てを登録する方法について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 295da428ce15e7775450dfa94e96047f200bdede
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079262"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Project Service Automation の予約割り当て方法

**Team** タブでチーム メンバーをプロジェクトに直接追加するか、スケジュール ボードからプロジェクトまたは要件にリソースを予約するかにかかわらず、いくつかの異なる予約の割当方法を使用できます。 このトピックでは、それぞれの方法がどのように機能し、どの方法がリソースのオーバーブッキングにつながるかを説明します。

## <a name="full-capacity"></a>全キャパシティ 
全キャパシティでは、指定した開始日および終了日のリソースのすべてのキャパシティが予約されます。 たとえば、あるリソースのカレンダーで1日8時間、1週間に5日の稼働日が設定されている場合、開始日と終了日に5日の稼働日を設定すると、そのリソースの40時間が予約されます。 リソースの残りのキャパシティに関係なく予約が実行されます。 他のプロジェクトでその期間中にリソースが既に予約されている場合、40 時間が追加時間として予約されるため、重複予約につながる可能性があります。

## <a name="remaining-capacity"></a>残りのキャパシティ
この方法は、スケジュール ボードを使用してプロジェクトに直接予約する場合にのみ使用することができます。 この方法は、指定された日付範囲内のリソースの使用可能なキャパシティを予約します。 たとえば、リソースのキャパシティが週40時間で、すでに10時間予約されている場合に、この週に予約すると、その週の残り30時間のキャパシティが予約されます。

## <a name="percentage-capacity"></a>キャパシティの割合
キャパシティの割合方式では、指定した開始日と終了日におけるキャパシティの割合によってリソースを予約します。 たとえば、リソースのカレンダーが週5日、1日8時間の稼働時間に設定されている場合、稼働率を50%に設定して稼働日を5日間に設定すると、リソースは20時間予約されます。 1 日あたりの個々の予約は、期間内で均等に分散されます。たとえば、この例では 1 日あたり 4 時間となります。 リソースの残りのキャパシティに関係なく予約が実行されます。 リソースがその期間中に他のプロジェクトですでに予約されている場合、20時間は追加時間として予約されるため、重複予約が発生する可能性があります。

## <a name="evenly-distribute-hours"></a>均等分布時間
この方法では、指定した開始日から終了日まで、1日あたりの時間を均等に配分して、指定した時間数のリソースを予約します。 たとえば、あるリソースを20時間、5日間で予約すると、20時間が各日で均等に配分されます。 リソースの残りのキャパシティに関係なく予約が実行されます。 リソースがその期間中に他のプロジェクトですでに予約されている場合、20時間は追加時間として予約されるため、重複予約が発生する可能性があります。

## <a name="front-load-hours"></a>前倒し時間
この方法では、指定された開始日から終了日まで1日当たりの時間を前倒しして、指定された時間数のリソースを予約します。 前倒しでは、リソースの使用可能なキャパシティが "空いている" 順に消費されます。 たとえば、リソースの作業スケジュールが1日8時間、1週間に5日で、現在の予約がない場合は、リソースを20時間、5営業日の期間にわたって予約すると、各日にわたって以下のような予約パターンになります。 

|         予約          |    1 日目    |    2 日目    |    3 日目    |    4 日目    |    5 日目    |    合計    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    既存の予約    |    12        |    12        |    12        |    12        |    12        |    12        |
|    新しい予約          |    8        |    8        |    4        |    0        |    0        |    20       |

前倒し方法は、既存の予約と使用可能なキャパシティを考慮します。 たとえば、同じリソースに作業週における 20 週間の予約が既にある場合、新しい予約は次のとおり残りのキャパティを消費します。

|   予約          | 1 日目 | 2 日目 | 3 日目 | 4 日目 | 5 日目 | 合計 |
|---------------------|-------|-------|-------|-------|-------|-------|
| 既存の予約 | 8     | 8     | 4     | 12     | 12     | 20    |
| 新しい予約       | 0     | 0     | 4     | 8     | 8     | 20    |

使用可能なキャパシティが考慮されるため、その予約が吸収できる残りのキャパシティがリソースにがない場合、エラー メッセージが発生することがあります。 この方法では、重複予約することはありません。

## <a name="none"></a>なし
この方法は、プロジェクト内の **チーム** タブから予約する場合にのみ使用できます。 この方法は、プロジェクトにリソース メンバーとしてリソースを追加しますが、リソースのキャパシティを吸収する予約は作成しません。 この方法は、プロジェクトの作成時に既定のプロジェクト マネージャー チーム メンバーが追加されるときに使用されます。 プロジェクト エンティティ レコードに所有者が設定され、プロジェクトの承認者が設定されるように、プロジェクトを作成したプロジェクト マネージャー ユーザーはプロジェクトに既定で追加されます。 このユーザーには予約がないため、リソースを予約する場合は、別の割り当て方法を使用してリソースを削除してから再度追加するか、タスクにリソースを追加してから、 **調整** タブの **予約の延長** を使用して予約の割り当てを作成できます。

## <a name="allocation-methods-that-lead-to-overbooking"></a>重複予約につながる割り当て方法
要約すると、次の割り当て方法は重複予約につながります。リソースが既に他のプロジェクト (または、他の作業指示書またはスケジュール可能なエンティティ) に割り当てられている場合。

- 全キャパシティ
- キャパシティの割合
- 均等分布時間

これらの割り当て方法の 1 つを使用すると、リソースが重複予約されても通知が表示されません。 重複予約を修正するには、スケジュール ボードを使用する必要があります。