---
title: 営業プロセス中のプロジェクトへの作業見積もりの提供
description: Project Service での営業プロセス実行中のプロジェクトへの作業見積もりの提供方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079318"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="c3abe-103">営業プロセス中のプロジェクトへの作業見積もりの提供 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c3abe-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c3abe-104">営業プロセスの間、見積依頼明細行を含む土台から営業見積もり解決できます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="c3abe-105">の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、作業項目を分解し、作業分解構造のプロジェクト用見積もりに寄与する関連属性を関連付けることによって、営業見積もりを考え出すより科学的かつ決定論的な方法提供します。</span><span class="sxs-lookup"><span data-stu-id="c3abe-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="c3abe-106">営業を達成したなら、プロジェクト計画で関連する作業明細構造を使用でき、それを、プロジェクトの成功完了に必要に応じて絞り込みます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="c3abe-107">見積依頼明細行にプロジェクトをリンクする</span><span class="sxs-lookup"><span data-stu-id="c3abe-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="c3abe-108">プロジェクトベースの見積依頼明細行の作成時に、その見積依頼明細行から新しいプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="c3abe-109">次に、事前に構成された標準プロジェクトの計画と組織に共通な財務見積もり、またはプロジェクト計画のコピーと過去のプロジェクトからの見積もりのいずれかであるプロジェクト テンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="c3abe-110">プロジェクトの作成時に、プロジェクト テンプレートの選択により、プロジェクト計画、見積もり、および役割要件を絞り込む基盤を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3abe-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="c3abe-111">見積もりからプロジェクトを作成することで、プログラムは見積依頼明細行と自動的にその関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="c3abe-112">プロジェクト見積もりのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="c3abe-112">Project estimate components</span></span>  
 <span data-ttu-id="c3abe-113">プロジェクトの作業分解構造は、作業をタスクに分解し、タスクの階層を維持して、各タスクを完了するために必要な行動の見積もりを割り当てる方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3abe-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="c3abe-114">さらに、タスクおよびスケジュールを完了するために必要なリソースの種類の見積もりを示すためにロールをタスクに関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="c3abe-115">仕事分解構造によって、作業負荷とスケジュールの見積もりを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="c3abe-116">既定では、プロジェクトでは前に定義した既定の価格表を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3abe-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="c3abe-117">価格表で定義されたコストと営業価格はプロジェクトの作業分解の財務見積もりを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="c3abe-118">プロジェクトが見積もりに関連付けられており、見積もりに既定以外の価格表がある場合、見積もりの価格表は財務の見積もりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c3abe-119">プロジェクトから見積もりへの見積もりのインポート</span><span class="sxs-lookup"><span data-stu-id="c3abe-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="c3abe-120">プロジェクトにプロジェクトの見積もりがあると、これらの見積もりを見積依頼明細行にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="c3abe-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="c3abe-121">で **見積依頼明細行** で、 **見積もりからのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3abe-121">In **Quote Line Details** , click **Import from estimates**.</span></span> 

-   <span data-ttu-id="c3abe-122">トランザクションの種類、役割、または仕事分解構造ノードのレベルによって、まとめられたプロジェクトの見積もりをインポートするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3abe-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c3abe-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3abe-123">See Also</span></span>  
 [<span data-ttu-id="c3abe-124">プロジェクト管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="c3abe-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
