---
title: Project Service Automation 更新プログラム リリース 33、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 33、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334560"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Project Service Automation 更新プログラム リリース 33、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 33 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.54.98 で、一般的に 2021 年 7 月の自己更新プログラムを通じて入手できます。

## <a name="update-release-33"></a>更新プログラム 33

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:

- 2 つのロックされたフィールド、**msdyn_description** と **msdyn_externaldescription** は、送信後に編集可能です。
- プロジェクトに関連しない経費を作成すると、エラーメッセージが表示される。
- 時間入力が作成されると、リソースロールが既定で非アクティブなロールとなる。
- 回収・削除された支出に関連する仕訳明細が削除されない。
- **時間入力のクイック作成フォーム** で、**プロジェクト タスク リスト** のビューを更新して、既定で表示される日付をタスクの開始日に変更される。
- 予約可能なリソースの **関連** タブから時間入力を作成すると、親のブッキング可能なリソースではなく、サインインしているユーザーの時間入力が誤って作成されてしまうという問題が発生していました。
- **一括承認 MDD** ダイアログ ボックスに新しいフィールドが追加されました。

**プロジェクト計画**

以下の問題が修正されました:
- プロジェクトの作業時間テンプレートを複雑なカレンダーに適用すると、プロジェクトの作成パフォーマンスが低下してしまう問題がありました。
- 開始日が終了日よりも大きい場合、各フィールドの時間コンポーネントが異なるため、コピー プロジェクトのテンプレートにエラーが表示される。

**リソース管理**

以下の問題が修正されました:
- リソース利用クエリで不正なパラメータが使用されており、その XML が原因で **リソース利用グリッド** のフィルター結果が不正になる問題が発生する。
- **予約の延長** 確認で、予約の終了日が正しく表示されない。

**営業**

以下の問題が修正されました:
- 値がない状態でカテゴリーの価格を作成するとエラーが発生する。
- 契約品目のマイルストーンを受注明細なしで作成した場合に、エラーが発生する。
