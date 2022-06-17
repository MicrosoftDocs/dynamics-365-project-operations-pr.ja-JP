---
title: Project Service Automation 更新プログラム リリース 24、V3 の新機能と変更点
description: この記事では、Project Service Automation 更新プログラム リリース 24、V3 で利用可能な機能と修正を一覧表示します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
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
ms.openlocfilehash: d2cd8c18a2ea10ae090d8258d835453b279d717f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926414"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation 更新プログラム リリース 24、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。 このリリースは、Dynamics 365 9.x と互換性があります。 このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

この記事では、Project Service Automation V3 更新プログラム リリース 24 の機能と修正を一覧表示します。 このバージョンのビルド番号は V 3.10.42.43 であり、一般的には 2020 年 10 月の自己プログラム更新の処理を通じて入手できます。

## <a name="update-release-24"></a>更新プログラム 24

### <a name="bug-fixes"></a>バグの修正

**営業**

以下の問題が修正されました:

- 製品の既定の価格表を設定する際の問題。
- 価格表とロール価格レコードのコピーが埋め込まれているため、見積もり獲得のパフォーマンスは遅くなります。
- **プロジェクト契約/営業ハブ** > **製品品目/注文明細行の数量** は、最も近い整数に自動的に丸められます。
- 価格表の読込み時にシステム特権に引き上げます。
- 顧客の住所フィールド **address1_freighttermscode** と **address1_shippingmethodcode** を見積もり/受注にコピーします。 


**時間と経費**

以下の問題が修正されました:

- **時間エントリ グリッド** は、**日付のみ** の時間動作をサポートしていません。
- **時間エントリ** は自動的に更新されません。 手動で更新する必要があります。
- リソースの割り当てにブレーク (0 時間) がある場合、割り当てから時間エントリをインポートできません。
- 時間エントリを作成するときは、開始を **msdyn_date** と同じに設定します。
- 時間エントリの一括編集を再度有効にします。

**リソース管理**

以下の問題が修正されました:

- 要件なしで日中の予約のステータスを更新しようとすると、null-ref 例外がスローされます。
- **調整ビュー** の読み込み中にエラーが発生しました。


**プロジェクト管理**

以下の問題が修正されました:

- **プロジェクト スケジュール** で、**手動** から **自動** に変更すると、自動保存が完了しません。
- 経費コストは、**プロジェクト追跡グリッド** の差異に対して計算すべきではありません。
- 読み込み中と **時間フェーズ** タイプの変更中の **見積もりタグ** 列の動作に一貫性がありません。
- プロジェクトの実際のコストは、**実績** からの合計を反映していない可能性があります。
- **概要** タブの **終了予定日** が **WBS スケジュール** に一致しません。
- インデント解除時の **実績時間の更新** が正しく機能しません。
- ルート **BU** 外のプロジェクト マネージャーがプロジェクトを作成できません。
- **経費の見積もり** のタスクまたはカテゴリへの変更は、保持されません。
- **契約のコピー** は、請求書スケジュールと実行ステータスをコピーします。
- **実績の更新** ボタンは、誤ってサマリー タスクを計算します。
- Microsoft Project アドイン: チーム メンバーのいずれかに空のリソース単位がある場合、Null 参照エラーを修正します。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
