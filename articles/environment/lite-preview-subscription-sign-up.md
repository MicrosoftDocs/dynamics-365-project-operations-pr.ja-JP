---
title: 試プレビュー サブスクリプションにサインアップする
description: このトピックでは、Project Operations ライト デプロイメントの購読および展開方法に関する情報を提供します - 見積もり請求の取引を行います。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079131"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="ab543-103">ライト展開のプレビュー サブスクリプションにサインアップ – 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="ab543-103">Sign up for a preview subscription for lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="ab543-104">このトピックでは、プレビュー パートナー オファーの購読方法および Dynamics 365 Project Operations の展開方法を説明します - 見積もり請求の取引を行います。</span><span class="sxs-lookup"><span data-stu-id="ab543-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="ab543-105">このプロセスは、Project Operations の今後のリリースで変更されます。</span><span class="sxs-lookup"><span data-stu-id="ab543-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab543-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="ab543-106">Prerequisites</span></span>

- <span data-ttu-id="ab543-107">プレビューへの参加を招待するメールが届きます。</span><span class="sxs-lookup"><span data-stu-id="ab543-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="ab543-108">[Project Operations Web サイト](https://dynamics.microsoft.com/en-us/project-operations/overview/) でプレビューを要求できます。</span><span class="sxs-lookup"><span data-stu-id="ab543-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="ab543-109">プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab543-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="ab543-110">すべての利用規約を確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab543-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="ab543-111">購読</span><span class="sxs-lookup"><span data-stu-id="ab543-111">Subscribe</span></span>

<span data-ttu-id="ab543-112">[プレビュー リクエスト](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) 承認を受け取ると、電子メールにより Microsoft から 2 つのオファーが送信されます。</span><span class="sxs-lookup"><span data-stu-id="ab543-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="ab543-113">これらのオファーを使用すると、Project Operations プレビューを展開できます。</span><span class="sxs-lookup"><span data-stu-id="ab543-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="ab543-114">Dynamics 365 Project Operations (CRM) – プレビュー試用版</span><span class="sxs-lookup"><span data-stu-id="ab543-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="ab543-115">Office 365 Project Operations - プレビュー試用版</span><span class="sxs-lookup"><span data-stu-id="ab543-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab543-116">このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。</span><span class="sxs-lookup"><span data-stu-id="ab543-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="ab543-117">このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="ab543-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="ab543-118">Dynamics 365 Project Operations (CRM) – プレビュー試用版</span><span class="sxs-lookup"><span data-stu-id="ab543-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="ab543-119">開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab543-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="ab543-120">最初のオファー コードである **Dynamics 365 Project Operations (CRM) – プレビュー試用版** をブラウザー URLに貼り付けて引き換えます。</span><span class="sxs-lookup"><span data-stu-id="ab543-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![オファーの引き換え](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="ab543-122">注文を確認します。</span><span class="sxs-lookup"><span data-stu-id="ab543-122">Confirm your order.</span></span>
<span data-ttu-id="ab543-123">![注文を確認](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="ab543-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="ab543-124">オファーが正常に引き換えられたことが確認できます。</span><span class="sxs-lookup"><span data-stu-id="ab543-124">You'll see confirmation offer was successfully redeemed.</span></span>

![確認](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="ab543-126">Office 365 Project Operations - プレビュー試用版</span><span class="sxs-lookup"><span data-stu-id="ab543-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="ab543-127">最初のオファー コードと同じ手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="ab543-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="ab543-128">最初のオファー コードで使用したのと同じユーザー アカウントを使用して、2 番目のオファー コードを必ず追加してください。</span><span class="sxs-lookup"><span data-stu-id="ab543-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="ab543-129">ライセンスの割り当て</span><span class="sxs-lookup"><span data-stu-id="ab543-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab543-130">次の手順を完了するには、組織の Microsoft 365 ポータルへの管理アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="ab543-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="ab543-131">[Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ab543-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![管理センター ホーム ページ](./media/14AdminPortal.png)

2. <span data-ttu-id="ab543-133">**アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab543-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![ライセンスの割り当て](./media/15AssignLicenses.png)

3. <span data-ttu-id="ab543-135">**Dynamics 365 Project Operations (CRM) プレビュー** と **Office 365 Project Operations - プレビュー** のライセンスが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab543-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="ab543-136">**変更を保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab543-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="ab543-137">新しい CDS 環境の作成</span><span class="sxs-lookup"><span data-stu-id="ab543-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="ab543-138">トピックの手順 [CDS 展開モデル](lite-deployment.md) に従い、新しい Project Operations CDS の展開環境をプロビジョニングします。</span><span class="sxs-lookup"><span data-stu-id="ab543-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="ab543-139">環境タイプを選択するときは、 **試用 (サブスクリプション ベース)** を必ず使用してください。</span><span class="sxs-lookup"><span data-stu-id="ab543-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="ab543-140">![新しい環境](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="ab543-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="ab543-141">**Dynamics 365 アプリを有効にする** の設定を選択し、 **これらのアプリを自動的に展開** を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="ab543-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="ab543-142">**保存** を選択して、環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="ab543-142">Select **Save** to create the environment.</span></span>

![データベースの追加](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="ab543-144">環境が作成されたら、 **Microsoft Dynamics 365 Project Operations** ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ab543-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![ソリューションのインストール](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="ab543-146">CDS コンフィグレーションをインストールし、デモ データを設定する</span><span class="sxs-lookup"><span data-stu-id="ab543-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="ab543-147">トピックの手順 [デモの設定および構成データを適用する](lite-apply-demo-setup-config-data.md) に従い、CDS 構成をインストールし、デモ データを設定します。</span><span class="sxs-lookup"><span data-stu-id="ab543-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>
