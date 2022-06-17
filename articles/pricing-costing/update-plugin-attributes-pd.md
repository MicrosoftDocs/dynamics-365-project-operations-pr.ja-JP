---
title: 新しい価格ディメンションでプラグイン属性を更新する
description: この記事では、価格ディメンションのプラグイン属性の更新方法について説明します。
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920020"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>新しい価格ディメンションでプラグイン属性を更新する

この記事では、価格ディメンションのプラグイン属性の更新方法について説明します。

> [!NOTE]
> この記事は、Dynamics 365 Project Operations の見積もりおよび契約機能にのみ適用されます。

## <a name="prerequisites"></a>前提条件
この記事の手順を完了する前に、次の記事の手順を完了している必要があります。

  - [カスタム フィールドとエンティティの作成](create-custom-fields-entities-pricing-dimensions.md) 
  - [カスタム フィールドを価格設定およびトランザクション エンティティに追加する](add-custom-fields-price-setup-transactional-entities.md)
  - [価格ディメンションとしてカスタム フィールドを設定します](set-up-custom-fields-pricing-dimensions.md)。 
  
次に、これらの手順を完了していない場合は、戻ってこれらを完了してから、この記事に戻ってください。

## <a name="register-a-plug-in"></a>プラグインの登録
プロジェクト見積明細行の **見積依頼明細行** ページで見積依頼明細行詳細を作成すると、システムは見積明細行を 2 件作成します。 1 件は見積もりのコスト側で、もう 1 件は営業側です。 これは、プロジェクト契約品目の場合も同様です。

数量への変更を行うとき、またはコスト側のフィールドを変更するとき、この変更が営業側に作成されます。 これが可能なのは、Quotelinedetail エンティティと契約品目詳細エンティティの PreOperation プラグインが、トランザクションでコスト側の特定属性が営業側に接続されているためです。 営業側の価格ディメンション値を変更し、コスト側でも変更する場合は、価格ディメンションの変更後に次のプラグインを再登録する必要があります。

これらは更新と再登録に使用するプラグインです。

- PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction の更新**
- PreOperationQuoteLineDetailUpdate - **msdyn_quotelinetransaction の更新**

プラグインの更新と再登録には、次の手順を実行します。

1. **PluginRegistrationTool** を開いて Project Operations の Dataverse 環境に接続します。
2. **検索** を選択して、更新するプラグイン名の最初の数文字を入力します。
3. プラグインが見つかったら選択し、**メイン フォームの選択** を選択します。
4. **Update msdyn_orderlinetransaction** ステップを選んで右クリックし、**更新** を選択します。
5. **更新** ダイアログ ページで、フィルタリング属性の省略記号 (**...**) を選択します。
6. フィルタリング属性ウィンドウが開き、エンティティが含むすべての属性と価格ディメンションの一覧が表示されます。 価格ディメンション属性のチェックボックスを選択します。
7. **OK** を選択してページを閉じ、**ステップの更新** を選択します。
8. 2 番目のプラグイン **PreOperationQuoteLineDetail** に対して手順 2 から 7 を繰り返します。 このプラグインでは **msdyn_quotelinetransaction の更新** ステップを更新する必要があります。
9. **PluginRegistrationTool** を閉じます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]