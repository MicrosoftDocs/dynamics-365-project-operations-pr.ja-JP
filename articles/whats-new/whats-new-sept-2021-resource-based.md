---
title: 2021 年 9 月 のニュース - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックは、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 9 月リリースで利用可能な品質更新に関する情報を提供します。
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582900"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 9 月 のニュース - リソース/非在庫ベースのシナリオ向け Project Operations

*適用対象: リソース/非在庫ベースのシナリオ向け Project Operations*

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

   - Microsoft Dataverse 環境バージョン 4.14.0.99 の Project Operations。
   - Dynamics 365 Finance 環境バージョン 10.0.20 でのプロジェクト管理と会計。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブルマッピングを有効にします。 最新バージョンのマッピングが有効になっていない場合、一部の機能や性能が正しく動作しないことがあります。 マッピングのアクティブなバージョンは、**バージョン** 列の **二重書き込み** のページで確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 既成のテーブル マッピングをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、デュアル ライト トラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 時間と経費 | 1811407 | 経費入力承認のためにプロジェクト承認者セキュリティ ロールを調整しました。 |
| 時間と経費 | 1811438 | 時間入力承認のキャンセルのためにプロジェクト承認者セキュリティ ロールを調整しました。 |
| 時間と経費 | 2370126 | **時間入力** エンティティの **プロジェクト タスク** アイコンと **役割** アイコンが更新されました。 |
| 時間と経費 | 2379879 | 電話用 Dynamics 365 を使用する場合の、時間入力の **コピー ウィーク** 機能を修正しました。 |
| 請求と価格 | 2371906 | リソース ベースの展開の Project Operations では、プロフォーマ請求書の合計金額を調整することはできません。 |
| 請求と価格 | 2385802 | プロジェクトの合計が更新されたときに負の実際の時間で発生するエラーを修正しました。 |
| 請求と価格 | 2389675 | プロフォーマ請求書の確認動作が改善されました。 長期実行ジョブ エンティティは、会計の確認結果を書き込むために必要なアクティビティを考慮に入れる必要があります。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 出張と経費 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | クレジットカード取引から作成された費用から転記されたベンダーおよび消費税取引の金額が正しくありません。 |
| 出張と経費 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 支払仕訳が生成されるときに、間違った決済明細が作成されます。 |
| 出張と経費 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | クレジットカード取引から作成された費用から転記された消費税取引の金額が正しくありません。 |
| 出張と経費 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 経費明細行の削除には時間がかかる場合があります。 |
| プロジェクト会計 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | KB 4619395 を適用した後、数列を **継続的** に変更することはサポートされておらず、見積もりを投稿すると、"システムは数列 Proj_X のセットアップの '連続' をサポートしていません" というエラーが発生します。 |
| プロジェクト会計 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | ベンダー請求書の転記は、次のエラーメッセージで失敗する可能性があります。"バウチャーのトランザクションは、2021 年 5 月 17 日の段階でバランスが取れていません。 (会計通貨: 0.00 - 報告通貨: 0.01)。" |
