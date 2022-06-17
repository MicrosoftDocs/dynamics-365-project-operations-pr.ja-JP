---
title: 経費の概要
description: この記事では、Project Operations での経費機能について説明します。
author: stsporen
ms.date: 10/06/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 935998adda4a967285d68016b4dad0bc2b0c56dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917904"
---
# <a name="expense-home-page"></a>経費ホーム ページ

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


Dynamics 365 Project Operations は、経費を処理する機能をサポートします。 経費処理は、ポリシー、トランザクション カテゴリ、および承認のカスタマイズ可能なワークフローを使用し、プロジェクトに関連して、またはプロジェクトに関連せず発生します。

Project Operations では、経費に対して 2 つのサポートされている展開モデルがあります。 

- **完全**: 完全展開は、**リソース/非在庫ベースのシナリオ向け Project Operations** および **製造オーダーに基づくシナリオ向け Project Operations** に利用できます。
- **基本**: 基本展開は **リソース/非在庫ベースのシナリオ向け Project Operations** および **ライト展開 – 見積もり請求の取引** 用に利用できます。

## <a name="full"></a>すべて 
全経費展開は、次のようなポリシーを作成する機能を含む完全なポリシーの適用機能を提供します。

  - 経費カテゴリの制限
  - 出張
  - 日当
  - クレジット カードのインポート
  - 領収書の光学式文字認識

## <a name="basic"></a>Basic 
基本経費の展開シナリオでは、プロジェクトに対する基本経費のみを記録できます。 

詳細については、[経費の入力 (ライト)](basic-expense.md) を参照してください

## <a name="determine-your-expense-deployment"></a>経費の展開を決定する
基本経費の管理展開を実行しているかどうかを決定するには、アドレス URL が **.crm.dynamics.com** で終わることを確認します。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]