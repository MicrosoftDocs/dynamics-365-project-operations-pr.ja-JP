---
title: 経費の概要
description: このトピックでは、Project Operations での経費機能に関する情報を提供します。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967372"
---
# <a name="expense-home-page"></a>経費ホーム ページ

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


Dynamics 365 Project Operations は、経費を処理する機能をサポートしています。 経費処理は、ポリシー、トランザクション カテゴリ、および承認のカスタマイズ可能なワークフローを使用して、プロジェクトの有無にかかわらず発生します。

Project Operations では、経費に対して 2 つのサポートされている展開モデルがあります。 

- **完全**: 完全展開は、**リソース/非在庫ベースのシナリオ向け Project Operations** および**製造オーダーに基づくシナリオ向け Project Operations** 用に利用できます。
- **基本**: 基本展開は**リソース/非在庫ベースのシナリオ向け Project Operations** および**ライト展開 – 見積もり請求の取引**用に利用できます。

## <a name="full"></a>すべて 
完全経費の展開は、次のような、ポリシーを作成する機能を含む完全なポリシーの実施を提供します。

  - 経費カテゴリの制限
  - 移動
  - 日当
  - クレジット カードのインポート
  - 領収書の光学式文字認識

## <a name="basic"></a>Basic 
基本経費の展開シナリオでは、プロジェクトに対する基本経費のみを記録できます。 

詳細については、[経費の入力 (ライト)](basic-expense.md) を参照してください

## <a name="determine-your-expense-deployment"></a>経費の展開を決定する
基本経費の管理展開を実行しているかどうかを決定するには、アドレス URL が **.crm.dynamics.com** で終わることを確認します。 
