---
title: タイム ゾーンの管理
description: プロジェクトが作成されると、そのタイム ゾーンは、適用する作業時間テンプレートで定義されたタイム ゾーンに基づきます。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119829"
---
# <a name="manage-time-zones"></a><span data-ttu-id="85c70-103">タイム ゾーンの管理</span><span class="sxs-lookup"><span data-stu-id="85c70-103">Manage time zones</span></span>

<span data-ttu-id="85c70-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="85c70-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="85c70-105">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="85c70-105">Projects</span></span>

<span data-ttu-id="85c70-106">プロジェクトが作成されると、タイム ゾーンは、適用された作業時間テンプレートで定義されたタイム ゾーンに基づきます。</span><span class="sxs-lookup"><span data-stu-id="85c70-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="85c70-107">**プロジェクト** の場合、日付は常に、**タスク** タブを除き、各タブにログインしているユーザーのタイム ゾーンを基準にしています。WBS (作業分解構造) を表示すると、日付は常にプロジェクトのタイム ゾーンで表示されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="85c70-108">タスク</span><span class="sxs-lookup"><span data-stu-id="85c70-108">Tasks</span></span>

<span data-ttu-id="85c70-109">タスクが作成されると、開始時間、終了時間、および 1 日あたりの時間は、プロジェクトの作業時間によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="85c70-110">たとえば、タイム ゾーンが -8 PST で、作業時間が月曜日から金曜日の午前 9 時から午後 5 時までのプロジェクトでタスクが作成された場合、割り当てなしで作成されたタスクは、プロジェクト カレンダーの開始時間と終了時間を利用します。</span><span class="sxs-lookup"><span data-stu-id="85c70-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="85c70-111">タイム ゾーンでリソースを管理する</span><span class="sxs-lookup"><span data-stu-id="85c70-111">Manage resources with time zones</span></span>

<span data-ttu-id="85c70-112">**予約の延長** を使用するときに正確で予測可能な結果を得るには、満たす必要のある 2 つの重要な前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="85c70-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="85c70-113">ユーザーは、システムの **個人設定** で定義されたタイム ゾーンと一致するようにデバイスのタイム ゾーンを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85c70-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Windows 10 のタイムゾーン設定](media/reconcile-assignments-03.png)

  ![パーソナライズ設定におけるタイムゾーンの設定](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="85c70-116">予約可能なリソースには、要求された拡張機能を定義するために使用する等高線と重複する作業時間が少なくとも 1 分間必要です。</span><span class="sxs-lookup"><span data-stu-id="85c70-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="85c70-117">たとえば、午前 9 時から午後 7 時までの間にある勤務時間の次のリソース。</span><span class="sxs-lookup"><span data-stu-id="85c70-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![リソースの等高線の比較](media/reconcile-assignments-05.png)

<span data-ttu-id="85c70-119">次の表に示されています:</span><span class="sxs-lookup"><span data-stu-id="85c70-119">The following table shows:</span></span>

- <span data-ttu-id="85c70-120">プロジェクト カレンダーのテンプレート</span><span class="sxs-lookup"><span data-stu-id="85c70-120">A project calendar template</span></span>
- <span data-ttu-id="85c70-121">リソース A：このリソースには同一のカレンダーがあり、プロジェクトと同じタイムゾーンにあります。</span><span class="sxs-lookup"><span data-stu-id="85c70-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="85c70-122">予約の開始時間は午前9時です。</span><span class="sxs-lookup"><span data-stu-id="85c70-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="85c70-123">リソースB: このリソースは、プロジェクトとは異なるタイム ゾーンにあり、そのタイム ゾーンの午前 7 時に開始します。</span><span class="sxs-lookup"><span data-stu-id="85c70-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="85c70-124">ただし、予約は割り当ての等高線の最も早い開始時刻となっているため、予約は午前9時に開始されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="85c70-125">リソース C および D: リソースは異なるタイム ゾーンにあり、両方とも互いに異なり、プロジェクトも異なり、予約はそれぞれの利用可能な開始時間より前に開始されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="85c70-126">エンティティ</span><span class="sxs-lookup"><span data-stu-id="85c70-126">Entity</span></span>  |<span data-ttu-id="85c70-127">カレンダー</span><span class="sxs-lookup"><span data-stu-id="85c70-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="85c70-128">プロジェクト カレンダー の テンプレート</span><span class="sxs-lookup"><span data-stu-id="85c70-128">Project calendar template</span></span>   | ![プロジェクト カレンダー](media/reconcile-assignments-06.png) |
|<span data-ttu-id="85c70-130">リソース A</span><span class="sxs-lookup"><span data-stu-id="85c70-130">Resource A</span></span>  | ![リソース A の カレンダー](media/reconcile-assignments-06.png) |
|<span data-ttu-id="85c70-132">リソース B</span><span class="sxs-lookup"><span data-stu-id="85c70-132">Resource B</span></span>  |  ![リソース B の カレンダー](media/reconcile-assignments-07.png) |
|<span data-ttu-id="85c70-134">リソース C</span><span class="sxs-lookup"><span data-stu-id="85c70-134">Resource C</span></span>  |  ![リソース C の カレンダー](media/reconcile-assignments-08.png) |
|<span data-ttu-id="85c70-136">リソース D</span><span class="sxs-lookup"><span data-stu-id="85c70-136">Resource D</span></span>  | ![リソース D の カレンダー](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="85c70-138">**調整** ビューに移動すると、リソース割り当ておよび関連する予約不足が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![拡張前の調整ビュー](media/reconcile-assignments-10.png)

<span data-ttu-id="85c70-140">予約拡張機能が各リソースに使用された後、各リソースの作業時間が不足の等高線と重なるため、予約は各リソースに対して正常に拡張されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![予約拡張機能の後の調整ビュー](media/reconcile-assignments-11.png) 

<span data-ttu-id="85c70-142">予約の詳細を詳しく見ると、予約の開始時間の違いがわかります。</span><span class="sxs-lookup"><span data-stu-id="85c70-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="85c70-143">予約は、割り当て等高線の開始時間より前、およびリソースの使用可能な開始時間より前に開始されます。</span><span class="sxs-lookup"><span data-stu-id="85c70-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![スケジュール ボードにおけるリソースの新規予約](media/reconcile-assignments-12.png)
