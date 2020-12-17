---
title: 新しい環境をプロビジョニングする
description: このトピックは、新しい Project Operations 環境でプロビジョニングする方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642983"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="dde92-103">新しい環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="dde92-103">Provision a new environment</span></span>

<span data-ttu-id="dde92-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="dde92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dde92-105">このトピックでは、リソース/非在庫ベースのシナリオについて Dynamics 365 Project Operations の新しい環境をプロビジョニングする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="dde92-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="dde92-106">LCS プロジェクトで Project Operations の自動プロビジョニングを有効にします</span><span class="sxs-lookup"><span data-stu-id="dde92-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="dde92-107">次の手順を使用して、LCS プロジェクトの ProjectOperations の自動プロビジョニング フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="dde92-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="dde92-108">[LCS](https://lcs.dynamics.com/v2) に移動し、**プレビュー機能の管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="dde92-109">**プレビュー機能** リストで、**Project Operations** 機能を選択し、Project Operations を有効にするために **プレビュー機能を有効する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="dde92-110">このステップは、LCS プロジェクトごとに 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="dde92-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="dde92-111">Project Operations 環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="dde92-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="dde92-112">新しい Dynamics 365 Finance[デモ環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) または[サンドボックス/運用環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) の展開を開きます。</span><span class="sxs-lookup"><span data-stu-id="dde92-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="dde92-113">**環境プロビジョニング** ウィザードを検証します。</span><span class="sxs-lookup"><span data-stu-id="dde92-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="dde92-114">選択したアプリケーションのバージョンが 10.0.13 以降であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dde92-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="dde92-115">Project Operations をプロビジョニングするには、**詳細設定** で、**Common Data Service** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="dde92-116">**はい** を選択して **Common Data Service 設定** を有効にし、必須項目フィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="dde92-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="dde92-117">件名</span><span class="sxs-lookup"><span data-stu-id="dde92-117">Name</span></span>
  - <span data-ttu-id="dde92-118">リージョン</span><span class="sxs-lookup"><span data-stu-id="dde92-118">Region</span></span>
  - <span data-ttu-id="dde92-119">言語</span><span class="sxs-lookup"><span data-stu-id="dde92-119">Language</span></span>
  - <span data-ttu-id="dde92-120">通貨</span><span class="sxs-lookup"><span data-stu-id="dde92-120">Currency</span></span>
 
5. <span data-ttu-id="dde92-121">**Common Data Service テンプレート** フィールドで、**Project Operations** を選択します</span><span class="sxs-lookup"><span data-stu-id="dde92-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="dde92-122">展開の環境タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="dde92-123">サブスクリプション ベースのトライアルでは、CDS 環境を 30 日間展開できます。</span><span class="sxs-lookup"><span data-stu-id="dde92-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![展開の設定](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="dde92-125">**同意する** を選択して利用規約サービスの利用条件を確認し、**完了** を選択して展開の設定に戻ります。</span><span class="sxs-lookup"><span data-stu-id="dde92-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![展開の同意](./media/2DeploymentConsent.png)

7. <span data-ttu-id="dde92-127">ウィザードの残りの必須フィールドを完了し、展開を確認します。</span><span class="sxs-lookup"><span data-stu-id="dde92-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="dde92-128">環境プロビジョニングの時間は、環境タイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="dde92-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="dde92-129">プロビジョニングには最大 6 時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dde92-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="dde92-130">展開が正常に完了すると、環境は **展開** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="dde92-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="dde92-131">環境が正常に展開されたことを確認するには、**ログイン** を選択し、確認のために環境にログオンします。</span><span class="sxs-lookup"><span data-stu-id="dde92-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 環境の詳細](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="dde92-133">Project Operations Finance のデモ データを適用する (オプションのステップ)</span><span class="sxs-lookup"><span data-stu-id="dde92-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="dde92-134">[この記事](resource-apply-finance-demo-data.md) で説明されているように、Project Operations Finance のデモ データを10.0.13 サービス リリースのクラウド ホスト環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="dde92-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="dde92-135">Finance 環境に更新を適用する</span><span class="sxs-lookup"><span data-stu-id="dde92-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="dde92-136">Project Operations には、**10.0.13 (10.0.569.20009)** 以上のアプリケーション バージョンを備えた Finance 環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="dde92-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="dde92-137">このバージョンを受け取るには、Finance 環境に品質更新を適用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="dde92-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="dde92-138">LCS では、**環境の詳細** ページの、**利用可能な更新** セクションで、**更新の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![ビューの更新](./media/5ViewUpdates.png)

2. <span data-ttu-id="dde92-140">**バイナリ更新** ページで、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-140">On the **Binary updates** page, select **Save package.**</span></span>

![パッケージの保存](./media/6SavePackage.png)

3. <span data-ttu-id="dde92-142">**すべて選択** をクリックし、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-142">Click **Select all** and then select **Save package**.</span></span>

![レビューと更新の保存](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="dde92-144">パッケージの名前と説明を入力し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="dde92-145">インターネット接続によっては、このプロセスに時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dde92-145">Depending on the internet connection, this process might take some time.</span></span>

![パッケージを資産ライブラリにアップロード](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="dde92-147">パッケージが保存されたら、**完了** を選択し、このパッケージを LCS プロジェクトの資産ライブラリに保存します。</span><span class="sxs-lookup"><span data-stu-id="dde92-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="dde92-148">パッケージの保存と検証には 15 分ほどかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dde92-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="dde92-149">更新を適用するには、LCS の **環境の詳細** ページで、**メンテナンス** > **更新の適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![環境のメンテナンス](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="dde92-151">更新リストで、作成したパッケージを選択し、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-151">In the updates list select the package you created, and select **Apply**.</span></span>

![更新の適用する](./media/10ApplyUpdates.png)

<span data-ttu-id="dde92-153">環境サービスには時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="dde92-153">Environment servicing will take some time.</span></span> <span data-ttu-id="dde92-154">完了すると、環境は展開された状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="dde92-154">After it is complete, the environment will return to a deployed state.</span></span>

![展開された環境](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="dde92-156">二重書き込み接続の確立</span><span class="sxs-lookup"><span data-stu-id="dde92-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="dde92-157">LCS プロジェクトで、**環境の詳細** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="dde92-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="dde92-158">**Common Data Service 環境情報** で、**アプリの CDS へのリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="dde92-159">リンクが完了したら、もう一度 **アプリの CDS へのリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="dde92-160">Finance の二重書き込みにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="dde92-160">You will be redirected to Dual Write in Finance.</span></span>

![CDS にリンク](./media/12LinktoCDS.png)

4. <span data-ttu-id="dde92-162">**ソリューションの適用** を選択し、統合でマップされるエンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="dde92-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![ソリューションを適用する](./media/13ApplySolutions.png)

5. <span data-ttu-id="dde92-164">**Dynamics 365 Finance and Operations 二重書き込みエンティティ マップ** と **Dynamics 365 Project Operations 二重書き込みエンティティ マップ** のソリューションを両方選択してから **適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![ソリューションの確認](./media/14ConfirmSolutions.png)

<span data-ttu-id="dde92-166">ソリューションが適用された後、二重書き込みエンティティが環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="dde92-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![ソリューションの適用](./media/15ApplyingSolutions.png)

<span data-ttu-id="dde92-168">エンティティが適用されると、使用可能なすべてのマッピングが環境に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="dde92-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![二重書き込みマップ](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="dde92-170">更新後にデータ エンティティを最新の情報に更新</span><span class="sxs-lookup"><span data-stu-id="dde92-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="dde92-171">Finance で、**データ管理** ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="dde92-171">In Finance, go to the **Data management** workspace.</span></span>

![データ管理のワークスペース](./media/16DataManagement.png)

2. <span data-ttu-id="dde92-173">**フレームワーク パラメータ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-173">Select the **Framework parameters** tile.</span></span>

![フレームワーク パラメータ](./media/17FrameworkParameters.png)

3. <span data-ttu-id="dde92-175">**エンティティ設定** ページで、**エンティティ　リストを最新の情報に更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![エンティティ リストを最新の情報に更新](./media/18RefreshEntityList.png)

<span data-ttu-id="dde92-177">最新の情報に更新するには約 20 分かかります。</span><span class="sxs-lookup"><span data-stu-id="dde92-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="dde92-178">完了するとアラート通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dde92-178">You will receive an alert when it is complete.</span></span>

![最新の情報に更新を確認](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="dde92-180">Project Operations の二重書き込みマップを実行する</span><span class="sxs-lookup"><span data-stu-id="dde92-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="dde92-181">LCS プロジェクトで、**環境の詳細** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="dde92-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="dde92-182">**Common Data Service 環境情報** で、**アプリの CDS へのリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="dde92-183">リンクを選択すると、マッピングでエンティティのリストにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="dde92-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="dde92-184">次の表の説明に従って、マップを開始します。</span><span class="sxs-lookup"><span data-stu-id="dde92-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="dde92-185">記載されている順序に従ってください。</span><span class="sxs-lookup"><span data-stu-id="dde92-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="dde92-186">**エンティティ マップ**</span><span class="sxs-lookup"><span data-stu-id="dde92-186">**Entity Map**</span></span> | <span data-ttu-id="dde92-187">**エンティティを最新の情報に更新**</span><span class="sxs-lookup"><span data-stu-id="dde92-187">**Refresh entity**</span></span> | <span data-ttu-id="dde92-188">**初期同期**</span><span class="sxs-lookup"><span data-stu-id="dde92-188">**Initial sync**</span></span> | <span data-ttu-id="dde92-189">**初期同期のマスター**</span><span class="sxs-lookup"><span data-stu-id="dde92-189">**Master for initial sync**</span></span> | <span data-ttu-id="dde92-190">**前提条件の実行**</span><span class="sxs-lookup"><span data-stu-id="dde92-190">**Run prerequisites**</span></span> | <span data-ttu-id="dde92-191">**前提条件の初期同期**</span><span class="sxs-lookup"><span data-stu-id="dde92-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="dde92-192">**すべての会社のプロジェクト リソース ロール (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="dde92-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="dde92-193">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-193">No</span></span> | <span data-ttu-id="dde92-194">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-194">Yes</span></span> | <span data-ttu-id="dde92-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dde92-195">Common Data Service</span></span> | <span data-ttu-id="dde92-196">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-196">No</span></span> | <span data-ttu-id="dde92-197">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-197">N\A</span></span> |
| <span data-ttu-id="dde92-198">**法人 (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="dde92-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="dde92-199">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-199">No</span></span> | <span data-ttu-id="dde92-200">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-200">Yes</span></span> | <span data-ttu-id="dde92-201">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="dde92-201">Finance and Operations apps</span></span> | <span data-ttu-id="dde92-202">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-202">No</span></span> | <span data-ttu-id="dde92-203">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-203">N\A</span></span> |
| <span data-ttu-id="dde92-204">**元帳 (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="dde92-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="dde92-205">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-205">No</span></span> | <span data-ttu-id="dde92-206">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-206">Yes</span></span> | <span data-ttu-id="dde92-207">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="dde92-207">Finance and Operations apps</span></span> | <span data-ttu-id="dde92-208">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-208">Yes</span></span> | <span data-ttu-id="dde92-209">はい、Finance and Operations アプリです</span><span class="sxs-lookup"><span data-stu-id="dde92-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="dde92-210">**Project Operations 統合実績 (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="dde92-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="dde92-211">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-211">No</span></span> | <span data-ttu-id="dde92-212">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-212">No</span></span> | <span data-ttu-id="dde92-213">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-213">N\A</span></span> | <span data-ttu-id="dde92-214">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-214">Yes</span></span> | <span data-ttu-id="dde92-215">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-215">No</span></span> |
| <span data-ttu-id="dde92-216">**プロジェクト 契約品目 (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="dde92-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="dde92-217">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-217">No</span></span> | <span data-ttu-id="dde92-218">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-218">No</span></span> | <span data-ttu-id="dde92-219">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-219">N\A</span></span> | <span data-ttu-id="dde92-220">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-220">No</span></span> | <span data-ttu-id="dde92-221">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-221">No</span></span> |
| <span data-ttu-id="dde92-222">**プロジェクト トランザクションの関連付けにおける統合エンティティ (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="dde92-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="dde92-223">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-223">No</span></span> | <span data-ttu-id="dde92-224">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-224">No</span></span> | <span data-ttu-id="dde92-225">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-225">N\A</span></span> | <span data-ttu-id="dde92-226">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-226">No</span></span> | <span data-ttu-id="dde92-227">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-227">N\A</span></span> |
| <span data-ttu-id="dde92-228">**Project Operations 統合契約品目のマイルストーン (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="dde92-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="dde92-229">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-229">No</span></span> | <span data-ttu-id="dde92-230">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-230">No</span></span> | <span data-ttu-id="dde92-231">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-231">N\A</span></span> | <span data-ttu-id="dde92-232">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-232">No</span></span> | <span data-ttu-id="dde92-233">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-233">N\A</span></span> |
| <span data-ttu-id="dde92-234">**経費見積もりのための Project Operations 統合エンティティ (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="dde92-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="dde92-235">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-235">No</span></span> | <span data-ttu-id="dde92-236">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-236">No</span></span> | <span data-ttu-id="dde92-237">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-237">N\A</span></span> | <span data-ttu-id="dde92-238">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-238">No</span></span> | <span data-ttu-id="dde92-239">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-239">N\A</span></span> |
| <span data-ttu-id="dde92-240">**Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="dde92-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="dde92-241">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-241">No</span></span> | <span data-ttu-id="dde92-242">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-242">No</span></span> | <span data-ttu-id="dde92-243">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-243">N\A</span></span> | <span data-ttu-id="dde92-244">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-244">No</span></span> | <span data-ttu-id="dde92-245">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-245">N\A</span></span> |
| <span data-ttu-id="dde92-246">**Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="dde92-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="dde92-247">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-247">Yes</span></span> | <span data-ttu-id="dde92-248">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-248">No</span></span> | <span data-ttu-id="dde92-249">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-249">N\A</span></span> | <span data-ttu-id="dde92-250">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-250">No</span></span> | <span data-ttu-id="dde92-251">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-251">N\A</span></span> |
| <span data-ttu-id="dde92-252">**時間見積もりのための Project Operations 統合エンティティ (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="dde92-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="dde92-253">有効</span><span class="sxs-lookup"><span data-stu-id="dde92-253">Yes</span></span> | <span data-ttu-id="dde92-254">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-254">No</span></span> | <span data-ttu-id="dde92-255">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-255">N\A</span></span> | <span data-ttu-id="dde92-256">無効</span><span class="sxs-lookup"><span data-stu-id="dde92-256">No</span></span> | <span data-ttu-id="dde92-257">N\A</span><span class="sxs-lookup"><span data-stu-id="dde92-257">N\A</span></span> |


4. <span data-ttu-id="dde92-258">エンティティを最新の情報に更新するには、マップ名を選択してから、**エンティティを最新の状態に更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dde92-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![マップを最新の情報に更新](./media/20RefreshMapping.png)

5. <span data-ttu-id="dde92-260">最新の情報に更新が完了したら、マップを実行します。</span><span class="sxs-lookup"><span data-stu-id="dde92-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="dde92-261">次のマップを有効にする前に、テーブル内のマップが **実行** の状態にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dde92-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="dde92-262">前提条件の数が多いマップの実行には、時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dde92-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="dde92-263">前提条件を使用してマップを実行するには、**関連するエンティティ マップの表示** 切り替えを有効にします。</span><span class="sxs-lookup"><span data-stu-id="dde92-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="dde92-264">テーブルに **前提条件の初期同期** が **いいえ** を示している場合、実行する前に、すべての前提条件マップで **初期同期** フラグが **オフ** であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dde92-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![マップを実行](./media/21RunMap.png)

6. <span data-ttu-id="dde92-266">プロジェクトに関連するすべてのマップが実行状態にあることを検証します。</span><span class="sxs-lookup"><span data-stu-id="dde92-266">Validate all project related maps are in the running state.</span></span>

![実行中のすべてのマップ](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="dde92-268">Project Operations 用の CDS で構成データを適用する (オプション)</span><span class="sxs-lookup"><span data-stu-id="dde92-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="dde92-269">Finance 環境にデモ データを適用した場合は、デモ データを CD S環境に適用するために [Project Operations 用の Common Data Service で構成データの設定と適用](resource-apply-pro-setup-config-data.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dde92-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="dde92-270">これで、Project Operations環境がプロビジョニングおよび構成されました。</span><span class="sxs-lookup"><span data-stu-id="dde92-270">Your Project Operations environment is now provisioned and configured.</span></span> 
