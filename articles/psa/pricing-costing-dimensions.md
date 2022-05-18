---
title: 価格とコストのディメンションのホーム ページ
description: このトピックでは、価格ディメンションの概要を説明します。
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7dbee508cea074a8c443506d280a1b52eb698202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593618"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>価格とコストのディメンションのホーム ページ

[!include [banner](../includes/psa-now-project-operations.md)]

プロジェクト ベースの組織で労働の価格とコストを設定するために使用されるディメンションは、次の属性の影響を受けます:

- 自分の経験、役割、または地理的に類似した仕事をしている人々
- 複雑さや時間帯に類似して行われる作業

これらの作業属性の典型的な性質と作業を実行するために必要な人員を考慮すると、Project Service Automation で使用できる価格ディメンション値には 2 つのタイプがあります: 

- **オプション セット** - 一連の値の固定リストである属性。
- **エンティティ ベースの値** - 有限であるが時間の経過とともに変化する可能性のあるさまざまな値のセットを持つことができる属性。

## <a name="pricing-dimensions"></a>価格ディメンション

PSAには、価格ディメンションの既定セットが付属しています。 これらを表示するには、 **Project Service** > **パラメーター** に移動します。 パラメーター レコードの **金額ベースの価格ディメンション** タブで、ロール **msdyn_resourcecategory** と リソース組織単位 **msdyn_organizationalunit** のフィールド **営業に適用可能** と **コストに適用可能** が **はい** に設定されていることを確認します。 これによって各ロールや組織単位の組み合わせの価格とコストを設定することができます。

!["営業に適用可能" が強調表示された Project Service パラメーターのスクリーンショット。](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> PSAのバージョン 3 よりも前に、価格ディメンションとしてロールと組織単位の標準フィールドを使用していた場合、注目すべき変更はありません。 通常どおり Project Service を引き続き使用できます。 

追加の属性を使用してリソースの価格やコストを設定する必要がある場合は、カスタマイズしたフィールド、エンティティおよびディメンションを作成できます。 詳細については、以下のトピックを参照してください。ただし、次に示す順序で手順を実行する必要があることに注意してください:

- [カスタム フィールドとエンティティの作成](create-custom-fields-entities.md)
- [価格設定とトランザクション エンティティに対してユーザー定義フィールドを追加する](field-references.md)
- [価格ディメンションとしてカスタム フィールドを設定する](set-up-pricing-dimensions.md)
- [プラグインの属性を更新して新しい価格ディメンションを含める](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>人的リソース時間の価格設定
組織が人的リソース時間をどのように価格設定するかは、多くの場合、組織の収益性に直接影響する重要な戦略的考慮事項です。 組織が人的リソース時間の請求レートとコスト レートの設定方法を決定する準備ができたら、財務チームおよび実務担当者と連携します。

価格設定に関する他の検討事項には、現在価格ディメンションではないが組織の価格ディメンションとして適用されるフィールドまたはエンティティを再利用するかどうかがあります。 **トランザクション カテゴリ** (**msdyn_transactioncategory**) と **予約可能リソース** (**bookableresource**) のようなフィールドが候補のディメンションの例です。 

価格ディメンションをテーブルにするかオプション セットにするかを検討する必要があります。 10 または 12 を超えるディメンションの値への変更が予測され、これらの値に追加の属性が必要な場合は、オプション セットではなくエンティティを作成します。 ほとんどのビジネス ユーザーは、テーブルに新しい行を追加できますが、値の追加や削除などのオプション セットを管理するには、管理者または開発者が必要です。

次の例にリソースが属するロールやリソースの組織単位に基づいて設定される請求レートを示します。 通常、コスト レートは従業員の給与範囲および所属する組織単位に基づきます。 この例では、請求レートとコストレートのテーブルは次のようになります。

**サンプル請求レート**

| ロール        | 組織単位    |出荷単位      |価格      |[通貨]  |
| ------------|-------------|----------|----------:|----------|
| 開発者   | Contoso US  |Hour | 200|USD     |
| 開発者   | Contoso India社 |Hour|   112|USD     |


**サンプル コスト レート**

| 給与範囲     | 組織単位    |出荷単位      |価格      |[通貨]  |
| ----------------|-------------|----------|----------:|----------|
| 自分の会社_Band1 | Contoso US  |Hour | 145|USD     |
| 自分の会社_Band2 | Contoso India社 |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
