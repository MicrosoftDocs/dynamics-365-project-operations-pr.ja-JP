---
title: 2022 年 7 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 7 月リリースで利用可能な品質更新について説明します。
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183910"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 7 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.44.0.22 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.28 でのプロジェクト管理と会計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 展開と構成 | 2761472 | Project Operations のインストール エラーが処理されます。 |
| 請求と価格 | 2746940 | 外注品目名の最大文字数は 100 にする必要があります。 |
| 請求と価格 | 2739162 | 顧客は、実際のグリッド ビューでリボン ボタンを表示できる必要があります。 |
| プロジェクトの計画と追跡 | 2730318 | プロジェクト件名にサポートされていない文字がある場合の検証を更新しました。 |
| 請求と価格 | 2705361 | マイルストーン請求済み営業実績は、プロジェクト追跡フィールドに含める必要があります。 |
| 請求と価格 | 2675880 | プロジェクトが作業ベースではない契約品目にリンクされるのを防止します。 |
| 請求と価格 | 2664396 | 見積もり価格表を見積もりなしで保存する場合、見積もりを空にできないという内容のエラーが発生するはずです。 |
| 請求と価格 | 2184019 | 裏付けとなる契約や見積もりがないプロジェクトでは、**タスクベースの請求** タブを表示しないようにします。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。

## <a name="features-turned-on-by-default-in-upcoming-release"></a>今後のリリースで、既定で有効になる機能

次の表に、バージョン 10.0.29 で既定で有効になる機能の一覧を示します。 自動的に有効にした機能のほとんどは、[機能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)でオフにできます。 今後、自動的に有効にした機能の一部が機能管理から削除され、必須になる可能性があります。 この変更は、顧客が現在の機能を使用していることを確認し、拡張機能が追加されても、現在の機能に構築することができます。 必要不可欠と判断される場合を除き、1 年未満の機能が自動的に有効になることはありません。

| 機能名 | 日付の有効化 | 機能の追加日 | 機能の状態 | モジュール |
| --- | --- | --- |--- |--- |
| 資金調達ルール配賦の変更に基づいて、時間トランザクションの調整の有効化 | 2022 年 9 月 16 日 | 2020 年 10 月 7 日 | 既定で有効 | プロジェクト管理および会計 |
| プロジェクト発注書前払い請求書の取り消し機能 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 既定で有効 | プロジェクト管理および会計 |
| リソースベース/非在庫のシナリオで Project Operations を使用する場合、請求書提案の明細行の削除 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 既定で有効 | プロジェクト管理および会計 |
| 転記されたプロジェクト トランザクションの会計の調整 | 2022 年 9 月 16 日 | 2020 年 5 月 10 日 | 既定で有効 | プロジェクト管理および会計 |
| プロジェクトの既定の会計設定の有効化 | 2022 年 9 月 16 日 | 2020 年 2 月 19 日 | 既定で有効 | プロジェクト管理および会計 |
| プロジェクトの複数の契約ラインを有効にする | 2022 年 9 月 16 日 | 2020 年 6 月 29 日 | 既定で有効 | プロジェクト管理および会計 |
| 現在の承認ステータスで編集が許可されていない場合、プロジェクトの時間仕訳の読み取り専用化 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 既定で有効 | プロジェクト管理および会計 |
| 購買注文明細行が更新され、発注書の変更管理パラメーターがオンになっている場合に、購買注文明細行からの販売明細行同期の有効化 | 2022 年 9 月 16 日 | 2020 年 10 月 7 日 | 既定で有効 | プロジェクト管理および会計 |
| Dynamics 365 Customer Engagement で Project Operations を有効にする | 2022 年 9 月 16 日 | 2020 年 6 月 29 日 | 既定で有効 | プロジェクト管理および会計 |
| プロジェクト トランザクションの取り消し修正機能 | 2022 年 9 月 16 日 | 2020 年 7 月 13 日 | 既定で有効 | プロジェクト管理および会計 |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>今後のリリースで必須となる機能

次の表に、バージョン 10.0.29 以降から必須になる機能の一覧を示します。

| 機能名 | 日付の有効化 | 機能の追加日 | 機能の状態 | モジュール |
| --- | --- | --- | --- | --- |
| 為替レートを四捨五入せずに、資金調達ソースの確定済みの値を計算 | 2022 年 9 月 16 日 | 2020 年 6 月 14 日 | Mandatory | プロジェクト管理および会計 |
| 元のトランザクションと同じ元帳勘定でプロジェクト調整転記の有効化 | 2022 年 9 月 16 日 | 2020 年 6 月 14 日 | Mandatory | プロジェクト管理および会計 |
| プロジェクト契約の確定済みの値の詳細 | 2022 年 9 月 16 日 | 2019 年 8 月 31 日 | Mandatory | プロジェクト管理および会計 |
| プロジェクトの請求書提案の作成中にリソースによる並べ替えの有効化 | 2022 年 9 月 16 日 | 2019 年 8 月 31 日 | Mandatory | プロジェクト管理および会計 |