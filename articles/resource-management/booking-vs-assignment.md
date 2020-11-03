---
title: 予約と割り当て
description: このトピックでは、リソースの予約とリソースの割り当ての違いについて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079117"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="44000-103">予約と割り当て</span><span class="sxs-lookup"><span data-stu-id="44000-103">Bookings vs assignments</span></span>

<span data-ttu-id="44000-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="44000-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44000-105">予約は、プロジェクトに対するリソースの本配賦または仮配賦です。</span><span class="sxs-lookup"><span data-stu-id="44000-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="44000-106">本予約はリソースのキャパシティを消費します。</span><span class="sxs-lookup"><span data-stu-id="44000-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="44000-107">割り当ては、プロジェクト スケジュール内のプロジェクト タスクに対するリソースの割り当てです。</span><span class="sxs-lookup"><span data-stu-id="44000-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="44000-108">このリソースは、実際のリソースまたは汎用リソースになります。</span><span class="sxs-lookup"><span data-stu-id="44000-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="44000-109">理想としては、実際のリソースに対して、予約と割り当ては違いがないことから、これらは一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="44000-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="44000-110">ただし、Microsoft Dynamics Project Operations はこの一致を強制しません。</span><span class="sxs-lookup"><span data-stu-id="44000-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="44000-111">**調整** ビューでは、リソースの予約と割り当てが一致しない場所のプロジェクト マネージャーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="44000-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
