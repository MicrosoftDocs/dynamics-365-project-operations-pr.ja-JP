---
title: 2022 年 11 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 11 月リリースで利用可能な品質更新について説明します。
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831087"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 11 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.58.0.119 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.30 でのプロジェクト管理と会計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブルマッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求と価格 | 2781818 | 材料使用ログの価格を既定の設定中にキーが見つからないというエラーが発生しました。 |
| 請求と価格 | 2922373 | 見積明細を失効見積としてクローズしたプロジェクトにリンクすることはできません。 |
| 請求と価格 | 2943206 | プロジェクト エンティティの **契約品目** フィールドはオプションである必要があります。 |
| 請求と価格 | 2953182 | 修正請求書のエラー メッセージを改善します。|
| 請求と価格 | 2959500 | 失われた見積もりに既に関連付けられているプロジェクト タスクに見積もり品目をリンクすることはできません。|
| 請求と価格 | 2959560 | 特定のロケールで落札された見積もりを閉じる際に、「この顧客は既にプロジェクト契約を結んでいます」というメッセージが表示されます。 |
| 請求と価格 | 3031727 | リソースの割り当てに失敗し、必須フィールド 'msdyn_Company' が見つからないというエラーが発生します。 |
| 請求と価格 | 3036905 | ProjectTeamMember で所有会社が初期化されることはありません。 |
| 営業案件管理 | 2763519 | EnsureProjectContractAllowsUpdates で Null 参照エラーが発生しました。 |
| 営業案件管理 | 2783798 | 見積もり明細行でプロジェクトの見積もりをインポートすると、経費と資材の見積もりのタスクの説明が欠落します。|
| 営業案件管理 | 2988635 | 見積もり中の顧客を削除する際のエラー メッセージの説明を改善しました。 |
| 営業案件管理 | 3001191 | 請求方法が null として指定されている営業案件から見積もりを作成できません。 |
| アップグレード | 3012324 | 名前に Tab などの制御文字が含まれるプロジェクトで、プロジェクトの変換が失敗します。 || プロジェクトの計画と追跡 | 2790384 | 保留中の OperationSet タイムアウトが短すぎます。 |
| プロジェクトの計画と追跡 | 3044275 | 次のローカライズが見つかりません: missingProjectSchedulerErrorMessage。 |
| プロジェクトの計画と追跡 | 3044277 | スケジューラが設定されていない場合、Project Recon グリッドがロードされません。|
| リソース管理 | 2943153 | [追跡] タブを更新して、期間の小数点以下 2 桁を表示します。|
| 外注 | 2932774 | 仕入先請求明細行の読み取り専用エラーが誤ってスローされます。 |
| 外注 | 2939556 | アクティブでない場合、仕入先請求書ヘッダーのステータスをドラフトのオンライン削除に設定しないでください。 |
| 時間と経費 | 2939998 | ProjOps で新しい TESA バージョンを取り込みます。 |


### <a name="project-management-and-accounting-in-finance"></a>Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート情報記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。
