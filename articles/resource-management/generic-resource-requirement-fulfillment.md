---
title: 汎用リソース要件への対応
description: このトピックでは、汎用的なリソース要件における、名前付きリソースを予約する方法について説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279594"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="eb661-103">汎用リソース要件への対応</span><span class="sxs-lookup"><span data-stu-id="eb661-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="eb661-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="eb661-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb661-105">名前付きリソースを予約して、リソース要件のある汎用的なリソースを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="eb661-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="eb661-106">**プロジェクト** ページで、**チーム** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb661-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="eb661-107">リストからリソース要件を保持している汎用的なリソースを選択し、 **予約する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb661-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="eb661-108">または、リソース要件を開き、 **予約する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb661-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="eb661-109">**スケジュール アシスタント** ページで、プロジェクトチームに登録をする名前付きリソースを選択して、 **予約する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb661-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="eb661-110">予約が完了し、名前付きリソースが実行されると、汎用リソースがチームから削除され、名前付きリソースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="eb661-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="eb661-111">スケジュールの割り当ても同様に名前付きリソースで更新されます。</span><span class="sxs-lookup"><span data-stu-id="eb661-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="eb661-112">複数の名前付きリソースで汎用リソースを使用する</span><span class="sxs-lookup"><span data-stu-id="eb661-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="eb661-113">複数の名前付きリソースを持つ汎用リソースの要件を満たすことは、単一の名前付きリソースを割り当てることと共通しています。</span><span class="sxs-lookup"><span data-stu-id="eb661-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="eb661-114">たとえば、5日間(120時間)の期間を要するタスクがあるとします。</span><span class="sxs-lookup"><span data-stu-id="eb661-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="eb661-115">このタスクを完了するには、1 日 8 時間の労働を 5 日間行う 1 つのリソースでは足りません。</span><span class="sxs-lookup"><span data-stu-id="eb661-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="eb661-116">5日間に渡って自動化技術を120時間稼働させる要件で、これには一日あたり24時間必要となります。</span><span class="sxs-lookup"><span data-stu-id="eb661-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="eb661-117">これは、汎用リソース要求を満たすにあたって、複数の名前付きリソースが必要となる場合の例です。</span><span class="sxs-lookup"><span data-stu-id="eb661-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="eb661-118">要件を実現するには複数のリソースを予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb661-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="eb661-119">このシナリオの主な違いは、汎用リソースはタスクに割り当てられたチームに残り、予約された名前付きリソースチームメンバーは職階の一部として割り当てられないことです。</span><span class="sxs-lookup"><span data-stu-id="eb661-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="eb661-120">プロジェクト管理者は、指定したリソースに必要に応じて作業を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="eb661-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="eb661-121">**調整** ビューを使用すると、プロジェクト管理者は複数のリソースからタスクへの割り当てを分割できます。</span><span class="sxs-lookup"><span data-stu-id="eb661-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="eb661-122">この処理は自動的には実行されません。要件を構成するタスクのバンドルがある場合や、プロジェクト マネージャが行う割り当ての判断基準など、上記のような単純な例よりも複雑なケースではシステムによる想定が必要となるためです。</span><span class="sxs-lookup"><span data-stu-id="eb661-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="eb661-123">システムは意図を理解できないため、想定していたことと意図していたことが異なる可能性が高く、誤った、または予測できない結果が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eb661-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="eb661-124">予測可能な結果は、プロジェクトマネージャが **調整** ビューのサポートを受けて割り当てを行うまで、汎用的なリソースが割り当てられた状態になることです。</span><span class="sxs-lookup"><span data-stu-id="eb661-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]