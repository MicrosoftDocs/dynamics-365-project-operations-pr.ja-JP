---
title: スケジュール モード
description: このトピックでは、スケジュール モードについて説明します。
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981441"
---
# <a name="scheduling-modes"></a><span data-ttu-id="4d208-103">スケジュール モード</span><span class="sxs-lookup"><span data-stu-id="4d208-103">Scheduling modes</span></span>

<span data-ttu-id="4d208-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="4d208-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4d208-105">Dynamics 365 Project Operationsは、WBS (作業分解構造) 内のタスクにおける重要な変数の変更をどのように管理するかを組織が定義する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d208-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="4d208-106">プロジェクト マネージャーは、組織の特定のニーズに基づいて、プロジェクトの作成時にスケジュール モードを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="4d208-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="4d208-107">Project Operations で使用できるスケジュール モードは 3 つあります:</span><span class="sxs-lookup"><span data-stu-id="4d208-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="4d208-108">固定期間 (これが既定のモードです)</span><span class="sxs-lookup"><span data-stu-id="4d208-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="4d208-109">固定作業</span><span class="sxs-lookup"><span data-stu-id="4d208-109">Fixed work</span></span>
  - <span data-ttu-id="4d208-110">固定単位</span><span class="sxs-lookup"><span data-stu-id="4d208-110">Fixed units</span></span>

<span data-ttu-id="4d208-111">特定のスケジュール モードの定義によって影響を受ける値は、次の式によって決定されます:</span><span class="sxs-lookup"><span data-stu-id="4d208-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="4d208-112">労力 (*作業*) = 期間 x 単位</span><span class="sxs-lookup"><span data-stu-id="4d208-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="4d208-113">プロジェクトのスケジュール モードを定義する際は、これらの値の 1 つを設定しているため、変更できません。</span><span class="sxs-lookup"><span data-stu-id="4d208-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="4d208-114">この値を一定に保つことで、その値に優先順位をつけ、他の 2 つの値が変化しても変更しないようにシステムに通知します。</span><span class="sxs-lookup"><span data-stu-id="4d208-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="4d208-115">以下の表は、特定のモードを選択した場合の影響についての情報です。</span><span class="sxs-lookup"><span data-stu-id="4d208-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="4d208-116">**このタスク**</span><span class="sxs-lookup"><span data-stu-id="4d208-116">**In this task**</span></span>             | <span data-ttu-id="4d208-117">**単位を修正する場合**</span><span class="sxs-lookup"><span data-stu-id="4d208-117">**If you revise units**</span></span>   | <span data-ttu-id="4d208-118">**期間を修正する場合**</span><span class="sxs-lookup"><span data-stu-id="4d208-118">**If you revise duration**</span></span> | <span data-ttu-id="4d208-119">**労力を修正する場合**</span><span class="sxs-lookup"><span data-stu-id="4d208-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="4d208-120">固定された単位のタスク</span><span class="sxs-lookup"><span data-stu-id="4d208-120">Fixed units task</span></span>     | <span data-ttu-id="4d208-121">期間が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-121">Duration is recalculated.</span></span> | <span data-ttu-id="4d208-122">労力が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-122">Effort is recalculated.</span></span>    | <span data-ttu-id="4d208-123">期間が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="4d208-124">固定工数タスク</span><span class="sxs-lookup"><span data-stu-id="4d208-124">Fixed effort task</span></span>    | <span data-ttu-id="4d208-125">期間が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-125">Duration is recalculated.</span></span> | <span data-ttu-id="4d208-126">単位が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-126">Units are recalculated.</span></span>    | <span data-ttu-id="4d208-127">期間が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="4d208-128">固定期間タスク</span><span class="sxs-lookup"><span data-stu-id="4d208-128">Fixed duration task</span></span>  | <span data-ttu-id="4d208-129">労力が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-129">Effort is recalculated.</span></span>   | <span data-ttu-id="4d208-130">労力が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-130">Effort is recalculated.</span></span>    | <span data-ttu-id="4d208-131">単位が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-131">Units are recalculated.</span></span>   |

<span data-ttu-id="4d208-132">特定のモードの影響の詳細については、[より正確なスケジュールのためにタスク タイプを変更します](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d208-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="4d208-133">トピックでは、**作業** の代わりに **工数** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d208-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="4d208-134">組織のスケジュール モードを変更する</span><span class="sxs-lookup"><span data-stu-id="4d208-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="4d208-135">組織のスケジュール モードを定義するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4d208-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="4d208-136">**設定** \> **一般** \> **パラメーター** に移動し、プロジェクト パラメータを選択します。</span><span class="sxs-lookup"><span data-stu-id="4d208-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="4d208-137">**プロジェクト パラメーター** ページで、組織の既定のスケジュール モードを選択し、プロジェクト マネージャーが新しいプロジェクトを作成する際に設定を上書きする機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="4d208-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="4d208-138">プロジェクトのスケジュール モードの設定を変更する</span><span class="sxs-lookup"><span data-stu-id="4d208-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="4d208-139">組織がプロジェクトマネージャーに既定のスケジュール モードの変更を許可している場合、プロジェクト マネージャーは新しいプロジェクトを作成する際にその変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4d208-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="4d208-140">ただし、プロジェクトの保存後は、スケジュール モードを変更できません。</span><span class="sxs-lookup"><span data-stu-id="4d208-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="4d208-141">コピーされたプロジェクト</span><span class="sxs-lookup"><span data-stu-id="4d208-141">Copied projects</span></span>

<span data-ttu-id="4d208-142">プロジェクトのコピー アクションが実行されるとプロジェクトが作成されるため、プロジェクト マネージャーはスケジュール モードを設定できません。</span><span class="sxs-lookup"><span data-stu-id="4d208-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="4d208-143">宛先のプロジェクトでは、常に組織レベルで定義されたモードが既定となります。</span><span class="sxs-lookup"><span data-stu-id="4d208-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="4d208-144">コピーされたタスク</span><span class="sxs-lookup"><span data-stu-id="4d208-144">Copied tasks</span></span>

<span data-ttu-id="4d208-145">タスクをあるプロジェクトから別のプロジェクトにコピーすると、そのタスクはコピー先のプロジェクトのスケジュール モードを継承します。</span><span class="sxs-lookup"><span data-stu-id="4d208-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
