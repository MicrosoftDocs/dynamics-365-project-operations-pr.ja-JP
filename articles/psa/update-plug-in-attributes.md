---
title: プラグインの属性を更新して新しい価格ディメンションを含める
description: このトピックでは、価格ディメンションのプラグイン属性の更新について説明します。
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079351"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>プラグインの属性を更新して新しい価格ディメンションを含める

> [!NOTE]
> Project Service Automation (PSA) の見積もりおよび契約機能を使用していない場合、このトピックはスキップできます。

このトピックでは、ユーザーが次のトピックの手順を完了していることを前提としています。[カスタム フィールドおよびエンティティを作成する](create-custom-fields-entities.md)、[価格設定とトランザクション エンティティにカスタム フィールドを追加する](field-references.md)、[カスタム フィールドを価格ディメンションとしてセットアップする](set-up-pricing-dimensions.md) 次に、これらの手順を完了していない場合は、戻ってこれらを完了してから、このトピックに戻ってください。

プロジェクト見積依頼明細用に見積依頼明細行の詳細を **見積依頼明細行** のページで作成するとき、システムがバックグラウンドで 2 つの見積もり明細行を作成します -- 1 つは見積もりコスト側用で、もう 1 つは営業側用の明細行です。 これは、プロジェクト契約品目の場合も同様です。

数量への変更を行うとき、またはコスト側のフィールドを変更するとき、変更が営業側に伝播されます。 これは、可能です。次のプラグインでは、価格ディメンションに対する変更を行った後、再登録する必要があるためです。

- PreOperationContractLineDetailUpdate - 更新 **msdyn_orderlinetransaction** 。
- PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction** 。

次の手順では、プラグインの登録に関して説明します。

1. **PluginRegistrationTool** 開いて、オンライン インスタンスに接続します。
2. **検索** をクリックし、更新するプラグインを検索します。

 ![検索ツリーのスクリーンショット](media/PRT-1.png)

3. プラグインが見つかったらそれを選択し、 **メイン フォームの選択** をクリックします。

4. 更新すべきプラグインのステップを選んで右クリックし、 **更新** を選択します。

 ![更新するプラグインのスクリーンショット](media/PRT-2.png)
 
5. [更新] ウィンドウで、フィルター属性の省略記号 ( **...** ) をクリックします。

 ![既存のステップ構成情報を更新するときのスクリーンショット](media/PRT-3.png)
 
6. 価格属性チェック ボックスをオンにします。

 ![価格属性のチェック ボックスの選択が表示されたスクリーン ショット](media/PRT-4.png)

7. **OK** をクリックして ページを閉じ、 **ステップの更新** を選択します。

 ![「手順の更新」 ボタンを示すスクリーン ショット](media/PRT-5.png)
 
8. この第 2 プラグイン、 **PreOperationQuoteLineDetail - msdyn_quotelinetransaction の更新** のプロセスを繰り返します。

9. プラグイン登録ツールを閉じます。

