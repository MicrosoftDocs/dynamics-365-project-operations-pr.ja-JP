---
title: Project Operations のデモ データを Finance クラウド ホスト環境に適用する
description: このトピックは、Project Operations からのデモ データを Dynamics 365 Finance のクラウド ホスト環境に適用する方法を説明しています。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096628"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="5e3c2-103">Project Operations のデモ データを Finance クラウド ホスト環境に適用する</span><span class="sxs-lookup"><span data-stu-id="5e3c2-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="5e3c2-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5e3c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e3c2-105">このトピックは Microsoft Dynamics 365 Finance バージョン 10.0.13 にのみ適用され、クラウド ホスト型環境でのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="5e3c2-106">環境に品質更新を適用する **前** に、このトピックの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="5e3c2-107">LCS プロジェクトで、 **環境の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="5e3c2-108">リモート デスクトップ プロトコル (RDP) を使用して環境に接続するために必要な詳細が含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ 環境の詳細](./media/1EnvironmentDetails.png)

<span data-ttu-id="5e3c2-110">強調表示された資格情報の最初のセットはローカル アカウントの資格情報であり、リモート デスクトップ接続へのハイパーリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="5e3c2-111">資格情報には、環境管理者のユーザー名とパスワードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="5e3c2-112">2 番目の資格情報のセットは、この環境で SQL Server にログインするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="5e3c2-113">**ローカル アカウント** のハイパーリンクで環境にリモート接続し、 **ローカルアカウントの資格情報** を使用して認証します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="5e3c2-114">**インターネット インフォメーション サービス** > **アプリケーション プール** > **AOSService** に移動し、サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="5e3c2-115">この時点でサービスを停止しているので、SQL データベースの置き換えを続行できます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS の停止](./media/2StopAOS.png)

4. <span data-ttu-id="5e3c2-117">**サービス** に移動し、次の 2 つの項目を停止します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="5e3c2-118">Microsoft Dynamics 365 Unified Operations: バッチ管理サービス</span><span class="sxs-lookup"><span data-stu-id="5e3c2-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="5e3c2-119">Microsoft Dynamics 365 Unified Operations: データのインポート/エクスポート フレームワーク</span><span class="sxs-lookup"><span data-stu-id="5e3c2-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![サービスの停止](./media/3StopServices.png)

5. <span data-ttu-id="5e3c2-121">Microsoft SQL Server Management Studio を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="5e3c2-122">SQL サーバーの資格情報を使用してログインし、LCS **環境の詳細** ページの axdbadmin ユーザーとパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="5e3c2-124">オブジェクト エクスプローラーで、 **データベース** を選択し、 **AXDB** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="5e3c2-125">データベースを、[ダウンロード センター](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) にある新しいデータベースに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="5e3c2-126">リモート先の VM に zip ファイルをコピーし、zip コンテンツを抽出します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="5e3c2-127">SQL Server Management Studio で、 **AxDB** を右クリックし、次に **タスク** > **復元** > **データベース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![データベースの復元](./media/5RestoreDatabase.png)

9. <span data-ttu-id="5e3c2-129">**ソース デバイス** を選択し、コピーした zip から抽出したファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![ソース デバイス](./media/6SourceDevice.png)

10. <span data-ttu-id="5e3c2-131">**オプション** を選択し、次に **既存のデータベースの上書き** と **宛先データベースへの既存の接続を閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="5e3c2-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-132">Select **OK**.</span></span>

![設定を復元](./media/7RestoreSetting.png)

<span data-ttu-id="5e3c2-134">AXDB の復元が成功したという確認が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="5e3c2-135">この確認が表示された後、SQL Services Management Studio を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="5e3c2-136">**インターネット インフォメーション サービス** > **アプリケーション プール** > **AOSService** に戻り、AOSService を開始します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="5e3c2-137">**サービス** に移動し、以前に停止した 2 つのサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="5e3c2-138">この VM で AdminUserProvisioning ツールを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="5e3c2-139">K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe の下をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="5e3c2-140">**電子メール アドレス** フィールドのユーザー アドレスを使用して .ext ファイルを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="5e3c2-141">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-141">Select **Submit**.</span></span>

![管理者ユーザー プロビジョニング](./media/8AdminUserProvisioning.png)

<span data-ttu-id="5e3c2-143">これが完了するまでに数分かかります。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="5e3c2-144">管理者ユーザーが正常に更新されたことを示す確認メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="5e3c2-145">最後に、コマンド プロンプトを管理者として実行し、iisreset を実行します</span><span class="sxs-lookup"><span data-stu-id="5e3c2-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS リセット](./media/9IISReset.png)

18. <span data-ttu-id="5e3c2-147">リモート デスクトップ セッションを閉じて、LCS **環境の詳細** ページを使用して環境にログインし、期待どおりに機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5e3c2-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
