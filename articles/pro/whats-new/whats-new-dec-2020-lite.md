---
title: 2020 年 12 月の新機能 - Project Operations Lite 展開 - 見積もり請求の取引
description: このトピックでは、Project Operations Lite 展開 - 見積もり請求の取引の 2020 年 12 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6a001cea56411865599a5c0a41fe47682dad35c2
ms.sourcegitcommit: 5791f6347e800fc4f6c76e7460947cb6824edebe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4700822"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>2020 年 12 月の新機能 - Project Operations Lite 展開 - 見積もり請求の取引

_**適用対象:** ライト展開 - 見積もり請求の取引_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

  - Dataverse 環境バージョン 4.5.0.134 での Project Operations 

次の表に、Dataverse 環境バージョン 4.4.0.70 の Project Operations に対する更新内容を示します。

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求と価格 | 1986009 | プロジェクトと契約品目のリンクが設定/解除される前に確認する場合は、手動で作成した仕訳帳明細行のパフォーマンスに一貫性がなくなります。 |
| 請求と価格 | 2014153 | 請求スケジュールから実行する場合、製品は請求されません。 |
| 請求と価格 | 2014159 | トランザクションで請求を更新する場合、製品はプルされません。 |
| 請求と価格 | 2028174 | 請求明細行詳細の更新は、仕訳帳の修正ロジックに従う必要があります。 |
| 請求と価格 | 2028315 | 編集できるネストされたグリッドの動作を修正します。 |
| 請求と価格 | 2031070 | 請求明細行修正の詳細の調整は、仕訳帳の修正ロジックに従う必要があります。 |
| 請求と価格 | 2034186 | 契約品目でプロジェクトの更新を可能にする必要があります。 |
| 請求と価格 | 2034206 | プロジェクトと契約品目のリンクを解除する際は、実際の取消時に調整ステータスの設定が必要です。 |
| 請求と価格 | 2040871 | 経費見積もりグリッドで単位と単位グループのセルについて更新を許可します。 |
| 請求と価格 | 2053754 | 請求書の編集で作成した実績は、調整ステータスと請求ステータスをマークしません。 |
| 請求と価格 | 2057874 | 請求明細行詳細の編集中に作成したトランザクション接続を修正します。 |
| 請求と価格 | 2057875 | 請求明細行詳細の編集中に作成したトランザクション発生元を修正します。 |
| 請求と価格 | 2057944 | 請求書修正の請求に対応していない実績に対して、コミット済みとして設定した超過しない状態。 |
| 請求と価格 | 2057963 | Create\_Product 特権を Create\_ProjectContract 特権から分割します。 |
| 請求と価格 | 2067622 | マイルストーンの生成中は処理中のアイコンを表示します。 |
| 請求と価格 | 2067624 | マイルストーンの生成時は、契約金額をビジネス推奨としてマークする必要があります。 |
| 請求と価格 | 2086880 | プロジェクト ベースの見積依頼明細行でリボンの **推奨** ボタンを非表示にします。 |
| 展開と構成 | 2101152 | Power Platform 管理センターで Project Operations テンプレートを使用して作成した新しい環境では、インストール後の操作をすべて実行する必要があります。 |
|  営業案件管理 | 2022204 | **プロジェクト** ページの **タスク請求** タブにあるプロジェクト ベースの請求グリッドに **すべてのタスク** の見積もり/契約品目が存在しない場合、またはその逆の場合、プロジェクト ベースのグリッドを非表示にする必要があります。 |
|  営業案件管理 | 2086601 | 非アクティブ化したロールとカテゴリは、見積依頼明細行と契約品目の課金対象のロールとカテゴリの一覧にコピーできません。 |
| プロジェクトの計画と追跡 | 1949065 | データの可視性は 200% ズーム時に正しく機能します |
| プロジェクトの計画と追跡 | 2046317 | Project Operations でプロジェクトのエンティティ名を変更できます |
| プロジェクトの計画と追跡 | 2057171 | **プロジェクト** ページの **プロジェクト開始日** フィールドが空の場合に使用する、更新されたエラー メッセージ。 |
| プロジェクトの計画と追跡 | 2057197 | タスク参照を使用した見積行のコピーはサポートしていません。 |
| プロジェクトの計画と追跡 | 2060687 | 特定期間の経過後にタイムゾーン警告が非表示になります。 |
| リソース管理 | 1832887 | Dataverse や Finance の環境で、繰り返し可能なデータ読み込みを行う際は、既定のリソース カテゴリ ID を静的にする必要があります。 |
| 時間と経費 | 2034882 | Dynamics 365 Field Service をインストールすると、**新規** ボタンが時間入力のコマンド バーに 2 回表示されます。 |
| 時間と経費 | 2056028 | **時間の編集** ページを更新してタイムラインを含めます。 |
| 時間と経費 | 1983747 | 時間入力グラフは追加データを示します。 |