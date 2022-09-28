---
title: 経費精算書の転記
description: この記事では、経費精算書の転記方法について説明します。
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524875"
---
# <a name="post-expense-reports"></a>経費精算書の転記

経費精算書は、承認されて一般仕訳帳に転送された後、転記することができます。 経費清算書を転記すると、付加価値税 (VAT) の還付に適用できる経費が特定されます。 VAT の支払いの確認および還付のタスクは、経費清算書の確認を担当する従業員に割り当てられます。

経費報告書の経費が従業員の採用会社以外の会社に請求される場合は、経費の支払先会社と経費の支払元会社を確認する必要があります。 たとえば、経費清算書を送信した従業員は DAT 社に勤務しているが、DIR 社への経費を請求されたとします。 この場合、DAT は経費の支払先会社、DIR は経費の支払元会社です。 これらの仕訳帳明細行を確認した後は、経費明細行を一般会計に転記できます。

経費清算書を転記するには、**承認された経費清算書** ページで経費清算書を選択し、アクション ウィンドウで **転記** を選択します。

同時にリストですべての経費清算書を転記することもできます。 すべての経費清算書を選択し、**転記** を選択します。

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>現金支払方法機能のベンダー通貨で経費負債を転記する機能を有効にする

**現金支払方法機能のベンダー通貨で経費負債を転記する機能** を使用すると、経費レポートを現金支払方法の仕入先通貨で転記できます。

現在、現金経費を提出すると、経費レポートは会計通貨で転記されます。 取引通貨、会計通貨、仕入先通貨間の金額換算のため、経費の取引日と実際の支払日の為替レートが異なる場合、仕入先に誤った金額が支払われます。

この機能により、経費レポートが転記されるときに、仕入先残高が仕入先通貨で記録されるようになります。

1. **ワークスペース** \> **機能管理** の順に移動します。
2. リストで、**現金支払方法の仕入先通貨で経費負債を転記する機能** を検索して選択し、**今すぐ有効にする** を選択します。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
