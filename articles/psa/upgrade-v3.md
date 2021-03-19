---
title: アップグレードに関する考慮事項 - Microsoft Dynamics 365 Project Service Automation バージョン 2.x または 1.x からバージョン 3
description: このトピックでは、Project Service Automation の バージョン 2.x または 1.x から バージョン 3 へアップグレードする際に必要な考慮事項について説明します。
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ff0777705c6d0e2c0d8aa4ed191f4ae6b1786100
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281664"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a><span data-ttu-id="68bca-103">PSA バージョン 2.x または 1.x からバージョン 3.x へのアップグレードに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="68bca-103">Upgrade considerations - PSA version 2.x or 1.x to version 3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a><span data-ttu-id="68bca-104">Project Service Automation および Field Service</span><span class="sxs-lookup"><span data-stu-id="68bca-104">Project Service Automation and Field Service</span></span>
<span data-ttu-id="68bca-105">Dynamics 365 Project Service Automation と Dynamics 365 Field Service のどちらも、リソース スケジュールには Universal Resourcing Scheduling（URS）ソリューションを使用します。</span><span class="sxs-lookup"><span data-stu-id="68bca-105">Both Dynamics 365 Project Service Automation and Dynamics 365 Field Service use the Universal Resourcing Scheduling (URS) solution for resource scheduling.</span></span> <span data-ttu-id="68bca-106">インスタンスに Project Service Automation および Field Service がある場合、両方のソリューションを最新バージョンに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68bca-106">If you have Project Service Automation and Field Service in your instance, upgrade both solutions to the latest version.</span></span> <span data-ttu-id="68bca-107">Project Service Automation の場合は、バージョン 3.x です。</span><span class="sxs-lookup"><span data-stu-id="68bca-107">For Project Service Automation, that is version 3.x.</span></span> <span data-ttu-id="68bca-108">Field Service の場合、バージョン 8.x です。</span><span class="sxs-lookup"><span data-stu-id="68bca-108">For Field Service, it is version 8.x.</span></span> <span data-ttu-id="68bca-109">Project Service Automation または Field Serviceをアップグレードすると、最新バージョンの URS がインストールされます。</span><span class="sxs-lookup"><span data-stu-id="68bca-109">Upgrading Project Service Automation or Field Service will install the latest version of URS.</span></span> <span data-ttu-id="68bca-110">同じインスタンス内の Project Service Automation ソリューションと Field Service ソリューションの両方が最新バージョンにアップグレードされていない場合、動作に一貫性がない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="68bca-110">If both the Project Service Automation and Field Service solutions in the same instance aren’t upgraded to the latest version, there might be some inconsistent behavior.</span></span>

## <a name="resource-assignments"></a><span data-ttu-id="68bca-111">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="68bca-111">Resource assignments</span></span>
<span data-ttu-id="68bca-112">Project Service Automation の バージョン 2 およびバージョン 1 では、タスクの割り当ては子のタスク (または行タスクとも呼ばれます) として **タスク エンティティ** に保存され、**リソースの割り当て** エンティティと間接的に連動していました。</span><span class="sxs-lookup"><span data-stu-id="68bca-112">In Project Service Automation version 2 and version 1, task assignments were stored as child tasks (also called line tasks) in the **Task entity**, and indirectly related to the **Resource Assignment** entity.</span></span> <span data-ttu-id="68bca-113">行タスクは、作業分解構造 (WBS) の割り当てのポップアップ ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-113">The line task was visible in the assignment pop-up window on the Work Breakdown Structure (WBS).</span></span>

![Project Service Automation バージョン2 と バージョン1 における WBS 上の行タスク](media/upgrade-line-task-01.png)

<span data-ttu-id="68bca-115">Project Service Automation のバージョン 3 では、予約可能なリソースをタスクに割り当てる際に基礎となるスキーマが変更されています。</span><span class="sxs-lookup"><span data-stu-id="68bca-115">In version 3 of Project Service Automation, the underlying schema of assigning bookable resources to tasks has changed.</span></span> <span data-ttu-id="68bca-116">行タスクは非推奨となり、**タスク エンティティ** のタスクと **リソースの割り当て** エンティティのチーム メンバーとの間で 1 : 1 で直接関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="68bca-116">The line task has been deprecated and there is a direct 1:1 relationship between the task in the **Task entity** and the team member in the **Resource Assignment** entity.</span></span> <span data-ttu-id="68bca-117">プロジェクト チーム メンバーに対する割り当てタスクは、現在、リソース割り当てエンティティに直接保存されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="68bca-117">Tasks that are assigned to a project team member are now stored directly in the Resource Assignment entity.</span></span>  

<span data-ttu-id="68bca-118">これらの変更は既存のプロジェクトのアップグレードの際に影響を与えます。既存のプロジェクトは、プロジェクト チームに、名前付き予約可能リソースおよび汎用リソースを含みます。</span><span class="sxs-lookup"><span data-stu-id="68bca-118">These changes impact the upgrade of any existing projects that have resource assignments for named bookable resources and generic resources on a project team.</span></span> <span data-ttu-id="68bca-119">このトピックでは、バージョン 3 にアップグレードする場合、プロジェクトとして考慮する必要のある事柄について説明します。</span><span class="sxs-lookup"><span data-stu-id="68bca-119">This topic provides the considerations that you will need to take into account for your projects when you upgrade to version 3.</span></span> 

### <a name="tasks-assigned-to-named-resources"></a><span data-ttu-id="68bca-120">名前付きリソースに割り当てられたタスク</span><span class="sxs-lookup"><span data-stu-id="68bca-120">Tasks assigned to named resources</span></span>
<span data-ttu-id="68bca-121">基礎となるタスク エンティティ、バージョン 2 およびバージョン 1 のタスクを使用することによって、チーム メンバーは既定の定義済みロールではないロールを構築できました。</span><span class="sxs-lookup"><span data-stu-id="68bca-121">Using the underlying task entity, tasks in version 2 and version 1 allowed team members to portray a role other than their default defined role.</span></span> <span data-ttu-id="68bca-122">たとえば、既定でプログラム管理者のロールに割り当てられていた石田 美月を、開発者ロールを使用するタスクに割り当てることができました。</span><span class="sxs-lookup"><span data-stu-id="68bca-122">For example, Gracie George, who’s by default assigned the role of Program Manager, could be assigned to a task with the role of Developer.</span></span> <span data-ttu-id="68bca-123">バージョン 3 では、チーム メンバーという名前のロールは常に規定であり、石田 美月が割り当てられているどのタスクでも、美月の既定ロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="68bca-123">In version 3, the role of a named team member is always the default, so any task that Gracie George is assigned to uses Gracie's default role of Program Manager.</span></span>

<span data-ttu-id="68bca-124">バージョン 1 およびバージョン 2 で既定のロールではないタスクにリソースを割り当てていいた場合、アップグレードすると、名前付きリソースはバージョン 2 のロール割り当てに関わらずすべてのタスク割り当ての既定ロールに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="68bca-124">If you have assigned a resource to a task outside of their default role in version 2 and version 1, when you upgrade, the named resource will be assigned the default role for all task assignments, regardless of role assignment in version 2.</span></span> <span data-ttu-id="68bca-125">この割当により、バージョン 2 またはバージョン 1 からバージョン 3 まで、計算された見積に違いが生じますが、これは、見積がリソース ロールに基づいて計算されたものであり、行タスクの割り当てに基づいていないためです。</span><span class="sxs-lookup"><span data-stu-id="68bca-125">This assignment results in differences in the calculated estimates from version 2 or version 1 to version 3 because estimates are calculated based on the role of the resource and not the line task assignment.</span></span> <span data-ttu-id="68bca-126">たとえば、バージョン 2 では、2 つのタスクが藤戸 茜に割り当てられていました。</span><span class="sxs-lookup"><span data-stu-id="68bca-126">For example, in version 2, two tasks have been assigned to Ashley Chinn.</span></span> <span data-ttu-id="68bca-127">タスク 1 の場合、行タスクのロールは開発者であり、タスク 2 の場合、プログラム管理者です。</span><span class="sxs-lookup"><span data-stu-id="68bca-127">The role on the line task for task 1 is Developer and for task 2, Program Manager.</span></span> <span data-ttu-id="68bca-128">藤戸 茜には、プログラム管理者としての既定ロールもあります。</span><span class="sxs-lookup"><span data-stu-id="68bca-128">Ashley Chinn has the default role of Program Manager.</span></span>

![一つのリソースに割り当てられた複数のロール](media/upgrade-multiple-roles-02.png)

<span data-ttu-id="68bca-130">開発者およびプログラム管理者ロールが異なるため、コストと営業見積りは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="68bca-130">Because the roles of Developer and Program Manager differ, the cost and sales estimates are as follows:</span></span>

![リソース ロールのコスト見積り](media/upggrade-cost-estimates-03.png)

![リソース ロールの営業見積り](media/upgrade-sales-estimates-04.png)

<span data-ttu-id="68bca-133">バージョン 3 にアップグレードすると、行タスクは、予約可能なリソース チーム メンバーのタスクでリソース割り当てに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="68bca-133">When you upgrade to version 3, line tasks are replaced with resource assignments on the task of the bookable resource team member.</span></span> <span data-ttu-id="68bca-134">割り当てでは、予約可能リソースに対する既定ロールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-134">The assignment will use the default role of the bookable resource.</span></span> <span data-ttu-id="68bca-135">次のグラフィックで、藤戸 茜はプログラム管理者のロールを持っていますが、このリソースです。</span><span class="sxs-lookup"><span data-stu-id="68bca-135">In the following graphic, Ashley Chinn who has a role of Program Manager, is the resource.</span></span>

![リソース割り当て](media/resource-assignment-v2-05.png)

<span data-ttu-id="68bca-137">見積がリソースに対して既定のロールを持っているため、営業およびコスト見積りは変わる場合があります。</span><span class="sxs-lookup"><span data-stu-id="68bca-137">Because the estimates are based on the default role for the resource, the sales and cost estimates may change.</span></span> <span data-ttu-id="68bca-138">次のグラフィックでは、ロールが予約可能リソースの既定ロールから取得されるようになったため、**開発者** ロールは表示されません。</span><span class="sxs-lookup"><span data-stu-id="68bca-138">In the following graphic, you no longer see the **Developer** role as the role is now taken from the bookable resource’s default role.</span></span>

<span data-ttu-id="68bca-139">![規定ロールに対するコスト見積り](media/resource-assignment-cost-estimate-06.png)
![規定ロールに対する営業見積り](media/resource-assignment-sales-estimate-07.png)</span><span class="sxs-lookup"><span data-stu-id="68bca-139">![Cost estimates for default roles](media/resource-assignment-cost-estimate-06.png)
![Sales estimate for default roles](media/resource-assignment-sales-estimate-07.png)</span></span>

<span data-ttu-id="68bca-140">アップグレード完了後は、チーム メンバー ロールを既定の割り当てのでないものに編集できます。</span><span class="sxs-lookup"><span data-stu-id="68bca-140">After upgrade is complete, you can edit a team member's role to be something other than the assigned default.</span></span> <span data-ttu-id="68bca-141">ただし、チーム メンバーのロールを変更すると、割り当てられたタスクすべてが変更されます。理由は、チーム メンバーがバージョン 3 で複数のロールを割り当てることができないためです。</span><span class="sxs-lookup"><span data-stu-id="68bca-141">However, if you change a team members role, it will be changed on all of their assigned tasks because team members can't be assigned multiple roles in version 3.</span></span>

![リソース ロールの更新](media/resource-role-assignment-08.png)

<span data-ttu-id="68bca-143">これは、リソースの組織単位を既定から別の組織単位に変更する際に名前付きリソースに割り当てた行タスクにも該当します。</span><span class="sxs-lookup"><span data-stu-id="68bca-143">This is also true for line tasks that were assigned to named resources when you change the resource’s organization unit from the default to another organization unit.</span></span> <span data-ttu-id="68bca-144">バージョン 3 のアップグレードの完了後、割り当てには、行タスクに設定済みのものではなく、リソース既定の組織単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-144">After the version 3 upgrade is complete, the assignment will use the resource’s default organization unit instead of the one set on the line task.</span></span>

### <a name="tasks-assigned-to-generic-resources"></a><span data-ttu-id="68bca-145">汎用リソースに割り当てられたタスク</span><span class="sxs-lookup"><span data-stu-id="68bca-145">Tasks assigned to generic resources</span></span>
<span data-ttu-id="68bca-146">バージョン 2 およびバージョン 1 では、タスクにロールや組織単位を設定して、**チームの生成** 機能を使用して、タスクに設定されている属性を持つ汎用リソースを生成できます。</span><span class="sxs-lookup"><span data-stu-id="68bca-146">In version 2 and version 1, you can set the role and org unit on a task and then use the **Generate team** feature to generate generic resources based on the attributes set on the task.</span></span> <span data-ttu-id="68bca-147">バージョン 3では、ロールや組織単位に汎用チーム メンバーを作成し、チーム メンバーにタスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="68bca-147">In version 3, you create the generic team members with role and org unit, and then assign the team members to tasks.</span></span>

<span data-ttu-id="68bca-148">バージョン 2 およびバージョン 1 では、汎用リソースを含むプロジェクトは二つに別れた状態か、またはタスクレベルで両者が融合した状態になっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="68bca-148">In version 2 and version 1, projects with generic resources can be in two states, or a mix of both at the task level.</span></span> <span data-ttu-id="68bca-149">たとえば、次のシナリオを使用できます。</span><span class="sxs-lookup"><span data-stu-id="68bca-149">For example, you can have the following scenarios:</span></span>

- <span data-ttu-id="68bca-150">ロールや組織単位を含むタスクは設定したが、関連リソースの割り当てを生成していなかった。</span><span class="sxs-lookup"><span data-stu-id="68bca-150">Tasks with roles and org units set, but no affiliated resource assignment has been generated.</span></span>
- <span data-ttu-id="68bca-151">**チームの生成** 機能を使用して汎用リソースを作成して、割り当て済みの汎用チーム メンバーのリソースを含むタスク。</span><span class="sxs-lookup"><span data-stu-id="68bca-151">Tasks with generic team member resource assignments that were assigned by creating generic resource using the **Generate team** feature.</span></span>

<span data-ttu-id="68bca-152">アップグレードを開始する前には、汎用リソースに割り当てられたタスクを含んでいる各プロジェクトか、または含んでいるがまだそこで実行するチーム プロセスを含まない各プロジェクトごとに、チームを再生成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="68bca-152">Before you begin your upgrade, we recommend that you regenerate the team for each project that has tasks assigned to generic resources or has yet to have the generate team process run on them.</span></span>

<span data-ttu-id="68bca-153">**チームの生成** を使用して生成された汎用チーム メンバーに割り当てられたタスクの場合、アップグレードでは汎用リソースがチームに置かれ、また割り当てがその汎用チーム メンバーに置かれます。</span><span class="sxs-lookup"><span data-stu-id="68bca-153">For tasks that are assigned to generic team members that were generated with **Generate Team**, the upgrade will leave the generic resource on the team and leave the assignment to that generic team member.</span></span> <span data-ttu-id="68bca-154">アップグレード後に汎用チーム メンバーに関するリソース要件を生成することをお勧めします。ただし、それはリソース要求を予約するか送信する前にしてください。</span><span class="sxs-lookup"><span data-stu-id="68bca-154">We recommend that you generate the resource requirement for the generic team member after the upgrade but before you book or submit a resource request.</span></span> <span data-ttu-id="68bca-155">これにより、プロジェクトの契約組織ユニットとは異なる汎用チーム メンバーの組織ユニットの割り当てを保持できます。</span><span class="sxs-lookup"><span data-stu-id="68bca-155">This will preserve any org unit assignments on the generic team members that are different than the project’s contracting org unit.</span></span>

<span data-ttu-id="68bca-156">たとえば、「プロジェクト Z」 プロジェクトでは、契約組織単位は、「Contoso US」 となります。</span><span class="sxs-lookup"><span data-stu-id="68bca-156">For example, in the Project Z project, the contracting org unit is Contoso US.</span></span> <span data-ttu-id="68bca-157">プロジェクト プランの実装段階内のテスト タスクでは、技術コンサルタントにロールが割り当てられていました。割り当てられた組織単位は、Contoso India です。</span><span class="sxs-lookup"><span data-stu-id="68bca-157">In the project plan, testing tasks within the Implementation phase have been assigned the role Technical Consultant and the assigned org unit is Contoso India.</span></span>

![実装段階の組織割り当て](media/org-unit-assignment-09.png)

<span data-ttu-id="68bca-159">実装段階の後、統合テスト タスクは、ロールの技術コンサルタントに割り当てられますが、組織は、「Contoso US」 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-159">After the implementation phase, the integration test task is assigned to the role Technical consultant, but the org is set to Contoso US.</span></span>  

![統合テスト タスク組織の割り当て](media/org-unit-generate-team-10.png)

<span data-ttu-id="68bca-161">プロジェクトのチームが生成されると、2 名の汎用チーム メンバーが、タスクで異なる組織単位に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-161">When you generate a team for the project, two generic team members are created due to the different org units on the tasks.</span></span> <span data-ttu-id="68bca-162">技術コンサルタント 1 は、Contoso India に割り当てられます。また、技術コンサルタント 2 は、Contoso US を有します。</span><span class="sxs-lookup"><span data-stu-id="68bca-162">Technical consultant 1 will be assigned the Contoso India tasks and Technical consultant 2 will have the Contoso US tasks.</span></span>  

![汎用チーム メンバーの生成](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> <span data-ttu-id="68bca-164">Project Service Automation のバージョン 2 と バージョン 1 では、チーム メンバーが組織単位を保持しておらず、組織単位は行タスクで保持されています。</span><span class="sxs-lookup"><span data-stu-id="68bca-164">In Project Service Automation version 2 and version 1, the team member does not hold the organization unit, that is maintained on the line task.</span></span>

![Project Service Automation バージョン2 と バージョン1 の行タスク](media/line-tasks-12.png)

<span data-ttu-id="68bca-166">見積もりビューの組織単位を表示できます。</span><span class="sxs-lookup"><span data-stu-id="68bca-166">You can see the organization unit on the estimates view.</span></span> 

![組織単位の予測](media/org-unit-estimates-view-13.png)
 
<span data-ttu-id="68bca-168">アップグレードが完了したら、汎用チーム メンバーに対応する行タスクの組織単位は汎用チーム メンバーに追加され、その行タスクは削除されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-168">When the upgrade is complete, the organization unit on the line task that corresponds to the generic team member is added to the generic team member and the line task is removed.</span></span> <span data-ttu-id="68bca-169">これにより、アップグレードの前に、汎用リソースを含む各プロジェクト チームを生成または再生成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="68bca-169">Because of this, we recommend that before you upgrade, you generate or regenerate the team on each project that contains generic resources.</span></span>

<span data-ttu-id="68bca-170">契約プロジェクトの組織単位と異なる組織単位、およびまだ生成されていないチームにロールを割り当てるタスクの場合は、アップグレードによってロールに対する汎用チーム メンバーを作成できますが、チーム メンバーの組織単位の場合はプロジェクトの契約単位を使用します。</span><span class="sxs-lookup"><span data-stu-id="68bca-170">For tasks that are assigned to a role with an org unit that differs from the org unit of the contracting project, and a team has not been generated, upgrade will create a generic team member for the role, but will use the contracting unit of the project for the team member's org unit.</span></span> <span data-ttu-id="68bca-171">「プロジェクト Z」 の例を再び見てみると、これは契約組織単位 「Contoso US」、および実装段階のプロジェクト プランのテスト タスクは、Contoso India に割り当てられている組織単位を使用する技術コンサルタントにロールが割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="68bca-171">Referring back to the example with Project Z, the contracting org unit Contoso US, and the project plan testing tasks within the Implementation phase have been assigned the role Technical Consultant with the org unit assigned to Contoso India.</span></span> <span data-ttu-id="68bca-172">実装段階後に完了した統合テスト タスクは、ロールの技術コンサルタントに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="68bca-172">The Integration test task that is completed after the Implementation phase has been assigned to the role Technical consultant.</span></span> <span data-ttu-id="68bca-173">組織単位は 「Contoso US」 で、チームは生成されていません。</span><span class="sxs-lookup"><span data-stu-id="68bca-173">The org unit is Contoso US and a team has not been generated.</span></span> <span data-ttu-id="68bca-174">アップグレードによって、1 つの汎用チーム メンバーが作成され、3 つのすべてのタスクに対して割り当て時間を持つ技術コンサルタント、およびプロジェクトの契約組織単位である Contoso US の組織単位が生成されます。</span><span class="sxs-lookup"><span data-stu-id="68bca-174">Upgrade will create one generic team member, a Technical consultant that has the assigned hours of all three tasks, and an org unit of Contoso US, the project’s contracting org unit.</span></span>   
 
<span data-ttu-id="68bca-175">生成されていないチーム メンバーについて、異なるリソース組織単位の既定を変更する理由は、汎用リソースを含む各プロジェクトで、アップグレード前にチームを生成または再生成し、組織単位割り当てが失われないようにするためで、Microsoft がお勧めしています。</span><span class="sxs-lookup"><span data-stu-id="68bca-175">Changing the default of the different resourcing org units on ungenerated team members is the reason we recommend that you generate or regenerate the team on each project that contains generic resources prior to the upgrade so that the org unit assignments are not lost.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]