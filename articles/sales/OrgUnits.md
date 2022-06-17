---
title: 組織単位
description: この記事では、組織単位の概念と Microsoft Dynamics 365 Project Operations で組織単位を作成および管理する方法について説明します。
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921630"
---
# <a name="organizational-units-overview"></a>組織単位の概要

Microsoft Dynamics 365 Project Operations における *組織単位* は、原価率を持つ請求可能リソースを使用するプロフェッショナル サービス企業の個別のグループまたは部門です。

さまざまな業務領域または業務ラインで技術リソースを採用するプロフェッショナル サービス企業の場合、役割を遂行する業務領域または業務ラインによって、役割を遂行するコストが異なる場合があります。 このシナリオでは、組織単位の概念は、これらの役割に明確なコスト構造を持つ企業の部門で請求可能な役割のセットをグループ化する方法を提供することにより役立ちます。

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Project Operations における組織単位の概念

Project Operations では、組織単位は特定の通貨と特定の原価価格リストを持ちます。

組織単位の通貨は、コストの追跡に使用される主要通貨です。

それぞれの組織単位に 1 つ以上の原価価格リストを添付できます。 Project Operations で組織単位に添付できる価格表には次の制限があります:

- 価格表は、組織単位の通貨である必要があります。
- 価格表は、原価価格表である必要があります。

さらに、Resource エンティティには、組織単位の属性が含まれます。 それぞれのリソースを 1 つの組織単位に割り当てることができます。

### <a name="roles-of-organizational-units"></a>組織単位の役割

組織単位は Project Operations で 2 つの役割を果たします。

- **契約単位** – 営業の獲得、納品、顧客サービスの提供の管理を主に担当する企業グループや部門を表す組織単位。 契約単位は **営業案件**、**見積もり**、**プロジェクト契約**、**プロジェクト** の各ページのヘッダーセクションの **契約単位** フィールドによって識別されます。
- **リソース単位** – リソースが属するまたは割り当てられている組織単位。 この組織単位は、所有する作業指示書 (SOW) とプロジェクトのいくつかの役割にリソースを提供できます。

![契約単位とリソース単位。](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>組織単位に関する FAQ

ここで組織部門に関するよくある質問をいくつか紹介します。

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Project Operations の Organizational Unit エンティティは、Dynamics 365 に既に存在する Organization エンティティとどのように関連しますか?

Dynamics 365 の Organization エンティティは、グローバルな Dynamics 365 インスタンスの名前を表します。 この名前は通常、グローバル企業の名前です。

組織単位エンティティは、グローバル企業のグループや部門を表します。 このグループや部門にはロールのセットとロールのコスト価格リストがあり、それらのロールと価格リストは企業内の他のグループや部門のロールと価格リストとは異なります。

Project Operations がインストールされると、組織に基づいて既定の組織単位が作成されます。 既存のリソースはすべて既定の組織単位に割り当てられます。 新しい Active Directory ユーザーやリソースが Dynamics 365 にインポートされた場合、ユーザー インポート プロセスは Project Operations の既定の組織単位にそれらを割り当てます。

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Organizational Unit エンティティと Business Unit エンティティの違いは何ですか?

Dynamics 365 で部署エンティティはセキュリティ構造です。 ユーザーと部署の関連付けにより、ユーザーがアクセスできるエンティティとエンティティ レコードが決まります。 また、これらのエンティティ レコードに対するユーザーのアクセス許可 (作成、読み取り、書き込み、削除、追加、任意の場所に追加、割り当て、共有) も決定します。

組織単位エンティティは、割り当てられた従業員のコスト率が異なる企業グループや部門を表します。 リソースと組織単位との関連付けにより、プロジェクト エンゲージメントに対するリソースのコストが決まります。

Dynamics 365 の実装時に、部署の階層のセキュリティ承認と、部署へのユーザーの割り当てを最適化します。 通常、同じレコード セットにアクセスするすべてのユーザーを同じ部署に割り当てます。 組織単位は、セキュリティ承認やアクセスに影響しません。

**組織単位とビジネス単位のモデル化における 1 つの潜在的な違いを示す例**

Contoso, Ltd. 社は積極的に Microsoft のテクノロジを実践しています。 直樹と綾乃はどちらも C\# 開発者ですが、綾乃は米国に、直樹はインドにいます。 プロジェクトへの取り組みのほとんどは、Contoso India と Contoso US の両方のリソースを必要とし、Prakash と Tricia はこの業務領域のプロジェクトで同じレベルのセキュリティ アクセスを必要とします。 ところが、Contoso India の開発者のコストは、Contoso US の開発者のコストと大きく異なります。

Dynamics 365 と Project Operations を使用して、このシナリオを設計する最適な方法について説明します。

1. Microsoft のテクノロジ プラクティスを部署として作成し、そこに直樹と綾乃を関連付けます。 この方法により、両方の従業員がその業務分野のプロジェクトに対して、同じレベルのセキュリティ アクセスを持つようにします。 どちらも進捗を確認し、時間、経費、材料用途、タスクの更新を報告できます。
2. 2 つの組織単位を作成して、プロジェクトのコストが正しく反映されるようにします。
3. Tricia を Contoso US に関連付け、Prakash を Contoso India に関連付けます。
4. 適切な原価価格表を両方の組織単位に割り当てます。 このようにして、Prakash と Tricia のプロジェクトに記録されたコストが、Contoso US と Contoso India のコストの差を正確に反映するようにします。

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>組織単位は Dynamics 365 の販売地域に関連していますか。

販売地域と組織単位との間に関連付けや関係はありません。 販売地域は通常、販売が行われる地理的領域です。 販売価格表は、それぞれの販売地域に関連付けることができます。

組織単位は、会社の内部グループや部門であり、他の部門や外部の顧客に販売する一連の役割のコストを追跡します。

**組織単位と営業担当地域のモデル化における 1 つの潜在的な違いを示す例**

Contoso, Ltd. 社には Contoso US と Contoso India の 2 つの開発センターがあります。 これらの 2 つの開発センターでは、リソースのコストが大きく異なります。 Contoso は、ラテン アメリカ、北米、アジア太平洋、西ヨーロッパ、中東など、多くの国際市場で情報技術 (IT) サービスを販売しています。 同じプロジェクトの役割の請求レートは、これらの市場ごとに大きく異なる可能性があります。 Contoso US と Contoso India を組織単位として設定し、それぞれの組織単位に独自の原価価格表を設定する必要があります。 アジア太平洋、ラテン アメリカ、北米、西ヨーロッパ、中東を販売地域として設定し、それぞれの販売地域に独自の販売価格表を設定する必要があります。

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>組織単位と価格表の関連付けに制限があるのはなぜですか。

通常、販売価格はサービスが販売される地理的領域や市場に固有です。 会社の内部部門は、同じタイプのサービスに対して通常は独自の販売価格を設定しません。 ただし、内部部門では雇用する従業員のスキルと事業を展開する地域の労働条件に応じて、売却済商品の原価 (COGS) が異なります。 組織単位は会社の内部部門としてモデル化されるため、原価価格表のみを持つことができます。

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>販売価格表を組織単位に関連付けることができないのはなぜですか?

Project Operations では販売価格表を顧客と営業担当地域に関連付けることができます。 Opportunity、Quote、Project Contract、Project などのトランザクション エンティティは、顧客アカウントや営業担当地域に添付される販売価格表を使用して、プロジェクト エンゲージメントの請求レートと潜在的な収益を決定します。

原価価格表は組織単位に関連付けられます。 Opportunity、Quote、Project Contract、Project などのトランザクション エンティティは、契約単位に添付される原価価格表を使用して、プロジェクト エンゲージメントのコストを決定します。

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Project Operations の組織単位は階層的ですか?

いいえ。 Project Operations の現在のリリースでは組織単位は階層的ではありません。 したがって、次のタスクは実行できません:

- 階層横断的な既定の原価価格を入力するパターンを構成をする。
- 組織単位階層のさまざまなレベルでロールアップした収益やコストを報告する。

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>私たちはコスト センター、部門、請求オフィスの複雑で多層な階層を持つ大規模な多国籍企業です。 現在のバージョンの Project Operations で組織単位の概念をどのように最適に利用できますか?

コスト センター、部門、請求オフィスなど、複雑な階層がある場合は、その階層のリーフ ノードを個別の組織単位として設定します。

典型的な階層を次の例で示します。

**Contoso India**

- SAP の実践

    - 技術コンサルタント
    - 機能コンサルタント

- Microsoftテクノロジの実践

    - 技術コンサルタント
    - 機能コンサルタント

**Contoso US**

- SAP の実践

    - 技術コンサルタント
    - 機能コンサルタント

- Microsoftテクノロジの実践

    - 技術コンサルタント
    - 機能コンサルタント

階層がこの例に類似している場合、以下に示すようにフラット リストとして設定する必要があります:

- Contoso India - SAP の実践 - 技術コンサルタント
- Contoso India - SAP の実践 - 機能コンサルタント
- Contoso India - Microsoft テクノロジの実践、機能コンサルタント
- Contoso India - Microsoft テクノロジの実践、機能コンサルタント
- Contoso US - SAP の実践 - 技術コンサルタント
- Contoso US - SAP の実践 - 機能コンサルタント
- Contoso US - Microsoft テクノロジの実践 - 技術コンサルタント
- Contoso US - Microsoft テクノロジの実践 - 機能コンサルタント

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>私たちは、1 つの部門として運営している小さな専門サービス企業です。 現在のバージョンの Project Operations で組織単位の概念をどのように最適に利用できますか?

会社を 1 つの原価価格表を持つ 1 つの単位として運営している場合、組織単位を設定する必要はありません。 Project Operations をインストールすると、組織と同じ名前を持つ既定の組織単位を 1 つ作成します。 すべてのユーザーがこの組織単位に既定で割り当てられます。 システムが組織単位の選択を必要とする場合、常にこの組織単位が既定で選択されます。

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>見積もりやプロジェクト契約品目からプロジェクトが作成される場合、既定の契約単位は見積もりやプロジェクト契約から取得されます。 Quote や Project Contract などの販売エンティティの前にプロジェクトを作成する場合、既定の契約単位は何ですか?

プロジェクトを独自に作成する場合、プロジェクトの既定の契約単位は、プロジェクトを作成したユーザーに基づきます。 そのユーザーは既定のプロジェクト マネージャーでもあります。 プロジェクトが見積もりやプロジェクト契約などの販売エンティティにマップされる場合、プロジェクトの契約単位は代わりに販売エンティティに基づきます。 この場合には、契約単位が変更された場合のコスト見積もり変更の計算に原価価格表が使用されるため、プロジェクトの見積もりが再計算される場合があります。 販売価格表は、見積もりのプロジェクト価格表と同期するように変更される販売見積もりの計算に使用されます。

プロジェクトがマップされる販売エンティティ (見積もりやプロジェクト契約) の値と同期する必要があるため、プロジェクトの **契約単位** フィールドと **通貨** フィールドは編集がロックされます。

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Project Operations における組織単位の作成と管理

Project Operations で組織単位を作成するには、次の手順に従います。

1. **設定 \> 組織単位** に移動します。
2. **新規** を選択します。
3. **全般** 領域の **名前** フィールドに組織単位の名前を入力します。 次に、必要に応じて他のフィールドを設定します。
4. **保存** を選択してレコードを作成し、引き続き編集できるようにします。
5. **原価価格表** の下で、プラス記号 (**+**) を選択して価格表を追加します。 ここでは、**コスト** コンテキストを持つ価格表のみを追加できます。
6. **名前** フィールドで **検索** ボタンを選択して、組織単位で使用できるようにする価格表を選択します。 必要に応じて、引き続き価格表を追加します。
7. 価格表の追加が完了したら、ページの右下隅にある **保存** を選択します。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
