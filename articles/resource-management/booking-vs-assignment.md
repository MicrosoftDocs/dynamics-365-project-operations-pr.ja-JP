---
title: 予約と割り当て
description: このトピックでは、リソースの予約とリソースの割り当ての違いについて説明します。
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841178"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="5edd1-103">予約と割り当て</span><span class="sxs-lookup"><span data-stu-id="5edd1-103">Bookings vs assignments</span></span>

<span data-ttu-id="5edd1-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="5edd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5edd1-105">予約は、プロジェクトに対するリソースの本配賦または仮配賦です。</span><span class="sxs-lookup"><span data-stu-id="5edd1-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="5edd1-106">本予約は、リソースの能力を消費します。</span><span class="sxs-lookup"><span data-stu-id="5edd1-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="5edd1-107">予約はチームの組織的な概念を表し、リソースがさまざまなプロジェクトにまたがってどのように関与するのか理解できます。</span><span class="sxs-lookup"><span data-stu-id="5edd1-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="5edd1-108">Dynamics 365 Project Operations は、予約をプロジェクト レベルの概念として扱います。</span><span class="sxs-lookup"><span data-stu-id="5edd1-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="5edd1-109">割り当ては予約と異なり、プロジェクト スケジュールのプロジェクト タスクに対してリソースを確保することです。</span><span class="sxs-lookup"><span data-stu-id="5edd1-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="5edd1-110">リソースには名前を付けることも、汎用なものにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5edd1-110">The resources can be named or generic.</span></span>  <span data-ttu-id="5edd1-111">リソース要件がプロジェクト タスクの割り当てから導き出される場合、Project Operations は、リソース割り当ての工数コントーを使用して、リソース要件の詳細のコントーを作成します。</span><span class="sxs-lookup"><span data-stu-id="5edd1-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="5edd1-112">ただし、リソース割り当てへの参照は維持されません。</span><span class="sxs-lookup"><span data-stu-id="5edd1-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="5edd1-113">リソース要件から導き出された予約を更新しても、リソース割り当ては更新されません。</span><span class="sxs-lookup"><span data-stu-id="5edd1-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="5edd1-114">通常、予約されたリソースの合計は、1 つまたは複数のタスクへのリソースの割り当ての合計と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="5edd1-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="5edd1-115">ただし、 Project Operations ではこの一致を強制しません。</span><span class="sxs-lookup"><span data-stu-id="5edd1-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="5edd1-116">**調整** ビューでは、リソースの予約と割り当てが一致しない箇所をプロジェクト マネージャに表示します。</span><span class="sxs-lookup"><span data-stu-id="5edd1-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


