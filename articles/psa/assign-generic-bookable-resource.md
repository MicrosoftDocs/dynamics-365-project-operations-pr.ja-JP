---
title: 一般的な予約可能なリソースをタスクとプロジェクト チームに割り当てる
description: このトピックでは、タスクとプロジェクト チームへの汎用リソースの予約に関する情報を提供します。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127074"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="6f86d-103">予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する</span><span class="sxs-lookup"><span data-stu-id="6f86d-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6f86d-104">プロジェクトに名前付きリソースや実リソースを予約して割り当てることに加えて、プロジェクト タスクに汎用リソースを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="6f86d-105">これらのリソースは、プロジェクトに名前付きリソースを配置する準備ができるまで、名前付きリソースのプレースホルダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="6f86d-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="6f86d-106">Project Service Automation (PSA) で **プロジェクト** ページを開き、**スケジュール** タブで、スケジュールの **リソース** セルに汎用リソースの位置名を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f86d-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="6f86d-107">または、セルの **リソース** アイコンをクリックしてリソース ピッカーを開き、作成する汎用リソースの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f86d-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![汎用チーム メンバーの作成と割り当て](media/RM-how-to-9.png)

<span data-ttu-id="6f86d-109">これで **簡易作成: プロジェクト チーム メンバー** パネルが開きます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="6f86d-110">汎用リソース チーム メンバーの役割と組織単位を入力して **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f86d-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![汎用チーム メンバーの簡易作成](media/RM-how-to-10.png)

3. <span data-ttu-id="6f86d-112">新しい汎用リソース チーム メンバーを作成が完了すると、タスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="6f86d-113">タスク スケジュール内の他のタスクに、その汎用リソースを引き続き割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![既存の汎用チーム メンバーをタスクに割り当てる](media/RM-how-to-11.png)

4. <span data-ttu-id="6f86d-115">汎用リソースを割り当てた後、リソース要求を生成して、リソース マネージャーに直接予約または送信してリソース要求を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![汎用チーム メンバーの要件の生成](media/RM-how-to-12.png)

<span data-ttu-id="6f86d-117">チーム メンバー グリッドでは、上述したリソース ピッカーを使用できることに加え、汎用リソースを直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="6f86d-118">リソースは **簡易作成: プロジェクト チーム メンバー** パネルで指定した開始/終了日と割り当て方法に基づいたリソース要件で追加されます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="6f86d-119">汎用チーム メンバーを直接追加して、カバーするのに必要な時間よりも多くのタスクを汎用リソースに割り当てると、違いがわかります。</span><span class="sxs-lookup"><span data-stu-id="6f86d-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="6f86d-120">**要件の生成** をクリックして要件を再生成し、必要な時間と割り当てのバランスを取ります。</span><span class="sxs-lookup"><span data-stu-id="6f86d-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="6f86d-121">チーム グリッドの **リソース要件** リンクをクリックして、要件を開き、スキル、優先リソースなどを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f86d-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![リソース要件](media/RM-how-to-13.png)

