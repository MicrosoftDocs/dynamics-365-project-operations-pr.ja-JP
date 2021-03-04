---
title: 価格表を作成します。
description: Project Service での価格表の作成方法
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18f6e7a7a96f374acc85ee1027c5252cbf7ab5f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149459"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="3a01f-103">価格表の作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3a01f-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3a01f-104">価格表は、取引先企業管理が見積もりとプロジェクトの作成のためと、プロジェクトのコストの確定のために使用できるテンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="3a01f-105">価格表はロールと経費の品目一覧と、それぞれに対して請求する価格を提供します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="3a01f-106">製品を販売する異なる地域、または異なる営業ルートごとに個別の価格構造を維持できるように、複数の価格表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="3a01f-107">顧客に請求を送る際に使用する通貨ごとに、価格表を少なくとも 1 つ作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="3a01f-108">納入する作業に対する財務上の見積もりを作成するために、プロジェクトごとにバッキング コストと販売価格表を必ず備えるようにします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="3a01f-109">組織で作成されるすべてのプロジェクトに適用される、既定のコストと販売価格表を設定します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="3a01f-110">価格表はロールと経費カテゴリに依存するので、価格表を作成する前に、価格表を作成する際に使用するロールと経費カテゴリの構成を必ず終えておきます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="3a01f-111">**Project Service > 価格表** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="3a01f-112">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="3a01f-113">**コンテキスト** で、価格表が **コスト** 用か、**購入** 用か、または **営業** 用かを選択します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="3a01f-114">**名前** に、価格表の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="3a01f-115">**通貨** で、請求書の作成または原価計算に使用する通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="3a01f-116">**時間単位** で、価格が適用される、日または時間などの期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="3a01f-117">必要に応じて、**開始日**、**終了日**、および **説明** を入力します。</span><span class="sxs-lookup"><span data-stu-id="3a01f-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="3a01f-118">**保存** をクリックしてレコードを作成します。これにより、そのレコードの編集を継続できます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="3a01f-119">価格表にロール価格を追加するには、**ロール価格** の下にある **+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="3a01f-120">**ロール価格** ウィンドウで詳細を入力してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="3a01f-121">必要に応じて、ロール価格の追加を続けます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="3a01f-122">完了したら、画面の右下隅の **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="3a01f-123">価格表に経費カテゴリ価格を追加するには、**カテゴリ価格** の下にある **+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="3a01f-124">**トランザクション カテゴリ価格** ウィンドウで、詳細を入力してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="3a01f-125">必要に応じて、カテゴリ価格の追加を続けます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="3a01f-126">完了したら、画面の右下隅の **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="3a01f-127">価格表に価格表品目を追加するには、**価格表品目** の下にある **+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="3a01f-128">**価格表品目** ウィンドウで詳細を入力してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="3a01f-129">必要に応じて、価格表品目の追加を続けます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="3a01f-130">完了したら、画面の右下隅の **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="3a01f-131">価格表に担当地域の関連付けを追加するには、**担当地域の関連付け** の下の **+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="3a01f-132">**新しい接続** ウィンドウで詳細を入力してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="3a01f-133">必要に応じて、担当地域の関連付けの追加を続けます。</span><span class="sxs-lookup"><span data-stu-id="3a01f-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="3a01f-134">完了したら、画面の右下隅の **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3a01f-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3a01f-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a01f-135">See Also</span></span>  
 [<span data-ttu-id="3a01f-136">Project Service Automation の構成</span><span class="sxs-lookup"><span data-stu-id="3a01f-136">Configure Project Service Automation</span></span>](../psa/configure.md)
