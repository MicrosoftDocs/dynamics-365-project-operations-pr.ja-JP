---
title: Project Service Automation バージョン 15、V3 更新プログラム の最新情報
description: このトピックでは、Project Service Automation バージョン 15、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752853"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3 、更新プログラム 15 の最新情報

Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、PSA V3 更新プログラム 15 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.5.28 であり、一般的には 2020年1月 の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-15"></a>更新プログラム 15 

### <a name="enhancements"></a>拡張機能

- プロジェクト管理

### <a name="bug-fixes"></a>バグ修正

- 時間と経費

  - 修正：調整ビューにオンロード エラー処理を追加。
  - 修正：プロジェクト リソース ハブ：**数量** を変更してあいまいさを回避します。
  - 修正：**時間入力列のコピー** のビューを調整して種別をを含めます。
  - 修正：小数を使用してグリッドビューで時間入力期間を編集すると、一部の数値で不明なエラーが発生します。

- プロジェクト管理

  - 修正：**トラッキング ビューで使用する** のドロップダウンメニューが、オプションの幅に基づいて展開できるようになりました。
  - 修正：+13 のタイムゾーンでプロジェクトを管理する場合、タスクの計算において不正確な結果が表示される場合があります。
  - 修繕：24時間 カレンダーを使用する場合の **チームメンバーの終了時間** が修正されました。
  - 修正：**msdyn_project** メインフォームの **BPF** を再アクティブ化しています。
  - 修正：割り当ての計算で1日の期間が対象とならない事象が解消されています。
  - 修正：ユーザーとプロジェクトでタイムゾーンが異なる場合に、新しい通知バナーがプロジェクトフォームに追加されました。

- Sales

  - 修正：費用見積カテゴリの参照を使用して重複のフィルター処理ができます。
  - 修正： **PluginDomain.ExecuteInTryCatchBlock(..)** のコードが例外の発生元を非表示にしなくなりました。
  - 修正：1000 以上のプロジェクトがある場合に、 **見積行** フォームの **プロジェクト検索** のエラーメッセージが表示されなくなりました。
  - 修正：労働と経費の **見積り** グリッドに正しい通貨記号が表示されるようになりました。
  - 修正：PSA を 更新プログラム 14 から 更新プログラム 15に更新後、**プロジェクト** フォームの **スケジュール** タブが空白で表示されなくなりました。
