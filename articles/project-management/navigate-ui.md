---
title: ユーザー インターフェイスのナビゲーション
description: このトピックは、Dynamics 365 プロジェクト操作でのプロジェクト管理に関する情報を提供します。
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079186"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="6ab4c-103">ユーザー インターフェイスのナビゲーション</span><span class="sxs-lookup"><span data-stu-id="6ab4c-103">Navigating the user interface</span></span>

<span data-ttu-id="6ab4c-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="6ab4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="6ab4c-105">概要</span><span class="sxs-lookup"><span data-stu-id="6ab4c-105">Overview</span></span>

<span data-ttu-id="6ab4c-106">メイン プロジェクト フォームはいくつかのタブに分かれています。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="6ab4c-107">各タブは、プロジェクト内のさまざまな詳細レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="6ab4c-108">**概要** : プロジェクトの説明を提供し、計画されたプロジェクトのパフォーマンスと実際のプロジェクトのパフォーマンスの両方を集約します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![概要タブとフィールド](media/navigation7.png)

- <span data-ttu-id="6ab4c-110">**タスク** : グリッド ビュー、ボード ビュー、およびガントで表される WBS (作業分解構造) に関する詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![タスク タブとフィールド](media/navigation8.png)

- <span data-ttu-id="6ab4c-112">**チーム** : プロジェクト参加者に関する詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="6ab4c-113">各チームメンバーに割り当てられた作業もこのビューに要約されます。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![チーム タブとフィールド](media/navigation9.png)

- <span data-ttu-id="6ab4c-115">**リソースの割り当て** : プロジェクトの各リソースの作業の時間フェーズ ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![リソースの割り当てタブとフィールド](media/navigation10.png)

- <span data-ttu-id="6ab4c-117">**リソースの調整** : 各名前付きリソースの割り当てとその予約の差を時間フェーズ ビューで提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![リソースの調整タブとフィールド](media/navigation11.png)

- <span data-ttu-id="6ab4c-119">**見積もり** : プロジェクトのコストと売上の見積もりの時間フェーズ ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![見積もりタブとフィールド](media/navigation12.png)

- <span data-ttu-id="6ab4c-121">**トラッキング** : 作業、コスト、および売上の WBS (作業分解構造) でのタスクの進行状況を示すビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![トラッキング タブとフィールド](media/navigation13.png)

- <span data-ttu-id="6ab4c-123">**営業** : プロジェクトに関連する見積もりと契約へのディープ リンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="6ab4c-124">**経費の見込み** : 組織の経費カテゴリに基づいてプロジェクト経費を定義するグリッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![経費見積もりタブとフィールド](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="6ab4c-126">グリッド コントロール</span><span class="sxs-lookup"><span data-stu-id="6ab4c-126">Grid controls</span></span>

<span data-ttu-id="6ab4c-127">以下は、さまざまなプロジェクト計画タブにある一般的なコントロールの簡単な概要です。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="6ab4c-128">最新の情報に更新</span><span class="sxs-lookup"><span data-stu-id="6ab4c-128">Refresh</span></span>

<span data-ttu-id="6ab4c-129">**更新** : グリッドのロード後に変更が発生した場合、サーバーから最新のデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![更新ボタン](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="6ab4c-131">グループ化の基準</span><span class="sxs-lookup"><span data-stu-id="6ab4c-131">Group by</span></span>

<span data-ttu-id="6ab4c-132">**グループ化** : グリッド内の行のグループ化を更新して、ユーザーのニーズに基づいてリソース、役割、またはカテゴリのいずれかを反映します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![ボタンによるグループ](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="6ab4c-134">前へ/次へ</span><span class="sxs-lookup"><span data-stu-id="6ab4c-134">Previous/Next</span></span>

<span data-ttu-id="6ab4c-135">**前へ**/**次へ** : 時間フェーズ グリッド上で表示されている期間を更新します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![前へボタンと次へボタン](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="6ab4c-137">タイムスケール</span><span class="sxs-lookup"><span data-stu-id="6ab4c-137">Timescale</span></span>

<span data-ttu-id="6ab4c-138">**タイムスケール** : 日、週、月、年で時間フェーズ データの集計を変更します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![タイムスケール ボタン](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="6ab4c-140">展開する</span><span class="sxs-lookup"><span data-stu-id="6ab4c-140">Expand</span></span>

<span data-ttu-id="6ab4c-141">**展開** : 表示されているグリッドを全画面表示にして、追加の役割を表示する機能を強化します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![[展開] ボタン](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="6ab4c-143">時間フェーズ別</span><span class="sxs-lookup"><span data-stu-id="6ab4c-143">Time-phase by</span></span>

<span data-ttu-id="6ab4c-144">**時間フェーズ別** : グリッド内の行のグループを更新して、売上見積もりのコスト見積もりを反映します。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="6ab4c-145">この制御は、見積もりスクリプトとトラッキング グリッドにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-145">This control also applies to the estimate script and the tracking grid.</span></span>

![ボタンによる時間フェーズ](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="6ab4c-147">列を追加します</span><span class="sxs-lookup"><span data-stu-id="6ab4c-147">Add column</span></span>

<span data-ttu-id="6ab4c-148">**列を追加** : ユーザーがグリッドに表示される列を定義できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="6ab4c-149">**プロジェクト計画** フォームで、すぐに使用できる列のみをグリッドに追加できます。</span><span class="sxs-lookup"><span data-stu-id="6ab4c-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![列ボタンを追加](media/navigation5.png)
