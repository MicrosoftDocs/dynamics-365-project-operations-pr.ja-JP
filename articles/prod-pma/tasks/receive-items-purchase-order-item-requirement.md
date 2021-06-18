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
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011692"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="e214c-103">品目要件から発注書の品目を受け取る</span><span class="sxs-lookup"><span data-stu-id="e214c-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e214c-104">このトピックでは、品目要件から発注書の品目を受け取る方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e214c-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="e214c-105">品目トランザクションの代わりに品目要件を使用することにより、品目が実際に使用される直前に配送を計画し、発注書を作成して、貿易合意フレームワークに品目を含め、生産計画に品目要件を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e214c-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="e214c-106">このタスクでは、USSI データセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="e214c-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e214c-107">ナビゲーションペインで、**モジュール > プロジェクト管理および会計 > プロジェクト >すべてのプロジェクト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e214c-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="e214c-108">リストで、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="e214c-109">アクション ペインで、**計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="e214c-110">**品目要件** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="e214c-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e214c-111">Select **New**.</span></span>
6. <span data-ttu-id="e214c-112">新しい行の **品目番号** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="e214c-113">**数量** フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="e214c-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="e214c-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-114">Select **Save**.</span></span>
9. <span data-ttu-id="e214c-115">アクション ペインで、**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="e214c-116">**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-116">Select **Functions**.</span></span>
11. <span data-ttu-id="e214c-117">**発注書を作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="e214c-118">**すべてを含める** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e214c-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="e214c-119">**仕入先口座** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="e214c-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-120">Select **OK**.</span></span>
15. <span data-ttu-id="e214c-121">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e214c-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="e214c-122">リストで、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="e214c-123">[アクション] ウィンドウで、**購入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="e214c-124">**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="e214c-125">アクション ウィンドウで、**受領** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="e214c-126">**製品受領書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="e214c-127">**製品受領書** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e214c-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="e214c-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e214c-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]