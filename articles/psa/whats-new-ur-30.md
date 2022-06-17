---
title: Project Service Automation 更新プログラム リリース 30、V3 の新機能と変更点
description: この記事では、Project Service Automation Update リリース 30、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925080"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Project Service Automation 更新プログラム リリース 30、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation Update リリース V3 更新リリース 30 の機能と修正を一覧表示します。 このバージョンのビルド番号は V3.10.51.61 で、通常は 2021 年 4 月の自己更新プログラムを通して使用できます。

## <a name="update-release-30"></a>更新プログラム 30

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:

- **役割** フィールドが削除された場合、**クイック作成** ページに時間エントリを作成して保存すると、エラーが発生します。
- 時間入力フィルターで、正しくないフィルター演算子が適用されます。
- 時間入力制御で **週のコピー** を選択すると、コピーされたタイムシートは自動的に表示されません。

**リソース管理**

以下の問題が修正されました:

- 予約を延長すると、ハード予約に割り当てられた予約ステータスが正しくなくなります。 予約の延長は、予約設定メタデータ内で **確定済み** と定義されている予約ステータスを尊重します。
- 有効な予約ステータスが指定されていない場合、エラー メッセージが正しくローカライズされません。

**プロジェクト管理**

以下の問題が修正されました:

- プロジェクトを 1 つの通貨で作成したり、関連するタスクを別の通貨に含めたりすることはできません。

**営業**

以下の問題が修正されました:

- 価格表がコピーされても、価格は更新されません。
- コストの詳細に発生元の値がある場合、見積もりを成約としてクローズできません。
- **プロジェクト タスク** エンティティで、**見積もりコスト** が **予定コスト (基本)** に改名されました。
- 請求書が作成または削除されると、null 参照例外が生成されます。
