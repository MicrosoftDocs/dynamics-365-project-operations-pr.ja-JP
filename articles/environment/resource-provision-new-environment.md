---
title: 新しい環境をプロビジョニングする
description: このトピックは、新しい Project Operations 環境でプロビジョニングする方法について説明します。
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995492"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="9ec23-103">新しい環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="9ec23-103">Provision a new environment</span></span>

<span data-ttu-id="9ec23-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="9ec23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9ec23-105">このトピックでは、リソース/非在庫ベースのシナリオについて Dynamics 365 Project Operations の新しい環境をプロビジョニングする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="9ec23-106">LCS プロジェクトで Project Operations の自動プロビジョニングを有効にします</span><span class="sxs-lookup"><span data-stu-id="9ec23-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="9ec23-107">次の手順を使用して、LCS プロジェクトの ProjectOperations の自動プロビジョニング フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9ec23-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="9ec23-108">[LCS](https://lcs.dynamics.com/v2) に移動し、**プレビュー機能の管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="9ec23-109">**プレビュー機能** リストで、**Project Operations** 機能を選択し、Project Operations を有効にするために **プレビュー機能を有効する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="9ec23-110">このステップは、LCS プロジェクトごとに 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="9ec23-111">Project Operations 環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="9ec23-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="9ec23-112">新しい Dynamics 365 Finance[デモ環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) または[サンドボックス/運用環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) の展開を開きます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="9ec23-113">**環境プロビジョニング** ウィザードを検証します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="9ec23-114">選択したアプリケーションのバージョンが 10.0.13 以降であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9ec23-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="9ec23-115">Project Operations をプロビジョニングするには、**詳細設定** で、**Common Data Service** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="9ec23-116">**はい** を選択して **Common Data Service 設定** を有効にし、必須項目フィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="9ec23-117">件名</span><span class="sxs-lookup"><span data-stu-id="9ec23-117">Name</span></span>
  - <span data-ttu-id="9ec23-118">リージョン</span><span class="sxs-lookup"><span data-stu-id="9ec23-118">Region</span></span>
  - <span data-ttu-id="9ec23-119">言語</span><span class="sxs-lookup"><span data-stu-id="9ec23-119">Language</span></span>
  - <span data-ttu-id="9ec23-120">通貨</span><span class="sxs-lookup"><span data-stu-id="9ec23-120">Currency</span></span>
 
5. <span data-ttu-id="9ec23-121">**Common Data Service テンプレート** フィールドで、**Project Operations** を選択します</span><span class="sxs-lookup"><span data-stu-id="9ec23-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="9ec23-122">展開の環境タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="9ec23-123">サブスクリプション ベースのトライアルでは、CDS 環境を 30 日間展開できます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![展開の設定](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="9ec23-125">**同意する** を選択して利用規約サービスの利用条件を確認し、**完了** を選択して展開の設定に戻ります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![展開の同意](./media/2DeploymentConsent.png)

7. <span data-ttu-id="9ec23-127">オプション - デモ データを環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="9ec23-128">**高度な設定** に移動して、**SQL データベース構成のカスタマイズ** を選択して、**アプリケーション データベースにデータセットを指定する** を **デモ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="9ec23-129">ウィザードの残りの必須フィールドを完了し、展開を確認します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="9ec23-130">環境をプロビジョニングする時間は、環境の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="9ec23-131">プロビジョニングには最大 6 時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="9ec23-132">展開が正常に完了すると、環境は **展開** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="9ec23-133">環境が正常に展開されたことを確認するには、**ログイン** を選択して、確認のために環境にログオンします。</span><span class="sxs-lookup"><span data-stu-id="9ec23-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 環境の詳細](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="9ec23-135">Finance 環境に更新を適用する</span><span class="sxs-lookup"><span data-stu-id="9ec23-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="9ec23-136">Project Operations には、**10.0.13 (10.0.569.20009)** 以上のアプリケーション バージョンを備えた Finance 環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="9ec23-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="9ec23-137">このバージョンを受け取るには、Finance 環境に品質更新を適用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="9ec23-138">LCS では、**環境の詳細** ページの、**利用可能な更新** セクションで、**更新の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![ビューの更新](./media/5ViewUpdates.png)

2. <span data-ttu-id="9ec23-140">**バイナリ更新** ページで、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-140">On the **Binary updates** page, select **Save package.**</span></span>

![パッケージの保存](./media/6SavePackage.png)

3. <span data-ttu-id="9ec23-142">**すべて選択** をクリックし、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-142">Click **Select all** and then select **Save package**.</span></span>

![レビューと更新の保存](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="9ec23-144">パッケージの名前と説明を入力し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="9ec23-145">インターネット接続によっては、このプロセスに時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-145">Depending on the internet connection, this process might take some time.</span></span>

![パッケージを資産ライブラリにアップロード](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="9ec23-147">パッケージが保存されたら、**完了** を選択し、このパッケージを LCS プロジェクトの資産ライブラリに保存します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="9ec23-148">パッケージの保存と検証には 15 分ほどかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="9ec23-149">更新を適用するには、LCS の **環境の詳細** ページで、**メンテナンス** > **更新の適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![環境のメンテナンス](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="9ec23-151">更新リストで、作成したパッケージを選択し、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-151">In the updates list select the package you created, and select **Apply**.</span></span>

![更新の適用する](./media/10ApplyUpdates.png)

<span data-ttu-id="9ec23-153">環境サービスには時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-153">Environment servicing will take some time.</span></span> <span data-ttu-id="9ec23-154">完了すると、環境は展開された状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-154">After it is complete, the environment will return to a deployed state.</span></span>

![展開された環境](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="9ec23-156">二重書き込み接続の確立</span><span class="sxs-lookup"><span data-stu-id="9ec23-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="9ec23-157">LCS プロジェクトで、**環境の詳細** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="9ec23-158">**Common Data Service 環境情報** で、**アプリの CDS へのリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="9ec23-159">リンクが完了したら、もう一度 **アプリの CDS へのリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="9ec23-160">Finance の二重書き込みにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-160">You will be redirected to Dual Write in Finance.</span></span>

![CDS にリンク](./media/12LinktoCDS.png)

4. <span data-ttu-id="9ec23-162">**ソリューションの適用** を選択し、統合でマップされるエンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9ec23-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![ソリューションを適用する](./media/13ApplySolutions.png)

5. <span data-ttu-id="9ec23-164">**Dynamics 365 Finance and Operations 二重書き込みエンティティ マップ** と **Dynamics 365 Project Operations 二重書き込みエンティティ マップ** のソリューションを両方選択してから **適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![ソリューションの確認](./media/14ConfirmSolutions.png)

<span data-ttu-id="9ec23-166">ソリューションが適用された後、二重書き込みエンティティが環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![ソリューションの適用](./media/15ApplyingSolutions.png)

<span data-ttu-id="9ec23-168">エンティティが適用されると、使用可能なすべてのマッピングが環境に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![二重書き込みマップ](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="9ec23-170">更新後にデータ エンティティを最新の情報に更新</span><span class="sxs-lookup"><span data-stu-id="9ec23-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="9ec23-171">Finance で、**データ管理** ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-171">In Finance, go to the **Data management** workspace.</span></span>

![データ管理のワークスペース](./media/16DataManagement.png)

2. <span data-ttu-id="9ec23-173">**フレームワーク パラメータ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-173">Select the **Framework parameters** tile.</span></span>

![フレームワーク パラメータ](./media/17FrameworkParameters.png)

3. <span data-ttu-id="9ec23-175">**エンティティ設定** ページで、**エンティティ　リストを最新の情報に更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![エンティティ リストを最新の情報に更新](./media/18RefreshEntityList.png)

<span data-ttu-id="9ec23-177">最新の情報に更新するには約 20 分かかります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="9ec23-178">完了するとアラート通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-178">You will receive an alert when it is complete.</span></span>

![最新の情報に更新を確認](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="9ec23-180">Dataverse 上の Project Operations のセキュリティ設定を更新する</span><span class="sxs-lookup"><span data-stu-id="9ec23-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="9ec23-181">Dataverse 環境で Project Operations に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="9ec23-182">**設定** >  **セキュリティ** > **セキュリティ ロール** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="9ec23-183">**セキュリティ ロール** ページのロールのリストで、**二重書き込みアプリ ユーザー** を選択してから、**カスタム エンティティ** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="9ec23-184">ロールに、次の **読み込み** と **追加先** 権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="9ec23-185">**通貨為替レートのタイプ**</span><span class="sxs-lookup"><span data-stu-id="9ec23-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="9ec23-186">**勘定科目表**</span><span class="sxs-lookup"><span data-stu-id="9ec23-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="9ec23-187">**会計カレンダー**</span><span class="sxs-lookup"><span data-stu-id="9ec23-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="9ec23-188">**Ledger**</span><span class="sxs-lookup"><span data-stu-id="9ec23-188">**Ledger**</span></span>

5. <span data-ttu-id="9ec23-189">セキュリティ ロールが更新されたら、**設定** > **セキュリティ** > **チーム** に移動し、**ローカル ビジネス オーナー** チーム ビューで既定のチームを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="9ec23-190">**ロールの管理** を選択して、**二重書き込みアプリ ユーザー** のセキュリティ特権がこのチームに適用されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="9ec23-191">Project Operations の二重書き込みマップを実行する</span><span class="sxs-lookup"><span data-stu-id="9ec23-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="9ec23-192">LCS プロジェクトで、**環境の詳細** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="9ec23-193">**Common Data Service 環境情報** で、**アプリの CDS へのリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="9ec23-194">リンクを選択すると、マッピングでエンティティのリストにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="9ec23-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="9ec23-195">次の表の説明に従って、マップを開始します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="9ec23-196">記載されている順序に従ってください。</span><span class="sxs-lookup"><span data-stu-id="9ec23-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="9ec23-197">**エンティティ マップ**</span><span class="sxs-lookup"><span data-stu-id="9ec23-197">**Entity Map**</span></span> | <span data-ttu-id="9ec23-198">**エンティティを最新の情報に更新**</span><span class="sxs-lookup"><span data-stu-id="9ec23-198">**Refresh entity**</span></span> | <span data-ttu-id="9ec23-199">**初期同期**</span><span class="sxs-lookup"><span data-stu-id="9ec23-199">**Initial sync**</span></span> | <span data-ttu-id="9ec23-200">**初期同期のマスター**</span><span class="sxs-lookup"><span data-stu-id="9ec23-200">**Master for initial sync**</span></span> | <span data-ttu-id="9ec23-201">**前提条件の実行**</span><span class="sxs-lookup"><span data-stu-id="9ec23-201">**Run prerequisites**</span></span> | <span data-ttu-id="9ec23-202">**前提条件の初期同期**</span><span class="sxs-lookup"><span data-stu-id="9ec23-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="9ec23-203">**すべての会社のプロジェクト リソース ロール (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="9ec23-204">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-204">No</span></span> | <span data-ttu-id="9ec23-205">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-205">Yes</span></span> | <span data-ttu-id="9ec23-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9ec23-206">Common Data Service</span></span> | <span data-ttu-id="9ec23-207">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-207">No</span></span> | <span data-ttu-id="9ec23-208">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-208">N\A</span></span> |
| <span data-ttu-id="9ec23-209">**法人 (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="9ec23-210">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-210">No</span></span> | <span data-ttu-id="9ec23-211">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-211">Yes</span></span> | <span data-ttu-id="9ec23-212">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="9ec23-212">Finance and Operations apps</span></span> | <span data-ttu-id="9ec23-213">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-213">No</span></span> | <span data-ttu-id="9ec23-214">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-214">N\A</span></span> |
| <span data-ttu-id="9ec23-215">**元帳 (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="9ec23-216">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-216">No</span></span> | <span data-ttu-id="9ec23-217">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-217">Yes</span></span> | <span data-ttu-id="9ec23-218">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="9ec23-218">Finance and Operations apps</span></span> | <span data-ttu-id="9ec23-219">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-219">Yes</span></span> | <span data-ttu-id="9ec23-220">はい、Finance and Operations アプリです</span><span class="sxs-lookup"><span data-stu-id="9ec23-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="9ec23-221">**Project Operations 統合実績 (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="9ec23-222">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-222">No</span></span> | <span data-ttu-id="9ec23-223">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-223">No</span></span> | <span data-ttu-id="9ec23-224">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-224">N\A</span></span> | <span data-ttu-id="9ec23-225">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-225">Yes</span></span> | <span data-ttu-id="9ec23-226">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-226">No</span></span> |
| <span data-ttu-id="9ec23-227">**プロジェクト 契約品目 (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="9ec23-228">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-228">No</span></span> | <span data-ttu-id="9ec23-229">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-229">No</span></span> | <span data-ttu-id="9ec23-230">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-230">N\A</span></span> | <span data-ttu-id="9ec23-231">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-231">No</span></span> | <span data-ttu-id="9ec23-232">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-232">No</span></span> |
| <span data-ttu-id="9ec23-233">**プロジェクト トランザクションの関連付けにおける統合エンティティ (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="9ec23-234">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-234">No</span></span> | <span data-ttu-id="9ec23-235">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-235">No</span></span> | <span data-ttu-id="9ec23-236">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-236">N\A</span></span> | <span data-ttu-id="9ec23-237">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-237">No</span></span> | <span data-ttu-id="9ec23-238">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-238">N\A</span></span> |
| <span data-ttu-id="9ec23-239">**Project Operations 統合契約品目のマイルストーン (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="9ec23-240">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-240">No</span></span> | <span data-ttu-id="9ec23-241">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-241">No</span></span> | <span data-ttu-id="9ec23-242">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-242">N\A</span></span> | <span data-ttu-id="9ec23-243">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-243">No</span></span> | <span data-ttu-id="9ec23-244">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-244">N\A</span></span> |
| <span data-ttu-id="9ec23-245">**経費見積もりのための Project Operations 統合エンティティ (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="9ec23-246">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-246">No</span></span> | <span data-ttu-id="9ec23-247">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-247">No</span></span> | <span data-ttu-id="9ec23-248">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-248">N\A</span></span> | <span data-ttu-id="9ec23-249">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-249">No</span></span> | <span data-ttu-id="9ec23-250">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-250">N\A</span></span> |
| <span data-ttu-id="9ec23-251">**Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="9ec23-252">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-252">No</span></span> | <span data-ttu-id="9ec23-253">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-253">No</span></span> | <span data-ttu-id="9ec23-254">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-254">N\A</span></span> | <span data-ttu-id="9ec23-255">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-255">No</span></span> | <span data-ttu-id="9ec23-256">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-256">N\A</span></span> |
| <span data-ttu-id="9ec23-257">**Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="9ec23-258">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-258">Yes</span></span> | <span data-ttu-id="9ec23-259">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-259">No</span></span> | <span data-ttu-id="9ec23-260">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-260">N\A</span></span> | <span data-ttu-id="9ec23-261">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-261">No</span></span> | <span data-ttu-id="9ec23-262">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-262">N\A</span></span> |
| <span data-ttu-id="9ec23-263">**時間見積もりのための Project Operations 統合エンティティ (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="9ec23-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="9ec23-264">有効</span><span class="sxs-lookup"><span data-stu-id="9ec23-264">Yes</span></span> | <span data-ttu-id="9ec23-265">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-265">No</span></span> | <span data-ttu-id="9ec23-266">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-266">N\A</span></span> | <span data-ttu-id="9ec23-267">無効</span><span class="sxs-lookup"><span data-stu-id="9ec23-267">No</span></span> | <span data-ttu-id="9ec23-268">N\A</span><span class="sxs-lookup"><span data-stu-id="9ec23-268">N\A</span></span> |


4. <span data-ttu-id="9ec23-269">エンティティを最新の情報に更新するには、マップ名を選択してから、**エンティティを最新の状態に更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![マップを最新の情報に更新](./media/20RefreshMapping.png)

5. <span data-ttu-id="9ec23-271">最新の情報に更新が完了したら、マップを実行します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="9ec23-272">次のマップを有効にする前に、テーブル内のマップが **実行** の状態にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9ec23-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="9ec23-273">前提条件の数が多いマップの実行には、時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ec23-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="9ec23-274">前提条件を使用してマップを実行するには、**関連するエンティティ マップの表示** 切り替えを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9ec23-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="9ec23-275">テーブルに **前提条件の初期同期** が **いいえ** を示している場合、実行する前に、すべての前提条件マップで **初期同期** フラグが **オフ** であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9ec23-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![マップを実行](./media/21RunMap.png)

6. <span data-ttu-id="9ec23-277">プロジェクトに関連するすべてのマップが実行状態にあることを検証します。</span><span class="sxs-lookup"><span data-stu-id="9ec23-277">Validate all project related maps are in the running state.</span></span>

![実行中のすべてのマップ](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="9ec23-279">Project Operations 用の CDS で構成データを適用する (オプション)</span><span class="sxs-lookup"><span data-stu-id="9ec23-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="9ec23-280">Finance 環境にデモ データを適用した場合は、デモ データを CD S環境に適用するために [Project Operations 用の Common Data Service で構成データの設定と適用](resource-apply-pro-setup-config-data.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ec23-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="9ec23-281">これで、Project Operations環境がプロビジョニングおよび構成されました。</span><span class="sxs-lookup"><span data-stu-id="9ec23-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]