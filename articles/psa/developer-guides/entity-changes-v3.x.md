---
title: エンティティ、コントロール、およびユーザー インターフェイスの変更 (Project Service Automation 3.x)
description: このトピックでは、Project Service Automation 3.x Microsoft Dynamics のソリューションの変更について説明します。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148739"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>エンティティ、コントロール、およびユーザー インターフェイスの変更 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Project Service Automation (PSA) 3.x Microsoft Dynamics のリリースでは、エンティティ、コントロール、ビュー、ユーザー インターフェイスに多くの変更がされています。 このトピックでは、これらの重要な変更について説明します。

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>営業ドキュメント、営業ドキュメントの明細、営業ドキュメント品目明細エンティティの親子関係
バージョン3.0よりも前にリリースされた Dynamics 365 Project Service Automation (PSA) では、営業ドキュメント、営業ドキュメントの明細、営業ドキュメント品目明細エンティティーでは、関連エンティティーのGUIDの文字列表現を保持するストリング フィールドによって実装されていました。 これは、ソリューションのサーバ側とクライアント側で重要なカスタム コードを必要とするプラットフォームの制限によるものです。このソリューションは、これらの関係を一般的な Dynamics CRM エンティティの関係と同様に動作させ、文字列フィールドをルックアップフィールドのように動作させます。

PSA 3.0では、営業文書と営業文書明細エンティティ間の新規エンティティの関連性を利用するように更新されました。

ルックアップフィールドを使用してエンティティへの参照を示すことができるようになったため、以前のバージョンで関連するエンティティのGUIDの文字列値を保持していたフィールドは不要になり、非推奨になりました。 従来の文字列フィールドで定義された関係を処理するカスタムクライアントおよびサーバー側のコードも廃止されています。

### <a name="entity-schema-changes"></a>エンティティ スキーマの変更
以下の表に、使用すべきでない文字列フィールドとエンティティの新たなルックアップフィールドのリストを示します。 

 エンティティ |   廃止された文字列 (文字列) | 新規フィールド(検索)
--- | --- | ---
請求明細 (請求書の明細) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (実績) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (プロジェクト 契約 請求書明細 スケジュール ) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (プロジェクト契約明細マイルストーン) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (実際) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (請求書明細詳細) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (仕訳帳明細行) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (プロジェクト契約品目リソースカテゴリ) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (プロジェクト契約品目詳細) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (プロジェクト契約品目トランザクションカテゴリ) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (プロジェクト契約品目トランザクション分類) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (見積明細請求書スケジュール) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (見積明細リソースカテゴリ) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (見積明細マイルストーン) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (見積明細詳細) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (見積明細トランザクションカテゴリ) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (見積明細トランザクション分類) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (受注明細) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>非推奨のカスタム ビューとコントロール
以下のカスタム ビューとコントロールおよび関連するアーティファクトは非推奨になりました。

- Chargeability ビュー
- 見積明細の **プロジェクト情報** ページに見積明細の詳細を表示するカスタム グリッド コントロール。
- 受注明細の **プロジェクト情報** ページにプロジェクト契約明細の詳細を表示するカスタム グリッド コントロール。

> [!NOTE]
> 廃止されたリソースの完全なリストについては、 [Project Service Automation v3.x で非推奨となったウェブリソース](../developer-guides/web-resources-deprecated-v3.x.md)を参照してください。

## <a name="unified-client-interface-app-module"></a>統合クライアント インターフェイス アプリケーション モジュール
統合クライアント インターフェイス (UCI) アプリケーション モジュールの導入にともない、PSAサイトマップエントリはシステムから削除されました。  
UCI アプリケーションモジュールにはPSA バージョンのフォームしか含まれていないため、営業案件、見積もり、受注、請求書ののフォーム切り替えに関する機能は不要となり、これらの使用は非推奨となりました。  

以下のWebリソースが非推奨となりました:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> 廃止されたリソースの完全なリストについては、 [Project Service Automation v3.x で非推奨となったウェブリソース](../developer-guides/web-resources-deprecated-v3.x.md)を参照してください。




[!INCLUDE[footer-include](../../includes/footer-banner.md)]