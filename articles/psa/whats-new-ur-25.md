---
title: Project Service Automation 更新プログラム リリース 25、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 25、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2d24403b1bf6a06cc138de3f0158f675f6d3b6ec
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581520"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Project Service Automation 更新プログラム リリース 25、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックでは、Project Service Automation V3、更新プログラム リリース 25 で新規または変更された機能と修正の一覧を示します。このバージョンのビルド番号は V 3.10.43.76 で、2020 年 10 月に自己更新で一般提供されます。

## <a name="update-release-25"></a>更新プログラム 25

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

次の問題が修正されました:

- 取得される間隔が大きすぎることに基づいて、追加データを示す時間エントリ グラフ。

**リソース管理**

次の問題が修正されました:

- 上位バージョンのパッチが既に存在する場合に、Universal Resource Scheduling のパッチ インポートをスキップする Package Deployer コードを追加しました。

**プロジェクト管理**

以下の問題が修正されました:

- プロジェクト追跡グリッドで不正確な予定コストにつながる、丸めと為替レートの不一致が修正されました。
- **プロジェクト** フォームに 2 つ以上の対応グリッドを表示する機能をサポートします。
- カレンダーの終了日を過ぎてタスクを割り当てると、リソースの割り当てに失敗することに対処するための検証が提供されました。
- 以下から生成される Null 参照例外に対処するためのエラー処理が改善されました:

    - **PreValidateProjectTeamMemberCreate** プラグイン
    - 関連するプロジェクトなしでプロジェクト タスクが作成された場合の **PreValidateProjectTaskCreate**
    - **PreProjectTeamMemberCreate** プラグイン
    - **PostProjectTeamMemberDelete** プラグイン
    - **PreValidateProjectTaskDelete** プラグイン

**営業**

以下の問題が修正されました:

- **プロジェクトのコピー: HelperResource 管理の見積もり** から生成される Null 参照例外に対処するためのエラー処理が改善されました。
- **時間と材料の請求バックログ** の **請求準備未完了** では、請求の状態がクリアされません。
- **ロール価格** と **カタログ品目** タブの誤ってラベル付けされた **価格** ボタンが修正されました。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
