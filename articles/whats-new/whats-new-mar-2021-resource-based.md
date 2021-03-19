---
title: 2021 年 3 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: このトピックでは、リソース/非在庫ベースのシナリオ向け Project Operations の 2021 年 3 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500015"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="6dfe3-103">2021 年 3 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="6dfe3-103">What's new March 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="6dfe3-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6dfe3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6dfe3-105">このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:</span><span class="sxs-lookup"><span data-stu-id="6dfe3-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="6dfe3-106">Dataverse 環境バージョン 4.8.0.91 での Project Operations</span><span class="sxs-lookup"><span data-stu-id="6dfe3-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 
- <span data-ttu-id="6dfe3-107">Dynamics 365 Finance 環境バージョン 10.0.16 でのプロジェクト管理および会計</span><span class="sxs-lookup"><span data-stu-id="6dfe3-107">Project management and accounting on Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="6dfe3-108">品質更新プログラム</span><span class="sxs-lookup"><span data-stu-id="6dfe3-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="6dfe3-109">Dataverse の Project Operations</span><span class="sxs-lookup"><span data-stu-id="6dfe3-109">Project Operations on Dataverse</span></span>


| <span data-ttu-id="6dfe3-110">**機能**</span><span class="sxs-lookup"><span data-stu-id="6dfe3-110">**Feature area**</span></span> | <span data-ttu-id="6dfe3-111">**照合番号**</span><span class="sxs-lookup"><span data-stu-id="6dfe3-111">**Reference number**</span></span> | <span data-ttu-id="6dfe3-112">**品質更新プログラム**</span><span class="sxs-lookup"><span data-stu-id="6dfe3-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6dfe3-113">請求および価格設定</span><span class="sxs-lookup"><span data-stu-id="6dfe3-113">Billing and pricing</span></span> | <span data-ttu-id="6dfe3-114">2133873</span><span class="sxs-lookup"><span data-stu-id="6dfe3-114">2133873</span></span> | <span data-ttu-id="6dfe3-115">**経費の見積もり** グリッドの **販売単価** の通貨記号の表示を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-115">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="6dfe3-116">請求および価格設定</span><span class="sxs-lookup"><span data-stu-id="6dfe3-116">Billing and pricing</span></span> | <span data-ttu-id="6dfe3-117">2174616</span><span class="sxs-lookup"><span data-stu-id="6dfe3-117">2174616</span></span> | <span data-ttu-id="6dfe3-118">見積もりが通って成約すると、見積もりからコピーされた契約品目の詳細で契約カスタム価格表が参照されます。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-118">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="6dfe3-119">営業案件管理</span><span class="sxs-lookup"><span data-stu-id="6dfe3-119">Opportunity Management</span></span> | <span data-ttu-id="6dfe3-120">2167475</span><span class="sxs-lookup"><span data-stu-id="6dfe3-120">2167475</span></span> | <span data-ttu-id="6dfe3-121">未請求の実績エントリを作成した修正請求書の税額を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-121">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="6dfe3-122">営業案件管理</span><span class="sxs-lookup"><span data-stu-id="6dfe3-122">Opportunity Management</span></span> | <span data-ttu-id="6dfe3-123">2176285</span><span class="sxs-lookup"><span data-stu-id="6dfe3-123">2176285</span></span> | <span data-ttu-id="6dfe3-124">税額は、売買契約/見積明細行の詳細から原価契約/見積明細行の詳細にコピーしてはいけまｓねん。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-124">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="6dfe3-125">営業案件管理</span><span class="sxs-lookup"><span data-stu-id="6dfe3-125">Opportunity Management</span></span> | <span data-ttu-id="6dfe3-126">2188079</span><span class="sxs-lookup"><span data-stu-id="6dfe3-126">2188079</span></span> | <span data-ttu-id="6dfe3-127">作業ベースでない契約に対しては、分割請求ルールを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-127">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="6dfe3-128">計画と追跡</span><span class="sxs-lookup"><span data-stu-id="6dfe3-128">Planning and Tracking</span></span> | <span data-ttu-id="6dfe3-129">2125274</span><span class="sxs-lookup"><span data-stu-id="6dfe3-129">2125274</span></span> | <span data-ttu-id="6dfe3-130">**プロジェクト開始日のマッピング** の **プロジェクト デュアル書き込みマップ** 属性が、**msdyn\_taskearlieststart** から **msdyn\_actualstart** に更新されました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-130">**Project Dual Write Map** attribute for **Project Start Date Mapping** updated from **msdyn\_taskearlieststart** to **msdyn\_actualstart**.</span></span> |
| <span data-ttu-id="6dfe3-131">計画と追跡</span><span class="sxs-lookup"><span data-stu-id="6dfe3-131">Planning and Tracking</span></span> | <span data-ttu-id="6dfe3-132">2138853</span><span class="sxs-lookup"><span data-stu-id="6dfe3-132">2138853</span></span> | <span data-ttu-id="6dfe3-133">プロジェクト コピー機能が更新され、タスクを参照する経費見積行がコピー先のプロジェクトに確実にコピーされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-133">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="6dfe3-134">計画と追跡</span><span class="sxs-lookup"><span data-stu-id="6dfe3-134">Planning and Tracking</span></span> | <span data-ttu-id="6dfe3-135">2154306</span><span class="sxs-lookup"><span data-stu-id="6dfe3-135">2154306</span></span> | <span data-ttu-id="6dfe3-136">リソースベースのシナリオの Project Operations で経費見積もりを削除する際の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-136">Fixed issues with deleting expense estimates in Project Operations for resource-based scenarios.</span></span> |
| <span data-ttu-id="6dfe3-137">計画と追跡</span><span class="sxs-lookup"><span data-stu-id="6dfe3-137">Planning and Tracking</span></span> | <span data-ttu-id="6dfe3-138">2173259</span><span class="sxs-lookup"><span data-stu-id="6dfe3-138">2173259</span></span> | <span data-ttu-id="6dfe3-139">プロジェクト コピー機能が更新され、特定のシナリオでの **WBS のコピー** エラーメッセージが表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-139">Project copy function updated to ensure it doesn't display **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="6dfe3-140">時間と経費</span><span class="sxs-lookup"><span data-stu-id="6dfe3-140">Time and Expense</span></span> | <span data-ttu-id="6dfe3-141">2148910</span><span class="sxs-lookup"><span data-stu-id="6dfe3-141">2148910</span></span> | <span data-ttu-id="6dfe3-142">**時間入力** グリッドの **エントリの編集** ページの表示に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-142">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="6dfe3-143">時間と経費</span><span class="sxs-lookup"><span data-stu-id="6dfe3-143">Time and Expense</span></span> | <span data-ttu-id="6dfe3-144">2159798</span><span class="sxs-lookup"><span data-stu-id="6dfe3-144">2159798</span></span> | <span data-ttu-id="6dfe3-145">承認された経費エントリを編集できないようにするための管理が厳格化されました。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-145">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a><span data-ttu-id="6dfe3-146">Dynamics 365 Finance のプロジェクト管理および会計</span><span class="sxs-lookup"><span data-stu-id="6dfe3-146">Project management and accounting on Dynamics 365 Finance</span></span>

<span data-ttu-id="6dfe3-147">詳細については、[2021 年 1 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations](whats-new-jan-2021-resource-based.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-147">For more information, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>

## <a name="regulatory-updates"></a><span data-ttu-id="6dfe3-148">規制の更新</span><span class="sxs-lookup"><span data-stu-id="6dfe3-148">Regulatory updates</span></span>

<span data-ttu-id="6dfe3-149">Finance and Operations アプリの規制の更新については、[規制の更新](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-149">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="6dfe3-150">規制の更新について学ぶもう 1 つの方法は、LCS にログインし、問題検索ツールを使用して計画された規制の更新を表示することです。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-150">Another way to learn about regulatory updates is to sign in to LCS and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="6dfe3-151">問題検索では、国、機能の種類、リリースで検索できます。</span><span class="sxs-lookup"><span data-stu-id="6dfe3-151">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
