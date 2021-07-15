---
title: 時間エントリ の UI の動作
description: このトピックでは、時間エントリの UI の動作について説明します。
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304307"
---
# <a name="time-entry-ui-behavior"></a><span data-ttu-id="fb1b9-103">時間エントリ の UI の動作</span><span class="sxs-lookup"><span data-stu-id="fb1b9-103">Time entry UI behavior</span></span>

<span data-ttu-id="fb1b9-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="fb1b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fb1b9-105">**週単位の時間エントリ** グリッドは、2 つのメイン セクション、**ディメンション** および **期間** を持つ カスタム コントロールです。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-105">The **Weekly time entry** grid is a custom control that has two main sections, **Dimensions** and **Duration**.</span></span>

## <a name="keyboard-shortcuts"></a><span data-ttu-id="fb1b9-106">キーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="fb1b9-106">Keyboard shortcuts</span></span>
| <span data-ttu-id="fb1b9-107">操作​​</span><span class="sxs-lookup"><span data-stu-id="fb1b9-107">Action</span></span>        | <span data-ttu-id="fb1b9-108">ショートカット</span><span class="sxs-lookup"><span data-stu-id="fb1b9-108">Shortcut</span></span>                  |
|------------   |------------------------   |
| <span data-ttu-id="fb1b9-109">新しい</span><span class="sxs-lookup"><span data-stu-id="fb1b9-109">New</span></span>           | <span data-ttu-id="fb1b9-110">Alt + Shift + n</span><span class="sxs-lookup"><span data-stu-id="fb1b9-110">Alt + Shift + n</span></span>           |
| <span data-ttu-id="fb1b9-111">行のコピー</span><span class="sxs-lookup"><span data-stu-id="fb1b9-111">Copy row</span></span>      | <span data-ttu-id="fb1b9-112">Alt + Shift + c</span><span class="sxs-lookup"><span data-stu-id="fb1b9-112">Alt + Shift + c</span></span>           |
| <span data-ttu-id="fb1b9-113">エントリの編集</span><span class="sxs-lookup"><span data-stu-id="fb1b9-113">Edit entry</span></span>    | <span data-ttu-id="fb1b9-114">Alt + Shift + e</span><span class="sxs-lookup"><span data-stu-id="fb1b9-114">Alt + Shift + e</span></span>           |
| <span data-ttu-id="fb1b9-115">行の編集</span><span class="sxs-lookup"><span data-stu-id="fb1b9-115">Edit row</span></span>      | <span data-ttu-id="fb1b9-116">Alt + Shift + Ctrl + e</span><span class="sxs-lookup"><span data-stu-id="fb1b9-116">Alt + Shift + Ctrl + e</span></span>    |
| <span data-ttu-id="fb1b9-117">オープンしているエントリ</span><span class="sxs-lookup"><span data-stu-id="fb1b9-117">Open entry</span></span>    | <span data-ttu-id="fb1b9-118">Alt + Shift + o</span><span class="sxs-lookup"><span data-stu-id="fb1b9-118">Alt + Shift + o</span></span>           |
| <span data-ttu-id="fb1b9-119">提出​​</span><span class="sxs-lookup"><span data-stu-id="fb1b9-119">Submit</span></span>        | <span data-ttu-id="fb1b9-120">Alt + Shift + s</span><span class="sxs-lookup"><span data-stu-id="fb1b9-120">Alt + Shift + s</span></span>           |
| <span data-ttu-id="fb1b9-121">取り消し</span><span class="sxs-lookup"><span data-stu-id="fb1b9-121">Recall</span></span>        | <span data-ttu-id="fb1b9-122">Alt + Shift + r</span><span class="sxs-lookup"><span data-stu-id="fb1b9-122">Alt + Shift + r</span></span>           |
| <span data-ttu-id="fb1b9-123">Delete キー</span><span class="sxs-lookup"><span data-stu-id="fb1b9-123">Delete</span></span>        | <span data-ttu-id="fb1b9-124">Alt + Shift + d</span><span class="sxs-lookup"><span data-stu-id="fb1b9-124">Alt + Shift + d</span></span>           |
| <span data-ttu-id="fb1b9-125">週のコピー</span><span class="sxs-lookup"><span data-stu-id="fb1b9-125">Copy week</span></span>     | <span data-ttu-id="fb1b9-126">Alt + Shift + w</span><span class="sxs-lookup"><span data-stu-id="fb1b9-126">Alt + Shift + w</span></span>           |

## <a name="dimensions"></a><span data-ttu-id="fb1b9-127">ディメンション</span><span class="sxs-lookup"><span data-stu-id="fb1b9-127">Dimensions</span></span>
<span data-ttu-id="fb1b9-128">**ディメンション** セクションには、時間を入力できるディメンションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-128">The **Dimensions** section shows the dimensions that time can be entered against.</span></span> <span data-ttu-id="fb1b9-129">次のディメンションは、標準でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-129">The following dimensions are supported out-of-the-box:</span></span>

  - <span data-ttu-id="fb1b9-130">Project</span><span class="sxs-lookup"><span data-stu-id="fb1b9-130">Project</span></span>
  - <span data-ttu-id="fb1b9-131">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="fb1b9-131">Project Task</span></span>
  - <span data-ttu-id="fb1b9-132">ロール</span><span class="sxs-lookup"><span data-stu-id="fb1b9-132">Role</span></span>
  - <span data-ttu-id="fb1b9-133">型</span><span class="sxs-lookup"><span data-stu-id="fb1b9-133">Type</span></span>
  - <span data-ttu-id="fb1b9-134">入力の状態</span><span class="sxs-lookup"><span data-stu-id="fb1b9-134">Entry Status</span></span>

<span data-ttu-id="fb1b9-135">**ディメンション** セクションではインライン編集はできません。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-135">The **Dimensions** section doesn't allow inline editing.</span></span> <span data-ttu-id="fb1b9-136">このセクションは、カスタム フィールドを毎週の時間エントリ グリッドに追加できるように、ビューにより支えられています。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-136">This section is backed by a view that enables custom fields to be added to the weekly time entry grid.</span></span>

## <a name="duration"></a><span data-ttu-id="fb1b9-137">時間</span><span class="sxs-lookup"><span data-stu-id="fb1b9-137">Duration</span></span>
<span data-ttu-id="fb1b9-138">期間セクションには、列見出しとしてその週の曜日が示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-138">The Duration section shows the days of the week as column headers.</span></span> <span data-ttu-id="fb1b9-139">このセクションはインライン編集が可能です。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-139">This section allows inline editing.</span></span> <span data-ttu-id="fb1b9-140">適切なディメンションで時間エントリ行が作成された後、ユーザーはそれらのディメンションで使用した時間数をすばやく入力できます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-140">After a time entry row is created with the appropriate dimensions, users can quickly enter the amount of time that they spent on those dimensions.</span></span>

## <a name="create-a-new-time-entry"></a><span data-ttu-id="fb1b9-141">新しい時間エントリを作成します</span><span class="sxs-lookup"><span data-stu-id="fb1b9-141">Create a new time entry</span></span>

1. <span data-ttu-id="fb1b9-142">時間エントリ グリッドで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-142">In the time entry grid, select **New**.</span></span> 
2. <span data-ttu-id="fb1b9-143">**時間入力簡易作成フォーム** ダイアログ ボックスで、時間エントリ日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-143">In the **Time Entry Quick Create** dialog box, select the time entry date.</span></span>
3. <span data-ttu-id="fb1b9-144">**プロジェクト** のデータ、**プロジェクトのタスク**、**ロール**、および **期間** のディメンションを入力します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-144">Enter data for the **Project**, **Project Task**, **Role**, and **Duration** dimensions.</span></span> <span data-ttu-id="fb1b9-145">この情報は、時、分、日付を **h**、**m**、**d** の形式で、数値と共に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-145">This information should be added in minutes, hours, or days by typing **h**, **m**, or **d**, together with the number.</span></span> 
4. <span data-ttu-id="fb1b9-146">エントリの説明および時間エントリに関連して外部に共有できるコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-146">Enter a description for the entry and any comments that can be shared externally regarding time entry.</span></span> 

<span data-ttu-id="fb1b9-147">エントリを保存すると、入力した値が **分析コード** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-147">When you save the entry, the entered values appear in the **Dimensions** section.</span></span> <span data-ttu-id="fb1b9-148">**期間** フィールドに入力した情報は、その時間エントリが作成された日付に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-148">The information entered in the **Duration** field appears on the date that the time entry was created for.</span></span>

<span data-ttu-id="fb1b9-149">検索フィールドは、システム ビューによってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-149">Lookup fields are backed by system views.</span></span> <span data-ttu-id="fb1b9-150">たとえば、ユーザーがプロジェクトを入力すると、**プロジェクト タスク** フィールドは既定により **コピー** ビューに設定されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-150">For example, after a user enters a project, the **Project Task** field is set to the **Copy** view by default.</span></span> <span data-ttu-id="fb1b9-151">ユーザーに割り当てられていないタスクの時間エントリを作成するには、検索ダイアログ ボックスの **ビューの変更** を選択し、**すべてのアクティブなプロジェクト タスク** ビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-151">To create time entries for tasks that aren't assigned to a user, select **Change View** in the lookup dialog box, and then select the **All Active Project Tasks** view.</span></span>

## <a name="edit-a-time-entry"></a><span data-ttu-id="fb1b9-152">時間エントリの編集</span><span class="sxs-lookup"><span data-stu-id="fb1b9-152">Edit a time entry</span></span> 
<span data-ttu-id="fb1b9-153">時間エントリ ページでの一部のフィールドの詳細、**説明** と **外部コメント** などは、週単位の時間エントリ グリッドに表示されません。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-153">Details from some fields on the time entry page, such as **Description** and **External Comments**, aren't shown in the weekly time entry grid.</span></span> <span data-ttu-id="fb1b9-154">代わりに、小さな三角の指標が、詳細情報がある **期間** のセルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-154">Instead, a small triangular indicator appears in the **Duration** cells that have these additional details.</span></span> 

1. <span data-ttu-id="fb1b9-155">時間エントリを編集するには、時間エントリで更新するセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-155">To edit a time entry, select the cell you want to update in the time entry.</span></span>
2. <span data-ttu-id="fb1b9-156">**詳細の編集** を選択し、**時間エントリ メイン フォーム** ウィンドウでデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-156">Select **Edit Details** to update the data in the **Time Entry Mainform** pane.</span></span> 

## <a name="copy-a-time-entry-row"></a><span data-ttu-id="fb1b9-157">時間エントリ行のコピー</span><span class="sxs-lookup"><span data-stu-id="fb1b9-157">Copy a time entry row</span></span>
<span data-ttu-id="fb1b9-158">行が作成された後、行全体を新しい行にコピーする場合は、**行のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-158">After the row has been created, you can select **Copy Row** to copy the whole row to a new row.</span></span> <span data-ttu-id="fb1b9-159">行がこのようにコピーされると、ディメンション、期間もコピーされます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-159">When a row is copied in this way, dimensions and durations are also copied.</span></span> <span data-ttu-id="fb1b9-160">**行の編集** を選択して、**期間** セクションのディメンション値と期間を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-160">You can also select **Edit Row** to update dimension values and durations in the **Duration** section.</span></span>

## <a name="open-a-time-entry-behavior"></a><span data-ttu-id="fb1b9-161">時間エントリを開くの動作</span><span class="sxs-lookup"><span data-stu-id="fb1b9-161">Open a time entry behavior</span></span>
<span data-ttu-id="fb1b9-162">最も目立つフィールドに最適かつ迅速に入力できるようにするために、週単位の時間エントリ グリッドには、選択済みのディメンションと期間のサブセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-162">To support optimal and quick entry in the most prominent fields, the weekly time entry grid shows a subset of selected dimensions and time durations.</span></span> <span data-ttu-id="fb1b9-163">単一の時間エントリのすべての情報を **エントリの編集** で表示するには、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-163">To view all the details of a single time entry, under **Edit Entry**, select **Open**.</span></span>

## <a name="submit-a-time-entry"></a><span data-ttu-id="fb1b9-164">時間エントリを送信する</span><span class="sxs-lookup"><span data-stu-id="fb1b9-164">Submit a time entry</span></span>
<span data-ttu-id="fb1b9-165">セルのブロックまたは時間エントリ行全体を選択した後、**送信** を選択して、単一の時間エントリまたは時間エントリの単一のグループを送信できます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-165">You can submit a single time entry or a group of time entries by selecting a block of cells or a whole time entry row, and then selecting **Submit**.</span></span> <span data-ttu-id="fb1b9-166">送信された時間エントリは、承認者の **承認** ページで承認が保留になっているエントリとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-166">Submitted time entries appear as entries that are pending approval on the approvers' **Approval** page.</span></span> <span data-ttu-id="fb1b9-167">時間エントリが正常に送信されると、編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-167">After time entries are successfully submitted, they can't be edited.</span></span>

## <a name="recall-a-time-entry"></a><span data-ttu-id="fb1b9-168">時間エントリの取り消し</span><span class="sxs-lookup"><span data-stu-id="fb1b9-168">Recall a time entry</span></span>
<span data-ttu-id="fb1b9-169">送信済みの時間エントリを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-169">You can recall time entries that you've submitted.</span></span> <span data-ttu-id="fb1b9-170">単一の時間エントリ、時間エントリの単一のブロック、または時間エントリ行全体を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-170">You can recall a single time entry, a block of time entries, or a whole row of time entries.</span></span> <span data-ttu-id="fb1b9-171">取り消した時間エントリは編集できます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-171">Recalled time entries can be edited.</span></span>

## <a name="time-entry-status"></a><span data-ttu-id="fb1b9-172">時間エントリの状態</span><span class="sxs-lookup"><span data-stu-id="fb1b9-172">Time entry status</span></span>

- <span data-ttu-id="fb1b9-173">**下書き**: 新しい時間エントリには、**下書き** 状態が自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-173">**Draft**: New time entries are automatically assigned a status of **Draft**.</span></span> <span data-ttu-id="fb1b9-174">**下書き** の状態の時間エントリしか削除できません。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-174">Only time entries that have a status of **Draft** can be deleted.</span></span>
- <span data-ttu-id="fb1b9-175">**送信済み**: 時間エントリを送信すると、その状態が **送信済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-175">**Submitted**: When a time entry is submitted, the status is updated to **Submitted**.</span></span> 
- <span data-ttu-id="fb1b9-176">**承認済み**: 送信した時間エントリが承認されると、その状態が **承認済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-176">**Approved**: When a submitted time entry is approved, the status is updated to **Approved**.</span></span> 
- <span data-ttu-id="fb1b9-177">**差し戻し済み**: 時間エントリが拒否されると、その状態が **差し戻し済み** に更新され、エントリは収集および再送信の対象となります。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-177">**Returned**: If a time entry is rejected, the status is updated to **Returned**, and the entry becomes available for correction and resubmission.</span></span> 

## <a name="view-rejection-comments"></a><span data-ttu-id="fb1b9-178">拒否のコメントを表示する</span><span class="sxs-lookup"><span data-stu-id="fb1b9-178">View rejection comments</span></span>
<span data-ttu-id="fb1b9-179">時間エントリが承認者に拒否された場合、承認者は、リソースが拒否の理由を理解しやすいように、コメントを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-179">When a time entry is rejected by an approver, the approver might add comments to help the resource understand the reason for the rejection.</span></span> <span data-ttu-id="fb1b9-180">時間エントリの拒否のコメントを表示するには、**エントリを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-180">To view the rejection comments for a time entry, select **Open entry**.</span></span> <span data-ttu-id="fb1b9-181">拒否のコメントはタイムラインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-181">The rejection comments will be shown in the timeline.</span></span> <span data-ttu-id="fb1b9-182">ユーザーは、エントリを再送信する前に、拒否のコメントに応答できます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-182">The user can respond to the rejection comments before they resubmit the entry.</span></span>

## <a name="copy-week"></a><span data-ttu-id="fb1b9-183">週のコピー</span><span class="sxs-lookup"><span data-stu-id="fb1b9-183">Copy week</span></span>
<span data-ttu-id="fb1b9-184">いくつかの時間エントリが作成された後、ユーザーは同時に複数の時間エントリを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-184">After a few time entries have been created, users can create multiple time entries at the same time.</span></span>

1. <span data-ttu-id="fb1b9-185">**時間エントリ** フォームで、**週のコピー** を選択して、追加の時間エントリを一括作成できます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-185">In the **Time Entries** form, select **Copy Week** to bulk-create additional time entries.</span></span> 
2. <span data-ttu-id="fb1b9-186">**コピー** ダイアログ ボックスの **期間開始** セクションで、**開始日** および **終了日** フィールドを使用して、時間エントリをコピーする場合のコピー元の日付範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-186">In the **Copy** dialog box, in the **From period** section, use the **Start Date** and **End Date** fields to define the date range to copy time entries from.</span></span> 
3. <span data-ttu-id="fb1b9-187">フィールド **終了期間** セクションあるいは **開始日** フィールドで、時間エントリを作成する日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-187">In the **To Period** section, in the **Start Date** field, specify the date to create time entries for.</span></span> 
4. <span data-ttu-id="fb1b9-188">**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-188">Select **Copy**.</span></span> <span data-ttu-id="fb1b9-189">**終了期間** で作成済みの日付に対し、**開始期間** の対象の週の、対応する曜日の時間エントリのコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-189">For the specified date in the **To period**, a copy of the time entries for the corresponding day of the week in the **From period** is created.</span></span> <span data-ttu-id="fb1b9-190">たとえば、先週の月曜日の時間エントリは、**終了期間** として指定された週の月曜日にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-190">For example, Monday's time entry from last week is copied into Monday of the week that is specified as the **To period**.</span></span>

## <a name="import"></a><span data-ttu-id="fb1b9-191">インポート</span><span class="sxs-lookup"><span data-stu-id="fb1b9-191">Import</span></span>
<span data-ttu-id="fb1b9-192">同一の基本プロセスが、予約、割り当て、および交換からインポートして使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-192">The same basic process is used to import from bookings, assignments, and exchanges.</span></span> <span data-ttu-id="fb1b9-193">予約のインポート元の日付範囲を指定し、時間エントリの下書きにコピーされる予約を明示的に選択することができます。</span><span class="sxs-lookup"><span data-stu-id="fb1b9-193">You can specify the date range that bookings are imported from and then explicitly select the bookings that should be copied into draft time entries.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
