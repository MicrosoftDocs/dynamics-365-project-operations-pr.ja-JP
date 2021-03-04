---
title: プロジェクト テンプレートを作成
description: Project Service でのプロジェクト テンプレートの作成方法
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149369"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="00f0d-103">プロジェクト テンプレート (Project Service) の作成</span><span class="sxs-lookup"><span data-stu-id="00f0d-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="00f0d-104">会社が類似した種類のプロジェクトで定期的に入札を行う場合は、プロジェクト テンプレートを使用すると時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="00f0d-105">プロジェクト テンプレートにより、プロジェクトの種類ごとにロールと推定時間の標準的なセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="00f0d-106">アカウント管理者およびプロジェクト管理者は、プロジェクト テンプレートに基づいてプロジェクトを作成でき、またテンプレートをコピーして独自のテンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="00f0d-107">プロジェクト テンプレートのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="00f0d-107">Components of project template</span></span>
 <span data-ttu-id="00f0d-108">プロジェクト テンプレートは、次の 3 つのコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="00f0d-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="00f0d-109">**作業分解構造**: プロジェクト テンプレートの作業分解構造は、そのプロジェクトと同じ要素のセットを持ちます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="00f0d-110">タスクの階層の作成、タスクへのロールの割り当て、スケジュール属性の定義、依存関係の設定、および Gantt 内のすべてのデータの表示ができます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="00f0d-111">プロジェクト テンプレートの作業分解構造は、各タスクごとのタスク モードもサポートします。</span><span class="sxs-lookup"><span data-stu-id="00f0d-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="00f0d-112">作業スケジュールを作成する場合、プロジェクト テンプレートとプロジェクトに違いはありません。</span><span class="sxs-lookup"><span data-stu-id="00f0d-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="00f0d-113">**プロジェクト見積もり**: テンプレートのプロジェクト見積もりは、プロジェクトの場合と同じように動作します。ただし、既定のコストと販売価格の価格表は常に [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] パラメーターで定義されている既定のコストと販売価格表です。</span><span class="sxs-lookup"><span data-stu-id="00f0d-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="00f0d-114">残りの機能はプロジェクトの場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="00f0d-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="00f0d-115">**プロジェクト チームの構成**: プロジェクト テンプレートのプロジェクト チームを構成する場合、テンプレートに名前付きリソースは予約できません。</span><span class="sxs-lookup"><span data-stu-id="00f0d-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="00f0d-116">作業分解構造 に **プロジェクト チームの生成** を使用することにより、汎用リソースのセットを生成できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="00f0d-117">汎用リソースに必要なスキルと能力も指定できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="00f0d-118">プロジェクト テンプレートでは汎用リソースの代わりに予約可能リソースを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="00f0d-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="00f0d-119">テンプレートからのプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="00f0d-119">Create a project from a template</span></span>  
 <span data-ttu-id="00f0d-120">次のように、テンプレートからプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="00f0d-121">見積もりからプロジェクトを作成した場合は、プロジェクトの簡易作成フォームでプロジェクト テンプレートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="00f0d-122">**新しいプロジェクト** をクリックしてプロジェクトを作成した場合は、レコードを保存する前にプロジェクト フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="00f0d-123">これ以降は、**テンプレートの選択** フィールドをクリックすることにより、組織で事前に定義されたプロジェクト テンプレートの一覧から選択できます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="00f0d-124">**プロジェクト テンプレート** ページで **テンプレートからのプロジェクトの作成** をクリックし、テンプレートからプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="00f0d-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="00f0d-125">テンプレートのコンポーネントのプロジェクトへのコピー</span><span class="sxs-lookup"><span data-stu-id="00f0d-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="00f0d-126">プロジェクトにテンプレートのコンポーネントをコピーする場合、理解しておく必要がある事項がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="00f0d-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="00f0d-127">**作業分解構造のコピー**: プロジェクト テンプレートの作業分解構造をコピーするときに、プロジェクトがテンプレートと異なるプロジェクト カレンダーを持つ場合、プロジェクト カレンダーの作業時間はタスク スケジュールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="00f0d-128">これにより、背景となっているプロジェクト カレンダーにスケジュールを調整します。</span><span class="sxs-lookup"><span data-stu-id="00f0d-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="00f0d-129">同様に、作業分解構造の最初のタスクがプロジェクトの開始日を使用する場合、タスク階層スケジュールの残り部分も、テンプレートの作業分解構造で指定されている期間と依存関係に基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="00f0d-130">**プロジェクト見積もりのコピー**: プロジェクト見積もり行をコピーする場合は、原価価格表と販売価格表の顧客用に、価格表がプロジェクトの所有部署に基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="00f0d-131">単位原価と販売価格は、営業エンティティに関連付けられているプロジェクトのこれらの価格表から決定されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="00f0d-132">**プロジェクト チームのコピー**: テンプレートからプロジェクトにプロジェクト チームをコピーする場合、汎用リソースはテンプレートで定義されているスキルおよび能力と共にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="00f0d-133">汎用リソースの割り当ては、プロジェクト テンプレートと同様に維持されます。</span><span class="sxs-lookup"><span data-stu-id="00f0d-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="00f0d-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="00f0d-134">See Also</span></span>  
 [<span data-ttu-id="00f0d-135">プロジェクト管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="00f0d-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
