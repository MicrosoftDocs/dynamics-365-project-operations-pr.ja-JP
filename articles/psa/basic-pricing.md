---
title: プロジェクトの価格設定
description: このトピックでは、Dynamics 365 Project Service Automation での価格設定の仕組みについて説明します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: b319f9be9fd72ac99ce6012b6baffde812e3077d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079465"
---
# <a name="project-pricing"></a>プロジェクトの価格設定 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation は Dynamics 365 Sales の価格表エンティティを拡張します。 

## <a name="key-entities"></a>主要なエンティティ

価格表には、次の 4 つの異なるエンティティによって提供される情報が含まれます。

- **価格表** - このエンティティには、コンテキスト、通貨、日付の有効性、および価格設定時間の時間単位に関する情報が格納されます。 コンテキストは、価格表が原価率または販売率のどちらを表すかを示します。 
- **通貨** - このエンティティには、価格表の価格の通貨が格納されます。 
- **日付** - このエンティティは、システムがトランザクションの既定の価格を入力しようとするときに使用されます。 PSA の価格設定は、トランザクションの日付などの日付有効性を持つ価格表を選択します。 PSA の価格設定が、関連する見積もり、契約、または組織単位に添付されているトランザクションの日付に有効な複数の価格表を見つけた場合、価格は既定にはなりません。 
- **時間** - このエンティティは、日単位または時間単位など、価格が表現される時間の単位を格納します。 

価格表エンティティには、価格を格納する次の 3 つの関連テーブルがあります。

  - **ロール価格** - このテーブルは、ロールと組織単位の値の組み合わせのレートを格納し、人的リソースのロールベースの価格を設定するために使用されます。
  - **トランザクション カテゴリ価格** - このテーブルはトランザクション カテゴリごとに価格を格納し、経費カテゴリの価格を設定するために使用されます。
  - **価格表品目** - このテーブルには、カタログ製品の価格が格納されます。

> ![価格表を使用した価格の設定](media/basic-guide-12.png)
 
価格表は価格カードです。 価格カードは、価格表エンティティと、ロール価格、トランザクション カテゴリ価格、および価格表品目テーブルの関連行の組み合わせです。

## <a name="resource-roles"></a>リソースのロール

*リソースのロール* という用語は、プロジェクトで特定のタスク セットを実行するために必要なスキル、コンピテンシー、および認定資格のセットを指します。

人的リソース時間は、通常、特定のプロジェクトでリソースが果たすロールに基づいて見積もりされます。 人的リソース時間については、PSA はリソースのロールに基づいた原価計算と請求をサポートしています。 時間は、 **時間** 出荷単位一覧の任意の単位で価格設定できます。

PSA がインストールされると、 **時間** 出荷単位一覧が作成されます。 既定の出荷単位は **時** です。 **時間** 出荷単位一覧または **時** 出荷単位の属性を削除、名称変更、または編集することはできません。 ただし、 **時間** 出荷単位一覧に他の出荷単位を追加できます。 **時間** 出荷単位一覧または **時** 出荷単位のどちらかを削除しようとすると、PSA ビジネス ロジックでエラーが発生する可能性があります。

> ![ロールによる価格の設定](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>トランザクション カテゴリと経費カテゴリ

通常、プロジェクト コンサルタントに発生する旅費およびその他の経費は、顧客に請求されます。 PSA は、価格表を使用することにより、経費カテゴリの価格設定をサポートしています。 経費カテゴリの例には、航空運賃、ホテル、およびレンタカーがあります。 各価格表の経費の行では、特定の経費カテゴリの価格を指定します。 経費カテゴリの価格設定について、PSA は次の 3 つの価格設定方法をサポートしています。

- **コスト** - 経費コストは顧客に請求され、利幅は適用されません。
- **利幅率** - 実際のコストに対する割合が顧客に請求されます。 
- **出荷単位ごとの価格** - 請求価格は、経費カテゴリの各出荷単位に設定されます。 顧客に請求される金額は、コンサルタントが報告する経費の出荷単位の数に基づいて計算されます。 マイレージは、出荷単位ごとの価格設定方法を使用します。 たとえば、マイレージの経費カテゴリは、1 日あたり 30 米ドル (USD) または 1 マイルあたり 2 米ドルに設定できます。 コンサルタントがプロジェクトのマイレージを報告する場合、請求額はコンサルタントが報告したマイル数に基づいて計算されます。

> ![経費カテゴリに関する価格の設定](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>プロジェクトの販売価格設定と上書き

プロジェクトの見積もりと契約において、プロジェクトの価格表には製品の価格表とは異なる上書きパターンがあります。 製品カタログ ベースの見積依頼明細行では、各見積依頼明細行が正確に 1 つのカタログ品目を指すため、見積依頼明細行で価格をロールおよびカテゴリに直接上書きできます。 ただし、プロジェクト ベースの見積依頼明細行では、見積依頼明細行で価格をロールおよびカテゴリに直接上書きすることはできません。 2 つの異なる上書きパターンをサポートするために、PSA は新しい価格表の関連付けであるプロジェクト価格表を導入しました。

> [!NOTE]
> 価格設定を上書きする場合の 2 つの動作には違いがあるため、プロジェクト リソース用とカタログ品目用にそれぞれ価格表を持つことをお勧めします。

次の各エンティティには、プロジェクトの価格設定用に 1 つ以上の関連する販売価格表を持つことができます。

- 顧客 (アカウント) 
- 営業案件 
- 見積もり 
- プロジェクト契約

これらのエンティティと価格表の関連付けは、プロジェクト価格表によって示されます。 顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、1 つ以上の価格表を関連付けることができます。

既定のプロジェクト価格表は、顧客レコードに自動的に入力されません。 ただし、顧客レコードに手動でプロジェクト価格表を添付できます。 それでも、顧客とのカスタムの価格設定について合意がある場合にのみ、手動でプロジェクト価格表を添付してください。 

プロジェクト価格表が営業エンティティに添付されると、PSA は次の情報を検証します。

- 価格表が **営業** コンテキストを持っている。 
- 価格表の通貨が顧客の通貨と一致している。 

プロジェクト契約では、PSA は次の優先順位を使用して、関連するプロジェクト価格表を自動的に設定します。

1. 見積もり
2. 営業案件
3. Customer 
4. PSA 用のグローバル設定

プロジェクト価格表が既定で入力されると、PSA は通貨が顧客の通貨と一致すること、および入力された既定の価格表が **営業** コンテキストを持っていることを検証します。

顧客、営業案件、見積もり、およびプロジェクト契約の営業エンティティには、複数のプロジェクト価格表を関連付けることができます。 この機能は、長期にわたるプロジェクト契約の日付固有の既定の価格をサポートします。この場合、インフレによって発生する価格更新に対応するため、アカウントに複数の価格表が必要になる場合があります。 ただし、顧客、営業案件、見積もり、またはプロジェクト契約のエンティティに関連付けられている価格表の日付の有効性が重複していると、既定の価格が正しくない場合があります。 そのため、日付の有効性が重複しているプロジェクト価格表がそれらのエンティティに関連付けられていないことを確認する必要があります。

### <a name="deal-specific-price-overrides"></a>取引固有の価格の上書き

PSA では、見積もりやプロジェクト契約に既定で入力されるプロジェクト価格表で選択した価格の取引固有の上書きを作成できます。

既定では、プロジェクト契約は、直接リンクの代わりにマスター販売価格表のコピーを常に取得します。 この動作は、マスター価格表が変更された場合に、作業指示書 (SOW) についての顧客との価格の合意が変更されないことを保証するのに役立ちます。

ただし、見積もりではマスター価格表を使用できます。 または、マスター価格表をコピーして編集し、その見積もりのみに適用されるカスタム価格表を作成できます。 見積もりに固有の新しい価格表を作成するには、 **見積もり** ページで **カスタム価格の作成** を選択します。 取引固有のプロジェクト価格表は見積もりからのみアクセスできます。 

カスタム プロジェクト価格表を作成すると、価格表のプロジェクト コンポーネントのみがコピーされます。 つまり、見積もりに添付されている既存のプロジェクト価格表のコピーとして作成された新しい価格表であり、この新しい価格表には関連するロール価格とトランザクション カテゴリ価格のみが含まれます。

> ![プロジェクト契約のカスタム価格の表示と設定](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>コストの追跡

PSA は、プロジェクトでの人的リソース時間の使用についてのコストを追跡します。 また、旅費など、プロジェクト中に発生した他の経費のコストも追跡します。

請求レートと同様に、人的リソースのコスト レートも価格表を使用して設定されます。 原価表と販売価格表の動作の主な違いは次のとおりです。

- リソースのコスト レートは、特定のプロジェクト、契約、または見積もりで上書きすることはできません。 ただし、取引の性質に固有の変更が行われた場合、取引ごとに請求レートが上書きされる可能性があります。 

- 次の順序は、原価価格表を解決するために使用されます。

    1. 組織単位に添付されている原価価格表。
    2. Project Service のパラメーターに添付されている原価価格表。 多くの異なる通貨の原価価格表を Project Service のパラメーターに添付できるため、PSA はプロジェクト、契約、または見積もりの契約組織単位の通貨と原価価格表の通貨の間で通貨照合を行います。
    3. 経費については、コスト価格設定方法およびコストに対する利幅価格設定方法は原価価格表には適用されません。 これらの価格設定方法を原価価格表の行で使用してトランザクション カテゴリ コストを設定しても、システムはそれらを無視し、既定の原価価格は入力されません。