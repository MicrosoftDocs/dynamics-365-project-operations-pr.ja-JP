---
title: プロジェクトベースの契約品目への見積もりのインポート
description: このトピックでは、財務見積もりをプロジェクトから契約品目にインポートする方法について説明します。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9ac367baba4529e86a42d812b7d9b2550812e297
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079501"
---
# <a name="importing-an-estimate-to-a-project-based-contract-line"></a>プロジェクトベースの契約品目への見積もりのインポート

_**適用対象:** ライト展開 - 見積もり請求の取引_

Dynamics 365 Project Operationsでは、見積もりをプロジェクトからプロジェクトベースの契約品目にインポートできます。

1. プロジェクトベースの契約品目にある **プロジェクト** フィールドが入力されていることを確認します。
2. **契約品目の詳細** タブのサブグリッドで、 **ププロジェクトの見積もりからインポート** を選択します。 集計オプションのあるダイアログ ページが開きます。 使用可能な集計オプションは、 **トランザクション クラス** 、 **カテゴリ** 、 **ロール** 、 **プロジェクト タスク** です。
3. 集計選択に基づいて、この契約品目に含まれるすべてのトランザクション クラスとタスクに対するプロジェクトからの見積もりがコピーされます。 どのトランザクション クラスが含まれているかを確認するには、プロジェクトベースの契約品目にある **全般** タブで、 **時間を含む** 、 **経費を含む** 、 **料金を含む** フィールドの値を確認します。 
4. どのタスクが含まれているかを確認するには、契約品目の **請求可能タスク** タブを選択します。 **含まれるトランザクション クラス** フィールドが **はい** に設定されている関連タスクに基づいて、これらのタスクとトランザクション クラスの組み合わせに対する見積もりのすべてが契約品目にインポートされます。

見積もりをインポートすると、システムは、契約に添付されたプロジェクト価格表と、契約品目で設定された請求の種類に基づいて価格を既定で設定します。 契約品目でタスク、ロール、またはカテゴリが請求不可として設定されている場合、インポートされた見積行は請求不可であり、契約品目の契約金額に加算されません。

契約品目に明細行の詳細がある場合、契約品目の **契約金額** と **予測税額** フィールドは集計され、編集できません。

複数の集計オプションが選択されると、システムは選択されたすべてのオプションで集計を試みます。 集計出力では、集計オプションを 1 つだけ選択した場合よりも、インポートされた契約品目が多くなります。

たとえば、プロジェクトに次の経費の見積行がある場合:

| タスク​ | カテゴリ | 日 | 数量 | 出荷単位価格 | 金額 |
| --- | --- | --- | --- | --- | --- |
| タスク A | 航空運賃 | 10/1/2020 | 4 | 400 | 1600 |
| タスク B | 宿泊 | 10/1/2020 | 4 | 200 | 800 |
| タスク C | 宿泊 | 11/1/2020 | 2 | 200 | 400 |

ユーザーが **トランザクション クラス** 別に集計することを選択すると、次の情報がインポートされます:

| タスク​ | カテゴリ | 日 | 数量 | 出荷単位価格 | 金額 |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

ユーザーが **トランザクション クラス** と **カテゴリ** 別に集計することを選択すると、次の情報がインポートされます:

| タスク​ | カテゴリ | 日 | 数量 | 出荷単位価格 | 金額 |
| --- | --- | --- | --- | --- | --- |
| タスク A | 航空運賃 | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| 宿泊 | 10/1/2020 | 6 | 200 | 1200 |

ユーザーが **トランザクション クラス** 、 **カテゴリ** 、 **リーフ ノード タスク** 別に集計することを選択すると、次の情報がインポートされます。 この結果は、プロジェクトの結果と同じであることに注目してください:

| タスク​ | カテゴリ | 日 | 数量 | 出荷単位価格 | 金額 |
| --- | --- | --- | --- | --- | --- |
| タスク A | 航空運賃 | 10/1/2020 | 4 | 400 | 1600 |
| タスク B | 宿泊 | 10/1/2020 | 4 | 200 | 800 |
| タスク C | 宿泊 | 11/1/2020 | 2 | 200 | 400 |