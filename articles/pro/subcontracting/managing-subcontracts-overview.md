---
title: Project Operations での外注管理
description: このトピックでは、Microsoft Dynamics 365 Project Operations でのエンドツーエンドの外注管理プロセスの概要について説明しています。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994237"
---
# <a name="subcontract-management-in-project-operations"></a>Project Operations での外注管理

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

Microsoft Dynamics 365 Project Operations の外注は、次のビジネス プロセス フローをサポートします。

![外注プロセス フロー](../media/SubcontractingProcessFlow.png)

外注プロセスの段階的な説明は次のとおりです。

1. プロジェクト マネージャーは、ベンダーとの下請け契約を作成します。 既定では、ベンダー レコードに添付されている価格表が外注に使用されます。 ベンダー勘定の関係タイプは、**ベンダー** または **サプライヤー** です。
2. プロジェクト マネージャーは、すべての購入を外注の品目として項目化できます。 外注品目は、時間、費用、または製品の場合があります。 各外注品目で選択されたトランザクション クラスによって、その行の目的が決まります。
3. ベンダー アカウント マネージャーとプロジェクト マネージャーは、外注を繰り返すことができます。 価格は、外注に添付された購買価格表で調整することができます。
4. このプロセスの現時点またはこれ以降で、外注品目が時間の場合、ベンダー アカウント マネージャーは取引先企業を各外注品目に関連付けます。 この関連付けは、外注に対応しているプロジェクト マネージャーに役立つ情報です。 取引先企業が外注品目に関連付けられている場合、予約可能リソースがまだ存在しない場合は、取引先企業から予約可能リソースが自動的に作成されます。
5. 各外注品目の請求方法は、**固定価格** または **時間と材料** です。 固定価格の外注品目の場合、マイルストーンベースの請求書スケジュールを設定できます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
