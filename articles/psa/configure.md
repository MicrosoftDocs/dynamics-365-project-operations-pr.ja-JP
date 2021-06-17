---
title: Project Service Automation の構成
description: Project Service の構成のステップ
author: ruhercul
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002846"
---
# <a name="configure-project-service"></a><span data-ttu-id="5494d-103">Project Service の構成</span><span class="sxs-lookup"><span data-stu-id="5494d-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5494d-104">取引先企業、プロジェクト、リソースを管理するために [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 自動化機能を使用するには、いくつかの構成手順を完了して、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ソリューションが組織のニーズに合っていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5494d-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="5494d-105">これらの手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="5494d-105">These steps include:</span></span>  
  
-   <span data-ttu-id="5494d-106">[時間単位のセットアップ](../psa/set-up-time-units.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="5494d-107">プロジェクトの予定と請求の基本として使用する製品カタログの時間単位を構成します。</span><span class="sxs-lookup"><span data-stu-id="5494d-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="5494d-108">[通貨と為替レートのセットアップ](../psa/set-up-currencies-exchange-rates.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="5494d-109">プロジェクトで使用する通貨を設定します。</span><span class="sxs-lookup"><span data-stu-id="5494d-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="5494d-110">[組織単位の作成](../psa/create-organizational-units.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="5494d-111">会社が、地理的条件、ビジネス機能、また論理的分割によってビジネスの分割に使用するグループを設定します。</span><span class="sxs-lookup"><span data-stu-id="5494d-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="5494d-112">[請求頻度のセットアップ](../psa/set-up-invoice-frequencies.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="5494d-113">ユーザーがクライアントの請求に使用する時間期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="5494d-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="5494d-114">[トランザクション カテゴリの構成](../psa/configure-transaction-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="5494d-115">コンサルタントが請求可能および請求不可能な費用を請求するトランザクション カテゴリをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="5494d-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="5494d-116">[経費カテゴリの構成](../psa/configure-expense-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="5494d-117">コンサルタントが請求可能および請求不可能な費用を請求するカテゴリをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="5494d-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="5494d-118">[製品カタログ品目の作成](../psa/create-product-catalog-items.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="5494d-119">販売する、ソフトウェア ライセンスなどの製品を製品カタログに追加します。</span><span class="sxs-lookup"><span data-stu-id="5494d-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="5494d-120">[価格表を作成](../psa/create-price-list.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="5494d-121">プロジェクトで必要な各ロールに対するクライアントへの請求額に応じて、異なる価格表を構成します。</span><span class="sxs-lookup"><span data-stu-id="5494d-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="5494d-122">[リソースの設定](../psa/set-up-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="5494d-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="5494d-123">スキル、能力、リソースの役割、およびプロジェクトに必要なその他のリソース情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="5494d-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5494d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="5494d-124">See Also</span></span>  
 <span data-ttu-id="5494d-125">[Project Service Automation の概要](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="5494d-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="5494d-126">[Project Service Automation の構成](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="5494d-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="5494d-127">[取引先企業管理者ガイド](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="5494d-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="5494d-128">[プロジェクト管理者ガイド](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="5494d-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="5494d-129">[Resource Manager ガイド](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="5494d-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="5494d-130">時間、経費、および共同作業ガイド</span><span class="sxs-lookup"><span data-stu-id="5494d-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]