---
title: プロジェクト リソース スケジュールのパフォーマンス
description: このトピックは、多数のプロジェクトのリソース スケジュールのパフォーマンスを改善する方法に関する情報を提供します。
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079251"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="0af1e-103">プロジェクト リソース スケジュールのパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="0af1e-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="0af1e-104">プロジェクトの数が数千に達すると、リソース スケジュールに関連するパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0af1e-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="0af1e-105">リソース スケジュールのパフォーマンスを向上させるために、ユーザーがリソース可用性フォームの起動にかかる時間を短縮できる機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="0af1e-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="0af1e-106">具体的には、これにより、リソース容量のロールアップ同期プロセスが削除され、リソース検索を高速化するための **ResProjectResource** テーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="0af1e-107">**ResRollup** テーブルは使用されなくなりますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="0af1e-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0af1e-108">リソース容量のロールアップ同期プロセス、または **ResProjectResource** テーブルのいずれかに依存関係がある場合は、この機能を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0af1e-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="0af1e-109">リソース スケジュールのパフォーマンス向上を有効にする</span><span class="sxs-lookup"><span data-stu-id="0af1e-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="0af1e-110">リソース スケジュールのパフォーマンス向上を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="0af1e-111">**機能管理** > **すべて** に移動して、機能リストで、 **プロジェクト リソース スケジュールのパフォーマンス向上機能を有効にする** を検索します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="0af1e-112">**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="0af1e-113">リストに機能が見つからない場合は、 **アップデートを確認する** リストを選択してリストを更新します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="0af1e-114">ブラウザを更新してから、 **プロジェクト管理と会計** > **定期的** > **プロジェクト リソース** > **すべての企業でリソース カレンダーの容量の同期** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="0af1e-115">**既存の容量レコードを削除する** を **はい** に設定して、以前のデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="0af1e-116">増分データを生成する場合は、これを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="0af1e-117">**期間コード** フィールドで、データを生成する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="0af1e-118">期間コードを選択する場合、開始日と終了日を定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0af1e-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="0af1e-119">**期間コード** フィールドを空白にする場合、特定の開始日と終了日を選択してデータを生成します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="0af1e-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="0af1e-121">これにより、一般的なデータを環境内のすべての会社の **ResCalendarCapacity** テーブルに配布するため、バッチ ジョブは 1 つの法人でのみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af1e-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="0af1e-122">このバッチ ジョブのデータは、関連するカレンダーを介してリソースのキャパシティを計算するために必要です。</span><span class="sxs-lookup"><span data-stu-id="0af1e-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="0af1e-123">**プロジェクト管理と会計** > **定期的** > **プロジェクト リソース** > **すべての企業にプロジェクト リソースを投入する** の順に移動して、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="0af1e-124">これは、 **ResProjectResource** テーブル、 **ResCalendarDateTimeRange** テーブル、 **ResEffectiveDateTimeRange** テーブルの一般的なデータのデータ アップグレード スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="0af1e-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="0af1e-125">**PSAPRojSchedRole.RootActivity** フィールドの値も更新されます。</span><span class="sxs-lookup"><span data-stu-id="0af1e-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="0af1e-126">これが実行されていない場合、リソース スケジュール操作を実行しようとすると、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0af1e-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="0af1e-127">リソース スケジュールのパフォーマンス向上をオフにする</span><span class="sxs-lookup"><span data-stu-id="0af1e-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="0af1e-128">**機能管理** > **すべて** に移動して、 **プロジェクト リソース スケジュールのパフォーマンス向上機能を有効にする** を検索します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="0af1e-129">機能を選択してから、 **無効にする** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="0af1e-130">ブラウザーを最新の情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-130">Refresh your browser.</span></span>
4. <span data-ttu-id="0af1e-131">**プロジェクト管理と会計** > **定期的** > **キャパシティの同期** > **リソース キャパシティのロールアップを同期する** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="0af1e-132">**キャパシティのロールアップ同期** ページで、 **既存のキャパシティ レコードを削除する** を **はい** に設定して以前のデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="0af1e-133">増分データを生成する場合は、これを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="0af1e-134">**期間コード** フィールドで、データを生成する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="0af1e-135">期間コードを選択する場合、開始日と終了日を定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0af1e-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="0af1e-136">**期間コード** フィールドを空白にする場合、特定の開始日と終了日を選択してデータを生成します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="0af1e-137">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af1e-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="0af1e-138">これは一般的なデータを環境内のすべての会社にまたがって **ResRollup** テーブルに配布するため、バッチ ジョブは 1 つの法人でのみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af1e-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="0af1e-139">このバッチ ジョブはすべての **リソースの可用性** ビューに対して必要です。</span><span class="sxs-lookup"><span data-stu-id="0af1e-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="0af1e-140">このバッチ ジョブが実行されていない場合、 **ResRollup** データはその場で生成されますが、時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0af1e-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
