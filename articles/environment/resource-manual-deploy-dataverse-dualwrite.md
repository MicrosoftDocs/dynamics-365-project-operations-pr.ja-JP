---
title: デュアル書き込みに対応する Project Operations の Dataverse アプリを手動でデプロイする
description: このトピックは、デュアル書き込みに対応する Project Operations の Dataverse アプリを手動でデプロイする方法について説明します。
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274014"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="69b3c-103">デュアル書き込みに対応する Project Operations の Dataverse アプリを手動でデプロイする</span><span class="sxs-lookup"><span data-stu-id="69b3c-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="69b3c-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="69b3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="69b3c-105">このトピックは、デュアル書き込みに対応する Microsoft Dataverse の Microsoft Dynamics 365 Project Operations を手動でデプロイする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="69b3c-106">Project Operations は、環境の構成を検出し、前提条件が満たされていれば、デュアル書き込みの対応を追加します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="69b3c-107">Microsoft Dynamics Lifecycle Services (LCS) によるデプロイメントの際は、このトピックで説明する手順を使用することで、Microsoft Power Platform 統合 (旧名 Common Data Service 環境) のデプロイを省略できます。</span><span class="sxs-lookup"><span data-stu-id="69b3c-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="69b3c-108">Dataverse に Project Operations を展開してデュアル書き込みに対応させるには、大きく分けて 4 つのステップがあります:</span><span class="sxs-lookup"><span data-stu-id="69b3c-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="69b3c-109">[Dataverse でデュアル書き込みに対応した新しい環境を作る](#create)。</span><span class="sxs-lookup"><span data-stu-id="69b3c-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="69b3c-110">[デュアル書き込みの前提条件を環境に追加する](#prerequisites)。</span><span class="sxs-lookup"><span data-stu-id="69b3c-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="69b3c-111">[Project Operations Dataverse アプリを追加する](#dataverse)。</span><span class="sxs-lookup"><span data-stu-id="69b3c-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="69b3c-112">[ご利用の環境をリンクする](#link)。</span><span class="sxs-lookup"><span data-stu-id="69b3c-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="69b3c-113">Dataverse でデュアル書き込みに対応した新しい環境を作る</span><span class="sxs-lookup"><span data-stu-id="69b3c-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="69b3c-114">この手順を完了するには、システム管理者でサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="69b3c-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="69b3c-115">[Power Platform管理センター](https://admin.powerplatform.com)を開き、管理者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="69b3c-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="69b3c-116">新しい環境を作成し、名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="69b3c-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="69b3c-117">環境の種類を選択する。</span><span class="sxs-lookup"><span data-stu-id="69b3c-117">Select the environment type.</span></span> <span data-ttu-id="69b3c-118">試用版のオファーにサインアップした場合は、**試用版 (サブスクリプション ベース)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="69b3c-119">展開するリージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="69b3c-120">**この環境にデータベースを作成する** オプションを有効化します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="69b3c-121">言語を確認し、次に通貨が Finance and Operations のアプリの通貨と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="69b3c-122">**Dynamics 365 アプリ** のオプションを有効にし、**これらのアプリを自動的にデプロイする** のフィールドが **無し** になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="69b3c-123">セキュリティ グループが必要な場合は、セキュリティ グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="69b3c-124">**保存** を選択して、環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="69b3c-125">デプロイが完了し、環境が **準備完了** の状態になるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="69b3c-126">デュアル書き込みの前提条件を環境に追加する</span><span class="sxs-lookup"><span data-stu-id="69b3c-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="69b3c-127">デュアル書き込み対応では、**会社** エンティティなどの主要なエンティティに追加されるフィールド含まれます。</span><span class="sxs-lookup"><span data-stu-id="69b3c-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="69b3c-128">既存の環境にデュアル書き込みのサポートを追加する場合、サポートを有効にするためにデータの更新が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="69b3c-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="69b3c-129">データをブートストラップする方法については、[会社のデータをブートストラップする](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69b3c-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="69b3c-130">デュアル書き込みの詳細については、[デュアル書き込みのシステム要件](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69b3c-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="69b3c-131">この手順を実行して、環境にデュアル書き込みの前提条件を追加します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="69b3c-132">作成したばかりの環境を開き、**リソース**\>**Dynamics 365 アプリ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="69b3c-133">アプリ リストで **デュアル書き込みコア ソリューション** を選択し、インストールします。</span><span class="sxs-lookup"><span data-stu-id="69b3c-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="69b3c-134">インストールが完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-134">Wait until the installation is completed.</span></span> <span data-ttu-id="69b3c-135">アプリ リストで **デュアル書き込みアプリのオーケストレーション ソリューション** を選択し、インストールします。</span><span class="sxs-lookup"><span data-stu-id="69b3c-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="69b3c-136">Project Operations Dataverse  アプリを追加します</span><span class="sxs-lookup"><span data-stu-id="69b3c-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="69b3c-137">この手順は、Project Operations をインストールする前に前の手順を完了している場合にのみ行うことができます。</span><span class="sxs-lookup"><span data-stu-id="69b3c-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="69b3c-138">インストール時に環境構成を分析し、必要に応じてデュアル書き込みへの対応を追加しています。</span><span class="sxs-lookup"><span data-stu-id="69b3c-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="69b3c-139">上記手順で作成した環境を開き、**リソース**\>**Dynamics 365 アプリ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="69b3c-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="69b3c-140">**Microsoft Dynamics 365 Project Operations** アプリ リストに追加してインストールします。</span><span class="sxs-lookup"><span data-stu-id="69b3c-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="69b3c-141">ご利用の環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="69b3c-141">Link your environments</span></span>

<span data-ttu-id="69b3c-142">Dataverse の環境がデプロイされた後、 Finance and Operations アプリでリンクを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="69b3c-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="69b3c-143">[デデュアル書き込みの設定ウィザードを使用して環境をリンクする](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="69b3c-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
