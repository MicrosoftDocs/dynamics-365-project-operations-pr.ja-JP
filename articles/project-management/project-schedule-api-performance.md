---
title: プロジェクト スケジュール API のパフォーマンス
description: このトピックでは、プロジェクト スケジュール API のパフォーマンスにおけるベンチマークに関する情報と、最適に使用するためのベストプラクティスを紹介します。
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750608"
---
# <a name="project-schedule-api-performance"></a>プロジェクト スケジュール API のパフォーマンス

_**適用対象:** リソース/非在庫ベースのシナリオの Project Operations、ライト展開 - 見積もり請求の取引、Project for the Web_

このトピックでは、プロジェクト スケジュールのアプリケーション プログラミング インターフェース (API) のパフォーマンス ベンチマークに関する情報と、使用方法を最適化するためのベストプラクティスについて説明します。

## <a name="project-scheduling-service"></a>プロジェクト スケジュール サービス
プロジェクト スケジュール サービスは、Microsoft Azure で実行されるマルチテナント サービスです。 ユーザーがプロジェクトに取り組む際に、高速で流動的なエクスペリエンスを提供することで、インタラクションの向上が実現できるように設計されています。 この改善は、変更要求を受け付けて処理し、その結果をただちに返すことで実現しています。 このサービスは、非同期的に Dataverse に永続化し、ユーザーによるその他操作の実行を妨げることはありません。

プロジェクト スケジュール API は、プロジェクト スケジュール サービスに依存しており、このトピックの後のセクションで詳細を説明するリクエストを実行します。

プロジェクト スケジュール API は、次の WBS (作業分解構造) エンティティと連携するように設計されています:

  - Project
  - プロジェクト タスク
  - プロジェクト タスクの依存関係
  - プロジェクト チーム メンバー
  - リソース割り当て
  
既成のフィールドとカスタム フィールドの両方がサポートされています。 特に明記されていない限り、作成、更新、削除などの一般的な操作がサポートされています。 詳細については、[プロジェクト スケジュール API を使用して、スケジュール設定エンティティで操作を行う](schedule-api-preview.md)を参照してください。

プロジェクト スケジュール API の一部として、作業単位パターンが追加されました。 このパターンは OperationSet と呼ばれ、1 つのトランザクションで複数のリクエストを処理する必要がある場合に使用できます。

次の図は、この機能を使用した場合のパートナーのフローを示しています。

![Dataverse とプロジェクト スケジューリング サービスのフロー。](./media/dataverse-project-scheduling-service-flow.png)

**手順 1**: クライアントは、Dataverse の Open Data Protocol (OData) エンドポイントに API を呼び出し、OperationSet を作成します。

**手順2**: 新しい OperationSet が作成されると、**OperationSetId** の値が返されます。

**手順 3**: クライアントは **OperationSetId** の値を使って、別のプロジェクト スケジュール API の要求を行います。 その結果、スケジューリング エンティティの作成、更新、削除の要求が行われます。 この要求がされるた場合、メタデータの検証が行われます。 検証に失敗した場合は要求が終了し、エラーが返されます。

**手順 4a 〜 4c**: これらの手順は、ACCEPT フェーズを表します。 クライアントが **ExecuteOperationSetV1** API を呼び出すと、プロジェクト スケジューリング サービスにすべての変更内容が一括して送信されます。 プロジェクト スケジューリング サービスは、バッチ内の要求に対して独自の検証を実行します。 検証に失敗した場合は、バッチが元に戻され、呼び出し元に例外が返されます。 プロジェクト スケジューリング サービスでバッチが正常に受け入れられると、OperationSet の状態が更新され、プロジェクト スケジューリング サービスで処理中であることが反映されます。

**手順 5**: この手順は、PERSIST フェーズを表します。 プロジェクト スケジューリング サービスは、非同期的に、トランザクションで Dataverse にバッチを書き込みます。 書き込み操作が成功した場合、OperationSet に **完了** マークが付きます。 エラーが発生すると、トランザクションとバッチがロールバックされ、OperationSet は **失敗** と判定されます。

## <a name="performance-methodology"></a>パフォーマンスの方法論
実行時間は、**ExecuteOperationSetV1** API を呼び出してから、プロジェクト スケジューリング サービスが Dataverse への書き込みを終了するまでの時間と定義されています。 すべての操作は合計 2,200 回実行され、P99 の実行時間を測定した結果が報告されます。 単一レコードと一括操作が測定されます。

単一レコード操作の場合、OperationSet には 1 つのリクエストが含まれます。 一括操作の場合は、20 件、50 件、100 件の要求が入っています。 それぞれの一括のサイズは別々に報告されます。

これらの操作は、北米でデプロイされている UR15 Project Operations Lite 上で行われています。

## <a name="results"></a>結果​​
### <a name="create-operations"></a>操作の作成
#### <a name="single-record-create-operations"></a>単一レコードの作成操作
次の表では、単一のレコードを作成する場合の実行時間を示しています。 時間の単位は秒です。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">レコードの&nbsp;&nbsp;&nbsp;種類</th>
    <th class="tg-0lax" colspan="2">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">タスク​</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">割り当て</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">チーム メンバー</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">依存関係</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>一括作成操作
次の表では、複数のレコードを作成する場合の実行時間を示しています。 具体的には、1 つの OperationSet に 20、50、100 のレコードを作成した場合の実行時間を測定しています。 時間の単位は秒です。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">レコードの&nbsp;&nbsp;&nbsp;種類</th>
    <th class="tg-0lax" colspan="6">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 レコード</th>
    <th class="tg-0lax" colspan="2">50 レコード</th>
    <th class="tg-0lax" colspan="2">100 レコード</th>
  </tr>
  <tr>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">タスク​</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">割り当て</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">依存関係</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> **プロジェクト** エンティティと **チーム メンバー** エンティティに対する一括作成操作は、この表には含まれていません。これらの操作のランタイムは、1 つのレコードを作成する API が複数回呼び出されたときのランタイムと類似するためです。 これらの API は Dataverse でただちに実行されます。

次の図は、20、50、100 のレコードを作成し、サポートされているすべてのフィールドを使用した場合の、**タスク**、**割り当て**、**依存関係** エンティティの実行時間をプロットしたものです。

![レコードの実行時間グラフを作成します。](./media/create-record-execution-time.png)

### <a name="update-operations"></a>更新操作
#### <a name="single-record-update-operations"></a>単一レコードの更新操作
次の表では、単一のレコードを更新する場合の実行時間を示しています。 時間の単位は秒です。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">レコードの&nbsp;&nbsp;&nbsp;種類</th>
    <th class="tg-0lax" colspan="2">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax">必須フィールド </th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">タスク​</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">チーム メンバー</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **リソースの割り当て** および **プロジェクトタスクの依存関係** エンティティに対する更新操作はサポートされていません。

#### <a name="bulk-update-operations"></a>一括更新操作
次の表では、複数のレコードを更新する場合の実行時間を示しています。 具体的には、1 つの OperationSet に 20、50、100 のレコードを更新した場合の実行時間を測定しています。 時間の単位は秒です。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">レコードの&nbsp;&nbsp;&nbsp;種類</th>
    <th class="tg-0lax" colspan="6">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 レコード</th>
    <th class="tg-0lax" colspan="2">50 レコード</th>
    <th class="tg-0lax" colspan="2">100 レコード</th>
  </tr>
  <tr>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
    <th class="tg-0lax">必須フィールド</th>
    <th class="tg-0lax">すべてのサポートされているフィールド</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">タスク​</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">チーム メンバー</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **リソースの割り当て** および **プロジェクトタスクの依存関係** エンティティに対する更新操作はサポートされていません。

次の図は、20、50、100 のレコードを更新し、サポートされているすべてのフィールドを使用した場合の、タスク、チーム メンバー エンティティの実行時間をプロットしたものです。

![レコードの実行時間グラフを更新します。](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>削除操作
#### <a name="single-record-delete-operations"></a>単一レコードの削除操作
次の表では、単一のレコードを更新する場合の実行時間を示しています。 時間の単位は秒です。

| レコードの種類 | 時間  |
|-------------|-------|
| タスク​        | 20.12 |
| 割り当て  | 10.86 |
| チーム メンバー | 12.52 |
| 依存関係  | 20.89 |

> [!NOTE]
> **プロジェクト** エンティティに対する削除操作はサポートされていません。

#### <a name="bulk-delete-operations"></a>一括削除操作
次の表では、複数のレコードを削除する場合の実行時間を示しています。 具体的には、1 つの OperationSet に 20、50、100 のレコードを削除した場合の実行時間を測定しています。 時間の単位は秒です。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">レコードの&nbsp;&nbsp;&nbsp;種類</th>
    <th class="tg-0lax" colspan="3">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 レコード</th>
    <th class="tg-0lax">50 レコード</th>
    <th class="tg-0lax">100 レコード</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">タスク​</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">割り当て</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">チーム メンバー</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">依存関係</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **プロジェクト** エンティティに対する削除操作はサポートされていません。

次の図は、20、50、100 のレコードを作成し、サポートされているすべてのフィールドを使用した場合の、**タスク**、**割り当て**、**チーム メンバー**、**依存関係** エンティティの実行時間をプロットしたものです。

![レコードの実行時間グラフを削除します。](./media/delete-record-execution-time.png)

## <a name="observations"></a>所見
**ExecuteOperationSet** APIは、1 回の記録操作につき、約 800 ミリ秒かけてプロジェクト スケジューリング サービスに要求を送信します。 その後、プロジェクト スケジューリング サービスは、ペイロードの処理と Dataverse の呼び出しに約 5 秒かかります。 残りの実行時間は、ビジネス ロジックの実行とデータベースへのデータ書き込みを Dataverse で行います。

100 件のレコードが作成、更新、削除されると、**ExecuteOperationSet** API は約 3 秒かけてプロジェクト スケジューリング サービスに要求を送信します。 その後、プロジェクト スケジューリング サービスは、要求の処理と Dataverse の呼び出しに約 5 秒かかります。 一括操作では、OperationSet 内のすべてのレコードに対して、**プロジェクト スケジューリング サービス税** を 1 度だけ支払う必要があります。 そのため、一括操作は単一レコードの操作よりも平均実行時間が大幅に短くなります。

## <a name="scenarios"></a>シナリオ
次の表は、特定のシナリオを達成するためにプロジェクト スケジュール API を使用した場合の実行時間です。 時間の単位は秒です。

| シナリオ                                                                   | 時間  |
|----------------------------------------------------------------------------|-------|
| 40 のタスクを持つプロジェクトを作成します。                                      | 36.01 |
| 40 のタスクと 20 の依存関係を持つプロジェクトを作成します。                  | 38.11 |
| 40 のタスクと 30 の割り当てを持つプロジェクトを作成します。                   | 60.17 |
| 40 のタスク、20 の依存関係、30 の割り当てを持つプロジェクトを作成します。 | 60.27 |

## <a name="best-practices"></a>ベスト プラクティス
前述のシナリオの結果に基づき、次の条件で API のパフォーマンスが向上します:

  - 可能な限り多くのオペレーションをグループ化します。 バルク操作の平均ランタイムは、シングル レコード操作の平均ランタイムよりも優れています。 使用する OperationSets の数が少なければ少ないほど、平均実行時間は速くなります。
  - シナリオを達成するために必要な最小限の属性のみを設定します。 OperationSet 要求に含まれる必須ではないフィールドの種類を選択してください。 外部キーやロールアップ フィールドを含むフィールドは、パフォーマンスに悪影響を与えます。
