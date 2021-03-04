---
title: デモのセットアップと構成データを適用する (ライト)
description: このトピックでは、Project Operations のデモ設定および構成データを適用する方法に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089125"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="a6cda-103">Project Operations に向けたデモの設定と構成データを適用する (ライト)</span><span class="sxs-lookup"><span data-stu-id="a6cda-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="a6cda-104">_\*\*ライト デプロイメント - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="a6cda-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="a6cda-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="a6cda-105">Prerequisites</span></span>

<span data-ttu-id="a6cda-106">構成を開始する前に、Dynamics 365 Project Operations 用にプロビジョニングされた Common Data Service (CDS) 環境が必要になります。</span><span class="sxs-lookup"><span data-stu-id="a6cda-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="a6cda-107">方法</span><span class="sxs-lookup"><span data-stu-id="a6cda-107">Instructions</span></span>

1. <span data-ttu-id="a6cda-108">[Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a6cda-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="a6cda-109">フォルダ *ProjOpsDemoDataSetupAndMaster - 統合 CMT* に移動し、実行可能ファイル *DataMigrationUtility* を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a6cda-110">Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、**データのインポート** を選び、**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![構成の移行](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a6cda-112">CMT Wizard の 2 ページで、**展開の種類** として **Microsoft 365** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a6cda-113">**利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a6cda-114">テナントの地域を選択し、資格情報を入力してから、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![構成サイン イン](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a6cda-116">3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="a6cda-117">4 ページで、解凍されたフォルダ *ProjOpsDemoDataSetupAndMaster - 統合 CMT* から、zip ファイル *MasterAndSetupData* を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Zip ファイル](./media/3ZipFile.png)

   ![ファイルの選択](./media/4SelectAFile.png)

9. <span data-ttu-id="a6cda-120">zip ファイルを選択したら、**データのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-120">After the zip file is selected, select **Import Data**.</span></span>

   ![データをインポート](./media/5ImportData.png)

10. <span data-ttu-id="a6cda-122">インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。</span><span class="sxs-lookup"><span data-stu-id="a6cda-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a6cda-123">完了後、CMT Wizard を終了します。</span><span class="sxs-lookup"><span data-stu-id="a6cda-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a6cda-124">次の 20 エンティティのデータについて組織を確認してください。</span><span class="sxs-lookup"><span data-stu-id="a6cda-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="a6cda-125">通貨</span><span class="sxs-lookup"><span data-stu-id="a6cda-125">Currency</span></span>
    -   <span data-ttu-id="a6cda-126">アカウント</span><span class="sxs-lookup"><span data-stu-id="a6cda-126">Account</span></span>
    -   <span data-ttu-id="a6cda-127">組織単位</span><span class="sxs-lookup"><span data-stu-id="a6cda-127">Organizational Unit</span></span>
    -   <span data-ttu-id="a6cda-128">取引先担当者 </span><span class="sxs-lookup"><span data-stu-id="a6cda-128">Contact</span></span>
    -   <span data-ttu-id="a6cda-129">単位</span><span class="sxs-lookup"><span data-stu-id="a6cda-129">Unit</span></span>
    -   <span data-ttu-id="a6cda-130">出荷単位一覧 </span><span class="sxs-lookup"><span data-stu-id="a6cda-130">Unit Group</span></span>
    -   <span data-ttu-id="a6cda-131">価格表 </span><span class="sxs-lookup"><span data-stu-id="a6cda-131">Price List</span></span>
    -   <span data-ttu-id="a6cda-132">プロジェクト パラメーター価格表</span><span class="sxs-lookup"><span data-stu-id="a6cda-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="a6cda-133">請求頻度</span><span class="sxs-lookup"><span data-stu-id="a6cda-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="a6cda-134">予約可能リソース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="a6cda-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="a6cda-135">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="a6cda-135">Transaction Category</span></span>
    -   <span data-ttu-id="a6cda-136">経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="a6cda-136">Expense Category</span></span>
    -   <span data-ttu-id="a6cda-137">ロール価格</span><span class="sxs-lookup"><span data-stu-id="a6cda-137">Role Price</span></span>
    -   <span data-ttu-id="a6cda-138">トランザクション カテゴリ価格</span><span class="sxs-lookup"><span data-stu-id="a6cda-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="a6cda-139">特性</span><span class="sxs-lookup"><span data-stu-id="a6cda-139">Characteristic</span></span>
    -   <span data-ttu-id="a6cda-140">予約可能リソース</span><span class="sxs-lookup"><span data-stu-id="a6cda-140">Bookable Resource</span></span>
    -   <span data-ttu-id="a6cda-141">予約可能リソース カテゴリ関連</span><span class="sxs-lookup"><span data-stu-id="a6cda-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="a6cda-142">予約可能リソースの特性</span><span class="sxs-lookup"><span data-stu-id="a6cda-142">Bookable Resource Characteristic</span></span>

    ![インポートの完了](./media/6CompleteImport.png)
