---
title: 組織単位の作成
description: Project Service での組織単位の作成方法
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f27cfd9d-1265-40e6-b19e-5d02c3d91ca6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2712c8a22d97148b5481be3cb5cced1746ea08e8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752793"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="4d1a9-103">組織単位の作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4d1a9-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4d1a9-104">会社は、地理、機能、またはその他の領域によってコンサルティング ビジネスを編成する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="4d1a9-105">コンサルティング ビジネスを反映した組織単位を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="4d1a9-106">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 組織単位は、企業内のこうしたグループまたは事業部とは別個のコスト レートを伴う請求できるリソースを雇う専門的サービス企業のグループまたは事業部です。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4d1a9-107">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 組織単位は、[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] の部署とは異なります。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="4d1a9-108">部署は、[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] 情報へのアクセス レベルに影響を与えるセキュリティ構造がより多く、通常、親会社および子会社または事業部など、会社事業部周囲で組織されます。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="4d1a9-109">組織単位は、地理的場所 (EMEA または LATAM など) によって、機能 (製品開発または IT アウトソーシングなど) によって、その他のパラメーターによってのいずれかで、コンサルティング会社がさまざまな業務をどのように分類するかを表します。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="4d1a9-110">**Project Service > 組織単位**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="4d1a9-111">**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="4d1a9-112">**概要**領域で、組織単位の名前を**名前**に入力してから、必要に応じて他のフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-112">In the **General** area, enter a name for the organization unit in **Name**, and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="4d1a9-113">**保存**をクリックしてレコードを作成します。これにより、そのレコードの編集を継続できます。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="4d1a9-114">**原価価格表**の下で、**+** をクリックして価格表を追加します。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-114">Under **Cost Price Lists**, click **+** to add a price list.</span></span> <span data-ttu-id="4d1a9-115">ここの**コスト**コンテキストでのみ価格表を追加できます。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="4d1a9-116">**名前**フィールドで、**検索**ボタンをクリックして、この組織単位で使用できるようにする価格表を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="4d1a9-117">必要に応じて価格表を追加し続けます。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="4d1a9-118">完了したら、画面の右下隅の**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d1a9-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4d1a9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d1a9-119">See Also</span></span>  
 [<span data-ttu-id="4d1a9-120">Project Service Automation の構成</span><span class="sxs-lookup"><span data-stu-id="4d1a9-120">Configure Project Service Automation</span></span>](../project-service/configure.md)
