---
title: Project Service Automation 更新プログラム リリース 47、V3 の新機能と変更点
description: この記事では、Microsoft Dynamics 365 Project Service Automation 更新プログラム リリース 47、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477236"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Project Service Automation 更新プログラム リリース 47、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation Update リリース 45、V3 の新機能または変更点を示します。 このバージョンのビルド番号は V3.10.78.8 で、一般的に 2022 年 7 月の自己更新プログラムを通じて入手できます。

## <a name="update-release-47"></a>更新プログラム 47

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**リソース管理**
- **予約可能なリソース** がないプロジェクト チーム メンバーを作成しようとしたときに、null 参照例外が発生しないようにするために、検証が更新されました。
