---
title: Project Service Automation 更新プログラム リリース 26、V3 の新機能と変更点
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643269"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation 更新プログラム リリース 26、V3
================================================

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation 更新プログラム 26 (V3) の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.44.59 で、2020 年 12 月のセルフアップデートで一般提供されます。

<a name="update-release-26"></a>更新プログラム 26
-----------------

### <a name="bug-fixes"></a>バグの修正

**時間と経費**

以下の問題が修正されました:

-   ユーザーは承認/送信済みのタイム入力でタスクを変更できます。

-   時間入力を保存する際の "オブジェクト参照が設定されていません" エラー。

-   リソース割り当てから時間入力をインポートすると、不正な DateTime 値で時間入力が作成されます。

-   Project Service Automation と Field Service アプリの両方がインストール済みの場合、Field Service アプリの時間入力のコマンド バーに **新規** ボタンを 2 回表示します。

-   **許可単位** と **出荷単位一覧** セルの更新が、現在は **経費の見積もり** グリッドで機能します。

-   **タイムライン** を含む **時間入力編集の更新** フォーム。

-   非プロジェクト時間入力の時間承認は、プロジェクト承認者ロールの検索時にシステムをブロックします。

**リソース管理**

以下の問題が修正されました:

-   **PostProjectCreate** プラグインに検証を追加して、主要な要件を作成する前に確認します。

-   フィールドをフォームから削除すると、**プロジェクト チーム メンバー** の簡易作成フォームが null 参照例外をスローします。

-   1 年間で 12 時間の要件生成は失敗します。

-   リソース要件作成での null 参照例外エラー メッセージを改善しました。

**プロジェクト管理**

以下の問題が修正されました:

-   **PreProjectUpdate** プラグインが生成する null 参照例外に対処する検証を改善しました。

-   Microsoft Project デスクトップ アドインで公開したプロジェクトは、未割り当ての割り当てを削除します。

-   **PreValidateProjectTaskUpdate** プラグインの null 参照例外が原因でタスクのプロジェクト参照が無効になる際の、新しい検証を追加しました。

-   チーム メンバー グリッドにチーム メンバー レコードの個別割り当てを表示しません。

-   **PreProjectTaskDelete** プラグインの null 参照例外に起因する、新しい検証とエラー メッセージを追加しました。

**営業**

以下の問題が修正されました:

-   見積もりや契約でプロジェクト ベースの品目を選択する場合、**提案** ボタンを既存の製品に関連付けられた製品ベースの品目を選択した時だけ表示します。

-   **Create_Product** 特権を **Create_ProjectContract** 特権から分割します。

-   請求明細行を削除すると **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** で null 参照エラーが発生します。
