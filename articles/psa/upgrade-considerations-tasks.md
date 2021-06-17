---
title: WBS (作業分解構造) のアップグレードに関する考慮事項
description: このトピックでは、「Project Service Automation 2.x から 3.x. へ」 の WBS (作業分解構造) をアップグレードする方法に関して説明します。
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005617"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="47650-103">WBS (作業分解構造) のアップグレードに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="47650-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="47650-104">このトピックでは、「Project Service Automation 2.x から 3.x. へ」 の WBS (作業分解構造) をアップグレードする方法に関して説明します。</span><span class="sxs-lookup"><span data-stu-id="47650-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="47650-105">このトピックでは、アップグレードを完了するのに必要な Project Service Automation (PSA) のプロジェクトについて、正常な条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="47650-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="47650-106">ここには、アップグレードが失敗する一般的なブロック条件についての詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="47650-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="47650-107">プロジェクト スケジュールのプロジェクト タスクおよび機能の定義に関する詳細は、[プロジェクト スケジュール](project-creating.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47650-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="47650-108">主要なエンティティ</span><span class="sxs-lookup"><span data-stu-id="47650-108">Key entities</span></span>
<span data-ttu-id="47650-109">リソースでロードされている正確な WBS (作業分解構造) に関して、次のエンティティが必要です。</span><span class="sxs-lookup"><span data-stu-id="47650-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="47650-110">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="47650-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="47650-111">プロジェクト チーム</span><span class="sxs-lookup"><span data-stu-id="47650-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="47650-112">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="47650-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="47650-113">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="47650-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="47650-114">プロジェクト タスクの依存関係</span><span class="sxs-lookup"><span data-stu-id="47650-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="47650-115">予約可能リソース</span><span class="sxs-lookup"><span data-stu-id="47650-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="47650-116">WBS (作業分解構造) がロードされたリソースを定義するには、次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="47650-117">新しいプロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="47650-117">Create a new project.</span></span> <span data-ttu-id="47650-118">新規プロジェクトの作成方法については、[msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47650-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="47650-119">1 つ以上のタスクを作成する。</span><span class="sxs-lookup"><span data-stu-id="47650-119">Create one or more tasks.</span></span> <span data-ttu-id="47650-120">タスクの作成方法については、[msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47650-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="47650-121">タスクの依存関係を定義します。</span><span class="sxs-lookup"><span data-stu-id="47650-121">Define the task dependencies.</span></span> <span data-ttu-id="47650-122">詳細については、 [プロジェクト タスクの依存関係](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47650-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="47650-123">プロジェクト チーム メンバーをプロジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="47650-123">Assign project team members to the project.</span></span> <span data-ttu-id="47650-124">詳細については、[msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47650-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="47650-125">プロジェクト チーム メンバーをタスクに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="47650-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="47650-126">詳細については、 [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47650-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="47650-127">プロジェクト チームの関連付け</span><span class="sxs-lookup"><span data-stu-id="47650-127">Project team relationships</span></span>

<span data-ttu-id="47650-128">アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:</span><span class="sxs-lookup"><span data-stu-id="47650-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="47650-129">すべてのプロジェクト チームのメンバーを、予約可能リソースに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="47650-130">すべてのプロジェクト チームのメンバーを、同一のプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="47650-131">プロジェクト タスクの関連付け</span><span class="sxs-lookup"><span data-stu-id="47650-131">Project task relationships</span></span>
<span data-ttu-id="47650-132">アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:</span><span class="sxs-lookup"><span data-stu-id="47650-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="47650-133">関連するタスクはすべて、同一のプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="47650-134">すべての行タスク対して親タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="47650-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="47650-135">すべてのタスクに対して親プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="47650-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="47650-136">有効な条件</span><span class="sxs-lookup"><span data-stu-id="47650-136">Valid conditions</span></span>

- <span data-ttu-id="47650-137">すべてのタスクの期間は、1 時間以上、1,800,000 分未満 (1,250 日) である必要があります。\*</span><span class="sxs-lookup"><span data-stu-id="47650-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="47650-138">すべてのタスクは、開始日を 2000/01/01 より後に設定されている必要があります。\*</span><span class="sxs-lookup"><span data-stu-id="47650-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="47650-139">すべてのタスクは、現在の日付の 18 年以上前である必要があります。\*</span><span class="sxs-lookup"><span data-stu-id="47650-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="47650-140">すべてのタスクは、完了日かそれよりも前に開始日を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="47650-141">分類上のすべてのトランザクションの種類 (経費、資料、税、および時間) には、**既定の単位** および **出荷単位** の値が必要です。</span><span class="sxs-lookup"><span data-stu-id="47650-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="47650-142">日付の書式に文字を使用することは避けてください。</span><span class="sxs-lookup"><span data-stu-id="47650-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="47650-143">潜在的緩和措置</span><span class="sxs-lookup"><span data-stu-id="47650-143">Potential mitigation steps</span></span>
- <span data-ttu-id="47650-144">詳細検索を使用して、プロジェクトIDを含んでいないプロジェクト タスクを識別します。</span><span class="sxs-lookup"><span data-stu-id="47650-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="47650-145">高度な検索を使用して、スケジュールされた期間が > 1,800,000 よりも大きいプロジェクト タスクを識別します。</span><span class="sxs-lookup"><span data-stu-id="47650-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="47650-146">データを変更する前に、データが不良な状態となった原因として考えられるエンティティに関連付けられている カスタマイズ を調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="47650-147">これらのカスタマイズは、データに関連する更新を進める前に対処する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="47650-148">孤立状態であると識別されたタスクについては、当該タスクが不要な場合、あるいは適切な親プロジェクトに関連付ける必要がある場合は、削除することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="47650-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="47650-149">期間が 1,250日 を超えるタスクについては、可能であれば、合計期間を表す複数のタスクを追加することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="47650-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="47650-150">アスタリスク (\*) が付いている項目には制限がありますが、これは顧客リレーションシップ マネジメント (CRM) が 7,320 回の繰り返し拡張機能のみに対応しているためです。</span><span class="sxs-lookup"><span data-stu-id="47650-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="47650-151">ユーザーはこの制限を受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="47650-152">リソース割り当ての関連付け</span><span class="sxs-lookup"><span data-stu-id="47650-152">Resource Assignment relationships</span></span>
<span data-ttu-id="47650-153">アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:</span><span class="sxs-lookup"><span data-stu-id="47650-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="47650-154">作業分解構造 でのすべてのリソースの割り当ては、同一のプロジェクトに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="47650-155">作業分解構造のすべてのリソースの割り当ては、同一のプロジェクトのプロジェクト チーム メンバーに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="47650-156">潜在的緩和措置</span><span class="sxs-lookup"><span data-stu-id="47650-156">Potential mitigation steps</span></span>
- <span data-ttu-id="47650-157">上記の条件に当てはまらないすべてのタスクを特定します。</span><span class="sxs-lookup"><span data-stu-id="47650-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="47650-158">既に有効ではないリソースの割り当てはすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="47650-159">プロジェクト タスク依存関係の関連付け</span><span class="sxs-lookup"><span data-stu-id="47650-159">Project task dependency relationships</span></span>
<span data-ttu-id="47650-160">アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:</span><span class="sxs-lookup"><span data-stu-id="47650-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="47650-161">すべてのプロジェクト タスクの依存関係は、同一のプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="47650-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="47650-162">タスクでは、参照済みの同一の依存関係を複数回使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="47650-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]