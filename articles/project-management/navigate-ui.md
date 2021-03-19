---
title: ユーザー インターフェイスのナビゲーション
description: このトピックは、Dynamics 365 プロジェクト操作でのプロジェクト管理に関する情報を提供します。
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286749"
---
# <a name="navigating-the-user-interface"></a>ユーザー インターフェイスのナビゲーション

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

## <a name="overview"></a>概要

メイン プロジェクト フォームはいくつかのタブに分かれています。 各タブは、プロジェクト内のさまざまな詳細レベルを表します。

- **概要**: プロジェクトの説明を提供し、計画されたプロジェクトのパフォーマンスと実際のプロジェクトのパフォーマンスの両方を集約します。

    ![概要タブとフィールド](media/navigation7.png)

- **タスク**: グリッド ビュー、ボード ビュー、およびガントで表される WBS (作業分解構造) に関する詳細を提供します。

    ![タスク タブとフィールド](media/navigation8.png)

- **チーム**: プロジェクト参加者に関する詳細を提供します。 各チームメンバーに割り当てられた作業もこのビューに要約されます。

    ![チーム タブとフィールド](media/navigation9.png)

- **リソースの割り当て**: プロジェクトの各リソースの作業の時間フェーズ ビューを提供します。

    ![リソースの割り当てタブとフィールド](media/navigation10.png)

- **リソースの調整**: 各名前付きリソースの割り当てとその予約の差を時間フェーズ ビューで提供します。

    ![リソースの調整タブとフィールド](media/navigation11.png)

- **見積もり**: プロジェクトのコストと売上の見積もりの時間フェーズ ビューを提供します。

    ![見積もりタブとフィールド](media/navigation12.png)

- **トラッキング**: 作業、コスト、および売上の WBS (作業分解構造) でのタスクの進行状況を示すビューを提供します。

    ![トラッキング タブとフィールド](media/navigation13.png)

- **営業**: プロジェクトに関連する見積もりと契約へのディープ リンクを提供します。

- **経費の見込み**: 組織の経費カテゴリに基づいてプロジェクト経費を定義するグリッドを提供します。

    ![経費見積もりタブとフィールド](media/navigation14.png)

## <a name="grid-controls"></a>グリッド コントロール

以下は、さまざまなプロジェクト計画タブにある一般的なコントロールの簡単な概要です。

### <a name="refresh"></a>最新の情報に更新

**更新**: グリッドのロード後に変更が発生した場合、サーバーから最新のデータを取得します。

![更新ボタン](media/navigation7.png)

### <a name="group-by"></a>グループ化の基準

**グループ化**: グリッド内の行のグループ化を更新して、ユーザーのニーズに基づいてリソース、役割、またはカテゴリのいずれかを反映します。

![ボタンによるグループ](media/navigation6.png)

### <a name="previousnext"></a>前へ/次へ

**前へ**/**次へ**: 時間フェーズ グリッド上で表示されている期間を更新します。

![前へボタンと次へボタン](media/navigation2.png)

### <a name="timescale"></a>タイムスケール

**タイムスケール**: 日、週、月、年で時間フェーズ データの集計を変更します。

![タイムスケール ボタン](media/navigation3.png)

### <a name="expand"></a>展開する

**展開**: 表示されているグリッドを全画面表示にして、追加の役割を表示する機能を強化します。

![[展開] ボタン](media/navigation4.png)

### <a name="time-phase-by"></a>時間フェーズ別

**時間フェーズ別**: グリッド内の行のグループを更新して、売上見積もりのコスト見積もりを反映します。 この制御は、見積もりスクリプトとトラッキング グリッドにも適用されます。

![ボタンによる時間フェーズ](media/navigation0.png)

### <a name="add-column"></a>列を追加します

**列を追加**: ユーザーがグリッドに表示される列を定義できるようにします。 **プロジェクト計画** フォームで、すぐに使用できる列のみをグリッドに追加できます。

![列ボタンを追加](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]