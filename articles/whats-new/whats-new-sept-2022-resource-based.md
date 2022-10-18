---
title: 2022 年 9 月 のニュース - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 9 月リリースで利用可能な品質更新について説明します。
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634811"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 9 月 のニュース - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.46.0.60 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.29 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

| 機能 | 機能名 | 詳細情報 |
| --- | --- | --- |
| 営業案件管理 | **見積もりの改訂とアクティブ化**<br>Project Operations は、販売プロセスを完全にサポートします。 プロジェクトの見積もりをアクティブ化して、見積もりが読み取り専用でレビュー中の状態を表すことができます。 アクティブ化された見積もりを改訂して、増分番号を持つ新しい見積もりを作成できます。 アクティブ化されたプロジェクト見積もりまたは見積もりの改訂は、受注または失注としてクローズすることができます。 | [プロジェクト見積もりを変更してアクティブ化する](/dynamics365/project-operations/sales/activation-and-revision) |
| 請求と価格 | **タイムゾーンにとらわれない価格のデフォルト設定**<br>Project Operations では、すべてのプロジェクト実績にタイムゾーンに依存しない日付の概念が導入されました。 新しい分野、**取引日**、仕訳明細行と実績で使用できるようになり、トランザクションが発生した日付を格納するために使用されますが、その日付は協定世界時に変換されません。 この日付は、価格の不履行や請求書の作成などのダウンストリーム プロセスに使用されます。 | <p>[プロジェクト ベースの見積もりと実績のコスト単価を決定する](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[プロジェクト ベースの見積もりと実績の販売価格を決定する](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| 請求と価格 | **Project Operations での有効日価格のオーバーライド**<br>日付有効価格の上書きは、価格リスト内の特定の価格を上書きしたり変更したりする方法です。 | [日付適用価格変更](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 外注 | **下請けとベンダー請求書の照合**<br>この機能により、顧客は、プロジェクト作業に使用されるリソース時間、経費カテゴリ、および資材を購入するための下請け契約を作成できます。 また、顧客は財務および運用アプリで、検証用に Dataverse でプロジェクト マネージャーが利用できる仕入先請求書を記録することもできます。 | <p>[外注管理](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[仕入先請求書の作成](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| 時間と経費 | **グローバル承認者**<br>この機能により、プロジェクト内のプロジェクトまたはチーム メンバーのステータスに関係なく、独立系ソフトウェア ベンダー (ISV) および一元化された承認が可能になります。 | [セキュリティと承認](/dynamics365/project-operations/approvals/approvals-security) |
| 経費管理 | **仕入先通貨で経費負債を転記する機能**<br>この機能は、現金支払方法機能のベンダー通貨で転記される経費報告書を有効にします。 | [仕入先通貨で経費負債を転記する機能](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| プロジェクト調達 | **受給時支払のベンダー支払い**<br>この機能により、支払時に支払う (PWP) 機能を Project Operations の非在庫環境で使用できるようになります。 これにより、顧客から支払いを受け取るまで、保留条件に基づいてベンダーの支払いをブロック/保留できます。 | [受給時支払のベンダー支払い](/dynamics365/project-operations/procurement/pay-when-paid) |
| プロジェクト調達 | **プロジェクト購買要求**<br>この機能により、ユーザーは、Dynamics 365 Customer Engagement 統合の Project Operations が有効になっている法人で、プロジェクト関連の発注書を作成できます。 プロジェクト発注書を使用して、調達部門のペルソナによるプロジェクトに対する非在庫資材調達を記録できます。 プロジェクトの発注書は Dataverse と同期されません。 ただし、仮想エンティティを使用して、プロジェクトの発注書明細行をプロジェクトマネージャー情報向けに Dataverse で表示できます。 プロジェクト関連の仕入先請求コストは、Dataverse でプロジェクト実績エンティティと統合されています。 プロジェクト コストは、Project Operations 統合仕訳帳を使用して、プロジェクトのサブ仕訳帳に記録されます。 | |
|プロジェクトの計画と追跡|**プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する** </br> </br>リソース割り当て配分型の編集 API を使用すると、開発者は、サポートされている日付範囲全体でタスク担当者の作業量をプログラムで指定して、より詳細な時間段階の作業計画を立てることができます。|[プロジェクト スケジュール API を使用して、スケジュール エンティティで操作を実行する](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

次のテーブルは、2022 年 9 月にリリースされた Project Operations で変更または追加された二重書き込みマップを表示しています。

| エンティティ マップ | 更新バージョン | Comments |
| -------------- | ------------------- | ------------|
| Project Operations 統合実績 (msdyn_actuals) | 1.0.0.15 | このマップは、リソース ベースのシナリオの Project Operations での外注実績処理をサポートします。 |
| Project Operations 統合プロジェクト ベンダー請求書のエクスポート エンティティ (msdyn_projectvendorinvoices) | 1.0.0.2 | このマップは、リソース ベースのシナリオの Project Operations での外注実績処理をサポートします。 |
| Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ (msdyn_projectvendorinvoicelines) | 1.0.0.5 | このマップは、リソース ベースのシナリオの Project Operations での外注実績処理をサポートします。 |

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求と価格 | 2754422 | プロジェクトが Dataverse でコピーされたときに、材料と経費の見積もりが Finance にフローされない。 |
| 時間と経費 | 2787409 | 有効でない承認者は、非プロジェクト時間エントリを承認できます。 |
| 営業案件管理 | 2788907 | フラグを含む注文明細行の一意性検証に関するエラー メッセージが更新されました。 |
| 時間と経費 | 2842253 | 時間承認の Null 例外処理。 |
| 請求と価格 | 2844181 | 関連付け ID を取得できないと、請求書の作成がブロックされます。 |
| 請求と価格 | 2876628 | QLD、CLD - 見積もり価格表の解決には、価格表の従来の日付範囲フィールドを使用する必要があります。 |
| 外注 | 2893222 | 下請けラインに役割が指定されていない場合は、チーム メンバーのそのラインを任意の役割で選択できる必要があります。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート情報記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) を参照してください。

## <a name="features-turned-on-by-default-in-upcoming-release"></a>今後のリリースで、既定で有効になる機能

次の表に、バージョン 10.0.30 で既定で有効になる機能の一覧を示します。 自動的に有効にした機能のほとんどは、[機能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)でオフにできます。 今後、自動的に有効にした機能の一部が機能管理から削除され、必須になる可能性があります。 この変更は、顧客が現在の機能を使用していることを確認し、拡張機能が追加されても、現在の機能に構築することができます。 必要不可欠と判断される場合を除き、1 年未満の機能が自動的に有効になることはありません。

| 機能名 | 日付の有効化 | 機能の追加日 | 機能の状態 | モジュール |
| --- | --- | --- |--- |--- |
| ユーザーが同期操作と非同期操作を切り替える必要がある場合に非同期操作を有効にする | 2022 年 10 月 21 日 | 2021 年 4 月 9 日 | 既定で有効 | 経費管理 |
| 必要な領収書の経費ポリシー評価 | 2022 年 10 月 21 日 | 2021 年 12 月 20 日 | 既定で有効 | 経費管理 |
| 代理作業者が作成した経費報告書のリスト ビュー | 2022 年 10 月 21 日 | 2020 年 2 月 19 日 | 既定で有効 | 経費管理 |
| 会計年度 によるマイレージ合計計算 | 2022 年 10 月 21 日 | 2022 年 5 月 10 日 | 既定で有効 | 経費管理 |
