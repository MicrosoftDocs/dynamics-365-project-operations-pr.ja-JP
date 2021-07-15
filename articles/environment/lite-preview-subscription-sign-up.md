---
title: プレビューのサブスクリプションにサインアップする (ライト)
description: このトピックでは、Project Operations ライト デプロイメントの購読および展開方法に関する情報を提供します - 見積もり請求の取引を行います。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334788"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="58383-103">プレビュー サブスクリプションにサインアップする (ライト)</span><span class="sxs-lookup"><span data-stu-id="58383-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="58383-104">このトピックでは、試用版のオファーに登録し、Dynamics 365 Project Operations ライトのデプロイから、プロフォーマ請求書への対応を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="58383-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="58383-105">このプロセスは、Project Operations の今後のリリースで変更されます。</span><span class="sxs-lookup"><span data-stu-id="58383-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="58383-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="58383-106">Prerequisites</span></span>
- <span data-ttu-id="58383-107">プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="58383-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="58383-108">最初のオファーの引き換え時にテナントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="58383-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58383-109">このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。</span><span class="sxs-lookup"><span data-stu-id="58383-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="58383-110">このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="58383-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="58383-111">試用版はテナントでの単一回の使用となります。</span><span class="sxs-lookup"><span data-stu-id="58383-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="58383-112">試用版は 1 度しか実行できません。</span><span class="sxs-lookup"><span data-stu-id="58383-112">You can only run a trial one time.</span></span> <span data-ttu-id="58383-113">試用版に特化した、新しいテナントを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="58383-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="58383-114">Dynamics 365 Project Operations 試用版</span><span class="sxs-lookup"><span data-stu-id="58383-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="58383-115">開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="58383-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="58383-116">[Project Operations 試用版](https://aka.ms/try-po)にアクセスし、**Dynamics 365 Project Operations** の最初のオファーコードを引き換えます。</span><span class="sxs-lookup"><span data-stu-id="58383-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="58383-117">注文を確認します。</span><span class="sxs-lookup"><span data-stu-id="58383-117">Confirm your order.</span></span>

  <span data-ttu-id="58383-118">オファーが正常に引き換えられたことを示す確認メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="58383-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="58383-119">ライセンスの割り当て</span><span class="sxs-lookup"><span data-stu-id="58383-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58383-120">次の手順を完了するには、組織の Microsoft 365 ポータルへの管理アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="58383-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="58383-121">[Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="58383-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="58383-122">**アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="58383-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="58383-123">**Dynamics 365 Project Operations** ライセンスが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="58383-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="58383-124">**変更を保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58383-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="58383-125">Dataverse 環境を作成する</span><span class="sxs-lookup"><span data-stu-id="58383-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="58383-126">トピック [Dataverse デプロイ モデル](lite-deployment.md) の指示に従って、新しい Project Operations Dataverse デプロイ環境をプロビジョニングします。</span><span class="sxs-lookup"><span data-stu-id="58383-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="58383-127">環境タイプを選択するときは、**試用 (サブスクリプション ベース)** を必ず使用してください。</span><span class="sxs-lookup"><span data-stu-id="58383-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![新しい環境](./media/19CreateEnvironment.png)

2. <span data-ttu-id="58383-129">**Dynamics 365 アプリを有効にする** の設定を選択し、**これらのアプリを自動的に展開** を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="58383-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="58383-130">**保存** を選択して、環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="58383-130">Select **Save** to create the environment.</span></span>

  ![データベースの追加](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="58383-132">環境が作成されたら、**Microsoft Dynamics 365 Project Operations** ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="58383-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![ソリューションのインストール](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="58383-134">CDS コンフィグレーションをインストールし、デモ データを設定する</span><span class="sxs-lookup"><span data-stu-id="58383-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="58383-135">トピックの手順 [デモの設定および構成データを適用する](lite-apply-demo-setup-config-data.md) に従い、CDS 構成をインストールし、デモ データを設定します。</span><span class="sxs-lookup"><span data-stu-id="58383-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
