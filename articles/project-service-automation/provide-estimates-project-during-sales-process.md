---
title: 営業プロセス中のプロジェクトへの作業見積もりの提供
description: Project Service での営業プロセス実行中のプロジェクトへの作業見積もりの提供方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752913"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>営業プロセス中のプロジェクトへの作業見積もりの提供 (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

営業プロセスの間、見積依頼明細行を含む土台から営業見積もり解決できます。 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 機能は、作業項目を分解し、作業分解構造のプロジェクト用見積もりに寄与する関連属性を関連付けることによって、営業見積もりを考え出すより科学的かつ決定論的な方法提供します。  
  
 営業を達成したなら、プロジェクト計画で関連する作業明細構造を使用でき、それを、プロジェクトの成功完了に必要に応じて絞り込みます。  
  
## <a name="link-a-project-to-a-quote-line"></a>見積依頼明細行にプロジェクトをリンクする  
 プロジェクトベースの見積依頼明細行の作成時に、その見積依頼明細行から新しいプロジェクトを作成できます。 次に、事前に構成された標準プロジェクトの計画と組織に共通な財務見積もり、またはプロジェクト計画のコピーと過去のプロジェクトからの見積もりのいずれかであるプロジェクト テンプレートを使用できます。 プロジェクトの作成時に、プロジェクト テンプレートの選択により、プロジェクト計画、見積もり、および役割要件を絞り込む基盤を提供します。 見積もりからプロジェクトを作成することで、プログラムは見積依頼明細行と自動的にその関連付けられます。  
  
## <a name="project-estimate-components"></a>プロジェクト見積もりのコンポーネント  
 プロジェクトの作業分解構造は、作業をタスクに分解し、タスクの階層を維持して、各タスクを完了するために必要な行動の見積もりを割り当てる方法を提供します。 さらに、タスクおよびスケジュールを完了するために必要なリソースの種類の見積もりを示すためにロールをタスクに関連付けることもできます。  
  
 仕事分解構造によって、作業負荷とスケジュールの見積もりを決定することができます。 既定では、プロジェクトでは前に定義した既定の価格表を使用します。 価格表で定義されたコストと営業価格はプロジェクトの作業分解の財務見積もりを決定するのに役立ちます。  
  
 プロジェクトが見積もりに関連付けられており、見積もりに既定以外の価格表がある場合、見積もりの価格表は財務の見積もりに使用されます。  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>プロジェクトから見積もりへの見積もりのインポート  
 プロジェクトにプロジェクトの見積もりがあると、これらの見積もりを見積依頼明細行にインポートできます。  
  
-   で**見積依頼明細行**で、**見積もりからのインポート**をクリックします。 

-   トランザクションの種類、役割、または仕事分解構造ノードのレベルによって、まとめられたプロジェクトの見積もりをインポートするかどうかを選択します。  
  
### <a name="see-also"></a>関連項目  
 [プロジェクト管理者ガイド](../project-service/project-manager-guide.md)
