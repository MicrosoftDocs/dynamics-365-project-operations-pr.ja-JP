---
title: プロジェクト見積りの作成
description: Project Service でのプロジェクト見積もりの作成方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 08ad2d2d-cc4b-4598-93c0-426c7ce1aa8f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: efe4ca78641518058b2ee30f3aa69796709eca83
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752803"
---
# <a name="create-a-project-quote-project-service"></a>プロジェクト見積もりの作成 (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

見積もりの作成は、営業案件の作成と似ています。 営業案件が内部情報のためですが、見積もりは潜在的な顧客に送信されるものです。 各営業案件について 1 つまたは複数の見積もりを作成できます。 潜在顧客に送信する見積もりを作成するとき、プロジェクトの**提案**ステージにあります。  
  
1. 営業案件から見積もりを作成するには、**Project Service > 営業案件**の順に移動してから、見積もりを作成する対象の営業案件をクリックします。  
  
2. プロセス バーの右側の**次のステージ**をクリックし、既存の見積もりを選択するか、新しい見積もりを作成するために**作成**をクリックします。  
  
3. **概要**領域で、必要に応じて情報を変更します。  
  
4. **保存**をクリックして見積もりを作成します。これにより、そのレコードの編集を継続できます。  
  
5. 見積もりに製品を追加するには、**見積依頼明細行**領域の**製品ベースの明細行**で、**新規**をクリックします。 **製品名**でアイテムを選択してから、数量、販売価格、および見積もり金額を指定します。  
  
6. 見積もりにプロジェクト見積もりを追加するには、**見積依頼明細行**領域の**プロジェクト ベースの明細行**で、**+** をクリックします。 名前、予算額、プロジェクトを可能な場合は入力します。 見積もりを用意するために WBS (作業分解構造) を使用してプロジェクトを作成する必要がある場合は、[プロジェクトの作成](../project-service/create-project.md) を参照してください。  
  
7. 編集が完了したら、画面の右下の**保存**ボタンをクリックします。  
  
8. 見積もりを顧客に送る準備ができたら、**その他** (…) をクリックし、**レポートの実行**をクリックしてから、**見積もり**をクリックします。 レポートを [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] ドキュメントとして保存し、必要に応じて編集し、見積もりを顧客に送信します。  
  
9. 顧客が見積もりを受け取った場合は、**見積もり**画面の上部の**受注としてクローズ**をクリックします。 顧客が一部の項目の変更を望む場合は、このプロセス全体を再度実行して新しい見積もりを作成します。 顧客が現段階でサービスの使用を決定しない場合は、**見積もり**画面の上部で、**失注としてクローズ**をクリックします。  
  
   受注として見積もりをクローズするとき、プロジェクトは**契約**ステージに進み、**プロジェクト契約**画面が表示されて、このプロジェクトに対する契約の作成を要求します。  
  
### <a name="see-also"></a>関連項目  
 [取引先企業管理者ガイド](../project-service/account-manager-guide.md)