---
title: Project Service Automation 更新プログラム リリース 18、V3 の新機能と変更点
description: この記事では、Project Service Automation 更新プログラム リリース 18、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918870"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation 更新プログラム リリース 18、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation V3 更新プログラム リリース 18 の機能と修正を一覧表示します。 このバージョンのビルド番号は V3.10.8.12 で、通常は 2020 年 4 月の自己更新プログラムを通して使用できます。

## <a name="update-release-18"></a>更新プログラム 18

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

- 修正：**リコール**、 **リクエスト**、 **承認のキャンセル** のフローが不明瞭なエラー メッセージとともに例外をスローする。
- 修正：経費に対する **承認のキャンセル** が失敗した際に、関連する例外エラーがスローされない。
- 修正：オーストラリアでは、10 月のサマータイム切替え後にも時間エントリのグリッドが、休日を適切に処理しない。
- 修正：規定のロジックが不正なために、費用の提出ができない。
- 修正：時間エントリの承認が失敗した際に、承認の状態が **保留中** のままとなる。
- 修正：一括承認にて SQL エラーが発生する（デッドロック／タイムアウト）。
- 修正：時間エントリの承認中にチーム メンバーを更新することで、ユーザー エクスペリエンスにおける重大なパフォーマンスの問題が発生する。

**プロジェクト管理**

- 修正：タイムゾーンの通知は **調整** ビューから **プロジェクト** メイン フォームに移動しています。
- 修正：カレンダーのテンプレートが、新規プロジェクトのフォームを開いた際に規定の設定とならない。
- 修正：クロミウム ベースのブラウザでは、先行するタスクを選択して削除することが困難である。
- 修正：**空白のテンプレートからプロジェクト** を作成、またはコピーすると関連性のない割り当てがされる。
- 修正：特定のエッジ ケースにおいて、タスク グリッドから新規割り当てを作成すると重複するレコードが作成される。
- 修正：マニュアル モードで、タスクの開始日を現在日以降に更新できない。

**リソース管理**

- 修正：予約の延長後、**調整** ビューの小計列に予約の差異が正確に計算されない。
- 修正：予約可能なリソースの日程表とプロジェクトの日程表が合致しない場合、**調整** ビューにリソース管理が正しく表示されない。

**営業**

- 修正：時間エントリが再承認 （**承認 > キャンセル >** 再度承認）された際に、重複する課金できない実績値が作成される。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
