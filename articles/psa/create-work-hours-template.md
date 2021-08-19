---
title: 作業時間テンプレートの作成
description: このトピックは、Project Service で作業時間テンプレートを作成する方法について説明しています。
author: ruhercul
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
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987397"
---
# <a name="create-a-work-hours-template-project-service"></a>作業時間テンプレートの作成 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

プロジェクトを作成、管理するには、カレンダーのテンプレートをプロジェクトに適用する必要があります。 カレンダーのテンプレートは、次のプロジェクト属性を定義します:

- 開始時間と終了時間を含む作業時間
- 営業日
- 非稼働日などのカレンダーの例外日

プロジェクトに適用されるカレンダーのテンプレートは、組織の設定で定義されたカレンダー テンプレートのコピーです。

> [!NOTE]
> カレンダーのテンプレートを変更しても、その変更はプロジェクトの作業時間には反映されません。 プロジェクトの作業時間を変更するには、新しいテンプレートを適用する必要があります。

組織で使用するカレンダーのテンプレートを作成するには、次の 2 つの重要な要件があります:

- 新規または既存の予約可能なリソースを使用して、テンプレートに適用する作業時間を定義します。
- 新しいカレンダーテンプレートを作成し、そのテンプレートを予約可能なリソースに関連付けます。

**テンプレートの作業時間を定義する**

1. **リソース** \> **リソース** へ移動します。
2. カレンダーのテンプレートで参照する新しいリソースを作成するか、既存のリソースを選択します。
3. リソースの **作業時間** タブを選択し、[リソースの作業時間の設定](/dynamics365/field-service/set-work-hours-resource.md)に記載の手順に従って、カレンダーのルールを設定します。

**新しいカレンダーのテンプレートを作成する**

1. **設定** \> **カレンダーのテンプレート** に移動します。
2. **新規** を選択し、名前、説明、テンプレート リソースを入力します。


> [!NOTE]
> カレンダーのテンプレートでリソースを参照すると、リソースのカレンダーのコピーがカレンダーのテンプレートに関連付けられます。 コピーしたテンプレートの作業時間が変更されても、この変更はカレンダーのテンプレートには反映されません。


### <a name="see-also"></a>関連項目  
 [リソースの設定](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
