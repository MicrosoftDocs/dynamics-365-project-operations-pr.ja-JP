---
title: スケジュール アシスタントの概要
description: このトピックは、スケジュール アシスタントを使用してリソースを予約する方法を説明します。
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: d2146e959119a78a27927b9e694474b3f04579fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585936"
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
-   ロール
-   部署
-   リソースの基本設定
-   工数コントー
-   タイム ゾーン

スケジュール アシスタントは、これらの詳細を使用してリソースをフィルター処理します。

## <a name="launch-the-schedule-assistant"></a>スケジュール アシスタントを起動します

スケジュール アシスタントを起動する方法は 2 つあります。 ハイブリッド モードを使用している場合、チーム メンバー グリッドで、未対応のリソース要件がチーム メンバーを選択してから、**予約** を選択します。 セントラル モードを使用している場合、リソース管理者はリソースを検索および選択します。

## <a name="schedule-assistant-filters"></a>スケジュール アシスタント フィルター

スケジュール アシスタントの実行後、リソース要件の詳細が左側のウィンドウにフィルター処理された値として表示されます。 リソース管理者またはプロジェクト管理者は、スケジュールのニーズに合わせてフィルターを調整することにより、結果を微調整できます。

フィルター ウィンドウには、次のような作業関連のオプションが表示されます。

-   作業の開始と終了
-   特性
-   ロール
-   組織単位
-   調達先の会社
-   リソースの種類
-   優先するリソース


[!INCLUDE[footer-include](../includes/footer-banner.md)]