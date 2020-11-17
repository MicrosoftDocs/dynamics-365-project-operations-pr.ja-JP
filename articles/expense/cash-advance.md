---
title: 現金前払い
description: このトピックでは、現金前払いについて説明します。
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079151"
---
# <a name="cash-advance"></a>現金前払い

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

現金前払いにより、従業員は経費が発生する前に会社からお金を借りることができます。 要求された現金前払いが承認されて支払われると、従業員はそのお金を、これから発生する可能性のある経費に使用できます。 

## <a name="create-and-submit-a-cash-advance-request"></a>現金前払い申請を作成して送信する

1. **自分の経費** の下にある **現金前払い** > **新規** を選択し、新規の現金前払いを作成します。 
2. に **新規現金前払い申請** ページで、経費の目的を入力し、経費が発生する場所を選択します。
3. 要求された金額と通貨を入力してから、 **保存** を選択します。 
4. 現金前払い申請を送信する準備ができたら、 **現金前払い申請** ページで、 **ワークフロー** > **送信** を選択します。

## <a name="modify-a-cash-advance-request"></a>現金前払い申請を修正する

承認のために提出されていない場合は、現金前払い申請を修正できます。

1. **自分の経費: 現金前払い** の下で、修正したい現金前払いを検索して修正します。
2. **編集** を選択し、現金前払い申請に必要な変更を加えます。 
3. **保存して閉じる** を選択します。


## <a name="view-cash-advance-requests"></a>現金前払い申請を表示する
**自分の経費: 現金前払い** の下で、下書き、送信済、レビュー済、または支払い済すべての現金前払いリストを確認することができます。 

## <a name="approve-cash-advance-requests"></a>現金前払い申請を承認する

ワークフローで承認者として構成されたマネージャーまたはユーザーは、レビューのために送信された現金支払いを承認できます。 

1. 現金前払いを承認するには、 **現金前払いのプロセス** の下の、 **レビュー用現金前払い** を選択します。
2. レビューの必要がある現金前払いを選択し、 **承認** を選択します。  

## <a name="pay-cash-advances"></a>現金前払いの支払い 
次の手順は、通常、会計士または会計権限を持つユーザーが実行します。

1. 承認された現金前払いを投稿するには、 **承認された現金前払い** を選択してから、 **支払いと送金** を選択します。  
2. 現金前払いのために仕訳帳詳細に入力し、 **OK** を選択します。 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>支払われた現金前払いに対して経費清算書を送信する 

すでに受け取った現金前払いの経費清算書を作成して送信すると、経費はその現金前払いに対して自動的に調整されます。 現金前払いが経費額よりも大きい場合は、 **現金償還** 経費カテゴリを使用して、残高を会社に返還する必要があります。 会社が支払った現金前払いが経費より少ない場合、会社はあなたに残高を払い戻す必要があります。 

### <a name="example"></a>例
あなたはシアトルからニューヨーク市へ会議のために旅行することを計画しています。 会議のチケット、フライト、ホテル、食事、タクシーの費用を見積もって、$3000 USD の現金前払い申請を作成します。 上司がこの申請を承認しない限り、支払いは行われません。 上司が承認した後、要求された現金前払い $3000 USDは銀行口座に支払われます。 それから会議に参加します。 旅行を終えた後、合計支出は$2790 USDだけだったことがわかります。 **支払方法** フィールドの **現金** を選択し、$2790 USDの経費を送信します。 送信された経費額は、貸与された $3000 USD の現金前払いに対して自動的に調整されます。 これで、会社に $210 USD (3000.00-2790.00) の借りがあり、 **現金償還** 経費カテゴリを使用して会社に返金することができます。 