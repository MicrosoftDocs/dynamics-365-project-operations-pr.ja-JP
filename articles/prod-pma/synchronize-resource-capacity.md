---
title: リソース キャパシティの同期
description: このトピックは、カレンダーとプロジェクト間でリソースの容量を同期する方法に関する情報を提供します。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288567"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="664e5-103">リソース キャパシティの同期</span><span class="sxs-lookup"><span data-stu-id="664e5-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="664e5-104">リソース同期のプロセスは、カレンダーと基本カレンダーの情報がプロジェクトのリソース スケジュールに流れ込むことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="664e5-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="664e5-105">カレンダーが変更された場合、プロセスはプロジェクト リソースのスケジュールに必要な更新を行います。</span><span class="sxs-lookup"><span data-stu-id="664e5-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="664e5-106">カレンダーのリソース情報は事前に同期されているため、プロセスはパフォーマンスの向上にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="664e5-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="664e5-107">したがって、リソース スケジュール情報の更新はより迅速に行われます。</span><span class="sxs-lookup"><span data-stu-id="664e5-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="664e5-108">プロセスは一度に 1 つではなくバッチとしてスケジュールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="664e5-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="664e5-109">それ以外の場合は、情報が最後に同期された包括的な日付をユーザーが忘れるというリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="664e5-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="664e5-110">包括的な日付を使用しない場合、日付の同期中にギャップが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="664e5-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="664e5-112">リソース キャパシティ ロールアップの同期</span><span class="sxs-lookup"><span data-stu-id="664e5-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="664e5-113">同期プロセスは、すべてのリソース カレンダー情報を同期するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="664e5-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="664e5-114">この情報には、プロジェクトのリソース カレンダーのキャパシティ テーブルへの変更に関する基本カレンダー情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="664e5-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="664e5-115">新しいリソースがプロジェクトに追加された場合、同期は、更新されたカレンダー情報が使用可能であることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="664e5-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="664e5-116">この同期はいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="664e5-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="664e5-117">バッチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="664e5-117">We recommend that you use a batch.</span></span> <span data-ttu-id="664e5-118">オプションは、確保済能力の同期中に使用できます。</span><span class="sxs-lookup"><span data-stu-id="664e5-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="664e5-119">**プロジェクト管理と会計**&gt;**定期的**&gt;**キャパシティの同期**&gt;**リソース キャパシティのロールアップの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="664e5-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="664e5-120">次の表にオプション設定します。</span><span class="sxs-lookup"><span data-stu-id="664e5-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="664e5-121">オプション</span><span class="sxs-lookup"><span data-stu-id="664e5-121">Option</span></span>      | <span data-ttu-id="664e5-122">内容</span><span class="sxs-lookup"><span data-stu-id="664e5-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="664e5-123">期間コード</span><span class="sxs-lookup"><span data-stu-id="664e5-123">Period code</span></span> | <span data-ttu-id="664e5-124">必要に応じて、総勘定元帳の日付範囲コードを選択して、リソース キャパシティ ロールアップの同期プロセスの開始日と終了日を設定します。</span><span class="sxs-lookup"><span data-stu-id="664e5-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="664e5-125">開始日</span><span class="sxs-lookup"><span data-stu-id="664e5-125">Start date</span></span>  | <span data-ttu-id="664e5-126">リソース キャパシティ ロールアップの同期プロセスの開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="664e5-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="664e5-127">終了日</span><span class="sxs-lookup"><span data-stu-id="664e5-127">End date</span></span>    | <span data-ttu-id="664e5-128">リソース キャパシティ ロールアップの同期プロセスの終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="664e5-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="664e5-129">[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="664e5-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]