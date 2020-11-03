---
title: 品目要件から発注書の品目を受け取る
description: このトピックでは、品目要件から発注書の品目を受け取る方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079435"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="4a27a-103">品目要件から発注書の品目を受け取る</span><span class="sxs-lookup"><span data-stu-id="4a27a-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a27a-104">このトピックでは、品目要件から発注書の品目を受け取る方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="4a27a-105">品目トランザクションの代わりに品目要件を使用することにより、品目が実際に使用される直前に配送を計画し、発注書を作成して、貿易合意フレームワークに品目を含め、生産計画に品目要件を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4a27a-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="4a27a-106">このタスクでは、USSI データセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4a27a-107">ナビゲーションペインで、 **モジュール > プロジェクト管理および会計 > プロジェクト >すべてのプロジェクト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="4a27a-108">リストで、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="4a27a-109">アクション ペインで、 **計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="4a27a-110">**品目要件** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="4a27a-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a27a-111">Select **New**.</span></span>
6. <span data-ttu-id="4a27a-112">新しい行の **品目番号** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="4a27a-113">**数量** フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="4a27a-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-114">Select **Save**.</span></span>
9. <span data-ttu-id="4a27a-115">アクション ペインで、 **管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="4a27a-116">**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-116">Select **Functions**.</span></span>
11. <span data-ttu-id="4a27a-117">**発注書を作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="4a27a-118">**すべてを含める** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4a27a-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="4a27a-119">**仕入先口座** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="4a27a-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-120">Select **OK**.</span></span>
15. <span data-ttu-id="4a27a-121">ナビゲーション ウィンドウで、 **モジュール > 買掛金勘定 > 発注書 > すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="4a27a-122">リストで、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="4a27a-123">[アクション] ウィンドウで、 **購入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="4a27a-124">**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="4a27a-125">アクション ウィンドウで、 **受領** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="4a27a-126">**製品受領書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="4a27a-127">**製品受領書** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="4a27a-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a27a-128">Select **OK**.</span></span>

