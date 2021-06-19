---
title: リソース要件で名前付きリソースを予約する。
description: このトピックでは、汎用的なリソース要件における、名前付きリソースの予約について説明します。
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013402"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="34b88-103">リソース要件で名前付きリソースを予約する。</span><span class="sxs-lookup"><span data-stu-id="34b88-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="34b88-104">名前付きリソースを予約して、リソース要件のある汎用的なリソースを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="34b88-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="34b88-105">Project Service Automation (PSA)の **プロジェクト** ページで、 **チーム** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="34b88-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="34b88-106">リストからリソース要件を保持している汎用的なリソースを選択し、 **予約する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34b88-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="34b88-107">または、リソース要件を開き、 **予約する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34b88-107">Or, open the resource requirement and then click **Book**.</span></span>


![汎用チームメンバーを予約する](media/RM-how-to-14.png)


3. <span data-ttu-id="34b88-109">**スケジュール アシスタント** ページで、プロジェクトチームに登録をする名前付きリソースを選択して、 **予約する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34b88-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![スケジュール アシスタントを使用して汎用的なチームメンバーを予約する](media/RM-how-to-15.png)

<span data-ttu-id="34b88-111">予約が完了し、名前付きリソースが実行されると、汎用リソースがチームから削除され、名前付きリソースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="34b88-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![名前付きメンバーが汎用チームメンバーを置き換える](media/RM-how-to-16.png)

<span data-ttu-id="34b88-113">スケジュールの割り当ても同様に名前付きリソースで更新されます。</span><span class="sxs-lookup"><span data-stu-id="34b88-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![名前付きメンバーがプロジェクトのタスクに割り当てられる](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="34b88-115">複数の名前付きリソースで汎用リソースを使用する</span><span class="sxs-lookup"><span data-stu-id="34b88-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="34b88-116">複数の名前付きリソースを持つ汎用リソースの要件を満たすことは、単一の名前付きリソースを割り当てることと共通しています。</span><span class="sxs-lookup"><span data-stu-id="34b88-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="34b88-117">たとえば、5日間(120時間)の期間を要するタスクがあるとします。</span><span class="sxs-lookup"><span data-stu-id="34b88-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="34b88-118">このタスクを完了するには、1日8時間の労働を5日間行う1つのリソースでは足りません。</span><span class="sxs-lookup"><span data-stu-id="34b88-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![ここでは、5日間で120時間分の作業が必要となります。](media/RM-how-to-21.png)

<span data-ttu-id="34b88-120">5日間に渡って自動化技術を120時間稼働させる要件で、これには一日あたり24時間必要となります。</span><span class="sxs-lookup"><span data-stu-id="34b88-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![各日ごとの要件](media/RM-how-to-22.png)

<span data-ttu-id="34b88-122">これは、汎用リソース要求を満たすにあたって、複数の名前付きリソースが必要となる場合の例です。</span><span class="sxs-lookup"><span data-stu-id="34b88-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="34b88-123">要件を実現するには複数のリソースを予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34b88-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![要件を実現するために複数のリソースを予約する](media/RM-how-to-23.png)

<span data-ttu-id="34b88-125">このシナリオの主な違いは、汎用リソースはタスクに割り当てられたチームに残り、予約された名前付きリソースチームメンバーは職階の一部として割り当てられないことです。</span><span class="sxs-lookup"><span data-stu-id="34b88-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="34b88-126">プロジェクト管理者は、指定したリソースに必要に応じて作業を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34b88-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="34b88-127">**調整** ビューを使用すると、プロジェクト管理者は複数のリソースからタスクへの割り当てを分割できます。</span><span class="sxs-lookup"><span data-stu-id="34b88-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="34b88-128">この処理は自動的には実行されません。要件を構成するタスクのバンドルがある場合や、プロジェクトマネージャが行う割り当ての判断基準など、上記のような単純な例よりも複雑なケースではシステムが想定する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="34b88-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="34b88-129">システムは意図を理解できないため、想定が意図と異なる可能性があり、誤った、または予測できない結果が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="34b88-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="34b88-130">予測可能な結果は、プロジェクトマネージャが **調整** ビューのサポートを受けて割り当てを行うまで、汎用的なリソースが割り当てられた状態になることです。</span><span class="sxs-lookup"><span data-stu-id="34b88-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]