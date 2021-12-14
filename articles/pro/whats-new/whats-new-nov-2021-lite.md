---
title: 2021 年 11 月のニュース - Project Operations のライト展開
description: このトピックは、リソース/非在庫ベースのシナリオの Project Operations のライト導入の 2021 年 11 月リリースで利用可能な品質更新に関する情報を提供します。
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e8560e7c7d6bae1bb2fda389a63bde1c57654bcb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827287"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>2021 年 11 月のニュース - Project Operations のライト展開

_適用対象: ライト展開 - 見積もり請求の取引_

このトピックは、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます:

- Dataverse 環境バージョン 4.26.0.145、4.26.0.148、または 4.26.0.150 の Project Operations
  
## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- プロジェクト スケジューリングアプリケーションプログラミングインターフェイス（API）は、プロジェクトバケットを作成および削除する機能をサポートするようになりました

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-in-dataverse"></a>Dataverse の Project Operations

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求と価格 | 2358236 | 請求書の修正では、ゼロ価格の行がある修正を許可する必要がある。 |
| リソース管理 | 2410072 | プロジェクト マネージャーとしてタスクに割り当てられたリソースのセットアップができるようになる。 |
| 請求と価格 | 2430234 | コスト パフォーマンス計算の問題を修正。 |
| 時間と経費 | 2436978 | hh:mm 形式で時間を入力できるようになる。 |
| 請求と価格 | 2448623 | 価格表が組織単位に関連付けられた後に更新できるようになる。 |
| 時間と経費 | 2460396 | セルをクリアして、時間エントリを削除できるようになる。 |
| 請求と価格 | 2467386 | タスクが落札見積もりに関連付けられている場合でも、タスクのあるプロジェクトを削除できるようになる。 |
| 時間と経費 | 2461744 | **失敗した承認** ビューには、**提出済み** ステージのプロジェクト承認のみが含まれる。 |
| 時間と経費 | 2464082 | 対象ステータスが一致したら、プロジェクト承認から承認セットへのリンクを削除する。 |
| 時間と経費 | 2468108 | スケジュール ジョブは承認セットの **処理** ステータスを設定すべきではない。 |
| 時間と経費 | 2471503 | 7 日経過した承認セットを削除する。 |
| 請求と価格 | 2480687 | 見積もり明細のマイルストーンを作成するときに、見積もり明細の参照を削除すべきではない。 |
