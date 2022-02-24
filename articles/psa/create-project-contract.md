---
title: プロジェクト契約の作成
description: Project Service でのプロジェクトの契約の作成方法
author: ruhercul
manager: kfend
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
ms.openlocfilehash: e26e5193353d7bbb594f9f31d95c18130d614517
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150854"
---
# <a name="create-a-project-contract-project-service"></a>プロジェクト契約の作成 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

プロジェクトの見積もりが得られたので、顧客との契約を作成し、それを正式なものにするときです。 各見積もりについて 1 つまたは複数の契約を作成できます。 契約を作成するとき、プロジェクトの **契約** 段階にあります。  
  
1. 前のステップの **プロジェクト契約** 画面で、必要に応じて、**概要** 領域の情報を変更します。  
  
2. 契約に製品を追加するには、**契約品目** 領域の **製品ベースの明細行** で、**新規** をクリックします。 **製品名** でアイテムを選択してから、数量、販売価格、および契約金額を指定します。  
  
3. 契約にプロジェクト ベースの明細行を追加するには、**契約品目** 領域の **プロジェクト ベースの明細行** で、**+** をクリックします。 名前、予算額、プロジェクトを可能な場合は入力します。 見積もりを用意するために WBS (作業分解構造) を使用してプロジェクトを作成する必要がある場合は、[プロジェクトの作成](../psa/create-project.md) を参照してください。  
  
4. 編集が完了したら、画面の右下の **保存** ボタンをクリックします。  
  
5. 契約書を顧客に送る準備ができたら、 **その他** (…) をクリックし、 **レポートの実行** をクリックしてから、 **受注** をクリックします。 レポートを [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] ドキュメントとして保存し、必要に応じて編集してから、契約を顧客に送信します。  
  
6. 顧客が契約を確認した場合、**プロジェクト契約** 画面の上部で、**確認** をクリックします。 顧客が一部のアイテムの変更を望む場合は、新しい契約を作成します。 顧客が現段階でサービスの使用を決定しない場合は、**プロジェクト契約** 画面の上部で、**失注としてクローズ** をクリックします。  
  
### <a name="see-also"></a>関連項目  
 [取引先企業管理者ガイド](../psa/account-manager-guide.md)
