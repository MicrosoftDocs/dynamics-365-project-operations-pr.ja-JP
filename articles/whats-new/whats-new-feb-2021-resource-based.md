---
title: 2021 年 2 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事は、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 2 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 38fede1746bcb09700c9c9c5e20653e0c39fea2a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910647"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 2 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事は、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます。

- Dataverse 環境 4.7.0.95 での Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.16 でのプロジェクト管理と会計 

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能領域** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| **請求と価格** | 2053736 | 請求書明細行の詳細には、**請求書** > **関連情報** に移動することでアクセスできるようになりました。 |
| **請求と価格** | 2122613 | **アクティブ化** と **非アクティブ化** アクションが、**価格表** 関連付けエンティティから削除されました。 |
| **請求と価格** | 2128606 | **GetEstimatesForProject** プラグインの **ullReferenceException** の問題を解決しました。 |
| **展開と構成** | 2139346 | アンマネージド **Dynamics365ProjectOperationsDualWrite** ソリューションのインポートに関する問題を解決しました。 |
| **展開と構成** | 2140569 | Dataverse Teams 環境にプロジェクト ソリューションをインストールしてはいけません。 |
| **展開と構成** | 2086991 | Web リソースのローカリゼーションのカスタマイズが制限されました。 |
| **営業案件管理** | 2136794 | **請求書の確認** または **請求書を支払済みとマーク** プロセスが失敗したときに、正しいエラーメッセージを表示します。 |
| **営業案件管理** | 2139330 | プロジェクトのプロジェクト マネージャーを変更しても、所有する会社を既定値にリセットしてはなりません。 |
| **営業案件管理** | 2146376 | 請求対象外の実績の修正済み税額が、請求書確認から作成されます。 |
| **プロジェクトの計画と追跡** | 2099879 | Dataverse 環境展開では、静的 ID を使用して既定のトランザクションカテゴリを作成する必要があり、環境ごとにランダムに生成することはできません。 |
| **プロジェクトの計画と追跡** | 2128577 | リソース割り当てのトランザクション カテゴリを更新するための Project service ユーザー権限を修正しました。 |
| **プロジェクトの計画と追跡** | 2164035 | **プロジェクトのコピー** 関数の問題を修正しました。 |
| **時間エントリ** | 2129161 | 送信または承認された時間エントリをユーザーが変更および更新できないようにするために、より厳しい制限が適用されました。 |
| **時間エントリ** | 2103572 | プロジェクト以外の時間エントリの時間承認で、プロジェクト承認者のロールを探さなくなりました。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要 

Dynamics 365 Finance でのプロジェクト管理と会計の詳細については、[2021 年 1 月新機能 - リソース/非在庫ベースのシナリオ向け Project Operations](whats-new-jan-2021-resource-based.md) を参照してください。


## <a name="regulatory-updates"></a>規制の更新

財務と運用アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 規制の更新について学ぶもう 1 つの方法は、Lifecycle Services (LCS) にログインし、問題検索ツールを使用して計画された規制の更新を表示することです。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]