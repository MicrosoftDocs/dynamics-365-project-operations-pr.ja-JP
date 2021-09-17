---
title: 外注品目リソース
description: このトピックは、特定の外注品目に対してベンダーが提供する専用リソースを指定する方法を説明しています。
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323377"
---
# <a name="subcontract-line-resources"></a>外注品目リソース

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

Dynamics 365 Project Operations では、ベンダーは、時間に対して外注品目で購入するリソース キャパシティを供給するために使用されるリソースを指定できます。

## <a name="create-subcontract-line-resources"></a>外注品目リソースを作成する

外注品目リソースを作成するには、次の手順のようにします。

1. ナビゲーション ウィンドウで、**外注** を選択し、次に作業する外注を開きます。
2. 仕入先リソースを指定する時間の外注品目を開きます。
3. **外注品目リソース** タブのサブグリッドで、**+新しい外注品目リソース** を選択します。
4. **新しい外注品目マイルストーン** ページで、必要な情報を入力し、**保存して閉じる** を選択します。

次の表で、外注品目リソースのフィールドについて説明します。

| フィールド |  内容 |
| ----- | ------------ |
| 予約可能リソース | 外注品目のリソースとして使用する「契約社員」タイプの予約可能なリソースを選択します。 契約社員用の予約可能なリソースをまだ作成していない場合は、このフィールドを空のままにします。 レコードを保存すると、予約可能なリソースが作成されます。  |
| 連絡先 | **予約可能なリソース** フィールドが空の場合、既存の取引先担当者から外注品目リソースを作成できます。 ルックアップを使用して、システム内のアクティブな取引先担当者のリストを表示します。 この外注のベンダーの取引先担当者を選択します。 選択した取引先担当者は、レコードを保存するときに検証されます。 選択した取引先担当者が有効な取引先担当者でない場合、レコードは保存されません。 選択した取引先担当者の予約可能なリソースがない場合、外注品目リソースを作成する前に、選択した取引先担当者の予約可能なリソースが作成されます。 |
| ユーザー  | **予約可能なリソース** フィールドが空の場合、アクティブなユーザーを選択することで外注品目リソースを作成できます。 ルックアップを使用して、システム内のアクティブ ユーザーのリストを表示します。 選択したユーザーの予約可能なリソースがない場合、外注品目リソースを作成する前に、選択したユーザーの予約可能なリソースが作成されます。 |
| 開始日 | 外注作業者の割り当てが開始される日付。 このリソースがこの日付範囲より前の期間に予約された場合、警告が発生します。 |
| 終了日 | 外注作業者の割り当てが終了する日付。 このリソースがこの日付範囲より後の期間に予約された場合、警告が発生します。 |
| 工数 | 外注作業者がこの外注品目に費やす合計工数。 このリソースがこの外注に割り当てられた労力を超えて予約された場合、警告が発生します。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]