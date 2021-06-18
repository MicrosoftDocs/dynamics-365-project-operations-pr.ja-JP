---
title: Finance 環境で Project Operations を更新する
description: このトピックでは、Dynamics 365 Finance 環境で Project Operations をアップデートする方法について説明します。
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011062"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="7d732-103">Finance 環境で Project Operations を更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="7d732-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7d732-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="7d732-105">このトピックでは、 Dynamics 365 Finance 環境で Dynamics 365 Project Operations を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7d732-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="7d732-106">Project Operationsを Update 5 (UR5) に更新するために必要な手順は 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="7d732-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="7d732-107">パッケージをプレビュー プロジェクトにインポートする</span><span class="sxs-lookup"><span data-stu-id="7d732-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="7d732-108">更新プログラムを適用する</span><span class="sxs-lookup"><span data-stu-id="7d732-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="7d732-109">Dataverse 環境を更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="7d732-110">パッケージを LCS プロジェクトにインポートする</span><span class="sxs-lookup"><span data-stu-id="7d732-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="7d732-111">[Lifecycle Services (LCS)](https://lcs.dynamics.com/) にプロジェクト オーナーまたは環境マネージャーとしてログインします。</span><span class="sxs-lookup"><span data-stu-id="7d732-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="7d732-112">プロジェクトのリストから、LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="7d732-113">**プロジェクト** ページの **環境** グループで、更新する環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="7d732-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="7d732-114">環境が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d732-114">Verify that the environment is running.</span></span> <span data-ttu-id="7d732-115">起動していない場合は、環境を起動してください。</span><span class="sxs-lookup"><span data-stu-id="7d732-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="7d732-116">**利用可能な更新プログラム** の **新しいリリース** 下のセクションで、 10.0.15 に対する **更新の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![更新の表示ボタン](media/view-update.png)

6. <span data-ttu-id="7d732-118">**バイナリ更新** ページで、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="7d732-119">**更新のレビューと保存** ページで、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="7d732-120">**パッケージをアセット ライブラリに保存** ペインが表示されたら、名前を入力し、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="7d732-121">LCS がパッケージの保存を完了すると、**完了** ボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="7d732-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="7d732-122">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-122">Select **Done**.</span></span> <span data-ttu-id="7d732-123">LCS がパッケージを検証します。</span><span class="sxs-lookup"><span data-stu-id="7d732-123">LCS will verify the package.</span></span> <span data-ttu-id="7d732-124">確認には数分から最大 1 時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d732-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="7d732-125">パッケージ更新プログラムを適用する</span><span class="sxs-lookup"><span data-stu-id="7d732-125">Apply the package update</span></span>

1. <span data-ttu-id="7d732-126">LCS の **環境の詳細** ページで、**メンテナンス** > **更新プログラムの適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="7d732-127">リストから、前に保存したパッケージを選択してから、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="7d732-128">**はい** をクリックして、パッケージを展開することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d732-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![パッケージ展開の確認ダイアログボックス](media/confirm-package-deployment.png)

4. <span data-ttu-id="7d732-130">**はい** をクリックして、アプリケーションを更新することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d732-130">Select **Yes** to confirm that you want to update the application.</span></span>

![アプリケーション更新の確認ダイアログボックス](media/confirm-application-update.png)

<span data-ttu-id="7d732-132">展開とアプリケーションの更新が開始されます。</span><span class="sxs-lookup"><span data-stu-id="7d732-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="7d732-133">**環境の詳細** ページの右上隅に、環境ステータスが **サービス提供中** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7d732-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="7d732-134">約 2 時間で、更新が完了します。</span><span class="sxs-lookup"><span data-stu-id="7d732-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="7d732-135">アプリケーション リリース情報は **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** に更新され、環境ステータスは **展開済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7d732-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="7d732-136">Dataverse 環境を更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="7d732-137">[Power Platform 管理センター](https://admin.powerplatform.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7d732-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="7d732-138">リストで、Project Operations のインストールに使用した環境を見つけて開きます。</span><span class="sxs-lookup"><span data-stu-id="7d732-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="7d732-139">**環境** ページで、**リソース** > **Dynamics 365アプリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="7d732-140">リストで、**Microsoft Dynamics 365 Project Operations** を探し、**ステータス** 列で、**利用可能な更新があります** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="7d732-141">**サービス利用条件に同意する** チェック ボックスをオンにして、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="7d732-142">ソリューションの最新バージョンがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7d732-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="7d732-143">インストールが完了すると、バージョン 4.5.0.134 がインストールされた状態になります。</span><span class="sxs-lookup"><span data-stu-id="7d732-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="7d732-144">新機能の構成</span><span class="sxs-lookup"><span data-stu-id="7d732-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="7d732-145">二重書き込みマッピングを有効にする</span><span class="sxs-lookup"><span data-stu-id="7d732-145">Enable dual-write mapping</span></span>

<span data-ttu-id="7d732-146">Finance と Dataverse 環境で更新を完了した後、必要な二重書き込みマッピングを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="7d732-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="7d732-147">次の手順で、二重書き込みマッピングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="7d732-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="7d732-148">Customer Engagement 環境のセキュリティ設定を更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="7d732-149">更新エンティティを更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="7d732-150">二重書き込みマッピングを更新して実行する</span><span class="sxs-lookup"><span data-stu-id="7d732-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="7d732-151">Dataverse 環境のセキュリティ設定を更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="7d732-152">UR5 の更新の一部として、エンティティのセキュリティ権限に対する次の更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="7d732-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="7d732-153">Dataverse 環境で、**設定** に移動し、**システム** グループで **セキュリティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse 環境の設定](media/Picture21.png)

2. <span data-ttu-id="7d732-155">**セキュリティ ロール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="7d732-156">ロール リストから、**二重書き込みアプリ ユーザー** を選択してから、**カスタム エンティティ** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="7d732-157">ロールに、次の **読み込み** と **追加先** 権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d732-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="7d732-158">**通貨為替レートのタイプ**</span><span class="sxs-lookup"><span data-stu-id="7d732-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="7d732-159">**勘定科目表**</span><span class="sxs-lookup"><span data-stu-id="7d732-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="7d732-160">**会計カレンダー**</span><span class="sxs-lookup"><span data-stu-id="7d732-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="7d732-161">**Ledger**</span><span class="sxs-lookup"><span data-stu-id="7d732-161">**Ledger**</span></span>

5. <span data-ttu-id="7d732-162">セキュリティ ロールが更新されたら、**設定** > **セキュリティ** > **チーム** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7d732-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="7d732-163">**二重書き込みアプリ ユーザー** ロールがチームに適用されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d732-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="7d732-164">更新からデータ エンティティを更新します</span><span class="sxs-lookup"><span data-stu-id="7d732-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="7d732-165">Finance 環境で、**データ管理** ワークスペースを開き、**フレームワーク パラメーター** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d732-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="7d732-166">**エンティティ設定** タブで、**エンティティ リストの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="7d732-167">**閉じる** を選択して、エンティティの更新を確認します。</span><span class="sxs-lookup"><span data-stu-id="7d732-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7d732-168">このプロセスが完了するまでに、約 20 分かかります。</span><span class="sxs-lookup"><span data-stu-id="7d732-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="7d732-169">更新が完了すると通知されます。</span><span class="sxs-lookup"><span data-stu-id="7d732-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="7d732-170">二重書き込みマッピングを更新する</span><span class="sxs-lookup"><span data-stu-id="7d732-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="7d732-171">**データ管理** ワークスペースで、**二重書き込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="7d732-172">**ソリューションを適用する** を選択して、リストから両方のソリューションを選択してから、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="7d732-173">**二重書き込み** ページで、次のテーブル マップを選択してから、**停止** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="7d732-174">**Project Operations 統合実績 (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="7d732-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="7d732-175">**Project Operations 統合プロジェクト経費カテゴリ (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="7d732-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="7d732-176">**Project Operations 統合実績プロジェクト経費カテゴリのエクスポート エンティティ (msdyn_expense)**</span><span class="sxs-lookup"><span data-stu-id="7d732-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="7d732-177">**テーブル マップ バージョン** ページで、3 つのエンティティのそれぞれに新しいバージョンのマップを適用します。</span><span class="sxs-lookup"><span data-stu-id="7d732-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="7d732-178">**二重書き込み** ページで、実行を選択してマップを再起動します。</span><span class="sxs-lookup"><span data-stu-id="7d732-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="7d732-179">マップのリストから、すべての前提条件を満たす **元帳 (msdyn_ledgers)** マップを選択し、**初期同期** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7d732-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="7d732-180">**初期同期のマスター** フィールドで、**Finance and Operations アプリ** を選び、次に **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d732-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![元帳マップの同期](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]