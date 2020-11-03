---
title: Project Service Automation 更新プログラム リリース 14、V3 の新機能と変更点
description: このトピックでは、Project Service Automation バージョン 14、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079226"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation 更新プログラム リリース 14、V3
Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、PSA V3 更新プログラム 14 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.4.21 であり、次のスケジュールで入手できます:

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

