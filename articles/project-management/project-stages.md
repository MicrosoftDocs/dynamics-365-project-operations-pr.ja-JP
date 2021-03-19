---
title: プロジェクト ステージ
description: このトピックでは、 Microsoft Dynamics プロジェクト オペレーションで利用可能なプロジェクトのステージについて説明します。
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286794"
---
# <a name="project-stages"></a><span data-ttu-id="32154-103">プロジェクト ステージ</span><span class="sxs-lookup"><span data-stu-id="32154-103">Project stages</span></span>

<span data-ttu-id="32154-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="32154-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="32154-105">プロジェクト ステージは、プロジェクトの進み具合の状態を反映するように設計されます。</span><span class="sxs-lookup"><span data-stu-id="32154-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="32154-106">カスタマイズを使用して、ビジネス プロセス フロー、Power Automate、またはプラグイン拡張機能でステージを自動的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="32154-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="32154-107">次のステージは既定のビジネス プロセス フローで定義されています :</span><span class="sxs-lookup"><span data-stu-id="32154-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="32154-108">新しい色</span><span class="sxs-lookup"><span data-stu-id="32154-108">New</span></span>
- <span data-ttu-id="32154-109">見積もり </span><span class="sxs-lookup"><span data-stu-id="32154-109">Quote</span></span>
- <span data-ttu-id="32154-110">プラン</span><span class="sxs-lookup"><span data-stu-id="32154-110">Plan</span></span>
- <span data-ttu-id="32154-111">実行</span><span class="sxs-lookup"><span data-stu-id="32154-111">Deliver</span></span>
- <span data-ttu-id="32154-112">完了</span><span class="sxs-lookup"><span data-stu-id="32154-112">Complete</span></span>
- <span data-ttu-id="32154-113">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="32154-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="32154-114">新しい色</span><span class="sxs-lookup"><span data-stu-id="32154-114">New</span></span>

<span data-ttu-id="32154-115">プロジェクトを作成する場合、プロジェクト ステージは **新規** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="32154-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="32154-116">プロジェクトがテンプレートから作成された場合は、それにはスケジュール、予測、チーム データがある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="32154-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="32154-117">そうでない場合は、プロジェクトの概要であり、残りの構成要素を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32154-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="32154-118">見積もり</span><span class="sxs-lookup"><span data-stu-id="32154-118">Quote</span></span>

<span data-ttu-id="32154-119">プロジェクトを見積もりに関連付けたり、見積もりからプロジェクトを作成する場合、このプロジェクト ステージは **見積もり** に設定され、予想される開始日と終了日も更新されます。</span><span class="sxs-lookup"><span data-stu-id="32154-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="32154-120">プロジェクトが **見積もり** ステージの場合、**プロジェクト エンティティ** ページにある **営業** タブは見積もりの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="32154-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="32154-121">計画</span><span class="sxs-lookup"><span data-stu-id="32154-121">Plan</span></span>

<span data-ttu-id="32154-122">プロジェクトに関連付けられた見積もりが達成された場合、プロジェクトは **契約** フェーズに移動され、プロジェクト ステージは **計画** へと更新されます。</span><span class="sxs-lookup"><span data-stu-id="32154-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="32154-123">プロジェクトが **計画** ステージの場合、**プロジェクト エンティティ** ページは契約の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="32154-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="32154-124">実行</span><span class="sxs-lookup"><span data-stu-id="32154-124">Deliver</span></span>

<span data-ttu-id="32154-125">プロジェクト計画が完了し、プロジェクトを開始する準備ができたら、プロジェクト管理者は、プロジェクト ステージを **実行** へと更新し、プロジェクトが開始したことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="32154-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="32154-126">完了</span><span class="sxs-lookup"><span data-stu-id="32154-126">Complete</span></span> 

<span data-ttu-id="32154-127">プロジェクトの作業が完了したら、プロジェクト管理者はステージを **完了** に更新できます。</span><span class="sxs-lookup"><span data-stu-id="32154-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="32154-128">プロジェクト ステージを **完了** に更新することで、プロジェクト管理者は、作業は 100 パーセント完了しているが、保留中の時間や経費項目が記録できるようにプロジェクトは開いたままになっていることを示します。</span><span class="sxs-lookup"><span data-stu-id="32154-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="32154-129">[閉じる]</span><span class="sxs-lookup"><span data-stu-id="32154-129">Close</span></span>

<span data-ttu-id="32154-130">プロジェクトのすべてのトランザクションが記録されたら、プロジェクト管理者はステージを **閉じる** に更新できます。</span><span class="sxs-lookup"><span data-stu-id="32154-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="32154-131">この時点で、トランザクションの記録はできなくなり、プロジェクトは読み取り専用に設定されます。</span><span class="sxs-lookup"><span data-stu-id="32154-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]