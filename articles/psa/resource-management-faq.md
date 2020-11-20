---
title: リソース管理に関するよくある質問
description: このトピックでは、リソース管理についてのよくある質問への回答を提供します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120144"
---
# <a name="resource-management-faq"></a><span data-ttu-id="e94dc-103">リソース管理に関するよくある質問</span><span class="sxs-lookup"><span data-stu-id="e94dc-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="e94dc-104">チーム メンバーとリソース要件の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="e94dc-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="e94dc-105">プロジェクト チーム メンバーは、タスクが割り当てられたり、予約または超過予約されたり、承認者として設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="e94dc-106">リソース要件は、要求の下書きメモとして、プロジェクト チーム メンバーなしでも存在することができます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="e94dc-107">提案された時間と仮予約された時間の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="e94dc-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="e94dc-108">提案された時間と仮予約された時間は表示形式が異なります。</span><span class="sxs-lookup"><span data-stu-id="e94dc-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="e94dc-109">提案された時間は、リソース要求を使用して要求を開始したリソース マネージャーのみに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="e94dc-110">仮予約された時間は、スケジュール ボードにアクセスできるすべてのユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="e94dc-111">チーム上でリソースに仮予約された時間はどうしたら見れますか？</span><span class="sxs-lookup"><span data-stu-id="e94dc-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="e94dc-112">仮予約は、リソース要件を予約した際に予約することができます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="e94dc-113">プロジェクト チームで仮予約されたリソースは、時間が仮予約されたチーム メンバーとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="e94dc-114">これらはスケジュール ボード上でも表示されます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="e94dc-115">予約したリソースに対して、必要な時間を変更し、1 日の開始および終了はどのようにおこないますか。</span><span class="sxs-lookup"><span data-stu-id="e94dc-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="e94dc-116">リソースを予約した後、**予約の維持** を選択して、必要な変更をおこないます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="e94dc-117">Project Service Automation ではどのような種類のリソースをサポートしますか？</span><span class="sxs-lookup"><span data-stu-id="e94dc-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="e94dc-118">**ユーザー** および **取引先担当者** が Dynamics 365 Project Service Automation でサポートされている唯一のリソースの種類です。</span><span class="sxs-lookup"><span data-stu-id="e94dc-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="e94dc-119">その他の種類 (**備品**、**グループ** など) のリソースも作成可能ですが、これはエンド ツー エンドでの使用はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e94dc-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="e94dc-120">割り当てと予約の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="e94dc-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="e94dc-121">割り当ては、プロジェクト スケジュール内のプロジェクト タスクに対するリソースの割り当てです。</span><span class="sxs-lookup"><span data-stu-id="e94dc-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="e94dc-122">このリソースは、実際のリソースまたは汎用リソースのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="e94dc-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="e94dc-123">予約は、プロジェクトに対するリソースの本配賦または仮配賦です。</span><span class="sxs-lookup"><span data-stu-id="e94dc-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="e94dc-124">本予約はリソースのキャパシティを消費します。</span><span class="sxs-lookup"><span data-stu-id="e94dc-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="e94dc-125">理想としては、実際のリソースに対して、予約と割り当ては違いがないことから、これらは一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e94dc-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="e94dc-126">ただし、PSA はこの一致を強制しません。</span><span class="sxs-lookup"><span data-stu-id="e94dc-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="e94dc-127">調整ビューでは、リソースの予約と割り当てが一致しない場所のプロジェクト マネージャーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e94dc-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
