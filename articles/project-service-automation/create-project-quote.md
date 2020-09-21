---
title: プロジェクト見積りの作成
description: Project Service でのプロジェクト見積もりの作成方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 08ad2d2d-cc4b-4598-93c0-426c7ce1aa8f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: efe4ca78641518058b2ee30f3aa69796709eca83
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752803"
---
# <a name="create-a-project-quote-project-service"></a><span data-ttu-id="81641-103">プロジェクト見積もりの作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="81641-103">Create a project quote (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="81641-104">見積もりの作成は、営業案件の作成と似ています。</span><span class="sxs-lookup"><span data-stu-id="81641-104">Creating a quote is similar to creating an opportunity.</span></span> <span data-ttu-id="81641-105">営業案件が内部情報のためですが、見積もりは潜在的な顧客に送信されるものです。</span><span class="sxs-lookup"><span data-stu-id="81641-105">While an opportunity is for internal information, a quote is what you send out to your potential customers.</span></span> <span data-ttu-id="81641-106">各営業案件について 1 つまたは複数の見積もりを作成できます。</span><span class="sxs-lookup"><span data-stu-id="81641-106">You can create one or more quotes for each opportunity.</span></span> <span data-ttu-id="81641-107">潜在顧客に送信する見積もりを作成するとき、プロジェクトの**提案**ステージにあります。</span><span class="sxs-lookup"><span data-stu-id="81641-107">When you’re creating a quote to send to your potential customer, you’re in the **Propose** stage of your project.</span></span>  
  
1. <span data-ttu-id="81641-108">営業案件から見積もりを作成するには、**Project Service > 営業案件**の順に移動してから、見積もりを作成する対象の営業案件をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-108">To create a quote from an opportunity, go to **Project Service > Opportunities**, and then click the opportunity you want to create a quote for.</span></span>  
  
2. <span data-ttu-id="81641-109">プロセス バーの右側の**次のステージ**をクリックし、既存の見積もりを選択するか、新しい見積もりを作成するために**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-109">Click **Next Stage** on the right side of the process bar, and then either select an existing quote or click **Create** to create a new quote.</span></span>  
  
3. <span data-ttu-id="81641-110">**概要**領域で、必要に応じて情報を変更します。</span><span class="sxs-lookup"><span data-stu-id="81641-110">In the **Summary** area, change any information as necessary.</span></span>  
  
4. <span data-ttu-id="81641-111">**保存**をクリックして見積もりを作成します。これにより、そのレコードの編集を継続できます。</span><span class="sxs-lookup"><span data-stu-id="81641-111">Click **Save** to create the quote so you can continue editing it.</span></span>  
  
5. <span data-ttu-id="81641-112">見積もりに製品を追加するには、**見積依頼明細行**領域の**製品ベースの明細行**で、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-112">To add a product to the quote, click **New** under **Product-based Lines** in the **Quote Lines** area.</span></span> <span data-ttu-id="81641-113">**製品名**でアイテムを選択してから、数量、販売価格、および見積もり金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="81641-113">Select an item under **Product Name**, and then specify the quantity, sales price, and quoted amount.</span></span>  
  
6. <span data-ttu-id="81641-114">見積もりにプロジェクト見積もりを追加するには、**見積依頼明細行**領域の**プロジェクト ベースの明細行**で、**+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-114">To add a project estimate to the quote, click **+** under **Project-based Lines** in the **Quote Lines** area.</span></span> <span data-ttu-id="81641-115">名前、予算額、プロジェクトを可能な場合は入力します。</span><span class="sxs-lookup"><span data-stu-id="81641-115">Enter the name, budget amount, and project, if available.</span></span> <span data-ttu-id="81641-116">見積もりを用意するために WBS (作業分解構造) を使用してプロジェクトを作成する必要がある場合は、[プロジェクトの作成](../project-service/create-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81641-116">If you need to create a project with a work breakdown structure to come up with an estimate, see [Create a project](../project-service/create-project.md).</span></span>  
  
7. <span data-ttu-id="81641-117">編集が完了したら、画面の右下の**保存**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-117">When you’re done editing, click the **Save** button at the bottom right of the screen.</span></span>  
  
8. <span data-ttu-id="81641-118">見積もりを顧客に送る準備ができたら、**その他** (…) をクリックし、**レポートの実行**をクリックしてから、**見積もり**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-118">When you’re ready to send the quote to your customer, click **More** (…), click **Run Report**, and then click **Quote**.</span></span> <span data-ttu-id="81641-119">レポートを [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] ドキュメントとして保存し、必要に応じて編集し、見積もりを顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="81641-119">Save the report as a [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] document, edit as necessary, and send the quote to your customer.</span></span>  
  
9. <span data-ttu-id="81641-120">顧客が見積もりを受け取った場合は、**見積もり**画面の上部の**受注としてクローズ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-120">If your customer accepts your quote, click **Close as Won** at the top of the **Quote** screen.</span></span> <span data-ttu-id="81641-121">顧客が一部の項目の変更を望む場合は、このプロセス全体を再度実行して新しい見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="81641-121">If your customer wants you to change some items, follow this entire process again to create a new quote.</span></span> <span data-ttu-id="81641-122">顧客が現段階でサービスの使用を決定しない場合は、**見積もり**画面の上部で、**失注としてクローズ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81641-122">If your customer decides not to use your services at this time, click **Close as Lost** at the top of the **Quote** screen.</span></span>  
  
   <span data-ttu-id="81641-123">受注として見積もりをクローズするとき、プロジェクトは**契約**ステージに進み、**プロジェクト契約**画面が表示されて、このプロジェクトに対する契約の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="81641-123">When you close a quote as won, your project moves on to the **Contract** stage, and the **Project Contract** screen prompts you to create a contract for this project.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="81641-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="81641-124">See Also</span></span>  
 [<span data-ttu-id="81641-125">取引先企業管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="81641-125">Account Manager Guide</span></span>](../project-service/account-manager-guide.md)
