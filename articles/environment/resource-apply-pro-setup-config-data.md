---
title: Common Data Service で構成データの設定と適用
description: このトピックでは、Project Operations の構成データの設定と適用に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642234"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="97b53-103">Common Data Service で構成データの設定と適用</span><span class="sxs-lookup"><span data-stu-id="97b53-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="97b53-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="97b53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="97b53-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="97b53-105">Prerequisites</span></span>

<span data-ttu-id="97b53-106">Common Data Service (CDS) でデータの構成を開始する前に、次の前提条件が満たされている必要があります:</span><span class="sxs-lookup"><span data-stu-id="97b53-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="97b53-107">Project Operations 用の CDS 環境と Dynamics 365 Finance 環境をプロビジョニングします。</span><span class="sxs-lookup"><span data-stu-id="97b53-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="97b53-108">Dynamics 365 Finance からの法人情報は、CDS 環境で共有されます。</span><span class="sxs-lookup"><span data-stu-id="97b53-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="97b53-109">つまり、CDS の **会社** エンティティには、次の会社レコードがあります:</span><span class="sxs-lookup"><span data-stu-id="97b53-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="97b53-110">THPM</span><span class="sxs-lookup"><span data-stu-id="97b53-110">THPM</span></span>
  - <span data-ttu-id="97b53-111">USPM</span><span class="sxs-lookup"><span data-stu-id="97b53-111">USPM</span></span>
  - <span data-ttu-id="97b53-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="97b53-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="97b53-113">設定および構成データをインストールする</span><span class="sxs-lookup"><span data-stu-id="97b53-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="97b53-114">[設定および構成データ パッケージ](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip) をダウンロード、ブロック解除および解凍します。</span><span class="sxs-lookup"><span data-stu-id="97b53-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="97b53-115">解凍したフォルダに移動し、実行可能ファイル *DataMigrationUtility* を実行します。</span><span class="sxs-lookup"><span data-stu-id="97b53-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="97b53-116">Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、**データのインポート** を選び、**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![構成の移行](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="97b53-118">CMT Wizard の 2 ページで、**展開の種類** として **Microsoft 365** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="97b53-119">**利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="97b53-120">テナントの地域を選択し、資格情報を入力してから、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![構成サイン イン](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="97b53-122">3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="97b53-123">4 ページで、解凍されたフォルダから、zip ファイル *SampleSetupAndConfigData* を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip ファイルの選択](./media/3ZipFile.png)

![ファイルの選択](./media/4SelectAFile.png)

9. <span data-ttu-id="97b53-126">zip ファイルを選択したら、**データのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-126">After the zip file is selected, select **Import Data**.</span></span>

![データの​​インポート](./media/5ImportData.png)

10. <span data-ttu-id="97b53-128">インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。</span><span class="sxs-lookup"><span data-stu-id="97b53-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="97b53-129">インポートの完了後、CMT Wizard を終了します。</span><span class="sxs-lookup"><span data-stu-id="97b53-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="97b53-130">次の 19 エンティティのデータについて組織を確認してください。</span><span class="sxs-lookup"><span data-stu-id="97b53-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="97b53-131">通貨</span><span class="sxs-lookup"><span data-stu-id="97b53-131">Currency</span></span>
  - <span data-ttu-id="97b53-132">組織単位</span><span class="sxs-lookup"><span data-stu-id="97b53-132">Organizational Unit</span></span>
  - <span data-ttu-id="97b53-133">連絡先</span><span class="sxs-lookup"><span data-stu-id="97b53-133">Contact</span></span>
  - <span data-ttu-id="97b53-134">税務グループ</span><span class="sxs-lookup"><span data-stu-id="97b53-134">Tax Group</span></span>
  - <span data-ttu-id="97b53-135">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="97b53-135">Customer Group</span></span>
  - <span data-ttu-id="97b53-136">単位</span><span class="sxs-lookup"><span data-stu-id="97b53-136">Unit</span></span>
  - <span data-ttu-id="97b53-137">出荷単位一覧 </span><span class="sxs-lookup"><span data-stu-id="97b53-137">Unit Group</span></span>
  - <span data-ttu-id="97b53-138">価格表 </span><span class="sxs-lookup"><span data-stu-id="97b53-138">Price List</span></span>
  - <span data-ttu-id="97b53-139">プロジェクト パラメーター価格表</span><span class="sxs-lookup"><span data-stu-id="97b53-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="97b53-140">請求頻度</span><span class="sxs-lookup"><span data-stu-id="97b53-140">Invoice Frequency</span></span>
  - <span data-ttu-id="97b53-141">予約可能リソース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="97b53-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="97b53-142">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="97b53-142">Transaction Category</span></span>
  - <span data-ttu-id="97b53-143">経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="97b53-143">Expense Category</span></span>
  - <span data-ttu-id="97b53-144">ロール価格</span><span class="sxs-lookup"><span data-stu-id="97b53-144">Role Price</span></span>
  - <span data-ttu-id="97b53-145">トランザクション カテゴリ価格</span><span class="sxs-lookup"><span data-stu-id="97b53-145">Transaction Category Price</span></span>
  - <span data-ttu-id="97b53-146">特性</span><span class="sxs-lookup"><span data-stu-id="97b53-146">Characteristic</span></span>
  - <span data-ttu-id="97b53-147">予約可能リソース</span><span class="sxs-lookup"><span data-stu-id="97b53-147">Bookable Resource</span></span>
  - <span data-ttu-id="97b53-148">予約可能リソース カテゴリ関連</span><span class="sxs-lookup"><span data-stu-id="97b53-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="97b53-149">予約可能リソースの特性</span><span class="sxs-lookup"><span data-stu-id="97b53-149">Bookable Resource Characteristic</span></span>

![インポートの完了](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="97b53-151">Project Operations 構成の更新</span><span class="sxs-lookup"><span data-stu-id="97b53-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="97b53-152">CE 環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="97b53-152">Navigate to the CE environment.</span></span> <span data-ttu-id="97b53-153">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com/environments) を開き、環境を選択してから、**環境を開く** を選択すると、見つかります。</span><span class="sxs-lookup"><span data-stu-id="97b53-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![環境を開く](./media/7OpenEnvironment.png)

2. <span data-ttu-id="97b53-155">**プロジェクト** > **リソース** に移動し、次に **新規** を選択して、ユーザーの予約可能なリソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="97b53-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![予約可能リソース](./media/8BookableResources.png)

3. <span data-ttu-id="97b53-157">**全般** タブで、管理者ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="97b53-158">タイム ゾーンが現在のタイム ゾーンと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="97b53-158">Verify that the time zone matches the one you are in.</span></span> 

![新規予約可能リソース](./media/9NewBookableResource.png)

4. <span data-ttu-id="97b53-160">**スケジュール設定** タブの、**会社** フィールドで、**USPM** 会社を選び、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![スケジュール タブ](./media/10SchedulingTab.png)

5. <span data-ttu-id="97b53-162">**作業時間** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-162">Select the **Work hours** tab.</span></span>  

![作業時間](./media/11WorkHours.png)

6. <span data-ttu-id="97b53-164">カレンダーの任意の値をダブルクリックして、**編集** > **シリーズのすべてのイベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![作業カレンダー](./media/12WorkCalendar.png)

7. <span data-ttu-id="97b53-166">作業時間を 8 時間作業日に変更し、週末を非作業日としてマークし、タイム ゾーンが自分のタイム ゾーンと一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="97b53-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="97b53-167">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-167">Select **Save and close**.</span></span>

![カレンダーの更新](./media/13UpdateCalendar.png)

9. <span data-ttu-id="97b53-169">**設定** > **カレンダー テンプレート** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![カレンダー テンプレート](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="97b53-171">名前を入力し、作成したテンプレート リソースを選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![カレンダー テンプレートの保存](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="97b53-173">**パラメーター** に移動し、レコードをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="97b53-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![プロジェクト パラメーター](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="97b53-175">次のフィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="97b53-175">Update the following fields:</span></span>

 - <span data-ttu-id="97b53-176">**既定の会社**: USPM</span><span class="sxs-lookup"><span data-stu-id="97b53-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="97b53-177">**既定のの組織単位**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="97b53-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="97b53-178">**請求書の頻度**: 7日目と最終日</span><span class="sxs-lookup"><span data-stu-id="97b53-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="97b53-179">**作業時間テンプレート**: 作成したテンプレートに変更します。</span><span class="sxs-lookup"><span data-stu-id="97b53-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="97b53-180">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97b53-180">Select **Save**.</span></span> 

![更新されるプロジェクト パラメーター](./media/17UpdatedProjectParameters.png)
