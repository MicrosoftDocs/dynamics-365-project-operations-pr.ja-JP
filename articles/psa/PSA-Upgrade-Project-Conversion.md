---
title: Project Service Automation から Project Operations への機能変更
description: この記事では、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Project Operations への機能変更の概要について説明します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621237"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Project Service Automation から Project Operations への機能変更

プロジェクトが正常に Microsoft Dynamics 365 Project Service Automation 3.X から Dynamics 365 Project Operations Lite にアップグレードされた後、タスク グリッドの作業分解構造 (WBS) でプロジェクト タスクを編集することはできません。 顧客は、タスクに関連するすべての詳細を提供するために新しいフィールドが追加された追跡グリッドで WBS を確認できます。 WBS への編集が必要なプロジェクトの場合、対象プロジェクトを新規 Project for the Web スケジュール設定エクスペリエンスに選択的に変換できます。

## <a name="project-conversion-process"></a>プロジェクト変換プロセス

プロジェクトを変換するには、以下の手順に従ってください。

1. プロジェクトのメイン ページを開き、アクション ペインで **変換** を選択します。
1. 確認メッセージボックスで **OK** を選択して、プロジェクトの変換を開始します。 次のアクションが発生します。

    1. プロジェクトのメイン ページに表示されるメッセージ バーには、次のように表示されます: 「プロジェクト スケジュールは変換中です。 変換が完了するまで、プロジェクトに変更を加えることはできません。」
    1. プロジェクト リストにリダイレクトされます。

    プロジェクトの変換が完了すると、次のアクションが発生します:

    1. 割り当てられたプロジェクト マネージャーは、アプリケーションの右側に通知を受け取ります。
    1. 変換が進行中であることを通知するメッセージ バーが削除されます。
    1. **スケジュール** タブには、Project for the web での新しいスケジュール設定エクスペリエンスが表示されます。 適切なライセンスとセキュリティ ロールを持つすべてのユーザーが WBS を編集できます。
    1. **スケジュール エンジン** フィールドが **Project for the web** に更新されます。
    1. **変換** ボタンがアクション ペインから削除されます。

> [!IMPORTANT]
> プロジェクトの一括変換はできません。 大量のプロジェクトを同時に更新しようとすると調整されます。 この制限は、すべての顧客に高いパフォーマンスを提供するのに役立ちます。

## <a name="manual-tasks-vs-automatic-tasks"></a>手動タスクと自動タスク

環境が Project Service Automation から Project Operations にアップグレードされると、WBS 内のすべてのタスクが自動的にスケジュールされたと見なされます。 手動でスケジュールされたタスクの概念は、Project for the web では使用できません。 ただし、プロジェクトの優先スケジュール動作を定義するには、新規プロジェクトの作成時に [スケジュール モード](/project-management/scheduling-modes.md) 設定を使用します。

## <a name="restricted-operations-for-pre-conversion-projects"></a>変換前プロジェクトの制限付き操作

このセクションでは、プロジェクトが変換されていない場合に予想される機能の違いについて説明します。

### <a name="copy-project"></a>プロジェクトのコピー

**コピー** 操作は、変換されたプロジェクトでのみサポートされます。 アップグレードされたプロジェクトは、変換前にコピーできません。

### <a name="move-project"></a>プロジェクトの移動

プロジェクトの開始日を変更しても、プロジェクトが変換されていない限り、タスクの開始日は比例して移動しません。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>変換されたプロジェクトと、アップグレードの完了後に作成された新しいプロジェクトの違いは何ですか?

環境がアップグレードされた後に変換されたプロジェクトの場合、プロジェクト カレンダーのみを尊重するようスケジュールに指示するフラグが設定されます。 この動作は、Project Service Automation の動作と一致します。 ただし、アップグレード後に作成された新しいプロジェクトにはフラグが設定されません。 したがって、リソースがタスクに割り当てられると、スケジュールはリソースの作業時間を尊重します。

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>プロジェクトの変換に失敗した場合はどうすればよいですか?

プロジェクトの変換に失敗した場合、まずエラー ログを確認して、WBS に関連する一般的な問題を特定します。 対処できる特定のエラーがログにない場合は、カスタマー サポートに連絡して、ケースをさらに検討してください。

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Project for the web では、休業日はどのように処理されますか?

Project for the web は、企業が組織レベルで定義する休業日を尊重しません。 ただし、特定の勤務時間テンプレートで定義されている他の種類の休日は尊重されます。

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the web の制限は何ですか?

[WBS (作業分解構造) の作成: プロジェクトの制限](/project-management/create-wbs#project-limitations.md) を参照してください。

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>コストと売上の見積もりに変更はありますか?

リソース割り当て配分型が再計算された場合や、ソース プロジェクトとは異なる日付境界に該当する場合は、まれに、売上とコストの見積もりに違いが見られる場合があります。 アップグレード プロセスの一環として、お客様は、潜在的なスケジュール変更を理解できるように、プロジェクトの代表的なサンプル セットをテストすることが期待されています。
