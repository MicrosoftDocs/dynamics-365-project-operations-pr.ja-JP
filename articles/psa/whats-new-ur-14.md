---
title: Project Service Automation 更新プログラム リリース 14、V3 の新機能と変更点
description: この記事では、Project Service Automation 更新プログラム リリース 14 V3 で新しい点について説明します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926552"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation 更新プログラム リリース 14、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation PSA V3 更新プログラム リリース 14 の機能と修正を一覧表示します。 このバージョンのビルド番号は V3.10.4.21 であり、次のスケジュールで入手できます:

- **一般的な入手（自己プログラム アップデート）：** 2020年1月
- **自動更新：** 2020年2月

## <a name="update-release-14"></a>更新プログラム 14

### <a name="enhancements"></a>拡張機能

- Sales

     - 見積が **商談成立としてクローズ** として更新された際に、 **見積明細の詳細** のカスタムフィールド値が、 **プロジェクト契約ラインの詳細** にコピーされます。
     - 確認済みのプロジェクトは **失注としてクローズ** となります。

- リソース管理

     - 予約を延長すると、予約結果を要約し、予約の管理 へのリンクを案内する確認のダイアログ ボックスが表示されます。


### <a name="bug-fixes"></a>バグ修正

- 時間と経費

     - 修正：修正する入力内容をユーザーが選択していない場合のユーザー エクスペリエンスが改善されました。

- リソース管理

     - 修正：リソースを複数回予約すると、予約可能なリソースの名前が桁あふれする。

- Sales

     - 修正済み：ユーザーがプロジェクトの費用の見積もり原価価格を入力するまで総販売価格が計算されない。
     - 修正：見積もりに関連付けられているプロジェクトの契約が **下書き** 状態の場合、この見積を **成約** としてクローズことができない。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
