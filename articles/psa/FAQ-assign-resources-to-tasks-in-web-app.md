---
title: 予約可能なリソースをウェブアプリケーションのタスクに割り当てる方法
description: 予約可能なリソースアサインする方法の概要。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079456"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Web アプリ (Project Service アプリ v2.x) で予約可能なリソースをタスクに割り当てる方法を教えてください。

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Project Service には、リソースをタスクを割り当てる 2 つの方法があります。 リソースをチーム メンバーとして予約し、タスクにリソースを割り当てることができます。 または、タスクでロールの割り当てを通じて汎用チーム メンバーを作成し、チームを生成した後、指定されたリソースを含むバッキング要件を実現できます。

タスクに予約可能リソースを割り当てる場合、予約可能リソース チームのメンバーに十分な予約が必要な点に注意してください。 予約の状態は、[コミットの状態] が [本予約]、[状態] が [確定済み] でなければなりません。 リソースに十分な予約がない場合、Project Service は割り当てを削除して、次のエラー メッセージが表示されます。

*リソースをタスクを割り当てることができません - 次のリソースにはプロジェクトで予約するための十分な時間がありません*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>リソースをチーム メンバーとして予約し、タスクにリソースを割り当てる

この方法では、プロジェクト チームに対してリソースを追加してから、プロジェクト スケジュールでタスクをリソースに割り当てます。 この方法は次のとおりです。
1.  チーム メンバー グリッドで、 **新規作成** を選択してチーム メンバーを追加します。
2.  チーム メンバーのクイック作成画面で、予約可能なリソース名を選択し、ロールを設定します。
3.  **開始** 日と **終了** 日を選択します。

    > [!div class="mx-imgBorder"] 
    > ![チームメンバー追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-1.png "チームメンバー追加のスクリーンショット")
 
4.  リソースを予約する次の割り当て方法の 1 つを選択します。
    - **全キャパシティ** は、指定されている開始日と終了日のリソースの全キャパシティを予約します。
    - **キャパシティの割合** は、指定されている開始日と終了日のリソースのキャパシティの割合でリソースを予約します。
    - **時間別 - 均等分布** は、指定された開始日から終了日まで 1 日あたりに等しく分散して、指定された時間数のリソースを予約します。
    - **時間別 - 前倒し** は、指定された開始日から終了日まで 1 日あたりの前倒し時間で、指定された時間数のリソースを予約します。

    **なし** を選択しないでください。この方法は、チームにリソースを追加しますが、リソースのキャパシティを吸収する予約は作成しません。
5.  **保存** を選びます。

    予約の時間数が、このリソースを割り当てるタスクの工数と日付範囲をカバーするのに十分であることに注意してください。 合っていない場合は、リソースをタスクに割り当てることはできません。

6.  タスクの WBS (作業分解構造) で、リソース セル ドロップダウンをクリックします。 次に、以下の操作を実行します。 

    1. **追加** を選択します。
    2. **リソース** の下でドロップダウンを選択し、上で追加したチーム メンバーを選択します。
    3. **OK** を選びます。 チーム メンバーがタスクに割り当てられました。

    > [!div class="mx-imgBorder"] 
    > ![WBSを使用したリソース追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-2.png "WBSを使用したリソース追加のスクリーンショット")
 
チーム メンバー グリッドの [割り当てられた時間] には、リソースの割り当てられた時間の合計が表示されます。 これは、リソースに予約された時間以内の時間になります。 

> [!div class="mx-imgBorder"] 
> ![リソースに割り当てられた時間のスクリーンショット](media/FAQ-Resources-to-Tasks2-3.png "リソースに割り当てられた時間のスクリーンショット")
 
リソースに割り当てようとしているタスクがリソース予約の終了日より後に始まる場合、リソースはドロップダウンに表示されません。

リソースに未割り当てのキャパシティがある場合、予約された時間より多くの時間をリソースに割り当てることができます。 この場合、リソースの一部分のみその予約に割り当てられます。 WBS (作業分解構造) に [スタッフが配置されていない時間] を追加することで、このような残りの見割り当てタスクを表示できます。

リソースがその予約された時間に割り当てられた場合 (予約された時間は割り当てられた時間と等しい)、さらにタスクを割り当てようとすると次のようなエラー メッセージが表示されます。

*リソースをタスクを割り当てることができません - 次のリソースにはプロジェクトで予約するための十分な時間がありません。*

また、プロジェクトを作成するときにチームに追加された既定のプロジェクト マネージャー プロジェクト チーム メンバーは予約なしで追加され、タスクに割り当てることはできません。 これらは、タスクのリソース ドロップダウンには表示されません。

このリソースを割り当て場合、それらをチームから削除し、[なし] 以外の割り当て方法を使用して再追加する必要があります。 プロジェクトを作成するときにそれらがチームに追加される理由は、プロジェクトに少なくとも 1 人プロジェクト承認者が既定でいるようにするためです。

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>タスクでのロール割り当てを通じた汎用チーム メンバーの作成

この方法では、リソースにタスクの予約が十分にあることを前提としています。 まず、ロールをタスクに割り当てた後に生成することで、最終的にタスクで作業する指定したリソースの特性を示すプレースホルダーまたは汎用リソースを作成します。 この方法は次のとおりです。

1. WBS (作業分解構造) で、タスクを選択します。
2. リソース セルの **割り当てられたロール** ドロップダウン アイコンを選択します。
3. **ロール** ドロップダウンを選択し、汎用リソースのロールを選択します。
4. **OK** を選びます。

    > [!div class="mx-imgBorder"] 
    > ![WBSを使用したリソースの追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-4.png "WBSを使用したリソースの追加のスクリーンショット")
 
WBS でタスクへロールの割り当てを完了したら、 **プロジェクト チームの生成** を選択します。 Project Service では、タスクの割り当てを集計することで、ロール、リソース組織単位、およびプロジェクトの予定表に基づいて汎用チーム メンバーの最小数が作成されます。

> [!div class="mx-imgBorder"] 
> ![プロジェクトチームの生成のスクリーンショット](media/FAQ-Resources-to-Tasks2-5.png "プロジェクトチームの生成のスクリーンショット")
 
チーム メンバー グリッドでは、汎用リソースの種類のリソースが、ロールとポジション名と共に表示されます。 ロールが作業を完了するために 2 つのリソースが必要な場合、チームの生成機能は 2 名のチーム メンバーを作成し、ポジション名を使用してそれらを別々に設定します。

> [!div class="mx-imgBorder"] 
> ![2つの汎用リソース追加のスクリーンショット](media/FAQ-Resources-to-Tasks2-6.png "2つの汎用リソース追加のスクリーンショット")
 
リソース要件の下のリンクを選択すると、汎用チーム メンバーのバッキング リソース要件を開くことができます。

> [!div class="mx-imgBorder"] 
> ![関連するリソースの要件を起動するスクリーンショット](media/FAQ-Resources-to-Tasks2-7.png "関連するリソースの要件を起動するスクリーンショット")

汎用リソースの **予約** を選択した後、実質のリソースの検索と予約にスケジュール ボードを使用できます。 また、 **要求の送信** を選択することで、リソース マネージャーによって実行するための要件を送信することもできます。

指定されたリソースによって汎用リソースが実行されると、汎用リソースがチームから削除され、汎用リソースのタスク割り当ては汎用リソースのリソース要件を実行したリソースに割り当てられます。
 
