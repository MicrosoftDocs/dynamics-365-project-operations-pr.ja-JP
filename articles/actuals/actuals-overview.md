---
title: 実績
description: このトピックでは、Microsoft Dynamics 365 Project Operations における実績の使用方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079258"
---
# <a name="actuals"></a>実績 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

実績とはプロジェクトで完了した作業の量です。 それは、時間と経費の入力、および仕訳入力と請求書の結果として作成されます。

## <a name="journal-lines-and-time-submission"></a>仕訳帳明細行と時間の送信

時間エントリの詳細については、[時間エントリの概要](../time/time-entry-overview.md) を参照してください。

### <a name="time-and-materials"></a>時間と材料

送信された時間エントリが、時間と材料の契約品目にマップされているプロジェクトにリンクされている場合、システムは 2 つの仕訳帳明細行を作成します。1 つはコスト用、もう 1 つは未請求販売用です。

### <a name="fixed-price"></a>固定価格

送信されるプロジェクトの時間エントリが固定価格の契約品目にマップされているプロジェクトにリンクされると、システムによってコストの仕訳帳明細行が 1 つ作成されます。

### <a name="default-pricing"></a>既定の価格

既定の価格を作成するロジックは仕訳帳明細行にあります。 時間エントリのフィールド値が仕訳帳明細行にコピーされます。 これらの値には、トランザクションの日付、プロジェクトがマップされる契約品目、適切な価格表の通貨結果が含まれます。

**ロール** や **組織単位** など既定の価格に影響するフィールドが、仕訳帳明細行の適切な価格を決定するために使用されます。 時間エントリにカスタム フィールドを追加できます。 フィールド値に実績を伝播する場合は、実績エンティティのフィールドを作成して、フィールド マッピングで時間エントリから実績にフィールドをコピーします。

## <a name="journal-lines-and-basic-expense-submission"></a>仕訳帳明細行と基本経費の送信

経費エントリの詳細については、[経費の概要](../expense/expense-overview.md) を参照してください。

### <a name="time-and-materials"></a>時間と材料

送信される基本経費が、時間と材料の契約品目にマップされているプロジェクトにリンクされている場合、システムは 2 つの仕訳帳明細行を作成します。1 つはコスト用、もう 1 つは未請求販売用です。

### <a name="fixed-price"></a>固定価格

送信されるプロジェクトの基本経費エントリが固定価格の契約品目にマップされているプロジェクトにリンクされると、システムによってコストの仕訳帳明細行が 1 つ作成されます。

### <a name="default-pricing"></a>既定の価格

経費の既定価格を入力するためのロジックは、経費カテゴリに基づいています。 取引日、プロジェクトがマップされる契約品目、通貨は、すべて適切な価格表を決定するために使用されます。 ただし、既定で価格自体について入力した金額は原価と販売に関連する経費の仕訳帳明細行に直接設定されます。

経費入力で、単位ごとの既定価格のカテゴリ ベースのエントリは使用できません。

## <a name="use-entry-journals-to-record-costs"></a>仕訳帳を使用してコストを記録する

仕訳帳を使用して、材料、料金、時間、経費、税のトランザクション クラスでコストや収益を記録できます。 仕訳帳は、次の目的で使用できます。

- プロジェクトで材料の実際のコストと売上を記録します。
- トランザクションの実績を別のシステムから Microsoft Dynamics 365 Project Operations に移動します。
- 別のシステムで発生したコストを記録します。 これらのコストには、調達コストまたは下請けコストが含まれる場合があります。

> [!IMPORTANT]
> アプリケーションは、仕訳明細タイプまたは仕訳明細行に入力された関連価格を検証しません。 したがって、実績がプロジェクトに与える会計上の影響を十分に認識しているユーザーのみが、仕訳帳を使用して実績を作成する必要があります。 この仕訳の種類が影響を与えるため、仕訳帳を作成するためのアクセス権を持つユーザーを慎重に選択する必要があります。
## <a name="record-actuals-based-on-project-events"></a>プロジェクト イベントに基づく実績を記録する

Project Operations はプロジェクト中に発生する財務取引を記録します。 これらの取引は 実績 として記録されます。 次の表はプロジェクトが時間と材料のプロジェクトであるか、固定価格のプロジェクトであるか、プリセールス段階にあるか、内部プロジェクトであるかに応じて、作成されるさまざまなタイプの実績を示しています。

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>リソースはプロジェクトの契約単位と同じ組織単位に属します

<table>
<thead>
<tr>
<th rowspan="3">イベント</th>
<th colspan="4">請求可能なプロジェクトまたは販売されたプロジェクト</th>
<th rowspan="3">プリセールス段階のプロジェクト</th>
<th rowspan="3">内部プロジェクト</th>
</tr>
<tr>
<th colspan="2">時間と材料</th>
<th colspan="2">固定価格</th>
</tr>
<tr>
<th>[実績]</th>
<th>取引通貨</th>
<th>固定価格</th>
<th>取引通貨</th>
</tr>
</thead>
<tbody>
<tr>
<td>時間エントリが作成されました。</td>
<td colspan="6">実績エンティティに活動がありません</td>
</tr>
<tr>
<td>時間エントリが送信されました。</td>
<td colspan="6">実績エンティティに活動がありません</td>
</tr>
<tr>
<td rowspan="2">時間が承認され、承認中に請求可能時間の変更や増加はありません。</td>
<td>コストの実績</td>
<td>契約単位の通貨</td>
<td rowspan="2">コストの実績</td>
<td rowspan="2">契約単位の通貨
<td rowspan="2">コストの実績</td>
<td rowspan="2">コストの実績</td>
</tr>
<tr>
<td>未請求の販売実績 – 請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="3">時間が承認され、承認中に請求可能時間が短縮されます。</td>
<td>コストの実績</td>
<td>契約単位の通貨</td>
<td rowspan="3">コストの実績</td>
<td rowspan="3">契約単位の通貨</td>
<td rowspan="3">コストの実績</td>
<td rowspan="3">コストの実績</td>
</tr>
<tr>
<td>未請求の販売実績 – 新しい数量に対して請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>未請求の販売実績 – 差額は請求不可</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="2">請求書が確認され、請求可能時間で変更や増加は発生しません。</td>
<td>未請求の販売取消</td>
<td>プロジェクト契約の通貨</td>
<td rowspan="2">マイルストーンの請求済み売上</td>
<td rowspan="2">プロジェクト契約の通貨</td>
<td rowspan="2">適用なし</td>
<td rowspan="2">適用なし</td>
</tr>
<tr>
<td>請求済み売上</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="3">請求書が確認され、請求可能時間に減少します。</td>
<td>未請求の販売取消</td>
<td>プロジェクト契約の通貨</td>
<td rowspan="3">適用なし</td>
<td rowspan="3">適用なし</td>
<td rowspan="3">適用なし</td>
<td rowspan="3">適用なし</td>
</tr>
<tr>
<td>請求済み売上 – 新しい数量に対して請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>請求済み売上 – 差額は請求不可</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="2">請求書は修正され、請求可能な数量が増えます。</td>
<td>請求済み売上 – 取消</td>
<td>プロジェクト契約の通貨</td>
<td rowspan="5">
<ul>
<li>マイルストーンの請求された販売の取り消し</li>
<li>マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</li>
</ul>
</td>
<td rowspan="5">プロジェクト契約の通貨</td>
<td rowspan="5">適用なし</td>
<td rowspan="5">適用なし</td>
</tr>
<tr>
<td>請求済み売上</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="3">請求書は修正され、請求可能な数量が減少します。</td>
<td>請求済み売上 – 取消</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>新しい数量の請求済み売上</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>未請求売上 – 差額は請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>リソースがプロジェクトの契約単位と異なる組織単位に属します

<table>
<thead>
<tr>
<th rowspan="3">イベント</th>
<th colspan="4">請求可能なプロジェクトまたは販売されたプロジェクト</th>
<th rowspan="3">プリセールス段階のプロジェクト</th>
<th rowspan="3">内部プロジェクト</th>
</tr>
<tr>
<th colspan="2">時間と材料</th>
<th colspan="2">固定価格</th>
</tr>
<tr>
<th>[実績]</th>
<th>取引通貨</th>
<th>固定価格</th>
<th>取引通貨</th>
</tr>
</thead>
<tbody>
<tr>
<td>時間エントリが作成されました。</td>
<td colspan="6">実績エンティティに活動がありません</td>
</tr>
<tr>
<td>時間エントリが送信されました。</td>
<td colspan="6">実績エンティティに活動がありません</td>
</tr>
<tr>
<td rowspan="4">時間が承認され、承認中に請求可能時間の変更や増加はありません。</td>
<td>コストの実績</td>
<td>契約単位の通貨</td>
<td rowspan="4">コストの実績</td>
<td rowspan="4">契約単位の通貨</td>
<td rowspan="4">コストの実績</td>
<td rowspan="4">コストの実績</td>
</tr>
<tr>
<td>未請求の販売実績 – 請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>リソース単位原価</td>
<td>リソース単位原価</td>
</tr>
<tr>
<td>組織間営業</td>
<td>契約単位の通貨</td>
</tr>
<tr>
<td rowspan="5">時間が承認され、承認中に請求可能時間が短縮されます。</td>
<td>コストの実績</td>
<td>契約単位の通貨</td>
<td rowspan="5">コストの実績</td>
<td rowspan="5">契約単位の通貨</td>
<td rowspan="5">コストの実績</td>
<td rowspan="5">コストの実績</td>
</tr>
<tr>
<td>リソース単位原価</td>
<td>リソース単位原価</td>
</tr>
<tr>
<td>組織間営業</td>
<td>契約単位の通貨</td>
</tr>
<tr>
<td>未請求の販売実績 – 新しい数量に対して請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>未請求の販売実績 – 差額は請求不可</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="2">請求書が確認され、請求可能時間で変更や増加は発生しません。</td>
<td>未請求の販売取消</td>
<td>プロジェクト契約の通貨</td>
<td rowspan="2">マイルストーンの請求済み売上</td>
<td rowspan="2">プロジェクト契約の通貨</td>
<td rowspan="2">適用なし</td>
<td rowspan="2">適用なし</td>
</tr>
<tr>
<td>請求済み売上</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="3">請求書が確認され、請求可能時間に減少します。</td>
<td>未請求の販売取消</td>
<td>プロジェクト契約の通貨</td>
<td rowspan="3">適用なし</td>
<td rowspan="3">適用なし</td>
<td rowspan="3">適用なし</td>
<td rowspan="3">適用なし</td>
</tr>
<tr>
<td>請求済み売上 – 新しい数量に対して請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>請求済み売上 – 差額は請求不可</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="2">請求書は修正され、請求可能な数量が増えます。</td>
<td>請求済み売上 – 取消</td>
<td>プロジェクト契約の通貨</td>
<td rowspan="5">
<ul>
<li>マイルストーンの請求された販売の取り消し</li>
<li>マイルストーンのステータスを<strong>請求済み</strong>から<strong>請求準備完了</strong>に変更</li>
</ul>
</td>
<td rowspan="5">プロジェクト契約の通貨</td>
<td rowspan="5">適用なし</td>
<td rowspan="5">適用なし</td>
</tr>
<tr>
<td>請求済み売上</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td rowspan="3">請求書は修正され、請求可能な数量が減少します。</td>
<td>請求済み売上 – 取消</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>新しい数量の請求済み売上</td>
<td>プロジェクト契約の通貨</td>
</tr>
<tr>
<td>未請求売上 – 差額は請求可能</td>
<td>プロジェクト契約の通貨</td>
</tr>
</tbody>
</table>
