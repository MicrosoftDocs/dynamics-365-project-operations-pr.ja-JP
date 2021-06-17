---
title: モバイル経費アプリ
description: このトピックでは、経費管理モバイル ワークスペースに関する説明をします。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2f274a5f0dfcfdbe8c6771fff7a636c6e93eeea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001972"
---
# <a name="mobile-expense-app"></a><span data-ttu-id="f2149-103">モバイル経費アプリ</span><span class="sxs-lookup"><span data-stu-id="f2149-103">Mobile Expense app</span></span>

<span data-ttu-id="f2149-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="f2149-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2149-105">このトピックでは、**経費管理** モバイル ワークスペースに関する説明をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-105">This topic provides information about the **Expense management** mobile workspace.</span></span> <span data-ttu-id="f2149-106">このワークスペースでは、領収書を取り込んでアップロードし、後で経費精算書に添付することができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-106">This workspace lets users capture and upload a receipt, so that they can attach it to an expense report later.</span></span> <span data-ttu-id="f2149-107">ユーザーは、添付の領収書を使用して経費明細をすばやく作成し、経費報告書を作成して管理することができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-107">Users can also quickly create an expense line by using an attached receipt, and create and manage their expense reports.</span></span> <span data-ttu-id="f2149-108">さらに、承認者は **経費管理** モバイル ワークスペースを使用してチームに割り当てられている経費報告書を表示し、これら経費報告書の承認や否認することができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-108">Additionally, approvers can use the **Expense management** mobile workspace to view expense reports that are assigned to them, and either approve or reject those expense reports.</span></span>

<span data-ttu-id="f2149-109">このモバイル ワークスペースは、Dynamics 365 Unified Operations Mobile アプリと共に使用することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="f2149-109">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span>

<span data-ttu-id="f2149-110">多くの組織では、従業員が経費精算に提出する出張関連、または業務関連の経費報告書に領収書のコピーを添付することを義務付けています。</span><span class="sxs-lookup"><span data-stu-id="f2149-110">Many organizations require that a copy of a receipt be attached to a travel-related or business-related expense report that an employee submits for reimbursement.</span></span> <span data-ttu-id="f2149-111">**経費管理** モバイル ワークスペースでは、領収書の写真を添付することで、ユーザーが選択したモバイル デバイス上に新しい経費明細を迅速に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-111">The **Expense management** mobile workspace lets users quickly create new expense lines on the mobile device of their choice by using an attached photo of a receipt.</span></span> <span data-ttu-id="f2149-112">または、領収書の写真をキャプチャして、後で経費報告書に添付することもできます。</span><span class="sxs-lookup"><span data-stu-id="f2149-112">Alternatively, users can capture a photo of a receipt and then attach it to an expense report later.</span></span> <span data-ttu-id="f2149-113">従業員は経費報告書を作成、管理し、モバイル デバイスを使って承認、精算のために提出することができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-113">Employees can also create and manage their expense reports, and then submit them for approval and reimbursement by using their mobile device.</span></span>

<span data-ttu-id="f2149-114">具体的には、**経費管理** モバイル ワークスペースでは、ユーザーは次のタスクを実行できます :</span><span class="sxs-lookup"><span data-stu-id="f2149-114">Specifically, the **Expense management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="f2149-115">領収書の写真を撮ります。</span><span class="sxs-lookup"><span data-stu-id="f2149-115">Take a photo of a receipt.</span></span> <span data-ttu-id="f2149-116">領収書の写真をアップロードして、後で経費報告書に添付します。</span><span class="sxs-lookup"><span data-stu-id="f2149-116">Upload the receipt photo and attach it to an expense report later.</span></span>
- <span data-ttu-id="f2149-117">キャプチャした領収書ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f2149-117">Upload a file as a captured receipt.</span></span> <span data-ttu-id="f2149-118">その後、このファイルを経費報告書に添付できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-118">You can then attach that file to an expense report later.</span></span>
- <span data-ttu-id="f2149-119">添付の領収書を使用して新しい経費明細を作成します。</span><span class="sxs-lookup"><span data-stu-id="f2149-119">Create a new expense line by using an attached receipt.</span></span> <span data-ttu-id="f2149-120">あとで経費報告書に明細項目を追加して、承認と精算のために提出することができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-120">You can then add the line item to an expense report later, and submit it for approval and reimbursement.</span></span>

<span data-ttu-id="f2149-121">次の機能を使用することもできます :</span><span class="sxs-lookup"><span data-stu-id="f2149-121">You can also use these features:</span></span>

- <span data-ttu-id="f2149-122">新規経費報告書の作成。</span><span class="sxs-lookup"><span data-stu-id="f2149-122">Create a new expense report.</span></span>
- <span data-ttu-id="f2149-123">クレジットカードの取引など、以前に作成した経費を経費報告書に添付する。</span><span class="sxs-lookup"><span data-stu-id="f2149-123">Attach credit card transactions and other previously created expenses to an expense report.</span></span>
- <span data-ttu-id="f2149-124">経費報告書の新しい経費を作成する。</span><span class="sxs-lookup"><span data-stu-id="f2149-124">Create new expenses for an expense report.</span></span>
- <span data-ttu-id="f2149-125">領収書の写真を撮る、またはキャプチャした領収書ファイルをアップロードして、経費報告書の経費に領収書を添付する。</span><span class="sxs-lookup"><span data-stu-id="f2149-125">Attach a receipt to any expense for an expense report, either by taking a photo of the receipt or by uploading a file as a captured receipt.</span></span>
- <span data-ttu-id="f2149-126">経費の方針に応じて、ゲストのリストを経費に追加する。</span><span class="sxs-lookup"><span data-stu-id="f2149-126">Depending on the company's expense policy, add the list of guests to an expense.</span></span>
- <span data-ttu-id="f2149-127">経費の方針に応じて、経費を明細化する。</span><span class="sxs-lookup"><span data-stu-id="f2149-127">Depending on the company's expense policy, itemize expenses.</span></span>
- <span data-ttu-id="f2149-128">経費報告書を提出して承認、精算を行う。</span><span class="sxs-lookup"><span data-stu-id="f2149-128">Submit an expense report for approval and reimbursement.</span></span>
- <span data-ttu-id="f2149-129">承認者として指定されている経費報告書を承認または拒否する。</span><span class="sxs-lookup"><span data-stu-id="f2149-129">Approve or reject expense reports that you're an assigned approver for.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2149-130">前提条件</span><span class="sxs-lookup"><span data-stu-id="f2149-130">Prerequisites</span></span>
<span data-ttu-id="f2149-131">前提条件は、導入されていのバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f2149-131">The prerequisites vary, based on the version that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="f2149-132">Dynamics 365 Finance を使用する場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="f2149-132">Prerequisites if you use Dynamics 365 Finance</span></span> 
<span data-ttu-id="f2149-133">Finance が展開されている場合は、システム管理者は **経費管理** モバイル ワークスペースを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2149-133">If Finance has been deployed for your organization, the system administrator must publish the **Expense management** mobile workspace.</span></span> 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="f2149-134">Platform update 3 以降のバージョン 1611 を使用する場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="f2149-134">Prerequisites if you use version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="f2149-135">プラットフォーム更新プログラム 3 以降のバージョン 1611 が展開されている場合、システム管理者は次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2149-135">If version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f2149-136">前提条件</span><span class="sxs-lookup"><span data-stu-id="f2149-136">Prerequisite</span></span></th>
<th><span data-ttu-id="f2149-137">ロール</span><span class="sxs-lookup"><span data-stu-id="f2149-137">Role</span></span></th>
<th><span data-ttu-id="f2149-138">内容</span><span class="sxs-lookup"><span data-stu-id="f2149-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2149-139">サポート情報 4019015 を実装する。</span><span class="sxs-lookup"><span data-stu-id="f2149-139">Implement KB 4019015.</span></span></td>
<td><span data-ttu-id="f2149-140">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f2149-140">System administrator</span></span></td>
<td><span data-ttu-id="f2149-141">サポート情報記事 4019015 は、<strong>経費管理</strong>モバイル ワークスペースを含む X++ 更新またはメタデータ修正プログラムです。</span><span class="sxs-lookup"><span data-stu-id="f2149-141">KB 4019015 is an X++ update or metadata hotfix that contains the <strong>Expense management</strong> mobile workspace.</span></span> <span data-ttu-id="f2149-142">サポート情報 4019015 を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2149-142">To implement KB 4019015, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="f2149-143"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lifecycle Services から更新プログラムをダウンロードする</a>。</span><span class="sxs-lookup"><span data-stu-id="f2149-143"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download updates from Lifecycle Services</a>.</span></span></li>
<li><span data-ttu-id="f2149-144"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします</a>。</span><span class="sxs-lookup"><span data-stu-id="f2149-144"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="f2149-145"><strong>ApplicationSuite</strong> および <strong>経費管理</strong> モデルを含む<a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">展開可能なパッケージを作成</a>し、展開可能なパッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f2149-145"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ExpenseMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="f2149-146"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">展開可能なパッケージを適用します</a>。</span><span class="sxs-lookup"><span data-stu-id="f2149-146"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2149-147"><strong>経費管理</strong>モバイル ワークスペースを公開する。</span><span class="sxs-lookup"><span data-stu-id="f2149-147">Publish the <strong>Expense management</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="f2149-148">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f2149-148">System administrator</span></span></td>
<td><span data-ttu-id="f2149-149"><a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの発行</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-149">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a><span data-ttu-id="f2149-150">Dynamics 365 Unified Ops モバイル アプリをダウンロードしてインストールする</span><span class="sxs-lookup"><span data-stu-id="f2149-150">Download and install the Dynamics 365 Unified Ops mobile app</span></span>
<span data-ttu-id="f2149-151">Dynamics 365 Unified Ops モバイル アプリをダウンロードしてインストールする :</span><span class="sxs-lookup"><span data-stu-id="f2149-151">Download and install the Dynamics 365 Unified Ops mobile app:</span></span>

- [<span data-ttu-id="f2149-152">Android 電話用</span><span class="sxs-lookup"><span data-stu-id="f2149-152">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="f2149-153">iPhones 用</span><span class="sxs-lookup"><span data-stu-id="f2149-153">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="f2149-154">モバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="f2149-154">Sign in to the mobile app</span></span>
1. <span data-ttu-id="f2149-155">モバイル デバイスからアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="f2149-155">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="f2149-156">Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-156">Enter your Dynamics 365 URL.</span></span>
4. <span data-ttu-id="f2149-157">初めてサインインするときに、ユーザー名とパスワードを入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="f2149-157">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="f2149-158">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-158">Enter your credentials.</span></span>
5. <span data-ttu-id="f2149-159">サインインすると、会社で使用可能なワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-159">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="f2149-160">システム管理者が後から新しいワークスペースを発行した場合、モバイル ワークスペースのリストを更新する必要がありますのでご注意ください。</span><span class="sxs-lookup"><span data-stu-id="f2149-160">If your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a><span data-ttu-id="f2149-161">経費管理モバイル ワークスペースを使用して領収書をキャプチャする</span><span class="sxs-lookup"><span data-stu-id="f2149-161">Capture a receipt by using the Expense management mobile workspace</span></span>

1. <span data-ttu-id="f2149-162">モバイル デバイスで **経費管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f2149-162">On your mobile device, open the **Expense management** workspace.</span></span>
2. <span data-ttu-id="f2149-163">**領収書をキャプチャする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-163">Select **Capture receipt**.</span></span>
3. <span data-ttu-id="f2149-164">**写真を撮る** または **画像を選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-164">Select **Take photo** or **Choose image**.</span></span>
4. <span data-ttu-id="f2149-165">次のいずれかの手順に従います :</span><span class="sxs-lookup"><span data-stu-id="f2149-165">Follow one of these steps:</span></span>

   - <span data-ttu-id="f2149-166">**写真を撮る** 選択した場合、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="f2149-166">If you selected **Take photo**, follow these steps:</span></span>

      1. <span data-ttu-id="f2149-167">モバイル デバイスのカメラに移動し、領収書の写真を撮ることができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-167">You're taken to the camera on your mobile device, so that you can take a photo of the receipt.</span></span> 
      2. <span data-ttu-id="f2149-168">写真の撮影が終わったら、**OK** を選択して写真を確定します。</span><span class="sxs-lookup"><span data-stu-id="f2149-168">When you've finished taking a photo, select **OK** to accept the photo.</span></span>
      3. <span data-ttu-id="f2149-169">オプション : 写真の名前とメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-169">Optional: Enter a name for the photo, and enter any notes.</span></span>

    - <span data-ttu-id="f2149-170">**画像を選択** を選択した場合、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="f2149-170">If you selected **Choose image**, follow these steps:</span></span>

        1. <span data-ttu-id="f2149-171">リスト内の画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-171">Select an image in the list.</span></span>
        2. <span data-ttu-id="f2149-172">オプション : 画像の名前とメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-172">Optional: Enter a name for the image, and enter any notes.</span></span>

5. <span data-ttu-id="f2149-173">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-173">Select **Done**.</span></span>

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a><span data-ttu-id="f2149-174">経費管理モバイル ワークスペースを使用して迅速に経費を入力する</span><span class="sxs-lookup"><span data-stu-id="f2149-174">Quickly enter expenses by using the Expense management mobile workspace</span></span>

1. <span data-ttu-id="f2149-175">モバイル デバイスで **経費管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f2149-175">On your mobile device, open the **Expense management** workspace.</span></span>
2. <span data-ttu-id="f2149-176">**経費の簡易入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-176">Select **Quick expense entry**.</span></span>
3. <span data-ttu-id="f2149-177">経費のカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-177">Select the expense category.</span></span> <span data-ttu-id="f2149-178">オフラインで使用するためにアプリに読み込まれている経費カテゴリのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-178">You see a list of expense categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-179">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-179">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-180">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-180">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-181">カテゴリが一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-181">If your category isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-182">経費カテゴリで検索するか、経費タイプ別の検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f2149-182">Search by expense category, or switch to search by expense type.</span></span>
4. <span data-ttu-id="f2149-183">経費のトランザクション日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-183">Enter the transaction date of the expense.</span></span>
5. <span data-ttu-id="f2149-184">オプション : 経費に使用するマーチャントを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-184">Optional: Enter the merchant for the expense.</span></span>
6. <span data-ttu-id="f2149-185">経費の金額を入力してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-185">Enter the amount of the expense.</span></span>
7. <span data-ttu-id="f2149-186">経費に使用する通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-186">Select the currency of the expense.</span></span> <span data-ttu-id="f2149-187">オフラインで使用するためにアプリに読み込まれている通貨コードのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-187">You see a list of the currency codes that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-188">既定では 400 の通貨が読み込まれていますが、開発者であればこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-188">By default, 400 currencies are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-189">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-189">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-190">通貨が一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-190">If your currency isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-191">通貨で検索するか、カテゴリ名別検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f2149-191">Search by currency, or switch to search by name.</span></span>
8. <span data-ttu-id="f2149-192">**写真を撮る** または **画像を選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-192">Select **Take photo** or **Choose image**.</span></span>
9. <span data-ttu-id="f2149-193">次のいずれかの手順に従います :</span><span class="sxs-lookup"><span data-stu-id="f2149-193">Follow one of these steps:</span></span>

    - <span data-ttu-id="f2149-194">**写真を撮る** を選択した場合、モバイル デバイスのカメラに移動し、領収書の写真を撮ることができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-194">If you selected **Take photo**, you're taken to the camera on your mobile device, so that you can take a photo of the receipt.</span></span> <span data-ttu-id="f2149-195">写真の撮影が終わったら、**OK** を選択して写真を確定します。</span><span class="sxs-lookup"><span data-stu-id="f2149-195">When you've finished taking a photo, select **OK** to accept the photo.</span></span>
    - <span data-ttu-id="f2149-196">**画像を選択する** を選択した場合、リストから画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-196">If you selected **Choose image**, select an image in the list.</span></span>

10. <span data-ttu-id="f2149-197">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-197">Select **Done**.</span></span>

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a><span data-ttu-id="f2149-198">経費管理モバイル ワークスペースを使用して経費レポートを承認する (2017年7月の更新プログラムを適用している場合)</span><span class="sxs-lookup"><span data-stu-id="f2149-198">Approve an expense report by using the Expense management mobile workspace (if you use the July 2017 update)</span></span>

1. <span data-ttu-id="f2149-199">モバイル デバイスで **経費管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f2149-199">On your mobile device, open the **Expense management** workspace.</span></span>
2. <span data-ttu-id="f2149-200">**経費承認** は、自分が承認者に割り当てられている経費報告書の件数を示しています。</span><span class="sxs-lookup"><span data-stu-id="f2149-200">**Expense approvals** shows the number of expense reports that are assigned to you for approval.</span></span> <span data-ttu-id="f2149-201">この件数は約 30 分ごとに更新されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-201">The number is updated approximately every 30 minutes.</span></span> <span data-ttu-id="f2149-202">**経費承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-202">Select **Expense approvals**.</span></span>

    <span data-ttu-id="f2149-203">経費報告書のリストは、自分が承認者に割り当てられている経費報告書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-203">The list of expense reports that are assigned to you for approval is shown.</span></span>
    
3. <span data-ttu-id="f2149-204">経費報告書を選択して、経費の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="f2149-204">Select an expense report to view the expense details for it.</span></span>
4. <span data-ttu-id="f2149-205">経費報告書を選択して、経費の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="f2149-205">Select an expense to view the details for it.</span></span> <span data-ttu-id="f2149-206">経費について表示される情報には、領収書、ゲスト、項目別の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f2149-206">The information that is shown for an expense includes any receipt, guest, and itemization details.</span></span>
5. <span data-ttu-id="f2149-207">**経費報告書** ページに戻り、経費報告書を承認または却下を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-207">Back on the **Expense report** page, select to approve or reject the expense report.</span></span>
6. <span data-ttu-id="f2149-208">承認アクションについてのコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-208">Enter any comments for the approval action.</span></span>
7. <span data-ttu-id="f2149-209">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-209">Select **Done**.</span></span>

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a><span data-ttu-id="f2149-210">経費管理モバイル ワークスペースを使用して新たな経費報告書を作成し、提出する (2017年7月の更新プログラムを適用している場合)</span><span class="sxs-lookup"><span data-stu-id="f2149-210">Create a new expense report and submit it for approval by using the Expense management mobile workspace (if you use the July 2017 update)</span></span>

1. <span data-ttu-id="f2149-211">モバイル デバイスで **経費管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f2149-211">On your mobile device, open the **Expense management** workspace.</span></span>
2. <span data-ttu-id="f2149-212">**経費の入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-212">Select **Expense entry**.</span></span>
3. <span data-ttu-id="f2149-213">**新規報告書**、またはリストから既存の経費報告書を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-213">Select **New report**, or select an existing expense report in the list.</span></span>
4. <span data-ttu-id="f2149-214">新しい経費報告書については、目的と利用可能な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-214">For new expense reports, enter the purpose and any additional information that is available.</span></span> <span data-ttu-id="f2149-215">この情報は、会社の経費管理がどのように構成されているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f2149-215">This information varies, depending on that way that expense management is configured for your company.</span></span>
5. <span data-ttu-id="f2149-216">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-216">Select **Done**.</span></span>
6. <span data-ttu-id="f2149-217">クレジットカード取引などの既存の費用を費用レポートに追加するには、**添付** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-217">To add existing expenses, such as credit card transactions, to the expense report, select **Attach**.</span></span>
7. <span data-ttu-id="f2149-218">経費の一覧で、1 人以上のユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-218">Select one or more expenses in the list.</span></span>
8. <span data-ttu-id="f2149-219">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-219">Select **Done**.</span></span>
9. <span data-ttu-id="f2149-220">経費レポートに新たな経費を追加するには、**新たな費用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-220">To add a new expense to the expense report, select **New expense**.</span></span>
10. <span data-ttu-id="f2149-221">経費のカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-221">Select the category for the expense.</span></span> <span data-ttu-id="f2149-222">オフラインで使用するためにアプリに読み込まれている経費カテゴリのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-222">You see a list of expense categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-223">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-223">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-224">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-224">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-225">カテゴリが一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-225">If your category isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-226">経費カテゴリで検索するか、経費タイプ別の検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f2149-226">Search by expense category, or switch to search by expense type.</span></span>
11. <span data-ttu-id="f2149-227">オプション : 経費に使用するマーチャントを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-227">Optional: Enter the merchant for the expense.</span></span>
12. <span data-ttu-id="f2149-228">経費のトランザクション日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-228">Enter the transaction date of the expense.</span></span>
13. <span data-ttu-id="f2149-229">経費の金額を入力してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-229">Enter the amount of the expense.</span></span>
14. <span data-ttu-id="f2149-230">経費に使用する通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-230">Select the currency of the expense.</span></span> <span data-ttu-id="f2149-231">オフラインで使用するためにアプリに読み込まれている通貨コードのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-231">You see a list of the currency codes that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-232">既定では 400 の通貨が読み込まれていますが、開発者であればこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-232">By default, 400 currencies are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-233">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-233">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-234">通貨が一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-234">If your currency isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-235">通貨で検索するか、カテゴリ名別検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f2149-235">Search by currency, or switch to search by name.</span></span>
15. <span data-ttu-id="f2149-236">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-236">Select **Done**.</span></span>
16. <span data-ttu-id="f2149-237">経費に詳細を追加するには、**詳細の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-237">To add more details to the expense, select **Add more details**.</span></span> <span data-ttu-id="f2149-238">使用可能となるフィールドは、会社の経費管理の構成によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f2149-238">The fields that are available depend on the configuration of expense management for your company.</span></span>
17. <span data-ttu-id="f2149-239">会社の方針で経費の領収書が必要な場合は、**領収書** を選択し、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="f2149-239">If company policy requires a receipt for the expense, select **Receipts**, and then follow these steps:</span></span>

    1. <span data-ttu-id="f2149-240">**領収書をキャプチャする**、または **領収書を添付する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-240">Select **Capture receipt** or **Attach receipt**.</span></span>
    2. <span data-ttu-id="f2149-241">次のいずれかの手順に従います :</span><span class="sxs-lookup"><span data-stu-id="f2149-241">Follow one of these steps:</span></span>

        - <span data-ttu-id="f2149-242">**領収書を添付** を選択した場合、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="f2149-242">If you selected **Capture receipt**, follow these steps:</span></span>

            1. <span data-ttu-id="f2149-243">**写真を撮る** または **画像を選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-243">Select **Take photo** or **Choose image**.</span></span>
            2. <span data-ttu-id="f2149-244">次のいずれかの手順に従います :</span><span class="sxs-lookup"><span data-stu-id="f2149-244">Follow one of these steps:</span></span>

                - <span data-ttu-id="f2149-245">**写真を撮る** 選択した場合、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="f2149-245">If you selected **Take photo**, follow these steps:</span></span>

                    1. <span data-ttu-id="f2149-246">モバイル デバイスのカメラに移動し、領収書の写真を撮ることができます。</span><span class="sxs-lookup"><span data-stu-id="f2149-246">You're taken to the camera on your mobile device, so that you can take a photo of the receipt.</span></span> <span data-ttu-id="f2149-247">写真の撮影が終わったら、**OK** を選択して写真を確定します。</span><span class="sxs-lookup"><span data-stu-id="f2149-247">When you've finished taking a photo, select **OK** to accept the photo.</span></span>
                    2. <span data-ttu-id="f2149-248">オプション : 写真の名前とメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-248">Optional: Enter a name for the photo, and enter any notes.</span></span>

                - <span data-ttu-id="f2149-249">**画像を選択** を選択した場合、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="f2149-249">If you selected **Choose image**, follow these steps:</span></span>

                    1. <span data-ttu-id="f2149-250">リスト内の画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-250">Select an image in the list.</span></span>
                    2. <span data-ttu-id="f2149-251">オプション : 画像の名前とメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-251">Optional: Enter a name for the image, and enter any notes.</span></span>

            3.  <span data-ttu-id="f2149-252">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-252">Select **Done**.</span></span>

        - <span data-ttu-id="f2149-253">**領収書を添付** を選択した場合は、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="f2149-253">If you selected **Attach receipt**, follow these steps:</span></span>

            1.  <span data-ttu-id="f2149-254">一覧で、1 つ以上の画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-254">Select one or more images in the list.</span></span>
            2.  <span data-ttu-id="f2149-255">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-255">Select **Done**.</span></span>

    3. <span data-ttu-id="f2149-256">**戻る**  ボタンをクリックして経費の詳細に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f2149-256">Select the **Back** button to return to the expense details.</span></span>

18. <span data-ttu-id="f2149-257">会社の方針で経費のゲストが必要な場合は、**ゲスト** を選択し、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="f2149-257">If company policy requires guests for the expense, select **Guests**, and then follow these steps:</span></span>

    1. <span data-ttu-id="f2149-258">**ゲスト**、**以前のゲスト**、**同僚** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-258">Select **Guest**, **Previous guests**, or **Coworkers**.</span></span>
    2. <span data-ttu-id="f2149-259">次のいずれかの手順に従います :</span><span class="sxs-lookup"><span data-stu-id="f2149-259">Follow one of these steps:</span></span>

        - <span data-ttu-id="f2149-260">**ゲスト** 選択した場合、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="f2149-260">If you selected **Guest**, follow these steps:</span></span>

            1. <span data-ttu-id="f2149-261">ゲストの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-261">Enter the name of the guest.</span></span>
            2. <span data-ttu-id="f2149-262">オプション : ゲストの組織および/または国を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-262">Optional: Enter the organization and/or country of the guest.</span></span>
            3. <span data-ttu-id="f2149-263">オプション : ゲストの役職を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-263">Optional: Enter the title of the guest.</span></span>
            4. <span data-ttu-id="f2149-264">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-264">Select **Done**.</span></span>

        - <span data-ttu-id="f2149-265">**以前のゲスト** を選択した場合、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="f2149-265">If you selected **Previous guests**, follow these steps:</span></span>

            1. <span data-ttu-id="f2149-266">一覧で、1 つまたは以前のゲストを選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-266">Select one or more previous guests in the list.</span></span> <span data-ttu-id="f2149-267">オフラインで使用するためにアプリに読み込まれた、以前の経費レポートに追加した以前のゲストのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-267">You see a list of previous guests that you've added to previous expense reports that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-268">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-268">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-269">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-269">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-270">ゲストが一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-270">If your previous guest isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-271">名前で検索をするか、組織、国、役職に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f2149-271">Search by name, or switch to search by organization, country, or title.</span></span>
            2. <span data-ttu-id="f2149-272">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-272">Select **Done**.</span></span>

        - <span data-ttu-id="f2149-273">**同僚** 選択した場合、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="f2149-273">If you selected **Coworkers**, follow these steps:</span></span>

            1. <span data-ttu-id="f2149-274">一覧で、1 人以上の同僚を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-274">Select one or more coworkers in the list.</span></span> <span data-ttu-id="f2149-275">オフラインで使用するためにアプリに読み込まれている同僚のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-275">You see a list of coworkers that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-276">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-276">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-277">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-277">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-278">同僚が一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-278">If your coworker isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-279">名前で検索をするか、会社や役職に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="f2149-279">Search by name, or switch to search by company or title.</span></span>
            2. <span data-ttu-id="f2149-280">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-280">Select **Done**.</span></span>

    3. <span data-ttu-id="f2149-281">**戻る**  ボタンをクリックして経費の詳細に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f2149-281">Select the **Back** button to return to the expense details.</span></span>

19. <span data-ttu-id="f2149-282">会社の方針で項目別経費が必要な場合は、**項目別** を選択し、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="f2149-282">If company policy requires that the expense be itemized, select **Itemize**, and then follow these steps:</span></span>

    1. <span data-ttu-id="f2149-283">項目化をする最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-283">Select the first date to itemize.</span></span>
    2. <span data-ttu-id="f2149-284">**項目化の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-284">Select **Add itemization**.</span></span>
    3. <span data-ttu-id="f2149-285">項目別経費のサブカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-285">Select the subcategory for the expense itemization.</span></span> <span data-ttu-id="f2149-286">オフラインで使用するためにアプリに読み込まれている経費サブカテゴリのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2149-286">You see a list of expense subcategories that are loaded into your app for offline use.</span></span> <span data-ttu-id="f2149-287">既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="f2149-287">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="f2149-288">詳細情報については、開発者は [モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2149-288">For more information, developers should see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started).</span></span> <span data-ttu-id="f2149-289">サブカテゴリが一覧にない場合は、**検索** を選択してオンライン検索をします。</span><span class="sxs-lookup"><span data-stu-id="f2149-289">If your subcategory isn't in the list, select **Search** to do an online search.</span></span> <span data-ttu-id="f2149-290">経費のサブカテゴリ名で検索します。</span><span class="sxs-lookup"><span data-stu-id="f2149-290">Search by expense subcategory name.</span></span>
    4. <span data-ttu-id="f2149-291">項目別の取引金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-291">Enter the transaction amount for the itemization.</span></span>
    5. <span data-ttu-id="f2149-292">必要に応じて、取引日付を編集します。</span><span class="sxs-lookup"><span data-stu-id="f2149-292">Edit the transaction date if it's required.</span></span>
    6. <span data-ttu-id="f2149-293">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-293">Select **Done**.</span></span>
    7. <span data-ttu-id="f2149-294">選択した日付のすべての項目の追加が完了するまで、前述の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f2149-294">Repeat the preceding steps until you've finished adding all itemizations for the selected date.</span></span>
    8. <span data-ttu-id="f2149-295">追加の日については、**翌日にコピー** を選択して項目化を翌日にコピーします。</span><span class="sxs-lookup"><span data-stu-id="f2149-295">For additional days, you can select **Copy to next day** to copy the itemizations to the next day.</span></span> <span data-ttu-id="f2149-296">または、項目化する日付を選択し、最初の日付と同じように項目化を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="f2149-296">Alternatively, you can select the date to itemize and then add itemizations as you did for the first date.</span></span>
    9. <span data-ttu-id="f2149-297">経費の項目化が終わったら、**戻る** ボタンを選択して経費の詳細に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f2149-297">After you've finished itemizing the expense, select the **Back** button to return to the expense details.</span></span>

20. <span data-ttu-id="f2149-298">**戻る** ボタンを選択して **経費の詳細** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="f2149-298">Select the **Back** button to return to the **Expense report** page.</span></span>
21. <span data-ttu-id="f2149-299">すべての経費の追加が完了するまで、上記の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f2149-299">Repeat the preceding steps until you've finished adding all expenses.</span></span>
22. <span data-ttu-id="f2149-300">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-300">Select **Submit**.</span></span>
23. <span data-ttu-id="f2149-301">承認者に向けたコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="f2149-301">Enter any comments for the approver.</span></span>
24. <span data-ttu-id="f2149-302">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2149-302">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]