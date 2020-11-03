---
title: 経費の委任を管理する
description: 経費の代理ユーザーは、組織内で別の従業員に代わって経費精算書を作成および管理できます。
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
ms.openlocfilehash: 2ce1d1cf35745ef4372258e07fd4d2b108ed4827
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079420"
---
# <a name="manage-expense-delegation"></a><span data-ttu-id="eacfa-103">経費の委任を管理する</span><span class="sxs-lookup"><span data-stu-id="eacfa-103">Manage expense delegation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eacfa-104">経費の代理ユーザーは、組織内で別の従業員に代わって経費精算書を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="eacfa-104">An expense delegate user can create and manage expense reports on behalf of another employee in the organization.</span></span>

## <a name="configuring-expense-delegation"></a><span data-ttu-id="eacfa-105">経費委任の構成</span><span class="sxs-lookup"><span data-stu-id="eacfa-105">Configuring expense delegation</span></span>

<span data-ttu-id="eacfa-106">ユーザーを経費の代理人として設定するには、 **経費管理 > 設定 > 全般 > 代理人** に移動し、 **代理人** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="eacfa-106">To set up a user as an expense delegate, go to **Expense management > Setup > General > Delegates** to open the **Delegates** page.</span></span> <span data-ttu-id="eacfa-107">**新規** を選択してから、代理人を定義する従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="eacfa-107">Select **New** and then select the employee that will have a delegate defined.</span></span> <span data-ttu-id="eacfa-108">代理ユーザーのエイリアス、委任期間の開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="eacfa-108">Enter the alias of the delegate user and the start and end date for the delegation period.</span></span>

## <a name="managing-expense-delegation-on-behalf-of-another-employee"></a><span data-ttu-id="eacfa-109">他の従業員に代わって経費の委任を管理する</span><span class="sxs-lookup"><span data-stu-id="eacfa-109">Managing expense delegation on behalf of another employee</span></span>

<span data-ttu-id="eacfa-110">機能管理キー **経費の委任一覧ページを有効にする** が有効になっている場合、 **経費管理 > 自分の経費 > 自分へ委任された経費** の順に移動すると、 **自分へ委任された経費** の一覧ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eacfa-110">If the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available by navigating to **Expense management > My expenses > Expenses delegated to me**.</span></span>

<span data-ttu-id="eacfa-111">代理ユーザーは、ユーザーに委任された既存の経費精算書をすばやくフィルター処理および検索できます。</span><span class="sxs-lookup"><span data-stu-id="eacfa-111">A delegate user can quickly filter and search on existing expense reports that hae been delegated to the user.</span></span> <span data-ttu-id="eacfa-112">ユーザーは、 **新規経費精算書** をクリックすると、他のユーザーに代わって新規経費精算書をすばやく作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="eacfa-112">The user can also quickly create a new expense report on behalf of other users by clicking **New expense report**.</span></span>

<span data-ttu-id="eacfa-113">代理ユーザーは、 **経費管理 > 自分の経費 > 経費精算書** の順に移動して、 **他のユーザーの経費を開く** ボタンをクリックして、他の従業員に代わって経費精算書を作成および管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="eacfa-113">Delegate users can also create and manage expense reports on behalf of other employees by navigating to **Expense management > My expenses > Expense reports** and clicking the **Open other user's expenses** button.</span></span>
