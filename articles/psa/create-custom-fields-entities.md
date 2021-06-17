---
title: カスタム フィールドとエンティティの作成
description: このトピックでは、Power Apps のプラットフォームでオプション セットとエンティティを作成する方法を説明します。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998957"
---
# <a name="create-custom-fields-and-entities"></a>カスタム フィールドとエンティティの作成 

[!include [banner](../includes/psa-now-project-operations.md)]

Power Apps プラットフォームにてカスタム オプション セットまたはエンティティを作成するには以下の手順に従ってください。  
このトピックで扱う手順は Project Service Automation (PSA) のWebインターフェイスを使用して実行する必要があります。

> [!IMPORTANT]
> すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行うことを推奨します。 この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。 必要な変更をすべて行った後、このソリューションを **管理ソリューション** としてエクスポートします。これを別のインスタンスにインポートして価格設定を再利用します。

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>価格設定のディメンションのソリューションにカスタム フィールドとオプション セットを作成します。

価格設定のディメンションは、オプション セット、あるいはエンティティである場合があります。 いずれも価格設定のソリューションにて作成されている必要があります。 この手順では、エンティティ ベースのディメンションと、オプション セット ベースのディメンションを作成する方法について説明します。

### <a name="entity-based-dimensions"></a>エンティティ ベースのディメンション

1. PSA で、**設定** > **ソリューション** をクリックし、続いて **\<your organization name> 価格ディメンション** をダブルクリックします。
2. ソリューション エクスプローラーの左側のナビゲーションパネルで、 **エンティティ** を選択します。
3. **新規** をクリックして、 **スタンダード タイトル** と呼ばれる新しいエンティティを作成します。 その他の必要情報を入力し、 **保存** をクリックします。

> ![スタンダード タイトル エンティティの定義](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>オプション セット ベースのディメンション 
2つのオプション セット ベースのディメンションを作成することができます。 **リソースの作業場所** を使用して、 **ホーム** と **オンサイト** の各作業場所の価格を追跡します。 **リソースの作業時間** に **Regular** and **Overtime** の値を使用して、作業完了時の利幅を適用します。


1. PSAで、**設定** > **ソリューション** をクリックし、続いて **\<your organization name> 価格ディメンション** をダブルクリックします。 
2. ソリューション エクスプローラーの左側のナビゲーションパネルで、  **オプション セット** を選択します。 
3. **新規** をクリックして新たなオプション セットを作成し、その他の必要な情報を入力し、 **保存** をクリックします。

> ![リソースの作業場所 と呼ばれるオプション セット ベースの 価格設定ディメンション ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![リソースの作業時間 と呼ばれるオプション セット ベースの 価格設定ディメンション ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>エンティティ ベースのディメンションのデータを作成する

エンティティ ベースのディメンションのデータは手動での作成、あるいは Microsoft Excel にてインポートやサービス呼び出しを使用して作成することが出来ます。 この手順では、エンティティ ベースのディメンションである **スタンダード タイトル** を使用して次の2つのスタンダード タイトルを作成します。 **システム エンジニア** と **シニア システム エンジニア** 。 以下の例に示すように、作成するデータが小さい場合は、標準フォームを使用することができます。

1. PSAで、 **高度な検索** をクリックします。 **スタンダード タイトル** エンティティを選択し、 **結果** をクリックします。 **スタンダード タイトル** エンティティのすべての行が表示されます。
2. **新規** をクリックします。 **名称** フィールドにて 「システムエンジニア」と入力し **保存** をクリックします。
3. フォームを閉じます。 
4. 手順1から3を繰り返し、他のスタンダード タイトル 「シニア システム エンジニア」を作成します。

> ![スタンダード タイトル エンティティ のサンプル データ ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]