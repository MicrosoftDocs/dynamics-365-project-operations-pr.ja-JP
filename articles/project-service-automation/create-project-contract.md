---
title: プロジェクト契約の作成
description: Project Service でのプロジェクトの契約の作成方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ffac492c-c5ce-40d2-8068-3904914c9efe
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7c915f4830b82edbd7365c1c7434d6b8f5ef7122
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752812"
---
# <a name="create-a-project-contract-project-service"></a><span data-ttu-id="74492-103">プロジェクト契約の作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="74492-103">Create a project contract (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="74492-104">プロジェクトの見積もりが得られたので、顧客との契約を作成し、それを正式なものにするときです。</span><span class="sxs-lookup"><span data-stu-id="74492-104">Now that you’ve won the quote for your project, it’s time to create a contract with your customer and make it official.</span></span> <span data-ttu-id="74492-105">各見積もりについて 1 つまたは複数の契約を作成できます。</span><span class="sxs-lookup"><span data-stu-id="74492-105">You can create one or more contracts for each quote.</span></span> <span data-ttu-id="74492-106">契約を作成するとき、プロジェクトの**契約**段階にあります。</span><span class="sxs-lookup"><span data-stu-id="74492-106">When you’re creating a contract, you’re in the **Contract** phase of your project.</span></span>  
  
1. <span data-ttu-id="74492-107">前のステップの**プロジェクト契約**画面で、必要に応じて、**概要**領域の情報を変更します。</span><span class="sxs-lookup"><span data-stu-id="74492-107">In the **Project Contract** screen from the previous step, change any information as necessary in the **Summary** area.</span></span>  
  
2. <span data-ttu-id="74492-108">契約に製品を追加するには、**契約品目**領域の**製品ベースの明細行**で、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74492-108">To add a product to the contract, click **New** under **Product-based Lines** in the **Contract Lines** area.</span></span> <span data-ttu-id="74492-109">**製品名**でアイテムを選択してから、数量、販売価格、および契約金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="74492-109">Select an item under **Product Name**, and then specify the quantity, sales price, and contracted amount.</span></span>  
  
3. <span data-ttu-id="74492-110">契約にプロジェクト ベースの明細行を追加するには、**契約品目**領域の**プロジェクト ベースの明細行**で、**+** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74492-110">To add a project-based line to the contract, click **+** under **Project-based Lines** in the **Contract Lines** area.</span></span> <span data-ttu-id="74492-111">名前、予算額、プロジェクトを可能な場合は入力します。</span><span class="sxs-lookup"><span data-stu-id="74492-111">Enter the name, budget amount, and project, if available.</span></span> <span data-ttu-id="74492-112">見積もりを用意するために WBS (作業分解構造) を使用してプロジェクトを作成する必要がある場合は、[プロジェクトの作成](../project-service/create-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74492-112">If you need to create a project with a work breakdown structure to come up with an estimate, see [Create a project](../project-service/create-project.md).</span></span>  
  
4. <span data-ttu-id="74492-113">編集が完了したら、画面の右下の**保存**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="74492-113">When you’re done editing, click the **Save** button at the bottom right of the screen.</span></span>  
  
5. <span data-ttu-id="74492-114">契約書を顧客に送る準備ができたら、 **その他** (…) をクリックし、 **レポートの実行**をクリックしてから、 **受注**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74492-114">When you’re ready to send the contract to your customer, click **More** (…), click **Run Report**, and then click **Order**.</span></span> <span data-ttu-id="74492-115">レポートを [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] ドキュメントとして保存し、必要に応じて編集してから、契約を顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="74492-115">Save the report as a [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] document, edit as necessary, and then send the contract to your customer.</span></span>  
  
6. <span data-ttu-id="74492-116">顧客が契約を確認した場合、**プロジェクト契約**画面の上部で、**確認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74492-116">If your customer confirms your contract, click **Confirm** at the top of the **Project Contract** screen.</span></span> <span data-ttu-id="74492-117">顧客が一部のアイテムの変更を望む場合は、新しい契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="74492-117">If your customer wants you to change some items, create a new contract.</span></span> <span data-ttu-id="74492-118">顧客が現段階でサービスの使用を決定しない場合は、**プロジェクト契約**画面の上部で、**失注としてクローズ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74492-118">If your customer decides not to use your services at this time, click **Close as Lost** at the top of the **Project Contract** screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="74492-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="74492-119">See Also</span></span>  
 [<span data-ttu-id="74492-120">取引先企業管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="74492-120">Account Manager Guide</span></span>](../project-service/account-manager-guide.md)
