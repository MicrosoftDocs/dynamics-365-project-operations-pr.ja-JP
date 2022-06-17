---
title: Project Service Automation 更新プログラム リリース 41、V3 の新機能と変更点
description: この記事では、Microsoft Dynamics 365 Project Service Automation 更新リリース 41、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930554"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Project Service Automation 更新プログラム リリース 41、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation Update リリース 41、V3 の新機能または変更点を示します。 このバージョンのビルド番号は V3.10.62.162 で、一般的には 2022 年 3 月 の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-41"></a>更新プログラム 41

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**プロジェクト管理**
- デスクトップ アドインで作成されたプロジェクトに基づくテンプレートでプロジェクトを作成しようとすると、次のエラーが表示されます。「リソース割り当ての計画済み作業フィールドの検証: 各リソース割り当てタイム スライスの終了日は、開始日より前にはできません」

**時間と経費**
- 時間エントリを削除しようとすると、「ISV コードから予期しないエラーが発生しました」というエラー メッセージが表示されます。

**営業**
- 固定価格マイルストーンの請求書を作成すると、**説明** と **外部の説明** フィールドは入力されません。 
