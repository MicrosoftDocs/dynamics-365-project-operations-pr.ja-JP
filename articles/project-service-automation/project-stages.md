---
title: プロジェクト ステージ
description: このトピックでは、プロジェクト ステージについて説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752830"
---
# <a name="project-stages"></a><span data-ttu-id="1fae7-103">プロジェクト ステージ</span><span class="sxs-lookup"><span data-stu-id="1fae7-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1fae7-104">プロジェクト ステージが更新されると、 プロジェクトの進捗状態が反映されます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="1fae7-105">既定の業務プロセス フローでは、一部のプロジェクトのステージは自動的に更新されますが、その他についてはプロジェクト マネージャーが手動で更新を行います。</span><span class="sxs-lookup"><span data-stu-id="1fae7-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="1fae7-106">次のステージは既定 BPF で定義されています。</span><span class="sxs-lookup"><span data-stu-id="1fae7-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="1fae7-107">新規</span><span class="sxs-lookup"><span data-stu-id="1fae7-107">New</span></span>
- <span data-ttu-id="1fae7-108">見積もり</span><span class="sxs-lookup"><span data-stu-id="1fae7-108">Quote</span></span>
- <span data-ttu-id="1fae7-109">計画</span><span class="sxs-lookup"><span data-stu-id="1fae7-109">Plan</span></span>
- <span data-ttu-id="1fae7-110">実行</span><span class="sxs-lookup"><span data-stu-id="1fae7-110">Deliver</span></span>
- <span data-ttu-id="1fae7-111">完了</span><span class="sxs-lookup"><span data-stu-id="1fae7-111">Complete</span></span>
- <span data-ttu-id="1fae7-112">[閉じる]</span><span class="sxs-lookup"><span data-stu-id="1fae7-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="1fae7-113">新規</span><span class="sxs-lookup"><span data-stu-id="1fae7-113">New</span></span>

<span data-ttu-id="1fae7-114">プロジェクトを作成する場合、プロジェクト ステージは**新規**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="1fae7-115">プロジェクトがテンプレートから作成された場合は、それにはスケジュール、予測、チーム データがある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1fae7-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="1fae7-116">さもなければ、これはプロジェクトの概説であり、残りのコンポーネントを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fae7-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="1fae7-117">見積もり</span><span class="sxs-lookup"><span data-stu-id="1fae7-117">Quote</span></span>

<span data-ttu-id="1fae7-118">プロジェクトを見積もりに関連付けたり、見積もりからプロジェクトを作成する場合、このプロジェクト ステージは**見積もり**に設定され、予想される開始日と終了日も更新されます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="1fae7-119">プロジェクトが**見積もり**ステージの場合、**プロジェクト エンティティ**ページにある**営業**タブは見積もりの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="1fae7-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="1fae7-120">計画</span><span class="sxs-lookup"><span data-stu-id="1fae7-120">Plan</span></span>

<span data-ttu-id="1fae7-121">プロジェクトに関連付けられた見積もりが達成された場合、プロジェクトは**契約**フェーズに移動され、プロジェクト ステージは**計画**へと更新されます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="1fae7-122">プロジェクトが**計画**ステージの場合、**プロジェクト エンティティ**ページは契約の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="1fae7-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="1fae7-123">実行</span><span class="sxs-lookup"><span data-stu-id="1fae7-123">Deliver</span></span>

<span data-ttu-id="1fae7-124">プロジェクト計画が完了し、プロジェクトを開始する準備ができたら、プロジェクト管理者は、プロジェクト ステージを**実行**へと更新し、プロジェクトが開始したことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fae7-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="1fae7-125">完了</span><span class="sxs-lookup"><span data-stu-id="1fae7-125">Complete</span></span> 

<span data-ttu-id="1fae7-126">プロジェクトの作業が完了したら、プロジェクト管理者はステージを**完了**に更新できます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="1fae7-127">プロジェクト ステージを**完了**に更新することで、プロジェクト管理者は、作業は 100 パーセント完了しているが、保留中の時間や経費項目が記録できるようにプロジェクトは開いたままになっていることを示します。</span><span class="sxs-lookup"><span data-stu-id="1fae7-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="1fae7-128">[閉じる]</span><span class="sxs-lookup"><span data-stu-id="1fae7-128">Close</span></span>

<span data-ttu-id="1fae7-129">プロジェクトのすべてのトランザクションが記録されたら、プロジェクト管理者はステージを**閉じる**に更新できます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="1fae7-130">この時点で、トランザクションの記録はできなくなり、プロジェクトは読み取り専用に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1fae7-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
