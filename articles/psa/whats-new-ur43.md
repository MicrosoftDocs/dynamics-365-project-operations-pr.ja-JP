---
title: Project Service Automation 更新プログラム リリース 43、V3 の新機能と変更点
description: このトピックには、Microsoft Dynamics 365 Project Service Automation 更新プログラム リリース 43 V3 で利用可能な機能と修正がリストされています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710003"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Project Service Automation 更新プログラム リリース 43、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation 更新プログラム 43 (V3) の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.74.200 で、通常は 2022 年 5 月の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-43"></a>更新プログラム 43

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。


**時間と経費**

- 予約またはリソース割り当てから時間エントリをインポートする場合、関連する予約可能リソースへの参照は維持されません。
- 時間エントリ グリッドが全画面表示に展開されている場合、タブ キーでグリッドをナビゲートすることはできません。
- 別のユーザーが作成した時間エントリを送信する場合、**送信者** フィールドは、タイム シートを作成したユーザーが誤って入力しています。