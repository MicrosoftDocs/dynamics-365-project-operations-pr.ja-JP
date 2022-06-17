---
title: 2021 年 8 月の新機能 - リソース/非在庫のシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 8 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912292"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 8 月の新機能 - リソース/非在庫のシナリオ向け Project Operations

*適用対象: リソース/非在庫ベースのシナリオ向け Project Operations*

この記事は、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます。

   - Microsoft Dataverse 環境バージョン 4.13.0.152 の Project Operations。
   - Dynamics 365 Finance 環境バージョン 10.0.20 でのプロジェクト管理と会計。

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- **承認セット**: 承認は、グループの時間、費用、または材料用途の承認要求を、操作のより小さなサブセットにまとめて設定します。 このグループ化により、承認をプロジェクトごとに特定の順序で処理し、再試行と順序付けを行うことができるようになります。 リクエストをグループ化すると、大量の承認に対する承認処理の信頼性と追跡可能性が向上します。 詳しくは、[承認セット](../approvals/approval-sets.md)を確認してください。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。

Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブルマッピングを有効にします。 最新バージョンのマッピングが有効になっていない場合、一部の機能や性能が正しく動作しないことがあります。 マッピングのアクティブなバージョンは、**バージョン** 列の **二重書き込み** のページで確認できます。 **テーブル マッピングのバージョン** を選択し、最新のバージョンを選択してから、選択したバージョンを保存することで、新しいバージョンのマッピングを有効にすることができます。 既成のテーブル マッピングをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マッピングの起動に問題がある場合は、二重書き込みのトラブルシューティング: [マッピングでのテーブル列が見つからない場合](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)に記載の内容に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求および価格設定 | 2295625 | マイルストーン名は、請求書スケジュールから請求書明細の詳細にコピーする必要があります。 |
| 請求および価格設定 | 2316323 | リソースベースのシナリオでは、Project Operations の見積もり請求で割引を編集できないようにする必要があります。 |
|  営業案件管理 | 2338619 | **機会** と **見積もり** ビジネス ルールはページでのみ呼び出す必要があります。 |
| リソース管理 | 2316523 | 役割がアタッチされているリソース要件から **リクエストを送信** を使用すると、エラーが表示されません。 |
| リソース管理 | 2326885 | プロジェクトを介してリソース要件を作成すると、エラーは表示されません。 |
| 時間と経費 | 2335584 | 時間エントリにおける非推奨のタスク フロー。 |
| 時間と経費 | 2336884 | **週のコピー** 時間エントリ ボタンは、現在のユーザー以外にも機能する必要があります。 |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 出張と経費 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | クレジット カード取引から経費が作成されると、誤った仕入先取引と消費税取引の金額が転記されます。 |
| 出張と経費 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 間違った決済は、支払仕訳帳が生成されるときに作成される明細行です。 |
| 出張と経費 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | クレジット カード取引から経費が作成されると、誤った消費税取引の金額が転記されます。 |
| 出張と経費 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 経費明細行の削除には時間がかかる場合があります。 |
| プロジェクト会計 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | KB 4619395 を適用した後に見積もりを転記する場合、システムは連続番号シーケンスの設定をサポートしません。 |
| プロジェクト会計 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | ベンダー請求書の転記は、エラー メッセージ「2021 年 5 月 17 日の伝票における取引の残高が等しくありません。 (会計通貨: 0.00 - 報告通貨: 0.01)」で失敗する可能性があります。 |
