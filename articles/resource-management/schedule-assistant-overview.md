---
title: スケジュール アシスタントの概要
description: このトピックは、スケジュール アシスタントを使用してリソースを予約する方法を説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079124"
---
# <a name="schedule-assistant-overview"></a>スケジュール アシスタントの概要

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

スケジュール アシスタントは、プロジェクト管理者によって定義された要件に基づいてリソースを予約するために使用されます。 スケジュール アシスタントは、リソース要件で提供されるパラメーターに依存してリソースを検索します。 スケジュール アシスタントは、時間枠や必要なスキルなど、関連する要件に一致するリソースを推奨します。

適切なリソースが特定されたら、リソース管理者またはプロジェクト管理者はリソースを作業に予約できます。

## <a name="prerequisites"></a>前提条件

スケジュール アシスタントは Universal Resource Scheduling ソリューションの一部です。 このソリューションは、Dynamics 365 Project Operations、Dynamics 365 Field Service、および Dynamics 365 Customer Service に含まれ、インストールされています。

## <a name="matching-requirements-and-resources"></a>要件とリソースの一致

生成されたリソース要件は、次のような詳細に基づいています。

-   特性
-   役割
-   部署
-   リソースの基本設定
-   工数コントー
-   タイム ゾーン

スケジュール アシスタントは、これらの詳細を使用してリソースをフィルター処理します。

## <a name="launch-the-schedule-assistant"></a>スケジュール アシスタントを起動します

スケジュール アシスタントを起動する方法は 2 つあります。 ハイブリッド モードを使用している場合、チーム メンバー グリッドで、未対応のリソース要件がチーム メンバーを選択してから、 **予約** を選択します。 セントラル モードを使用している場合、リソース管理者はリソースを検索および選択します。

## <a name="schedule-assistant-filters"></a>スケジュール アシスタント フィルター

スケジュール アシスタントの実行後、リソース要件の詳細が左側のウィンドウにフィルター処理された値として表示されます。 リソース管理者またはプロジェクト管理者は、スケジュールのニーズに合わせてフィルターを調整することにより、結果を微調整できます。

フィルター ウィンドウには、次のような作業関連のオプションが表示されます。

-   作業の開始と終了
-   特性
-   役割
-   組織単位
-   リソース会社
-   リソースの種類
-   優先するリソース
