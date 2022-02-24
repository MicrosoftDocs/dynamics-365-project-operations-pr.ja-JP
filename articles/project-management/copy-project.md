---
title: プロジェクトのコピー
description: このトピックでは、Dynamics 365 Project Operations のプロジェクトのコピーについて説明します。
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479525"
---
# <a name="copy-a-project"></a>プロジェクトのコピー

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations では、**プロジェクト** フォームで **プロジェクトのコピー** を選択することで新しいプロジェクトをすばやく構築できます。 プロジェクトをコピーするには、コピーするプロジェクトを開き、**プロジェクトのコピー** を選択します。 操作は以下をコピーします:

- プロジェクトのプロパティ (推定開始日はソース プロジェクトからコピーされます)
- WBS(作業分解構造)
- プロジェクト チーム メンバー
- プロジェクト見積もり
- プロジェクト経費の見積もり

## <a name="project-properties"></a>プロジェクト プロパティ

プロジェクトがコピーされると、次のフィールドの値がコピーされます:

- 件名
- 内容
- 顧客
- カレンダー テンプレート
- 通貨
- 契約単位
- プロジェクト管理者
- ステータス
- 全体的なプロジェクトの状態
- コメント
- 見積もり
- 開始予定日
- 終了日
- 工数 (時間)
- 見積もり労務コスト
- 見積もり経費

## <a name="work-breakdown-structure"></a>WBS (作業分解構造)

プロジェクトがコピーされると、ロードされたリソース WBS(作業分解構造) 全体がコピーされます。 名前付きリソースは汎用リソースによって置き換えられます。 名前付きリソースの作業時間が汎用リソースと同じでない場合、スケジュールが再計算され、タスクの期間が変更される可能性があります。

## <a name="project-team-members"></a>プロジェクト チーム メンバー

プロジェクト チームがソース プロジェクトからコピーされると、汎用リソースがコピーされます。 汎用リソースの割り当ては、ソース プロジェクトと同様に維持されます。 名前付きリソースは、汎用チーム メンバーに変換されます。

## <a name="estimates"></a>見積もり

プロジェクトがコピーされると、リソースおよび経費見積品目の両方がソース プロジェクトからコピーされます。 

コピー プロジェクトにプログラムでアクセスする方法については、[コピー プロジェクトでプロジェクト テンプレートを開発する](dev-copy-project.md)を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
