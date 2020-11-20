---
title: リソース マネージャー ガイド
description: Project Service でのリソース管理のガイド
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 04ee87e5b1a2cf96434f4862e07d2b85bad9eace
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124014"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="e1bf8-103">リソース マネージャー ガイド (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e1bf8-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e1bf8-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、適切なプロジェクトに対して適切なタイミングで適切なリソースを見つけるのに役立ち、すべてのリソースが確実に効率的に使用されるようにします。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="e1bf8-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で、会社のコンサルタントを効果的かつ効率的に展開します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="e1bf8-106">これらの機能では、プロジェクトのコンサルティングの要件およびスケジュールと、コンサルタントのスキルと可用性に基づいてリソースをスケジュールするために必要なツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="e1bf8-107">プロジェクトに取り組むために利用できるほとんどの適格なコンサルタントを簡単に見つけることができ、各プロジェクトの流れの中でコンサルタントを適切にスケジュール方法を簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="e1bf8-108">リソースのスケジューリングは以下の操作の実行に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="e1bf8-109">リソースのスキルおよび能力のレベルとプロジェクトのリソース要件とを照合する方法に基づいて、リソースとプロジェクトとを照合します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="e1bf8-110">リソースの可用性とスケジュールされている休暇に基づいて、プロジェクトのカレンダーとリソースのスケジュールを照合します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="e1bf8-111">色分けされたカレンダーが、リソースの可用性を一目で分かるように表示します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="e1bf8-112">各コンサルタントの容量を確認して、その容量が現在どのように使用されているかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="e1bf8-113">これは、コンサルタントの使用率がどこで低い場合があるかまたは高い場合があるか、あるいはコンサルタントが全能力で働いているかどうかを知るために役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="e1bf8-114">作業者の容量の割合または特定の時間数をプロジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="e1bf8-115">グループ リソースの予約を行います。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="e1bf8-116">リソースをソフト予約またはハード予約して、ソフト予約した時間をワンステップでハード予約した時間に変換します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="e1bf8-117">プロジェクトの作業分解構造で定義されているリソースに基づいて、プロジェクト チームを自動的に形成します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="e1bf8-118">リソースの要求を入力します (代替リソースを予約、提案、または検索します)。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="e1bf8-119">集中モデル (リソース マネージャーが割り当てる) またはハイブリッド モデル (リソース マネージャーおよびその他のマネージャが割り当てできる) に従って、リソースを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="e1bf8-120">集中およびハイブリッド管理モデルの設定の詳細については、[追加パラメーター設定を構成 (Project Service)](../psa/configure-additional-parameters-settings.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="e1bf8-121">プロジェクト全体のリソースを効率的に管理し、プロジェクトの人員を確実に適切に配置します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="e1bf8-122">次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="e1bf8-123">[リソース要求の管理](../psa/manage-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="e1bf8-124">コンサルタントのスキルと能力を適切なプロジェクトに対して照合します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="e1bf8-125">[ビュー リソースの空き時間](../psa/view-resource-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="e1bf8-126">コンサルタントの可用性をカレンダー ビューで確認します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="e1bf8-127">[ビュー リソースの稼働率](../psa/view-resource-utilization.md)。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="e1bf8-128">コンサルタントが現在予約されている時間の割合を確認します。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="e1bf8-129">[プロジェクトのリソースをスケジュールする](../psa/schedule-resources-project.md)。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="e1bf8-130">プロジェクトに対してコンサルタントのスケジュールを設定する</span><span class="sxs-lookup"><span data-stu-id="e1bf8-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="e1bf8-131">個別のプロジェクトのリソース要求の送信の詳細については、「[リソース要求の送信](../psa/submit-resource-requests.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1bf8-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e1bf8-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1bf8-132">See Also</span></span>  
 <span data-ttu-id="e1bf8-133">[Project Service の概要](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="e1bf8-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="e1bf8-134">[管理者ガイド](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e1bf8-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="e1bf8-135">[取引先企業管理者ガイド](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e1bf8-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="e1bf8-136">[プロジェクト管理者ガイド](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e1bf8-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="e1bf8-137">時間、経費、および共同作業ガイド</span><span class="sxs-lookup"><span data-stu-id="e1bf8-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
