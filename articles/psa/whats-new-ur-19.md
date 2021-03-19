---
title: Project Service Automation 更新プログラム リリース 19、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 19、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280719"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation 更新プログラム リリース 19、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、PSA V3 更新プログラム 19 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.30.41 であり、2020 年 5 月のセルフ アップデートを通じて一般提供されました。

## <a name="update-release-19"></a>更新プログラム 19

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました: 

- 時間エントリのインポートから派生したエラーが正しく表示されません。
- 時間エントリ グリッドは **日付のみ** フィールドの動作をサポートしていません。
- プロジェクト リソースは、プロジェクトで経費を作成できません。

**プロジェクト管理**

以下の問題が修正されました: 

-  孫タスクでは、完了 (EAC) 計算中に誤った工数の推定が発生します。

**営業**

以下の問題が修正されました: 

- **再計算** アクションは、経費契約品目の詳細または見積依頼明細行の詳細では機能しません。
- **価格の更新** が、経費の見積もりに欠けています。
-  顧客は、**プロジェクト契約** ページからカスタム契約の状態の理由を選択できません。
- 見積もりからカスタム価格表を作成すると、パフォーマンスが低下します。
- **見積依頼明細行の詳細** ページと **契約品目の詳細** ページで **単位** の既定値に不整合が発生します。
- 請求不可トランザクション カテゴリ項目を請求可能な契約品目に追加しても、トランザクション カテゴリの **請求不可** の請求タイプは考慮されません。
- 顧客は、以前に作成された契約で新たに追加されたロールとカテゴリを使用できません。
- PreValidateProjectTeamMemberUpdate.cs でパフォーマンスの不要な取得が低下します
- **リソース カテゴリ** の一覧で請求不可として設定されたロールは、プロジェクトの契約品目で **請求可能ロール** タブに **請求不可** として追加する必要があります。
- **GetBookableResourceIdFromUser** がプライマリ ID だけでなく、予約可能なリソースのすべての列を取得するため、プロジェクトを作成するときに、パフォーマンスが低下する可能性があります。
- **TransactionType** エンティティに事前検証更新プラグインがないため、ユーザーがトランザクション タイプに対して無効な **単位** と **UnitGroups** を入力できません。
- **削除** ステップは、時間エントリのインポートでは機能しません。


[!INCLUDE[footer-include](../includes/footer-banner.md)]