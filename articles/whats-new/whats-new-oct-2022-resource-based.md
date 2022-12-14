---
title: 2022 年 10 月 の最新情報 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 10 月リリースで利用可能な品質更新について説明します。
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806633"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 10 月 の最新情報 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.57.0.176 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.30 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

| 機能 | 機能名 | 詳細情報 |
| --- | --- | --- |
| プロジェクトの計画と追跡 | **Project Operations 外部のスケジューリング**<br>外部スケジューリング モードは、ネイティブの Dataverse API を使用して、作業内訳構造 (WBS) に関連するエンティティを、Project for the Web で強制される現在の制限なしに、ネイティブに作成、更新、削除できるようにするものです。 | [外部スケジュール](/dynamics365/project-operations/project-management/external-scheduling) |
| 展開と構成 | <p>**顧客が導入タイプを選択できるようにする**<br>Project Operations の製品主導の更新プログラム (PDU) は、二重書き込みコアおよびオーケストレーション ソリューションが環境にインストールされている場合に、Project Operations 二重書き込みソリューションを自動的にインストールするために使用されます。</p><p>この機能により、プロジェクト パラメータに新しい **ソリューション アップグレード動作** パラメータが導入されました。 このパラメーターを **ライトのみ** に設定すると、二重書き込みコアおよびオーケストレーション ソリューションが環境にインストールされている場合でも、PUD は Project Operations 二重書き込みソリューションを自動的にインストールしなくなります。 この動作は、二重書き込みソリューションを使用して販売注文を財務と運用アプリに統合することを計画しているが、Project Operations をライト モード (つまり、財務と運用アプリに統合しない) で使用したい場合に役立ちます。</p> | |
| 請求と価格 | <p>**統合環境での経費未請求販売トランザクションの通貨換算**<br>Project Operations を財務と運用アプリと統合して使用してい (リソース/非在庫展開タイプ) の場合、為替レートは通常、財務と運用アプリでマスターします。 しかし、顧客への請求時に「原価」または「原価を上回るマークアップ」という価格計算方法を用いて価格設定すべき経費区分の場合、売上金額の計算に使用する為替レートは、財務と運用アプリの為替レートではなく、Dataverse の為替レートを使用することになります。</p><p>この機能により、プロジェクト パラメータに新しい **通貨変換の動作** パラメータが導入されました。 このパラメーターが **フォールバック付きで拡張** に設定されている場合、経費トランザクションの未請求売上高は、財務および運用アプリからの為替レートを使用して計算されます。</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求と価格 | 2316317 | このシステムでは、請求可能トランザクションを含まない請求書を作成できます。 |
| 請求と価格 | 2737300 | フォームにアクセスする前に、**顧客** フィールドの可用性を検証します。 |
| 請求と価格 | 2744948 | 請求方法の null チェックを追加します。 |
| 請求と価格 | 2763515 | 請求書の売買契約書が存在しない場合の Null 参照エラー処理。 |
| 請求と価格 | 2844301 | エラーのため、一括請求書の作成が失敗します。 |
| 請求と価格 | 2845869 | 組織サービスのストレージが正しくありません。 |
| 請求と価格 | 2853729 | 請求タイプが変更されると、役割と価格の詳細が更新されます。 |
| 請求と価格 | 2940350 | 実績が価格設定される場合、アクティブな価格表のみが自動的に入力されます。 |
| 展開と構成 | 3001206 | The msdyn\_replaylogheader エンティティが、Customer Orgs のアップグレードを妨げています。 |
| 営業案件管理 | 2755582 | 分割請求ルール ヘルパーで Null 参照例外が処理されます。 |
| 営業案件管理 | 2761477 | 分割請求が使用されている場合、マイルストーン (ヘッダー) を削除すると孤立したマイルストーンが残ります。 |
| 営業案件管理 | 2767595 | メイン フォームで材料使用量レコードを開くと、そのレコードの予約可能なリソースが現在サインインしているユーザーに変更されます。 |
| プロジェクトの計画と追跡 | 2790384 | 保留中の OperationSet タイムアウトが短すぎます。 |
| プロジェクトの計画と追跡 | 2957840 | タスクを保存できないため、統合 Project Operations の **タスク** ページに列を追加できません。 |
| リソース管理 | 2751560 | リソース要件の優先組織単位が矛盾しています。 |
| 外注 | 2853245 | 契約明細行が既に仕入先請求書明細行にリンクされている場合、仕入先請求明細行の実績の照合は検証ステータスを更新しません。 |
| 外注 | 2907231 | 仕入先請求書の処理段階を進めることができません。 |
| 時間と経費 | 2867363 | 承認待ちの状態でも、承認待ちの不在/休暇のビューから記録が外れることはありません。 |
| 時間と経費 | 2894405 | TESA: 未使用の POC ディレクトリがコンプライアンスの問題を引き起こしています。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート情報記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。
