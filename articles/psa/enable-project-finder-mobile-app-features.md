---
title: Project Finder Mobile アプリ機能 (プロジェクトサービス) を有効化する
description: Project Service の Project Finder Mobile アプリ機能を有効化する方法
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144554"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Project Finder Mobile アプリ機能 (Project Service) を有効化する

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

リソースが [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用するスマートフォンの Project Finder Mobile アプリケーションを使用して、新しいプロジェクトを検索して作業し、スキルセットを更新できます。  
  
 このアプリケーションは [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] フォン、および [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] で使用可能です。  
    
 ユーザーがプロジェクト リソース要件を表示してスキルを更新できるようにするため、組織単位に対してパラメーター設定のいくつかのオプションを設定する必要があります。
  
> [!NOTE]
>  Project Finder Mobile アプリは、設置型インストールではなく、[!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] でのみ動作します。  
  
1. **Project Service > パラメーター** に移動します。  
  
2. Project Finder Mobile アプリケーション機能を許可するために使用するパラメーター設定をクリックします。  
  
3. **全般** 領域で、**リソースに表示されるリソース要件** を **はい** に設定します。  
  
4. **リソースによるスキルの更新を許可** を **はい** に設定します。  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   これはグローバル設定です。 プロジェクト管理者は、個別のプロジェクトを、プロジェクトの **プロジェクト チーム** ページで表示するかどうかを設定できます。  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>電子メール通知  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] は、次の時間に次の受信者に対してリソース要求に関する電子メールを送信します。  
  
|受信者|イベント|  
|---------------|-----------|  
|プロジェクト マネージャー|- リソースが、Project Finder Mobile アプリケーションを使用してプロジェクトにサインアップします。|  
|リソース |- リソースがサインアップしたプロジェクトの作業は、既に別のリソースによって実行されています。<br />- スキル承認要求が、既に承認または拒否されました。<br />- プロジェクトのサインアップ要求が、既に承認または拒否されました。|  
  
## <a name="privacy-notice"></a>プライバシー通知  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>関連項目  
 [リソースの設定](../psa/set-up-resources.md)
