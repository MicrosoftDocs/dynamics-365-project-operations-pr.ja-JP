---
title: 売上予測とプロジェクト
description: このトピックは、営業プロセスでスケジュールおよび見積もりのメリットを最大限に活用する方法について説明します。
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 87dc72b76ec4f88684ef2c702718e1ab631ff936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283914"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="dc36e-103">売上予測とプロジェクト</span><span class="sxs-lookup"><span data-stu-id="dc36e-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dc36e-104">営業プロセス中には、プロジェクトを販売見積とリンクすることで売上予測を立てることができます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="dc36e-105">このようにして、営業プロセス中に明確な予測を立てることができ、プロジェクトのスケジュールと予測能力を最大限に活用することができます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="dc36e-106">販売が処理されると、売上予測目的でしようされたスケジュールは、プロジェクト計画のさらなる精密化のベースとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="dc36e-107">プロジェクトを見積依頼明細行にリンクする</span><span class="sxs-lookup"><span data-stu-id="dc36e-107">Linking a project to a quote line</span></span>

<span data-ttu-id="dc36e-108">プロジェクトベースの見積依頼明細行を作成する場合、新規プロジェクトの作成や、**見積依頼明細行** ページの既存のプロジェクトと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![見積依頼明細行フォーム](media/project-8.png)
 
<span data-ttu-id="dc36e-110">見積依頼明細行の詳細で新規プロジェクトを作成する場合、プロジェクト テンプレートを利用できます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="dc36e-111">プロジェクト テンプレートは、標準プロジェクト計画と組織内の一般的な会計の予測を表すモデル プロジェクトです。</span><span class="sxs-lookup"><span data-stu-id="dc36e-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="dc36e-112">過去のプロジェクトからのプロジェクト計画や予測のコピーも表すことができます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![見積依頼明細行の詳細](media/project-9.png)
  
<span data-ttu-id="dc36e-114">見積からプロジェクトを作成する場合、プロジェクトは自動的に見積依頼明細行と関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="dc36e-115">プロジェクト内の見積もりのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="dc36e-115">Components of estimates in a project</span></span>

<span data-ttu-id="dc36e-116">スケジュールにより、作業のタスクへの分割、タスクの階層維持、タスク完了に必要とされるリソースの決定、タスク完了に必要とされる工数の割り当てができます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="dc36e-117">**プロジェクト** ページの **スケジュール** タブのフィールドを使用することで、作業労力とスケジュール予測を定義できます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="dc36e-118">価格表がプロジェクトに関連付けられているため、価格表で定義されている原価と売上を使用して、財務見積りが計算されます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="dc36e-119">プロジェクトからの見積もりを見積へインポートする</span><span class="sxs-lookup"><span data-stu-id="dc36e-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="dc36e-120">プロジェクト見積もりを定義した後、これらを見積依頼明細行にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="dc36e-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="dc36e-121">**見積依頼明細行の詳細** ページで、リボン上の **見積もりからのインポート** を選択して、トランザクションの種類、ロール、またはタスク レベルによるプロジェクト見積もりを要約します。</span><span class="sxs-lookup"><span data-stu-id="dc36e-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]