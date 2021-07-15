---
title: リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします
description: このトピックは、リソース/非在庫ベースのシナリオ向け Project Operations をサブスクライブして展開する方法について説明します。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334833"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="021b1-103">リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします</span><span class="sxs-lookup"><span data-stu-id="021b1-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="021b1-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="021b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="021b1-105">このトピックでは、試用版のオファーに登録して、リソース/非ストックベースのシナリオ用に Project Operations 環境をデプロイする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="021b1-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="021b1-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="021b1-106">Prerequisites</span></span>
- <span data-ttu-id="021b1-107">プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="021b1-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="021b1-108">最初のオファーの引き換え時にテナントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="021b1-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="021b1-109">Finance 環境を展開するには、環境ごとに請求される有効な Azure サブスクリプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="021b1-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="021b1-110">組織の既存のサブスクリプションを使用するか、[Azure トライアル](https://azure.microsoft.com/en-us/free/) を使用して開始できます。</span><span class="sxs-lookup"><span data-stu-id="021b1-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="021b1-111">CDS 環境は、30 日間限定で無料で提供されます。</span><span class="sxs-lookup"><span data-stu-id="021b1-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="021b1-112">このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。</span><span class="sxs-lookup"><span data-stu-id="021b1-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="021b1-113">このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="021b1-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="021b1-114">試用版はテナントでの単一回の使用となります。</span><span class="sxs-lookup"><span data-stu-id="021b1-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="021b1-115">試用版は 1 度しか実行できません。</span><span class="sxs-lookup"><span data-stu-id="021b1-115">You can only run a trial one time.</span></span> <span data-ttu-id="021b1-116">試用版に特化した、新しいテナントを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="021b1-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="021b1-117">Dynamics 365 Project Operations (CE) - プレビュー試用版</span><span class="sxs-lookup"><span data-stu-id="021b1-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="021b1-118">開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="021b1-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="021b1-119">[Project Operations 試用版](https://aka.ms/try-po)にアクセスし、 最初のオファーコードを **Dynamics 365 Project Operations** こちらで引き換えます。</span><span class="sxs-lookup"><span data-stu-id="021b1-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="021b1-120">注文を確認します。</span><span class="sxs-lookup"><span data-stu-id="021b1-120">Confirm your order.</span></span>

  <span data-ttu-id="021b1-121">オファーが正常に引き換えられたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="021b1-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="021b1-122">Dynamics 365 Finance プレビュー 試用版</span><span class="sxs-lookup"><span data-stu-id="021b1-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="021b1-123">[Dynamics 365 for Finance プレビューの試用版](https://aka.ms/trypoche)にアクセスし、「クラウドホスト環境に登録する」のオファーを使用して、前述のセクションに記載の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="021b1-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="021b1-124">ライセンスの割り当て</span><span class="sxs-lookup"><span data-stu-id="021b1-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="021b1-125">次の手順を完了するには、組織の Microsoft 365 ポータルへの管理アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="021b1-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="021b1-126">[Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="021b1-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="021b1-127">**アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="021b1-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="021b1-128">**Dynamics 365 Project Operations** のライセンスが選択されていることを確認し、**変更を保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="021b1-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="021b1-129">Finance 試用版オファーをユーザーに割り当てる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="021b1-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="021b1-130">LCS で新しいプロジェクトを開始する</span><span class="sxs-lookup"><span data-stu-id="021b1-130">Start a new project in LCS</span></span>

<span data-ttu-id="021b1-131">トピック[LCS で新しいプロジェクトの開始](create-lcs-project.md) の説明に従って、新しい LCS プロジェクトを作成します</span><span class="sxs-lookup"><span data-stu-id="021b1-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="021b1-132">LCS プロジェクトに Azure サブスクリプションを追加する</span><span class="sxs-lookup"><span data-stu-id="021b1-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="021b1-133">このタスクを完了するには、トピック[LCS プロジェクトに Azure サブスクリプションを追加する](resource-add-azure-subscription-lcs-project.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="021b1-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="021b1-134">リソース/非在庫のシナリオの Project Operations で Finance デモ環境を展開する</span><span class="sxs-lookup"><span data-stu-id="021b1-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="021b1-135">トピック[新しい環境をプロビジョニングする](resource-provision-new-environment.md) のガイダンスに従い、展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="021b1-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="021b1-136">プレビューの[デモ環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) の展開の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="021b1-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="021b1-137">CDS 設定および構成データをインストールする</span><span class="sxs-lookup"><span data-stu-id="021b1-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="021b1-138">トピック[Common Data Service で構成データを設定および適用](resource-apply-pro-setup-config-data.md) の説明に従って、CDS の設定および構成データをインストールします。</span><span class="sxs-lookup"><span data-stu-id="021b1-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="021b1-139">この手順は、Finance のデモ環境がデプロイされ、デモデータの準備ができてから行ってください。</span><span class="sxs-lookup"><span data-stu-id="021b1-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
