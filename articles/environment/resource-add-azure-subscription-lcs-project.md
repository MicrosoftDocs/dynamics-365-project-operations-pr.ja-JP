---
title: LCS プロジェクトに Azure サブスクリプションを追加する
description: このトピックは、Azure サブスクリプションを LCS プロジェクトに接続する方法に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289915"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="15973-103">LCS プロジェクトに Azure サブスクリプションを追加する</span><span class="sxs-lookup"><span data-stu-id="15973-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="15973-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="15973-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="15973-105">クラウド ホスト環境は、既存の Azure サブスクリプションを使用して展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15973-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="15973-106">このトピックは、既存の Azure サブスクリプションを LCS プロジェクトに接続する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="15973-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="15973-107">管理者の同意を与える</span><span class="sxs-lookup"><span data-stu-id="15973-107">Grant admin consent</span></span>

1. <span data-ttu-id="15973-108">LCS プロジェクトの、**環境** セクションで、**Microsoft Azure 設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure の設定](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="15973-110">**プロジェクト設定** ページの、**Azure コネクタ** タブで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="15973-111">これにより、環境をこのプロジェクトに展開できます。</span><span class="sxs-lookup"><span data-stu-id="15973-111">This allows environments to be deployed to this project.</span></span>

![Azure コネクタ](./media/2AzureConnectors.png)

3. <span data-ttu-id="15973-113">もう一度 **承認** を選択して、管理者の同意を提供します。</span><span class="sxs-lookup"><span data-stu-id="15973-113">Select **Authorize** again to provide admin consent.</span></span>

![管理者の同意を与える](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="15973-115">アクセス許可の要求を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="15973-115">Accept the permissions request.</span></span>

![アクセス許可の要求を受け入れます](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="15973-117">これで承認は完了です。</span><span class="sxs-lookup"><span data-stu-id="15973-117">The authorization is now complete.</span></span> 

![承認に成功しました](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a> <span data-ttu-id="15973-119">Dynamics Deployment Services に Azure サブスクリプションへのアクセスを提供します</span><span class="sxs-lookup"><span data-stu-id="15973-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="15973-120">[Microsoft Azure 請求](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) に移動し、サブスクリプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="15973-121">Dynamics Deployment Servicesは、環境を展開できるようにするために、このサブスクリプションにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="15973-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure のサブスクリプションの詳細](./media/6AzureSubscription.png)

2. <span data-ttu-id="15973-123">ナビゲーション ウィンドウで **アクセス制御 (IAM)** を選択し、**ロールの割り当ての追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="15973-124">右側のスライダーで、**共同作成者ロール** を選択し、提供されたリストで、**Dynamics Deployment Services** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="15973-125">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-125">Select **Save**.</span></span>

![サブスクリプション アクセス](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="15973-127">LCS プロジェクトにサブスクリプション コネクタを追加する</span><span class="sxs-lookup"><span data-stu-id="15973-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="15973-128">LCS プロジェクトの、**Microsoft Azure 設定** ページで、**追加** を選択して、新しいコネクタを追加します。</span><span class="sxs-lookup"><span data-stu-id="15973-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="15973-129">Azure サブスクリプション ID を入力してください。</span><span class="sxs-lookup"><span data-stu-id="15973-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="15973-130">[Azure portal](https://ms.portal.azure.com/)の、画面の左下にある **設定** で Azure サブスクリプション ID を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="15973-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="15973-131">**Azure Resource Manager を使用するための構成** フィールドで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="15973-132">Azure のサブスクリプション AAD テナント ドメインが、使用しているドメイン所有の Azure サブスクリプションと一致することを確認し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="15973-133">**Microsoft Azure セットアップ** 画面で、確認のために **次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="15973-134">この画面でエラーが発生した場合は、このトピックの[Dynamics Deployment Servicesに Azure サブスクリプションへのアクセスを提供する](#provide) セクションに戻り、すべての手順を完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="15973-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="15973-135">Azure 管理証明書 をコンピューターのローカル フォルダーにダウンロードし、**設定** > **管理証明書** に移動して Azure 管理ポータルにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="15973-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="15973-136">この証明書により、LCS がユーザーに代わって Azure と通信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="15973-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="15973-137">ユーザーがサブスクリプションにアクセスできる場合は、この手順をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="15973-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="15973-138">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-138">Select  **Next**.</span></span>
8. <span data-ttu-id="15973-139">展開する Azure リージョンを選択し、このシステムを使用する予定の場所に近いデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="15973-140">**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15973-140">Select  **Connect**.</span></span>

<span data-ttu-id="15973-141">これで、Azure サブスクリプションが正常に接続されました。</span><span class="sxs-lookup"><span data-stu-id="15973-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="15973-142">これで、Dynamics 365 Finance のクラウド ホスト環境を展開できます。</span><span class="sxs-lookup"><span data-stu-id="15973-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]