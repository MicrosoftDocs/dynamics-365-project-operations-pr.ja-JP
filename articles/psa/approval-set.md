---
title: 承認セット
description: このトピックでは、承認セット、要求、およびそれらの操作のサブセットについて説明します。
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116877"
---
# <a name="approval-sets"></a><span data-ttu-id="4b586-103">承認セット</span><span class="sxs-lookup"><span data-stu-id="4b586-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4b586-104">承認セットは、承認要求を操作のより小さなサブセットにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="4b586-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="4b586-105">このグループ化により、承認はプロジェクトごとに順番に処理され、再試行と順序付けが可能になります。</span><span class="sxs-lookup"><span data-stu-id="4b586-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="4b586-106">グループ化により、大量の承認に対する承認処理の信頼性と追跡可能性が向上します。</span><span class="sxs-lookup"><span data-stu-id="4b586-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="4b586-107">承認セットは、関連するレコードの全体的な処理状態を示します。</span><span class="sxs-lookup"><span data-stu-id="4b586-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="4b586-108">承認セットを使用して承認レコードが処理されると、レコードは **提出済み** から **承認済** になり、承認セットからリンク解除されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="4b586-109">承認のために提出されたときにレコードが失敗した場合、レコードの状態は **提出済み** のままで、承認セットは失敗としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="4b586-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="4b586-110">承認セットには、失敗のエラー メッセージが記録されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="4b586-111">処理中の承認と承認セット</span><span class="sxs-lookup"><span data-stu-id="4b586-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="4b586-112">処理待ちの承認は、**処理中の承認** ビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="4b586-113">システムは、すべてのエントリを非同期で複数回処理しようとしますが、これには以前の試みが失敗した場合の承認の再試行も含まれます。</span><span class="sxs-lookup"><span data-stu-id="4b586-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="4b586-114">**承認セットの有効期間** フィールドには、セットが失敗としてマークされるまでに残された処理の試行回数が記録されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="4b586-115">失敗した承認と承認セット</span><span class="sxs-lookup"><span data-stu-id="4b586-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="4b586-116">**失敗した承認** ビューには、ユーザーの介入が必要なすべての承認が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="4b586-117">関連する承認セットのログを開いて、失敗の原因を特定します。</span><span class="sxs-lookup"><span data-stu-id="4b586-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="4b586-118">**再試行** を選択すると、承認セットの有効期間カウントが追加され、承認セット状態が **処理中** に戻り、残りのレコードの処理を試みます。</span><span class="sxs-lookup"><span data-stu-id="4b586-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="4b586-119">承認セットの構成</span><span class="sxs-lookup"><span data-stu-id="4b586-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="4b586-120">承認セット機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="4b586-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="4b586-121">承認セット機能を有効にする前に、現在処理中の承認がないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4b586-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="4b586-122">**プロジェクト パラメーター** ページに移動し、**機能コントロール** > **最新の承認を有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b586-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="4b586-123">承認セット機能を無効にする</span><span class="sxs-lookup"><span data-stu-id="4b586-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="4b586-124">承認セット機能を無効にする前に、現在処理中の承認がないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4b586-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="4b586-125">**プロジェクト パラメーター** ページに移動し、**機能コントロール** > **最新の承認を無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b586-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="4b586-126">非同期しきい値を構成する</span><span class="sxs-lookup"><span data-stu-id="4b586-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="4b586-127">承認セットを作成すると、承認のために選択したレコード数が指定されたしきい値を超えると、処理はバックグラウンドに移動します。</span><span class="sxs-lookup"><span data-stu-id="4b586-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="4b586-128">**非同期しきい値** フィールドを使用して、承認処理を同期または非同期で実行する時期を構成します。</span><span class="sxs-lookup"><span data-stu-id="4b586-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="4b586-129">有効な値は:</span><span class="sxs-lookup"><span data-stu-id="4b586-129">Valid values are:</span></span>

  - <span data-ttu-id="4b586-130">ゼロ: すべての要求は非同期に処理されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="4b586-131">0 より大きい数値: 承認は、提出された承認の数がこの値を超えた場合にのみ非同期に処理されます。</span><span class="sxs-lookup"><span data-stu-id="4b586-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
