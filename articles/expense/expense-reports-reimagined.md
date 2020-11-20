---
title: 刷新された経費報告書
description: このトピックでは、経費報告書エントリの再設計および刷新されたエクスペリエンスに関する情報を提供します。
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122800"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="cabe8-103">刷新された経費報告書</span><span class="sxs-lookup"><span data-stu-id="cabe8-103">Expense reports reimagined</span></span>

<span data-ttu-id="cabe8-104">経費報告書のエントリが、プロセスを簡素化し、レポートを完成するのにかかる時間を短縮するように再設計されました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-104">Expense report entry has been redesigned to simplify the process and reduce the time needed to complete a report.</span></span> <span data-ttu-id="cabe8-105">新しい経費エクスペリエンスの主要コンポーネントは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cabe8-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="cabe8-106">代理人の経費にアクセスできる新しい経費管理ワークスペース。</span><span class="sxs-lookup"><span data-stu-id="cabe8-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="cabe8-107">ヘッダーレベルの領収書をより適切に表示し、経費明細に領収書を添付するプロセスを簡素化する新しい領収書照合エクスペリエンス。</span><span class="sxs-lookup"><span data-stu-id="cabe8-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="cabe8-108">より多くの経費明細および追加のデータ列を表示できる新しい読み取り専用グリッド。</span><span class="sxs-lookup"><span data-stu-id="cabe8-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="cabe8-109">これで、すべての項目別および分割された行が、それらの親経費とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="cabe8-110">経費を編集するための簡素化されたペイン。</span><span class="sxs-lookup"><span data-stu-id="cabe8-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="cabe8-111">エラー、警告、およびポリシーメッセージを再設計して、問題の正しいコンテキストと解釈、およびその解決方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="cabe8-111">Redesigned error, warning, and policy messages to provide the correct context and understanding of the issue and how to resolve it.</span></span> <span data-ttu-id="cabe8-112">ユーザーがタスクを完了して問題に対処する前に表示されるメッセージのいくつかを削除しました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-112">We have removed several of the messages that appeared before users could complete their tasks and address the issues.</span></span>
- <span data-ttu-id="cabe8-113">必須フィールド、オプション フィールド、および含めるべきではないフィールドを指定するための新しいページ。</span><span class="sxs-lookup"><span data-stu-id="cabe8-113">A new page to specify required fields, optional fields, and the fields that should not be included.</span></span> <span data-ttu-id="cabe8-114">このページは、設定する必要のあるフィールドの数を削減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-114">This page helps to reduce the number of fields that must be set.</span></span>
- <span data-ttu-id="cabe8-115">経費報告書の新しいルック アンド フィールにより、報告書は会計ペルソナ用に設計されたかのようには見えなくなります。</span><span class="sxs-lookup"><span data-stu-id="cabe8-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="cabe8-116">新しいエクスペリエンスを有効にするには、**機能管理** ワークスペースを使用して、**刷新された経費報告書** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="cabe8-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports reimagined** feature.</span></span> <span data-ttu-id="cabe8-117">この機能を有効にすると、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="cabe8-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="cabe8-118">既存の経費ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="cabe8-119">経費フィールドの表示に使用する新たなメニュー項目が追加されました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="cabe8-120">経費報告書 (既存のページ) または経費報告書フィールドの既存のメニュー項目が削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="cabe8-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="cabe8-121">ワークフローや承認では、既存の経費報告書のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="cabe8-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="cabe8-122">新しいユーザー向けの作業の開始に関するビデオ</span><span class="sxs-lookup"><span data-stu-id="cabe8-122">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="cabe8-123">[Dynamics 365 for Finance and Operations での経費エクスペリエンス](https://youtu.be/Ocy-MsTvEE0) ビデオ (上に表示) は、YouTube で使用可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="cabe8-123">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="cabe8-124">新機能</span><span class="sxs-lookup"><span data-stu-id="cabe8-124">New features</span></span>

| <span data-ttu-id="cabe8-125">新機能</span><span class="sxs-lookup"><span data-stu-id="cabe8-125">New feature</span></span> | <span data-ttu-id="cabe8-126">内容</span><span class="sxs-lookup"><span data-stu-id="cabe8-126">Description</span></span> |
|---|----|
| <span data-ttu-id="cabe8-127">経費フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="cabe8-127">Expense field visibility</span></span> | <span data-ttu-id="cabe8-128">新しい設定ページでは、組織でどのフィールドを無効にするか、どのフィールドを必要とするか、およびどのフィールドを推奨するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-128">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="cabe8-129">必須フィールド</span><span class="sxs-lookup"><span data-stu-id="cabe8-129">Required fields</span></span> | <span data-ttu-id="cabe8-130">新しい簡単な構成により、ポリシー フレームワークを使用せずに一部のフィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-130">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="cabe8-131">オプション フィールド</span><span class="sxs-lookup"><span data-stu-id="cabe8-131">Optional fields</span></span> | <span data-ttu-id="cabe8-132">オプション フィールドの 2 番目のページが追加されました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-132">A second page for optional fields is added.</span></span> <span data-ttu-id="cabe8-133">これにより、従業員はフィールドを設定する必要があるように感じることはありませんが、フィールドには引き続き簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-133">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="cabe8-134">添付されていない領収書の追加</span><span class="sxs-lookup"><span data-stu-id="cabe8-134">Add unattached receipts</span></span> | <span data-ttu-id="cabe8-135">添付されていない領収書を経費報告書に追加する機能は、ワークスペースからおよび経費報告書でより見やすくなります。</span><span class="sxs-lookup"><span data-stu-id="cabe8-135">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="cabe8-136">改善されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="cabe8-136">Improved messaging</span></span> | <span data-ttu-id="cabe8-137">警告またはエラーのある経費明細をより的確に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-137">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="cabe8-138">メッセージ バーのメッセージの削減</span><span class="sxs-lookup"><span data-stu-id="cabe8-138">Reduction in messages in the message bar</span></span>| <span data-ttu-id="cabe8-139">情報ログ メッセージの数を減らし、重複したメッセージが多くの場合に表示されないようにする努力がなされました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-139">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="cabe8-140">共通の操作をグループ化</span><span class="sxs-lookup"><span data-stu-id="cabe8-140">Grouped together common actions</span></span> | <span data-ttu-id="cabe8-141">インターフェースは、ほとんどの共通の明細行レベルのアクション用の新しいアクション ボタンの追加と、ヘッダーおよびその他の頻度の低いアクション用の省略記号ボタン (...) の追加でクリーンアップされました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-141">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="cabe8-142">可視性を向上する新しいワークスペース</span><span class="sxs-lookup"><span data-stu-id="cabe8-142">New workspace to increase visibility</span></span> | <span data-ttu-id="cabe8-143">新しいワークスペースは、ユーザーがさまざまな領域に移動できるようにする機能およびリンクを統合します。</span><span class="sxs-lookup"><span data-stu-id="cabe8-143">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="cabe8-144">経費作成時の既存の経費および領収書の追加</span><span class="sxs-lookup"><span data-stu-id="cabe8-144">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="cabe8-145">経費報告書を作成するときに、全てまたは選択した経費および領収書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-145">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="cabe8-146">為替レート計算機</span><span class="sxs-lookup"><span data-stu-id="cabe8-146">Exchange rate calculator</span></span> | <span data-ttu-id="cabe8-147">自己負担した複数通貨トランザクションの為替レートを計算できる為替レート計算機が追加されました。</span><span class="sxs-lookup"><span data-stu-id="cabe8-147">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="cabe8-148">新しい経費明細の保存および追加</span><span class="sxs-lookup"><span data-stu-id="cabe8-148">Save and add new expense lines</span></span> | <span data-ttu-id="cabe8-149">**保存** および **新規** ボタンは新しい経費を入力するときに使用でき、経費明細をすばやく入力するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-149">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="cabe8-150">分割および項目別された行の可視性の向上</span><span class="sxs-lookup"><span data-stu-id="cabe8-150">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="cabe8-151">項目別および分割された行は経費のリストに直接追加され、可視性を向上し、エラーがあるかどうかを簡単に判断するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-151">Itemized and split lines are added directly to the list of expenses to increase visibility and help you easily determine whether there are any errors.</span></span> |
| <span data-ttu-id="cabe8-152">項目別化中に領収書を表示する</span><span class="sxs-lookup"><span data-stu-id="cabe8-152">Show receipts during itemization</span></span> | <span data-ttu-id="cabe8-153">領収書は項目別化中に表示できます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-153">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="cabe8-154">最初のリリースは、経費入力シナリオに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="cabe8-154">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="cabe8-155">経費報告書のレビューまたは承認シナリオでは、引き続き既存の経費入力ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="cabe8-155">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="cabe8-156">次の機能は既存のページには含まれていますが、新しいページにはまだ含まれていません。</span><span class="sxs-lookup"><span data-stu-id="cabe8-156">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="cabe8-157">これらの機能は、次のいくつかのリリースで再導入されます。</span><span class="sxs-lookup"><span data-stu-id="cabe8-157">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="cabe8-158">承認</span><span class="sxs-lookup"><span data-stu-id="cabe8-158">Approvals</span></span>
- <span data-ttu-id="cabe8-159">買掛金勘定の承認および会計を編集する機能</span><span class="sxs-lookup"><span data-stu-id="cabe8-159">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="cabe8-160">複数のエントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="cabe8-160">Multiple entry points</span></span>
- <span data-ttu-id="cabe8-161">出張費要求の統合</span><span class="sxs-lookup"><span data-stu-id="cabe8-161">Travel requisition integration</span></span>
- <span data-ttu-id="cabe8-162">経費フィールドの可視性のためのデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="cabe8-162">Data entity for expense field visibility</span></span>
- <span data-ttu-id="cabe8-163">日当経費の入力</span><span class="sxs-lookup"><span data-stu-id="cabe8-163">Entry for per-diem expenses</span></span>
- <span data-ttu-id="cabe8-164">明細行レベルのワークフロー</span><span class="sxs-lookup"><span data-stu-id="cabe8-164">Line-level workflow</span></span>
- <span data-ttu-id="cabe8-165">中間承認者のサポート</span><span class="sxs-lookup"><span data-stu-id="cabe8-165">Interim approver support</span></span>
- <span data-ttu-id="cabe8-166">詳細項目別化</span><span class="sxs-lookup"><span data-stu-id="cabe8-166">Advanced itemization</span></span>
