---
title: Project Finder Mobile アプリ機能 (プロジェクトサービス) を有効化する
description: Project Service の Project Finder Mobile アプリ機能を有効化する方法
author: JohnPBurrows
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079275"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="c9396-103">Project Finder Mobile アプリ機能 (Project Service) を有効化する</span><span class="sxs-lookup"><span data-stu-id="c9396-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c9396-104">リソースが [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用するスマートフォンの Project Finder Mobile アプリケーションを使用して、新しいプロジェクトを検索して作業し、スキル セットを更新できます。</span><span class="sxs-lookup"><span data-stu-id="c9396-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="c9396-105">このアプリケーションは [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] フォン、および [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="c9396-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="c9396-106">組織単位でパラメーター設定のいくつかのオプションを設定して、プロジェクト リソース要件の表示およびスキルの更新をユーザーに許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9396-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c9396-107">Project Finder Mobile アプリは、設置型インストールではなく、[!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="c9396-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="c9396-108">**Project Service > パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9396-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="c9396-109">Project Finder Mobile アプリケーション機能を許可するために使用するパラメーター設定をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9396-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="c9396-110">**全般** 領域で、 **リソースに表示されるリソース要件** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c9396-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="c9396-111">**リソースによるスキルの更新を許可** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c9396-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="c9396-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="c9396-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="c9396-113">これはグローバル設定です。</span><span class="sxs-lookup"><span data-stu-id="c9396-113">This is a global setting.</span></span> <span data-ttu-id="c9396-114">プロジェクト管理者は、個別のプロジェクトを、プロジェクトの **プロジェクト チーム** ページで表示するかどうかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c9396-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="c9396-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="c9396-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="c9396-116">電子メール通知</span><span class="sxs-lookup"><span data-stu-id="c9396-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="c9396-117">は、次の時間に次の受信者に対してリソース要求に関する電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="c9396-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="c9396-118">受信者</span><span class="sxs-lookup"><span data-stu-id="c9396-118">Recipient</span></span>|<span data-ttu-id="c9396-119">イベント</span><span class="sxs-lookup"><span data-stu-id="c9396-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="c9396-120">プロジェクト管理者</span><span class="sxs-lookup"><span data-stu-id="c9396-120">Project manager</span></span>|<span data-ttu-id="c9396-121">- Project Finder Mobile アプリを使用するプロジェクトに対してリソースをサインアップする場合。</span><span class="sxs-lookup"><span data-stu-id="c9396-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="c9396-122">リソース </span><span class="sxs-lookup"><span data-stu-id="c9396-122">Resource</span></span>|<span data-ttu-id="c9396-123">- プロジェクトの作業リソースがサインアップされ、既に別のリソースによって実行されている場合。</span><span class="sxs-lookup"><span data-stu-id="c9396-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="c9396-124">- スキルの承認要求が既に承認または拒否されている場合。</span><span class="sxs-lookup"><span data-stu-id="c9396-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="c9396-125">- プロジェクトのサインアップ要求が既に承認または拒否されている場合。</span><span class="sxs-lookup"><span data-stu-id="c9396-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="c9396-126">プライバシーに関する声明</span><span class="sxs-lookup"><span data-stu-id="c9396-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="c9396-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9396-127">See Also</span></span>  
 [<span data-ttu-id="c9396-128">リソースの設定</span><span class="sxs-lookup"><span data-stu-id="c9396-128">Set up resources</span></span>](../psa/set-up-resources.md)
