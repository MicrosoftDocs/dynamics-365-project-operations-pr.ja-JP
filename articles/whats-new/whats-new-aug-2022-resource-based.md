---
title: 2022 年 8 月の新機能 - リソース/非在庫のシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 8 月リリースで利用可能な品質更新について説明します。
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403862"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 8 月の新機能 - リソース/非在庫のシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.45.0.53 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.28 でのプロジェクト管理と会計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 営業案件管理 | 2762089 | 組織で自動保存が無効になっている場合、失われたものとして契約を閉じる際のエラー処理。|
|プロジェクトの計画と追跡 | 2767841 | テレメトリの更新 プロジェクト エンティティ シナリオの作成または更新。|
|請求と価格 | 2771072 | 見積もりを獲得する際の null 参照の例外処理。|
|請求と価格 | 2844181 |関連付け ID の取得に失敗したため、請求書の作成がブロックされました。|
|請求と価格 | 2852836 | CE で作成および承認された会社間経費の会社間実績がありません。|


### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。
