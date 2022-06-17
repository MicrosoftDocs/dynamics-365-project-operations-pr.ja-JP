---
title: 展開の種類を決定する
description: この記事では、会社の Project Operations の正しい展開タイプを判断するための情報を提供します。
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912200"
---
# <a name="determine-your-deployment-type"></a>展開の種類を決定する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

> [!IMPORTANT]
> ライセンスを購入したら、[ガイド付きインストール フロー](https://aka.ms/provisionprojectoperations) を使って、ここから Dynamics 365 Project Operations の最適な展開モデルを決定します。
> ガイド付きインストール フローを終了した後、正しい管理ポータルに移動してインストールを完了します。 展開の詳細を参照して、インストールを完了します。


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamics 365 Project Service Automation を使用する Dynamics の既存の顧客
Project Operations には、Project Service Automation に付属する機能が含まれています。 これらのお客様向けに、2021 年のリリースサイクル 1 でアップグレード パスがリリースされます。

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>プロジェクト管理と会計を使用している Dynamics 365 Finance の既存の顧客 

プロジェクト管理および会計機能を使用する財務の既存のお客様は、そのままご利用いただけます。 [在庫/製造オーダー シナリオ向け Project Operations](#pma) を参照してください。


## <a name="deployment-regions"></a>展開リージョン
Project Operations の展開をサポートするリージョンを決定するには、[Dynamics 365 および Power Platform レポートの地域的利用可能性](https://dynamics.microsoft.com/en-us/geographic-availability/) を参照してください。 **レポートを見る** を選択して、**Dynamics 365 > オペレーション アプリ > Dynamics 365 Project Operations** を展開して、サポートされているリージョンを表示します。

## <a name="deployment-types"></a>展開タイプ
Project Operations では、要件に合わせて複数の展開オプションがサポートされます。 新規または既存の Dynamics 365 の顧客のいずれの場合でも、Project Operations はニーズにあわせた対応ができます。

[展開アンケート](https://aka.ms/provisionprojectoperations) は、適切な展開を決定するのに役立ちます。 結果により、次のいずれかの展開の種類にガイドされます。

- [ライト展開 - 見積もり請求の取引](#lite)
- [リソース/非在庫のシナリオ向け Project Operations](#integrated)
- [在庫/製造指示のシナリオ向け Project Operations](#pma)

Project Operations は、法人エンティティ レベルの構成を通じて、同じ環境で、在庫/製造オーダー シナリオおよび非在庫/リソースベースのシナリオをサポートします。 たとえば、Contoso 社は、米国の製造施設（法人= Contoso Manufacturing United States）で在庫/製造注文機能を使用できます。 Contoso は、英国 の Contoso Robotics Arms サービス施設（法人= Contoso Robotics United Kingdom）で、在庫のない/リソースベースの機能を使用できます。

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>ライト展開 - 見積もり請求の取引

ライト展開には、次の機能が含まれています。

- Dynamics 365 Sales アプリケーションのエクスペリエンスを拡張するプロジェクトの営業プロセス
- Web 向けの Microsoft Project を使用したプロジェクト計画
- 多次元の価格
- 統合されたリソース管理
- 時間のトラッキング
- 基本経費
- プロジェクト マネージャーのレビューと編集のための見積請求 

#### <a name="deployment-steps"></a>展開の手順
[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。

この展開については、[プレビュー サブスクリプションにサインアップする](lite-preview-subscription-sign-up.md) および[新しい環境をプロビジョニングする](lite-deployment.md) を参照してください。 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>リソース/非在庫のシナリオ向け Project Operations
リソース/非在庫のシナリオ向け Project Operations には、次の機能が含まれています。
 
- Dynamics 365 Sales アプリケーションのエクスペリエンスを拡張するプロジェクトの営業プロセス
- Web 向けの Microsoft Project を使用したプロジェクト計画
- 多次元の価格
- 統一リソースの管理
- 時間のトラッキング
- 基本の経費
- フル経費
- レシート OCR
- 見積送り状と顧客向けの請求書 
- プロジェクトに対する売上の認識

#### <a name="deployment-steps"></a>展開の手順
[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。

この展開については、[プレビュー サブスクリプションにサインアップする](resource-sign-up-preview-subscription.md) および[新しい環境をプロビジョニングする](resource-provision-new-environment.md) を参照してください。 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>在庫/製造指示のシナリオ向け Project Operations

- WBS を使用したプロジェクト計画
- リソース管理
- 時間のトラッキング
- フル経費
- OCR の受け取り
- 完全な請求
- 売上認識
- 製造オーダー
- 在庫による在庫材料のサポート

#### <a name="deployment-steps"></a>展開の手順
[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。

この展開については、[プレビュー サブスクリプションにサインアップする](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) および[新しい環境をプロビジョニングする](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json) を参照してください。 



[!INCLUDE[footer-include](../includes/footer-banner.md)]