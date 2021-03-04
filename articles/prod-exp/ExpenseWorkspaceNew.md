---
title: 再設計された経費報告書
description: このトピックでは、Microsoft Dynamics 365 Finance における経費報告書エントリの再設計および刷新されたエクスペリエンスに関する情報を提供します。 新しいエクスペリエンスにより、経費報告書を完成させるプロセスが簡素化され、所用時間が短縮されます。
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d076c0a596940cb08433f7ee57dea54903f6078f
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960253"
---
# <a name="redesigned-expense-reports"></a><span data-ttu-id="f85e1-104">再設計された経費報告書</span><span class="sxs-lookup"><span data-stu-id="f85e1-104">Redesigned expense reports</span></span>

<span data-ttu-id="f85e1-105">経費報告書の入力を一新され、経費報告書の記入作業を簡素化し、所要時間を短縮しました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="f85e1-106">新しい経費エクスペリエンスの主要コンポーネントは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f85e1-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="f85e1-107">代理人の経費にアクセスできる新しい経費管理ワークスペース。</span><span class="sxs-lookup"><span data-stu-id="f85e1-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="f85e1-108">ヘッダーレベルの領収書をより適切に表示し、経費明細に領収書を添付するプロセスを簡素化する新しい領収書照合エクスペリエンス。</span><span class="sxs-lookup"><span data-stu-id="f85e1-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="f85e1-109">より多くの経費明細および追加のデータ列を表示できる新しい読み取り専用グリッド。</span><span class="sxs-lookup"><span data-stu-id="f85e1-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="f85e1-110">これで、すべての項目別および分割された行が、それらの親経費とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="f85e1-111">経費を編集するための簡素化されたペイン。</span><span class="sxs-lookup"><span data-stu-id="f85e1-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="f85e1-112">エラー、警告、方針のメッセージを再設計されており、問題の内容と解決方法を理解するための正しいコンテキストが保証されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="f85e1-113">Microsoft は、ユーザーがタスクを完了して問題に対処する機会を得る前に表示された、不完全な項目化メッセージなどの多くのメッセージを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="f85e1-114">組織でどのフィールドが必要か、どのフィールドが任意か、どのフィールドをキャプチャしてはいけないかを指定する新たなページが導入されています。</span><span class="sxs-lookup"><span data-stu-id="f85e1-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="f85e1-115">このページでは、ユーザーが設定しなければならないフィールドの数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="f85e1-116">経費報告書の新しいルック アンド フィールにより、報告書は会計ペルソナ用に設計されたかのようには見えなくなります。</span><span class="sxs-lookup"><span data-stu-id="f85e1-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="f85e1-117">新しいエクスペリエンスをオンにするには、**機能管理** ワークスペースを使用して、**新しくなった経費報告書** 機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="f85e1-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="f85e1-118">この機能を有効にすると、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="f85e1-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="f85e1-119">既存の経費ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="f85e1-120">経費フィールドの表示に使用する新たなメニュー項目が追加されました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="f85e1-121">経費報告書 (既存のページ) または経費報告書フィールドの既存のメニュー項目が削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="f85e1-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="f85e1-122">ワークフローや承認では、既存の経費報告書のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="f85e1-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="f85e1-123">新しいユーザー向けの作業の開始に関するビデオ</span><span class="sxs-lookup"><span data-stu-id="f85e1-123">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="f85e1-124">[Dynamics 365 for Finance and Operations での経費エクスペリエンス](https://youtu.be/Ocy-MsTvEE0) ビデオ (上に表示) は、YouTube で使用可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="f85e1-124">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="f85e1-125">新機能</span><span class="sxs-lookup"><span data-stu-id="f85e1-125">New features</span></span>

| <span data-ttu-id="f85e1-126">新機能</span><span class="sxs-lookup"><span data-stu-id="f85e1-126">New feature</span></span> | <span data-ttu-id="f85e1-127">内容</span><span class="sxs-lookup"><span data-stu-id="f85e1-127">Description</span></span> |
|---|----|
| <span data-ttu-id="f85e1-128">経費フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="f85e1-128">Expense field visibility</span></span> | <span data-ttu-id="f85e1-129">新しい設定ページでは、組織でどのフィールドを無効にするか、どのフィールドを必要とするか、およびどのフィールドを推奨するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-129">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="f85e1-130">必須フィールド</span><span class="sxs-lookup"><span data-stu-id="f85e1-130">Required fields</span></span> | <span data-ttu-id="f85e1-131">新しい簡単な構成により、ポリシー フレームワークを使用せずに一部のフィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-131">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="f85e1-132">オプション フィールド</span><span class="sxs-lookup"><span data-stu-id="f85e1-132">Optional fields</span></span> | <span data-ttu-id="f85e1-133">オプション フィールドの 2 番目のページが追加されました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-133">A second page for optional fields is added.</span></span> <span data-ttu-id="f85e1-134">これにより、従業員はフィールドを設定する必要があるように感じることはありませんが、フィールドには引き続き簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-134">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="f85e1-135">添付されていない領収書の追加</span><span class="sxs-lookup"><span data-stu-id="f85e1-135">Add unattached receipts</span></span> | <span data-ttu-id="f85e1-136">添付されていない領収書を経費報告書に追加する機能は、ワークスペースからおよび経費報告書でより見やすくなります。</span><span class="sxs-lookup"><span data-stu-id="f85e1-136">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="f85e1-137">改善されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="f85e1-137">Improved messaging</span></span> | <span data-ttu-id="f85e1-138">警告またはエラーのある経費明細をより的確に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-138">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="f85e1-139">メッセージ バーのメッセージの削減</span><span class="sxs-lookup"><span data-stu-id="f85e1-139">Reduction in messages in the message bar</span></span>| <span data-ttu-id="f85e1-140">情報ログ メッセージの数を減らし、重複したメッセージが多くの場合に表示されないようにする努力がなされました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-140">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="f85e1-141">共通の操作をグループ化</span><span class="sxs-lookup"><span data-stu-id="f85e1-141">Grouped together common actions</span></span> | <span data-ttu-id="f85e1-142">インターフェースは、ほとんどの共通の明細行レベルのアクション用の新しいアクション ボタンの追加と、ヘッダーおよびその他の頻度の低いアクション用の省略記号ボタン (...) の追加でクリーンアップされました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-142">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="f85e1-143">可視性を向上する新しいワークスペース</span><span class="sxs-lookup"><span data-stu-id="f85e1-143">New workspace to increase visibility</span></span> | <span data-ttu-id="f85e1-144">新しいワークスペースは、ユーザーがさまざまな領域に移動できるようにする機能およびリンクを統合します。</span><span class="sxs-lookup"><span data-stu-id="f85e1-144">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="f85e1-145">経費作成時の既存の経費および領収書の追加</span><span class="sxs-lookup"><span data-stu-id="f85e1-145">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="f85e1-146">経費報告書を作成するときに、全てまたは選択した経費および領収書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-146">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="f85e1-147">為替レート計算機</span><span class="sxs-lookup"><span data-stu-id="f85e1-147">Exchange rate calculator</span></span> | <span data-ttu-id="f85e1-148">自己負担した複数通貨トランザクションの為替レートを計算できる為替レート計算機が追加されました。</span><span class="sxs-lookup"><span data-stu-id="f85e1-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="f85e1-149">新しい経費明細の保存および追加</span><span class="sxs-lookup"><span data-stu-id="f85e1-149">Save and add new expense lines</span></span> | <span data-ttu-id="f85e1-150">**保存** および **新規** ボタンは新しい経費を入力するときに使用でき、経費明細をすばやく入力するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="f85e1-151">分割および項目別された行の可視性の向上</span><span class="sxs-lookup"><span data-stu-id="f85e1-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="f85e1-152">箇条書きや分割線を直接経費の一覧に追加することで、視認性を高め、方針ミスなどの誤りがないかどうかを簡単に判断できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f85e1-152">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="f85e1-153">項目別化中に領収書を表示する</span><span class="sxs-lookup"><span data-stu-id="f85e1-153">Show receipts during itemization</span></span> | <span data-ttu-id="f85e1-154">領収書は項目別化中に表示できます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-154">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="f85e1-155">最初のリリースは、経費入力シナリオに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="f85e1-155">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="f85e1-156">経費報告書のレビューまたは承認シナリオでは、引き続き既存の経費入力ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="f85e1-156">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="f85e1-157">次の機能は既存のページには含まれていますが、新しいページにはまだ含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f85e1-157">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="f85e1-158">これらの機能は、次のいくつかのリリースで再導入されます。</span><span class="sxs-lookup"><span data-stu-id="f85e1-158">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="f85e1-159">承認</span><span class="sxs-lookup"><span data-stu-id="f85e1-159">Approvals</span></span>
- <span data-ttu-id="f85e1-160">買掛金勘定の承認および会計を編集する機能</span><span class="sxs-lookup"><span data-stu-id="f85e1-160">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="f85e1-161">複数のエントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="f85e1-161">Multiple entry points</span></span>
- <span data-ttu-id="f85e1-162">出張費要求の統合</span><span class="sxs-lookup"><span data-stu-id="f85e1-162">Travel requisition integration</span></span>
- <span data-ttu-id="f85e1-163">経費フィールドの可視性のためのデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="f85e1-163">Data entity for expense field visibility</span></span>
- <span data-ttu-id="f85e1-164">日当経費の入力</span><span class="sxs-lookup"><span data-stu-id="f85e1-164">Entry for per-diem expenses</span></span>
- <span data-ttu-id="f85e1-165">明細行レベルのワークフロー</span><span class="sxs-lookup"><span data-stu-id="f85e1-165">Line-level workflow</span></span>
- <span data-ttu-id="f85e1-166">中間承認者のサポート</span><span class="sxs-lookup"><span data-stu-id="f85e1-166">Interim approver support</span></span>
- <span data-ttu-id="f85e1-167">詳細項目別化</span><span class="sxs-lookup"><span data-stu-id="f85e1-167">Advanced itemization</span></span>
