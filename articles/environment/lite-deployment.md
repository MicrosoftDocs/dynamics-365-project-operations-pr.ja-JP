---
title: Project Operations の展開 (ライト)
description: このトピックでは、Project Operations ライト デプロイメントのインストール方法に関する情報を提供します - 見積もり請求の取引を行います。
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995537"
---
# <a name="deploy-project-operations---lite"></a>Project Operations の展開 (ライト)

_**適用対象:** ライト展開 - 見積もり請求の取引_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations は、複数の展開モデルをサポートしています。 最適な展開モデルを決定するには、[展開の種類](determine-deployment-type.md) を参照してください。


> [!IMPORTANT]
> この展開、ライト展開 – 見積もり請求に対処すると、**Common Data Service - Project Operations の展開のみ** となります。

- [Project Operations を新しい CDS 環境にインストールする](#new)
- [既存の CDS 環境にインストールする](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Project Operations を新しい CDS 環境にインストールする

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、[PowerPlatform 管理センター](https://admin.powerplatform.com) で新しい CDS 環境を作成します。 **CDS データベース** および **Dynamics 365 アプリ** は、有効であることを確認します。 詳細については、[Power Platform 管理センターで環境を作成および管理する](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) を参照してください。
2. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** を選択します。


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Project Operations を既存の CDS 環境にインストールする

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、Project Operations をインストールする [PowerPlatform 管理センター](https://admin.powerplatform.com) で環境を見つけます。
2. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** をインストールします。 詳細については、[Dynamics 365 アプリを管理する](/power-platform/admin/manage-apps) 参照してください。




[!INCLUDE[footer-include](../includes/footer-banner.md)]