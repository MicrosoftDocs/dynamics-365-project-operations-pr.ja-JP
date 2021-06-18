---
title: Project Finder Mobile アプリ機能 (プロジェクトサービス) を有効化する
description: Project Service の Project Finder Mobile アプリ機能を有効化する方法
author: JohnPBurrows
ms.prod: ''
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
ms.openlocfilehash: f068c32ac957dc5921ccabc989b3b7a347585c19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007732"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="c078f-103">Project Finder Mobile アプリ機能 (Project Service) を有効化する</span><span class="sxs-lookup"><span data-stu-id="c078f-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c078f-104">リソースが [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用するスマートフォンの Project Finder Mobile アプリケーションを使用して、新しいプロジェクトを検索して作業し、スキルセットを更新できます。</span><span class="sxs-lookup"><span data-stu-id="c078f-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="c078f-105">このアプリケーションは [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] フォン、および [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="c078f-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="c078f-106">ユーザーがプロジェクト リソース要件を表示してスキルを更新できるようにするため、組織単位に対してパラメーター設定のいくつかのオプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c078f-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="c078f-107">Project Finder Mobile アプリは、設置型インストールではなく、[!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="c078f-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="c078f-108">**Project Service > パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c078f-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="c078f-109">Project Finder Mobile アプリケーション機能を許可するために使用するパラメーター設定をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c078f-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="c078f-110">**全般** 領域で、**リソースに表示されるリソース要件** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c078f-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="c078f-111">**リソースによるスキルの更新を許可** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c078f-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="c078f-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="c078f-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="c078f-113">これはグローバル設定です。</span><span class="sxs-lookup"><span data-stu-id="c078f-113">This is a global setting.</span></span> <span data-ttu-id="c078f-114">プロジェクト管理者は、個別のプロジェクトを、プロジェクトの **プロジェクト チーム** ページで表示するかどうかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c078f-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="c078f-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="c078f-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="c078f-116">電子メール通知</span><span class="sxs-lookup"><span data-stu-id="c078f-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="c078f-117">は、次の時間に次の受信者に対してリソース要求に関する電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="c078f-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="c078f-118">受信者</span><span class="sxs-lookup"><span data-stu-id="c078f-118">Recipient</span></span>|<span data-ttu-id="c078f-119">イベント</span><span class="sxs-lookup"><span data-stu-id="c078f-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="c078f-120">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="c078f-120">Project manager</span></span>|<span data-ttu-id="c078f-121">- リソースが、Project Finder Mobile アプリケーションを使用してプロジェクトにサインアップします。</span><span class="sxs-lookup"><span data-stu-id="c078f-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="c078f-122">リソース </span><span class="sxs-lookup"><span data-stu-id="c078f-122">Resource</span></span>|<span data-ttu-id="c078f-123">- リソースがサインアップしたプロジェクトの作業は、既に別のリソースによって実行されています。</span><span class="sxs-lookup"><span data-stu-id="c078f-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="c078f-124">- スキル承認要求が、既に承認または拒否されました。</span><span class="sxs-lookup"><span data-stu-id="c078f-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="c078f-125">- プロジェクトのサインアップ要求が、既に承認または拒否されました。</span><span class="sxs-lookup"><span data-stu-id="c078f-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="c078f-126">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="c078f-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="c078f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c078f-127">See Also</span></span>  
 [<span data-ttu-id="c078f-128">リソースの設定</span><span class="sxs-lookup"><span data-stu-id="c078f-128">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]