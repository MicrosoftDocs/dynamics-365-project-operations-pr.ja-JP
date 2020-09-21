---
title: 重要な概念
description: このトピックでは、Project Service Automation のリソース管理で重要な概念について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f5f96f65-c191-493a-aef7-df7deb52a9cb
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4a839b828d5e1da1e5a8d8a378197b3d4932e529
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752911"
---
# <a name="key-concepts"></a><span data-ttu-id="10e60-103">重要な概念</span><span class="sxs-lookup"><span data-stu-id="10e60-103">Key concepts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="10e60-104">次の表は、Dynamics 365 Project Service Automation アプリで使用される重要な概念を定義します。</span><span class="sxs-lookup"><span data-stu-id="10e60-104">The following table defines key concepts that are used in the Dynamics 365 Project Service Automation app.</span></span>

| <span data-ttu-id="10e60-105">概念</span><span class="sxs-lookup"><span data-stu-id="10e60-105">Concept</span></span>                    | <span data-ttu-id="10e60-106">定義</span><span class="sxs-lookup"><span data-stu-id="10e60-106">Definition</span></span> |
|----------------------------|------------|
| <span data-ttu-id="10e60-107">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="10e60-107">Project team member</span></span>        | <span data-ttu-id="10e60-108">プロジェクト チームの一員として、プロジェクト チーム メンバーは、予約のある名前の付いたリソース、予約のない名前の付いたリソース、または汎用リソースである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10e60-108">As part of the project team, a project team member can be a named resource that has bookings, a named resource that doesn't have bookings, or a generic resource.</span></span> <span data-ttu-id="10e60-109">予約がない汎用リソースは、プロジェクトに対してローカルで、プロジェクト全体で容量制約はありません。</span><span class="sxs-lookup"><span data-stu-id="10e60-109">Generic resources don't have bookings, are local to the project, and don't have capacity constraints across projects.</span></span> |
| <span data-ttu-id="10e60-110">プロジェクトの汎用リソース</span><span class="sxs-lookup"><span data-stu-id="10e60-110">Project generic resource</span></span>   | <span data-ttu-id="10e60-111">名前つきリソースを知ることなく、チームを形成でき、プロジェクト計画にスタッフを配置できるリソース プレースホルダー。</span><span class="sxs-lookup"><span data-stu-id="10e60-111">A resource placeholder that lets you form a team and staff a project plan without having to know the named resource.</span></span> <span data-ttu-id="10e60-112">プロジェクトのカレンダーは汎用リソースのカレンダーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="10e60-112">The project calendar is used as the generic resource's calendar.</span></span> <span data-ttu-id="10e60-113">汎用リソースはプロジェクト チームに追加され、タスクに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="10e60-113">Generic resources can be added to a project team and assigned to tasks.</span></span> |
| <span data-ttu-id="10e60-114">予約された時間</span><span class="sxs-lookup"><span data-stu-id="10e60-114">Booked hours</span></span>               | <span data-ttu-id="10e60-115">リソース時間はプロジェクトに対して本予約されており、プロジェクト作業の完了の保証に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="10e60-115">Resource hours are hard-booked against a project to help guarantee that the project work is completed.</span></span> <span data-ttu-id="10e60-116">予約された時間はリソース全体のキャパシティから消費されます。</span><span class="sxs-lookup"><span data-stu-id="10e60-116">Booked hours are consumed from the resource's overall capacity.</span></span> <span data-ttu-id="10e60-117">予約は、汎用リソースに対してではなく、名前付きのリソース対しておこなわれます。</span><span class="sxs-lookup"><span data-stu-id="10e60-117">Bookings are against named resources only, not against generic resources.</span></span> |
| <span data-ttu-id="10e60-118">割り当てられた時間</span><span class="sxs-lookup"><span data-stu-id="10e60-118">Assigned hours</span></span>             | <span data-ttu-id="10e60-119">リソース時間は、プロジェクト スケジュール内のタスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="10e60-119">Resource hours are assigned to tasks in the project schedule.</span></span> <span data-ttu-id="10e60-120">割り当ては、名前のついたリソースか汎用リソースのいずれかに対しておこなえます。</span><span class="sxs-lookup"><span data-stu-id="10e60-120">Assignments can be against either named resources or generic resources.</span></span> <span data-ttu-id="10e60-121">割り当ては予約からは独立させることができます。</span><span class="sxs-lookup"><span data-stu-id="10e60-121">Assignments can be independent of bookings.</span></span> |
| <span data-ttu-id="10e60-122">必要な時間</span><span class="sxs-lookup"><span data-stu-id="10e60-122">Required hours</span></span>             | <span data-ttu-id="10e60-123">必要だが、名前の付いたリソースによってまだ実行されてないキャパシティ。</span><span class="sxs-lookup"><span data-stu-id="10e60-123">The capacity that is required, but that isn't yet fulfilled by a named resource.</span></span> <span data-ttu-id="10e60-124">必要な時間は、リソース要件を生成した汎用チーム メンバーに対してのみ関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="10e60-124">Required hours are relevant only for generic team members that have generated resource requirements.</span></span> |
| <span data-ttu-id="10e60-125">要求</span><span class="sxs-lookup"><span data-stu-id="10e60-125">Demand</span></span>                     | <span data-ttu-id="10e60-126">現在および将来のワークロード。</span><span class="sxs-lookup"><span data-stu-id="10e60-126">The current and incoming workload.</span></span> <span data-ttu-id="10e60-127">Project Service Automation では、要求は、リソース要件またはリソース要求として表示されます。</span><span class="sxs-lookup"><span data-stu-id="10e60-127">In Project Service Automation, demand is shown as resource requirements or resource requests.</span></span> |
| <span data-ttu-id="10e60-128">リソース要件</span><span class="sxs-lookup"><span data-stu-id="10e60-128">Resource requirement</span></span>       | <span data-ttu-id="10e60-129">必要なり楚洲に対する必要な時間、開始日と終了日、スキル、地理条件、およびその他の価格設定のディメンションを取得するために使用されるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="10e60-129">An entity that is used to capture required hours, start and end dates, skills, geography, and other pricing dimensions for the required resources.</span></span> <span data-ttu-id="10e60-130">リソース要件はプロジェクト チーム メンバーから生成するか、または個別に作成されます。</span><span class="sxs-lookup"><span data-stu-id="10e60-130">Resource requirements are either generated from project team members or individually created.</span></span> |
| <span data-ttu-id="10e60-131">リソース要求</span><span class="sxs-lookup"><span data-stu-id="10e60-131">Resource request</span></span>           | <span data-ttu-id="10e60-132">リソース マネージャーによって実行される必要があるリソース要件を含む「エンベロープ」として使用されるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="10e60-132">An entity that is used as an "envelope" to carry the resource requirement that must be fulfilled by a resource manager.</span></span> |
| <span data-ttu-id="10e60-133">リソースの規定ロール</span><span class="sxs-lookup"><span data-stu-id="10e60-133">Resource default role</span></span>      | <span data-ttu-id="10e60-134">リソースが使用率コンピューティングの下でグループ化されているロール。</span><span class="sxs-lookup"><span data-stu-id="10e60-134">The role that a resource is grouped under for utilization calculation.</span></span> <span data-ttu-id="10e60-135">このリソースはロールに必要なスキルを持ち、そのロールの対象使用率に合うものと仮定されています。</span><span class="sxs-lookup"><span data-stu-id="10e60-135">The resource is assumed to have the required skills for the role and to meet the target utilization for that role.</span></span> |
| <span data-ttu-id="10e60-136">リソース組織単位</span><span class="sxs-lookup"><span data-stu-id="10e60-136">Resource organization unit</span></span> | <span data-ttu-id="10e60-137">リソースが割り当られる組織単位。</span><span class="sxs-lookup"><span data-stu-id="10e60-137">The organizational unit that a resource is assigned to.</span></span> |
| <span data-ttu-id="10e60-138">概略</span><span class="sxs-lookup"><span data-stu-id="10e60-138">Contour</span></span>                    | <span data-ttu-id="10e60-139">タスク、要件、または割り当て時間 (毎日の配分への内訳)。</span><span class="sxs-lookup"><span data-stu-id="10e60-139">Task, requirement, or assignment hours as they are broken down into a daily distribution.</span></span> <span data-ttu-id="10e60-140">たとえば、5 日、40 時間のタスクは、5 日間に渡る 8 時間と設定することができます。</span><span class="sxs-lookup"><span data-stu-id="10e60-140">For example, a five-day, 40-hour task can be contoured into eight hours per day over five days.</span></span> |
| <span data-ttu-id="10e60-141">調整ビュー</span><span class="sxs-lookup"><span data-stu-id="10e60-141">Reconciliation view</span></span>        | <span data-ttu-id="10e60-142">各プロジェクト チーム メンバーの予約や割り当てを示すビュー。</span><span class="sxs-lookup"><span data-stu-id="10e60-142">A view that shows the bookings and assignments for each project team member.</span></span> <span data-ttu-id="10e60-143">このビューでは、プロジェクト マネージャーが予約と割り当ての間の不一致を探し、不一致が発生した場合に修正措置を講じることができます。</span><span class="sxs-lookup"><span data-stu-id="10e60-143">This view lets the project manager look for any mismatch between bookings and assignments, and to take corrective action if any mismatch occurs.</span></span> |
| <span data-ttu-id="10e60-144">作業時間</span><span class="sxs-lookup"><span data-stu-id="10e60-144">Work hours</span></span>                 | <span data-ttu-id="10e60-145">リソース キャパシティ、作業時間と非作業時間の識別に使用されるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="10e60-145">An entity that is used to identify resource capacity, and working and non-working hours.</span></span> <span data-ttu-id="10e60-146">このエンティティは、リソース カレンダーとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="10e60-146">This entity is also referred to as the resource calendar.</span></span> |
