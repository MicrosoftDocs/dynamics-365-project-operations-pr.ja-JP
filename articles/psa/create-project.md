---
title: プロジェクトの作成
description: Project Service でのプロジェクトの作成方法
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 93958f8e7654ebc4cb038ba7ca0c5e4e02f39937
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148874"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="d2aae-103">プロジェクトの作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d2aae-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d2aae-104">プロジェクト ベースのサービスの営業案件、見積もり、または契約を作成するとき、[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能を使用して、プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="d2aae-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、営業案件から完了までのプロジェクトの管理を支援します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="d2aae-106">プロジェクトを作成するとき、見積もり、コスト予測、およびリソース管理に影響する作業分解構造も作成します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="d2aae-107">**Project Service > プロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="d2aae-108">**新しいプロジェクト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2aae-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="d2aae-109">**概要** 領域で、プロジェクトの名前を入力してから、入力可能な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="d2aae-110">赤いアスタリスク (\*) が付いたパラメーターは必須です。</span><span class="sxs-lookup"><span data-stu-id="d2aae-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="d2aae-111">**保存** をクリックしてプロジェクトを作成します。これにより、プロジェクトの編集を継続できます。</span><span class="sxs-lookup"><span data-stu-id="d2aae-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="d2aae-112">次に、プロジェクトの仕事明細構造を作成して、プロジェクトに必要なタスク、時期、およびリソースのロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="d2aae-113">スケジュール時に、Project Service Automation は適用された **作業時間** テンプレートのタイム ゾーンを尊重します。</span><span class="sxs-lookup"><span data-stu-id="d2aae-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="d2aae-114">ただし、スケジュール タスクを表示すると、タスクの開始日と終了日がユーザーのタイム ゾーンに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2aae-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="d2aae-115">これは、**プロジェクト** フォームの他の時間フェーズ ビューに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d2aae-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="d2aae-116">ユーザーのタイム ゾーンがプロジェクトに適用されている作業時間テンプレートのタイム ゾーンと一致しない場合、違いを説明する警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2aae-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="d2aae-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2aae-117">See Also</span></span>  
 [<span data-ttu-id="d2aae-118">プロジェクト管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="d2aae-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
