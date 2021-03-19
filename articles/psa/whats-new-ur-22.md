---
title: Project Service Automation 更新プログラム リリース 22、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 22、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280584"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation 更新プログラム リリース 22、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 22 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V 3.10.33.48 であり、2020 年 6 月のセルフ アップデートを通じて一般提供されました。

## <a name="update-release-22"></a>更新プログラム 22

### <a name="bug-fixes"></a>バグの修正



**時間と経費**

以下の問題が修正されました:

- **時間エントリ** は、インポート後、時間エントリ スケジュールに自動的に追加されません。
- **時間エントリ** グリッドの日付ピッカーは、ユーザーの地域設定を認識しません。

**リソース管理**

以下の問題が修正されました:

- 手動モードでは、**リソース要件** の生成時に **リソース割り当て** 輪郭は認識されません。
- **リソース要求** はカスタム リクエスト ステータスをサポートしていません。

**プロジェクト管理**

以下の問題が修正されました:

- EstimateGridControl をダブルクリックすると、オランダ語形式の数値は正しく解析されません。
- Microsoft Project デスクトップ クライアント アドインを使用して割り当てを変更すると、割り当てられた時間は正しく更新されません。
- 契約通貨が顧客の通貨と異なり、組織が通貨記号の代わりに通貨コードを表示するように構成されている場合、プロジェクトの追跡と見積もりグリッドに誤った販売通貨コードが表示されます。
- 勤務時間のスケジュールが 1 日 24 時間の場合、チーム メンバーの終了日は 1 日追加されます。
- プロジェクト スケジュールで、トランザクション カテゴリをタスクに追加しても、自動保存はトリガーされません。
- チーム メンバーをプロジェクト テンプレート: "リソース要件をプロジェクト テンプレートに関連付けることはできません" に追加すると、次のエラーが表示されます。 
- リボン ルール スクリプト "msdyn.Approval.CanApproveOrReject"がタイムアウトエラーを表示します。

**営業**

以下の問題が修正されました:

- '新規見積もりプロジェクト価格表' フォーム/エンティティの価格表検索ダイアログで原価価格表が選択されていると、検証エラーメッセージが表示されません。
- 見積もりに添付された BPF が最終段階にある場合、見積もりを受注としてクローズしても作成された契約に移動しません。
- **未請求売上** の戻し処理は、時間エントリが取り消されると、元のコストにリンクされます。
- **確認** ボタンを選択した後、請求書の状態は請求書が更新されない限り、**確認済み** に変わりません。


[!INCLUDE[footer-include](../includes/footer-banner.md)]