---
title: アプリ バージョン 2.x でリソースを "仮予約" する方法を教えてください。
description: この記事では、Project Service でプロジェクト チーム メンバーを仮予約する方法を説明します。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122259"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="dc0f7-103">Web アプリでリソースを "仮予約" する方法を教えてください (Project Service アプリ v2.x)。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dc0f7-104">プロジェクトにリソースを割り当てる予定であることを示すため、リソースをプロジェクト チームに一時的にスケジュールつまり "仮予約" することができます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="dc0f7-105">仮予約では、リソースの使用可能なキャパシティが使用されません。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="dc0f7-106">仮予約されたチーム メンバーはプロジェクト タスクに割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="dc0f7-107">[状態] が [本予約済み] で [コミットの種類] が [確定済み] のリソースのみタスクに割り当てることができます (割り当ての工数をカバーするのに十分な本予約時間があることが前提)。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="dc0f7-108">仮予約されたプロジェクト チーム メンバーは、[仮予約] 列に仮予約時間が表示された状態でチーム メンバー グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="dc0f7-109">スケジュール ボードにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-109">They also show up on the schedule board.</span></span> <span data-ttu-id="dc0f7-110">繰り返しになりますが、仮予約はリソースのキャパシティを使用しないため、キャパシティの消費は表示されません。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="dc0f7-111">Project Service バージョン 2.x でチーム メンバーをプロジェクトに仮予約する方法は 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="dc0f7-112">スケジュール ボードで仮予約する、[予約の維持管理] 機能を使用する、または汎用リソースを作成する、です。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="dc0f7-113">これらの方法について以下に詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="dc0f7-114">スケジュール ボードで仮予約</span><span class="sxs-lookup"><span data-stu-id="dc0f7-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="dc0f7-115">スケジュール ボードを使用して仮予約するには、この手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="dc0f7-116">スケジュール ボードを開きます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-116">Open the schedule board.</span></span>
2. <span data-ttu-id="dc0f7-117">スケジュール ボードの下部の [要件の予約] パネルで [プロジェクト] タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="dc0f7-118">リソースを仮予約するプロジェクトを探します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="dc0f7-119">多くのプロジェクトがある場合、プロジェクトの列見出しをクリックし、フィルターを使用してプロジェクトを見つけます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="dc0f7-120">プロジェクトをクリックし、リソースの時間グリッドにドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="dc0f7-121">右側に [リソース予約の作成] パネルが開きます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="dc0f7-122">開始日と終了日を調整し、[予約の状態] として [仮] を選択して時間を設定します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="dc0f7-123">[予約] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-123">Click Book.</span></span>
7. <span data-ttu-id="dc0f7-124">プロジェクトに戻ると、リソースがチーム メンバーとして表示されるようになり、[仮予約] 列に仮予約時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="dc0f7-125">リソースを割り当てるにはチームで本予約されている必要があるため、WBS (作業分解構造) でタスクに割り当てることはできない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="dc0f7-126">[予約の維持管理] 機能を使用して仮予約</span><span class="sxs-lookup"><span data-stu-id="dc0f7-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="dc0f7-127">[予約の維持管理] を使用して仮予約するには、この手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="dc0f7-128">チーム メンバー グリッドから、[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="dc0f7-129">予約可能リソース、ロール、開始日、終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="dc0f7-130">[なし] 以外の割り当て方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="dc0f7-131">全キャパシティ</span><span class="sxs-lookup"><span data-stu-id="dc0f7-131">Full Capacity</span></span>
- <span data-ttu-id="dc0f7-132">キャパシティの割合</span><span class="sxs-lookup"><span data-stu-id="dc0f7-132">Percentage Capacity</span></span>
- <span data-ttu-id="dc0f7-133">時間別 - 均等分布</span><span class="sxs-lookup"><span data-stu-id="dc0f7-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="dc0f7-134">時間別 - 前倒し</span><span class="sxs-lookup"><span data-stu-id="dc0f7-134">By Hours Front Load</span></span>
4. <span data-ttu-id="dc0f7-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-135">Click Save.</span></span> <span data-ttu-id="dc0f7-136">チーム グリッドにリソースが表示され、その時間が [本] と示されます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="dc0f7-137">[予約の維持管理] をクリックし、リソースの予約を維持管理します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="dc0f7-138">スケジュール ボードが開いた状態で、予約を表示するためにリソースを展開します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="dc0f7-139">予約が [本] として表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="dc0f7-140">予約を右クリックし、[状態の変更] で [仮予約]、[仮] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="dc0f7-141">予約の状態が [仮] になります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="dc0f7-142">スケジュール ボードを閉じると、チーム メンバー グリッドでリソースの時間が [本] から [仮] に変わったのがわかります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="dc0f7-143">リソースをチームに本予約し、WBS でそれらにタスクを割り当てた場合、予約の維持管理を使って状態を [本] から [仮] に変更すると、そのリソースのタスクから割り当てが削除されます。本予約されたリソースのみタスクに割り当てることができるためです。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="dc0f7-144">汎用リソースの作成による仮予約</span><span class="sxs-lookup"><span data-stu-id="dc0f7-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="dc0f7-145">汎用リソース チーム メンバーを生成して、スケジュール ボードやリソース要求を実行し、予約時に種類を変更することで、仮予約を作成できます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="dc0f7-146">これを行うには、以下の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="dc0f7-147">プロジェクト WBS で、汎用チーム メンバーを生成するタスクにロールを割り当ててください。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="dc0f7-148">[プロジェクト チームの生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="dc0f7-149">プロジェクト チーム メンバー グリッドで、汎用リソースを選択し、[予約] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="dc0f7-150">スケジュール ボードで、予約するリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="dc0f7-151">スケジュール ボードの [リソース予約の作成] パネルで、[予約の状態] を [仮] に変更します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="dc0f7-152">[予約] または [予約して終了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="dc0f7-153">スケジュール ボードを閉じると、仮予約時間および割り当てられた時間と共に、選択されたリソースがチームに追加されたのがわかります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="dc0f7-154">タスクが仮予約されたチーム メンバーに割り当てられたことのインジケーターとして、汎用リソースがチームに残っているのがわかります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="dc0f7-155">タスクに割り当てることができるように、本予約されたチーム メンバーに仮予約されたチーム メンバーのリソースを変更する準備ができたら、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="dc0f7-156">そのリソースを選択し、[予約の維持管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="dc0f7-157">スケジュール ボードが開いた状態で、予約を表示するためにリソースを展開します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="dc0f7-158">予約が [仮] としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="dc0f7-159">予約を右クリックし、[状態の変更] で [本予約]、[本] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="dc0f7-160">予約の状態が [本] になります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="dc0f7-161">スケジュール ボードを閉じると、チーム メンバー グリッドでリソースの時間が [仮] から [本] に変わったのがわかります。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="dc0f7-162">リソースをタスクに割り当てることができるようになりました (本予約された時間と、割り当てるタスクの工数が一致していることが前提)。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="dc0f7-163">上の項目 3 にある汎用リソース実行ステップに従った場合、仮予約された予約可能リソースの状態を [本] に変更すると、汎用チーム メンバーはチームから削除されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc0f7-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
