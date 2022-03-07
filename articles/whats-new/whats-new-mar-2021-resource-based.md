---
title: 2021 年 3 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオ向け Project Operations の 2021 年 3 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006342"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 3 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

- Dataverse 環境バージョン 4.8.0.91 での Project Operations 
- Dynamics 365 Finance 環境バージョン 10.0.16 でのプロジェクト管理および会計 

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations


| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求および価格設定 | 2133873 | **経費の見積もり** グリッドの **販売単価** の通貨記号の表示を修正しました。 |
| 請求および価格設定 | 2174616 | 見積もりが通って成約すると、見積もりからコピーされた契約品目の詳細で契約カスタム価格表が参照されます。 |
| 営業案件管理 | 2167475 | 未請求の実績エントリを作成した修正請求書の税額を修正しました。 |
| 営業案件管理 | 2176285 | 税額は、売買契約/見積明細行の詳細から原価契約/見積明細行の詳細にコピーしてはいけまｓねん。 |
| 営業案件管理 | 2188079 | 作業ベースでない契約に対しては、分割請求ルールを作成しないでください。 |
| 計画と追跡 | 2125274 | **プロジェクト開始日のマッピング** の **プロジェクト デュアル書き込みマップ** 属性が、**msdyn\_taskearlieststart** から **msdyn\_actualstart** に更新されました。 |
| 計画と追跡 | 2138853 | プロジェクト コピー機能が更新され、タスクを参照する経費見積行がコピー先のプロジェクトに確実にコピーされるようになりました。 |
| 計画と追跡 | 2154306 | リソースベースのシナリオの Project Operations で経費見積もりを削除する際の問題を修正しました。 |
| 計画と追跡 | 2173259 | プロジェクト コピー機能が更新され、特定のシナリオでの **WBS のコピー** エラーメッセージが表示されなくなりました。 |
| 時間と経費 | 2148910 | **時間入力** グリッドの **エントリの編集** ページの表示に関する問題が修正されました。 |
| 時間と経費 | 2159798 | 承認された経費エントリを編集できないようにするための管理が厳格化されました。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance のプロジェクト管理および会計

詳細については、[2021 年 1 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations](whats-new-jan-2021-resource-based.md)を参照してください。

## <a name="regulatory-updates"></a>規制の更新

Finance and Operations アプリの規制の更新については、[規制の更新](/dynamics365/finance/localizations/regulatory-updates) を参照してください。 規制の更新について学ぶもう 1 つの方法は、LCS にログインし、問題検索ツールを使用して計画された規制の更新を表示することです。 問題検索では、国、機能の種類、リリースで検索できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]