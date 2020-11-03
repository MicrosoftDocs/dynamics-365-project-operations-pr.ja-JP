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
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Project Finder Mobile アプリ機能 (Project Service) を有効化する

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

リソースが [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用するスマートフォンの Project Finder Mobile アプリケーションを使用して、新しいプロジェクトを検索して作業し、スキル セットを更新できます。  
  
 このアプリケーションは [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] フォン、および [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] で使用可能です。  
  
 組織単位でパラメーター設定のいくつかのオプションを設定して、プロジェクト リソース要件の表示およびスキルの更新をユーザーに許可する必要があります。  
  
> [!NOTE]
>  Project Finder Mobile アプリは、設置型インストールではなく、[!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] でのみ動作します。  
  
1. **Project Service > パラメーター** に移動します。  
  
2. Project Finder Mobile アプリケーション機能を許可するために使用するパラメーター設定をクリックします。  
  
3. **全般** 領域で、 **リソースに表示されるリソース要件** を **はい** に設定します。  
  
4. **リソースによるスキルの更新を許可** を **はい** に設定します。  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   これはグローバル設定です。 プロジェクト管理者は、個別のプロジェクトを、プロジェクトの **プロジェクト チーム** ページで表示するかどうかを設定できます。  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>電子メール通知  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] は、次の時間に次の受信者に対してリソース要求に関する電子メールを送信します。  
  
|受信者|イベント|  
|---------------|-----------|  
|プロジェクト管理者|- Project Finder Mobile アプリを使用するプロジェクトに対してリソースをサインアップする場合。|  
|リソース |- プロジェクトの作業リソースがサインアップされ、既に別のリソースによって実行されている場合。<br />- スキルの承認要求が既に承認または拒否されている場合。<br />- プロジェクトのサインアップ要求が既に承認または拒否されている場合。|  
  
## <a name="privacy-notice"></a>プライバシーに関する声明  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>関連項目  
 [リソースの設定](../psa/set-up-resources.md)
