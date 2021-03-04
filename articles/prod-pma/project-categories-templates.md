---
title: プロジェクト経費カテゴリを Finance and Operations と Project Service Automation 間で同期する
description: このトピックは、Microsoft Dynamics 365 Finance と Dynamics 365 Project Service Automation 間でプロジェクト経費カテゴリを直接同期するために使用されるテンプレートおよび基礎となるタスクについて説明しています。
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079407"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>プロジェクト経費カテゴリを Finance and Operations と Project Service Automation 間で同期する

[!include[banner](../includes/banner.md)]

このトピックは、Dynamics 365 Finance と Dynamics 365 Project Service Automation 間でプロジェクト経費カテゴリを直接同期するために、使用されるテンプレートおよび基礎となるタスクについて説明しています。

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。
> - 実績の統合は、バージョン 8.0.1 以降で使用できます。
> - KB 4132657 および KB 4132660 をインストールした後で、Enterprise Edition 7.3.0 を使用している場合は、テンプレートを使用して、プロジェクト タスク、経費トランザクション カテゴリ、時間見積もり、経費見積もり、および実績を統合して機能ロックを設定できます。 勘定配布をリセットする必要がある場合は、サポート情報 4131710 をインストールすることもお勧めします。

## <a name="data-flow-for-project-service-automation-and-finance"></a>Project Service Automation と Finance のデータ フロー

Project Service Automation と Finance の統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。 データ統合機能で使用可能な統合テンプレートを使用すると、Finance と Project Service Automation 間のプロジェクト経費トランザクションに関するデータのフローが可能になります。

プロジェクト経費カテゴリが Finance で習得されている場合、統合フローは最初 Finance から Project Service Automation までです。 そして、プロジェクト経費カテゴリの統合 ID が Project Service Automation から Finance へ同期によって更新されます。

プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初 Project Service Automation から Finance までです。 プロジェクト カテゴリは、Project Service Automation から同期する前に、Finance で既に構成されている必要があります。 その後、Finance から Project Service Automation に戻り同期を実行し、Project Service Automation から Finance に再度同期します。 このようにして、カテゴリがリンクされ、重複が作成されないことを保証するのに役立ちます。

> [!NOTE]
> 通常、プロジェクト経費カテゴリは Finance で習得されます。 ただし、そうでない場合、または経費カテゴリが既に Project Service Automation で作成されている場合は、最初にプロジェクト経費トランザクション カテゴリ (PSA から Fin および Ops へ) テンプレートを使用して同期する必要があります。 そして、プロジェクト経費トランザクション カテゴリ (Fin および Ops から PSA へ) テンプレートを使用して同期します。 その後、もう一度 Project Service Automation から Finance へ同期を実行する必要があります。
>
> 最初に Project Service Automation から同期する場合、同期を実行する前に、Finance で次の要件を満たしている必要があります。
>
> - Project Service Automation で設定されているプロジェクト カテゴリと一致する共有カテゴリが存在し、 **プロジェクト** と **経費** の両方で有効になっている必要があります。
> - 統合する必要がある Finance の法人ごとに、次のプロジェクト カテゴリが存在する必要があります。
>
>     - **プロジェクト カテゴリー** は存在します。 
>     - **経費での使用** が有効になっています。
>     - **ジャーナルでアクティブ** が有効になっています。
>     - **トランザクション タイプ** が **経費** に設定されています。

次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。

[![Finance を使用した Project Service Automation 統合用データ フロー](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>プロジェクト経費カテゴリを Finance と Project Service Automation 間で同期

### <a name="template-and-task"></a>テンプレートとタスク

テンプレートにアクセスするには、Microsoft Power Apps 管理センターで、 **プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。

以下のテンプレートおよび基礎となるタスクは、Finance から Project Service Automation へプロジェクト経費カテゴリを同期するために使用されます。

- **データ統合のテンプレートの名前:** プロジェクト経費カテゴリ (Fin と Ops から PSA へ)
- **プロジェクトのタスク名:** カテゴリを PSA に同期

### <a name="entity-set"></a>エンティティ セット

| 財務                           | Project Service Automation |
|-----------------------------------|----------------------------|
| カテゴリの統合エンティティ | トランザクション カテゴリ     |

### <a name="entity-flow"></a>エンティティ フロー

プロジェクト経費カテゴリは Finance で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。

### <a name="power-query"></a>Power Query

Project Service Automation に同期する場合は、Microsoft Power Query for Excel を使用して、トランザクション カテゴリに請求タイプを設定する必要があります。 プロジェクト経費のトランザクション カテゴリ (Fin と Ops から PSA へ) テンプレートは、デフォルトの列とマッピングを提供します。 独自のテンプレートを作成する場合は、Power Query に条件列を追加する必要があります。 次の手順を実行します。

1. 矢印をクリックして、プロジェクト経費トランザクション カテゴリ (Fin と Ops から PSA へ) テンプレートで、プロジェクト経費カテゴリ タスクのマッピングを開きます。
2. **高度なクエリとフィルター処理** リンクをクリックして、Power Query を開きます。
2. **条件付き列を追加** を選択します。
3. **BillingType** などの新しい列の名前を入力します。
4. 次の条件を入力します: **CATEGORYID が null と等しくない場合は 19235001、そうでない場合は null** 。
5. 列で **OK** をクリックします。
6. この新しい列をマッピング ページに必ずマッピングしてください。

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。 マッピングには、Finance から Project Service Automation に同期されるフィールド情報が表示されます。

[![プロジェクト経費カテゴリから Project Service Automation へのテンプレート マッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>プロジェクト経費カテゴリを Project Service Automation から Finance へ同期

### <a name="template-and-task"></a>テンプレートとタスク

以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト経費カテゴリを同期するために使用されます。

- **データ統合のテンプレートの名前:** プロジェクト経費カテゴリ (PSA から Fin と Ops へ)
- **プロジェクトのタスク名:** カテゴリを Fin Ops に同期

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | 財務                           |
|----------------------------|-----------------------------------|
| トランザクション カテゴリ     | カテゴリの統合エンティティ |

### <a name="entity-flow"></a>エンティティ フロー

プロジェクト経費カテゴリは Finance で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。 Finance に戻った同期により、Project Service Automation からの統合 ID で Finance のプロジェクト カテゴリを更新されます。

### <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。

> [!NOTE]
> マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。

[![Project Service Automation から Finance へのテンプレート マッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]