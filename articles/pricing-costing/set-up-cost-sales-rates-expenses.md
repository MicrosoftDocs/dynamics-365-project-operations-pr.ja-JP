---
title: 経費の原価率と販売率を設定する
description: このトピックは、トランザクションと経費のカテゴリのためのコストと販売率を設定する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079187"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>経費の原価率と販売率を設定する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations で、トランザクション カテゴリのコストと販売価格を設定できます。 コストと販売価格は経費用に設計されているため、これらを含む各トランザクション カテゴリも経費カテゴリとして設定する必要があります。 この設定により、ダウンストリーム機能の精度が保証されます。 トランザクション カテゴリのコストと販売価格は、1 つの通貨でのみ表示できます。これは、価格表ヘッダーの通貨である必要があります。

トランザクション カテゴリのコストと販売率を設定するには、次の手順を実行します。 

1. 価格表ヘッダーに基づいて価格表を作成します。 
2. **カテゴリ価格** のサブグリッド メニューで、 **+ 新規カテゴリ価格** を選択します。 
3. **クイック作成** ページで、新しい価格を作成する取引カテゴリと単位を入力します。

次のテーブルは、 **一般** タブのフィールドと販売または原価価格表でカテゴリ価格を作成する際に留意すべき、 **クイック作成** ページののカテゴリ価格の明細行を一覧表示しています。

| フィールド | 場所 | 関連性、目的、およびガイダンス | 下位への影響 |
| --- | --- | --- | --- |
| トランザクション カテゴリ | **全般** タブと **簡易作成** ページ | 販売価格または原価価格を作成するトランザクション カテゴリを選択します。 | 受信見積もりまたは経費の実績のトランザクション カテゴリがこの明細行と照合され、トランザクション カテゴリのコストまたは販売率が規定値設定されています。 |
| 出荷単位スケジュール | **全般** タブと **簡易作成** ページ | 単位スケジュールは、トランザクション カテゴリの単位スケジュールから規定値設定されます。 | このフィールドから下位への影響はありません。 |
| 単位 | **全般** タブと **簡易作成** ページ | 料金を設定する単位を選択します。 | 受信見積もりまたは実績の単位は、この明細行の単位と照合され、経費見積もりまたは実績のレートが規定値設定になります。 |
| 価格設定方法 | **全般** タブと **簡易作成** ページ | **価格設定方法** フィールドの可能性のある値は、 **単位当たりの価格** 、 **コストで** 、 **コストにマークアップ** になります。 | 価格設定時に、 **単位当たりの価格** を選択すると、 **パーセント** フィールドをカテゴリ価格明細行にロックします。 **コストで** が選択されている場合、 **価格** フィールドと **パーセント** フィールドは販売価格リストでロックされています。 **コストにマークアップ** を選択すると、販売価格リストの **価格** フィールドをロックします。 経費のための実際の着信回線では、 **コストで** または **コストにマークアップ** 価格設定方法では、対応する未請求の販売ラインに、実際原価の価格に等しい価格が割り当てられるか、価格に対するマークアップとして計算されます。 |
| 料金 | **全般** タブと **簡易作成** ページ | トランザクション カテゴリとユニットの組み合わせのユニットあたりのレートを設定します。 たとえば、マイレージのレートは 1 マイルあたり 10 米国ドル、キロメートルあたり 8 米国ドルです。 | このマイレージ レートは、経費トランザクション クラスの受信見積もりまたは実際の行の単価またはコストあたりの規定レートになります。|
| パーセント | **全般** タブと **簡易作成** ページ | トランザクション カテゴリとユニットの組み合わせに対するコストに対する率を設定します。 たとえば、航空運賃の販売率は、発生した航空運賃の費用よりも 10％ 高くする必要があります。 | このコストに対する率は、選択した価格の計算方法が **コストにマークアップ** の場合にのみ販売価格表に適用されます。 |
| 通貨 | **全般** タブと **簡易作成** ページ | 規定では、この値は価格表のヘッダーにある通貨から取得されます。 トランザクション カテゴリの価格設定の場合、通貨を上書きすることはできません。 | この通貨は、コストと売上の経費トランザクション クラスの実際の入荷ラインの単価が規定値になります。 |

## <a name="pricing-methods-for-expenses"></a>経費の価格設定方法

経費価格設定のコンテキストにのみ関連するカテゴリ価格を設定する場合は、次の 3 つの価格設定方法のいずれかを使用できます。

- **出荷単位ごとの価格**
- **コスト**
- **コストにマークアップ**

### <a name="price-per-unit"></a>出荷単位ごとの価格
販売価格リストにリンクされているカテゴリ価格ラインでこの価格設定方法を選択すると、見積もりと実際の両方で、カテゴリと単位の組み合わせの価格が規定値になります。 見積もりとは、経費に対するプロジェクト見積もり項目、見積もり項目の詳細、および経費に対する契約品目の詳細を指します。

### <a name="at-cost"></a>コスト
販売価格表にリンクされているカテゴリ価格明細行でこの価格設定方法を選択すると、実際の経費のみで、カテゴリと単位の組み合わせの価格が規定値になります。 たとえば、経費トランザクション クラスの未請求の販売実績。 この単価は、その費用の実績原価の単価から、未請求売上実績に設定されます。 コストに基づく価格の規定値設定は、費用のプロジェクト見積もり、または費用の見積明細と契約明細の詳細では行われません。

### <a name="markup-over-cost"></a>コストにマークアップ
販売価格表にリンクされているカテゴリ価格明細行でこの価格設定方法を選択すると、実際の経費のみで、カテゴリと単位の組み合わせの価格が規定値になります。 たとえば、経費トランザクション クラスの未請求の販売実績。 この単価は、未請求の実際の売上に設定され、定義されたマークアップ率が適用された後、その費用の実際のコストの単価から計算された値に設定されます。 コストに基づく価格の規定値設定は、費用のプロジェクト見積もり、または費用の見積明細と契約明細の詳細では行われません。