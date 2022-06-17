---
title: Project Service Automation 更新プログラム リリース 29、V3 の新機能と変更点
description: この記事では、Project Service Automation 更新プログラム リリース 29、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 733bbad53933b2de62222e78e3c5c919543c59e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915375"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Project Service Automation 更新プログラム リリース 29、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation V3 更新プログラム リリース 29 の機能と修正を一覧表示します。 このバージョンのビルド番号は V3.10.47.7 で、2021 年 2 月のセルフアップデートで一般提供されます。

## <a name="update-release-29"></a>更新プログラム 29

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:

- ユーザーは、時間入力グリッドで非稼働日に記録された作業時間を表示できません。
- 承認された経費エントリは、グリッド上で編集できます。

**プロジェクト管理**

以下の問題が修正されました:

- リソース割り当ての作業時間を確保するための検証ロジックが欠落していても、マイナスになることはありません。
- **AssignResourcesForTask** カスタムアクションは、変更されたフィールドだけでなく、すべてのフィールドを更新します。
- **CreateProject** イベントにプラグインまたはワークフローが登録されている環境でプロジェクトをコピーする場合、**CopyWBSToProject** が失敗すると、**msdyn_bulkgenerationstatus** 属性が更新されません。
- プロジェクト カレンダーを展開すると、稼働日日が昇順で並べ替えられないため、一部のプロジェクト タスクの更新が失敗します。
- 既存のプロジェクトでプロジェクト マネージャーを変更すると、組織単位が既定となるロジックがトリガーされます。

**営業**

以下の問題が修正されました:

- 契約行がない場合、**契約** ページの **契約履行** タブが初期化中にサイレントに失敗します。
