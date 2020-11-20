---
title: 予約と割り当て
description: このトピックでは、リソースの予約とリソースの割り当ての違いについて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130224"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="1c104-103">予約と割り当て</span><span class="sxs-lookup"><span data-stu-id="1c104-103">Bookings vs assignments</span></span>

<span data-ttu-id="1c104-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1c104-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c104-105">予約は、プロジェクトに対するリソースの本配賦または仮配賦です。</span><span class="sxs-lookup"><span data-stu-id="1c104-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="1c104-106">本予約はリソースのキャパシティを消費します。</span><span class="sxs-lookup"><span data-stu-id="1c104-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="1c104-107">予約はチームの組織的なコンセプトを表すため、様々なプロジェクトでリソースをどのように活用するかを理解できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="1c104-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="1c104-108">Dynamics 365 Project Operations は、予約をプロジェクト レベルのコンセプトとして捉えています。</span><span class="sxs-lookup"><span data-stu-id="1c104-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="1c104-109">割り当てとは、予約とは異なり、プロジェクト スケジュールの中で、プロジェクトのタスクにリソースを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1c104-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="1c104-110">リソースには名前を付けることも、汎用なものにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1c104-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="1c104-111">通常、リソースの予約の合計は、1つまたは複数のタスクを横断するリソースの割り当ての合計と同じになります。</span><span class="sxs-lookup"><span data-stu-id="1c104-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="1c104-112">ただし、 Project Operations ではこの一致を強制しません。</span><span class="sxs-lookup"><span data-stu-id="1c104-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="1c104-113">**調整** ビューでは、リソースの予約と割り当てが一致しない箇所をプロジェクト マネージャに表示します。</span><span class="sxs-lookup"><span data-stu-id="1c104-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
