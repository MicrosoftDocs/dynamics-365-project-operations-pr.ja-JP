---
title: 仮予約の要件
description: このトピックでは、仮予約の要件について説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997922"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="aa1fb-103">仮予約の要件</span><span class="sxs-lookup"><span data-stu-id="aa1fb-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="aa1fb-104">リソース要件は本予約できます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="aa1fb-105">本予約では、リソースの容量を使用する提案を作成できます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="aa1fb-106">提案が承認のために要求者に返されます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="aa1fb-107">仮予約でプロジェクト チームに一時的にリソースが追加され、スケジュール ボードに別の状態が示されますが、リソースの容量は消費されません。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="aa1fb-108">スケジュール ボードの仮予約リソースに対して、**予約の状態** フィールドを **仮予約** に設定します。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![ [仮予約] に設定された予約の状態](media/Resource-Management-image77.png)

<span data-ttu-id="aa1fb-110">**チーム** タブが **名前付きチーム メンバー** ビューにある場合は、リソースは常にそこに表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="aa1fb-111">仮予約された時間は **仮予約時間** 列に報告されます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![[名前付きチーム メンバー] ビューの仮予約時間](media/Resource-Management-image78.png)

<span data-ttu-id="aa1fb-113">仮予約済みのチーム メンバーはタスクに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-113">Soft-booked team members can be assigned to tasks.</span></span>

![タスクに割り当てられた仮予約済みのチーム メンバー](media/Resource-Management-image79.png)

<span data-ttu-id="aa1fb-115">**調整** タブについて、**調整** タブは本予約のみを対象とするため、仮予約リソースについては表示されません。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![調整タブの、仮予約済みで予約なしのリソース](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="aa1fb-117">汎用チーム メンバーから生成される要件内のリソースは仮予約できません。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="aa1fb-118">スケジュール ボードで、別のカラリングは、リソースの仮予約のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![スケジュール ボードで仮予約](media/Resource-Management-image81.png)

<span data-ttu-id="aa1fb-120">仮予約を本予約に変換するには、スケジュール ボードで [仮予約] を右クリックし、**状態を変更する**\> **本予約**\>**本予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![予約の状態を [本予約] に変更する](media/Resource-Management-image82.png)

<span data-ttu-id="aa1fb-122">予約が変更され、状態はスケジュール ボードで変更されます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="aa1fb-123">現在の予約の状態が **本予約** である場合は、リソースが予約済みであることを示しています。また、容量と可用性が調整されます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="aa1fb-124">スケジュール ボードから本予約または仮予約を取り消す場合、同じ方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="aa1fb-125">プロジェクトの **チーム** タブで仮予約済みのリソースを本予約済みに変換するには、リソースを選び、**確認する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa1fb-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![コマンドを確認する](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]