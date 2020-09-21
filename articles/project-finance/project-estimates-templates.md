---
title: Project Service Automation から Finance and Operations へのプロジェクト見積もりの直接同期
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト時間の見積もりおよびプロジェクト経費の見積もりを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752844"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations へのプロジェクト見積もりの直接同期

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト時間の見積もりおよびプロジェクト経費の見積もりを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。
> - 実績の統合は、バージョン 8.0.1 以降で使用できます。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation から Finance へのデータ フロー

Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。 データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト時間の見積もりおよびプロジェクト経費の見積もりに関するデータのフローが可能になります。

次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。

[![Finance との Project Service Automation 統合用データ フロー](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>プロジェクト時間の見積もり

### <a name="template-and-tasks"></a>テンプレートとタスク

利用可能なテンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト**を選択してから、右上隅で**新しいプロジェクト**を選択して公開テンプレートを選択します。

以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト時間の見積もりを同期するために使用されます。

- **データ統合のテンプレートの名前:** プロジェクト時間の見積もり (PSA から Finance and Operation へ)
- **プロジェクトのタスクの名前:**

    - トランザクションの関連付け
    - 経費の見積もり

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | 財務                                       |
|----------------------------|-----------------------------------------------|
| プロジェクト タスク              | プロジェクト時間の見積もりの統合エンティティ |

### <a name="entity-flow"></a>エンティティ フロー

プロジェクト時間の見積もりは Project Service Automation で管理され、プロジェクト時間の予測として Finance に同期されます。

### <a name="prerequisites"></a>前提条件

プロジェクト時間の見積もりを同期する前に、プロジェクト、プロジェクト タスク、およびプロジェクト経費のトランザクション カテゴリを同期する必要があります。

### <a name="power-query"></a>Power Query

プロジェクト時間の見積もりテンプレートでは、Microsoft Power Query for Excel を使用して次のタスクを完了する必要があります。

- 統合が新しい時間予測を作成するときに使用される既定の予測モデル ID を設定します。
- 時間予測への統合に失敗するタスクで、リソース固有の任意のレコードを除外します。
- 空のトランザクション カテゴリ行をすべて除外します。 このタスクを完了しないと、時間予測が不正確になる可能性があります。

#### <a name="set-the-default-forecast-model-id"></a>既定の予測モデル ID の設定

テンプレートで既定の予測モデル ID を更新するには、**マップ**矢印をクリックしてマッピングを開きます。 次に、**高度なクエリとフィルター処理**リンクを選択します。

- 既定のプロジェクト時間の見積もり (PSA から Finance and Operation へ) テンプレートを使用している場合は、**適用したステップ**の一覧で**挿入した条件**を選択します。 **関数**エントリで、**O\_forecast** を統合で使用する予測モデル ID の名前に置き換えます。 既定のテンプレートには、デモ データからの予測モデル ID があります。
- 新しいテンプレートを作成する場合は、この列を追加する必要があります。 Power Query で、**条件列の追加**を選択し、**ModelID** などの新しい列の名前を入力します。 列の条件を入力します。プロジェクト タスクが null でない場合は、\<予測モデル ID を入力\>します; それ以外の場合は null です。

#### <a name="filter-out-resource-specific-records"></a>リソース固有のレコードを除外する

プロジェクト時間の見積もり (PSA から Finance and Operation へ) テンプレートには、リソース固有のレコードを削除する既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。 **msdyn\_islinetask** 列でフィルター処理する**高度なクエリとフィルター処理**リンクを選択して、**False** レコードのみが含まれるようにします。

#### <a name="filter-out-empty-transaction-category-rows"></a>空のトランザクション カテゴリ行を除外する

フィルターを追加して、空のトランザクション カテゴリがある行をすべて削除する必要があります。 既定のテンプレートを使用しているか、または独自のテンプレートを作成しているかどうかに関係なく、このタスクは必要です。 このフィルターは Project Service Automation から概要行をすべて削除します。これにより、Finance の時間予測が不正確になる可能性があります。 **高度なクエリとフィルー処理**リンクを選択して、**msdyn\_transactioncategory\_value** 列で null レコードを除外します。

### <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。 マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。

[![テンプレート マッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>プロジェクト経費の見積もり

### <a name="template-and-tasks"></a>テンプレートとタスク

以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト経費の見積もりを同期するために使用されます。

- **データ統合のテンプレートの名前:** プロジェクト経費の見積もり (PSA から Finance and Operation へ)
- **プロジェクトのタスクの名前:**

    - トランザクションの関連付け 
    - 経費の見積もり

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | 財務                                                  |
|----------------------------|----------------------------------------------------------|
| トランザクション接続    | プロジェクト トランザクションの関連性における統合エンティティ |
| 見積行             | プロジェクト経費の見積もりの統合エンティティ         |

### <a name="entity-flow"></a>エンティティ フロー

プロジェクト経費の見積もりは Project Service Automation で管理され、プロジェクト経費の予測として Finance に同期されます。

### <a name="prerequisites"></a>前提条件

プロジェクト経費の見積もりを同期する前に、プロジェクト、プロジェクト タスク、およびプロジェクト経費のトランザクション カテゴリを同期する必要があります。

### <a name="power-query"></a>Power Query

プロジェクト経費の見積もりテンプレートでは、Power Query を使用して次のタスクを完了する必要があります。

- 経費見積行レコードのみを含めるようにフィルター処理します。
- 統合が新しい時間予測を作成するときに使用される既定の予測モデル ID を設定します。
- 請求タイプを変換します。
- トランザクション タイプを変換します。

#### <a name="filter-to-include-only-expense-estimate-lines"></a>経費見積品目のみを含めるようにフィルター処理します

プロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートには、統合に経費品目のみを含む既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。 **トランザクションの関連付け**タスクを選択してから、**マップ**矢印をクリックしてマッピングを開きます。 **高度なクエリとフィルター処理**リンクを選択します。 **msdyn\_transactiontype1** 列をフィルター処理して、**msdyn\_estimateline** のみが含まれるようにします。

#### <a name="set-the-default-forecast-model-id"></a>既定の予測モデル ID の設定

テンプレートで既定の予測モデル ID を更新するには、**経費の見積もり**タスクを選択してから、**マップ**矢印をクリックしてマッピングを開きます。 **高度なクエリとフィルター処理**リンクを選択します。

- 既定のプロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートを使用している場合は、Power Query で、**適用したステップ** セクションから最初に**挿入した条件**を選択します。 **関数**エントリで、**O\_forecast** を統合で使用する予測モデル ID の名前に置き換えます。 既定のテンプレートには、デモ データからの予測モデル ID があります。
- 新しいテンプレートを作成する場合は、この列を追加する必要があります。 Power Query で、**条件列の追加**を選択し、**ModelID** などの新しい列の名前を入力します。 列の条件を入力します。見積品目 ID が null でない場合は、\<予測モデル ID を入力\>します; それ以外の場合は null です。

#### <a name="transform-the-billing-types"></a>請求タイプを変換する

プロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートには、統合中に Project Service Automation から受け取る請求タイプを変換するために使用する条件列が含まれます。 独自のテンプレートを作成する場合は、この条件列を追加する必要があります。 **高度なクエリとフィルター処理**リンクを選択してから、**条件列の追加**を選択します。 **BillingType** などの新しい列の名前を入力します。 次に以下の条件を入力します:

**msdyn\_billingtype** = 192350000 の場合、**NonChargeable**  
**msdyn\_billingtype** = 192350001 の場合、**請求可能**  
**msdyn\_billingtype** = 192350002 の場合、**無料**  
それ以外は **NotAvailable**

#### <a name="transform-the-transaction-types"></a>トランザクション タイプを変換する

プロジェクト経費の見積もり (PSA から Finance and Operation へ) テンプレートには、統合中に Project Service Automation から受け取るトランザクション タイプを変換するために使用する条件列が含まれます。 独自のテンプレートを作成する場合は、この条件列を追加する必要があります。 **高度なクエリとフィルター処理**リンクを選択してから、**条件列の追加**を選択します。 **TransactionType** などの新しい列の名前を入力します。 次に以下の条件を入力します:

**msdyn\_transactiontypecode** = 192350000 の場合、**コスト**  
**msdyn\_transactiontypecode** = 192350005 の場合、**営業**  
それ以外は **null**

### <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。 マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。

[![テンプレート マッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![テンプレート マッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
