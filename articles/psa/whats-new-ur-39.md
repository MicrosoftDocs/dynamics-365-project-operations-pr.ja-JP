---
title: Project Service Automation 更新プログラム リリース 39、V3 の新機能と変更点
description: このトピックには、Microsoft Dynamics 365 Project Service Automation 更新プログラム リリース 39 V3 で利用可能な機能と修正がリストされています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588742"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Project Service Automation 更新プログラム リリース 39、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation 更新プログラム 39 (V3) の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.60.170 であり、一般的には 2022 年 1 月 の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-39"></a>更新プログラム 39

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**全般**

- アラビア語翻訳用のサイト マップが改善しました。

**プロジェクト管理**

- プロジェクトのプロジェクト マネージャーを、すでにプロジェクトのチーム メンバーであるユーザーに変更すると、エラーが発生します。

**営業**

- 価格表を自動的に作成する場合、**プロジェクト契約価格表** の所有者は正しくありません。 
- 価格表がプロジェクト パラメータに適用される場合、価格表の日付の有効性は尊重されません。
- 2 つの別々の見積もりを編集する場合、契約単位の既定値が正しくない可能性があります。
