---
title: プロジェクト ステージのタイプ
description: このトピックでは、プロジェクト ステージについて説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008992"
---
# <a name="project-stage-types"></a><span data-ttu-id="75ef0-103">プロジェクト ステージのタイプ</span><span class="sxs-lookup"><span data-stu-id="75ef0-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="75ef0-104">プロジェクト ステージは、プロジェクトの進み具合の状態を反映するように設計されます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="75ef0-105">カスタマイズを使用して、ビジネス プロセス フロー、Power Automate、またはプラグイン拡張機能でステージを自動的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="75ef0-106">次のステージは既定 BPF で定義されています。</span><span class="sxs-lookup"><span data-stu-id="75ef0-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="75ef0-107">新規​​</span><span class="sxs-lookup"><span data-stu-id="75ef0-107">New</span></span>
- <span data-ttu-id="75ef0-108">見積もり</span><span class="sxs-lookup"><span data-stu-id="75ef0-108">Quote</span></span>
- <span data-ttu-id="75ef0-109">計画</span><span class="sxs-lookup"><span data-stu-id="75ef0-109">Plan</span></span>
- <span data-ttu-id="75ef0-110">実行</span><span class="sxs-lookup"><span data-stu-id="75ef0-110">Deliver</span></span>
- <span data-ttu-id="75ef0-111">完了</span><span class="sxs-lookup"><span data-stu-id="75ef0-111">Complete</span></span>
- <span data-ttu-id="75ef0-112">[閉じる]</span><span class="sxs-lookup"><span data-stu-id="75ef0-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="75ef0-113">新規</span><span class="sxs-lookup"><span data-stu-id="75ef0-113">New</span></span>

<span data-ttu-id="75ef0-114">プロジェクトを作成する場合、プロジェクト ステージは **新規** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="75ef0-115">プロジェクトがテンプレートから作成された場合は、それにはスケジュール、予測、チーム データがある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="75ef0-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="75ef0-116">さもなければ、これはプロジェクトの概説であり、残りのコンポーネントを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75ef0-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="75ef0-117">見積もり</span><span class="sxs-lookup"><span data-stu-id="75ef0-117">Quote</span></span>

<span data-ttu-id="75ef0-118">プロジェクトを見積もりに関連付けたり、見積もりからプロジェクトを作成する場合、このプロジェクト ステージは **見積もり** に設定され、予想される開始日と終了日も更新されます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="75ef0-119">プロジェクトが **見積もり** ステージの場合、**プロジェクト エンティティ** ページにある **営業** タブは見積もりの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="75ef0-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="75ef0-120">計画</span><span class="sxs-lookup"><span data-stu-id="75ef0-120">Plan</span></span>

<span data-ttu-id="75ef0-121">プロジェクトに関連付けられた見積もりが達成された場合、プロジェクトは **契約** フェーズに移動され、プロジェクト ステージは **計画** へと更新されます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="75ef0-122">プロジェクトが **計画** ステージの場合、**プロジェクト エンティティ** ページは契約の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="75ef0-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="75ef0-123">実行</span><span class="sxs-lookup"><span data-stu-id="75ef0-123">Deliver</span></span>

<span data-ttu-id="75ef0-124">プロジェクト計画が完了し、プロジェクトを開始する準備ができたら、プロジェクト管理者は、プロジェクト ステージを **実行** へと更新し、プロジェクトが開始したことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="75ef0-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="75ef0-125">完了</span><span class="sxs-lookup"><span data-stu-id="75ef0-125">Complete</span></span> 

<span data-ttu-id="75ef0-126">プロジェクトの作業が完了したら、プロジェクト管理者はステージを **完了** に更新できます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="75ef0-127">プロジェクト ステージを **完了** に更新することで、プロジェクト管理者は、作業は 100 パーセント完了しているが、保留中の時間や経費項目が記録できるようにプロジェクトは開いたままになっていることを示します。</span><span class="sxs-lookup"><span data-stu-id="75ef0-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="75ef0-128">[閉じる]</span><span class="sxs-lookup"><span data-stu-id="75ef0-128">Close</span></span>

<span data-ttu-id="75ef0-129">プロジェクトのすべてのトランザクションが記録されたら、プロジェクト管理者はステージを **閉じる** に更新できます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="75ef0-130">この時点で、トランザクションの記録はできなくなり、プロジェクトは読み取り専用に設定されます。</span><span class="sxs-lookup"><span data-stu-id="75ef0-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]