---
title: プロジェクト テンプレート
description: このトピックは、すばやくプロジェクト設定をするためにプロジェクト テンプレートを使用する方法につい説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998282"
---
# <a name="project-templates"></a><span data-ttu-id="45a6f-103">プロジェクト テンプレート</span><span class="sxs-lookup"><span data-stu-id="45a6f-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="45a6f-104">プロジェクト テンプレートはプロジェクトをすばやく簡単に開始するのに役立つ、あらかじめ定義されたフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="45a6f-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="45a6f-105">1 回クリックするだけで、あらかじめ定義されたテンプレートを使用して新しいプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="45a6f-106">プロジェクトについては、プロジェクト テンプレートの前提条件を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="45a6f-107">各プロジェクトでカレンダーを定義し、ロールと価格表も組織であらかじめ定義する必要があります。これにより、テンプレートのコンポーネントにも有用なデータが存在するようになります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="45a6f-108">一つのプロジェクト テンプレートは、スケジュール、プロジェクト見積もり、およびプロジェクト チーム メンバーの 3 つのコンポーネントから構成されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="45a6f-109">Schedule</span><span class="sxs-lookup"><span data-stu-id="45a6f-109">Schedule</span></span>

<span data-ttu-id="45a6f-110">プロジェクト テンプレートのスケジュールには、プロジェクト内のスケジュールと同じ要素のセットがあります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="45a6f-111">タスク階層の作成、タスクへのロールの関連付け、スケジュール属性の定義、依存関係の設定ができます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="45a6f-112">プロジェクト テンプレートのスケジュールは、各タスクのタスク モードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="45a6f-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="45a6f-113">したがって、スケジュール エンジンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="45a6f-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="45a6f-114">プロジェクトとプロジェクト カレンダーを関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="45a6f-115">作業スケジュールを作成する場合は、プロジェクト テンプレートとプロジェクトに違いはありません。</span><span class="sxs-lookup"><span data-stu-id="45a6f-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="45a6f-116">プロジェクト見積もり</span><span class="sxs-lookup"><span data-stu-id="45a6f-116">Project estimates</span></span>

<span data-ttu-id="45a6f-117">プロジェクト テンプレートのプロジェクト見積りは、プロジェクトのプロジェクト見積もりと同様に機能します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="45a6f-118">ただし、パラメーターで定義された規定の原価と販売価格からコストと販売価格表を引きだされます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="45a6f-119">テンプレートからのプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="45a6f-119">Creating a project from a template</span></span>
 
<span data-ttu-id="45a6f-120">プロジェクト テンプレートからプロジェクトを作成する方法は次の通りいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="45a6f-121">見積もりからプロジェクトを作成した場合は、**簡易作成 : プロジェクト** のダイアログボックス内でプロジェクト テンプレートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![簡易作成: プロジェクト ダイアログ ボックス](media/project-11.png)

- <span data-ttu-id="45a6f-123">**新規プロジェクト** を選択してプロジェクトを作成する場合、**プロジェクト** ページは、レコードが保存される前に表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="45a6f-124">**テンプレートの選択** フィールドで、組織内の慈善定義済みプロジェクト テンプレートの一つを選択します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="45a6f-125">**テンプレート エンティティ** ページで、**テンプレートからプロジェクトを作成** を使用します。</span><span class="sxs-lookup"><span data-stu-id="45a6f-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="45a6f-126">テンプレートのコンポーネントをプロジェクトへコピーする</span><span class="sxs-lookup"><span data-stu-id="45a6f-126">Copying components of template to project</span></span>

<span data-ttu-id="45a6f-127">プロジェクトにプロジェクト テンプレートのコンポーネントをコピーする場合は、プロジェクトの設定に応じて、上書きがいくつか発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="45a6f-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="45a6f-128">スケジュールのコピー</span><span class="sxs-lookup"><span data-stu-id="45a6f-128">Copying the schedule</span></span>

<span data-ttu-id="45a6f-129">プロジェクト テンプレートからコピーする場合、プロジェクトがテンプレートと異なるプロジェクト カレンダーを持つ場合、プロジェクトのカレンダーからの作業時間がタスク スケジュールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="45a6f-130">これにより、スケジュールはバッキング プロジェクト カレンダーと一致するように調整されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="45a6f-131">同様に、スケジュール上の最初のタスクがプロジェクトの開始日を取り、残りの階層のスケジュールも、テンプレートで指定されている期間と依存関係に基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="45a6f-132">プロジェクト見積もりのコピー</span><span class="sxs-lookup"><span data-stu-id="45a6f-132">Copying project estimates</span></span> 

<span data-ttu-id="45a6f-133">プロジェクト見積もり明細行全体にコピーする場合、価格表が更新されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="45a6f-134">コスト価格表については、更新はプロジェクトの所有ユニットに基づいています。</span><span class="sxs-lookup"><span data-stu-id="45a6f-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="45a6f-135">販売価格表については、顧客に基づいています。</span><span class="sxs-lookup"><span data-stu-id="45a6f-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="45a6f-136">営業エンティティに関連付けられているプロジェクトについては、単位コストと販売価格はこれらの価格表に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="45a6f-137">プロジェクト チームのコピー</span><span class="sxs-lookup"><span data-stu-id="45a6f-137">Copying a project team</span></span>

<span data-ttu-id="45a6f-138">プロジェクト テンプレートからプロジェクト チームをコピーする場合、汎用リソースはテンプレートで定義されているスキルおよび能力と共にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="45a6f-139">汎用リソースの割り当ては、プロジェクト テンプレートと同様に維持されます。</span><span class="sxs-lookup"><span data-stu-id="45a6f-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="45a6f-140">名前の付いたリソースは、プロジェクト テンプレートではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="45a6f-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]