---
title: 刷新された経費報告書
description: このトピックでは、経費精算書エントリの再設計および再考されたエクスペリエンスについて説明しています。
author: suvaidya
manager: AnnBe
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 79e6a407689813f8c87fdffba0cda84df10d3b83
ms.sourcegitcommit: 46726e5c8c994735c1e570e08d6ed8f9c9341319
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2021
ms.locfileid: "5717701"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="af4cb-103">刷新された経費報告書</span><span class="sxs-lookup"><span data-stu-id="af4cb-103">Expense reports reimagined</span></span>

<span data-ttu-id="af4cb-104">経費報告書のエントリが、プロセスを簡素化し、レポートを完成するのにかかる時間を短縮するように再設計されました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-104">Expense report entry has been redesigned to simplify the process and reduce the time needed to complete a report.</span></span> <span data-ttu-id="af4cb-105">新しい経費エクスペリエンスの主要コンポーネントは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="af4cb-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="af4cb-106">代理人の経費にアクセスできる新しい経費管理ワークスペース。</span><span class="sxs-lookup"><span data-stu-id="af4cb-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="af4cb-107">ヘッダーレベルの領収書をより適切に表示し、経費明細に領収書を添付するプロセスを簡素化する新しい領収書照合エクスペリエンス。</span><span class="sxs-lookup"><span data-stu-id="af4cb-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="af4cb-108">より多くの経費明細および追加のデータ列を表示できる新しい読み取り専用グリッド。</span><span class="sxs-lookup"><span data-stu-id="af4cb-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="af4cb-109">これで、すべての項目別および分割された行が、それらの親経費とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="af4cb-110">経費を編集するための簡素化されたペイン。</span><span class="sxs-lookup"><span data-stu-id="af4cb-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="af4cb-111">エラー、警告、およびポリシーメッセージを再設計して、問題の正しいコンテキストと解釈、およびその解決方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="af4cb-111">Redesigned error, warning, and policy messages to provide the correct context and understanding of the issue and how to resolve it.</span></span> <span data-ttu-id="af4cb-112">ユーザーがタスクを完了して問題に対処する前に表示されるメッセージのいくつかを削除しました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-112">We have removed several of the messages that appeared before users could complete their tasks and address the issues.</span></span>
- <span data-ttu-id="af4cb-113">必須フィールド、オプション フィールド、および含めるべきではないフィールドを指定するための新しいページ。</span><span class="sxs-lookup"><span data-stu-id="af4cb-113">A new page to specify required fields, optional fields, and the fields that should not be included.</span></span> <span data-ttu-id="af4cb-114">このページは、設定する必要のあるフィールドの数を削減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-114">This page helps to reduce the number of fields that must be set.</span></span>
- <span data-ttu-id="af4cb-115">経費報告書の新しいルック アンド フィールにより、報告書は会計ペルソナ用に設計されたかのようには見えなくなります。</span><span class="sxs-lookup"><span data-stu-id="af4cb-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="af4cb-116">新しいエクスペリエンスを有効にするには、**機能管理** ワークスペースを使用して、**刷新された経費報告書** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="af4cb-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports reimagined** feature.</span></span> <span data-ttu-id="af4cb-117">この機能を有効にすると、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="af4cb-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="af4cb-118">既存の経費ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="af4cb-119">経費フィールドの表示に使用する新たなメニュー項目が追加されました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="af4cb-120">経費報告書 (既存のページ) または経費報告書フィールドの既存のメニュー項目が削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="af4cb-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="af4cb-121">ワークフローや承認では、既存の経費報告書のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="af4cb-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a><span data-ttu-id="af4cb-122">新機能</span><span class="sxs-lookup"><span data-stu-id="af4cb-122">New features</span></span>

| <span data-ttu-id="af4cb-123">新機能</span><span class="sxs-lookup"><span data-stu-id="af4cb-123">New feature</span></span> | <span data-ttu-id="af4cb-124">内容</span><span class="sxs-lookup"><span data-stu-id="af4cb-124">Description</span></span> |
|---|----|
| <span data-ttu-id="af4cb-125">経費フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="af4cb-125">Expense field visibility</span></span> | <span data-ttu-id="af4cb-126">新しい設定ページでは、組織でどのフィールドを無効にするか、どのフィールドを必要とするか、およびどのフィールドを推奨するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-126">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="af4cb-127">必須フィールド</span><span class="sxs-lookup"><span data-stu-id="af4cb-127">Required fields</span></span> | <span data-ttu-id="af4cb-128">新しい簡単な構成により、ポリシー フレームワークを使用せずに一部のフィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-128">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="af4cb-129">オプション フィールド</span><span class="sxs-lookup"><span data-stu-id="af4cb-129">Optional fields</span></span> | <span data-ttu-id="af4cb-130">オプション フィールドの 2 番目のページが追加されました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-130">A second page for optional fields is added.</span></span> <span data-ttu-id="af4cb-131">これにより、従業員はフィールドを設定する必要があるように感じることはありませんが、フィールドには引き続き簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-131">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="af4cb-132">添付されていない領収書の追加</span><span class="sxs-lookup"><span data-stu-id="af4cb-132">Add unattached receipts</span></span> | <span data-ttu-id="af4cb-133">添付されていない領収書を経費報告書に追加する機能は、ワークスペースからおよび経費報告書でより見やすくなります。</span><span class="sxs-lookup"><span data-stu-id="af4cb-133">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="af4cb-134">改善されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="af4cb-134">Improved messaging</span></span> | <span data-ttu-id="af4cb-135">警告またはエラーのある経費明細をより的確に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-135">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="af4cb-136">メッセージ バーのメッセージの削減</span><span class="sxs-lookup"><span data-stu-id="af4cb-136">Reduction in messages in the message bar</span></span>| <span data-ttu-id="af4cb-137">情報ログ メッセージの数を減らし、重複したメッセージが多くの場合に表示されないようにする努力がなされました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-137">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="af4cb-138">共通の操作をグループ化</span><span class="sxs-lookup"><span data-stu-id="af4cb-138">Grouped together common actions</span></span> | <span data-ttu-id="af4cb-139">インターフェースは、ほとんどの共通の明細行レベルのアクション用の新しいアクション ボタンの追加と、ヘッダーおよびその他の頻度の低いアクション用の省略記号ボタン (...) の追加でクリーンアップされました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-139">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="af4cb-140">可視性を向上する新しいワークスペース</span><span class="sxs-lookup"><span data-stu-id="af4cb-140">New workspace to increase visibility</span></span> | <span data-ttu-id="af4cb-141">新しいワークスペースは、ユーザーがさまざまな領域に移動できるようにする機能およびリンクを統合します。</span><span class="sxs-lookup"><span data-stu-id="af4cb-141">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="af4cb-142">経費作成時の既存の経費および領収書の追加</span><span class="sxs-lookup"><span data-stu-id="af4cb-142">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="af4cb-143">経費精算書を作成する際、すべての経費を追加するか、添付されていない経費を選択できます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-143">When you create expense reports, you can add all expenses, or select unattached expenses.</span></span> <span data-ttu-id="af4cb-144">添付されていない経費とは、企業のクレジット カード フィードからインポートされた経費、またはユーザーが手動で作成したが経費精算書に添付されていない経費のことです。</span><span class="sxs-lookup"><span data-stu-id="af4cb-144">Unattached expenses are expenses that were imported from the corporate credit card feed or expenses that were manually created by the user but haven't been attached to an expense report.</span></span>|
| <span data-ttu-id="af4cb-145">為替レート計算機</span><span class="sxs-lookup"><span data-stu-id="af4cb-145">Exchange rate calculator</span></span> | <span data-ttu-id="af4cb-146">自己負担した複数通貨トランザクションの為替レートを計算できる為替レート計算機が追加されました。</span><span class="sxs-lookup"><span data-stu-id="af4cb-146">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="af4cb-147">新しい経費明細の保存および追加</span><span class="sxs-lookup"><span data-stu-id="af4cb-147">Save and add new expense lines</span></span> | <span data-ttu-id="af4cb-148">**保存** および **新規** ボタンは新しい経費を入力するときに使用でき、経費明細をすばやく入力するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-148">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="af4cb-149">分割および項目別された行の可視性の向上</span><span class="sxs-lookup"><span data-stu-id="af4cb-149">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="af4cb-150">項目別および分割された行は経費のリストに直接追加され、可視性を向上し、エラーがあるかどうかを簡単に判断するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-150">Itemized and split lines are added directly to the list of expenses to increase visibility and help you easily determine whether there are any errors.</span></span> |
| <span data-ttu-id="af4cb-151">項目別化中に領収書を表示する</span><span class="sxs-lookup"><span data-stu-id="af4cb-151">Show receipts during itemization</span></span> | <span data-ttu-id="af4cb-152">領収書は項目別化中に表示できます。</span><span class="sxs-lookup"><span data-stu-id="af4cb-152">Receipts can be shown during itemization.</span></span> |
| <span data-ttu-id="af4cb-153">現金前払いの選択</span><span class="sxs-lookup"><span data-stu-id="af4cb-153">Cash advance selection</span></span> | <span data-ttu-id="af4cb-154">単一の経費トランザクションを実行するために、1 つ以上の現金前払いを選択します。</span><span class="sxs-lookup"><span data-stu-id="af4cb-154">Select one or more cash advances for fulfilling a single expense transaction.</span></span> |
| <span data-ttu-id="af4cb-155">現金前払い残高</span><span class="sxs-lookup"><span data-stu-id="af4cb-155">Cash advance balance</span></span> | <span data-ttu-id="af4cb-156">承認済みかつ支払済み現金前払いに対して経費エントリを作成する際に、現金前払い残高をリアルタイムでレビューします。</span><span class="sxs-lookup"><span data-stu-id="af4cb-156">Review the cash advance balance in real time when you create an expense entry against approved and paid cash advances.</span></span> |

<span data-ttu-id="af4cb-157">最初のリリースは、経費入力シナリオに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="af4cb-157">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="af4cb-158">経費報告書のレビューまたは承認シナリオでは、引き続き既存の経費入力ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="af4cb-158">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="af4cb-159">次の機能は、[再考された経費ワークスペース] ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="af4cb-159">The following features aren't supported on the Reimagined Expense Workspace:</span></span>

- <span data-ttu-id="af4cb-160">出張費要求の統合</span><span class="sxs-lookup"><span data-stu-id="af4cb-160">Travel requisition integration</span></span>
- <span data-ttu-id="af4cb-161">日当費用エントリ</span><span class="sxs-lookup"><span data-stu-id="af4cb-161">Per diem expense entry</span></span>
- <span data-ttu-id="af4cb-162">中間承認者のサポート</span><span class="sxs-lookup"><span data-stu-id="af4cb-162">Interim approver support</span></span>
- <span data-ttu-id="af4cb-163">ワークフロー履歴を表示する機能</span><span class="sxs-lookup"><span data-stu-id="af4cb-163">Ability to view workflow history</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
