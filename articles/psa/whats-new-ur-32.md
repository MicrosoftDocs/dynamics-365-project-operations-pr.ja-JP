---
title: Project Service Automation 更新プログラム リリース 32、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 32、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 3ad87eceb90a48997aadf00803b8d14c5108eb83
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580094"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Project Service Automation 更新プログラム リリース 32、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 32 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.53.108 であり、2021 年 6 月の自己更新を通じて一般提供されています。

## <a name="update-release-32"></a>更新プログラム 32

### <a name="bug-fixes"></a>バグの修正

#### <a name="general"></a>全般

- メジャー アップグレードが失敗した場合は、メイン アプリケーションのエントリ ポイントのみをブロックして、共有エンティティに引き続きアクセスできるようにする必要があります。

#### <a name="time-and-expense"></a>時間と経費

以下の問題が修正されました:

- **TimeEntriesImportFromResourceAssignment** は、リソース要件の配分型スライスの開始時刻と終了時刻を維持しません。
- **オープンしているエントリ** を **時間エントリ** グリッドで選択すると、他のフォームを選択できない場合があります。
- 時間エントリへの割り当てをインポートしている間に、クライアント コード クエリが長い URL を生成して、クエリに失敗するする場合があります。
- **時間エントリ** グリッドでは、セルから値が削除された後、フォーカスはグリッドに残りません。
- **却下** ボタンは、最新の承認の **処理中の承認** ビューから削除されました。
- 時間エントリの一括承認の安定性とパフォーマンスは、デッドロックと **時間エントリ** エンティティに関連するカスタマイズを適切に処理できないことによって影響を受けます。

#### <a name="project-planning"></a>プロジェクトの計画

- **契約単位** フィールドに null 値があるプロジェクトを更新すると、null 参照例外が生成されます。
- **プロジェクト合計の更新** では、プロジェクトの残コストと残売上が正しく計算されません。
- 冗長な価格計算は、リソース要件の配分型の更新に関連するパフォーマンスに影響します。

#### <a name="resource-management"></a>リソース管理

次の問題が修正されました:

- 予約可能なリソースのカレンダー キャパシティが 1 を超えると、Project Service Automation はキャパシティを 0 (ゼロ) と誤って認識します。 そのため、スケジュール ビューで無限ループが発生します。

#### <a name="sales"></a>営業

以下の問題が修正されました:

- カスタム トランザクションの種類を持つ仕訳帳明細行が作成されると、次の null 参照例外が発生します: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*。
- 見積がコピーされる前に非アクティブ化されたロールとカテゴリは、新しくコピーされた見積書の請求可能ロールとカテゴリに追加しないでください。
- ドキュメントの日付と会計日は、下書き請求書で直接作成された請求書明細行の詳細に記載されている開始日と一致していません。
- null 参照例外は、見積がコピーされる前に、ロールとカテゴリの非アクティブ化に関連するシナリオで生成されます。
- **プロジェクト** ページの **価格の更新** アクションでは、経費見積もりと材料見積もりは更新されません。
