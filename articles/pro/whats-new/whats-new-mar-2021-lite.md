---
title: 2021 年 3 月の新機能 - Project Operations のライト展開
description: このトピックでは、Project Operations のライト展開の 2021 年 3 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500014"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="25c9b-103">2021 年 3 月の新機能 - Project Operations のライト展開</span><span class="sxs-lookup"><span data-stu-id="25c9b-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="25c9b-104">_適用対象: ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="25c9b-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="25c9b-105">このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:</span><span class="sxs-lookup"><span data-stu-id="25c9b-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="25c9b-106">Dataverse 環境バージョン 4.8.0.91 での Project Operations</span><span class="sxs-lookup"><span data-stu-id="25c9b-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="25c9b-107">品質更新プログラム</span><span class="sxs-lookup"><span data-stu-id="25c9b-107">Quality updates</span></span>

| <span data-ttu-id="25c9b-108">**機能**</span><span class="sxs-lookup"><span data-stu-id="25c9b-108">**Feature area**</span></span> | <span data-ttu-id="25c9b-109">**照合番号**</span><span class="sxs-lookup"><span data-stu-id="25c9b-109">**Reference number**</span></span> | <span data-ttu-id="25c9b-110">**品質更新プログラム**</span><span class="sxs-lookup"><span data-stu-id="25c9b-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="25c9b-111">請求および価格設定</span><span class="sxs-lookup"><span data-stu-id="25c9b-111">Billing and pricing</span></span> | <span data-ttu-id="25c9b-112">2133873</span><span class="sxs-lookup"><span data-stu-id="25c9b-112">2133873</span></span> | <span data-ttu-id="25c9b-113">**経費の見積もり** グリッドの **販売単価** の通貨記号の表示を修正しました。</span><span class="sxs-lookup"><span data-stu-id="25c9b-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="25c9b-114">請求および価格設定</span><span class="sxs-lookup"><span data-stu-id="25c9b-114">Billing and pricing</span></span> | <span data-ttu-id="25c9b-115">2174616</span><span class="sxs-lookup"><span data-stu-id="25c9b-115">2174616</span></span> | <span data-ttu-id="25c9b-116">見積もりが通って成約すると、見積もりからコピーされた契約品目の詳細で契約カスタム価格表が参照されます。</span><span class="sxs-lookup"><span data-stu-id="25c9b-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="25c9b-117">営業案件管理</span><span class="sxs-lookup"><span data-stu-id="25c9b-117">Opportunity Management</span></span> | <span data-ttu-id="25c9b-118">2167475</span><span class="sxs-lookup"><span data-stu-id="25c9b-118">2167475</span></span> | <span data-ttu-id="25c9b-119">未請求の実績エントリを作成した修正請求書の税額を修正しました。</span><span class="sxs-lookup"><span data-stu-id="25c9b-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="25c9b-120">営業案件管理</span><span class="sxs-lookup"><span data-stu-id="25c9b-120">Opportunity Management</span></span> | <span data-ttu-id="25c9b-121">2176285</span><span class="sxs-lookup"><span data-stu-id="25c9b-121">2176285</span></span> | <span data-ttu-id="25c9b-122">税額は、売買契約/見積明細行の詳細から原価契約/見積明細行の詳細にコピーしてはいけまｓねん。</span><span class="sxs-lookup"><span data-stu-id="25c9b-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="25c9b-123">営業案件管理</span><span class="sxs-lookup"><span data-stu-id="25c9b-123">Opportunity Management</span></span> | <span data-ttu-id="25c9b-124">2188079</span><span class="sxs-lookup"><span data-stu-id="25c9b-124">2188079</span></span> | <span data-ttu-id="25c9b-125">作業ベースでない契約に対しては、分割請求ルールを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="25c9b-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="25c9b-126">計画と追跡</span><span class="sxs-lookup"><span data-stu-id="25c9b-126">Planning and Tracking</span></span> | <span data-ttu-id="25c9b-127">2138853</span><span class="sxs-lookup"><span data-stu-id="25c9b-127">2138853</span></span> | <span data-ttu-id="25c9b-128">プロジェクト コピー機能が更新され、タスクを参照する経費見積行がコピー先のプロジェクトに確実にコピーされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="25c9b-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="25c9b-129">計画と追跡</span><span class="sxs-lookup"><span data-stu-id="25c9b-129">Planning and Tracking</span></span> | <span data-ttu-id="25c9b-130">2173259</span><span class="sxs-lookup"><span data-stu-id="25c9b-130">2173259</span></span> | <span data-ttu-id="25c9b-131">プロジェクト コピー機能が更新され、特定のシナリオでの **WBS のコピー** エラーメッセージが表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="25c9b-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="25c9b-132">時間と経費</span><span class="sxs-lookup"><span data-stu-id="25c9b-132">Time and Expense</span></span> | <span data-ttu-id="25c9b-133">2148910</span><span class="sxs-lookup"><span data-stu-id="25c9b-133">2148910</span></span> | <span data-ttu-id="25c9b-134">**時間入力** グリッドの **エントリの編集** ページの表示に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="25c9b-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="25c9b-135">時間と経費</span><span class="sxs-lookup"><span data-stu-id="25c9b-135">Time and Expense</span></span> | <span data-ttu-id="25c9b-136">2159798</span><span class="sxs-lookup"><span data-stu-id="25c9b-136">2159798</span></span> | <span data-ttu-id="25c9b-137">承認された経費エントリを編集できないようにするための管理が厳格化されました。</span><span class="sxs-lookup"><span data-stu-id="25c9b-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


