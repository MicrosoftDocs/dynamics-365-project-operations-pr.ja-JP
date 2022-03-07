---
title: Project Service Automation 更新プログラム リリース 37、V3 の新機能と変更点
description: このトピックには、Microsoft Dynamics 365 Project Service Automation 更新プログラム リリース 37 V3 で利用可能な機能と修正がリストされています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727611"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Project Service Automation 更新プログラム リリース 37、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation 更新プログラム 37 (V3) の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.58.120 であり、一般的には 2021 年 11 月 の自己更新処理を通じて入手できます。

## <a name="update-release-37"></a>更新プログラム 37

### <a name="bug-fixes"></a>バグ修正

以下の問題が修正されました。

**時間と経費**
- ユーザーは、セルをクリアして時間エントリを削除することはできません。
- **失敗した承認** ビューには、状態が **提出済み** となっているプロジェクト承認のみが含まれます。

**プロジェクト管理**
- Microsoft デスクトップ アドインでプロジェクトを開くときに、プロジェクトのチームメンバーの役職名が空の場合、ユーザーに NULL 参照例外エラーが発生するという問題がありました。
- **プロジェクト タスク** ページには **保存** ボタンがないため、ユーザーはタスク記録の変更を保存できません。
- ユーザーは、状態が **成約** となっている見積書に関連するタスクが存在するプロジェクトを削除できません。

**営業**
- **プロジェクト** ページの **通貨** フィールドが、適用したテンプレートの通貨に合わせて更新されます。
- 複数の通貨を持つタスクでは、コストが正しく計算されません。