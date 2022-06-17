---
title: 固定価格売上見積もりプロジェクト
description: この記事では、プロジェクトでの固定価格売上について説明します。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928392"
---
# <a name="fixed-price-revenue-estimate-projects"></a>固定価格売上見積もりプロジェクト 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Microsoft Dataverse の Dynamics 365 Project Operations で以下の属性を使用してプロジェクト契約品目を作成すると、システムは固定価格の売上見積もりプロジェクトを自動で作成します。 このプロジェクトの情報は、以下に基づいています。

  - 固定価格の請求方法。
  - 関連するプロジェクト。
  - **プロジェクト契約品目** ページの **請求スケジュール** タブで定義した少なくとも 1 件のマイルストーン。

## <a name="review-fixed-price-revenue-estimates-projects"></a>固定価格の売上見積もりプロジェクトを確認する
固定価格の売上見積もりプロジェクトを確認する際は、次の手順を実行します。

1. Dynamics 365 Finance 環境で、**プロジェクト管理と会計** > **プロジェクト** > **固定価格収入見積もりプロジェクト** に移動します。
2. 確認するプロジェクトを選択し、**見積もりプロジェクト ID** をダブルクリックしてレコードを開き、プロジェクトの詳細を確認します。
3. **プロジェクト** タブを展開します。**選択したプロジェクト** グリッドに 1 件のプロジェクトが表示されます。 これはプロジェクト契約品目に関連付けられたプロジェクトなので、これを既定プロジェクトとしてシステムが使用します。 
4. 関連付けを変更する場合はさらにプロジェクトを選択して、それらを **選択したプロジェクト** グリッドに追加します。 このグリッドで複数のプロジェクトを選択すると、選択したすべてのプロジェクトに対してプロジェクトの完了割合と収益の見積もりを一緒に計算します。

  プロジェクトのコスト、売上プロファイル、コスト テンプレート、期間コードを手動で設定できます。 手動で設定しない場合は、プロジェクトのコストと売上プロファイルに対して構成したルールを使用するプロジェクトの最初の見積もり計算時に、この値が既定になります。



[!INCLUDE[footer-include](../includes/footer-banner.md)]