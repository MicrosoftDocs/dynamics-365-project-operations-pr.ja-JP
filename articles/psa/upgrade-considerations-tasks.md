---
title: WBS (作業分解構造) のアップグレードに関する考慮事項
description: このトピックでは、「Project Service Automation 2.x から 3.x. へ」 の WBS (作業分解構造) をアップグレードする方法に関して説明します。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149549"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>WBS (作業分解構造) のアップグレードに関する考慮事項

[!include [banner](../includes/psa-now-project-operations.md)]

このトピックでは、「Project Service Automation 2.x から 3.x. へ」 の WBS (作業分解構造) をアップグレードする方法に関して説明します。 このトピックでは、アップグレードを完了するのに必要な Project Service Automation (PSA) のプロジェクトについて、正常な条件を定義します。 ここには、アップグレードが失敗する一般的なブロック条件についての詳細が含まれます。 プロジェクト スケジュールのプロジェクト タスクおよび機能の定義に関する詳細は、[プロジェクト スケジュール](project-creating.md) を参照してください。

## <a name="key-entities"></a>主要なエンティティ
リソースでロードされている正確な WBS (作業分解構造) に関して、次のエンティティが必要です。

- [プロジェクト](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [プロジェクト チーム](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [プロジェクト タスク](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [リソース割り当て](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [プロジェクト タスクの依存関係](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [予約可能リソース](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

WBS (作業分解構造) がロードされたリソースを定義するには、次の手順を完了する必要があります。

1. 新しいプロジェクトを作成する 新規プロジェクトの作成方法については、[msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)を参照してください。
2. 1 つ以上のタスクを作成する。 タスクの作成方法については、[msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)を参照してください。
3. タスクの依存関係を定義します。 詳細については、 [プロジェクト タスクの依存関係](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency) を参照してください。
4. プロジェクト チーム メンバーをプロジェクトに割り当てます。 詳細については、[msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam) を参照してください。
5. プロジェクト チーム メンバーをタスクに割り当てます。 詳細については、 [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment) を参照してください。

## <a name="project-team-relationships"></a>プロジェクト チームの関連付け

アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:
- すべてのプロジェクト チームのメンバーを、予約可能リソースに関連付ける必要があります。
- すべてのプロジェクト チームのメンバーを、同一のプロジェクトに関連付ける必要があります。 

## <a name="project-task-relationships"></a>プロジェクト タスクの関連付け
アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:

- 関連するタスクはすべて、同一のプロジェクトに関連付ける必要があります。
- すべての行タスク対して親タスクが必要です。
- すべてのタスクに対して親プロジェクトが必要です。

### <a name="valid-conditions"></a>有効な条件

- すべてのタスクの期間は、1 時間以上、1,800,000 分未満 (1,250 日) である必要があります。*
- すべてのタスクは、開始日を 2000/01/01 より後に設定されている必要があります。*
- すべてのタスクは、現在の日付の 18 年以上前である必要があります。*
- すべてのタスクは、完了日かそれよりも前に開始日を持つ必要があります。
- 分類上のすべてのトランザクションの種類 (経費、資料、税、および時間) には、**既定の単位** および **出荷単位** の値が必要です。
- 日付の書式に文字を使用することは避けてください。

### <a name="potential-mitigation-steps"></a>潜在的緩和措置
- 詳細検索を使用して、プロジェクトIDを含んでいないプロジェクト タスクを識別します。
- 高度な検索を使用して、スケジュールされた期間が > 1,800,000 よりも大きいプロジェクト タスクを識別します。
- データを変更する前に、データが不良な状態となった原因として考えられるエンティティに関連付けられている カスタマイズ を調査する必要があります。 これらのカスタマイズは、データに関連する更新を進める前に対処する必要があります。
- 孤立状態であると識別されたタスクについては、当該タスクが不要な場合、あるいは適切な親プロジェクトに関連付ける必要がある場合は、削除することを検討してください。
- 期間が 1,250日 を超えるタスクについては、可能であれば、合計期間を表す複数のタスクを追加することを検討してください。

> [!NOTE]
> アスタリスク (\*) が付いている項目には制限がありますが、これは顧客リレーションシップ マネジメント (CRM) が 7,320 回の繰り返し拡張機能のみに対応しているためです。 ユーザーはこの制限を受け入れる必要があります。

## <a name="resource-assignment-relationships"></a>リソース割り当ての関連付け
アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:

- 作業分解構造 でのすべてのリソースの割り当ては、同一のプロジェクトに関連付けられている必要があります。
- 作業分解構造のすべてのリソースの割り当ては、同一のプロジェクトのプロジェクト チーム メンバーに関連付けられている必要があります。

### <a name="potential-mitigation-steps"></a>潜在的緩和措置
- 上記の条件に当てはまらないすべてのタスクを特定します。  
- 既に有効ではないリソースの割り当てはすべて削除する必要があります。

## <a name="project-task-dependency-relationships"></a>プロジェクト タスク依存関係の関連付け
アップグレードを正常に実行するには、次の関連付けを正常に維持する必要があります:

- すべてのプロジェクト タスクの依存関係は、同一のプロジェクトに関連付ける必要があります。
- タスクでは、参照済みの同一の依存関係を複数回使用することはできません。
