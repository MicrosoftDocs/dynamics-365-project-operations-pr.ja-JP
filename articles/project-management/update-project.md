---
title: プロジェクトの更新
description: このトピックは、Project Operations でプロジェクトを更新する方法について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079123"
---
# <a name="update-a-project"></a><span data-ttu-id="de906-103">プロジェクトの更新</span><span class="sxs-lookup"><span data-stu-id="de906-103">Update a project</span></span>

<span data-ttu-id="de906-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="de906-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de906-105">プロジェクトの作成後に更新できるフィールドおよび適用できる更新の考慮事項の概要は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="de906-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="de906-106">プロジェクト詳細のフィールド</span><span class="sxs-lookup"><span data-stu-id="de906-106">Project detail fields</span></span>

- <span data-ttu-id="de906-107">**名前** : プロジェクトのタイトル。</span><span class="sxs-lookup"><span data-stu-id="de906-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="de906-108">**説明** : プロジェクトの概要。</span><span class="sxs-lookup"><span data-stu-id="de906-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="de906-109">**顧客** : プロジェクトの配信先の会社。</span><span class="sxs-lookup"><span data-stu-id="de906-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="de906-110">**カレンダー テンプレート** : プロジェクトの作業時間。</span><span class="sxs-lookup"><span data-stu-id="de906-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="de906-111">フィールドが変更されると、スケジュール全体が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="de906-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="de906-112">**通貨** : プロジェクトの通貨。</span><span class="sxs-lookup"><span data-stu-id="de906-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="de906-113">このフィールドは、契約単位で定義された通貨に基づいて既定値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="de906-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="de906-114">契約単位が更新されると、フィールドも更新されます。</span><span class="sxs-lookup"><span data-stu-id="de906-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="de906-115">**契約単位** : 営業の獲得、納品、顧客サービスの提供の管理を主に担当する企業グループや部門を表す組織単位。</span><span class="sxs-lookup"><span data-stu-id="de906-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="de906-116">**プロジェクト管理者** : 時間エントリと経費の確認および承認をする権限を持つプロジェクト チーム メンバー。</span><span class="sxs-lookup"><span data-stu-id="de906-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="de906-117">見積もりのフィールド</span><span class="sxs-lookup"><span data-stu-id="de906-117">Estimate fields</span></span>

- <span data-ttu-id="de906-118">**開始予定日** : プロジェクトが開始する日付。</span><span class="sxs-lookup"><span data-stu-id="de906-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="de906-119">このフィールドが更新されると、プロジェクトのすべてのタスクは、新しい開始日に比例して移動します。</span><span class="sxs-lookup"><span data-stu-id="de906-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="de906-120">**終了日** : プロジェクトが終了するようスケジュールされている日付。</span><span class="sxs-lookup"><span data-stu-id="de906-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="de906-121">**工数** : プロジェクトの推定作業量。</span><span class="sxs-lookup"><span data-stu-id="de906-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="de906-122">タスクがプロジェクトに追加されると、このフィールドは編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="de906-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="de906-123">**見積もり労務コスト** : プロジェクトの見積もり労務コスト。</span><span class="sxs-lookup"><span data-stu-id="de906-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="de906-124">労務コストがプロジェクトに追加されると、このフィールドは編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="de906-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="de906-125">**見積もり経費** : プロジェクトの見積もり経費。</span><span class="sxs-lookup"><span data-stu-id="de906-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="de906-126">経費がプロジェクトに追加されると、このフィールドは編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="de906-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="de906-127">プロジェクト実績のフィールド</span><span class="sxs-lookup"><span data-stu-id="de906-127">Project actual fields</span></span>
- <span data-ttu-id="de906-128">**実際の開始日** : プロジェクトが開始した日付。</span><span class="sxs-lookup"><span data-stu-id="de906-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="de906-129">**実際の終了日** : プロジェクトが完了したときに更新されます。</span><span class="sxs-lookup"><span data-stu-id="de906-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="de906-130">プロジェクトの状態のフィールド</span><span class="sxs-lookup"><span data-stu-id="de906-130">Project status fields</span></span>

- <span data-ttu-id="de906-131">**全体的なプロジェクトの状態** : プロジェクト管理者によって提供される全体的なプロジェクトの正常性。</span><span class="sxs-lookup"><span data-stu-id="de906-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="de906-132">**コメント** : プロジェクトの現在の正常性に関してプロジェクト管理者によって提供される説明。</span><span class="sxs-lookup"><span data-stu-id="de906-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

