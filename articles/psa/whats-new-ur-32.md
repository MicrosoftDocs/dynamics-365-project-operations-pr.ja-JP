---
title: Project Service Automation 更新プログラム リリース 32、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 32、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129672"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="224b5-103">Project Service Automation 更新プログラム リリース 32、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="224b5-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="224b5-104">Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="224b5-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="224b5-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="224b5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="224b5-106">Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="224b5-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="224b5-107">このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="224b5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="224b5-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="224b5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="224b5-109">このトピックには、Project Service Automation V3 更新プログラム 32 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="224b5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="224b5-110">このバージョンのビルド番号は V3.10.53.108 であり、2021 年 6 月の自己更新を通じて一般提供されています。</span><span class="sxs-lookup"><span data-stu-id="224b5-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="224b5-111">更新プログラム 32</span><span class="sxs-lookup"><span data-stu-id="224b5-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="224b5-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="224b5-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="224b5-113">全般</span><span class="sxs-lookup"><span data-stu-id="224b5-113">General</span></span>

- <span data-ttu-id="224b5-114">メジャー アップグレードが失敗した場合は、メイン アプリケーションのエントリ ポイントのみをブロックして、共有エンティティに引き続きアクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="224b5-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="224b5-115">時間と経費</span><span class="sxs-lookup"><span data-stu-id="224b5-115">Time and Expense</span></span>

<span data-ttu-id="224b5-116">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="224b5-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="224b5-117">**TimeEntriesImportFromResourceAssignment** は、リソース要件の配分型スライスの開始時刻と終了時刻を維持しません。</span><span class="sxs-lookup"><span data-stu-id="224b5-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="224b5-118">**オープンしているエントリ** を **時間エントリ** グリッドで選択すると、他のフォームを選択できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="224b5-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="224b5-119">時間エントリへの割り当てをインポートしている間に、クライアント コード クエリが長い URL を生成して、クエリに失敗するする場合があります。</span><span class="sxs-lookup"><span data-stu-id="224b5-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="224b5-120">**時間エントリ** グリッドでは、セルから値が削除された後、フォーカスはグリッドに残りません。</span><span class="sxs-lookup"><span data-stu-id="224b5-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="224b5-121">**却下** ボタンは、最新の承認の **処理中の承認** ビューから削除されました。</span><span class="sxs-lookup"><span data-stu-id="224b5-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="224b5-122">時間エントリの一括承認の安定性とパフォーマンスは、デッドロックと **時間エントリ** エンティティに関連するカスタマイズを適切に処理できないことによって影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="224b5-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="224b5-123">プロジェクトの計画</span><span class="sxs-lookup"><span data-stu-id="224b5-123">Project Planning</span></span>

- <span data-ttu-id="224b5-124">**契約単位** フィールドに null 値があるプロジェクトを更新すると、null 参照例外が生成されます。</span><span class="sxs-lookup"><span data-stu-id="224b5-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="224b5-125">**プロジェクト合計の更新** では、プロジェクトの残コストと残売上が正しく計算されません。</span><span class="sxs-lookup"><span data-stu-id="224b5-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="224b5-126">冗長な価格計算は、リソース要件の配分型の更新に関連するパフォーマンスに影響します。</span><span class="sxs-lookup"><span data-stu-id="224b5-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="224b5-127">リソース管理</span><span class="sxs-lookup"><span data-stu-id="224b5-127">Resource Management</span></span>

<span data-ttu-id="224b5-128">次の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="224b5-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="224b5-129">予約可能なリソースのカレンダー キャパシティが 1 を超えると、Project Service Automation はキャパシティを 0 (ゼロ) と誤って認識します。</span><span class="sxs-lookup"><span data-stu-id="224b5-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="224b5-130">そのため、スケジュール ビューで無限ループが発生します。</span><span class="sxs-lookup"><span data-stu-id="224b5-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="224b5-131">営業</span><span class="sxs-lookup"><span data-stu-id="224b5-131">Sales</span></span>

<span data-ttu-id="224b5-132">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="224b5-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="224b5-133">カスタム トランザクションの種類を持つ仕訳帳明細行が作成されると、次の null 参照例外が発生します: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*。</span><span class="sxs-lookup"><span data-stu-id="224b5-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="224b5-134">見積がコピーされる前に非アクティブ化されたロールとカテゴリは、新しくコピーされた見積書の請求可能ロールとカテゴリに追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="224b5-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="224b5-135">ドキュメントの日付と会計日は、下書き請求書で直接作成された請求書明細行の詳細に記載されている開始日と一致していません。</span><span class="sxs-lookup"><span data-stu-id="224b5-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="224b5-136">null 参照例外は、見積がコピーされる前に、ロールとカテゴリの非アクティブ化に関連するシナリオで生成されます。</span><span class="sxs-lookup"><span data-stu-id="224b5-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="224b5-137">**プロジェクト** ページの **価格の更新** アクションでは、経費見積もりと材料見積もりは更新されません。</span><span class="sxs-lookup"><span data-stu-id="224b5-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
