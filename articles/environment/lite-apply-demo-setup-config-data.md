---
title: デモ設定および構成データを適用する
description: このトピックでは、Project Operations のデモ設定および構成データを適用する方法に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079133"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="02bbd-103">Project Operations ライト デプロイメントのデモ設定および構成データを適用します - プロフォーマ インボイスに対処</span><span class="sxs-lookup"><span data-stu-id="02bbd-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="02bbd-104">_\*\*ライト デプロイメント - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="02bbd-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="02bbd-105">[Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="02bbd-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="02bbd-106">フォルダ *ProjOpsDemoDataSetupAndMaster - 統合 CMT* に移動し、実行可能ファイル *DataMigrationUtility* を実行します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="02bbd-107">Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、 **データのインポート** を選び、 **続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![構成の移行](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="02bbd-109">CMT Wizard の 2 ページで、 **展開の種類** として **Microsoft 365** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="02bbd-110">**利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="02bbd-111">テナントの地域を選択し、資格情報を入力してから、 **ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![構成サイン イン](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="02bbd-113">3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、 **ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="02bbd-114">4 ページで、解凍されたフォルダ *ProjOpsDemoDataSetupAndMaster - 統合 CMT* から、zip ファイル *MasterAndSetupData* を選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip ファイル](./media/3ZipFile.png)

![ファイルの選択](./media/4SelectAFile.png)

9. <span data-ttu-id="02bbd-117">zip ファイルを選択したら、 **データのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-117">After the zip file is selected, select **Import Data**.</span></span>

![データをインポート](./media/5ImportData.png)

10. <span data-ttu-id="02bbd-119">インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。</span><span class="sxs-lookup"><span data-stu-id="02bbd-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="02bbd-120">完了後、CMT Wizard を終了します。</span><span class="sxs-lookup"><span data-stu-id="02bbd-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="02bbd-121">次の 20 エンティティのデータについて組織を確認してください。</span><span class="sxs-lookup"><span data-stu-id="02bbd-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="02bbd-122">通貨</span><span class="sxs-lookup"><span data-stu-id="02bbd-122">Currency</span></span>
- <span data-ttu-id="02bbd-123">組織単位</span><span class="sxs-lookup"><span data-stu-id="02bbd-123">Organizational Unit</span></span>
- <span data-ttu-id="02bbd-124">連絡先</span><span class="sxs-lookup"><span data-stu-id="02bbd-124">Contact</span></span>
- <span data-ttu-id="02bbd-125">税務グループ</span><span class="sxs-lookup"><span data-stu-id="02bbd-125">Tax Group</span></span>
- <span data-ttu-id="02bbd-126">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="02bbd-126">Customer Group</span></span>
- <span data-ttu-id="02bbd-127">単位</span><span class="sxs-lookup"><span data-stu-id="02bbd-127">Unit</span></span>
- <span data-ttu-id="02bbd-128">出荷単位一覧 </span><span class="sxs-lookup"><span data-stu-id="02bbd-128">Unit Group</span></span>
- <span data-ttu-id="02bbd-129">価格表 </span><span class="sxs-lookup"><span data-stu-id="02bbd-129">Price List</span></span>
- <span data-ttu-id="02bbd-130">プロジェクト パラメーター価格表</span><span class="sxs-lookup"><span data-stu-id="02bbd-130">Project Parameter Price List</span></span>
- <span data-ttu-id="02bbd-131">請求頻度</span><span class="sxs-lookup"><span data-stu-id="02bbd-131">Invoice Frequency</span></span>
- <span data-ttu-id="02bbd-132">請求頻度の詳細</span><span class="sxs-lookup"><span data-stu-id="02bbd-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="02bbd-133">予約可能リソース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="02bbd-133">Bookable Resource Category</span></span>
- <span data-ttu-id="02bbd-134">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="02bbd-134">Transaction Category</span></span>
- <span data-ttu-id="02bbd-135">経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="02bbd-135">Expense Category</span></span>
- <span data-ttu-id="02bbd-136">ロール価格</span><span class="sxs-lookup"><span data-stu-id="02bbd-136">Role Price</span></span>
- <span data-ttu-id="02bbd-137">トランザクション カテゴリ価格</span><span class="sxs-lookup"><span data-stu-id="02bbd-137">Transaction Category Price</span></span>
- <span data-ttu-id="02bbd-138">特性</span><span class="sxs-lookup"><span data-stu-id="02bbd-138">Characteristic</span></span>
- <span data-ttu-id="02bbd-139">予約可能リソース</span><span class="sxs-lookup"><span data-stu-id="02bbd-139">Bookable Resource</span></span>
- <span data-ttu-id="02bbd-140">予約可能リソース カテゴリ関連</span><span class="sxs-lookup"><span data-stu-id="02bbd-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="02bbd-141">予約可能リソースの特性</span><span class="sxs-lookup"><span data-stu-id="02bbd-141">Bookable Resource Characteristic</span></span>

![インポートの完了](./media/6CompleteImport.png)
