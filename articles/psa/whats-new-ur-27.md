---
title: Project Service Automation 更新プログラム リリース 27、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 27、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146669"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Project Service Automation 更新プログラム リリース 27、V3 の新機能と変更点

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、Project Service Automation V3 更新プログラム 27 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.45.98 であり、一般的には 2021 年1月 の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-27"></a>更新プログラム 27

### <a name="bug-fixes"></a>バグの修正

**一般**

以下の問題が修正されました:

- Project Service Automation のプラグインによって生成されたログが、自動削除に設定されていません。
- Project Service Automation ソリューションにレガシー null NavBarArea とタイトル要素が含まれているため、自動アップグレードが失敗します。

**時間と経費**

以下の問題が修正されました:

- **時間エントリ** グリッドで、**タイム ゾーン非依存** 日付動作に対して誤ったデータが表示されます。
- **時間エントリ** グリッドで、**タイム ゾーン非依存** 日付動作に対して誤った時間が作成されます。
- タスク検索が、**時間エントリの編集** ページで選択したプロジェクトに限定されません。
- 非プロジェクト時間エントリの承認が、プロジェクト承認者の検索時にブロックされます。
- 実績に正しい値を入力しても、誤ったエラー メッセージが表示されます。
- タスクに実際のコストの null 値が含まれていて、プロジェクトの合計が更新されると、「指定されたキーが辞書に存在しません」というエラーが発生します。
- 具体的な例としては、**プロジェクトの見積もり** タブの **グループ別** フィルターに経費の見積もりが表示されません。
- 時間エントリで、**夏時間** の間隔が正しくありません。

**プロジェクト管理**

以下の問題が修正されました:

- キャッシングが改善され、**プロジェクト** ページのロードに関連するパフォーマンスが向上しました。
- 廃止されたビジネス ルールにより、プロジェクト タスクが完了できなくなっています。
- Microsoft Project アドインのコントーがアドインのカレンダーに沿っていないため、リソース要件が正しくなくなっています。
- テンプレートからプロジェクトを作成すると、割り当て日が誤って設定され、リソース要件を生成できなくなります。
- ユーザーがキーボードを使って **カテゴリ**、**説明**、**ステータス** オプションにアクセスできません。
- プロジェクトの実際の販売額に、料金や資材の販売額が含まれていません。
- 異なる為替レートを使うと、実際の売上と実際のコストの集計が正しくなくなります。
- **既定の作業時間テンプレート** の説明が誤解を招く内容です。
- ユーザー インターフェイスを更新するまで、タスクをインデントしても **カテゴリー** が削除されません。
- プロジェクトが終了日を超えて移動することを禁止するための検証が欠落しています。

**営業**

以下の問題が修正されました:

- プロジェクトが選択されていない場合に、**プロジェクトの見積もりからインポート** が表示されるため、null 参照例外がプロジェクトの見積もり行で生成されます。
- 見積もりを **受注** としてクローズすると、「オブジェクト参照がオブジェクトのインスタンスに設定されていません」というエラーが発生します。
- プロジェクトと契約品目のリンクを解除する際、実際の取消時に調整ステータスが設定されません。
- Dynamics 365 Field Service と Project Service Automationの 両方がインストールされている場合、**請求書** ページに **価格のロック** と **現在の値付けを​​使用** オプションが同時に表示されません。
- 日本語の場合、他のカレンダー ベースのページとの翻訳に一貫性がありません。
- **アクティブ化** と **非アクティブ化** が、Project Service Automation の **価格表の関連付け** エンティティから削除されました。


[!INCLUDE[footer-include](../includes/footer-banner.md)]