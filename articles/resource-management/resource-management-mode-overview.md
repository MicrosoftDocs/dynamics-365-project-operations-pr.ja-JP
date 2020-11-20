---
title: リソース管理モードの概要
description: このトピックは、Dynamics 365 Project Operations でのリソース管理機能に関する情報を提供します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118524"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="5343a-103">リソース管理モードの概要</span><span class="sxs-lookup"><span data-stu-id="5343a-103">Resource management modes overview</span></span>

<span data-ttu-id="5343a-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="5343a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5343a-105">Dynamics 365 Project Operations は、予約フロー全体を実行するために 2 つのモードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5343a-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="5343a-106">管理モードはプロジェクト パラメータとして定義されており、ビジネス ニーズが変更する場合は修正可能です。</span><span class="sxs-lookup"><span data-stu-id="5343a-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="5343a-107">セントラル モード</span><span class="sxs-lookup"><span data-stu-id="5343a-107">Central mode</span></span>
<span data-ttu-id="5343a-108">プロジェクトへのリソースの割り当てを一元管理する組織の場合、セントラル モードは、プロジェクト マネージャーがプロジェクト レベルでリソース要件を定義できるようにする方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="5343a-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="5343a-109">リソース要件の履行は、リソース マネージャーに委任されます。</span><span class="sxs-lookup"><span data-stu-id="5343a-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="5343a-110">プロジェクト マネージャーは、リソース マネージャーによって提案されたリソースを承認または拒否できます。</span><span class="sxs-lookup"><span data-stu-id="5343a-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![セントラル モード](./media/resource-management-central.png)

<span data-ttu-id="5343a-112">セントラル モードでリソースを管理するには、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5343a-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="5343a-113">予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する</span><span class="sxs-lookup"><span data-stu-id="5343a-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="5343a-114">リソース要件から名前付きリソースを予約する</span><span class="sxs-lookup"><span data-stu-id="5343a-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="5343a-115">リソース要求の送信</span><span class="sxs-lookup"><span data-stu-id="5343a-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="5343a-116">リソース要求を実行</span><span class="sxs-lookup"><span data-stu-id="5343a-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="5343a-117">リソース要求から提案されたプロジェクト リソースの承諾または拒否</span><span class="sxs-lookup"><span data-stu-id="5343a-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="5343a-118">ハイブリッド モード</span><span class="sxs-lookup"><span data-stu-id="5343a-118">Hybrid mode</span></span>
<span data-ttu-id="5343a-119">リソースの割り当てに柔軟性が必要な組織の場合、ハイブリッド モードでは、プロジェクト マネージャーとリソース マネージャーの両方がリソースを予約できます。</span><span class="sxs-lookup"><span data-stu-id="5343a-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![ハイブリッド モード](./media/resource-management-hybrid.png)

<span data-ttu-id="5343a-121">サポートされているセントラル モード プロセスに加えて、ハイブリッド モードでサポートされている他のすべての予約フローを管理するには、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5343a-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="5343a-122">プロジェクトにリソースを直接予約する:</span><span class="sxs-lookup"><span data-stu-id="5343a-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="5343a-123">名前付き予約可能リソースをプロジェクト チームに予約して、タスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="5343a-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="5343a-124">リソース要件からリソースを予約する:</span><span class="sxs-lookup"><span data-stu-id="5343a-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="5343a-125">予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する</span><span class="sxs-lookup"><span data-stu-id="5343a-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="5343a-126">リソース要件から名前付きリソースを予約する</span><span class="sxs-lookup"><span data-stu-id="5343a-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
