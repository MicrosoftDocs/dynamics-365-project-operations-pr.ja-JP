---
title: 期間タイプ
description: このトピックでは、売上見積もりに対する期間タイプを設定する方法について説明します。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531473"
---
# <a name="period-types"></a>期間タイプ

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

期間タイプはプロジェクトの売上を見積もる頻度を定義します。 このトピックでは、売上見積もりに対する期間タイプを設定する方法について説明します。 

## <a name="create-and-work-with-period-types"></a>期間タイプを作成して操作する
期間タイプの作成と操作には、以下の手順を実行します。

1. Dynamics 365 Finance 環境で **プロジェクト管理と会計** > **設定** > **見積もり** > **期間タイプ** を順に選択します。
2. **新規** を選択して新しい期間タイプを作成します。 名前と説明を入力します。
3. **頻度** フィールドで値を選択します。

    - **毎週**、**隔週**、**半月ごと**、**毎月**、**毎日**、**四半期ごと**、**毎年** を選択すると、このカレンダーを期間の生成に使用します。 
    - **元帳期間** を選択すると、一般会計を構成する元帳期間を期間の生成に使用します。
    - **無制限** を選択した場合、カスタム期間を指定できます。
4. 期間タイプ レコードを選択してから **期間の生成** を選択して期間タイプの期間を作成します。 選択した期間頻度に基づいて、開始日や生成する期間の数を指定するオプションを利用できる場合があります。
5. **期間** を選択して生成した期間を確認します。

