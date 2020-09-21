---
title: リソース マネージャー ガイド
description: Project Service でのリソース管理のガイド
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752931"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="60d5e-103">リソース マネージャー ガイド (Project Service)</span><span class="sxs-lookup"><span data-stu-id="60d5e-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="60d5e-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、適切なプロジェクトに対して適切なタイミングで適切なリソースを見つけるのに役立ち、すべてのリソースが確実に効率的に使用されるようにします。</span><span class="sxs-lookup"><span data-stu-id="60d5e-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="60d5e-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で、会社のコンサルタントを効果的かつ効率的に展開します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="60d5e-106">これらの機能では、プロジェクトのコンサルティングの要件およびスケジュールと、コンサルタントのスキルと可用性に基づいてリソースをスケジュールするために必要なツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="60d5e-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="60d5e-107">プロジェクトに取り組むために利用できるほとんどの適格なコンサルタントを簡単に見つけることができ、各プロジェクトの流れの中でコンサルタントを適切にスケジュール方法を簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="60d5e-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="60d5e-108">リソースのスケジューリングは以下の操作の実行に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="60d5e-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="60d5e-109">リソースのスキルおよび能力のレベルとプロジェクトのリソース要件とを照合する方法に基づいて、リソースとプロジェクトとを照合します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="60d5e-110">リソースの可用性とスケジュールされている休暇に基づいて、プロジェクトのカレンダーとリソースのスケジュールを照合します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="60d5e-111">色分けされたカレンダーが、リソースの可用性を一目で分かるように表示します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="60d5e-112">各コンサルタントの容量を確認して、その容量が現在どのように使用されているかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="60d5e-113">これは、コンサルタントの使用率がどこで低い場合があるかまたは高い場合があるか、あるいはコンサルタントが全能力で働いているかどうかを知るために役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="60d5e-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="60d5e-114">作業者の容量の割合または特定の時間数をプロジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="60d5e-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="60d5e-115">グループ リソースの予約を行います。</span><span class="sxs-lookup"><span data-stu-id="60d5e-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="60d5e-116">リソースをソフト予約またはハード予約して、ソフト予約した時間をワンステップでハード予約した時間に変換します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="60d5e-117">プロジェクトの作業分解構造で定義されているリソースに基づいて、プロジェクト チームを自動的に形成します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="60d5e-118">リソースの要求を入力します (代替リソースを予約、提案、または検索します)。</span><span class="sxs-lookup"><span data-stu-id="60d5e-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="60d5e-119">集中モデル (リソース マネージャーが割り当てる) またはハイブリッド モデル (リソース マネージャーおよびその他のマネージャが割り当てできる) に従って、リソースを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="60d5e-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="60d5e-120">集中およびハイブリッド管理モデルの設定の詳細については、[追加パラメーター設定を構成 (Project Service)](../project-service/configure-additional-parameters-settings.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60d5e-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="60d5e-121">プロジェクト全体のリソースを効率的に管理し、プロジェクトの人員を確実に適切に配置します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="60d5e-122">次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60d5e-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="60d5e-123">[リソース要求の管理](../project-service/manage-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="60d5e-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="60d5e-124">コンサルタントのスキルと能力を適切なプロジェクトに対して照合します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="60d5e-125">[ビュー リソースの空き時間](../project-service/view-resource-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="60d5e-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="60d5e-126">コンサルタントの可用性をカレンダー ビューで確認します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="60d5e-127">[ビュー リソースの稼働率](../project-service/view-resource-utilization.md)。</span><span class="sxs-lookup"><span data-stu-id="60d5e-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="60d5e-128">コンサルタントが現在予約されている時間の割合を確認します。</span><span class="sxs-lookup"><span data-stu-id="60d5e-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="60d5e-129">[プロジェクトのリソースをスケジュールする](../project-service/schedule-resources-project.md)。</span><span class="sxs-lookup"><span data-stu-id="60d5e-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="60d5e-130">プロジェクトに対してコンサルタントのスケジュールを設定する</span><span class="sxs-lookup"><span data-stu-id="60d5e-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="60d5e-131">個別のプロジェクトのリソース要求の送信の詳細については、「[リソース要求の送信](../project-service/submit-resource-requests.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60d5e-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="60d5e-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="60d5e-132">See Also</span></span>  
 <span data-ttu-id="60d5e-133">[Project Service の概要](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="60d5e-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="60d5e-134">[管理者ガイド](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="60d5e-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="60d5e-135">[取引先企業管理者ガイド](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="60d5e-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="60d5e-136">[プロジェクト管理者ガイド](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="60d5e-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="60d5e-137">時間、経費、および共同作業ガイド</span><span class="sxs-lookup"><span data-stu-id="60d5e-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
