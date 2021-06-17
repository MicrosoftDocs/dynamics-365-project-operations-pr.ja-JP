---
title: リソース キャパシティの同期
description: このトピックは、カレンダーとプロジェクト間でリソースの容量を同期する方法に関する情報を提供します。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997517"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="820a3-103">リソース キャパシティの同期</span><span class="sxs-lookup"><span data-stu-id="820a3-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="820a3-104">リソース同期のプロセスは、カレンダーと基本カレンダーの情報がプロジェクトのリソース スケジュールに流れ込むことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="820a3-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="820a3-105">カレンダーが変更された場合、プロセスはプロジェクト リソースのスケジュールに必要な更新を行います。</span><span class="sxs-lookup"><span data-stu-id="820a3-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="820a3-106">カレンダーのリソース情報は事前に同期されているため、プロセスはパフォーマンスの向上にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="820a3-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="820a3-107">したがって、リソース スケジュール情報の更新はより迅速に行われます。</span><span class="sxs-lookup"><span data-stu-id="820a3-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="820a3-108">プロセスは一度に 1 つではなくバッチとしてスケジュールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="820a3-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="820a3-109">それ以外の場合は、情報が最後に同期された包括的な日付をユーザーが忘れるというリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="820a3-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="820a3-110">包括的な日付を使用しない場合、日付の同期中にギャップが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="820a3-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="820a3-112">リソース キャパシティ ロールアップの同期</span><span class="sxs-lookup"><span data-stu-id="820a3-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="820a3-113">同期プロセスは、すべてのリソース カレンダー情報を同期するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="820a3-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="820a3-114">この情報には、プロジェクトのリソース カレンダーのキャパシティ テーブルへの変更に関する基本カレンダー情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="820a3-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="820a3-115">新しいリソースがプロジェクトに追加された場合、同期は、更新されたカレンダー情報が使用可能であることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="820a3-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="820a3-116">この同期はいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="820a3-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="820a3-117">バッチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="820a3-117">We recommend that you use a batch.</span></span> <span data-ttu-id="820a3-118">オプションは、確保済能力の同期中に使用できます。</span><span class="sxs-lookup"><span data-stu-id="820a3-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="820a3-119">**プロジェクト管理と会計**&gt;**定期的**&gt;**キャパシティの同期**&gt;**リソース キャパシティのロールアップの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="820a3-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="820a3-120">次の表にオプション設定します。</span><span class="sxs-lookup"><span data-stu-id="820a3-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="820a3-121">オプション</span><span class="sxs-lookup"><span data-stu-id="820a3-121">Option</span></span>      | <span data-ttu-id="820a3-122">内容</span><span class="sxs-lookup"><span data-stu-id="820a3-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="820a3-123">期間コード</span><span class="sxs-lookup"><span data-stu-id="820a3-123">Period code</span></span> | <span data-ttu-id="820a3-124">必要に応じて、総勘定元帳の日付範囲コードを選択して、リソース キャパシティ ロールアップの同期プロセスの開始日と終了日を設定します。</span><span class="sxs-lookup"><span data-stu-id="820a3-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="820a3-125">開始日</span><span class="sxs-lookup"><span data-stu-id="820a3-125">Start date</span></span>  | <span data-ttu-id="820a3-126">リソース キャパシティ ロールアップの同期プロセスの開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="820a3-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="820a3-127">終了日</span><span class="sxs-lookup"><span data-stu-id="820a3-127">End date</span></span>    | <span data-ttu-id="820a3-128">リソース キャパシティ ロールアップの同期プロセスの終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="820a3-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="820a3-129">[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="820a3-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]