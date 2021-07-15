---
title: リソース稼働率の概要
description: このトピックでは、Project Operations でのリソース稼働率について説明します。
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367942"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="ef521-103">リソース稼働率の概要</span><span class="sxs-lookup"><span data-stu-id="ef521-103">Resource utilization overview</span></span>

<span data-ttu-id="ef521-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ef521-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ef521-105">リソースは支払請求可能な目標稼働率を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="ef521-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="ef521-106">この目標稼働率は、リソースの既定ロールの属性として定義されるか、個々の予約可能リソースのレコードで設定されます。</span><span class="sxs-lookup"><span data-stu-id="ef521-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="ef521-107">稼働率の計算は、承認された時間エントリを使用してリソースが報告した実際の時間数に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="ef521-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="ef521-108">次の計算式を使用して稼働率を計算します:</span><span class="sxs-lookup"><span data-stu-id="ef521-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="ef521-109">支払請求可能な稼働率 = 課金可能な実際の時間数 ÷ リソース キャパシティ</span><span class="sxs-lookup"><span data-stu-id="ef521-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="ef521-110">支払請求不可能な稼働率 = 請求タイプ ID が支払請求不可能、無料、該当なし/利用不可である実際の時間 ÷ リソース キャパシティ</span><span class="sxs-lookup"><span data-stu-id="ef521-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="ef521-111">内部 = 販売契約なしの実際の時間 ÷ リソース キャパシティ</span><span class="sxs-lookup"><span data-stu-id="ef521-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="ef521-112">リソース キャパシティ = リソース作業時間 – 外出中 – 非勤務日</span><span class="sxs-lookup"><span data-stu-id="ef521-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="ef521-113">**リソース** ウィンドウの **リソース稼働率** ビューがあります。</span><span class="sxs-lookup"><span data-stu-id="ef521-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="ef521-114">グリッド内の各セルは、日、週、または月などの期間でのリソースの支払請求可能な稼働率パーセントを表します。</span><span class="sxs-lookup"><span data-stu-id="ef521-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="ef521-115">セルの色付けには次の計算式が使用されます:</span><span class="sxs-lookup"><span data-stu-id="ef521-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="ef521-116">**緑**: 請求可能稼働率 >= リソース目標稼働率</span><span class="sxs-lookup"><span data-stu-id="ef521-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="ef521-117">**黄**: 目標稼働率 – 20 <= 請求可能稼働率 < 目標稼働率</span><span class="sxs-lookup"><span data-stu-id="ef521-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="ef521-118">**赤**: 請求可能稼働率 < 目標稼働率 – 20</span><span class="sxs-lookup"><span data-stu-id="ef521-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="ef521-119">**リソースの稼働率** ビューはスケジュール ボードに基づいているため、スケジュール ボードのフィルター処理機能を使用して結果をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="ef521-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="ef521-120">グリッドでは、ロールまたは個々のリソースのいずれかで目標稼働率を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef521-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="ef521-121">これを設定するには、**リソース** > **リソース ロール** へと移動します。</span><span class="sxs-lookup"><span data-stu-id="ef521-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="ef521-122">さらに、既定ロールは各予約可能リソースに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef521-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="ef521-123">**リソース** > **リソース** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="ef521-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="ef521-124">**Project Service** タブでは、リソース ロールが定義され、**既定** フィールドが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef521-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="ef521-125">**既定** = **いいえ** の場合には、さらにロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="ef521-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="ef521-126">**既定** = **はい** のロールは、そのロールの目標に対するリソース稼働率を評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef521-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="ef521-127">**Project Service** タブでは、リソースの個々の目標リソース稼働率も設定できます。</span><span class="sxs-lookup"><span data-stu-id="ef521-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="ef521-128">その後、稼働率計算を使って、リソースの既定ロールの目標の代わりに、リソースの目標を評価します。</span><span class="sxs-lookup"><span data-stu-id="ef521-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="ef521-129">稼働率は、グリッドに表示されている期間中に、リソースが承認され、課金対象時間を持っている場合にのみ、リソースに対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef521-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]