---
title: 経費精算書を転記する
description: このトピックでは、総勘定元帳に経費精算書を転記する方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079414"
---
# <a name="post-an-expense-report"></a>経費精算書を転記する

[!include [banner](../includes/banner.md)]

経費精算書は、承認されて一般仕訳帳に転送された後、総勘定元帳に転記することができます。 経費清算書を転記すると、付加価値税 (VAT) の還付に適用できる経費が特定されます。 VAT の支払いの確認および還付のタスクは、経費清算書の確認を担当する従業員に割り当てられます。

経費精算書の経費が従業員を雇用している会社以外の会社に請求される場合は、経費の支払先会社と経費の支払元会社を確認する必要があります。 たとえば、経費清算書を送信した従業員は DAT 社に勤務しているが、DIR 社への経費を請求されたとします。 この場合、DAT は経費の支払先会社、DIR は経費の支払元会社です。 これらの仕訳帳明細行を確認した後は、経費明細行を一般会計に転記できます。

経費清算書を転記するには、 **承認された経費清算書** ページで経費清算書を選択し、アクション ウィンドウで **転記** を選択します。

同時にリストですべての経費清算書を転記することもできます。 すべての経費清算書を選択し、 **転記** を選択します。
