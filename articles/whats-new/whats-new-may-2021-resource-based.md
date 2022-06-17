---
title: 2021 年 5 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事は、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 5 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930416"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 5 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます。

- Dynamics 365 Dataverse 環境バージョン 4.10.0.186 での Project Operations
- 財務と運用アプリの環境バージョン 10.0.18 でのプロジェクト管理および会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- [スケジュール モード](../project-management/scheduling-modes.md): プロジェクト マネージャーは、固定期間、固定作業、または固定単位のスケジュール モードを使用して、プロジェクトを管理する必要があるかどうかを定義できます。
- [マイレージ レート階層を使用したマイレージの設定](../expense/set-up-mileage.md): 従業員経費精算書のマイレージ レート階層を更新します。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

次のリストは、Project Operations 2021 年 5 月リリースで変更または追加された二重書き込みのマッピングを示します。

| エンティティ マップ | 更新バージョン | コメント |
| --- | --- | --- |
| プロジェクトの資金源 (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | プロジェクト契約の顧客支払条件の同期。 |
| プロジェクトの仮発行請求書 V2 (invoices) | 1.0.0.3 | 見積もり請求の支払条件の同期。 |
| Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | 品質更新プログラム |
| プロジェクト V2 (msdyn\_projects) | 1.0.0.2 | 品質更新プログラム |

最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションやF財務と運用アプリ ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にする必要があります。 最新バージョンのマッピングが有効になっていない場合、一部の機能や性能が正しく動作しないことがあります。 マッピングのアクティブなバージョンは、**二重書き込み**  ページの  **バージョン**  の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 既成のテーブル マッピングをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの起動に問題がある場合は、二重書き込みのトラブルシューティング ガイドの [マッピング上にテーブルの列が表示されない問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) のセクションの手順に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求と価格 | 2227635 | **単位グループ** と **単位** フィールドの値は、**材料の見積もり** グリッドの製品から既定で設定されます。 |
| 請求と価格 | 2234127 | **タスク ID** フィールドは、仕入先請求書が転記されたときに、Dataverse のプロジェクト実績に正しく統合されるようになりました。 |
| 請求と価格 | 2235564 | 仕訳帳明細行を保存すると、仕訳帳明細行エントリに表示される通貨が、保存後の明細行の既定通貨と一致するようになります。 |
| 請求と価格 | 2246671 | 請求請求時にトランザクションを請求不可にすると、元の未請求販売レコードが取り消され、新しい未請求販売レコードが請求不可として作成されます。 |
| 請求と価格 | 2264042 | 環境内に無効な請求書修正の詳細がある場合でも、有効な請求書修正をブロックすることはできません。 |
| 請求と価格 | 2146367 | プロジェクト請求書ヘッダーの二重書き込みマッピングが拡張され、支払条件が含まれるようになりました。 |
|  営業案件管理 | 2086888 | 見積を新しくコピーした見積の請求可能ロールとカテゴリにコピーする前に、非アクティブ化されたロールとカテゴリを追加しないでください。 |
|  営業案件管理 | 2234376 | 読み取り専用フィールドは、**材料の見積もり** グリッドでグレー表示されます。 |
|  営業案件管理 | 2238337 | 連絡先に基づく見積もりは、プロジェクトの価格表に関連付けられていなくても保存できます。 |
|  営業案件管理 | 2239810 | 失注として見積をクローズすると、関連するプロジェクトもクローズされ、予約もキャンセルされます。 |
| プロジェクトの計画と追跡 | 2099559 | **プロジェクト タスク** グリッドを開くの前に、システムの正常性に関する検証を追加しました。 |
| プロジェクトの計画と追跡 | 2178987 | **次のステージ** を **プロジェクト** ページで選択したときに発生する一時的なエラーを修正しました。 |
| リソース管理 | 2224817 | 予約を延長する機能は、既定で正しい予約状態になります。 |
| 時間エントリ | 2202476 | **時間エントリ** ページでは、反応グリッド コントロールを使用し、グリッドのずれなどの問題を修正しました。 |
| 時間エントリ | 2223377 | 時間エントリは **予約可能リソース** ページの **関連** セクションから非表示になり、ユーザビリティとの混同を回避します。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| プロジェクト管理および会計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | リソース ベースのシナリオ向け Project Operations: 統合エラーのため見積を受注に変換できません。 |
| プロジェクト管理および会計 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: 重複する契約品目とトランザクション タイプがチェックされているため、契約品目をプロジェクト ID に関連付けようとするとエラー メッセージが表示されます。 |
| プロジェクト管理および会計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** は、別の顧客からの資金調達ソースの請求書住所を設定します。 |
| 出張と経費 | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | マイルの設定に関連する転記エラーが発生する場合があります。 |
| 出張と経費 | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | 機能 **個人に分割** は、外貨通貨の経費処理では使用できません。 |
| 出張と経費 | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 経費カテゴリのドロップダウン値は、リソースであるかどうかに関係なく、代行に対して誤ったカテゴリを表示しています。 |
| 出張と経費 | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | **リソース/カテゴリの検証** エラーのため、会社間取引の経費精算書を保存できません。 |
| 出張と経費 | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 経費報告書の転記でのマイレージ率の計算が間違っていると、行が分割されてしまう。 |
| 出張と経費 | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 消費税が含まれていて、支払い方法の相手勘定タイプが **作業者** の場合、会社間の経費報告書を転記できません。 |
| 出張と経費 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | ロールバック **TrvRequisitionLine** データ エンティティと一意のインデックスが関連付けられます。 |
| 出張と経費 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 経費精算書は、元伝票明細行の作成と更新をサポートします。 |
| 出張と経費 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 消費税が転記先の法人に転記されている場合、会社間シナリオで誤った補助元帳仕訳が表示されます。 |
| 出張と経費 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Dataverse から削除されても Finance から経費の見積もりは削除されません。 |
| 出張と経費 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 経費カテゴリが非プロジェクト カテゴリの場合、**経費** ページで選択された財務分析コードは経費精算書にコピーされません。 |
