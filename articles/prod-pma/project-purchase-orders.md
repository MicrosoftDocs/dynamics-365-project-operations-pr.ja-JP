---
title: プロジェクトの発注書
description: この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。 使用する方法は、発注書の目的、および購入したアイテムがいつ消費されてプロジェクトに請求されるかによって異なります。
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5de28f3844b802a980c811411cae75549c697538f89e8c3d2495ea171a188524
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008997"
---
# <a name="purchase-orders-for-a-project"></a>プロジェクトの発注書

[!include [banner](../includes/banner.md)]

この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。 使用する方法は、発注書の目的、および購入したアイテムがいつ消費されてプロジェクトに請求されるかによって異なります。

### <a name="methods-for-creating-a-purchase-order"></a>発注書の作成方法

次のいずれかの方法を使用してプロジェクト管理と会計で発注書を作成できます。 発注書の目的は、発注書がいつ消費され、アイテムがいつプロジェクトに請求されるかを決定します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>メソッド</th>
<th>目的</th>
<th>品目の消費</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>プロジェクトから直接発注書を作成します。</td>
<td>このメソッドを使用して、プロジェクトで消費するために外部仕入先からアイテムを購入します。 発注書は 2 日で作成できます。
<ul>
<li>プロジェクト自体から。 この場合、プロジェクトは発注書に対してすでに定義されています。</li>
<li>プロジェクトの発注書に移動する。 仕入先とプロジェクトの両方を選択して、発注書を作成する必要があります。</li>
</ul></td>
<td>品目はベンダー請求書が更新されるときに消費されます。</td>
</tr>
<tr class="even">
<td>販売注文から発注書を作成します。</td>
<td>このメソッドは、プロジェクトから受注を作成する場合、アイテムを購入するために使用します。</td>
<td>品目は、受注が顧客に請求されるときに消費されます。</td>
</tr>
<tr class="odd">
<td>品目要件から発注書を作成します。</td>
<td>このメソッドは、プロジェクトからアイテム要件を作成する場合、アイテムを購入するために使用します。</td>
<td>品目は、品目要件梱包明細が更新されるときに消費されます。</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> 仕入先請求書または梱包明細を更新すると、アイテム要件の梱包明細を更新するように求められます。

詳細については、[アイテム要件から発注書のアイテムを受け取る](tasks/receive-items-purchase-order-item-requirement.md) を参照してください。



[!INCLUDE[footer-include](../includes/footer-banner.md)]