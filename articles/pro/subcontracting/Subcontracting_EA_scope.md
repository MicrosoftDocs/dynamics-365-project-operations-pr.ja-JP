---
title: 2021 年 10 月の早期アクセス リリースでの外注
description: このトピックは、2021 年 10 月の早期アクセス リリースの一部である Project Operations における外注機能の概要を提供します。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383701"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>2021 年 10 月の早期アクセス リリースでの外注

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

このトピックは、2021 年 10 月の早期アクセス リリースの一部である Dynamics 365 Project Operations における外注機能の概要を提供します。 この機能セットは実稼働環境またはライブ環境に対応していないため、これらの機能は、完全な機能セットがリリースされるまで早期アクセス リリースのままになります。 プレビュー バナーが削除されるまで、実稼働シナリオに外注機能セットを使用しないことを強くお勧めします。 

次のリストは、2021 年 10 月の早期アクセス リリースで現在利用可能なものの概要を示しています。

1. プロジェクト マネージャーは、ベンダーとの下請け契約を作成します。 既定では、ベンダー レコードに添付されている価格表が外注に使用されます。 ベンダー勘定の関係タイプは、**ベンダー** または **サプライヤー** です。

2. プロジェクト マネージャーは、すべての購入を外注の品目として項目化できます。 外注品目は、時間、費用、または製品の場合があります。 外注品目のトランザクション クラスによって、その行の目的が決まります。

3. ベンダー アカウント マネージャーとプロジェクト マネージャーは、外注を繰り返すことができます。 価格は、外注に添付された購買価格表で調整することができます。

4. このプロセスの現時点またはこれ以降で、外注品目が時間の場合、ベンダー アカウント マネージャーは仕入先連絡先を各外注品目に関連付けます。 この関連付けは、外注に対応しているプロジェクト マネージャーに役立つ情報です。 仕入先連絡先が外注品目に関連付けられている場合、予約可能リソースがまだ存在しない場合は、取引先企業から予約可能リソースが自動的に作成されます。

5. 各外注品目の請求方法は、**固定価格** または **時間と材料** です。 固定価格の外注品目の場合、マイルストーンベースの請求書スケジュールが設定されます。

概要で概説されている外注のビジネス プロセス フローの残りの手順は、現在利用できません。 新しい機能が追加されると、このトピックが更新されます。 

次の図は、エンド ツー エンドのビジネス プロセスと比較した、外注の早期アクセス リリースを表しています。

![外注プロセス フロー](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>数量基準の外注品目と作業基準の外注品目の早期アクセス リリース
2021 年 10 月の早期アクセス リリースでは、数量基準の外注品目のみがサポートされています。 つまり、外注品目を使用して、時間、費用、または材料をベンダーから購入することはできますが、作業全体を購入することはできません。 これは、外注品目で購入された数量 (時間単位、費用、または材料の数量) を、システム内の任意のプロジェクトで使用できることも意味します。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]