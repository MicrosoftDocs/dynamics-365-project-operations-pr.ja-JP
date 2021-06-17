---
title: 再設計された経費報告書
description: このトピックでは、経費報告書エントリの再設計および刷新されたエクスペリエンスに関する情報を提供します。
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: bd334d3404e9baae4f8314173834d9fbb708d574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993693"
---
# <a name="redesigned-expense-reports"></a><span data-ttu-id="2f3b7-103">再設計された経費報告書</span><span class="sxs-lookup"><span data-stu-id="2f3b7-103">Redesigned expense reports</span></span>

<span data-ttu-id="2f3b7-104">経費報告書の入力を一新され、経費報告書の記入作業を簡素化し、所要時間を短縮しました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-104">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="2f3b7-105">新しい経費エクスペリエンスの主要コンポーネントは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="2f3b7-106">代理人の経費にアクセスできる新しい経費管理ワークスペース。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="2f3b7-107">ヘッダーレベルの領収書をより適切に表示し、経費明細に領収書を添付するプロセスを簡素化する新しい領収書照合エクスペリエンス。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="2f3b7-108">より多くの経費明細および追加のデータ列を表示できる新しい読み取り専用グリッド。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="2f3b7-109">これで、すべての項目別および分割された行が、それらの親経費とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="2f3b7-110">経費を編集するための簡素化されたペイン。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="2f3b7-111">エラー、警告、方針のメッセージを再設計されており、問題の内容と解決方法を理解するための正しいコンテキストが保証されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-111">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="2f3b7-112">Microsoft は、ユーザーがタスクを完了して問題に対処する機会を得る前に表示された、不完全な項目化メッセージなどの多くのメッセージを削除しました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-112">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="2f3b7-113">組織でどのフィールドが必要か、どのフィールドが任意か、どのフィールドをキャプチャしてはいけないかを指定する新たなページが導入されています。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-113">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="2f3b7-114">このページでは、ユーザーが設定しなければならないフィールドの数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-114">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="2f3b7-115">経費報告書の新しいルック アンド フィールにより、報告書は会計ペルソナ用に設計されたかのようには見えなくなります。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="2f3b7-116">新しいエクスペリエンスをオンにするには、**機能管理** ワークスペースを使用して、**新しくなった経費報告書** 機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="2f3b7-117">この機能を有効にすると、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="2f3b7-118">既存の経費ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2f3b7-119">経費フィールドの表示に使用する新たなメニュー項目が追加されました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2f3b7-120">経費報告書 (既存のページ) または経費報告書フィールドの既存のメニュー項目が削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="2f3b7-121">ワークフローや承認では、既存の経費報告書のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="new-features"></a><span data-ttu-id="2f3b7-122">新機能</span><span class="sxs-lookup"><span data-stu-id="2f3b7-122">New features</span></span>

| <span data-ttu-id="2f3b7-123">新機能</span><span class="sxs-lookup"><span data-stu-id="2f3b7-123">New feature</span></span> | <span data-ttu-id="2f3b7-124">内容</span><span class="sxs-lookup"><span data-stu-id="2f3b7-124">Description</span></span> |
|---|----|
| <span data-ttu-id="2f3b7-125">経費フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="2f3b7-125">Expense field visibility</span></span> | <span data-ttu-id="2f3b7-126">新しい設定ページでは、組織でどのフィールドを無効にするか、どのフィールドを必要とするか、およびどのフィールドを推奨するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-126">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="2f3b7-127">必須フィールド</span><span class="sxs-lookup"><span data-stu-id="2f3b7-127">Required fields</span></span> | <span data-ttu-id="2f3b7-128">新しい簡単な構成により、ポリシー フレームワークを使用せずに一部のフィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-128">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="2f3b7-129">オプション フィールド</span><span class="sxs-lookup"><span data-stu-id="2f3b7-129">Optional fields</span></span> | <span data-ttu-id="2f3b7-130">オプション フィールドの 2 番目のページが追加されました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-130">A second page for optional fields is added.</span></span> <span data-ttu-id="2f3b7-131">これにより、従業員はフィールドを設定する必要があるように感じることはありませんが、フィールドには引き続き簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-131">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="2f3b7-132">添付されていない領収書の追加</span><span class="sxs-lookup"><span data-stu-id="2f3b7-132">Add unattached receipts</span></span> | <span data-ttu-id="2f3b7-133">添付されていない領収書を経費報告書に追加する機能は、ワークスペースからおよび経費報告書でより見やすくなります。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-133">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="2f3b7-134">改善されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="2f3b7-134">Improved messaging</span></span> | <span data-ttu-id="2f3b7-135">警告またはエラーのある経費明細をより的確に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-135">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="2f3b7-136">メッセージ バーのメッセージの削減</span><span class="sxs-lookup"><span data-stu-id="2f3b7-136">Reduction in messages in the message bar</span></span>| <span data-ttu-id="2f3b7-137">情報ログ メッセージの数を減らし、重複したメッセージが多くの場合に表示されないようにする努力がなされました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-137">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="2f3b7-138">共通の操作をグループ化</span><span class="sxs-lookup"><span data-stu-id="2f3b7-138">Grouped together common actions</span></span> | <span data-ttu-id="2f3b7-139">インターフェースは、ほとんどの共通の明細行レベルのアクション用の新しいアクション ボタンの追加と、ヘッダーおよびその他の頻度の低いアクション用の省略記号ボタン (...) の追加でクリーンアップされました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-139">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="2f3b7-140">可視性を向上する新しいワークスペース</span><span class="sxs-lookup"><span data-stu-id="2f3b7-140">New workspace to increase visibility</span></span> | <span data-ttu-id="2f3b7-141">新しいワークスペースは、ユーザーがさまざまな領域に移動できるようにする機能およびリンクを統合します。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-141">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="2f3b7-142">経費作成時の既存の経費および領収書の追加</span><span class="sxs-lookup"><span data-stu-id="2f3b7-142">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="2f3b7-143">経費報告書を作成するときに、全てまたは選択した経費および領収書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-143">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="2f3b7-144">為替レート計算機</span><span class="sxs-lookup"><span data-stu-id="2f3b7-144">Exchange rate calculator</span></span> | <span data-ttu-id="2f3b7-145">自己負担した複数通貨トランザクションの為替レートを計算できる為替レート計算機が追加されました。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-145">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="2f3b7-146">新しい経費明細の保存および追加</span><span class="sxs-lookup"><span data-stu-id="2f3b7-146">Save and add new expense lines</span></span> | <span data-ttu-id="2f3b7-147">**保存** および **新規** ボタンは新しい経費を入力するときに使用でき、経費明細をすばやく入力するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-147">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="2f3b7-148">分割および項目別された行の可視性の向上</span><span class="sxs-lookup"><span data-stu-id="2f3b7-148">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="2f3b7-149">箇条書きや分割線を直接経費の一覧に追加することで、視認性を高め、方針ミスなどの誤りがないかどうかを簡単に判断できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-149">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="2f3b7-150">項目別化中に領収書を表示する</span><span class="sxs-lookup"><span data-stu-id="2f3b7-150">Show receipts during itemization</span></span> | <span data-ttu-id="2f3b7-151">領収書は項目別化中に表示できます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-151">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="2f3b7-152">最初のリリースは、経費入力シナリオに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-152">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="2f3b7-153">経費報告書のレビューまたは承認シナリオでは、引き続き既存の経費入力ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-153">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="2f3b7-154">次の機能は既存のページには含まれていますが、新しいページにはまだ含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-154">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="2f3b7-155">これらの機能は、次のいくつかのリリースで再導入されます。</span><span class="sxs-lookup"><span data-stu-id="2f3b7-155">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="2f3b7-156">承認</span><span class="sxs-lookup"><span data-stu-id="2f3b7-156">Approvals</span></span>
- <span data-ttu-id="2f3b7-157">買掛金勘定の承認および会計を編集する機能</span><span class="sxs-lookup"><span data-stu-id="2f3b7-157">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="2f3b7-158">複数のエントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="2f3b7-158">Multiple entry points</span></span>
- <span data-ttu-id="2f3b7-159">出張費要求の統合</span><span class="sxs-lookup"><span data-stu-id="2f3b7-159">Travel requisition integration</span></span>
- <span data-ttu-id="2f3b7-160">経費フィールドの可視性のためのデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="2f3b7-160">Data entity for expense field visibility</span></span>
- <span data-ttu-id="2f3b7-161">日当経費の入力</span><span class="sxs-lookup"><span data-stu-id="2f3b7-161">Entry for per-diem expenses</span></span>
- <span data-ttu-id="2f3b7-162">明細行レベルのワークフロー</span><span class="sxs-lookup"><span data-stu-id="2f3b7-162">Line-level workflow</span></span>
- <span data-ttu-id="2f3b7-163">中間承認者のサポート</span><span class="sxs-lookup"><span data-stu-id="2f3b7-163">Interim approver support</span></span>
- <span data-ttu-id="2f3b7-164">詳細項目別化</span><span class="sxs-lookup"><span data-stu-id="2f3b7-164">Advanced itemization</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]