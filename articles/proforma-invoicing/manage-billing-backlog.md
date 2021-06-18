---
title: 請求バックログの管理
description: このトピックでは、Project Operations で請求バックログを表示および操作する方法について説明します。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7c242937cd9dd277f8d92b7a29333c1fa272e5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011917"
---
# <a name="manage-billing-backlog"></a><span data-ttu-id="c0396-103">請求バックログの管理</span><span class="sxs-lookup"><span data-stu-id="c0396-103">Manage billing backlog</span></span>

<span data-ttu-id="c0396-104">_ **適用対象:** リソース/非在庫ベースのシナリオの Project Operations</span><span class="sxs-lookup"><span data-stu-id="c0396-104">_ **Applies To:** Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="c0396-105">Dynamics 365 Project Operations には、請求のバックログの管理に役立つ専用ビューがあります。</span><span class="sxs-lookup"><span data-stu-id="c0396-105">Dynamics 365 Project Operations has dedicated views to help manage the billing backlog.</span></span> <span data-ttu-id="c0396-106">請求バックログを管理するには、**請求** 配下の **営業** エリアを選択します。</span><span class="sxs-lookup"><span data-stu-id="c0396-106">To manage the billing backlog, select the links in the **Sales** area, under **Billing**.</span></span> 

<span data-ttu-id="c0396-107">次のビューを使用できます :</span><span class="sxs-lookup"><span data-stu-id="c0396-107">The following views available:</span></span>

- <span data-ttu-id="c0396-108">着手金と前払金</span><span class="sxs-lookup"><span data-stu-id="c0396-108">Retainers and Advances</span></span>
- <span data-ttu-id="c0396-109">使用可能な前払金と着手金</span><span class="sxs-lookup"><span data-stu-id="c0396-109">Available Retainers and Advances</span></span>
- <span data-ttu-id="c0396-110">固定価格マイルストーン</span><span class="sxs-lookup"><span data-stu-id="c0396-110">Fixed Price Milestones</span></span>
- <span data-ttu-id="c0396-111">時間と材料の請求バックログ</span><span class="sxs-lookup"><span data-stu-id="c0396-111">Time and Material Billing Backlog</span></span>

## <a name="retainers-and-advances"></a><span data-ttu-id="c0396-112">着手金と前払金</span><span class="sxs-lookup"><span data-stu-id="c0396-112">Retainers and Advances</span></span>

<span data-ttu-id="c0396-113">**着手金と前払金** ビューには、すべてのプロジェクト契約の着手金と前払金が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-113">The **Retainers and Advances** view lists the retainers and advances across all project contracts.</span></span> <span data-ttu-id="c0396-114">留保金または立替金が請求された後、立替金の金額が利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c0396-114">After a retainer or advance is invoiced, the amount of the advance becomes available to use.</span></span>

## <a name="available-retainers-and-advances"></a><span data-ttu-id="c0396-115">使用可能な前払金と着手金</span><span class="sxs-lookup"><span data-stu-id="c0396-115">Available Retainers and Advances</span></span>

<span data-ttu-id="c0396-116">**使用可能な着手金と前払金** ビューには、すべてのプロジェクト契約の使用可能な着手金と前払金が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-116">The **Available Retainers and Advances** view lists all available retainers and advances across all project contracts.</span></span> <span data-ttu-id="c0396-117">留保金または立替金が請求された後、立替金の金額が利用できるようになり、リストに追加されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-117">After a retainer or advance is invoiced, the amount of the advance becomes available to use and is added to the list.</span></span> <span data-ttu-id="c0396-118">着手金または前払金の金額をすべて使用すると、一覧から削除されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-118">After the amount of the retainer or advance is used completely, it's removed from the list.</span></span>

## <a name="fixed-price-milestones"></a><span data-ttu-id="c0396-119">固定価格マイルストーン</span><span class="sxs-lookup"><span data-stu-id="c0396-119">Fixed Price Milestones</span></span>

<span data-ttu-id="c0396-120">**固定価格マイルストーン** ビューには、すべてのプロジェクト契約品目の固定価格のマイルストーンが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-120">The **Fixed Price Milestones** view lists all fixed price milestones across all project contract lines.</span></span> <span data-ttu-id="c0396-121">このビューでは、単一つまたは複数のマイルストーンを **請求準備完了** または **請求準備未完了** としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="c0396-121">From this view, single or multiple milestones can be marked as **Ready to invoice** or **Not ready to invoice**.</span></span> <span data-ttu-id="c0396-122">マイルストーンを **請求準備完了** としてマークすると、ドラフトの請求書に記載できます。</span><span class="sxs-lookup"><span data-stu-id="c0396-122">Marking a milestone as **Ready to invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="c0396-123">複数顧客の契約品目に固定価格の請求方法がある場合、契約品目上の顧客ごとにマイルストーンが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-123">When multi-customer contract lines have a fixed price billing method, a milestone is created for each customer on the contract line.</span></span> <span data-ttu-id="c0396-124">マイルストーンを作成し、顧客ごとのマイルストーン レコードに分割することができます。</span><span class="sxs-lookup"><span data-stu-id="c0396-124">A milestone can be created and then split into individual customer-specific milestone records.</span></span> <span data-ttu-id="c0396-125">この分割は内部的なものであり、契約品目の各顧客に対して定義された請求割合の分割に準拠します。</span><span class="sxs-lookup"><span data-stu-id="c0396-125">This split is internal and in accordance with the billing percentage split defined for each customer on the contract line.</span></span> <span data-ttu-id="c0396-126">**固定価格のマイルストーン** ビューでは、個々の顧客固有のマイルストーン レコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-126">In the **Fixed Price Milestones** view, you will see the individual customer-specific milestone records.</span></span> <span data-ttu-id="c0396-127">これらのマイルストーン レコードはそれぞれ、このビューとは別に **請求準備完了** としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="c0396-127">Each of these milestone records can be marked as **Ready to Invoice** separately from this view.</span></span> <span data-ttu-id="c0396-128">関連するマイルストーン分割の 1 つ以上が **請求準備完了** とマークされている場合、ヘッダー ステータスが **開始前** から **進行中** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-128">When one or more of the related milestone splits are marked as **Ready to Invoice**, the header status updates to **In Progress** from **Not Started**.</span></span> <span data-ttu-id="c0396-129">すべてのマイルストーン分割が請求されると、ヘッダー マイルストーン ステータスは **完了** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-129">When all of the milestone splits are invoiced, the header milestone status updates to **Completed**.</span></span>

<span data-ttu-id="c0396-130">下書き請求書のマイルストーンが、このビューに **顧客請求書作成済み** という請求の状態で表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-130">A milestone on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="c0396-131">請求書のドラフトが確認されると、レコード上の請求状況が **顧客請求書転記済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-131">When the draft invoice is confirmed, the billing status on the record is updated to **Customer Invoice Posted**.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c0396-132">カスタム コードを使用してこのステータス値を更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="c0396-132">Do not update this status value by using custom code.</span></span> <span data-ttu-id="c0396-133">これらの状態コードがカスタム コードで更新されると、Project Operations は正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="c0396-133">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>

## <a name="time-and-material-billing-backlog"></a><span data-ttu-id="c0396-134">時間と材料の請求バックログ</span><span class="sxs-lookup"><span data-stu-id="c0396-134">Time and Material Billing Backlog</span></span>

<span data-ttu-id="c0396-135">**時間と材料の請求バックログ** ビューには、システム内のすべてのプロジェクト契約のうち、請求書が発行されていないすべての未請求売上実績を表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-135">The **Time and Material Billing Backlog** view lists all unbilled sales actuals across all project contracts in the system that haven't been invoiced.</span></span> <span data-ttu-id="c0396-136">1 つまたは複数の未請求売上金額は、このビューから **請求準備完了** または **請求準備未完了** としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="c0396-136">Single or multiple unbilled sales actuals can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="c0396-137">未請求売上金額を **請求準備完了** とマークすると、下書き請求書に記載できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c0396-137">Marking an unbilled sales actual as **Ready to Invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="c0396-138">**上限** の状態が **失敗** となっている未請求の売上実績は、**請求準備完了** としてマークすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c0396-138">Unbilled sales actuals with a **Not-to-Exceed** status of **Failed** can't be marked as **Ready to Invoice**.</span></span> <span data-ttu-id="c0396-139">実績を **請求準備完了** とマークする必要がある場合、コミットされた契約品目上の他の実績のステータスをリセットしてから、**上限** ステータスを再評価します。</span><span class="sxs-lookup"><span data-stu-id="c0396-139">If the actuals need to be marked as **Ready to Invoice**, reset the status on other actuals on the contract line that are committed, and then re-evaluate the **Not-to-Exceed** status.</span></span>

<span data-ttu-id="c0396-140">複数顧客の契約品目に時間と材料の請求方法がある場合、時間と費用が承認されると、契約品目上の顧客ごとに定義された請求割合の分割に従って、契約品目上の顧客ごとに 1 つの未請求の売上実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-140">If multi-customer contract lines have a time and material billing method, when time and expenses are approved, one unbilled sales actual is created for each customer on the contract line according to the billing percentage split defined for each of the customers.</span></span> <span data-ttu-id="c0396-141">**時間と材料の請求バックログ** ビューでは、これらの個々の顧客固有の未請求の販売実績が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-141">In the **Time and Material Billing Backlog** view, you will see these individual customer-specific unbilled sales actuals.</span></span> <span data-ttu-id="c0396-142">これらの未請求売上金額はそれぞれ、このビューとは別に **請求準備完了** としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="c0396-142">Each of these unbilled sales actual records can be marked as **Ready to Invoice** separately from this view.</span></span>

<span data-ttu-id="c0396-143">ドラフトの請求書に記載されている未請求の売上実績は、請求の状態が **顧客請求書作成済み** の場合にこのビューで表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-143">An unbilled sales actual that's on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="c0396-144">ドラフトの請求書を確定すると、このレコードの請求の状態は **顧客請求書転記済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c0396-144">When the draft invoice is confirmed, the billing status on this record is updated to **Customer Invoice Posted**.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c0396-145">カスタム コードを使用してこのステータス値を更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="c0396-145">Do not update this status value by using custom code.</span></span> <span data-ttu-id="c0396-146">これらの状態コードがカスタム コードで更新されると、Project Operations は正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="c0396-146">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
