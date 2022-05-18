---
title: 2022 年 5 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオの Microsoft Dynamics 365 Project Operations の 2022 年 5 月リリースで利用可能な品質更新に関する情報について説明します。
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709998"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 5 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます:

- Dataverse 環境のバージョン 4.42.0.70 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.26 でのプロジェクト管理と会計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム
### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| リソース管理 | 2634019 | 汎用チーム メンバーをリソースとして追加する際のビジネス検証のエラー メッセージが改善されました。 |
| プロジェクト計画および追跡 | 2648515 | スケジュール エンティティで **所有者 ID**、**状態**、**ステータス** の更新を制限しました。 |
| 請求および価格設定 | 2653167 | **見積り** グリッドの小数点は、**個人用オプション** の形式設定に従う必要があります。 |
| 請求および価格設定| 2662251 | 材料見積もりレコードの作成時に、**修正された単位** と **出荷単位一覧** フィールドの値は規定値に設定されます。 |
| 請求および価格設定| 2571408 | 未請求の売上実績には、ドラフト請求書を作成するときに見積もり請求書 ID が記録されます。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) を参照してください。
