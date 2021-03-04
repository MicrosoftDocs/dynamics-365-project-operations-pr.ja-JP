---
title: 固定価格売上見積もりプロジェクト
description: このトピックは、プロジェクトの固定価格売上に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531474"
---
# <a name="fixed-price-revenue-estimate-projects"></a>固定価格売上見積もりプロジェクト 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Microsoft Dataverse の Dynamics 365 Project Operations で以下の属性を使用してプロジェクト契約品目を作成すると、システムは固定価格の売上見積もりプロジェクトを自動で作成します。 このプロジェクトの情報は、以下に基づいています。

  - 固定価格の請求方法。
  - 関連するプロジェクト。
  - **プロジェクト契約品目** ページの **請求スケジュール** タブで定義した少なくとも 1 件のマイルストーン。

## <a name="review-fixed-price-revenue-estimates-projects"></a>固定価格の売上見積もりプロジェクトを確認する
固定価格の売上見積もりプロジェクトを確認する際は、次の手順を実行します。

1. Dynamics 365 Finance 環境で **プロジェクト管理と会計** > **プロジェクト** > **固定価格の売上見積もりプロジェクト** に順に移動します。
2. 確認するプロジェクトを選択し、**見積もりプロジェクト ID** をダブルクリックしてレコードを開き、プロジェクトの詳細を確認します。
3. **プロジェクト** タブを展開します。**選択したプロジェクト** グリッドに 1 件のプロジェクトが表示されます。 これはプロジェクト契約品目に関連付けられたプロジェクトなので、これを既定プロジェクトとしてシステムが使用します。 
4. 関連付けを変更する場合はさらにプロジェクトを選択して、それらを **選択したプロジェクト** グリッドに追加します。 このグリッドで複数のプロジェクトを選択すると、選択したすべてのプロジェクトに対してプロジェクトの完了割合と収益の見積もりを一緒に計算します。

  プロジェクトのコスト、売上プロファイル、コスト テンプレート、期間コードを手動で設定できます。 手動で設定しない場合は、プロジェクトのコストと売上プロファイルに対して構成したルールを使用するプロジェクトの最初の見積もり計算時に、この値が既定になります。



[!INCLUDE[footer-include](../includes/footer-banner.md)]