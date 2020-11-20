---
title: スケジュール ボードからプロジェクトの予約を作成する
description: このトピックでは、スケジュールボードからプロジェクトの予約を作成する方法についての情報を提供します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122304"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="4e17a-103">スケジュール ボードからプロジェクトの予約を作成する</span><span class="sxs-lookup"><span data-stu-id="4e17a-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="4e17a-104">プロジェクトにリソースを登録するには、プロジェクトの **チーム** タブから直接登録するか、汎用的なチームメンバーの割当てからリソース要件を生成し、生成された要件をプロジェクトチームメンバーとともに満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="4e17a-105">また、スケジュール ボードからリソースをプロジェクトに直接予約することができます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="4e17a-106">これを行うには 3 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-106">There are three ways to do this:</span></span>

- <span data-ttu-id="4e17a-107">**生成されたリソース要件から予約する:** 汎用リソースを作成し、プロジェクト内でタスクを割り当てた後に、リソース要件を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="4e17a-108">**主要要件から予約する:** 主要な要件は、**プロジェクト** タブのスケジュールボードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="4e17a-109">**新規リソース要件から予約する:** リソース要件を最初から作成し、プロジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="4e17a-110">スケジュール ボードで、リソース要件は **オープンな要件** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="4e17a-111">生成されるリソース要件から予約</span><span class="sxs-lookup"><span data-stu-id="4e17a-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="4e17a-112">汎用リソースを作成し、それに対してプロジェクト内のタスクまたは複数のタスクを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="4e17a-113">次に、汎用チーム メンバーからリソース要件を生成してください。</span><span class="sxs-lookup"><span data-stu-id="4e17a-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="4e17a-114">スケジュール ボードで、このリソースは **オープンな要件** タブに表示されます。オープンな要件がたくさんある場合は、グリッドにて列フィルターを使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="4e17a-115">![スケジュール ボードで要件タブを起動する](media/FAQ-Project-Booking-Schedule-Board-1.png "予約および割り当てテーブルのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="4e17a-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="4e17a-116">要件を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e17a-116">Select the requirement.</span></span> <span data-ttu-id="4e17a-117">**空き時間の検索** タブは、選択された行の先頭に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="4e17a-118">タブを選択すると、スケジュール ボードのスケジュール アシスタント モードが開き、リソース要件を満たす利用可能なリソースがフィルタされます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="4e17a-119">そこからリソースを予約することができます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="4e17a-120">スケジュール ボードの下部から上のグリッドのリソースのセルに、選択した行をドラッグ アンド ドロップすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="4e17a-121">ドロップすると、右側に **リソース予約の作成** パネルが開きます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="4e17a-122">**予約** を選択すると、プロジェクト チームにリソースが予約されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-122">Selecting **Book** books the resource onto the project team.</span></span>

![リソース予約パネルの作成](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="4e17a-124">プライマリ要件から予約</span><span class="sxs-lookup"><span data-stu-id="4e17a-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="4e17a-125">Project Service でプロジェクトを作成すると、自動的にプライマリ要件と呼ばれるリソース要件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="4e17a-126">これは、要件の生成や新規作成をすることなく、スケジュール ボードを使用してリソースを迅速に予約する目的で使用される空の要件です。</span><span class="sxs-lookup"><span data-stu-id="4e17a-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="4e17a-127">要件は空であるため、日付、割り当て方法、時間 (該当する場合) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="4e17a-128">主要な要件を持つリソースを予約するには、スケジュール ボードで **プロジェクト** タブを選択します。プロジェクトが多数ある場合は、 **プロジェクト** 列で列フィルタを使用した方がよい場合があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="4e17a-129">![スケジュール ボードの列フィルター](media/FAQ-Project-Booking-Schedule-Board-2.png "予約および割り当てテーブルのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="4e17a-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="4e17a-130">プロジェクトの名前が設定されていても、期間が0となっている要件を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e17a-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="4e17a-131">行に表示された **空き時間の検索** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e17a-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="4e17a-132">これにより、スケジュール ボードがスケジュール アシスタント モードになり、プロジェクトで予約できる利用可能なリソースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="4e17a-133">**主要な要件** に要件が割り当てられておらず期間が 0 となっているので、リソースを選択して予約する際に、 **リソースの予約を作成** パネルで期間を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="4e17a-134">また、スケジュール ボードの下部にある **プロジェクトのプライマリ要件** を選択し、リソースにドラッグ アンド ドロップして予約することもできます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="4e17a-135">**主要な要件** に要件が割り当てられておらず期間が 0 となっているので、リソースを選択して予約する際に、 **リソースの予約を作成** パネルで期間を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="4e17a-136">スケジュールボードの **主要な要件** 使用してリソースを登録すると、割り当ての処理がされずにでプロジェクトチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="4e17a-137">新しいリソース要件から予約</span><span class="sxs-lookup"><span data-stu-id="4e17a-137">Book from a new resource requirement</span></span>
<span data-ttu-id="4e17a-138">新しいリソース要件から予約するには、以下手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="4e17a-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="4e17a-139">**リソース要件** に移動し、 **新規** を選択して新しいリソース要件を作成します。</span><span class="sxs-lookup"><span data-stu-id="4e17a-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="4e17a-140">**プロジェクト** タブで、プロジェクトを選択して、要件をプロジェクトに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="4e17a-141">スケジュール ボードで、この新しい要件は実行可能な **オープンな要件** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e17a-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="4e17a-142">リソースを予約してプロジェクトチームに追加します。</span><span class="sxs-lookup"><span data-stu-id="4e17a-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="4e17a-143">これでリソースが予約されました。タスクは手動で割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e17a-143">Now that the resource is booked, you must assign tasks manually.</span></span>

