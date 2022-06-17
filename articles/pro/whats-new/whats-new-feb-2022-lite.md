---
title: 2022 年 2 月の新機能 - Project Operations のライト展開
description: この記事では、Project Operations ライト展開の 2022 年 2 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922826"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>2022 年 2 月の新機能 - Project Operations のライト展開

_適用対象: ライト展開 - 見積もり請求の取引_

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.28.0.120 の Project Operations

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースの時点で、1 つのプロジェクトに最大 300 人のチーム メンバーを追加できます。 以前は、チーム メンバー数の制限は 150 人でした。 詳細については、[プロジェクトの制限](../../project-management/create-wbs.md#project-limitations) を参照してください。

## <a name="quality-updates"></a>品質更新プログラム

| 機能 | 照合番号 | 品質更新プログラム |
| --- | --- | --- |
| 請求および価格設定 | 2497369 | 材料の修正は、**修正** パラメーターの日付値に従う必要があります。 |
| 請求および価格設定 | 2498697 | **時間エントリのリコール** のセキュリティ構成を改善しました。 |
| 請求および価格設定 | 2517455 | **更新された請求書行のトランザクション** アクションは、同じ請求書に対してアクションを複数回同時にトリガーできません。 |
| 請求および価格設定 | 2517465 | **請求書行の詳細を非アクティブ化する** アクションはサポートされていないためブロックされています。 |
| 請求および価格設定 | 2556660 | プロジェクト パラメーター レコードに添付されている価格表で実行される日付有効性チェックを修正しました。 |
| 営業案件管理 | 2369202 | 重複している有効日がある価格表を同じプロジェクト契約に添付できることを確認するビジネス ロジックを修正しました。 |
| 営業案件管理 | 2385965 | **保存して閉じる** を選択したときの **プロジェクト契約** ページの **顧客** タブにある動作を修正しました。 |
