---
title: 経費管理統合
description: この記事では、デュアル ライトを使った Project Operations での経費レポート統合について説明します。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e11f1cfd714212691146eed59bcfb5b5facd750c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029215"
---
# <a name="expense-management-integration"></a>経費管理統合

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事では、デュアル ライトを使った Project Operations [経費の完全展開](../expense/expense-overview.md) での経費レポート統合について説明します。

## <a name="expense-categories"></a>経費カテゴリ

完全な経費展開では、経費カテゴリは財務と運用アプリで作成および維持されます。 経費のカテゴリーを新たに作成するには、以下の手順で行います :

1. Microsoft Dataverse で、**トランザクション** のカテゴリを作成します。 二重書き込み統合により、このトランザクション カテゴリが財務と運用アプリに同期されます。 詳細については、[プロジェクト カテゴリの構成](/dynamics365/project-operations/project-accounting/configure-project-categories) と [Project Operations の設定と構成データの統合](resource-dual-write-setup-integration.md)を参照してください。 この統合の結果として、システムは財務と運用アプリで 4 つの共有カテゴリ レコードを作成します。
2. Finance で、**経費管理** > **設定** > **共有カテゴリ** に移動し、トランザクション クラスが **費用** となっている共有カテゴリを選択します。 **経費で使用可能** パラメータを **True** に設定し、使用する経費のタイプを定義します。
3. この共有カテゴリ レコードを使用して、次に移動して新しい経費のカテゴリを作成します : **経費管理** > **設定** > **経費管理** に移動して **新規** を選択します。 レコードが保存されると、二重書き込みはテーブル マッピングを使用します。**Project Operations の統合 プロジェクト経費のカテゴリーのエクスポート エンティティ (msdyn\_expensecategories)** で Dataverse にこのレコードを同期します。

  ![経費カテゴリの統合。](./media/DW6ExpenseCategories.png)

財務と運用アプリの経費カテゴリは、会社または法人に固有です。 Dataverse には、対応する法人別のレコードがあります。 プロジェクト マネージャーが経費を見積もる際は、自分が担当しているプロジェクトを所有している会社とは別の会社が所有しているプロジェクト用に作成された経費カテゴリーを選択することはできません。 

## <a name="expense-reports"></a>経費報告書

経費報告書は、財務と運用アプリで作成および承認されます。 詳細については、[Dynamics 365 Project Operationsで経費報告書を作成して処理する](/learn/modules/create-process-expense-reports/)を参照してください。 経費報告書はプロジェクト マネージャーによって承認された後、総勘定元帳に転記されます。 Project Operations では、プロジェクト関連の経費報告書の明細は、特別な転記ルールを使用して転記されます。

  - プロジェクト関連のコスト (回収不能な税金を含む) は、総勘定元帳のプロジェクトの原価勘定にすぐには転記されるのではなく、費用統合勘定に転記されます。 この勘定は、**プロジェクト管理と会計** > **設定** > **プロジェクト管理と会計パラメーター**、**Dynamics 365 Customer engagement の Project Operations** タブで構成されます。
  - 二重書き込みは Dataverse に同期され、これは **Project Operations 統合 プロジェクト 経費エクスポート エンティティ (msdyn\_expenses)** テーブル マッピングを使用して行われます。
  - 税補助元帳、仕入先補助元帳、その他の財務転記は、経費報告書の転記時に該当する場合に記録されます。

  ![経費報告書の統合。](./media/DW6ExpenseReports.png)

レコードが Dataverse の **費用** エンティティに書き込まれる際、システムはレコードの自動承認プロセスをトリガーします。 必要に応じて、次にアクセスすることで、Dataverse の自動承認プロセスの状態を確認できます : **高度な設定** > **システム** > **システム ジョブ**。 承認が完了すると、経費トランザクション クラスのレコードが **実績** エンティティ に作成されます。

経費関連の実績は、二重書き込みテーブル マッピングの  **Project Operations 統合実績 (msdyn\_actuals)** を使って処理されます。 詳細については、[プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md) を参照してください。

定期的なプロセスである **ステージング テーブルからのインポート** は、Project Operations 統合仕訳帳に経費報告書関連の仕訳を作成します。 オフセット勘定は、既定で経費統合勘定になります。 転記統合仕訳帳では、経費取引の勘定残高を決済し、経費の金額をプロジェクトの原価勘定に移動させます。 また、このシステムは、下流の請求書作成や収益認識のために、プロジェクトの補助元帳トランザクションを作成します。
