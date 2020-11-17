---
title: プロジェクトの作成
description: Project Service でのプロジェクトの作成方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079280"
---
# <a name="create-a-project-project-service"></a>プロジェクトの作成 (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

プロジェクト ベースのサービスの営業案件、見積もり、または契約を作成するとき、[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能を使用して、プロジェクトを作成します。 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、営業案件から完了までのプロジェクトの管理を支援します。 プロジェクトを作成するとき、見積もり、コスト予測、およびリソース管理に影響する作業分解構造も作成します。  
  
1.  **Project Service > プロジェクト** の順に移動します。  
  
2.  **新しいプロジェクト** をクリックします。  
  
3.  **概要** 領域で、プロジェクトの名前を入力してから、入力可能な詳細を入力します。 赤いアスタリスク (*) が付いたパラメーターは必須です。  
  
4.  **保存** をクリックしてプロジェクトを作成します。これにより、プロジェクトの編集を継続できます。  
  
次に、プロジェクトの仕事明細構造を作成して、プロジェクトに必要なタスク、時期、およびリソースのロールを定義します。  

> [!NOTE]
> スケジュール時に、Project Service Automation は適用された **作業時間** テンプレートのタイム ゾーンを尊重します。 ただし、スケジュール タスクを表示すると、タスクの開始日と終了日がユーザーのタイム ゾーンに表示されます。 これは、 **プロジェクト** フォームの他の時間フェーズ ビューに適用されます。 ユーザーのタイム ゾーンがプロジェクトに適用されている作業時間テンプレートのタイム ゾーンと一致しない場合、違いを説明する警告が表示されます。 
  
### <a name="see-also"></a>関連項目  
 [プロジェクト管理者ガイド](../psa/project-manager-guide.md)