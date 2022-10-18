---
title: 2022 年 9 月のニュース - Project Operations のライト展開
description: この記事では、Microsoft Dynamics 365 Project Operations ライト展開の 2022 年 9 月リリースで利用可能な品質更新について説明します。
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634858"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>2022 年 9 月のニュース - Project Operations のライト展開

_**適用対象:** ライト展開 - 見積もり請求の取引_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.46.0.60 の Project Operations

## <a name="features-included-in-this-release"></a>このリリースが含む機能

| 機能 | 機能名 | 詳細情報 |
| --- | --- | --- |
| 営業案件管理 | **見積もりの改訂とアクティブ化**<br>Project Operations は、販売プロセスを完全にサポートします。 プロジェクトの見積もりをアクティブ化して、見積もりが読み取り専用でレビュー中の状態を表すことができます。 アクティブ化された見積もりを改訂して、増分番号を持つ新しい見積もりを作成できます。 アクティブ化されたプロジェクト見積もりまたは見積もりの改訂は、受注または失注としてクローズすることができます。 | [プロジェクト見積もりを変更してアクティブ化する](/dynamics365/project-operations/sales/activation-and-revision) |
| 請求と価格 | **タイムゾーンにとらわれない価格のデフォルト設定**<br>Project Operations では、すべてのプロジェクト実績にタイムゾーンに依存しない日付の概念が導入されました。 新しい分野、**取引日**、仕訳明細行と実績で使用できるようになり、トランザクションが発生した日付を格納するために使用されますが、その日付は協定世界時に変換されません。 この日付は、価格の不履行や請求書の作成などのダウンストリーム プロセスに使用されます。 | <p>[プロジェクト ベースの見積もりと実績のコスト単価を決定する](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[プロジェクト ベースの見積もりと実績の販売価格を決定する](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| 請求と価格 | **Project Operations での有効日価格のオーバーライド**<br>日付有効価格の上書きは、価格リスト内の特定の価格を上書きしたり変更したりする方法です。 | [日付適用価格変更](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 時間と経費 | **グローバル承認者**<br>この機能により、プロジェクト内のプロジェクトまたはチーム メンバーのステータスに関係なく、独立系ソフトウェア ベンダー (ISV) および一元化された承認が可能になります。 | [セキュリティと承認](/dynamics365/project-operations/approvals/approvals-security) |
|プロジェクトの計画と追跡|**プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する** </br> </br>リソース割り当て配分型の編集 API を使用すると、開発者は、サポートされている日付範囲全体でタスク担当者の作業量をプログラムで指定して、より詳細な時間段階の作業計画を立てることができます。|[プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>品質更新プログラム

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求と価格 | 2754422 | プロジェクトが Dataverse でコピーされたときに、材料と経費の見積もりが Dynamics 365 Finance に流れない . |
| 時間と経費 | 2787409 | 有効でない承認者は、非プロジェクト時間エントリを承認できます。 |
| 営業案件管理 | 2788907 | フラグを含む注文明細行の一意性検証に関するエラー メッセージが更新されました。 |
| 時間と経費 | 2842253 | 時間承認の Null 例外処理。 |
| 請求と価格 | 2844181 | 関連付け ID を取得できないと、請求書の作成がブロックされます。 |
| 請求と価格 | 2876628 | QLD、CLD - 見積もり価格表の解決には、価格表の従来の日付範囲フィールドを使用する必要があります。 |
| 外注 | 2893222 | 下請けラインに役割が指定されていない場合は、チーム メンバーのそのラインを任意の役割で選択できる必要があります。 |
