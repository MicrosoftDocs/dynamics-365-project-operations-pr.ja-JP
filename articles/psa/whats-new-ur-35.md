---
title: Project Service Automation 更新プログラム リリース 35、V3 の新機能と変更点
description: このトピックには、Microsoft Dynamics 365 Project Service Automation 更新プログラム リリース 35 V3 で利用可能な機能と修正がリストされています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574034"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Project Service Automation 更新プログラム リリース 35、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation 更新プログラム 35 (V3) の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.56.110 で、一般的に 2021 年 9 月の自己更新プログラムを通じて入手できます。

## <a name="update-release-35"></a>更新プログラム 35

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**時間と経費**

- プロジェクト承認者は、**プロジェクト承認者** 役割で経費エントリを承認すると、読み取り権限エラーを受け取ります。
- プロジェクト承認者は、**プロジェクト承認者** 役割で承認された時間エントリをキャンセルすると、**msdyn_projectapproval** で書き込み権限エラーを受け取ります。
- 電話用 Dynamics 365 - プロジェクト リソース ハブ アプリ モジュールで **週のコピー** を選択した場合、エラー「...\OfficeProductivity_RibbonRules.js.map: HTTP エラー: ステータス コード 404、net::ERR_HTTP_RESPONSE_CODE_FAILURE」が発生します。
- **再試行** ポリシーは、以前に拒否されたエントリを自動的に承認します。
- **承認セット** サブグリッドには、適用できないリボン アクションが表示されます。
- **時間エントリ** エンティティの **プロジェクト タスク** と **リソースの役割** のアイコンはありません。
- リソース割り当てをインポートした場合、インポートされた時間エントリには、手動モードのタスクで作成された割り当ての正しい期間がありません。
- **時間エントリ レコードの高度な検索** ページに **削除** がありません。
- **時間エントリ情報** ページに **保存** がありません。 この問題により、ページを閉じたときに変更が保存されなくなります。

**プロジェクト計画**

- **リソースの割り当て** と **リソースの調整** グリッドでは、グループ化された属性がアルファベット順に並べ替えられません。
- 日付の動作が **日付のみ** にカスタマイズされている場合、タスクを作成できません。

**リソース管理**

- Dynamics 365 Field Service および Project Service Automation の両方がインストールされている場合、**リソース要件関連ビュー** がメイン ページに関連付けられると、オーバーレイの問題が発生します。
- **チーム メンバーのクイック作成** ダイアログ ボックスで **保存** をダブルクリックすると、リソース要件が作成されなくなります。

**営業**

- ステータスが **受注** の見積もりに関連付けられているタスクを削除すると、例外がスローされます。
