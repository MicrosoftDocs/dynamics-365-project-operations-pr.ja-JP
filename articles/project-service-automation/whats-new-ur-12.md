---
title: Project Service Automation バージョン 12、V3 更新プログラム の最新情報
description: このトピックでは、Project Service Automation バージョン 12、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752856"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3 、更新プログラム 12 の最新情報
Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 12 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.2.34 であり、一般的には 2019年10月 の自己更新処理を通じて入手できます。

## <a name="update-release-12"></a>更新プログラム 12

### <a name="bug-fixes"></a>バグ修正

- 時間と経費

    - 修正：時間の入力でのエラーメッセージが更新され、より関連性の高いコンテキストが追加されました。
    - 修正：時間入力のグリッドとスケジュールが、必要に応じて垂直方向のスクロールバーを正しく表示します。
    - 修正：送信済みの経費と時間入力を承認することができます。
    - 修正：承認キャンセル時の確認ダイアログ メッセージが修正され、 **承認済み** から **提出済み** へと変更された際の承認ステータスが反映されるようになりました。
    - 修正： **価格**、 **単位**、 **数量** フィールドが、承認後に経費レコード上でロックされるようになりました。

- プロジェクト管理

    - 修正：メイン フォームの **チームメンバー** 上の **新規** アクション が削除されました。
    - 修正：タスクの終了日がずれる原因となる端数処理のエラーが不正確なため、リソースの割り当てが変更されました。
    - 修正：タスク グリッドで、関連するサーバー側のエラーがユーザーに表示されます。
    - 修正：役職名の代わりにチームメンバーの名前がタスクのユーザー ピッカーで表示されるようになりました。

- リソース管理

    - 修正：テンプレートから作成されたプロジェクトのリソース要件の詳細で、プロジェクトカレンダーが使用されるようになりました。
    - 修正：スキルとコンピテンシーが、ロール マスターデータから、そのロールに対して作成されたリソースの要件に既定で設定されます。

- Sales

    - 修正：**契約のメイン** フォームで重複するオブジェクトIDが見つかりました。
    - 修正： **見積もり分析** タブが表示されるようにロジックが更新され、タブのメタデータ設定が表示されるようになりました。
    - 修正：実績レコードの計上日は、承認された日ではなく、時間/経費の入力日となります。