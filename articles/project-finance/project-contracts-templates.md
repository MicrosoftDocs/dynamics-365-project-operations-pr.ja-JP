---
title: Project Service Automation から Finance and Operations へのプロジェクト契約およびプロジェクトの直接同期
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト契約およびプロジェクトを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752806"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations へのプロジェクト契約およびプロジェクトの直接同期

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance へのプロジェクト契約およびプロジェクトを直接同期するために使用されるテンプレートと基礎となるタスクについて説明します。

> [!NOTE] 
> Enterprise Edition 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation から Finance へのデータ フロー

> [!NOTE]
> Project Service Automation から Finance への統合ソリューションを使用する前に、Dynamics 365 のデータ統合機能に精通している必要があります。

Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Project Service Automation および Finance のインスタンス間でデータを同期します。 データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト契約、プロジェクト、プロジェクト契約品目、およびプロジェクト契約品目のマイルストーンについてのデータのフローが可能になります。

次の図は、Project Service Automation と Finance 間でデータを同期する方法を示します。

[![Finance との Project Service Automation 統合用データ フロー](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、Microsoft Power Apps 管理センターで、**プロジェクト**を選択してから、右上隅で**新しいプロジェクト**を選択して公開テンプレートを選択します。

以下のテンプレートおよび基礎となるタスクは、Project Service Automation から Finance へのプロジェクト契約およびプロジェクトを同期するために使用されます。

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Dynamics 365 Project Service Automation v2.x との統合
- **データ統合のテンプレートの名前:** プロジェクトおよび契約 (PSA から Finance and Operation へ)
- **プロジェクトのタスクの名前:**

    - PSA から Finance and Operation へのプロジェクト契約
    - PSA から Finance and Operation へのプロジェクト
    - PSA から Finance and Operation へのプロジェクト契約品目
    - PSA から Finance and Operation へのプロジェクト契約品目のマイルストーン
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Dynamics 365 Project Service Automation v3.x との統合
Project Service Automation にはスキーマの変更があり、プロジェクト契約品目のマイルストーン テンプレートに影響します。ProjectService Automation v3.x を Dynamics 365 と統合するには、テンプレートの v2 バージョンを使用する必要があります。

- **データ統合のテンプレートの名前:** プロジェクトおよび契約 (PSA 3.x から Finance and Operation へ) - v2
- **プロジェクトのタスクの名前:**

    - PSA から Finance and Operation へのプロジェクト契約
    - PSA から Finance and Operation へのプロジェクト
    - PSA から Finance and Operation へのプロジェクト契約品目
    - PSA から Finance and Operation へのプロジェクト契約品目のマイルストーン

プロジェクト契約およびプロジェクトの同期を行う前に、アカウントを同期する必要があります。

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation       | 財務                                                |
|----------------------------------|--------------------------------------------------------|
| 受注                           | プロジェク契約の統合エンティティ                |
| プロジェクト                         | プロジェクトの統合エンティティ                         |
| 受注明細行                      | プロジェク契約品目の統合エンティティ           |
| プロジェクト契約品目のマイルストーン | プロジェク契約品目のマイルストーンの統合エンティティ |

## <a name="entity-flow"></a>エンティティ フロー

プロジェクト契約は Project Service Automation で管理され、プロジェクト契約として Finance に同期されます。 統合テンプレートの一部として、プロジェクト契約の統合ソースを Finance で設定できます。

時間/実費払プロジェクトおよび固定価格プロジェクトは Project Service Automation で管理され、プロジェクトとして Finance に同期されます。 テンプレート統合の一部として、プロジェクトの統合ソースを Finance で設定できます。

プロジェクト契約品目は Project Service Automation で管理され、プロジェクト契約の請求ルールとして Finance に同期されます。 請求方法が既定のプロジェクト タイプと異なる場合、同期により、契約品目プロジェクトとプロジェクト グループのプロジェクト タイプが更新されます。

プロジェクト契約品目のマイルストーンは Project Service Automation で管理され、プロジェクト契約の請求ルール マイルストーンとして Finance に同期されます。

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation から Finance への統合ソリューション

**プロジェクト契約 ID** フィールドは、**プロジェクト契約**ページで利用可能です。 このフィールドは、統合をサポートするための自然で一意のキーになっています。

新しいプロジェクト契約が作成されると、**プロジェクト契約 ID** 値がまだ存在しない場合、番号順序を使用して自動的に生成されます。 値は **ORD** から成り、番号順序が増分し、その後に 6 文字の接尾辞が続きます。 次に例を示します: **ORD-01022-Z4M9Q0**。

**プロジェクト番号**フィールドは、**プロジェクト** ページで利用可能です。 このフィールドは、統合をサポートするための自然で一意のキーになっています。

新しいプロジェクトが作成されると、**プロジェクト番号**値がまだ存在しない場合、番号順序を使用して自動的に生成されます。 値は **PRJ** から成り、番号順序が増分し、その後に 6 文字の接尾辞が続きます。 次に例を示します: **PRJ-01049-CCNID0**。

Project Service Automation から Finance への統合ソリューションが適用されると、アップグレード スクリプトにより、既存のプロジェクト契約の**プロジェクト契約 ID** フィールド、および Project Service Automation の既存のプロジェクトの**プロジェクト番号**フィールドが設定されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件とマッピングの設定

- プロジェクト契約およびプロジェクトの同期を行う前に、アカウントを同期する必要があります。
- 接続設定で、**msdyn\_organizationalunits** から**msdyn\_name\[名前\]** への統合キー フィールドのマッピングを追加します。 最初にプロジェクトを接続設定に追加する必要があるかもしれません。 詳細については、[アプリ用 Common Data Service へのデータの統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)を参照してください。
- 接続設定で、**msdyn\_projects** から**msdynce\_projectnumber\[プロジェクト番号\]** への統合キー フィールドのマッピングを追加します。 最初にプロジェクトを接続設定に追加する必要があるかもしれません。 詳細については、[アプリ用 Common Data Service へのデータの統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)を参照してください。
- プロジェクト契約およびプロジェクトの **SourceDataID** は、別の値に更新したり、マッピングから削除したりできます。 既定のテンプレート値は **Project Service Automation** です。
- **PaymentTerms** マッピングは、Finance の有効な支払条件を反映するように更新する必要があります。 プロジェクト タスクからマッピングを削除することもできます。 既定値マップには、デモ データの既定値があります。 次の表は、Project Service Automation の値を示します。

    | Value | 内容   |
    |-------|---------------|
    | 6     | 支払期限 30 日以内        |
    | 2     | 10 日以内支払割引 2%、支払期限 30 日以内 |
    | 3     | 支払期限 45 日以内        |
    | 4     | 支払期限 60 日以内        |

## <a name="power-query"></a>Power Query

次の条件が満たされている場合、Microsoft Power Query for Excel を使用してデータをフィルター処理する必要があります。

- Dynamics 365 Sales に受注があります。
- Project Service Automation に複数の組織単位があり、これらの組織単位は Finance の複数の法人にマップされます。

Power Query を使用する必要がある場合は、これらのガイドラインに従ってください。

- プロジェクトと契約 (PSA から Finance and Operation) テンプレートには既定のフィルターがあり、**作業項目 (msdyn\_ordertype = 192350001)** タイプの受注のみが含まれます。 このフィルターは、プロジェクト契約が Finance の受注に対して作成されないことを保証するのに役立ちます。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。
- 統合接続設定の法人に同期する必要がある契約組織のみを含む Power Query フィルターを作成する必要があります。 たとえば、Contoso US の契約組織単位とのプロジェクト契約は USSI 法人に同期する必要がありますが、Contoso グローバルの契約組織単位とのプロジェクト契約は USMF 法人に同期する必要があります。 このフィルターをタスク マッピングに追加しない場合、契約組織単位に関係なく、すべてのプロジェクト契約が接続設定に定義されている法人に同期されます。

## <a name="template-mapping-in-data-integration"></a>データ統合におけるテンプレート マッピング

> [!NOTE] 
> **CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、 **AddressLine2**、**AddressState**、および **AddressZipCode** フィールドは、プロジェクト契約の既定マッピングには含まれません。 このデータをプロジェクト契約で同期する必要がある場合は、マッピングを追加できます。
>
> **Description**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber**、および **ProjectType** フィールドは、プロジェクトの既定マッピングには含まれません。 このデータをプロジェクトで同期する必要がある場合は、マッピングを追加できます。

次の図は、データ統合のテンプレート タスク マッピングの例を示しています。 マッピングには、Project Service Automation から Finance に同期されるフィールド情報が表示されます。

[![テンプレート マッピング](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![テンプレート マッピング](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![テンプレート マッピング](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![テンプレート マッピング](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>プロジェクトおよび契約におけるプロジェクト契約品目のマイルストーン マッピング (PSA 3.x から Dynamics へ) - v2 テンプレート:

[![テンプレート マッピング](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
