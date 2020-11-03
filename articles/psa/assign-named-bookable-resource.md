---
title: 名前付き予約可能リソースをプロジェクト チームに予約して、タスクを割り当てる
description: このトピックでは、プロジェクト チームに名前付きリソースを予約し、タスクに割り当てる方法を説明します。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079387"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="9e784-103">名前付き予約可能リソースをプロジェクト チームに予約して、タスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="9e784-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9e784-104">チームに直接予約することで、プロジェクト チームに名前付きリソースを追加できます。</span><span class="sxs-lookup"><span data-stu-id="9e784-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="9e784-105">それには、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="9e784-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="9e784-106">Project Service Automation で **プロジェクト** に移動して、予約するプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e784-106">In  Project Service Automation, go to **Projects** , and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="9e784-107">**プロジェクト** ページの **チーム** タブで **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e784-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![チームタブからチーム メンバーを追加する](media/RM-how-to-1.png)

3. <span data-ttu-id="9e784-109">**プロジェクト チーム メンバーの簡易作成** ダイアログ ボックスで、予約可能リソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e784-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="9e784-110">リソースのデフォルトの役割が割り当てられている場合、 **役割** フィールドにその役割が入力されます。</span><span class="sxs-lookup"><span data-stu-id="9e784-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="9e784-111">必要に応じて役割を変更できます。</span><span class="sxs-lookup"><span data-stu-id="9e784-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="9e784-112">リソースが必要な開始日と終了日を選択し、リソースの容量の割り当て方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e784-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="9e784-113">チーム メンバーをプロジェクト承認者にしたい場合は **プロジェクト承認者** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e784-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="9e784-114">これで、そのチーム メンバーがこのプロジェクトに提出された時間と費用のエントリを承認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9e784-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="9e784-115">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e784-115">Click **Save**.</span></span>

![クイック作成フォームにチーム メンバーを追加する](media/RM-how-to-2.png)


<span data-ttu-id="9e784-117">これで、予約したリソースをプロジェクトのタスクに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9e784-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="9e784-118">**プロジェクト** ページで **スケジュール** タブをクリックして、タスクを新しいリソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9e784-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="9e784-119">タスク グリッドの **リソース** フィールドから起動するリソース ピッカーに、選択可能なチーム メンバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e784-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![スケジュール タブでタスクにチーム メンバーを割り当てる](media/RM-how-to-3.png)

<span data-ttu-id="9e784-121">Project Service Automation (PSA) のバージョン 3 では、リソースの予約とタスクの割り当ては緊密に結び付いていません。</span><span class="sxs-lookup"><span data-stu-id="9e784-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="9e784-122">つまり、スケジュールでリソース ピッカーを使用すると、プロジェクトで予約がカバーする時間よりも長い時間タスクをチーム メンバーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9e784-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="9e784-123">チーム メンバーの予約と割り当ての違いは **チーム** タブや **リソースの調整** タブで確認できます。また、リソースの予約と割り当ての違いをより詳細なレベルで調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="9e784-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![リソースの調整タブ](media/RM-how-to-4.png)

<span data-ttu-id="9e784-125">**スケジュール** タブのリソース ピッカーを使用して、プロジェクト チームにまだ含まれていない予約可能リソースを検索して選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="9e784-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="9e784-126">これらは **そのほかのリソース** としてリソース ピッカーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e784-126">These are shown in the resource picker as **Other Resources**.</span></span>

![チーム メンバー以外のリソースをタスクに割り当てる](media/RM-how-to-5.png)

<span data-ttu-id="9e784-128">これを行った場合、リソースをプロジェクト チームに追加してタスクに割り当てますが、予約は生成しません。</span><span class="sxs-lookup"><span data-stu-id="9e784-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![割り当てがあり、予約がないチーム メンバー](media/RM-how-to-6.png)

<span data-ttu-id="9e784-130">**調整** タブの拡張予約機能や **スケジュール ボード** を使用して、リソースの容量をプロジェクトに予約できます。</span><span class="sxs-lookup"><span data-stu-id="9e784-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![リソース調整 タブでのチーム メンバーの予約の延長](media/RM-how-to-7.png)

<span data-ttu-id="9e784-132">チーム メンバーをプロジェクトに予約した後で、予約の管理を使用するかスケジュール ボードを直接使用して予約を管理できます。</span><span class="sxs-lookup"><span data-stu-id="9e784-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
