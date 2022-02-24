---
title: Project Operations のセットアップと構成データの統合
description: このトピックでは、Project Operations 二重書き込みマッピングの設定および構成についての情報を提供します。
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939006"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations のセットアップと構成データの統合

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、Project Operations の設定と構成エンティティの二重書き込み統合に関する情報を提供します。

## <a name="project-contracts-contract-lines-and-projects"></a>プロジェクト契約、契約品目、プロジェクト

プロジェクト契約、契約品目、プロジェクトは、Dataverse で作成され、追加の会計のために Finance and Operations アプリに同期されます。 これらのエンティティのレコードは、Dataverseでのみ作成、削除できます。 しかし、消費税のグループの既定値や財務分析コードなどの会計属性は、Finance and Operations アプリでこれらのレコードに追加することができます。

  ![プロジェクト契約統合の概念](./media/1ProjectContract.jpg)

営業活動のリード、営業案件、見積もりは Dataverse で追跡され、この活動に関連するダウンストリームの会計がないため Finance and Operations のアプリには同期されません。

Dataverse のプロジェクト契約機能では、**プロジェクト契約ヘッダー (salesorders)** のテーブルマッピングを使って Finance and Operations アプリにプロジェクト契約のレコードを作成します。 Dataverse でプロジェクト契約を保存すると、プロジェクト契約の顧客エンティティ レコードの作成が開始されます。 このレコードは、**プロジェクトの資金源 (msdyn\_projectcontractssplitbillingrules)** テーブル マッピングを使って Finance and Operations のアプリに同期しています。 このマッピングは、プロジェクト契約の顧客の追加、更新、削除を同期します。 プロジェクト契約の顧客間での分割請求のパーセンテージは、Dataverse でのみ管理され、Finance and Operations のアプリには同期されません。

Dataverse でプロジェクト契約を作成した後、プロジェクト担当者は **プロジェクト管理と会計** > **プロジェクト契約** > **設定** > **既定の会計を表示** にアクセスして Finance and Operations アプリでこのプロジェクト契約の会計属性を更新することができます。 経理担当者は、Finance and Operations アプリでプロジェクト契約 ID を選択し、Dataverse アプリで関連するプロジェクト契約レコードを開くことで、要められる納期や契約金額など、運用中のプロジェクト契約の属性を確認することができます。

プロジェクト エンティティは、**Projects V2 (msdyn\_projects)** テーブル マッピングを使用して Finance and Operations アプリに同期されます。 プロジェクト会計士は次のことができます:

  - Finance and Operations アプリでプロジェクトを確認するには、**プロジェクト管理と会計** > **すべてのプロジェクト** にアクセスします。 
  - **プロジェクト管理と会計** > **すべてのプロジェクト** > **設定** > **既定の会計を表示する** にアクセスし、Finance and Operations アプリのプロジェクトの会計属性を更新します。  
  - プロジェクトの開始予定日や終了予定日など、運用中のプロジェクトの属性を確認するには、Finance and Operations アプリでプロジェクト ID を選択し、Dataverse アプリで関連するプロジェクトのレコードを開きます。

プロジェクトには、**プロジェクトの契約品目** エンティティを通じてプロジェクト契約が関連付けられています。

Dataverse のプロジェクト契約品目は、**プロジェクト契約品目 (salesorderdetails)** のテーブル マッピングを使用して Finance and Operations アプリにプロジェクト契約の請求ルールを作成します。 請求方法は、Finance and Operations アプリのプロジェクト契約の課金ルールタイプを定義します:

  - 課金方法が時間と材料となっているプロジェクト契約品目は、時間と材料タイプの課金ルールを作成します。
  - 固定価格課金方式の契約品目では、マイルストーン課金のルールを作成します。

プロジェクトの契約品目は、プロジェクトの会計担当者が Finance and Operations アプリで **プロジェクト管理と会計** > **プロジェクト契約** > **設定** > **既定の会計を表示する** にアクセスし、**契約品目** タブで詳細を確認することで確認できます。会計担当者は、このタブで固定価格請求方式の契約ラインに既定の財務分析コードを設定することもできます。

## <a name="billing-milestones"></a>請求のマイルストーン

固定価格での請求方法を採用しているプロジェクト契約品目は、請求のマイルストーンを通じて請求されます。 請求のマイルストーンは、**Project Operations 統合の契約品目マイルストーン (msdyn\_contractlinescheduleofvalues)** テーブル マッピングを使用して、Finance and Operations アプリのプロジェクトの当座預金トランザクションに同期します。

  ![請求マイルストーンの統合](./media/2Milestones.jpg)

経理担当者は、当座預金取引を確認し、その取引の会計属性を調整するには、**プロジェクト管理と会計** > **プロジェクト契約** > **管理** > **当座預金取引** または **プロジェクト管理と会計** > **すべてのプロジェクト** > **管理** > **当座預金取引** にアクセスします。

特定のプロジェクト契約ラインの請求マイルストーンを最初に作成すると、システムはこの契約品目に関連付けられたプロジェクトの固定価格収益見積もりプロジェクトを自動的に作成します。 固定価格制の収益見積プロジェクトは、**プロジェクト管理と会計** > **固定価格の収益見積もりプロジェクト** にアクセスして確認することができます。

### <a name="project-tasks"></a>プロジェクト タスク

プロジェクトのタスクは、参照用の **プロジェクト タスク (msdyn\_projecttasks)** テーブル マッピングを通じて、Finance and Operations アプリに同期されます。 Finance and Operations アプリでは、作成、更新、削除の操作には対応していません。

  ![プリジェクト タスクの統合](./media/3Tasks.jpg)

## <a name="project-resources"></a>プロジェクト リソース

**プロジェクト リソースの役割** のエンティティは、参照用にFinance and Operations のテーブルマッピングを使って **すべての会社のプロジェクトリソースの役割 (bookableresourcecategories)** のアプリと同期しています。 Dataverse のリソースの役割は会社固有のものではないため、システムは、二重書きの統合範囲に含まれるすべての法人について、Finance and Operations アプリにそれぞれの会社固有のリソースの役割のレコードを自動的に作成します。

![リソース ロールの統合](./media/5Resources.jpg)

Project Operations のプロジェクト リソースは Dataverse で管理されており、Finance and Operations のアプリには同期されていません。

### <a name="transaction-categories"></a>トランザクション カテゴリ

トランザクションのカテゴリーは Dataverse に保持され、**プロジェクト トランザクション カテゴリ (msdyn\_transactioncategories)** のテーブル マッピングを使って Finance and Operations のアプリに同期されます。 トランザクションのカテゴリー レコードが同期されると、システムは自動的に 4 つの共有カテゴリー レコードを作成します。 各レコードは Finance and Operations アプリのトランザクション タイプに対応しており、トランザクション カテゴリのレコードにリンクしています。

![トランザクション カテゴリの統合](./media/4TransactionCategories.jpg)

見積もりと実績にトランザクション カテゴリーを使用する場合は、プロジェクトの会計士またはシステム管理者は、すべての法人に対応するプロジェクト カテゴリーを作成する必要があります。 詳細については、[プロジェクト　カテゴリの構成](../project-accounting/configure-project-categories.md) を参照してください。
