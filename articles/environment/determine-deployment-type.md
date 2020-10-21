---
title: 展開の種類
description: このトピックでは、会社のプロジェクト オペレーションの正しい展開の種類を決定するのに役立つ情報を提供します。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948938"
---
# <a name="deployment-types"></a>展開の種類

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

> [!IMPORTANT]
> ライセンスを購入した後、ここから開始して、[ガイド付きインストール フロー](https://aka.ms/provisionprojectoperations) を使用し Dynamics 365 Project Operations の最適な展開モデルを決定します。
> ガイド付きインストール フローを終了した後、正しい管理ポータルに移動してインストールを完了します。 以下の展開の詳細を参照して、インストールを完了します。


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamics 365 Project Service Automation を使用する Dynamics の既存の顧客
Project Operations には、Project Service Automation に付属する機能が含まれています。 将来、これらの顧客に対してアップグレード パスがリリースされる予定です。

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>プロジェクト管理および会計を使用する Dynamics 365 Finance の既存の顧客 

プロジェクト管理および会計機能を使用する Finance の既存の顧客は、これをそのままの状態で引き続き使用できます。 [在庫/製造オーダー シナリオ向け Project Operations](#pma) を参照してください。

Project Operations は、要件に合った複数の展開オプションをサポートします。 新規または既存の Dynamics 365 の顧客のいずれの場合でも、Project Operations はニーズにあわせてサポートできます。

[展開アンケート](https://aka.ms/provisionprojectoperations) は、適切な展開を決定するのに役立ちます。 結果により、次のいずれかの展開の種類にガイドされます。

- [ライト展開 - 見積もり請求の取引](#lite)
- [リソース/非在庫のシナリオ向け Project Operations](#integrated)
- [在庫/製造指示のシナリオ向け Project Operations](#pma)

Project Operations は、法人エンティティ レベルの構成を通じて、同じ環境で、在庫/製造オーダー シナリオおよび非在庫/リソースベースのシナリオをサポートします。 たとえば、Contoso は、米国の製造施設 (法人 = 米国 Contoso Manufacturing) で在庫/製造オーダーの機能を、および英国のContoso Robotics Arms サービス施設 (法人 = 英国 Contoso Robotics) で非在庫/リソースベースの機能を活用できます。

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>ライト展開 - 見積もり請求の取引
ライト展開には、次の機能が含まれています。

- Web 向けの Microsoft Project を使用したプロジェクト計画
- 多次元の価格
- 統一リソース管理
- 時間のトラッキング
- 基本経費
- 請求書の提案

### <a name="deployment-steps"></a>展開の手順:
[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。

この展開については、[プレビュー サブスクリプションにサインアップする](lite-preview-subscription-sign-up.md) および[新しい環境をプロビジョニングする](lite-deployment.md) を参照してください。 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>リソース/非在庫のシナリオ向け Project Operations
リソース/非在庫のシナリオ向け Project Operations には、次の機能が含まれています。
  
- Web 向けの Microsoft Project を使用したプロジェクト計画
- 多次元の価格設定
- 統一リソース管理
- 時間のトラッキング
- 基本経費
- フル経費
- レシート OCR
- フル請求
- 売上認識

### <a name="deployment-steps"></a>展開の手順:
[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。

この展開については、[プレビュー サブスクリプションにサインアップする](resource-sign-up-preview-subscription.md) および[新しい環境をプロビジョニングする](resource-provision-new-environment.md) を参照してください。 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>在庫/製造指示のシナリオ向け Project Operations

- WBS を使用したプロジェクト計画
- リソース管理
- 時間のトラッキング
- フル経費
- レシート OCR
- フル請求
- 売上認識
- 製造オーダー
- 材料サポート

### <a name="deployment-steps"></a>展開の手順:
[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。

この展開については、[プレビュー サブスクリプションにサインアップする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) および[新しい環境をプロビジョニングする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json) を参照してください。 



