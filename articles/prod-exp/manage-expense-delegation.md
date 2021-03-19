---
title: 経費の委任を管理する
description: 経費代理人ユーザーは、組織内の別の従業員の経費レポートを作成および管理できます。
author: KimANelson
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2020-01-10
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9e3504a89f598c9acf3925e8b27930724ef2d3a5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271494"
---
# <a name="manage-expense-delegation"></a><span data-ttu-id="c3842-103">経費の委任の管理</span><span class="sxs-lookup"><span data-stu-id="c3842-103">Manage expense delegation</span></span>

<span data-ttu-id="c3842-104">経費委任者は、他の従業員の経費精算書を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="c3842-104">An expense delegate can create and manage expense reports for another employee.</span></span>

## <a name="configure-expense-delegation"></a><span data-ttu-id="c3842-105">経費代理人の構成</span><span class="sxs-lookup"><span data-stu-id="c3842-105">Configure expense delegation</span></span>

1. <span data-ttu-id="c3842-106">ユーザーを経費代理人として設定するには、**経費管理 > 設定 > 一般 > 代理人** に移動してください。</span><span class="sxs-lookup"><span data-stu-id="c3842-106">To set up a user as an expense delegate, go to **Expense management > Setup > General > Delegates**.</span></span>
2. <span data-ttu-id="c3842-107">**代理人** ページで、**新規** を選びます。</span><span class="sxs-lookup"><span data-stu-id="c3842-107">On the **Delegates** page, select **New**.</span></span>
3. <span data-ttu-id="c3842-108">代理人を定義する従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3842-108">Select the employee that will have a delegate defined.</span></span> 
4. <span data-ttu-id="c3842-109">代理ユーザーのエイリアス、委任期間の開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3842-109">Enter the alias of the delegate user and the start and end date for the delegation period.</span></span>

## <a name="manage-expense-delegation-for-another-employee"></a><span data-ttu-id="c3842-110">別の従業員の経費委任を管理する</span><span class="sxs-lookup"><span data-stu-id="c3842-110">Manage expense delegation for another employee</span></span>

<span data-ttu-id="c3842-111">機能管理キー **経費代理人リスト ページを有効にする** が有効になっている場合、**自分に委任された経費** リスト ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3842-111">When the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available.</span></span> <span data-ttu-id="c3842-112">**経費管理** > **自分の経費** > **自分へ委任された経費** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c3842-112">Go to **Expense management** > **My expenses** > **Expenses delegated to me**.</span></span>

<span data-ttu-id="c3842-113">代理人ユーザーは、委任された既存の経費報告書をすばやくフィルターして検索できます。</span><span class="sxs-lookup"><span data-stu-id="c3842-113">A delegate user can quickly filter and search on existing expense reports that have been delegated to them.</span></span> <span data-ttu-id="c3842-114">また、**新しい経費精算書** を選択して、他のユーザーに新しい経費精算書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="c3842-114">They can also create a new expense report for other users by selecting **New expense report**.</span></span>

<span data-ttu-id="c3842-115">代理人ユーザーは、**経費管理** > **自分の経費** > **経費清算書** に移動して、**他のユーザーの経費を開く** を選択することで、他の従業員の経費清算書を作成および管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="c3842-115">Delegate users can also create and manage expense reports for other employees by going to **Expense management** > **My expenses** > **Expense reports** and selecting **Open other user's expenses**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]