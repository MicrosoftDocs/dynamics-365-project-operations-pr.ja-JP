---
title: 2022 年 4 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事では、リソース/非在庫ベースのシナリオ向け Microsoft Dynamics 365 Project Operations の 2022 年 4 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110890"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 4 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.41.0.45 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.26 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

プロジェクトの発注書と保留中の仕入先請求書で調達カテゴリを使用することができます。 詳細については、[プロジェクトの発注書と保留中の仕入先請求書で調達カテゴリを使用する](../procurement/configure-procurement-categories.md) を参照してください。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

次のテーブルは、2022 年 3 月にリリースされた Project Operations で変更または追加された二重書き込みマップを表示しています。

| エンティティ マップ | 更新バージョン | Comments |
| -------------- | ------------------- | ------------|
| Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ msdyn\_projectvendorinvoicelines | 1.0.0.4 | このマップは、発注書と保留中の仕入先請求書で調達カテゴリの使用をサポートします。 |

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| ------------ | ---------------- | -------------- |
| 時間と経費 | 2573900 | **最新の承認** 機能は既定で有効にする必要があります。 |
| 請求および価格設定 | 2603313 | 製品を含む見積もりと契約品目の追加を回避する重複レコード エラーを修正しました。 |
| 展開と構成 | 2611368 | 顧客は、最新のアプリ デザイナーを使用して、最大 5 つのユーザー定義エンティティをソリューションに追加できる必要があります。 |
| 時間と経費 | 2628285 | タイム エントリのインポート中に、正しいリソース カテゴリを設定する機能に影響する問題を修正しました。 |
| 営業案件管理| 2628815 | 見積もり行の詳細説明の文字数制限をタスクの件名の文字数制限に一致するように更新して、件名が 100 文字より長いタスクでインポートが成功するようにします。 |
| 時間と経費| 2629547 | プロジェクト承認の **送信者** フィールドは、レコードを送信したユーザーを指定する必要があります。 |
| 時間と経費| 2629865 | プロジェクトがコピーされたときの、タスクの **カテゴリをコピー** フィールド。 |
| 時間と経費| 2636463 | 最新の承認フォームの承認のフィルターを修正しました。 |
| プロジェクト計画および追跡 | 2648300 | プロジェクトの所有者が変更されない問題を修正しました。 |
| 請求および価格設定 | 2563000 | 通貨が契約通貨と異なる未請求売上の仕訳帳明細行は、許可しないでください。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) を参照してください。
