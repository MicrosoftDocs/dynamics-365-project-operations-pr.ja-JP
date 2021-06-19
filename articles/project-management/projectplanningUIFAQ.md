---
title: タスク グリッドでの作業のトラブルシューティング
description: このトピックでは、タスク グリッドで作業するときに必要なトラブルシューティング情報を提供します。
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213406"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="bbbf4-103">タスク グリッドでの作業のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="bbbf4-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="bbbf4-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="bbbf4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bbbf4-105">このトピックでは、コスト管理の作業中に発生する可能性のある問題を修正する方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="bbbf4-106">Cookie を有効にする</span><span class="sxs-lookup"><span data-stu-id="bbbf4-106">Enable cookies</span></span>

<span data-ttu-id="bbbf4-107">Project Operations では、WBS (作業分解構造) をレンダリングするためにサードパーティの Cookie を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="bbbf4-108">サードパーティの Cookie が有効になっていない場合、**プロジェクト** ページの **タスク** タブを選択するとタスクではなく空白のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![サードパーティの Cookie が有効になっていない場合の空白タブ](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="bbbf4-110">回避策</span><span class="sxs-lookup"><span data-stu-id="bbbf4-110">Workaround</span></span>
<span data-ttu-id="bbbf4-111">Microsoft Edge または Google Chrome ブラウザの場合、次の手順でブラウザの設定を更新してサードパーティの Cookie を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="bbbf4-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bbbf4-112">Microsoft Edge</span></span>

1. <span data-ttu-id="bbbf4-113">Edge ブラウザーを開きます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="bbbf4-114">右上隅で、 **省略記号** (...) を選択してから **設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="bbbf4-115">**Cookie とサイトの許可** の下で、**Cookie とサイト データ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="bbbf4-116">**サードパーティの Cookie をブロックする** をオフにします。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="bbbf4-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="bbbf4-117">Google Chrome</span></span>

1. <span data-ttu-id="bbbf4-118">Chrome ブラウザーを開きます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="bbbf4-119">右上の歯車アイコンを選択して、3 つの縦のドットを選択してから **設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="bbbf4-120">**プライバシーとセキュリティ** の下で、**Cookie とその他のサイト データ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="bbbf4-121">**すべての Cookie を許可する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbbf4-122">サードパーティの Cookie をブロックすると、そのサイトが例外リストで許可されている場合でも、他のサイトのすべての Cookie とサイト データがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="bbbf4-123">PEX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="bbbf4-123">PEX Endpoint</span></span>

<span data-ttu-id="bbbf4-124">Project Operations では、プロジェクト パラメーターが PEX エンドポイントを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="bbbf4-125">このエンドポイントは、WBS (作業分解構造) のレンダリングに使用されるサービスと通信するために必要です。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="bbbf4-126">パラメーターが有効になっていない場合、「プロジェクト パラメーターが無効です」というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="bbbf4-127">回避策</span><span class="sxs-lookup"><span data-stu-id="bbbf4-127">Workaround</span></span>
 ![プロジェクト パラメーターの PEX エンドポイント フィールド](media/projectparameter.png)

1. <span data-ttu-id="bbbf4-129">**PEX エンドポイント** フィールドを **プロジェクト パラメーター** ページに追加します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="bbbf4-130">フィールドを`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2` フィールドの値で更新します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="bbbf4-131">**プロジェクト パラメーター** ページからフィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="bbbf4-132">Web の Project の特権</span><span class="sxs-lookup"><span data-stu-id="bbbf4-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="bbbf4-133">Project Operations は、外部のスケジューリング サービスに依存しています。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="bbbf4-134">このサービスでは、WBS (作業分解構造) に関連するエンティティの読み取りと書き込みを行うために、ユーザーにいくつかの役割が割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="bbbf4-135">これらのエンティティには、プロジェクト タスク、リソース割り当て、およびタスク依存関係が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="bbbf4-136">ユーザーが **タスク** タブに移動したときに WBS (作業分解構造)をレンダリングできない場合、おそらく Project Operations のプロジェクトが有効になっていないためです。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="bbbf4-137">ユーザーは、セキュリティ ロール エラー、またはアクセスの拒否に関連するエラーのいずれかを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="bbbf4-138">回避策</span><span class="sxs-lookup"><span data-stu-id="bbbf4-138">Workaround</span></span>

1. <span data-ttu-id="bbbf4-139">**設定 > セキュリティ > ユーザー > アプリケーション ユーザー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![アプリケーション リーダー](media/applicationuser.jpg)
   
2. <span data-ttu-id="bbbf4-141">アプリケーション ユーザー レコードをダブルクリックして次の項目を確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="bbbf4-142">ユーザーにはプロジェクトへのアクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-142">The user has access to the project.</span></span> <span data-ttu-id="bbbf4-143">この検証は通常、ユーザーが **プロジェクト マネージャー** セキュリティ  ロールがあることを確認することにより行われます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="bbbf4-144">Microsoft Project アプリケーション ユーザーが存在し、正しく構成されています。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="bbbf4-145">このユーザーが存在しない場合は、新規ユーザー レビューを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="bbbf4-146">**新しいユーザー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-146">Select **New Users**.</span></span> <span data-ttu-id="bbbf4-147">入力フォームを **アプリケーション ユーザー** に変更してから、**アプリケーション ID** を追加します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![アプリケーション ユーザー詳細](media/applicationuserdetails.jpg)

4. <span data-ttu-id="bbbf4-149">ユーザーに正しいライセンスが割り当てられていること、およびライセンスのサービス プラン詳細でサービスが有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="bbbf4-150">ユーザーが project.microsoft.com を開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="bbbf4-151">プロジェクト パラメーターを使用して、システムが正しいプロジェクト エンドポイントをポイントしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="bbbf4-152">プロジェクト アプリケーション ユーザーが作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="bbbf4-153">次のセキュリティ ロールをユーザーに適用します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="bbbf4-154">Dataverse ユーザー</span><span class="sxs-lookup"><span data-stu-id="bbbf4-154">Dataverse User</span></span>
  - <span data-ttu-id="bbbf4-155">Project Operations システム</span><span class="sxs-lookup"><span data-stu-id="bbbf4-155">Project Operations System</span></span>
  - <span data-ttu-id="bbbf4-156">プロジェクト システム</span><span class="sxs-lookup"><span data-stu-id="bbbf4-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="bbbf4-157">WBS (作業分解構造) の更新時にエラーが発生しました</span><span class="sxs-lookup"><span data-stu-id="bbbf4-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="bbbf4-158">WBS (作業分解構造) に 1 つ以上の更新が行われると、変更は最終的に失敗し、保存されません。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="bbbf4-159">スケジュール グリッドで「最近行った変更を保存できませんでした」というエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="bbbf4-160">回避策</span><span class="sxs-lookup"><span data-stu-id="bbbf4-160">Workaround</span></span>

1. <span data-ttu-id="bbbf4-161">ユーザーに正しいライセンスが割り当てられていること、およびライセンスのサービス プラン詳細でサービスが有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="bbbf4-162">ユーザーが project.microsoft.com を開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="bbbf4-163">システムが正しいプロジェクト エンドポイントをポイントしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="bbbf4-164">プロジェクト アプリケーション ユーザーが作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="bbbf4-165">次のセキュリティ ロールをユーザーに適用します。</span><span class="sxs-lookup"><span data-stu-id="bbbf4-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="bbbf4-166">Dataverse ユーザーまたは Base ユーザー</span><span class="sxs-lookup"><span data-stu-id="bbbf4-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="bbbf4-167">Project Operations システム</span><span class="sxs-lookup"><span data-stu-id="bbbf4-167">Project Operations System</span></span>
  - <span data-ttu-id="bbbf4-168">プロジェクト システム</span><span class="sxs-lookup"><span data-stu-id="bbbf4-168">Project System</span></span>
  - <span data-ttu-id="bbbf4-169">Project Operations 二重書き込みシステム (このロールは、Project Operations のリソース/非在庫ベースのシナリオを展開する場合に必要です。)</span><span class="sxs-lookup"><span data-stu-id="bbbf4-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
