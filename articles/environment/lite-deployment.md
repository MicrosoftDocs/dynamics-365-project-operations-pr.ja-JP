---
title: Deploy Project Operations Lite 展開 – 見積もり請求の取引
description: このトピックでは、Project Operations ライト デプロイメントのインストール方法に関する情報を提供します - 見積もり請求の取引を行います。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948936"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a>Deploy Project Operations Lite 展開 – 見積もり請求の取引

_**適用対象:** ライト展開 - 見積もり請求の取引_

Project Operations は、複数の展開モデルをサポートしています。 最適な展開モデルを決定するには、[展開の種類](determine-deployment-type.md) を参照してください。


> [!IMPORTANT]
> この展開、ライト展開 – 見積もり請求に対処すると、**Common Data Service - Project Operations の展開のみ** となります。

- [Project Operations を新しい CDS 環境にインストールする](#new)
- [既存の CDS 環境にインストールする](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Project Operations を新しい CDS 環境にインストールする

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) として、[ PowerPlatform 管理センター](https://admin.powerplatform.com) で新しい CDS 環境を作成します。 **CDS データベース** および **Dynamics 365 アプリ**は、有効であることを確認します。 詳細については、[Power Platform 管理センターで環境を作成および管理する](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) を参照してください。
2. Dynamics 365 アプリの展開リストから、**Microsoft Dynamics 365 プロジェクトの営業案件**を選択します。


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Project Operations を既存の CDS 環境にインストールする

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) として、Project Operations をインストールする [PowerPlatform 管理センター](https://admin.powerplatform.com) で環境を見つけます。
2. Dynamics 365 アプリの展開リストから、**Microsoft Dynamics 365 プロジェクトの営業案件**をインストールします。 詳細については、[Dynamics 365 アプリを管理する](https://docs.microsoft.com/power-platform/admin/manage-apps) 参照してください。


