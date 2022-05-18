---
title: Project Operations の展開 (ライト)
description: このトピックでは、Project Operations ライト デプロイメントのインストール方法に関する情報を提供します - 見積もり請求の取引を行います。
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580738"
---
# <a name="deploy-project-operations---lite"></a>Project Operations の展開 (ライト)

_**適用対象:** ライト展開 - 見積もり請求の取引_



Project Operations は、複数の展開モデルをサポートしています。 最適な展開モデルを決定するには、[展開の種類](determine-deployment-type.md) を参照してください。


> [!IMPORTANT]
> この展開、ライト展開 – 見積もり請求に対処すると、**Dataverse - Project Operations の展開のみ** となります。

- [Project Operations を新しい Dataverse 環境にインストールする](#new)
- [既存の Dataverse 環境にインストールする](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations を新しい Dataverse 環境にインストールする

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、[PowerPlatform 管理センター](https://admin.powerplatform.com) で新しい Dataverse 環境を作成します。 **この環境用のデータベースの作成** と **Dynamics 365 アプリ** が有効になっていることを確認します。 詳細については、[Power Platform 管理センターで環境を作成および管理する](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) を参照してください。
2. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** を選択します。


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations を既存の Dataverse 環境にインストールする
1. インストールすると、[リソース/非在庫ベースのシナリオ機能のための Project Operations](project-operations-integrated-deployment-overview.md) がインストールされるため、環境が[デュアルライト](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)で構成されていないことを確認します。
2. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、Project Operations をインストールする [PowerPlatform 管理センター](https://admin.powerplatform.com) で環境を見つけます。
3. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** をインストールします。 詳細については、[Dynamics 365 アプリを管理する](/power-platform/admin/manage-apps) 参照してください。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
