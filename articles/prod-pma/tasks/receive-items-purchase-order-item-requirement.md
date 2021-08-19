---
title: 品目要件から発注書の品目を受け取る
description: このトピックでは、品目要件から発注書の品目を受け取る方法について説明します。
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da5eff576040f20cc206800b4d4ca987d08b0185ec5364bc1efc940f85d36371
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998962"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>品目要件から発注書の品目を受け取る

[!include [banner](../../includes/banner.md)]

このトピックでは、品目要件から発注書の品目を受け取る方法について説明します。

品目トランザクションの代わりに品目要件を使用することにより、品目が実際に使用される直前に配送を計画し、発注書を作成して、貿易合意フレームワークに品目を含め、生産計画に品目要件を含めることができます。 

このタスクでは、USSI データセットを使用します。

1. ナビゲーションペインで、**モジュール > プロジェクト管理および会計 > プロジェクト >すべてのプロジェクト** に移動します。
2. リストで、目的の行のリンクを選択します。
3. アクション ペインで、**計画** を選択します。
4. **品目要件** を選択します。
5. **新規** をクリックします。
6. 新しい行の **品目番号** フィールドで、値を入力または選択します。
7. **数量** フィールドに番号を入力します。
8. **保存** を選択します。
9. アクション ペインで、**管理** を選択します。
10. **機能** を選択します。
11. **発注書を作成する** を選択します。
12. **すべてを含める** チェック ボックスをオンにします。
13. **仕入先口座** フィールドで、値を入力または選択します。
14. **OK** を選択します。
15. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > すべての発注書** に移動します。
16. リストで、目的の行のリンクを選択します。
17. [アクション] ウィンドウで、**購入** を選択します。
18. **確認** を選択します。
19. アクション ウィンドウで、**受領** を選択します。
20. **製品受領書** を選択します。
21. **製品受領書** フィールドに値を入力します。
22. **OK** を選択します。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]