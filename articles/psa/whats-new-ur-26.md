---
title: Project Service Automation 更新プログラム リリース 26、V3 の新機能と変更点
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643269"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="5893c-102">Project Service Automation 更新プログラム リリース 26、V3</span><span class="sxs-lookup"><span data-stu-id="5893c-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="5893c-103">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="5893c-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5893c-104">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5893c-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5893c-105">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="5893c-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5893c-106">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="5893c-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5893c-107">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5893c-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5893c-108">このトピックには、Project Service Automation 更新プログラム 26 (V3) の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="5893c-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="5893c-109">このバージョンのビルド番号は V3.10.44.59 で、2020 年 12 月のセルフアップデートで一般提供されます。</span><span class="sxs-lookup"><span data-stu-id="5893c-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="5893c-110">更新プログラム 26</span><span class="sxs-lookup"><span data-stu-id="5893c-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="5893c-111">バグの修正</span><span class="sxs-lookup"><span data-stu-id="5893c-111">Bug fixes</span></span>

<span data-ttu-id="5893c-112">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="5893c-112">**Time and Expense**</span></span>

<span data-ttu-id="5893c-113">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="5893c-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5893c-114">ユーザーは承認/送信済みのタイム入力でタスクを変更できます。</span><span class="sxs-lookup"><span data-stu-id="5893c-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="5893c-115">時間入力を保存する際の "オブジェクト参照が設定されていません" エラー。</span><span class="sxs-lookup"><span data-stu-id="5893c-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="5893c-116">リソース割り当てから時間入力をインポートすると、不正な DateTime 値で時間入力が作成されます。</span><span class="sxs-lookup"><span data-stu-id="5893c-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="5893c-117">Project Service Automation と Field Service アプリの両方がインストール済みの場合、Field Service アプリの時間入力のコマンド バーに **新規** ボタンを 2 回表示します。</span><span class="sxs-lookup"><span data-stu-id="5893c-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="5893c-118">**許可単位** と **出荷単位一覧** セルの更新が、現在は **経費の見積もり** グリッドで機能します。</span><span class="sxs-lookup"><span data-stu-id="5893c-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="5893c-119">**タイムライン** を含む **時間入力編集の更新** フォーム。</span><span class="sxs-lookup"><span data-stu-id="5893c-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="5893c-120">非プロジェクト時間入力の時間承認は、プロジェクト承認者ロールの検索時にシステムをブロックします。</span><span class="sxs-lookup"><span data-stu-id="5893c-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="5893c-121">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="5893c-121">**Resource Management**</span></span>

<span data-ttu-id="5893c-122">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="5893c-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5893c-123">**PostProjectCreate** プラグインに検証を追加して、主要な要件を作成する前に確認します。</span><span class="sxs-lookup"><span data-stu-id="5893c-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="5893c-124">フィールドをフォームから削除すると、**プロジェクト チーム メンバー** の簡易作成フォームが null 参照例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5893c-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="5893c-125">1 年間で 12 時間の要件生成は失敗します。</span><span class="sxs-lookup"><span data-stu-id="5893c-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="5893c-126">リソース要件作成での null 参照例外エラー メッセージを改善しました。</span><span class="sxs-lookup"><span data-stu-id="5893c-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="5893c-127">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="5893c-127">**Project Management**</span></span>

<span data-ttu-id="5893c-128">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="5893c-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5893c-129">**PreProjectUpdate** プラグインが生成する null 参照例外に対処する検証を改善しました。</span><span class="sxs-lookup"><span data-stu-id="5893c-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="5893c-130">Microsoft Project デスクトップ アドインで公開したプロジェクトは、未割り当ての割り当てを削除します。</span><span class="sxs-lookup"><span data-stu-id="5893c-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="5893c-131">**PreValidateProjectTaskUpdate** プラグインの null 参照例外が原因でタスクのプロジェクト参照が無効になる際の、新しい検証を追加しました。</span><span class="sxs-lookup"><span data-stu-id="5893c-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="5893c-132">チーム メンバー グリッドにチーム メンバー レコードの個別割り当てを表示しません。</span><span class="sxs-lookup"><span data-stu-id="5893c-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="5893c-133">**PreProjectTaskDelete** プラグインの null 参照例外に起因する、新しい検証とエラー メッセージを追加しました。</span><span class="sxs-lookup"><span data-stu-id="5893c-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="5893c-134">**営業**</span><span class="sxs-lookup"><span data-stu-id="5893c-134">**Sales**</span></span>

<span data-ttu-id="5893c-135">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="5893c-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5893c-136">見積もりや契約でプロジェクト ベースの品目を選択する場合、**提案** ボタンを既存の製品に関連付けられた製品ベースの品目を選択した時だけ表示します。</span><span class="sxs-lookup"><span data-stu-id="5893c-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="5893c-137">**Create_Product** 特権を **Create_ProjectContract** 特権から分割します。</span><span class="sxs-lookup"><span data-stu-id="5893c-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="5893c-138">請求明細行を削除すると **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** で null 参照エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5893c-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
