---
title: Project Service Automation から Finance and Operations へのプロジェクト タスクの直接同期
description: このトピックは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance へプロジェクト タスクを直接同期するために使用されるテンプレートと基礎となるタスクについて説明しています。
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079250"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations へのプロジェクト タスクの直接同期

[!include[banner](../includes/banner.md)]

このトピックは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へプロジェクト タスクを直接同期するために使用されるテンプレートと基礎となるタスクについて説明しています。

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。
> - KB 4132657 および KB 4132660 をインストールした後で、Enterprise Edition 7.3.0 を使用している場合は、テンプレートを使用して、プロジェクト タスク、経費トランザクション カテゴリ、時間見積もり、経費見積もり、および実績を統合して機能ロックを設定できます。 勘定配布をリセットする必要がある場合は、サポート情報 4131710 をインストールすることもお勧めします。
> - 実績の統合は、バージョン 8.0.1 以降で使用できます。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation から Finance へのデータ フロー

Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。 データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト タスクに関するデータ フローが可能になります。

次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。

[![Project Service Automation と Finance の統合用データ フロー](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>テンプレートとタスク

テンプレートにアクセスするには、Microsoft Power Apps 管理センターで、 **プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。

以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクト タスクを同期するために使用されます。

- **データ統合のテンプレートの名前:** プロジェクト タスク (PSA から Finance and Operation へ)
- **プロジェクトのタスクの名前:** プロジェクト タスク

プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation | 財務                             |
|----------------------------|-------------------------------------|
| プロジェクト タスク              | プロジェクト タスクの統合エンティティ |

## <a name="entity-flow"></a>エンティティ フロー

プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance に同期されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件とマッピングの設定

プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。

## <a name="power-query"></a>Power Query

この条件が満たされている場合、Microsoft Power Query for Excel を使用してデータをフィルター処理する必要があります。

- プロジェクト タスクにリソース固有のレコードがあります。

Power Query を使用する必要がある場合は、このガイドラインに従ってください。

- プロジェクト タスク (PSA から Finance and Operation へ) テンプレートには、フィルターを **IsLineTask** から **False** に設定することで、プロジェクト タスクからリソース固有のレコードを除外する既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。

## <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。 マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。

[![テンプレート マッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)