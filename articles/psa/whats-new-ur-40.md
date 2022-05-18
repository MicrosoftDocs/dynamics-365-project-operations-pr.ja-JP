---
title: Project Service Automation 更新プログラム リリース 40、V3 の新機能と変更点
description: このトピックには、Microsoft Dynamics 365 Project Service Automation 更新プログラム リリース 40 V3 で利用可能な機能と修正がリストされています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588650"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Project Service Automation 更新プログラム リリース 40、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation 更新プログラム 40 (V3) の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.61.61 で、一般的には 2022 年 2 月の自己プログラム更新処理を通じて一般入手できます。

## <a name="update-release-40"></a>更新プログラム 40

### <a name="features"></a>機能
Project Service Automation から Project Operations へのアップグレードのフェーズ 1 - ライトは、2022 年 2 月にすべての顧客にリリースされます。 適格性に関しては、[Project Service Automation から Project Operations にアップグレードする](upgrade-project-operations-non-stocked.md) を参照してください。 アプリケーションがインスタンスに表示されない場合、Power Platform 管理センターでサポートに連絡し、ご使用の環境でフライトを有効にするよう要求してください。 要求には、フライトを有効にする必要がある環境 ID の一覧を含める必要があります。

### <a name="bug-fixes"></a>バグの修正

以下の問題が修正されました。

**時間と経費**
- メモ エントリがない場合、時間エントリが拒否またはキャンセルされます。 

**営業**

- すぐに使用できるプラグインを使用して、コスト見積もりまたは売上見積もりを更新すると、ユーザー インターフェイスの外部で無効な JSON ペイロードの送信を誤って許可します。
- 簡易表示を使用して見積もり行を更新すると、見積もりをアクティブ化することができます。
