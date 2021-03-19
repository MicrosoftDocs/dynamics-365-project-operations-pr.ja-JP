---
title: 売上の見積もりの管理
description: このトピックでは、プロジェクトで売上見積もりを処理する方法を説明します。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279009"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="0eba1-103">売上の見積もりの管理</span><span class="sxs-lookup"><span data-stu-id="0eba1-103">Manage revenue estimates</span></span>

<span data-ttu-id="0eba1-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0eba1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0eba1-105">売上見積もりの作成、計算、転記、取り消し、削除を行えます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="0eba1-106">手動または定期的なプロセスを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="0eba1-107">このトピックでは、プロジェクトで売上見積もりを処理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="0eba1-108">売上見積もりの手動管理</span><span class="sxs-lookup"><span data-stu-id="0eba1-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="0eba1-109">固定価格売上見積もりプロジェクトまたは **見積もり照会** ページ (**プロジェクトの管理と会計** > **レポートと照会** > **見積もり照会とレポート**) で、**見積もり** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="0eba1-110">定期的なプロセスを使用して売上見積もりを管理する</span><span class="sxs-lookup"><span data-stu-id="0eba1-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="0eba1-111">**プロジェクトの管理と会計** > **定期的** > **見積もり** に移動して対応するプロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="0eba1-112">売上見積もりを作成する</span><span class="sxs-lookup"><span data-stu-id="0eba1-112">Create a revenue estimate</span></span>

<span data-ttu-id="0eba1-113">売上見積もりの作成には、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="0eba1-114">**プロジェクトの管理と会計** > **定期的** > **見積もり** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="0eba1-115">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0eba1-115">Select **New**.</span></span> <span data-ttu-id="0eba1-116">**見積もり作成** ページで、以下のパラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="0eba1-117">**期間コード**: このコードは見積もりの転記頻度を決定します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="0eba1-118">**見積もり日**: 見積もりを処理する日付。</span><span class="sxs-lookup"><span data-stu-id="0eba1-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="0eba1-119">**継続的**: 前の期間に見積もりを転記した場合や、これが作成した最初の見積もりの場合にのみ、このチェックボックスを選択して見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="0eba1-120">これを選択しないと、前の期間に見積もりを転記していない場合も見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="0eba1-121">**メソッドを完了するコスト**: 残りのプロジェクト作業を見積もる方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="0eba1-122">詳細については [メソッドを完了するコスト](cost-complete-methods.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0eba1-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="0eba1-123">**完了方法**: 以下のオプションから完了方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="0eba1-124">**自動**: 計算に含めるコスト明細行に基づいて、完了割合を自動で計算します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="0eba1-125">含めるコスト明細行はコスト テンプレートで定義します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="0eba1-126">**手動**: 完了割合は、最後の見積もり完了割合と同じです。</span><span class="sxs-lookup"><span data-stu-id="0eba1-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="0eba1-127">見積もりの作成後に **見積もり** ページから **手動計算** を変更できます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="0eba1-128">**コスト テンプレートから**: 自動と手動の方法の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="0eba1-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="0eba1-129">このオプションは、コスト テンプレートの既定値に応じて自動または手動に設定します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="0eba1-130">**予測モデル**: 見積もりの予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="0eba1-131">**見積もり一覧の印刷**: 見積もり一覧の作成と表示。</span><span class="sxs-lookup"><span data-stu-id="0eba1-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="0eba1-132">このリストは現在の機能の状態を含みます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-132">The list contains the status of the current function.</span></span> <span data-ttu-id="0eba1-133">レポート上の見積もりに関する警告を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="0eba1-134">次の条件は、見積もり一覧に表示される警告の原因になります。</span><span class="sxs-lookup"><span data-stu-id="0eba1-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="0eba1-135">100% を超える完了割合。</span><span class="sxs-lookup"><span data-stu-id="0eba1-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="0eba1-136">0% 未満の完了割合。</span><span class="sxs-lookup"><span data-stu-id="0eba1-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="0eba1-137">**完了対象** 列に存在する負の金額。</span><span class="sxs-lookup"><span data-stu-id="0eba1-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="0eba1-138">対応する契約金額が見積もりに存在しない場合。</span><span class="sxs-lookup"><span data-stu-id="0eba1-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="0eba1-139">コスト見積もりを添付していない見積もり。</span><span class="sxs-lookup"><span data-stu-id="0eba1-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="0eba1-140">**情報ログを表示**: ジョブの実行時に処理したプロジェクト見積もりに関する情報を含むメッセージを受信する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="0eba1-141">仕掛品または見越計上を転記する</span><span class="sxs-lookup"><span data-stu-id="0eba1-141">Post WIP or accruals</span></span>

<span data-ttu-id="0eba1-142">見積もりの評価後に、それらを維持、減少、増加させます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="0eba1-143">その後、**完了した契約** 評価プリンシパルで作業する場合は仕掛品を転記し、**完成率** 評価プリンシパルで作業する場合は見越計上を転記できます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="0eba1-144">見積もり期間のステータスが **作成済み** から **転記済み** に変化します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="0eba1-145">仕掛品や見越計上の取り消し</span><span class="sxs-lookup"><span data-stu-id="0eba1-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="0eba1-146">取り消しオプションを使用して転記済みの仕掛品や見越計上を貸方に記入してから、その期間の見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="0eba1-147">他の期間に挟まれた期間を取り消す場合は、必要な見積もり期間を取り消してから、それらを再転記します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="0eba1-148">以降のすべての期間は前の期間の見積もりに依存するため、期間はスキップできません。</span><span class="sxs-lookup"><span data-stu-id="0eba1-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="0eba1-149">見積もりプロジェクトを削除して、プロジェクトを終了します</span><span class="sxs-lookup"><span data-stu-id="0eba1-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="0eba1-150">見積もりプロセスの最終ステップは、見積もりプロジェクトを削除して、完了割合が 100% に達したら固定価格プロジェクトを終了することです。</span><span class="sxs-lookup"><span data-stu-id="0eba1-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="0eba1-151">消去を実行すると、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0eba1-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="0eba1-152">完了した契約をともなう固定価格プロジェクトの場合、仕掛品の値を残高勘定からクリアして損益勘定に転記します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="0eba1-153">完了割合をともなう固定価格プロジェクトの場合、見越計上を損益勘定から削除します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="0eba1-154">この見積もりはステータスを **削除済み** に変更します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="0eba1-155">特別な場合、割合が 100% を超えることがあります。</span><span class="sxs-lookup"><span data-stu-id="0eba1-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="0eba1-156">これが発生した場合は **完了するコストをゼロに設定する方法** を使用して 100% に到達させ、完了割合を減らします。</span><span class="sxs-lookup"><span data-stu-id="0eba1-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="0eba1-157">削除を取り消す</span><span class="sxs-lookup"><span data-stu-id="0eba1-157">Reverse elimination</span></span>

1. <span data-ttu-id="0eba1-158">**プロジェクトの管理と会計** > **定期的** > **見積もり** > **削除を取り消す** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="0eba1-159">アクション ウィンドウの **プロセス** タブの **維持** グループで、**見積もり** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="0eba1-160">**削除を取り消す** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="0eba1-161">このページを使用して、指定した見積もり日で見積もりステータスが **消去済み** の消去をすべて取り消します。</span><span class="sxs-lookup"><span data-stu-id="0eba1-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="0eba1-162">適切なフィールドを選択するとトランザクションのステータスが変わります。</span><span class="sxs-lookup"><span data-stu-id="0eba1-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="0eba1-163">プロジェクト ステージが終了に設定されている場合、これによりプロジェクト ステータスが **処理中** に自動で変更されます。</span><span class="sxs-lookup"><span data-stu-id="0eba1-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="0eba1-164">プロジェクト期間の見積もりステータスが **転記済み** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="0eba1-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]