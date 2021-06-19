---
title: プロジェクトのコピー
description: このトピックでは、Dynamics 365 Project Operations のプロジェクトのコピーについて説明します。
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091260"
---
# <a name="copy-a-project"></a><span data-ttu-id="401f3-103">プロジェクトのコピー</span><span class="sxs-lookup"><span data-stu-id="401f3-103">Copy a project</span></span>

<span data-ttu-id="401f3-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="401f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="401f3-105">Dynamics 365 Project Operations では、**プロジェクト** フォームで **プロジェクトのコピー** を選択することで新しいプロジェクトをすばやく構築できます。</span><span class="sxs-lookup"><span data-stu-id="401f3-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="401f3-106">プロジェクトをコピーするには、コピーするプロジェクトを開き、**プロジェクトのコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="401f3-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="401f3-107">アクションは以下をコピーします:</span><span class="sxs-lookup"><span data-stu-id="401f3-107">The action will copy the following:</span></span>

- <span data-ttu-id="401f3-108">プロジェクト プロパティ</span><span class="sxs-lookup"><span data-stu-id="401f3-108">Project properties</span></span> 
- <span data-ttu-id="401f3-109">WBS (作業分解構造)</span><span class="sxs-lookup"><span data-stu-id="401f3-109">Work breakdown structure</span></span>
- <span data-ttu-id="401f3-110">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="401f3-110">Project team members</span></span>
- <span data-ttu-id="401f3-111">プロジェクト見積もり</span><span class="sxs-lookup"><span data-stu-id="401f3-111">Project estimates</span></span>
- <span data-ttu-id="401f3-112">プロジェクト経費の見積もり</span><span class="sxs-lookup"><span data-stu-id="401f3-112">Project expense estimates</span></span>
- <span data-ttu-id="401f3-113">プロジェクトの材料の見積もり</span><span class="sxs-lookup"><span data-stu-id="401f3-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="401f3-114">プロジェクト プロパティ</span><span class="sxs-lookup"><span data-stu-id="401f3-114">Project properties</span></span>

<span data-ttu-id="401f3-115">プロジェクトがコピーされると、次のフィールドの値がコピーされます:</span><span class="sxs-lookup"><span data-stu-id="401f3-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="401f3-116">件名</span><span class="sxs-lookup"><span data-stu-id="401f3-116">Name</span></span>
- <span data-ttu-id="401f3-117">内容</span><span class="sxs-lookup"><span data-stu-id="401f3-117">Description</span></span>
- <span data-ttu-id="401f3-118">顧客</span><span class="sxs-lookup"><span data-stu-id="401f3-118">Customer</span></span>
- <span data-ttu-id="401f3-119">カレンダー テンプレート</span><span class="sxs-lookup"><span data-stu-id="401f3-119">Calendar Template</span></span>
- <span data-ttu-id="401f3-120">通貨</span><span class="sxs-lookup"><span data-stu-id="401f3-120">Currency</span></span>
- <span data-ttu-id="401f3-121">契約単位</span><span class="sxs-lookup"><span data-stu-id="401f3-121">Contracting Unit</span></span>
- <span data-ttu-id="401f3-122">プロジェクト管理者</span><span class="sxs-lookup"><span data-stu-id="401f3-122">Project Manager</span></span>
- <span data-ttu-id="401f3-123">ステータス</span><span class="sxs-lookup"><span data-stu-id="401f3-123">Status</span></span>
- <span data-ttu-id="401f3-124">全体的なプロジェクトの状態</span><span class="sxs-lookup"><span data-stu-id="401f3-124">Overall Project Status</span></span>
- <span data-ttu-id="401f3-125">コメント</span><span class="sxs-lookup"><span data-stu-id="401f3-125">Comments</span></span>
- <span data-ttu-id="401f3-126">見積もり</span><span class="sxs-lookup"><span data-stu-id="401f3-126">Estimates</span></span>
- <span data-ttu-id="401f3-127">開始予定日: これは、プロジェクトがコピーから作成された日付です。</span><span class="sxs-lookup"><span data-stu-id="401f3-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="401f3-128">推定終了日: この日付は、コピーから作成された新しいプロジェクトの開始日に基づいて調整されます。</span><span class="sxs-lookup"><span data-stu-id="401f3-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="401f3-129">工数 (時間)</span><span class="sxs-lookup"><span data-stu-id="401f3-129">Effort (Hours)</span></span>
- <span data-ttu-id="401f3-130">労務コスト見積</span><span class="sxs-lookup"><span data-stu-id="401f3-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="401f3-131">経費見積</span><span class="sxs-lookup"><span data-stu-id="401f3-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="401f3-132">材料コスト見積</span><span class="sxs-lookup"><span data-stu-id="401f3-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="401f3-133">プロジェクトのコピーは時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="401f3-133">Copy project is a long running operation.</span></span> <span data-ttu-id="401f3-134">プロジェクト レコード、それらの関連属性、および多くの関連エンティティもコピーされます。</span><span class="sxs-lookup"><span data-stu-id="401f3-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="401f3-135">操作は長時間実行されるため、コピーが開始されると、コピー操作が完了するまで、ターゲット プロジェクト ページは編集用にロックされます。</span><span class="sxs-lookup"><span data-stu-id="401f3-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="401f3-136">WBS (作業分解構造)</span><span class="sxs-lookup"><span data-stu-id="401f3-136">Work breakdown structure</span></span>

<span data-ttu-id="401f3-137">プロジェクトがコピーされると、ロードされたリソース WBS(作業分解構造) 全体がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="401f3-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="401f3-138">名前付きリソースは汎用リソースによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="401f3-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="401f3-139">名前付きリソースの作業時間が汎用リソースと同じでない場合、スケジュールが再計算され、タスクの期間が変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="401f3-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="401f3-140">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="401f3-140">Project team members</span></span>

<span data-ttu-id="401f3-141">プロジェクト チームがソース プロジェクトからコピーされると、汎用リソースがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="401f3-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="401f3-142">汎用リソースの割り当ては、ソース プロジェクトと同様に維持されます。</span><span class="sxs-lookup"><span data-stu-id="401f3-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="401f3-143">名前付きリソースは、汎用チーム メンバーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="401f3-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="401f3-144">見積もり</span><span class="sxs-lookup"><span data-stu-id="401f3-144">Estimates</span></span>

<span data-ttu-id="401f3-145">プロジェクトがコピーされると、リソース、経費、材料の見積もり行がソース プロジェクトからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="401f3-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="401f3-146">コピー プロジェクトにプログラムでアクセスする方法については、[コピー プロジェクトでプロジェクト テンプレートを開発する](dev-copy-project.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="401f3-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
