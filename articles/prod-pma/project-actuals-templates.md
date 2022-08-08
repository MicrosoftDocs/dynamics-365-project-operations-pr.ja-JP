---
title: 財務と運用に転記するために、Project Service Automation からプロジェクト統合仕訳帳にプロジェクトの実績を直接同期する
description: この記事では、Microsoft Dynamics 365 Project Service Automation から財務と運用にプロジェクト実績を直接同期するために使用されるテンプレートと基になるタスクについて説明します。
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 34a0a0f7277777895077d221cd95e8d962d2a902
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028984"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>財務と運用に転記するために、Project Service Automation からプロジェクト統合仕訳帳にプロジェクトの実績を直接同期する

[!include[banner](../includes/banner.md)]

この記事では、Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト実績を直接同期するために使用されるテンプレートと基になるタスクについて説明します。

テンプレートは、Project Service Automation からのトランザクションを Finance のステージング テーブルに同期します。 同期が完了すると、ステージング テーブルから統合ジャーナルにデータをインポートする **必要** があります。

> [!NOTE]
> - プロジェクト実績の統合は、バージョン 8.0.1 以降で使用できます。
> - KB 4132657 および KB 4132660 をインストールした後で、Enterprise Edition 7.3.0 を使用している場合は、テンプレートを使用してプロジェクト タスク、経費トランザクション カテゴリ、時間見積もり、経費見積もり、および実績を統合して機能ロックを設定できます。 勘定配布をリセットする必要がある場合は、サポート情報 4131710 をインストールすることもお勧めします。
> - バージョン 7.3.0 を使用していて、Project Service Automation から料金のトランザクションを引き継いでいる場合、プロジェクト請求書にこれらの料金を含めるために、KB 4345320 をインストールする必要があります。
> - Project Service Automation にて、時間または費用トランザクションに消費税額を入力する場合は、Project Service Automation Update 7 をインストールする必要があります。 そうでない場合、税の実績は関連する時間または費用の実績にリンクされず、Finance に同期されません。 詳細については Support にお問い合わせください。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation から Finance へのデータ フロー

Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。 データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクトの実績に関するデータ フローが可能になります。

次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。

[![Project Service Automation のデータ フローを財務と運用と統合する。](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation からのプロジェクトの実績

### <a name="template-and-tasks"></a>テンプレートとタスク

利用可能なテンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト** を選択してから、右上隅で **新しいプロジェクト** を選択して公開テンプレートを選択します。

以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へプロジェクトの実績を同期するために使用されます。

- **データ統合のテンプレート名:** プロジェクトの実績 (PSA から Fin および Ops へ)
- **プロジェクトのタスクの名前:**

    - 実績
    - TransactionConnections

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | 財務                                   |
|----------------------------|----------------------------------------------------------|
| 実績                    | プロジェク実績の統合エンティティ                   |
| トランザクション接続    | プロジェクト トランザクションの関連性における統合エンティティ |

### <a name="entity-flow"></a>エンティティ フロー

プロジェクトの実績は、Project Service Automation で管理され、Finance のプロジェクト統合ジャーナルに同期されます。 会計は、デフォルトの財務分析コードと転記設定に基づいて適用されます。

### <a name="prerequisites"></a>前提条件

実績の同期を行う前に、Project Service Automation 統合パラメーターを構成し、プロジェクト、プロジェクト タスク、およびプロジェクト費用トランザクション カテゴリを同期する必要があります。

### <a name="power-query"></a>Power Query

プロジェクト実績テンプレートで、Microsoft Power Query for Excel を使用してこれらのタスクを完了する必要があります:

- Project Service Automation のトランザクション タイプを、Finance の正しいトランザクション タイプに変換します。 この変換は、プロジェクト実績 (PSA から Fin および Ops へ) テンプレートですでに定義されています。
- Project Service Automation の請求タイプを、Finance の正しい請求タイプに変換します。 この変換は、プロジェクト実績 (PSA から Fin および Ops へ) テンプレートですでに定義されています。 次に、請求タイプは明細行プロパティにマップされ、**Project Service Automation 統合パラメーター** ページの設定に基づきます。
- このテンプレートと同期する必要がある特定のリソース組織単位にフィルターします。
- 会社間の時間または会社間の費用の実績が Finance に同期される場合は、契約組織単位を Finance の正しい法人に変換する必要があります。 プロジェクト実績 (PSA から Fin および Ops へ) テンプレートでは、条件付きの列がデモ データに基づいて定義されています。 最後に挿入された条件付き列を正しい法人に更新する必要があります。 そうしないと、統合エラーが発生するか、または誤った実際のトランザクションが Finance にインポートされる可能性があります。
- 会社間の時間または会社間の費用の実績が Finance に同期されない場合は、最後に挿入された条件付き列をテンプレートから削除する必要があります。 そうしないと、統合エラーが発生するか、または誤った実際のトランザクションが Finance にインポートされる可能性があります。

#### <a name="contract-organizational-unit"></a>契約組織の単位
テンプレートで挿入された条件付き列を更新するには、**マップ** 矢印をクリックしてマッピングを開きます。 **高度なクエリおよびフィルター処理** のリンクを選択して、Power Query を開きます。

- 既定のプロジェクト実績 (PSA から Fin and Ops) テンプレートを使用している場合、Power Query で、**適用したステップ** セクションから最後に **挿入された条件** を選択します。 **関数** エントリで、**USSI** を統合で使用する法人名に置き換えます。 必要に応じて、条件を **関数** にエントリに追加し、**USMF** から正しい法人に **他の** 条件を更新します。
- 新しいテンプレートを作成する場合は、会社間の時間と費用をサポートするために列を追加する必要があります。 **条件列の追加** を選択し、**LegalEntity** などの列の名前を入力します。 列の条件 **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null を入力します。

### <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

次の図は、データ統合のテンプレート タスク マッピングの一例を示しています。 マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。

[![テンプレート マッピング - 実績。](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![テンプレート マッピング - トランザクション接続。](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Project Service Automation からの統合後のステージング テーブルからのインポート

ステージング テーブルからの定期的なインポート プロセスは、Project Service Automation から Finance への実績の同期後に実行する必要があります。 このプロセスでは、プロジェクト トランザクションがステージング テーブルから Project Service Automation 統合ジャーナルにインポートされます。ここで、アカウンティングが適用され、インポートされたトランザクションを転記できます。 このプロセスはバッチ モードで実行することをお勧めします。オプションで、定期バッチとして実行するように設定できます。

## <a name="update-actuals-from-finance"></a>Finance からの実績を更新

### <a name="template-and-tasks"></a>テンプレートとタスク

次のテンプレートと基になるタスクを使用して、転記されたプロジェクト トランザクションのバウチャー番号と売上税を、Finance から Project Service Automation に同期します。

- **データ統合のテンプレート名:** プロジェクト実績の更新 (Fin Ops から PSA へ)
- **プロジェクトのタスクの名前:**

    - 実績 
    - TransactionConnections

### <a name="entity-set"></a>エンティティ セット

| 財務                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| プロジェク実績の統合エンティティ                   | 実績                    |
| プロジェクト トランザクションの関連性における統合エンティティ | トランザクション接続    |

### <a name="entity-flow"></a>エンティティ フロー

プロジェクトの実績は、Project Service Automation で管理され、Finance のプロジェクト統合ジャーナルに同期されます。 実績が Finance に転記された後、Project Service Automation にて、Finance からのバウチャー番号を使い更新されます。 売上税が Finance に追加された場合、新しい税の実績が Project Service Automation で作成されます。

### <a name="power-query"></a>Power Query

プロジェクト実績更新テンプレートで、Power Query を使用してこれらのタスクを完了する必要があります:

- Finance のトランザクション タイプを、Project Service Automation で正しいトランザクション タイプに変換します。 この変換は、プロジェクト実績の更新 (Fin Ops から PSA へ) テンプレートですでに定義されています。
- Finance の請求タイプを、Project Service Automation の正しい請求タイプに変換します。 この変換は、プロジェクト実績の更新 (Fin Ops から PSA へ) テンプレートですでに定義されています。

### <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。 マッピングには、Finance から Project Service Automation に同期されるフィールド情報が表示されます。

[![テンプレート マッピング - 実績の更新。](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![テンプレート マッピング - トランザクションの更新。](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]