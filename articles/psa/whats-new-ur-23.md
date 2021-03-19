---
title: Project Service Automation 更新プログラム リリース 23、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 23、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 379379ff643baa10417333b4be5e56d56eb5bc26
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280539"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation 更新プログラム リリース 23、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 23 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V 3.10.34.30 であり、一般的には 2020 年 8 月の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-23"></a>更新プログラム 23

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:
- **プロジェクト チーム メンバーの削除** のエッジ ケースを処理して、意味のある例外を提供します。
- 割り当てをインポートすると、削除画面が空白になります。

**リソース管理**

以下の問題が修正されました:

- タイム スケールが 5 日を超えると、**リソース稼働率グリッド リソース カード** に誤ったデータが表示されます。
- 顧客が予約可能リソースを作成すると、プラグインは断続的にリソースを Microsoft Office 365 グループ に自動的に追加できません。
- **調整** ビューでは、**週** や **月** ビューに手動の配分型が正しく表示されません。

**プロジェクト管理**

以下の問題が修正されました:

- **RetrieveMultiple for usersettings** エンティティの数が多すぎると、プロジェクト承認やその他の操作のパフォーマンスが低下します。
- **タスク計画** グリッドのリソース検索では、プロジェクト チームから最大 5 人のチーム メンバーのみを表示するように制限されています。 
- **タスク計画** グリッドのリソース検索では、非アクティブなリソースをフィルタリングしません。
- 手動モードは、プロジェクト計画 WBS (作業分解構造) で予想どおりに機能していません。
- **タスク計画** グリッドには、**非アクティブなトランザクション カテゴリ** が表示されます。
- タスクに複数の割り当てがある場合、**リソース割り当て** グリッドは正しく丸められません。
- 丸め値は、1 つのタスクの計画コストと実際コストで異なります。

**営業**

以下の問題が修正されました:

- **すべてのトランザクション カテゴリの取得** のダブルクリックで、複数行を作成します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]