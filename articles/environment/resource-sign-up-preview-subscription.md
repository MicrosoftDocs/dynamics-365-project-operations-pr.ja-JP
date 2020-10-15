---
title: リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします
description: このトピックは、リソース/非在庫ベースのシナリオ向け Project Operations をサブスクライブして展開する方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948942"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="83b77-103">リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします</span><span class="sxs-lookup"><span data-stu-id="83b77-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="83b77-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="83b77-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="83b77-105">このトピックは、プレビュー/パートナー オファーをサブスクライブし、リソース/非在庫ベースのシナリオ向け Project Operations 環境を展開する方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="83b77-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83b77-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="83b77-106">Prerequisites</span></span>

- <span data-ttu-id="83b77-107">プレビューへの参加を招待するメールが届きます。</span><span class="sxs-lookup"><span data-stu-id="83b77-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="83b77-108">[Project Operations Web サイト](https://dynamics.microsoft.com/en-us/project-operations/overview/) でプレビューを要求できます。</span><span class="sxs-lookup"><span data-stu-id="83b77-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="83b77-109">プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b77-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="83b77-110">Finance 環境を展開するには、環境ごとに請求される有効な Azure サブスクリプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="83b77-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="83b77-111">組織の既存のサブスクリプションを使用するか、[Azure トライアル](https://azure.microsoft.com/en-us/free/) を使用して開始できます。</span><span class="sxs-lookup"><span data-stu-id="83b77-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="83b77-112">CDS 環境は、30 日間限定で無料で提供されます。</span><span class="sxs-lookup"><span data-stu-id="83b77-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="83b77-113">購読</span><span class="sxs-lookup"><span data-stu-id="83b77-113">Subscribe</span></span>

<span data-ttu-id="83b77-114">[プレビュー要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) が承認されると、メールで Microsoft から 2 つのオファーが送信されますを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="83b77-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="83b77-115">これらのオファーを使用すると、Project Operations プレビューを展開できます。</span><span class="sxs-lookup"><span data-stu-id="83b77-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="83b77-116">Dynamics 365 Project Operations – プレビュー 試用版</span><span class="sxs-lookup"><span data-stu-id="83b77-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="83b77-117">Dynamics 365 for Finance and Operations プレビュー 試用版。</span><span class="sxs-lookup"><span data-stu-id="83b77-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83b77-118">このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。</span><span class="sxs-lookup"><span data-stu-id="83b77-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="83b77-119">このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="83b77-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="83b77-120">Dynamics 365 Project Operations – プレビュー 試用版</span><span class="sxs-lookup"><span data-stu-id="83b77-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="83b77-121">最初のオファーである、**Dynamics 365 Project Operations 試用版**を、歓迎メールに記載されている URL で利用します。</span><span class="sxs-lookup"><span data-stu-id="83b77-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![最初のオファー](./media/1FirstOffer.png)

2. <span data-ttu-id="83b77-123">サービスにサブスクライブする組織に属するユーザーとしてログインしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="83b77-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="83b77-124">オファーの引き換えに進みます。</span><span class="sxs-lookup"><span data-stu-id="83b77-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="83b77-125">**はい、アカウントに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="83b77-125">Select **Yes, add it to my account**.</span></span>

![オファーの引き換え](./media/2RedeemFirstOffer.png)

![オファーの確認](./media/3ConfirmFirstOffer.png)

![引き換え済みオファー](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="83b77-129">Dynamics 365 Finance プレビュー 試用版</span><span class="sxs-lookup"><span data-stu-id="83b77-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="83b77-130">歓迎メールの 2 番目のオファーで同じ手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="83b77-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="83b77-131">ライセンスの割り当て</span><span class="sxs-lookup"><span data-stu-id="83b77-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83b77-132">次の手順を完了するためには、組織の Office 365 のポータルへの管理アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="83b77-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="83b77-133">[Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="83b77-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office 管理ポータル](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="83b77-135">**アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="83b77-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![ライセンスの割り当て](./media/6AssignLicenses.png)

3. <span data-ttu-id="83b77-137">Project Operations ライセンスが選択されていることを確認し、**変更の保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="83b77-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="83b77-138">Finance 試用版オファーをユーザーに割り当てる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="83b77-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="83b77-139">LCS で新しいプロジェクトを開始する</span><span class="sxs-lookup"><span data-stu-id="83b77-139">Start a new project in LCS</span></span>

<span data-ttu-id="83b77-140">トピック[LCS で新しいプロジェクトの開始](create-lcs-project.md) の説明に従って、新しい LCS プロジェクトを作成します</span><span class="sxs-lookup"><span data-stu-id="83b77-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="83b77-141">LCS プロジェクトに Azure サブスクリプションを追加する</span><span class="sxs-lookup"><span data-stu-id="83b77-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="83b77-142">このタスクを完了するには、トピック[LCS プロジェクトに Azure サブスクリプションを追加する](resource-add-azure-subscription-lcs-project.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="83b77-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="83b77-143">リソース/非在庫のシナリオの Project Operations で Finance デモ環境を展開する</span><span class="sxs-lookup"><span data-stu-id="83b77-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="83b77-144">トピック[新しい環境をプロビジョニングする](resource-provision-new-environment.md) のガイダンスに従い、展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="83b77-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="83b77-145">プレビューの[デモ環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) の展開の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="83b77-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="83b77-146">CDS 設定および構成データをインストールする</span><span class="sxs-lookup"><span data-stu-id="83b77-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="83b77-147">トピック[Common Data Service で構成データを設定および適用](resource-apply-pro-setup-config-data.md) の説明に従って、CDS の設定および構成データをインストールします。</span><span class="sxs-lookup"><span data-stu-id="83b77-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

