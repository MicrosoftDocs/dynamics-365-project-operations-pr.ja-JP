---
title: 会社間プロジェクト請求を構成する
description: このトピックでは、組織内の 2 つの会社間でプロジェクト請求を設定する方法について説明します。
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001207"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="c20e0-103">会社間プロジェクト請求を構成する</span><span class="sxs-lookup"><span data-stu-id="c20e0-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c20e0-104">このトピックでは、組織内の 2 つの会社間でプロジェクト請求を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="c20e0-105">このタスクでは、USSI データセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c20e0-106">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > ベンダー > すべてのベンダー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c20e0-107">**すべてのベンダー** リストで、目的のレコードを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="c20e0-108">アクション ウィンドウで、**全般** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c20e0-109">**会社間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="c20e0-110">**アクティブ** を **はい** に設定し、会社間取引を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="c20e0-111">**顧客の会社** フィールドに値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="c20e0-112">**自分のアカウント** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="c20e0-113">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-113">Select **Save**.</span></span>
9. <span data-ttu-id="c20e0-114">ページを閉じてホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="c20e0-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="c20e0-115">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > プロジェクト管理および会計パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="c20e0-116">**会社間** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="c20e0-117">スライダーを **はい** に移動させ、会社間リソース スケジュールとタイムシートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="c20e0-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c20e0-119">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-119">Select **New**.</span></span>
15. <span data-ttu-id="c20e0-120">**借入法人** フィールドで、値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="c20e0-121">**売上の計上** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="c20e0-122">**既定のタイムシート カテゴリ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="c20e0-123">**既定の経費カテゴリ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="c20e0-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-124">Select **Save**.</span></span>
20. <span data-ttu-id="c20e0-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c20e0-125">Close the page.</span></span>
21. <span data-ttu-id="c20e0-126">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 転記 > 元帳転記の設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="c20e0-127">**勘定科目の種類** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="c20e0-128">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-128">Select **New**.</span></span>
24. <span data-ttu-id="c20e0-129">新しい行の **主勘定** フィールドで、必要な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="c20e0-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-130">Select **Save**.</span></span>
26. <span data-ttu-id="c20e0-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c20e0-131">Close the page.</span></span>
27. <span data-ttu-id="c20e0-132">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 移転価格** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="c20e0-133">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c20e0-133">Select **New**.</span></span>
29. <span data-ttu-id="c20e0-134">**有効日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="c20e0-135">**借入法人** フィールドで、値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="c20e0-136">**移転価格モデル** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="c20e0-137">**価格** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="c20e0-138">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c20e0-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]