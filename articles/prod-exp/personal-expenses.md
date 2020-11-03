---
title: 経費報告書の個人的な経費
description: このトピックでは、Microsoft Dynamics 365 Finance で従業者の個人的な経費を処理するための 2 つの方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079417"
---
# <a name="personal-expenses-on-an-expense-report"></a>経費報告書の個人的な経費

[!include [banner](../includes/banner.md)]

出張中に、従業者が会社のクレジットカードに個人的な経費を付けることがあります。 個人的な経費の処理プロセスを定義しないと、従業者が項目別経費報告書を提出したときに、経費報告書の承認プロセスが中断される可能性があります。 

従業者の個人的な経費を処理する方法には 2 つあります:

- **従業員による支払い** – 組織は、会社のクレジット カードの請求書に記載されている個人的な経費を支払いません。 代わりに、会社のクレジットカードに請求された個人的な経費を会社の経費と一緒に表示するレポートを作成します。
- **会社による支払い** – 組織は、会社のクレジットカードの全額を支払い、その後、個人的な経費を従業者の口座から引き落とします。

**経費管理パラメーター** ページで、組織が使用する方法を選択できます。
