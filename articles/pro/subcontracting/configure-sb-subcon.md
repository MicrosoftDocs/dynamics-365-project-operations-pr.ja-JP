---
title: スケジュール ボードを構成して請負社員と外注キャパシティを表示する
description: このトピックでは、Microsoft Dynamics 365 Project Operations のスケジュール ボードを設定して、プロジェクトのリソース要件に人員を配置する際に外注リソースのキャパシティを表示する方法について説明します。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903462"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>スケジュール ボードを構成して請負社員と外注キャパシティを表示する 

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

Microsoft Dynamics 365 Project Operations のスケジュール ボードは、2 つの方法でリソースの検索を行うことができます:

- 特定のプロジェクト ベースのリソース要求のコンテキストを使用しない一般的なリソース検索です。
- 要件別リソース検索では、プロジェクト要件が提案されたリソースのコンテキストを提供します。

外注リソースキャパシティや契約労働者をスケジュール ボードに通知するには、スケジュール ボードの設定を更新する必要があります。 これらのアップデートには次のものが含まれます: 
- 一般的なリソース検索のスケジュールボード設定を更新します。
- 要件ベースのリソース検索のスケジュールボード設定を更新します。

## <a name="update-schedule-board-settings-for-general-resource-search"></a>一般的なリソース検索のスケジュールボード設定を更新する
### <a name="update-filters-for-general-resource-search"></a>一般的なリソース検索用のフィルターを更新する
リソースを検索する際には、スケジュール ボードで利用できるフィルターを更新し、以下のいずれかまたはすべてを指定して外部リソースも検索できるようにする必要があります:
  - 従業員の種類: 表示されるリソースが契約社員であるか従業員であるかを示します。
  - リソースの所属先となるベンダー企業です。
  - 特定の下請契約や下請ラインに属するリソースです。
    
### <a name="update-retrieve-resource-query"></a>リソース取得クエリの更新
また、検索に使用するクエリについても、これらの追加フィルター属性を使用するように更新する必要があります。 一般的なリソース検索で使用するスケジュールボードの構成を更新するには、以下の手順で行います:  
1. 特定のスケジュールボードで使用する **スケジュールボードの設定** を開きます。
2. **一般設定** タブをを開き、クリックして **その他の設定** までスクロールします。
3. このセクションの設定リストで、**フィルター レイアウト** を **Project Operations Lite の既定のフィルターレイアウト** に更新します。
4. **リソース クエリの取得** を **Project Operations Lite の既定のリソース取得クエリ** に更新します。

![一般的なリソース検索のスケジュールボード設定を更新する](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>要件ベースのリソース検索のスケジュールボード設定を更新する
### <a name="update-filters-for-requirement-specific-resource-search"></a>要件に特化したリソース検索用のフィルターを更新する 
リソースを検索する際には、スケジュール ボードで利用できるフィルターを更新し、以下のいずれかまたはすべてを指定して外部リソースも検索できるようにする必要があります:
 - 従業員の種類: 表示されるリソースが契約社員であるか従業員であるかを示します。
 - リソースの所属先となるベンダー企業です。
 - 特定の下請契約や下請ラインに属するリソースです。

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>要件に特化したリソース検索のリソース取得クエリを更新する 
また、検索に使用するクエリについても、これらの追加フィルター属性を使用するように更新する必要があります。 要件に特化したリソース検索で使用するスケジュールボードの構成を更新するには、以下の手順で行います:

1. 要件に特化した **スケジュールボードの設定** を開き、**既定の設定を開く** を選択して要件に特化した検索設定を開きます。
2. **一般設定** タブをを開き、クリックして **その他の設定** までスクロールします。
3. このセクションの設定リストで、**フィルター レイアウト** を **Project Operations Lite の既定のフィルターレイアウト** に更新します。
4. **リソース クエリの取得** を **Project Operations Lite の既定のリソース取得クエリ** に更新します。
5. **スケジュール タイプ** タブをを開き、**プロジェクト** に移動します。
6. **プロジェクト** の設定下で、**スケジュールアシスタントリソース取得クエリー** を **Project Operations Lite 向け既定のリソース取得クエリー** に更新し、**スケジュールアシスタント制約条件の取得クエリー** を **Project Operations Lite 向け既定の制約取得クエリー** に更新します。

![要件ベースのリソース検索のスケジュールボード設定を更新する](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
