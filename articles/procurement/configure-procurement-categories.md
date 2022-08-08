---
title: プロジェクトの発注書と保留中のベンダーの請求書で調達カテゴリを使用する
description: この記事では、プロジェクト発注書と保留中のベンダーの請求書で使用できる調達カテゴリを設定する方法について説明します。
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028616"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>プロジェクトの発注書と保留中のベンダーの請求書で調達カテゴリを使用する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

購買担当者は、プロジェクトの発注書や保留中のベンダーの請求書に使用できる品目やサービスのカタログを作成し、管理することができます。 [調達カタログ](/dynamics365/supply-chain/procurement/procurement-catalogs)では、リリースされた製品カタログを構成して使用することなく、購入を分類する簡単な方法を提供します。 各調達カテゴリは、時間、費用、または品目トランザクションのプロジェクト カテゴリにマッピングできます。 調達カテゴリを使用する保留中のベンダー請求書が計上された後、システムは時間、費用、材料プロジェクトの実績、プロジェクト トランザクション、および補助元帳エントリを作成します。

## <a name="minimum-version-requirements"></a>必要最小バージョン

Microsoft Dynamics 365 Project Operations の非在庫/リソース ベースのシナリオで、プロジェクト発注で調達カテゴリを使用するには、以下のバージョンが必要です:

- Project Operations Dataverse ソリューション バージョン 4.41.0.45 以降
- 財務と運用環境バージョン 10.0.26 以降

## <a name="run-dual-write-maps-for-procurement-category-support"></a>調達カテゴリ対応のデュアル ライト マップの実行

**Project Operations 統合プロジェクト ベンダー用請求書エクスポート エンティティ msdyn\_projectvendorinvoicelines** 用のマッピングがバージョン 1.0.0.4 以降を使用していることを確認してください。

## <a name="enable-the-feature-key-for-procurement-categories"></a>調達カテゴリの機能キーを有効にする

次の手順に従って、プロジェクト発注書で調達カテゴリを使用するための機能を有効にします。

1. Dynamics 365 Finance で、**機能管理** ワークスペースを開きます。
1. 機能リストで、**リソースベース/非在庫シナリオに、Project Operations で調達カテゴリを使用する** 機能を見つけて選択し、**有効化** を選択します。

> [!IMPORTANT]
> そのための前提条件として、**リソースベース/非在庫シナリオで、Project Operations でベンダーへの請求書発行を保留する** 機能も有効にしておく必要があります。

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>調達カテゴリ階層にプロジェクト カテゴリをマッピングする

以下の手順に従って、プロジェクト カテゴリーと調達カテゴリーを **調達カテゴリー階層** にマッピングします:

1. **調達とソーシング \> 調達カテゴリ** の順に移動します。
1. **カテゴリ階層の編集** を選択します。
1. 目的のカテゴリ階層ノードを選択してから、**プロジェクト カテゴリの割り当て** タブで、**時間**、**経費**、**品目プロジェクト** のカテゴリー (**既定の時間** または **既定の経費** カテゴリー) から、ノードをプロジェクトカテゴリーに関連付けます。
1. **保存** を選択します。
1. ページを閉じます。

> [!NOTE]
> 調達カテゴリのプロジェクト カテゴリへのマッピングはオプションです。 調達カテゴリがマッピングされていない場合、システムは **プロジェクト管理および会計パラメータ** ページの **Dynamics 365 Customer engagement の Project Operations** タブにある **既定のプロジェクトカテゴリー** セクションの **品目** フィールドに設定されている値を使用します。
