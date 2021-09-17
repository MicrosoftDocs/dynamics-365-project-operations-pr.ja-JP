---
title: Project Service Automation 更新プログラム リリース 34、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 34、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323287"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Project Service Automation 更新プログラム リリース 34、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 34 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.55.38 で、一般的に 2021 年 7 月の自己更新プログラムを通じて入手できます。

## <a name="update-release-34"></a>更新プログラム 34

### <a name="bug-fixes"></a>バグの修正
以下の問題が修正されました。

**全般**

- 発行元主導の更新は、新しい最新の承認ワークフローをアクティブ化しません。
- **ターゲットの状態** と **アクションの種類** 属性が **承認セット** のメイン ページにありません。

**時間と経費**

- 最新の承認フローを使用したリコール要求を承認できません。
- ログインしたユーザーに関係のないエントリをコピーする場合、1 週間の時間エントリをコピーすることはできません。

**プロジェクト計画**

- Microsoft Project デスクトップ アドインからインポートすると、リソース割り当て配分型が破損します。

**リソース管理**

- Microsoft Project デスクトップ クライアント アドインからプロジェクトを公開すると、既存の要件の終了日が変更されます。
- 予約確認ダイアログの延長で小数点以下の桁数が小数点以下 2 桁を超えています。

**営業**

- 既存の製品を含む製品ベースのラインをプロジェクト契約に追加すると、例外の **ディクショナリにキーが見つかりません** が表示されます。
- 注文タイプがリードから営業案件にマップされている場合、リードを評価することはできません。
