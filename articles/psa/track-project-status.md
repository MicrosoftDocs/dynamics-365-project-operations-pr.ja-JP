---
title: プロジェクトの状態の追跡
description: Project Service 内のプロジェクトの状態の追跡方法
author: ruhercul
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079354"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="5ca8b-103">プロジェクトの状態の追跡 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="5ca8b-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5ca8b-104">クライアントのプロジェクトの進行状況を追跡するために、[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] を使用します。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="5ca8b-105">取り組みが進行するにつれて、取り組みのステージを反映するようにプロジェクトのステージが更新します:</span><span class="sxs-lookup"><span data-stu-id="5ca8b-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="5ca8b-106">**新規**</span><span class="sxs-lookup"><span data-stu-id="5ca8b-106">**New**</span></span>    | <span data-ttu-id="5ca8b-107">プロジェクトを作成すると、ステージは **新規** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="5ca8b-108">テンプレートからプロジェクトを作成した場合、このステージで、プロジェクトにはスケジュール、見積もりやチーム データがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="5ca8b-109">それ以外の場合、プロジェクトの概要で、手動でプロジェクト コンポーネントの残りを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="5ca8b-110">**見積もり**</span><span class="sxs-lookup"><span data-stu-id="5ca8b-110">**Quote**</span></span>   |      <span data-ttu-id="5ca8b-111">プロジェクトを見積もりに関連付けたり、見積もりからそれを作成する場合、プロジェクト ステージは **見積もり** に設定され、予想される開始日と終了日も同様に更新されます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="5ca8b-112">プロジェクトが見積もりのステージの場合、見積もり明細が **プロジェクト** の **営業** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="5ca8b-113">**計画**</span><span class="sxs-lookup"><span data-stu-id="5ca8b-113">**Plan**</span></span>   |                                     <span data-ttu-id="5ca8b-114">プロジェクトに関連付けられた見積もりが達成され、取り組みが契約ステージに進行すると、プロジェクト ステージは **計画** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="5ca8b-115">**プロジェクト** ページの **営業** タブで、契約の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="5ca8b-116">**完了**</span><span class="sxs-lookup"><span data-stu-id="5ca8b-116">**Complete**</span></span> |                    <span data-ttu-id="5ca8b-117">プロジェクトの作業の完了時に、ステージを **完了** にフリップできます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="5ca8b-118">プロジェクト ステージが完了に設定されると、作業が 100% 完了であるが、プロジェクトは記録される保留時間または経費エントリに対してオープンが保たれることが理解されます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="5ca8b-119">**閉じる**</span><span class="sxs-lookup"><span data-stu-id="5ca8b-119">**Close**</span></span>   |           <span data-ttu-id="5ca8b-120">すべてのトランザクションがプロジェクトに記録され、他に何も記録されることが想定されない場合、手動でステージを **クローズ** に設定できます 。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="5ca8b-121">プロジェクトが **クローズ** に設定されると、プロジェクトに関するトランザクションをもう記録できず、プロジェクトは読み取られるだけです。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="5ca8b-122">プロジェクトの状態を追跡するには</span><span class="sxs-lookup"><span data-stu-id="5ca8b-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="5ca8b-123">**Project Service > プロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="5ca8b-124">作業対象のプロジェクトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="5ca8b-125">画面上部のバーで、プロジェクト名の隣の下矢印を選択してから、 **プロジェクトの追跡** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="5ca8b-126">**行動の追跡** または **コストの追跡** をタスク一覧の上部にあるドロップダウン リストで選択します。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="5ca8b-127">編集するいずれかのタスクをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-127">Double-click any task to edit it.</span></span> <span data-ttu-id="5ca8b-128">また、ガント チャートのバーを移動したり、サイズ変更して、タスクの時間および進行状態を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="5ca8b-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="5ca8b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ca8b-129">See Also</span></span>  
 [<span data-ttu-id="5ca8b-130">プロジェクト管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="5ca8b-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
