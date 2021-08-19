---
title: 2021 年 5 月の新機能 - Project Operations ライト展開
description: このトピックは、Project Operations ライト展開の 2021 年 5 月リリースで利用可能な品質アップデートに関する情報を提供します。
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060439"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>2021 年 5 月の新機能 - Project Operations ライト展開

_適用対象: ライト展開 - 見積もり請求の取引_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

   - Dataverse 環境バージョン 4.10.0.186 での Project Operations。

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- [スケジュール モード](../../project-management/scheduling-modes.md): プロジェクト マネージャーは、固定期間、固定作業、または固定単位のスケジュール モードを使用してプロジェクトを管理する必要があるかどうかを定義できるようになりました。

## <a name="quality-updates"></a>品質更新プログラム

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求および価格設定 | 2224568 | 請求書確認プラグインの呼び出しを含むカスタマイズを可能にするロジックが追加されました。 |
| 請求および価格設定 | 2101098 | 見積もり請求書に対する既定フィールドのロジックを改善しました。 これらのフィールドには、**請求先住所**、**請求先氏名**、**支払条件** が含まれます。 フィールドは、対応するプロジェクト契約の顧客レコードから既定で設定されるようになりました。 |
| 請求および価格設定 | 2021413 | **タスク** エンティティの **実際のコスト** と **売上** フィールドが更新され、タスクの未請求および請求済み経費からの売上値が含まれるようになりました。 |
| 請求および価格設定 | 2182110 | プロジェクト契約をコピーするとき、契約品目 ID は、それが一意であることを保証するために、コピー先プロジェクト契約で再生成されます。 |
| 営業案件管理 | 2186741 | **発生元** フィールドとトランザクションの種類を確認するために追加された検証は、既存の見積もり行の詳細で更新できません。 |
| 営業案件管理 | 2191353 | マイルストーンの作成を、時間と材料の契約品目で許可しないでください。 |
| 営業案件管理 | 2216956 | **価格の更新** の問題を修正しました。 |
| 計画と追跡 | 2182979 | プロジェクト コピー機能が改善され、経費見積もり行が元のプロジェクトから確実にコピーされるようになりました。 |
| 計画と追跡 | 2184144 | プロジェクト コピー機能が改善され、リソース位置名が元のプロジェクトから確実にコピーされるようになりました。 |
| 計画と追跡 | 2184799 | コピーの進行中に推定開始日を変更できないように、プロジェクトをコピーするときの制御を強化しました。 |
| 計画と追跡 | 2185134 | プロジェクトのコピー中に、コピー先プロジェクトの推定開始日は、今日の日付に設定されます。 |
| 計画と追跡 | 2196373 | プロジェクト マネージャーとチーム メンバーのレコードが、プロジェクトをコピーするときに、プロジェクト チームで重複していないことを確認します。 |
| 計画と追跡 | 2211833 | リソースの割り当ては、ソース プロジェクト タスクからコピー先プロジェクトにコピーされます。 |
| 計画と追跡 | 2186541 | **リソース** 別にグループ化する場合の **見積り** グリッドの問題を修正しました。 |
| 計画と追跡 | 2166906 | タスクのトランザクション カテゴリを **リソース割り当て** エンティティにコピーする必要があります。 |
| リソース管理 | 2125362 | 時間ベースの割り当て方法を使用して汎用チーム メンバーを作成する際の問題を修正しました。 |
| 時間と経費 | 2113603 | **時間入力** ページから属性を削除する際のカスタマイズ関連の問題を修正しました。 システムは、スクリプトを使用して属性にアクセスする前に、属性がページに存在するかどうかを確認します。 |
| 時間と経費 | 2204377 | **週のコピー** を選択すると、コピーしたタイムシートが自動的に表示されます。 |
| 時間と経費 | 2209059 | Dynamics 365 Field Service の時間エントリでは **ステータス** フィールドを編集できます。 |