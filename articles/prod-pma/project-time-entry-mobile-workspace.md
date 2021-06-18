---
title: プロジェクト時間エントリ モバイル ワークスペース
description: このトピックでは、プロジェクト時間エントリ モバイル ワークスペースに関する情報を提供します。 このワークスペースを使用すると、ユーザーはモバイル デバイスを使用して、プロジェクトに時間を入力および保存できます。
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f087e15780272fd376a14b42ed9e00420f86a61f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009937"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="0ffb4-104">プロジェクト時間エントリ モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="0ffb4-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ffb4-105">このトピックでは、**プロジェクト時間エントリ** モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="0ffb4-106">このワークスペースを使用すると、ユーザーはモバイル デバイスを使用して、プロジェクトに時間を入力および保存できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="0ffb4-107">このモバイル ワークスペースは、Dynamics 365 Unified Operations Mobile アプリと共に使用することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="0ffb4-108">概要</span><span class="sxs-lookup"><span data-stu-id="0ffb4-108">Overview</span></span>
<span data-ttu-id="0ffb4-109">日々の業務の一環として、プロジェクト リソースは多くの場合、オンサイトまたは出張中です。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="0ffb4-110">**プロジェクト時間入力** モバイル ワークスペースを使用すると、ユーザーが選択したモバイル デバイスでプロジェクトに対して支払請求可能な時間または支払請求可能でない時間を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="0ffb4-111">したがって、プロジェクト リソースは、時間エントリをいつでも、どこでも記録できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="0ffb4-112">また、既に記録されている時間エントリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="0ffb4-113">具体的には、**プロジェクト時間エントリ** モバイル ワークスペースで、ユーザーは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="0ffb4-114">選択した日付に対して、特定のタスクに費やした時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="0ffb4-115">時間を入力するプロジェクトをプロジェクト名または顧客で検索します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="0ffb4-116">費やした時間のカテゴリと活動を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="0ffb4-117">プロジェクトの時間を請求可能または請求不可能として記録します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="0ffb4-118">必要に応じて、外部または内部のコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ffb4-119">前提条件</span><span class="sxs-lookup"><span data-stu-id="0ffb4-119">Prerequisites</span></span>
<span data-ttu-id="0ffb4-120">前提条件は、組織に展開されている Microsoft Dynamics 365 のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="0ffb4-121">Dynamics 365 Finance を使用する場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="0ffb4-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="0ffb4-122">Finance が組織に展開されている場合、システム管理者は **プロジェクト時間エントリ** モバイル ワークスペースを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="0ffb4-123">詳細については、[モバイル ワークスペースの発行](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-123">For instructions, see [Publish a mobile workspace](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="0ffb4-124">Platform update 3 以降のバージョン 1611 を使用する場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="0ffb4-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="0ffb4-125">プラットフォーム更新プログラム 3 以降のバージョン 1611 が組織に展開されている場合、システム管理者は次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0ffb4-126">前提条件</span><span class="sxs-lookup"><span data-stu-id="0ffb4-126">Prerequisite</span></span></th>
<th><span data-ttu-id="0ffb4-127">ロール</span><span class="sxs-lookup"><span data-stu-id="0ffb4-127">Role</span></span></th>
<th><span data-ttu-id="0ffb4-128">内容</span><span class="sxs-lookup"><span data-stu-id="0ffb4-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="0ffb4-129">サポート情報 4018050 を実装する。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="0ffb4-130">システム管理者</span><span class="sxs-lookup"><span data-stu-id="0ffb4-130">System administrator</span></span></td>
<td><span data-ttu-id="0ffb4-131">サポート情報 4018050 は、<strong>プロジェクト時間エントリ</strong> モバイル ワークスペースを含む X++ 更新またはメタデータ修正プログラムです。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="0ffb4-132">サポート情報 4018050 を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="0ffb4-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="0ffb4-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします</a>。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="0ffb4-135"><strong>ApplicationSuite</strong> および <strong>ProjectMobile</strong> モデルを含む<a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">展開可能なパッケージを作成</a>してから、展開可能なパッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="0ffb4-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">展開可能なパッケージを適用します</a>。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ffb4-137"><strong>プロジェクト時間エントリ</strong> モバイル ワークスペースを発行します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="0ffb4-138">システム管理者</span><span class="sxs-lookup"><span data-stu-id="0ffb4-138">System administrator</span></span></td>
<td><span data-ttu-id="0ffb4-139"><a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの発行</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-139">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="0ffb4-140">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="0ffb4-140">Download and install the mobile app</span></span>

<span data-ttu-id="0ffb4-141">Finance and Operations モバイル アプリのダウンロードとインストール:</span><span class="sxs-lookup"><span data-stu-id="0ffb4-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="0ffb4-142">Android 電話用</span><span class="sxs-lookup"><span data-stu-id="0ffb4-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="0ffb4-143">iPhones 用</span><span class="sxs-lookup"><span data-stu-id="0ffb4-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="0ffb4-144">モバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="0ffb4-145">モバイル デバイスからアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="0ffb4-146">Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="0ffb4-147">初めてサインインするときに、ユーザー名とパスワードを入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="0ffb4-148">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="0ffb4-149">サインインすると、会社で使用可能なワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="0ffb4-150">システム管理者が後で新しいワークスペースを発行した場合は、モバイル ワークスペースのリストを更新する必要がありますのでご注意ください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="0ffb4-151">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="0ffb4-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="0ffb4-152">プロジェクト時間エントリ モバイル ワークスペースを使用した時間の入力</span><span class="sxs-lookup"><span data-stu-id="0ffb4-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="0ffb4-153">モバイル デバイスで、**プロジェクト時間エントリ** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="0ffb4-154">**時間エントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-154">Select **Time entry**.</span></span> <span data-ttu-id="0ffb4-155">現在の週のカレンダー日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="0ffb4-156">選択した日付で、**操作** &gt; **新しいエントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="0ffb4-157">記録する時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="0ffb4-158">時間エントリのプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-158">Select the project for the time entry.</span></span> <span data-ttu-id="0ffb4-159">一覧には、オフラインで使用するためにアプリに読み込まれているプロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="0ffb4-160">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="0ffb4-161">詳細については、[モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-161">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="0ffb4-162">プロジェクトが一覧にない場合は、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="0ffb4-163">名前で検索するか、プロジェクト名または顧客別検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="0ffb4-164">カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-164">Select a category.</span></span> <span data-ttu-id="0ffb4-165">一覧には、オフラインで使用するためにアプリに読み込まれているカテゴリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="0ffb4-166">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="0ffb4-167">詳細については、[モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-167">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="0ffb4-168">カテゴリが一覧にない場合は、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="0ffb4-169">カテゴリで検索するか、カテゴリ名別検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="0ffb4-170">活動を選択してください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-170">Select an activity.</span></span> <span data-ttu-id="0ffb4-171">一覧には、オフラインで使用するためにアプリに読み込まれている活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="0ffb4-172">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="0ffb4-173">詳細については、[モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-173">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="0ffb4-174">活動が一覧にない場合は、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="0ffb4-175">活動番号で検索するか、目的別検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="0ffb4-176">ライン プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-176">Select the line property.</span></span>
12. <span data-ttu-id="0ffb4-177">任意: 外部および内部のコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="0ffb4-178">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ffb4-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]