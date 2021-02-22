---
title: 会社間請求の構成
description: このトピックでは、プロジェクトの会社間請求を構成する方法ついて情報と例を提供します。
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595502"
---
# <a name="configure-intercompany-invoicing"></a>会社間請求の構成

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

次の手順を実行して、Dynamics 365 Project Operations のプロジェクトに会社間請求を設定します。 会社間トランザクションは、1 つの会社や組織単位に属するプロジェクト契約に基づいた時間とコストのトランザクションで、プロジェクト契約のリソースは、異なる会社や組織単位の一部です。

## <a name="example-configure-intercompany-invoicing"></a>例: 会社間請求の構成

次の例では、Contoso Robotics USA (USPM) が借入法人であり、Contoso Robotics UK (GBPM) が貸付法人です。 

1. **法人間に会社間会計を構成します**。 借入法人と貸付法人の各ペアは、一般会計の [会社間会計](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup) ページで構成する必要があります。
    
    1. Dynamics 365 Finance で **一般会計** > **転記の設定** > **会社間会計** の順に移動します。 以下の情報を使用してレコードを作成します。

        - **元の会社** = **GBPM**
        - **相手の会社** = **USPM**

2. **法人間に取引関係を構成します**。 借入法人を表す顧客レコードは、貸付法人に作成する必要があります。 貸付法人を表すベンダー レコードは、借入法人に作成する必要があります。

     1. Finance で法人 **GBPM** を選択します。
     2. **売掛金勘定** > **顧客** > **すべての顧客** に移動します。 法人 **USPM** に新しいレコードを作成します。
     3. **名前** を展開して **タイプ** でレコードをフィルターし、**法人** を選択します。 
     4. **Contoso Robotics USA (USPM)** の顧客レコードを見つけて選択します。
     5. **照合の使用** を選択します。 
     6. 顧客グループを選択してレコードを保存します。
     7. 法人 **USPM** を選択します。
     8. **買掛金勘定** > **ベンダー** > **すべてのベンダー** に移動します。 法人 **GBPM** に新しいレコードを作成します。
     9. **名前** を展開して **タイプ** でレコードをフィルターし、**法人** を選択します。 
     10. **Contoso Robotics UK (GBPM)** の顧客レコードを見つけて選択します。
     11. **照合を使用する** を選択してベンダー グループを選択し、このレコードを保存します。
     12. ベンダー レコードで **一般** > **設定** > **会社間** を順に選択します。
     13. **取引関係** タブで **アクティブ** を **はい** に設定します。
     14. ベンダー企業 **GBPM** を選択し、この手順の前半で作成した顧客レコードを **自分の会計レコード** で選択します。

3. **プロジェクト管理と会計パラメーターで会社間の設定を構成します**。 

    1. 法人 **USPM** を選択して **プロジェクトの管理と会計** > **設定** > **プロジェクト管理と会計パラメーター** に移動します。
    2. **会社間** タブで、自動で生成するベンダー請求書と一致する調達カテゴリを選択します。
    3. **既定のカテゴリ** で **会社間リソース** を選択します。
    4. 法人 **GBPM** を選択して **プロジェクトの管理と会計** > **設定** > **プロジェクト管理と会計パラメーター** に移動します。
    5. **会社間** タブで、トランザクション タイプごとにプロジェクトの既定カテゴリを選択します。 会社間トランザクションの請求済みカテゴリが借入法人にのみ存在する場合、プロジェクト カテゴリは税のコンフィギュレーションに使用されます。 会社間トランザクションの売上の計上を選択できます。 発生主義は、トランザクションが貸付法人の Project Operations の統合仕訳帳で転記されたときに発生します。 会社間の請求書を転記すると仕訳が取り消されます。
    6. **リソースの貸付時** グループで **...** > **新規** を選択します。 
    7. グリッドから次の情報を選択します。

          - **借入法人** = **GBPM**
          - **売上計上** = **はい**
          - **既定のタイムシート カテゴリ** = **既定 – 時間**
          - **既定の経費カテゴリ** = **既定 – 経費**

4. **元帳転記設定で会社間コストと売上勘定を設定します**。 会社間の売上勘定は、会社間の顧客請求書を貸付法人に転記する際に貸方転記します。 会社間のコスト勘定は、一致した保留中のベンダー請求書を借入法人に転記する際に借方記入します。 こうした勘定は対応する法人に設定します。 
      
     1. Finance で借入法人 **USPM** を選択します。 
     2. **プロジェクトの管理と会計** > **設定** > **転記** > **元帳転記設定** に移動します。 
     3. **コスト勘定** タブの **元帳勘定タイプ** で **会社間コスト** を選択します。 以下の情報を使用して新規レコードを作成します。
      
        - **貸付法人** = **GBPM**
        - **主勘定** = 会社間コストの主勘定を選択する
        
     4. 貸付法人 **GBPM** を選択します。 
     5. **プロジェクトの管理と会計** > **設定** > **転記** > **元帳転記設定** に移動します。 
     6. **売上勘定** タブの **元帳勘定タイプ** で **会社間売上** を選択します。 以下の情報を使用して新規レコードを作成します。

        - **借入法人** = **USPM**
        - **主勘定** = 会社間売上の主勘定を選択する 

5. **労務の振替価格を設定します**。 会社間の振替価格は Dataverse の Project Operations で設定します。 会社間の請求に対して [労務の原価率](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) と [労務の請求レート](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) を構成します。 会社間の経費トランザクションは振替価格をサポートしていません。 組織間の販売単価は、常にリソース単位原価の値段と同じ値に設定します。

      Contoso Robotics UK の開発者リソース コストは 1 時間あたり 88 GBP です。 Contoso Robotics UK は、このリソースが米国のプロジェクトに取り組んだ時間ごとに Contoso Robotics USA に 120 USD を請求します。 Contoso Robotics USA は、Contoso Robotics UK の開発者リソースが行った作業に対して顧客である Adventure Works に 200 USD を請求します。

      1. Dataverse の Project Operations で **販売** > **価格表** に移動します。 **Contoso Robotics UK の原価率** という名前の新しい原価価格表を作成します。 
      2. 原価価格表に、以下の情報を使用してレコードを作成します。
         - **ロール** = **開発者**
         - **コスト** = **88 GBP**
      3. **設定** > **組織単位** に移動して、この原価価格表を **Contoso Robotics UK** 組織単位に添付します。
      4. **販売** > **価格表** に移動します。 **Contoso Robotics USA の原価率** という名前で原価価格表を作成します。 
      5. 原価価格表に、以下の情報を使用してレコードを作成します。
          - **ロール** = **開発者**
          - **リソース会社** = **Contoso Robotics UK**
          - **コスト** = **120 USD**
      6. **設定** > **組織単位** に移動して **Contoso Robotics USA の原価率** 原価価格表を **Contoso Robotics USA** 組織単位に添付します。
      7. **販売** > **価格表** に移動します。 **Adventure Works の請求レート** という名前で販売価格表を作成します。 
      8. 販売価格表に、以下の情報を使用してレコードを作成します。
          - **ロール** = **開発者**
          - **リソース会社** = **Contoso Robotics UK**
          - **請求レート** = **200 USD**
      9. **販売** > **プロジェクト契約** に移動して、**Adventure Works の請求レート** 価格表をプロジェクト契約の Adventure Works プロジェクト価格表に添付します。