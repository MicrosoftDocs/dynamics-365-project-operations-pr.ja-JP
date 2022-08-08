---
title: Project Service Automation 更新プログラム リリース 45、V3 の新機能と変更点
description: この記事では、Microsoft Dynamics 365 Project Service Automation 更新リリース 45、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169159"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Project Service Automation 更新プログラム リリース 45、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation Update リリース 45、V3 の新機能または変更点を示します。 このバージョンのビルド番号は V3.10.76.168 で、一般的に 2022 年 7 月の自己更新プログラムを通じて入手できます。

## <a name="update-release-45"></a>更新プログラム 45

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**営業**

- ユーザーがページの同じインスタンスを表示していて更新しない場合、未請求の売上実績なしで請求書を作成しようとした後、ユーザーは請求書を正常に作成できません。

**時間と経費**

- 最新の承認が有効になっていて、リコールされたプロジェクト承認が承認されると、レコード ステージが誤って **取り消し要求承認済み** と更新されます。
- 最新の承認が有効で、クラウド フローが非アクティブの場合、承認プロセスは成功せず、送信または承認するユーザーには通知されません。
