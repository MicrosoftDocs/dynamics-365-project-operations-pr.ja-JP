---
title: プロジェクトのコピー
description: このトピックでは、Dynamics 365 Project Operations のプロジェクトのコピーについて説明します。
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574436"
---
# <a name="copy-a-project"></a>プロジェクトのコピー

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations では、**プロジェクト** フォームで **プロジェクトのコピー** を選択することで新しいプロジェクトをすばやく構築できます。 プロジェクトをコピーするには、コピーするプロジェクトを開き、**プロジェクトのコピー** を選択します。 アクションは以下をコピーします:

- プロジェクト プロパティ 
- WBS (作業分解構造)
- プロジェクト チーム メンバー
- プロジェクト見積もり
- プロジェクト経費の見積もり
- プロジェクトの材料の見積もり
- プロジェクト チェックリスト
- プロジェクト バケット

## <a name="project-properties"></a>プロジェクト プロパティ

プロジェクトがコピーされると、次のフィールドの値がコピーされます。

| Field | 非在庫材料向け Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| 件名 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 説明設定 | :heavy_check_mark: | :heavy_check_mark: | |
| 大変お世話になっております | :heavy_check_mark: | :heavy_check_mark: | |
| カレンダー テンプレート | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Currency | :heavy_check_mark: | :heavy_check_mark: | |
| 契約単位 | :heavy_check_mark: | :heavy_check_mark: | |
| 所有会社 | :heavy_check_mark: | | |
| プロジェクト管理者 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| 全体的なプロジェクトの状態 | :heavy_check_mark: | :heavy_check_mark: | |
| Comments | :heavy_check_mark: | :heavy_check_mark: | |
| 見積もり | :heavy_check_mark: | :heavy_check_mark: | |
| <p>開始予定日</p><p><strong>メモ:</strong> このフィールドは、プロジェクトがコピーから作成された日付を指定します。 | :heavy_check_mark: | :heavy_check_mark: | |
| <p>推定終了日</p><p><strong>メモ:</strong> このフィールドの日付は、コピーから作成された新しいプロジェクトの開始日に基づいて調整されます。</p> | :heavy_check_mark: | :heavy_check_mark: | |
| 工数 (時間) | :heavy_check_mark: | :heavy_check_mark: | |
| 労務コスト見積 | :heavy_check_mark: | :heavy_check_mark: | |
| 経費見積 | :heavy_check_mark: | :heavy_check_mark: | |
| 材料コスト見積 | | :heavy_check_mark: | |

> [!NOTE]
> プロジェクトのコピーは時間がかかります。 プロジェクト レコード、それらの関連属性、および多くの関連エンティティもコピーされます。 操作は長時間実行されるため、コピーが開始されると、コピー操作が完了するまで、ターゲット プロジェクト ページは編集用にロックされます。

## <a name="work-breakdown-structure"></a>WBS (作業分解構造)

プロジェクトがコピーされると、ロードされたリソース WBS(作業分解構造) 全体がコピーされます。 名前付きリソースは汎用リソースによって置き換えられます。 名前付きリソースが汎用リソースと同じ勤務時間でない場合、スケジュールは再計算され、タスクの所要時間が変更される可能性があります。

## <a name="project-team-members"></a>プロジェクト チーム メンバー

プロジェクト チームがソース プロジェクトからコピーされると、汎用リソースがコピーされます。 汎用リソースの割り当ては、ソース プロジェクトと同様に維持されます。 名前付きリソースは、汎用チーム メンバーに変換されます。

> [!NOTE]
> チームメンバーと割り当ては、Project for the Web にコピーされません。

## <a name="estimates"></a>見積もり

プロジェクトがコピーされると、リソース、経費、材料の見積もり行がソース プロジェクトからコピーされます。 

コピー プロジェクトにプログラムでアクセスする方法については、[コピー プロジェクトでプロジェクト テンプレートを開発する](dev-copy-project.md)を参照してください。

## <a name="quotes-and-contracts"></a>見積もりと契約

見積もりと契約は、宛先プロジェクトにリンクされていません。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
