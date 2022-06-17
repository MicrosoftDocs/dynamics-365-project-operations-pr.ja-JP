---
title: Project Service Automation 更新プログラム リリース 28、V3 の新機能と変更点
description: この記事では、Project Service Automation 更新プログラム リリース 28、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930600"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Project Service Automation 更新プログラム リリース 28、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation V3、更新プログラム リリース 28 の新しいまたは変更された機能と修正を一覧表示します。このバージョンのビルド番号は V3.10.46.32 で、一般的に 2021 年 1 月の自己更新で入手できます。

## <a name="update-release-28"></a>更新プログラム 28

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:

- ユーザーは **一括編集** を使って、承認および送信済みの時間エントリを更新できます。

**プロジェクト管理**

以下の問題が修正されました:

- タスク GUID が数値として解釈される場合、**WBS (作業分解構造)** ページのリボンに表示された **タスクの編集** を使用して編集するためにタスクを開くことはできません。

**営業**

以下の問題が修正されました:

- **GetEstimatesForProject** プラグインが呼び出されると、null 参照例外が生成されます。
- マイルストーン グリッドの **請求準備完了としてマーク** は、**InvoiceStatus** 属性 (更新済み) 以外の属性を部分的にのみ更新します。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
