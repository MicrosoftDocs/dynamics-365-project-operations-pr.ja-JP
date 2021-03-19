---
title: Project Operations の展開 (ライト)
description: このトピックでは、Project Operations ライト デプロイメントのインストール方法に関する情報を提供します - 見積もり請求の取引を行います。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290095"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="a9f96-103">Project Operations の展開 (ライト)</span><span class="sxs-lookup"><span data-stu-id="a9f96-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="a9f96-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="a9f96-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a9f96-105">Project Operations は、複数の展開モデルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a9f96-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="a9f96-106">最適な展開モデルを決定するには、[展開の種類](determine-deployment-type.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9f96-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="a9f96-107">この展開、ライト展開 – 見積もり請求に対処すると、**Common Data Service - Project Operations の展開のみ** となります。</span><span class="sxs-lookup"><span data-stu-id="a9f96-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="a9f96-108">Project Operations を新しい CDS 環境にインストールする</span><span class="sxs-lookup"><span data-stu-id="a9f96-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="a9f96-109">既存の CDS 環境にインストールする</span><span class="sxs-lookup"><span data-stu-id="a9f96-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="a9f96-110">Project Operations を新しい CDS 環境にインストールする</span><span class="sxs-lookup"><span data-stu-id="a9f96-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="a9f96-111">Project Operations ライセンスの[グローバルまたは Power Platform 管理者](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) として、[PowerPlatform 管理センター](https://admin.powerplatform.com) で新しい CDS 環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="a9f96-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="a9f96-112">**CDS データベース** および **Dynamics 365 アプリ** は、有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9f96-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="a9f96-113">詳細については、[Power Platform 管理センターで環境を作成および管理する](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9f96-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="a9f96-114">Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9f96-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="a9f96-115">Project Operations を既存の CDS 環境にインストールする</span><span class="sxs-lookup"><span data-stu-id="a9f96-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="a9f96-116">Project Operations ライセンスの[グローバルまたは Power Platform 管理者](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) として、Project Operations をインストールする [PowerPlatform 管理センター](https://admin.powerplatform.com) で環境を見つけます。</span><span class="sxs-lookup"><span data-stu-id="a9f96-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="a9f96-117">Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a9f96-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="a9f96-118">詳細については、[Dynamics 365 アプリを管理する](https://docs.microsoft.com/power-platform/admin/manage-apps) 参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9f96-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]