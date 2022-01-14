---
title: 2021 年 12 月のニュース - Project Operations lite の展開
description: このトピックは、リソース/非在庫ベースのシナリオの Project Operations lite の導入の 2021 年 12 月リリースで利用可能な品質更新に関する情報を提供します。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942983"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>2021 年 12 月のニュース - Project Operations lite の展開

_適用対象: ライト展開 - 見積もり請求の取引_

このトピックは、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます:

- Dataverse 環境のバージョン 4.27.0.195、4.27.0.242 の Project Operations


## <a name="features-included-in-this-release"></a>このリリースが含む機能

### <a name="subcontract-management"></a>外注管理 

- [外注プロジェクトチーム メンバー](../subcontracting/subcontracting-project-team-members.md)：プロジェクト マネージャーは、人員配置と見積もりに影響を与える外注および外注ラインを備えた指名された、または汎用チームメンバーを作成できます。
- [プロジェクト チームメンバーの外注オプション](../subcontracting/subcon-options.md): 指名された、または汎用プロジェクトチームメンバーの人員配置を選択する場合、プロジェクト マネージャーは、既存の外注契約を確認したり、1人以上のプロジェクトチームメンバーの新しい外注契約を作成したりできます。 
- [外注リソース割り当てのコスト見積もり](../subcontracting/costing-subcon-ra.md): プロジェクトコストの見積もりでは、外注のリソース割り当てが考慮され、外注に関連付けられた購入価格表を使用してコストが計算されます。 
- [契約労働者と外注能力を表示するようにスケジュールボードを構成する](../subcontracting/configure-sb-subcon.md)：Project Operations のスケジュールボードを構成して、契約社員タイプの予約可能なリソースと外注のキャパシティを従業員とともに検索して提案できるようになりました。 この構成は、特定のプロジェクト要件の人員配置のコンテキスト内でリソースを検索する場合、またはプロジェクト要件のコンテキスト外で検索する場合に適用できます。
- [契約労働者と外注のキャパシティをプロジェクトに配置する](../subcontracting/staffing-cw.md): 契約労働者は、スケジュール ボードの経験を活用したプロジェクトで予約できるようになりました。
- [外注部品のプロジェクトでの時間、費用、材料使用量の記録](../subcontracting/recording-subcon-actuals.md): 契約労働者は時間と費用を記録でき、プロジェクト チームメンバーはプロジェクトの外注を使用して購入した資材の使用状況も記録できます。 これにより、購入したキャパシティまたは材料を使用するプロジェクトの正確なコストが記録されます。
- [外注の状態遷移](../subcontracting/subcon-states.md): 外注は、ベンダーとの交渉を完了するために確認するか、納品の完了を示すために閉じるか、納品が完了する前にベンダーとの契約の終了を示すためにキャンセルすることができます。

### <a name="task-planning"></a>タスクの計画
- システム管理者向けトラブルシューティングを改善しました。 ユーザーがプロジェクトを開くことができない場合、管理者は Project for the Web から生成された[プロジェクト スケジュール ログ](../../project-management/schedule-api-logs.md)の関連エラーで確認することができます。
- [Microsoft Project for the Web のタスク チェック リストを使用する](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)。 Microsoft Project for the Webでは、タスクにチェックリストを追加して、特定の項目を追跡できます。

## <a name="quality-updates"></a>品質更新プログラム

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 計画と追跡 | 2392596 | スケジュールAPIで、 **残りの作業**、**完了した作業**、**% 完了** の各フィールドを更新できるようになりました。 |
| 計画と追跡 | 2478497 | スケジュール API の **アクティビティ番号** と **タスク ID** のフィールドは、システムが自動採番で入力するため、入力時に空白にすることができます。|
| 時間と経費 | 2468135 | 承認の再試行回数が 5 回から 3 回に減りました。 |
| 時間と経費 | 2468188 | **注釈** エンティティの **notetext** 属性で、ログテキストが最大長を超える問題を修正しました。 |
