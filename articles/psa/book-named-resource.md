---
title: リソース要件で名前付きリソースを予約する。
description: このトピックでは、汎用的なリソース要件における、名前付きリソースの予約について説明します。
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 92a61012beb9aa200f4ea65b777acb0fae04e7e6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590076"
---
# <a name="book-named-resources-from-resource-requirements"></a>リソース要件で名前付きリソースを予約する。

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

名前付きリソースを予約して、リソース要件のある汎用的なリソースを置き換えることができます。

1. Project Service Automation (PSA)の **プロジェクト** ページで、 **チーム** タブをクリックします。
2. リストからリソース要件を保持している汎用的なリソースを選択し、 **予約する** をクリックします。 または、リソース要件を開き、 **予約する** をクリックします。


![汎用チーム メンバーを予約する。](media/RM-how-to-14.png)


3. **スケジュール アシスタント** ページで、プロジェクトチームに登録をする名前付きリソースを選択して、 **予約する** をクリックします。

![スケジュール アシスタントを使用して汎用的なチーム メンバーを予約する。](media/RM-how-to-15.png)

予約が完了し、名前付きリソースが実行されると、汎用リソースがチームから削除され、名前付きリソースに置き換えられます。

![汎用チーム メンバーを置き換える名前付きチーム メンバー。](media/RM-how-to-16.png)

スケジュールの割り当ても同様に名前付きリソースで更新されます。

![プロジェクトのタスクに割り当てられた名前付きチーム メンバー。](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>複数の名前付きリソースで汎用リソースを使用する
複数の名前付きリソースを持つ汎用リソースの要件を満たすことは、単一の名前付きリソースを割り当てることと共通しています。 たとえば、5日間(120時間)の期間を要するタスクがあるとします。 このタスクを完了するには、1日8時間の労働を5日間行う1つのリソースでは足りません。 

![5 日以上で 120 時間の作業が必要なタスク。](media/RM-how-to-21.png)

5日間に渡って自動化技術を120時間稼働させる要件で、これには一日あたり24時間必要となります。

![各日ごとの要件。](media/RM-how-to-22.png)

これは、汎用リソース要求を満たすにあたって、複数の名前付きリソースが必要となる場合の例です。 要件を実現するには複数のリソースを予約する必要があります。

![要件を実現するために複数のリソースを予約する。](media/RM-how-to-23.png)

このシナリオの主な違いは、汎用リソースはタスクに割り当てられたチームに残り、予約された名前付きリソースチームメンバーは職階の一部として割り当てられないことです。 プロジェクト管理者は、指定したリソースに必要に応じて作業を割り当てることができます。 **調整** ビューを使用すると、プロジェクト管理者は複数のリソースからタスクへの割り当てを分割できます。 この処理は自動的には実行されません。要件を構成するタスクのバンドルがある場合や、プロジェクトマネージャが行う割り当ての判断基準など、上記のような単純な例よりも複雑なケースではシステムが想定する必要があるためです。 システムは意図を理解できないため、想定が意図と異なる可能性があり、誤った、または予測できない結果が生じる可能性があります。 予測可能な結果は、プロジェクトマネージャが **調整** ビューのサポートを受けて割り当てを行うまで、汎用的なリソースが割り当てられた状態になることです。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
