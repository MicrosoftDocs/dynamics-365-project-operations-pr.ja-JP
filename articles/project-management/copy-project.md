---
title: プロジェクトのコピー
description: このトピックでは、Dynamics 365 Project Operations でのプロジェクトのコピーについて説明します。
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079209"
---
# <a name="copy-a-project"></a><span data-ttu-id="d029d-103">プロジェクトのコピー</span><span class="sxs-lookup"><span data-stu-id="d029d-103">Copy a project</span></span>

<span data-ttu-id="d029d-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d029d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d029d-105">Dynamics 365 Project Operations を使用すると、 **プロジェクト** フォームの **プロジェクトのコピー** を選択して新しいプロジェクトをすばやく構築できます。</span><span class="sxs-lookup"><span data-stu-id="d029d-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="d029d-106">プロジェクトをコピーするには、コピーするプロジェクトを開き、 **プロジェクトのコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d029d-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="d029d-107">操作は以下をコピーします:</span><span class="sxs-lookup"><span data-stu-id="d029d-107">The action will copy:</span></span>

- <span data-ttu-id="d029d-108">プロジェクト プロパティ</span><span class="sxs-lookup"><span data-stu-id="d029d-108">Project properties</span></span>
- <span data-ttu-id="d029d-109">WBS(作業分解構造)</span><span class="sxs-lookup"><span data-stu-id="d029d-109">The Work breakdown structure</span></span>
- <span data-ttu-id="d029d-110">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="d029d-110">Project team members</span></span>
- <span data-ttu-id="d029d-111">プロジェクト見積もり</span><span class="sxs-lookup"><span data-stu-id="d029d-111">Project estimates</span></span>
- <span data-ttu-id="d029d-112">プロジェクト経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="d029d-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="d029d-113">プロジェクト プロパティ</span><span class="sxs-lookup"><span data-stu-id="d029d-113">Project properties</span></span>

<span data-ttu-id="d029d-114">プロジェクトがコピーされると、次のフィールドの値がコピーされます:</span><span class="sxs-lookup"><span data-stu-id="d029d-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="d029d-115">件名</span><span class="sxs-lookup"><span data-stu-id="d029d-115">Name</span></span>
- <span data-ttu-id="d029d-116">内容</span><span class="sxs-lookup"><span data-stu-id="d029d-116">Description</span></span>
- <span data-ttu-id="d029d-117">顧客</span><span class="sxs-lookup"><span data-stu-id="d029d-117">Customer</span></span>
- <span data-ttu-id="d029d-118">カレンダー テンプレート</span><span class="sxs-lookup"><span data-stu-id="d029d-118">Calendar Template</span></span>
- <span data-ttu-id="d029d-119">通貨</span><span class="sxs-lookup"><span data-stu-id="d029d-119">Currency</span></span>
- <span data-ttu-id="d029d-120">契約単位</span><span class="sxs-lookup"><span data-stu-id="d029d-120">Contracting Unit</span></span>
- <span data-ttu-id="d029d-121">プロジェクト管理者</span><span class="sxs-lookup"><span data-stu-id="d029d-121">Project Manager</span></span>
- <span data-ttu-id="d029d-122">ステータス</span><span class="sxs-lookup"><span data-stu-id="d029d-122">Status</span></span>
- <span data-ttu-id="d029d-123">全体的なプロジェクトの状態</span><span class="sxs-lookup"><span data-stu-id="d029d-123">Overall Project Status</span></span>
- <span data-ttu-id="d029d-124">コメント</span><span class="sxs-lookup"><span data-stu-id="d029d-124">Comments</span></span>
- <span data-ttu-id="d029d-125">見積もり</span><span class="sxs-lookup"><span data-stu-id="d029d-125">Estimates</span></span>
- <span data-ttu-id="d029d-126">開始予定日</span><span class="sxs-lookup"><span data-stu-id="d029d-126">Estimated Start Date</span></span>
- <span data-ttu-id="d029d-127">終了日</span><span class="sxs-lookup"><span data-stu-id="d029d-127">Finish Date</span></span>
- <span data-ttu-id="d029d-128">工数 (時間)</span><span class="sxs-lookup"><span data-stu-id="d029d-128">Effort (Hours)</span></span>
- <span data-ttu-id="d029d-129">見積もり労務コスト</span><span class="sxs-lookup"><span data-stu-id="d029d-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="d029d-130">見積もり経費</span><span class="sxs-lookup"><span data-stu-id="d029d-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="d029d-131">WBS (作業分解構造)</span><span class="sxs-lookup"><span data-stu-id="d029d-131">Work breakdown structure</span></span>

<span data-ttu-id="d029d-132">プロジェクトがコピーされると、ロードされたリソース WBS(作業分解構造) 全体がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d029d-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="d029d-133">名前付きリソースは汎用リソースによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d029d-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="d029d-134">名前付きリソースの作業時間が汎用リソースと同じでない場合、スケジュールが再計算され、タスクの期間が変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d029d-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="d029d-135">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="d029d-135">Project team members</span></span>

<span data-ttu-id="d029d-136">プロジェクト チームがソース プロジェクトからコピーされると、汎用リソースがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d029d-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="d029d-137">汎用リソースの割り当ては、ソース プロジェクトと同様に維持されます。</span><span class="sxs-lookup"><span data-stu-id="d029d-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="d029d-138">名前付きリソースは、汎用チーム メンバーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="d029d-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="d029d-139">見積もり</span><span class="sxs-lookup"><span data-stu-id="d029d-139">Estimates</span></span>

<span data-ttu-id="d029d-140">プロジェクトがコピーされると、リソースおよび経費見積品目の両方がソース プロジェクトからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d029d-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="d029d-141">コピー プロジェクトにプログラムでアクセスする方法については、[コピー プロジェクトでプロジェクト テンプレートを開発する](dev-copy-project.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d029d-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
