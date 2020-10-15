---
title: チーム メンバーの維持管理
description: このトピックでは、プロジェクト チームに名前付きリソースを予約して、タスクに割り当てる方法を説明します。
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961893"
---
# <a name="maintain-team-members"></a><span data-ttu-id="9ad72-103">チーム メンバーの維持管理</span><span class="sxs-lookup"><span data-stu-id="9ad72-103">Maintain team members</span></span>

<span data-ttu-id="9ad72-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="9ad72-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9ad72-105">チームに直接予約することで、プロジェクト チームに名前付きリソースを追加できます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="9ad72-106">Dynamics 365 プロジェクト オペレーションで**プロジェクト**に移動して、予約するプロジェクトを開くを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ad72-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="9ad72-107">**チーム** タブの**プロジェクト** ページで**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ad72-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="9ad72-108">**プロジェクト チーム メンバーの簡易作成** ダイアログ ボックスで、予約可能リソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ad72-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="9ad72-109">リソースのデフォルトの役割が割り当てられている場合、**役割** フィールドにその役割が入力されます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="9ad72-110">役割を変更できます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-110">You can change the role.</span></span> 
4. <span data-ttu-id="9ad72-111">リソースが必要な開始日と終了日を選択し、リソースの容量の割り当て方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ad72-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="9ad72-112">チーム メンバーをプロジェクト承認者にしたい場合は、**プロジェクト承認者**フィールドで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ad72-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="9ad72-113">チーム メンバーは、このプロジェクトに提出された時間と経費のエントリを承認できます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="9ad72-114">**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ad72-114">Select **Save**.</span></span>

<span data-ttu-id="9ad72-115">これで、予約したリソースをプロジェクトのタスクに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="9ad72-116">**スケジュール** タブの**プロジェクト** ページで、タスクを新しいリソースに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="9ad72-117">タスク グリッドの **リソース** フィールドから起動するリソース ピッカーに、選択可能なチーム メンバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="9ad72-118">プロジェクト オペレーションでは、リソース予約とタスク割り当ては緊密に結びついていません。</span><span class="sxs-lookup"><span data-stu-id="9ad72-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="9ad72-119">スケジュールでリソース ピッカーを使用する場合、プロジェクトで予約がカバーする時間よりも長い時間タスクをチーム メンバーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="9ad72-120">チーム メンバーの予約と割り当ての違いは、**チーム**および**リソースの調整**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="9ad72-121">より詳細なレベルで、リソースの予約と割り当ての違いを調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="9ad72-122">**スケジュール** タブのリソース ピッカーを使用して、プロジェクト チームにまだ含まれていない予約可能リソースを検索して選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="9ad72-123">これらのリソースは**その他のリソース**としてリソース ピッカーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="9ad72-124">選択を行う場合、リソースはプロジェクト チームに追加されタスクに割り当てられますが、予約は生成されません。</span><span class="sxs-lookup"><span data-stu-id="9ad72-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="9ad72-125">**調整** タブの拡張予約機能や **スケジュール ボード** を使用して、リソースの容量をプロジェクトに予約できます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="9ad72-126">チーム メンバーをプロジェクトに予約した後で、**予約の管理**または**スケジュール ボード**を直接使用して予約を管理できます。</span><span class="sxs-lookup"><span data-stu-id="9ad72-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
