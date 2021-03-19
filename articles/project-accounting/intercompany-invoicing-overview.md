---
title: 会社間請求の概要
description: このトピックでは、プロジェクトの会社間請求に関する情報と例を提供します。
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287334"
---
# <a name="intercompany-invoicing-overview"></a>会社間請求の概要

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

組織には、プロジェクトのために製品とサービスを相互に転送する複数の部署、子会社、およびその他の法人が存在する場合があります。 サービスや製品を提供する法人は *貸付法人* と呼ばれます。 サービスや製品を受領する法人は *借入法人* と呼ばれます。

次の図は、2 つの法人で典型的なシナリオを示します。Contoso Robotics USA (借入法人) と Contoso Robotics UK (貸付法人) リソースを共有して顧客である Adventure works にプロジェクトを提供します。 このシナリオでは、Contoso Robotics USA が Adventure Works に納品する契約を結んでいます。

![会社間請求](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations は会社間取引の処理に次のフローを使用します。

1. 貸付法人のリソースは、借入法人のプロジェクトに対して時間と費用を予約して、会社間の時間や経費のトランザクションを記録します。
2. 時間と経費のコストは、借入法人の単位原価の価格表を使用して貸付法人に記録します。
3. 会社間の未請求販売トランザクションは、借入法人の単位原価の価格表を使用して貸付法人に記録します。
4. 未請求売上は、プロジェクト契約の販売価格表を使用して借入法人に記録します。 未請求売上の記録時に顧客に請求できます。 顧客は会社間請求処理の完了を待つ必要がありません。
5. 会社間顧客請求書は貸付法人で定期的に作成します。 この請求書は、手動または定期的な自動プロセスを使用して作成します。 借入法人ごとに 1 つの請求書を作成することも、プロジェクトごとに個別の請求書を作成することもできます。
6. 会社間顧客請求書を貸付法人に転記すると、対応する保留中のベンダー請求書が借入法人に作成されます。 ベンダー請求書の保留中コストは、請求書の転記時にプロジェクトの補助元帳に記録します。

次の図は、会計イベントと一般会計への予測転記に関連する会社間請求を示します。

![会社間のフロー](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>その他のリソース

- [会社間請求の構成](configure-intercompany-invoicing.md)
- [会社間トランザクションの記録](create-intercompany-transactions.md)
- [会社間で顧客およびベンダーの請求書を作成する](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]