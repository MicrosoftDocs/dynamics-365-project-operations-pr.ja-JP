---
title: プロジェクト営業案件の作成
description: Project Service でのプロジェクトの営業案件の作成方法
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
ms.openlocfilehash: 57f85549154455f538cbdf3cde11989064968334
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146894"
---
# <a name="create-a-project-opportunity-project-service"></a><span data-ttu-id="f27b2-103">プロジェクト営業案件の作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f27b2-103">Create a project opportunity (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f27b2-104">営業案件とは、サービスの契約に関心のある顧客のうち発注の可能性のある潜在顧客です。</span><span class="sxs-lookup"><span data-stu-id="f27b2-104">Opportunities are warm leads from customers who are interested in contracting your services.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="f27b2-105">の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、取引先企業の 1 つの営業案件を開き、プロジェクトの見積もりを準備し、顧客とのプロジェクト契約を実現するための手順を案内します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] guide you through the steps for opening an opportunity for one of your accounts, preparing a project quote, and working out a project contract with your customer.</span></span> <span data-ttu-id="f27b2-106">営業案件を追加して開始します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-106">Start by adding an opportunity.</span></span> <span data-ttu-id="f27b2-107">サービスおよび製品の見積もりを営業案件に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="f27b2-107">You can add estimates for services and products to the opportunity, as well.</span></span> <span data-ttu-id="f27b2-108">営業案件を追加するときは、プロジェクトの **見込みありと評価** 段階にあります。</span><span class="sxs-lookup"><span data-stu-id="f27b2-108">When you add an opportunity, you’re in the **Qualify** phase of your project.</span></span>  
  
1.  <span data-ttu-id="f27b2-109">**Project Service > 営業案件** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-109">Go to **Project Service > Opportunities**.</span></span>  
  
2.  <span data-ttu-id="f27b2-110">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-110">Click **New**.</span></span>  
  
3.  <span data-ttu-id="f27b2-111">**概要** 領域で、営業案件の会社およびその他の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-111">In the **Summary** area, enter your opportunity's company and other information.</span></span>  
  
4.  <span data-ttu-id="f27b2-112">この潜在顧客に関連付けられているメモと活動 (たとえば、電話や電子メール) を追加します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-112">Add any notes and activities (for example, phone calls or emails) related to this lead.</span></span> <span data-ttu-id="f27b2-113">メモと活動の追加の詳細については、[活動に関するメモ、タスク、電話または電子メールの追跡](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/work-with-activities) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f27b2-113">To learn more about adding notes and activities, see [Keep track of notes, tasks, calls, or email with activities](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/work-with-activities).</span></span>  
  
5.  <span data-ttu-id="f27b2-114">関係者を追加するには、**関係者** 領域で、**+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-114">To add stakeholders, in the **Stakeholders** area, click **+**.</span></span>  
  
6.  <span data-ttu-id="f27b2-115">営業チーム メンバーを追加するには、**営業チーム** 領域で、**+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-115">To add sales team members, in the **Sales Team** area, click **+**.</span></span>  
  
7.  <span data-ttu-id="f27b2-116">競合企業を追加するには、**競合企業** 領域で、**+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-116">To add competitors, in the **Competitors** area, click **+**.</span></span>  
  
8.  <span data-ttu-id="f27b2-117">営業案件に製品を追加するには、**営業案件品目** 領域の **製品ベースの明細行** で、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-117">To add a product to the opportunity, click **New** under **Product-based Lines** in the **Opportunity Lines** area.</span></span> <span data-ttu-id="f27b2-118">**製品名** でアイテムを選択してから、数量、販売価格、および顧客予算を指定します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-118">Select an item under **Product Name**, and then specify the quantity, sales price, and customer budget.</span></span>  
  
9. <span data-ttu-id="f27b2-119">営業案件に製品をプロジェクト見積もり追加するには、**営業案件品目** 領域の **プロジェクト ベースの明細行** で、**+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-119">To add a project estimate to the opportunity, click **+** under **Project-based Lines** in the **Opportunity Lines** area.</span></span> <span data-ttu-id="f27b2-120">名前、予算額、プロジェクトを可能な場合は入力します。</span><span class="sxs-lookup"><span data-stu-id="f27b2-120">Enter the name, budget amount, and project, if available.</span></span> <span data-ttu-id="f27b2-121">見積もりを用意するために WBS (作業分解構造) を使用してプロジェクトを作成する必要がある場合は、[プロジェクトの作成](../psa/create-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f27b2-121">If you need to create a project with a work breakdown structure to come up with an estimate, see [Create a project](../psa/create-project.md).</span></span>  
  
10. <span data-ttu-id="f27b2-122">編集が完了したら、画面の右下の **保存** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f27b2-122">When you’re done editing, click the **Save** button at the bottom right of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f27b2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f27b2-123">See Also</span></span>  
 [<span data-ttu-id="f27b2-124">取引先企業管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="f27b2-124">Account Manager Guide</span></span>](../psa/account-manager-guide.md)
