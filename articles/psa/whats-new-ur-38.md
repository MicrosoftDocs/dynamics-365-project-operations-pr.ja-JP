---
title: Project Service Automation 更新プログラム リリース 38、V3 の新機能と変更点
description: この記事では、Microsoft Dynamics 365 Project Service Automation 更新リリース 38、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915191"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Project Service Automation 更新プログラム リリース 38、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation Update リリース 38、V3 の新機能または変更点を示します。 このバージョンのビルド番号は V3.10.59.117 で、2021 年 12 月のセルフアップデートで一般提供されます。

## <a name="update-release-38"></a>更新プログラム 38

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**時間と経費**

- 承認セットログの長さが100,000 レコードを超えると、例外が発生します。
- ユーザーは、**タイムエントリ** メインページの **タイムエントリ** グリッドにはアクセスできません。
- インポートできるアイテムがない場合、ダ **タイム エントリのインポート** ダイアログボックスにテキストは表示されません。
- **ターゲット ステータス** フィールドが **不明** に設定されている場合、ユーザーは承認セットを作成できます。

**プロジェクト管理**

- サマータイム開始時の UTC (+09:30) および UTC (+10:00) のリソース割り当てで、輪郭が正しく表示されません。
- 一部のロケールでは、WBS の **追加の列** フィールドが非表示になります。
- **プロジェクト  タスク** グリッドのカレンダー コントロールの日付ピッカーが、中国語に正しくローカライズされていません。

**営業**

- 契約単位や通貨が異なる予約可能なリソースがタイムエントリを送信すると、**契約実績** と **プロジェクトの実際のコスト** の値が一致しません。
- 請求書がマネージド ソリューションとしてインポートされると、請求書を自動的に確認するカスタム ワークフローが失敗する。 次のメッセージが表示されます: 「Microsoft.Xrm.Sdk.InvalidPluginExecutionException メッセージ: 無効な請求書のステータス」
- 要約オプションとして **ルート** を選択した場合、プロジェクトに複数の取引クラスの見積もりが混在していると (例えば、時間、費用、材料の見積もりの組み合わせなど)、システムは複数の取引クラスを単一の料金ラインとして要約します。
- 契約行がプロジェクトに関連付けられる前に経費明細行が追加された場合、正しい価格が **更新価格** フィールドの既定値として入力されません。
- **プロジェクト** と **タスク** のエンティティでは、売上金額のマイナスは許されません。
