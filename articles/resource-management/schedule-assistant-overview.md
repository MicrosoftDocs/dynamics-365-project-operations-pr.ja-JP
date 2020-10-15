---
title: スケジュール アシスタントの概要
description: このトピックは、スケジュール アシスタントを使用してリソースを予約する方法を説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908288"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="70826-103">スケジュール アシスタントの概要</span><span class="sxs-lookup"><span data-stu-id="70826-103">Schedule assistant overview</span></span>

<span data-ttu-id="70826-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="70826-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70826-105">スケジュール アシスタントは、プロジェクト管理者によって定義された要件に基づいてリソースを予約するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="70826-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="70826-106">スケジュール アシスタントは、リソース要件で提供されるパラメーターに依存してリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="70826-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="70826-107">スケジュール アシスタントは、時間枠や必要なスキルなど、関連する要件に一致するリソースを推奨します。</span><span class="sxs-lookup"><span data-stu-id="70826-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="70826-108">適切なリソースが特定されたら、リソース管理者またはプロジェクト管理者はリソースを作業に予約できます。</span><span class="sxs-lookup"><span data-stu-id="70826-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="70826-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="70826-109">Prerequisites</span></span>

<span data-ttu-id="70826-110">スケジュール アシスタントは Universal Resource Scheduling ソリューションの一部です。</span><span class="sxs-lookup"><span data-stu-id="70826-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="70826-111">このソリューションは、Dynamics 365 Project Operations、Dynamics 365 Field Service、および Dynamics 365 Customer Service に含まれ、インストールされています。</span><span class="sxs-lookup"><span data-stu-id="70826-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="70826-112">要件とリソースの一致</span><span class="sxs-lookup"><span data-stu-id="70826-112">Matching requirements and resources</span></span>

<span data-ttu-id="70826-113">生成されたリソース要件は、次のような詳細に基づいています。</span><span class="sxs-lookup"><span data-stu-id="70826-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="70826-114">特性</span><span class="sxs-lookup"><span data-stu-id="70826-114">Characteristics</span></span>
-   <span data-ttu-id="70826-115">役割</span><span class="sxs-lookup"><span data-stu-id="70826-115">Roles</span></span>
-   <span data-ttu-id="70826-116">部署</span><span class="sxs-lookup"><span data-stu-id="70826-116">Business units</span></span>
-   <span data-ttu-id="70826-117">リソースの基本設定</span><span class="sxs-lookup"><span data-stu-id="70826-117">Resource preferences</span></span>
-   <span data-ttu-id="70826-118">工数コントー</span><span class="sxs-lookup"><span data-stu-id="70826-118">Effort contours</span></span>
-   <span data-ttu-id="70826-119">タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="70826-119">Time zone</span></span>

<span data-ttu-id="70826-120">スケジュール アシスタントは、これらの詳細を使用してリソースをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="70826-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="70826-121">スケジュール アシスタントを起動します</span><span class="sxs-lookup"><span data-stu-id="70826-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="70826-122">スケジュール アシスタントを起動する方法は 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="70826-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="70826-123">ハイブリッド モードを使用している場合、チーム メンバー グリッドで、未対応のリソース要件がチーム メンバーを選択してから、**予約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="70826-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="70826-124">セントラル モードを使用している場合、リソース管理者はリソースを検索および選択します。</span><span class="sxs-lookup"><span data-stu-id="70826-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="70826-125">スケジュール アシスタント フィルター</span><span class="sxs-lookup"><span data-stu-id="70826-125">Schedule assistant filters</span></span>

<span data-ttu-id="70826-126">スケジュール アシスタントの実行後、リソース要件の詳細が左側のウィンドウにフィルター処理された値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="70826-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="70826-127">リソース管理者またはプロジェクト管理者は、スケジュールのニーズに合わせてフィルターを調整することにより、結果を微調整できます。</span><span class="sxs-lookup"><span data-stu-id="70826-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="70826-128">フィルター ウィンドウには、次のような作業関連のオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="70826-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="70826-129">作業の開始と終了</span><span class="sxs-lookup"><span data-stu-id="70826-129">Work start and end</span></span>
-   <span data-ttu-id="70826-130">特性</span><span class="sxs-lookup"><span data-stu-id="70826-130">Characteristics</span></span>
-   <span data-ttu-id="70826-131">役割</span><span class="sxs-lookup"><span data-stu-id="70826-131">Roles</span></span>
-   <span data-ttu-id="70826-132">組織単位</span><span class="sxs-lookup"><span data-stu-id="70826-132">Organizational units</span></span>
-   <span data-ttu-id="70826-133">リソース会社</span><span class="sxs-lookup"><span data-stu-id="70826-133">Resourcing company</span></span>
-   <span data-ttu-id="70826-134">リソースの種類</span><span class="sxs-lookup"><span data-stu-id="70826-134">Resource types</span></span>
-   <span data-ttu-id="70826-135">優先するリソース</span><span class="sxs-lookup"><span data-stu-id="70826-135">Preferred resources</span></span>
