---
title: Project Service Automation 更新プログラム リリース 31、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 31、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586764"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Project Service Automation 更新プログラム リリース 31、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 31 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.52.77 であり、2021 年 5 月のセルフ アップデートを通じて一般提供されました。

## <a name="update-release-31"></a>更新プログラム 31

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:

- **予約可能なリソース** ページのの時間入力制御コマンドボタンがわかりにくい。
- 時間入力を承認する際に、**Project.SetTrackingFields** で null 値参照の例外が発生する。

**リソース管理**

以下の問題が修正されました:

- **チーム メンバーを作成する** 予約設定メタデータの **既定の予約コミット状態** が正しく表示されませんでした。
- PSA 1.X から 3.X にアップグレードする際に、**UpgradeResourceRequirements** でアップグレード処理が失敗する問題が発生しました。


**営業**

以下の問題が修正されました:

- 実際の収益が、追跡グリッドで金額をプロジェクトの通貨に変換される。
- 組織の基本通貨とプロジェクトの通貨が異なる場合に、仕訳明細、見積明細、契約明細を作成すると、既定の通貨のが不明瞭になる。
- **修正ジャーナルの検証を保留中** クエリがプロジェクトでフィルター処理されない。
- プロジェクトで残りの売上が正しく計算されない。
- 価格表を作成せずに、連絡先担当者を元に見積書を作成すると失敗する。
- **請求書の確認** を選択しても、処理スピナーが表示されない。
- **請求書の作成** を選択しても、処理スピナーが表示されない。
- 見積書を失注としてクローズしても、予約をキャンセルできない。







