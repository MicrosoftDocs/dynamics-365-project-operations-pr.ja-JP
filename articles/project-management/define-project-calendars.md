---
title: プロジェクト カレンダーの定義
description: このトピックでは、プロジェクト カレンダーを使用してプロジェクトのスケジュールを追跡する方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286974"
---
# <a name="define-project-calendars"></a>プロジェクト カレンダーの定義

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

プロジェクト スケジュールを作成するには、1 日分に対応する作業時間数と休業日を定義するプロジェクト カレンダー テンプレートを作成します。 プロジェクトのカレンダー テンプレートを作成するには、プロジェクトの **カレンダー テンプレート** フィールドで、作業テンプレートを関連付けます。 作業テンプレートを作成するには、次の手順に従います。

1. 左側のナビゲーション ウィンドウで、**リソース** を選択します。 
2. **リソース** リスト ページで、ユーザー レコードを開き、**作業時間を表示する** を選択します。

  > [!NOTE]
  > ブラウザー ページでポップアップを許可していることを確認してください。 これにより、そのリソースに設定された作業時間が表示されます。
  
3. **月次ビュー** タブで、**設定** を選択します。 次の 3 つのオプションが表示されます。 

  - 新しい週単位のスケジュール
  - 1 日の作業スケジュール
  - 休暇

4. **新規週単位スケジュール** を選択し、このリソース スケジュールのオプションを設定します。 定期的な週単位のスケジュール、毎日の時間パラメーター、休業日の設定などを設定できます。
5. 日付の範囲を設定して、**保存** を選択し、**閉じる** を選択します。 
6. **リソース** リストページへ戻り、作業時間のために設定するリソースを選択します。 
7. 作業テンプレートを設定するには、**カレンダーを次のとおり設定** を選択します。 
8. **作業テンプレート** ダイアログ ボックスで、作業テンプレートの名前を入力し、**適用** を選択します。 

ここで、プロジェクトのカレンダー テンプレートがある作業テンプレートを関連付けることができます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]