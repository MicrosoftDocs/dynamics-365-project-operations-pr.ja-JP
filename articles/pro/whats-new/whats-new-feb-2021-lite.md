---
title: 2021 年 2 月の新機能 - Project Operations のライト展開
description: このトピックでは、Project Operations のライト展開の 2021 年 2 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: df6490d3d9c28b095efd5ef856064de4b1517055
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272169"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>2021 年 2 月の新機能 - Project Operations のライト展開

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

  - Dataverse 環境バージョン 4.7.0.95 での Project Operations

## <a name="quality-updates"></a>品質更新プログラム

| **機能領域** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| **請求と価格** | 2053736 | 請求書明細行の詳細には、**請求書** > **関連情報** に移動することでアクセスできるようになりました。 |
| **請求と価格** | 2122613 | **アクティブ化** と **非アクティブ化** アクションが、**価格表** 関連付けエンティティから削除されました。 |
| **請求と価格** | 2128606 | **GetEstimatesForProject** プラグインの **ullReferenceException** の問題を解決しました。 |
| **展開と構成** | 2140569 | Dataverse Teams 環境にプロジェクト ソリューションをインストールしてはいけません。 |
| **展開と構成** | 2086991 | Web リソースのローカリゼーションのカスタマイズが制限されました。 |
| **営業案件管理** | 2136794 | **請求書の確認** または **請求書を支払済みとマーク** プロセスが失敗したときに、正しいエラーメッセージを表示します。 |
| **営業案件管理** | 2146376 | 請求対象外の実績の修正済み税額が、請求書確認から作成されます。 |
| **プロジェクトの計画と追跡** | 2099879 | Dataverse 環境展開では、静的 ID を使用して既定のトランザクションカテゴリを作成する必要があり、環境ごとにランダムに生成することはできません。 |
| **プロジェクトの計画と追跡** | 2128577 | リソース割り当てのトランザクション カテゴリを更新するための Project service ユーザー権限を修正しました。 |
| **プロジェクトの計画と追跡** | 2164035 | **プロジェクトのコピー** 関数の問題を修正しました。 |
| **時間エントリ** | 2129161 | 送信または承認された時間エントリをユーザーが変更および更新できないようにするために、より厳しい制限が適用されました。 |
| **時間エントリ** | 2103572 | プロジェクト以外の時間エントリの時間承認で、プロジェクト承認者のロールを探さなくなりました。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]