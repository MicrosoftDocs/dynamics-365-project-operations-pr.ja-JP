---
title: プロジェクトのリソースをスケジュールする
description: Project Service でのプロジェクトのリソースをスケジュールする方法
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079474"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="799a7-103">プロジェクトのリソースをスケジュールする (Project Service)</span><span class="sxs-lookup"><span data-stu-id="799a7-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="799a7-104">リソースの空き時間をチェックして、リソースの予約状況の全体のビューを取得できます。または、ビューをスキル、チーム、場所、およびその他のオプションでフィルターすることができます。</span><span class="sxs-lookup"><span data-stu-id="799a7-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="799a7-105">スケジュール ボードにはリソースと可用性が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="799a7-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="799a7-106">ビュー モードを選択し、 **時間** 、 **日** 、 **週** 、または **月** 別に可用性を表示します。</span><span class="sxs-lookup"><span data-stu-id="799a7-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="799a7-107">スケジュール ボードを使用する前に、それをセットすることは重要です。</span><span class="sxs-lookup"><span data-stu-id="799a7-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="799a7-108">詳細については、 [スケジュール ボードの構成 (Field Service または Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="799a7-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="799a7-109">リソースの可用性の目的で、古いバージョンを使用している場合は、[ビュー リソースの可用性](../psa/view-resource-availability.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="799a7-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="799a7-110">スケジュール ボード予約機能、ジオコード化、および位置サービスを使用するには、マップを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="799a7-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="799a7-111">メイン メニューから、 **リソース スケジュール** > **管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="799a7-112">**スケジュール パラメーター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="799a7-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="799a7-113">レコードを開き、 **Resource Scheduling Optimization** セクションへと下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="799a7-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="799a7-114">**マップに接続する** フィールドで、 **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="799a7-115">サブスクリプション利用条件に同意し、レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="799a7-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="799a7-116">メイン メニューで、 **プロジェクト サービス** > **スケジュール ボード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="799a7-117">ここでは、予約条件を手動でスケジュールするには複数の方法があります。</span><span class="sxs-lookup"><span data-stu-id="799a7-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="799a7-118">都合のよい方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="799a7-119">利用可能なリソースをみつける</span><span class="sxs-lookup"><span data-stu-id="799a7-119">Find available resources</span></span>

1.  <span data-ttu-id="799a7-120">**予約の条件** リストから、スケジュールが完了していない予約を右クリックし、次のいずれかを選びます:</span><span class="sxs-lookup"><span data-stu-id="799a7-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="799a7-121">**使用可能の検索 - 現在のリソース** を選択して、スケジュール ボードのリストから使用可能なリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="799a7-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="799a7-122">**使用可能の検索 - 全てのリソース** を選択して、システムのリソースから使用可能なリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="799a7-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="799a7-123">この操作を行う場合、フィルターは選択された予約要件のオプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="799a7-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="799a7-124">利用可能な時間帯が表示されたら、スケジュール ボードの時間帯を右クリックし、 **ここを予約する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="799a7-125">または、使用可能な時間スロットに予約の条件をドラッグ・アンド・ドロップします。</span><span class="sxs-lookup"><span data-stu-id="799a7-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="799a7-126">日単位を使用してリソースを予約し、誰の名前で予約されているかを検索する</span><span class="sxs-lookup"><span data-stu-id="799a7-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="799a7-127">スケジュール ボードで、 **モードの表示** を選択し **日** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="799a7-128">これではリソースが 1 日あたりに何時間予約されるかおよび何日が空いているかのグリッド ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="799a7-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="799a7-129">予約するリソース名をクリックし、 **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="799a7-130">**リソースの予約 (作成)** ダイアログ ボックスで、予約方法と開始時間や終了時間と共に、リソースを予約するプロジェクトを選びます。</span><span class="sxs-lookup"><span data-stu-id="799a7-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="799a7-131">完了したら、 **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="799a7-132">スケジュール ボードの表示</span><span class="sxs-lookup"><span data-stu-id="799a7-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="799a7-133">下部の一覧からスケジュールが完了していない予約要件を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="799a7-134">その予約要件をスケジュール ボード上の使用可能なリソース/時間帯にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="799a7-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="799a7-135">完了したら、 **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="799a7-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="799a7-136">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="799a7-136">Additional resources</span></span>  
 [<span data-ttu-id="799a7-137">リソース マネージャー ガイド</span><span class="sxs-lookup"><span data-stu-id="799a7-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
