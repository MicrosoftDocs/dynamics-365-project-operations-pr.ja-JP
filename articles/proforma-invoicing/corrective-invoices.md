---
title: 請求書の修正
description: このトピックでは、請求書の修正に関する情報を提供します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122394"
---
# <a name="corrected-invoices"></a>請求書の修正

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

確認済みの請求書は編集可能です。 確認済みの請求書を編集すると、修正請求書のドラフトが作成されます。 元の請求書のすべてのトランザクションと数量を取り消すことを前提としているため、この修正請求書には元の請求書のすべてのトランザクションが含まれ、その数量はすべて 0 (ゼロ) となります。

トランザクションが修正を必要とない場合は、その修正請求書をドラフトから削除できます。 部分的に数量を取り消す、または元に戻す場合は、明細行の詳細の数量フィールドを編集できます。 請求明細行の詳細を開くと、元の請求書の数量が表示されます。 その後、現在の請求書の数量を編集して、元の請求書の数量よりも少なく、または多くすることができます。

修正請求書を確認すると、元の請求済み売上実績が取り消され、新規の請求済み売上実績が作成されます。 数量が削減された場合、差異により未請求売上実績も作成されます。 例えば、元の請求済み売上が 8 時間分であり、修正された請求明細行の詳細の数量が 6 時間に減少した場合、元の請求売上明細行を戻し、新たに 2 つの実績が作成されます :

- 6 時間の請求済み売上実績。
- 残り 2 時間の未請求売上実績。 このトランザクションは、顧客との交渉に応じて後で請求するか、または、請求不可としてマークすることができます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]