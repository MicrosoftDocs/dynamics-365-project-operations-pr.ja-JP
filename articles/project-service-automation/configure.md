---
title: Project Service Automation の構成
description: Project Service の構成のステップ
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752839"
---
# <a name="configure-project-service"></a><span data-ttu-id="18009-103">Project Service の構成</span><span class="sxs-lookup"><span data-stu-id="18009-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="18009-104">取引先企業、プロジェクト、リソースを管理するために [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 自動化機能を使用するには、いくつかの構成手順を完了して、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ソリューションが組織のニーズに合っていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18009-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="18009-105">これらの手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="18009-105">These steps include:</span></span>  
  
-   <span data-ttu-id="18009-106">[時間単位のセットアップ](../project-service/set-up-time-units.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="18009-107">プロジェクトの予定と請求の基本として使用する製品カタログの時間単位を構成します。</span><span class="sxs-lookup"><span data-stu-id="18009-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="18009-108">[通貨と為替レートのセットアップ](../project-service/set-up-currencies-exchange-rates.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="18009-109">プロジェクトで使用する通貨を設定します。</span><span class="sxs-lookup"><span data-stu-id="18009-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="18009-110">[組織単位の作成](../project-service/create-organizational-units.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="18009-111">会社が、地理的条件、ビジネス機能、また論理的分割によってビジネスの分割に使用するグループを設定します。</span><span class="sxs-lookup"><span data-stu-id="18009-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="18009-112">[請求頻度のセットアップ](../project-service/set-up-invoice-frequencies.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="18009-113">ユーザーがクライアントの請求に使用する時間期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="18009-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="18009-114">[トランザクション カテゴリの構成](../project-service/configure-transaction-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="18009-115">コンサルタントが請求可能および請求不可能な費用を請求するトランザクション カテゴリをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="18009-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="18009-116">[経費カテゴリの構成](../project-service/configure-expense-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="18009-117">コンサルタントが請求可能および請求不可能な費用を請求するカテゴリをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="18009-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="18009-118">[製品カタログ品目の作成](../project-service/create-product-catalog-items.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="18009-119">販売する、ソフトウェア ライセンスなどの製品を製品カタログに追加します。</span><span class="sxs-lookup"><span data-stu-id="18009-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="18009-120">[価格表を作成](../project-service/create-price-list.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="18009-121">プロジェクトで必要な各ロールに対するクライアントへの請求額に応じて、異なる価格表を構成します。</span><span class="sxs-lookup"><span data-stu-id="18009-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="18009-122">[リソースの設定](../project-service/set-up-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="18009-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="18009-123">スキル、能力、リソースの役割、およびプロジェクトに必要なその他のリソース情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="18009-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="18009-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="18009-124">See Also</span></span>  
 <span data-ttu-id="18009-125">[Project Service Automation の概要](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="18009-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="18009-126">[Project Service Automation の構成](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="18009-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="18009-127">[取引先企業管理者ガイド](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="18009-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="18009-128">[プロジェクト管理者ガイド](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="18009-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="18009-129">[Resource Manager ガイド](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="18009-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="18009-130">時間、経費、および共同作業ガイド</span><span class="sxs-lookup"><span data-stu-id="18009-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
