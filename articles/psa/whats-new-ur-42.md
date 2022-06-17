---
title: Project Service Automation 更新プログラム リリース 42、V3 の新機能と変更点
description: この記事では、Microsoft Dynamics 365 Project Service Automation 更新リリース 42、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912721"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Project Service Automation 更新プログラム リリース 42、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation Update リリース 42、V3 の新機能または変更点を示します。 このバージョンのビルド番号は V3.10.73.61 で、通常は 2022 年 4 月の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-42"></a>更新プログラム 42

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**時間と経費**

- タイム シートが拒否された場合、それを拒否したユーザーは誤って **システム** と識別されます。
- 時間エントリがインポートされた場合、**リソース カテゴリ** 値がありません。
- アクセス許可が特に **承認可** に設定されていない場合、プロジェクト承認者はプロジェクトを承認できます。

**営業**

- 実績がルート レベル以外のタスクに記録されると、実際のコストが誤って集計されます。
