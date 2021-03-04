---
title: Project Service Automation 更新プログラム リリース 20、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 20、V3 で利用可能な機能と修正をリスト化しています
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147119"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation 更新プログラム リリース 20、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 20 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V 3.10.31.37 であり、2020 年 6 月のセルフ アップデートを通じて一般提供されました。

## <a name="update-release-20"></a>更新プログラム 20

### <a name="bug-fixes"></a>バグの修正

**プロジェクト管理**

以下の問題が修正されました:

- 時間を必要とする割り当て方法でプロジェクト チーム メンバーをインポートすると、指定した時間がゼロの場合に不明確なエラー メッセージが表示されます。
- プロジェクトタスクの **説明** フィールドに最大文字数を入力すると、ユーザーは誤ったエラーを受け取ります。
- ユーザーの言語設定が日本語に設定されている場合、**Microsoft Dynamics 365 Project Service Automation アドインのダウンロード** ページは英語のダウンロード ページにリダイレクトされます。
- サーバー エラーが発生すると、**プロジェクト** フォームの **スケジュール** タブに同期ラベルが残ることがあります。
- タスクが変更されると、冗長なタスク更新がサーバーに送信されます。

**営業**

以下の問題が修正されました:

- **契約** フォームで、**請求書の作成** をダブルクリックすると、1 つの実績レコードに対して 2 つの請求書が作成されます。
- Internet Explorer 11 では、ユーザーは経費エントリを作成できません。
- 原価の取消と未請求売上実績の取消はリンクされていません。
- **プロジェクト** フォームの **実績の更新** ボタンは、**タスクの実時間数** を更新しません。
- **PreValidateProjectTeamMemberCreate** プラグインは、属性 **msdyn_isgenericresourceprojectscoped** が　**False** に設定されている場合、重複する予約可能な汎用リソースを作成できます。
- **再計算** は、製品ベースの見積依頼明細行の詳細と契約品目の詳細の請求可能コストをクリアします。
- 特定のシナリオでは、**PostEstimateLineUpdate** プラグインが Null 参照の例外エラーを表示します。
- **収益性分析チャート** の時間フェーズ期間は、見積の固定価格見積依頼明細行の詳細のコストの期間と一致しません。
- 出荷単位および出荷単位一覧の値は、**契約品目の詳細** と **見積依頼明細行の詳細** フォームの経費カテゴリで正しく既定値設定されません。
- **組織単位原価価格** 一覧には、日付の有効性の重複が許可されています。
- 受注タイプが作業ベースではない場合、null 参照例外エラーが発生するため、ユーザーは **OrgUnit** を変更できません。
- **見積依頼明細行の詳細** フォームから **見積もり** タブに戻って移動しようとすると、フォームが更新され、**概要** タブが表示されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]