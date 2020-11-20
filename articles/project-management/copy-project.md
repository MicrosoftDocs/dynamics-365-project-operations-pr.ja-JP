---
title: プロジェクトのコピー
description: このトピックでは、Dynamics 365 Project Operations でのプロジェクトのコピーについて説明します。
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131799"
---
# <a name="copy-a-project"></a><span data-ttu-id="3d861-103">プロジェクトのコピー</span><span class="sxs-lookup"><span data-stu-id="3d861-103">Copy a project</span></span>

<span data-ttu-id="3d861-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="3d861-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d861-105">Dynamics 365 Project Operations を使用すると、**プロジェクト** フォームの **プロジェクトのコピー** を選択して新しいプロジェクトをすばやく構築できます。</span><span class="sxs-lookup"><span data-stu-id="3d861-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="3d861-106">プロジェクトをコピーするには、コピーするプロジェクトを開き、**プロジェクトのコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d861-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="3d861-107">操作は以下をコピーします:</span><span class="sxs-lookup"><span data-stu-id="3d861-107">The action will copy:</span></span>

- <span data-ttu-id="3d861-108">プロジェクト プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d861-108">Project properties</span></span>
- <span data-ttu-id="3d861-109">WBS(作業分解構造)</span><span class="sxs-lookup"><span data-stu-id="3d861-109">The Work breakdown structure</span></span>
- <span data-ttu-id="3d861-110">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="3d861-110">Project team members</span></span>
- <span data-ttu-id="3d861-111">プロジェクト見積もり</span><span class="sxs-lookup"><span data-stu-id="3d861-111">Project estimates</span></span>
- <span data-ttu-id="3d861-112">プロジェクト経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="3d861-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="3d861-113">プロジェクト プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d861-113">Project properties</span></span>

<span data-ttu-id="3d861-114">プロジェクトがコピーされると、次のフィールドの値がコピーされます:</span><span class="sxs-lookup"><span data-stu-id="3d861-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="3d861-115">件名</span><span class="sxs-lookup"><span data-stu-id="3d861-115">Name</span></span>
- <span data-ttu-id="3d861-116">内容</span><span class="sxs-lookup"><span data-stu-id="3d861-116">Description</span></span>
- <span data-ttu-id="3d861-117">顧客</span><span class="sxs-lookup"><span data-stu-id="3d861-117">Customer</span></span>
- <span data-ttu-id="3d861-118">カレンダー テンプレート</span><span class="sxs-lookup"><span data-stu-id="3d861-118">Calendar Template</span></span>
- <span data-ttu-id="3d861-119">通貨</span><span class="sxs-lookup"><span data-stu-id="3d861-119">Currency</span></span>
- <span data-ttu-id="3d861-120">契約単位</span><span class="sxs-lookup"><span data-stu-id="3d861-120">Contracting Unit</span></span>
- <span data-ttu-id="3d861-121">プロジェクト管理者</span><span class="sxs-lookup"><span data-stu-id="3d861-121">Project Manager</span></span>
- <span data-ttu-id="3d861-122">ステータス</span><span class="sxs-lookup"><span data-stu-id="3d861-122">Status</span></span>
- <span data-ttu-id="3d861-123">全体的なプロジェクトの状態</span><span class="sxs-lookup"><span data-stu-id="3d861-123">Overall Project Status</span></span>
- <span data-ttu-id="3d861-124">コメント</span><span class="sxs-lookup"><span data-stu-id="3d861-124">Comments</span></span>
- <span data-ttu-id="3d861-125">見積もり</span><span class="sxs-lookup"><span data-stu-id="3d861-125">Estimates</span></span>
- <span data-ttu-id="3d861-126">開始予定日</span><span class="sxs-lookup"><span data-stu-id="3d861-126">Estimated Start Date</span></span>
- <span data-ttu-id="3d861-127">終了日</span><span class="sxs-lookup"><span data-stu-id="3d861-127">Finish Date</span></span>
- <span data-ttu-id="3d861-128">工数 (時間)</span><span class="sxs-lookup"><span data-stu-id="3d861-128">Effort (Hours)</span></span>
- <span data-ttu-id="3d861-129">見積もり労務コスト</span><span class="sxs-lookup"><span data-stu-id="3d861-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="3d861-130">見積もり経費</span><span class="sxs-lookup"><span data-stu-id="3d861-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="3d861-131">WBS (作業分解構造)</span><span class="sxs-lookup"><span data-stu-id="3d861-131">Work breakdown structure</span></span>

<span data-ttu-id="3d861-132">プロジェクトがコピーされると、ロードされたリソース WBS(作業分解構造) 全体がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3d861-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="3d861-133">名前付きリソースは汎用リソースによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3d861-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="3d861-134">名前付きリソースの作業時間が汎用リソースと同じでない場合、スケジュールが再計算され、タスクの期間が変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d861-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="3d861-135">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="3d861-135">Project team members</span></span>

<span data-ttu-id="3d861-136">プロジェクト チームがソース プロジェクトからコピーされると、汎用リソースがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3d861-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="3d861-137">汎用リソースの割り当ては、ソース プロジェクトと同様に維持されます。</span><span class="sxs-lookup"><span data-stu-id="3d861-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="3d861-138">名前付きリソースは、汎用チーム メンバーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="3d861-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="3d861-139">見積もり</span><span class="sxs-lookup"><span data-stu-id="3d861-139">Estimates</span></span>

<span data-ttu-id="3d861-140">プロジェクトがコピーされると、リソースおよび経費見積品目の両方がソース プロジェクトからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3d861-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="3d861-141">コピー プロジェクトにプログラムでアクセスする方法については、[コピー プロジェクトでプロジェクト テンプレートを開発する](dev-copy-project.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d861-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
