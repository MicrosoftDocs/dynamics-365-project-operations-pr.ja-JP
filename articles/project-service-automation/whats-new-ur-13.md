---
title: Project Service Automation バージョン 13、V3 更新プログラム の最新情報
description: このトピックでは、Project Service Automation バージョン 13、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752855"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3 、更新プログラム 13 の最新情報
Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 13 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.3.18 であり、次のスケジュールで入手できます:

- **一般的な入手（自己プログラム アップデート）：** 2019年11月
- **自動更新:** 2019年12月


## <a name="update-release-13"></a>更新プログラム 13 

### <a name="bug-fixes"></a>バグ修正

- 時間と経費

     - 修正：**経費の承認**ページの検索機能が経費の検索として機能しない。

- リソース管理

     - 修正：調整の数値が右揃えに更新されています。
     - 修正：名前付きのリソースを、 **スケジュール** タブを介して割り当てできない。

- プロジェクト管理

     - **TransactionType** が **単位** と **DefaultGroup** に対して未入力の場合に、チーム メンバーを割り当てするとNULL参照例外が発生する。

- Sales

     - 修正：重複する取引タイプのレコードが、ロール価格レコードの作成時にエラーを返します。
     - 修正：追加のボタン **新規営業案件**、 **見積もり**、 **注文明細**、 **製品の追加** に新たなボタンが追加され、営業案件、見積もり、製品受注、プロジェクト ベースのラインのサブグリッド で表示されます。


