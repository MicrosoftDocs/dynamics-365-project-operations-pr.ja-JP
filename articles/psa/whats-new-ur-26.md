---
title: Project Service Automation 更新プログラム リリース 26、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 26、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6aafe66fe8c63dc886455a36e93f32d4a581d5cc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005572"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="3f31e-103">Project Service Automation 更新プログラム リリース 26、V3</span><span class="sxs-lookup"><span data-stu-id="3f31e-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3f31e-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="3f31e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3f31e-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f31e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3f31e-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="3f31e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3f31e-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="3f31e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3f31e-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f31e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3f31e-109">このトピックには、Project Service Automation 更新プログラム 26 (V3) の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="3f31e-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="3f31e-110">このバージョンのビルド番号は V3.10.44.59 で、2020 年 12 月のセルフアップデートで一般提供されます。</span><span class="sxs-lookup"><span data-stu-id="3f31e-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="3f31e-111">更新プログラム 26</span><span class="sxs-lookup"><span data-stu-id="3f31e-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3f31e-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="3f31e-112">Bug fixes</span></span>

<span data-ttu-id="3f31e-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="3f31e-113">**Time and Expense**</span></span>

<span data-ttu-id="3f31e-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="3f31e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f31e-115">ユーザーは承認/送信済みのタイム入力でタスクを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3f31e-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="3f31e-116">時間入力を保存する際の "オブジェクト参照が設定されていません" エラー。</span><span class="sxs-lookup"><span data-stu-id="3f31e-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="3f31e-117">リソース割り当てから時間入力をインポートすると、不正な DateTime 値で時間入力が作成されます。</span><span class="sxs-lookup"><span data-stu-id="3f31e-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="3f31e-118">Project Service Automation と Field Service アプリの両方がインストール済みの場合、Field Service アプリの時間入力のコマンド バーに **新規** ボタンを 2 回表示します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="3f31e-119">**許可単位** と **出荷単位一覧** セルの更新が、現在は **経費の見積もり** グリッドで機能します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="3f31e-120">**タイムライン** を含む **時間入力編集の更新** フォーム。</span><span class="sxs-lookup"><span data-stu-id="3f31e-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="3f31e-121">非プロジェクト時間入力の時間承認は、プロジェクト承認者ロールの検索時にシステムをブロックします。</span><span class="sxs-lookup"><span data-stu-id="3f31e-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="3f31e-122">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="3f31e-122">**Resource Management**</span></span>

<span data-ttu-id="3f31e-123">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="3f31e-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f31e-124">**PostProjectCreate** プラグインに検証を追加して、主要な要件を作成する前に確認します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="3f31e-125">フィールドをフォームから削除すると、**プロジェクト チーム メンバー** の簡易作成フォームが null 参照例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="3f31e-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="3f31e-126">1 年間で 12 時間の要件生成は失敗します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="3f31e-127">リソース要件作成での null 参照例外エラー メッセージを改善しました。</span><span class="sxs-lookup"><span data-stu-id="3f31e-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="3f31e-128">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="3f31e-128">**Project Management**</span></span>

<span data-ttu-id="3f31e-129">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="3f31e-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f31e-130">**PreProjectUpdate** プラグインが生成する null 参照例外に対処する検証を改善しました。</span><span class="sxs-lookup"><span data-stu-id="3f31e-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="3f31e-131">Microsoft Project デスクトップ アドインで公開したプロジェクトは、未割り当ての割り当てを削除します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="3f31e-132">**PreValidateProjectTaskUpdate** プラグインの null 参照例外が原因でタスクのプロジェクト参照が無効になる際の、新しい検証を追加しました。</span><span class="sxs-lookup"><span data-stu-id="3f31e-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="3f31e-133">チーム メンバー グリッドにチーム メンバー レコードの個別割り当てを表示しません。</span><span class="sxs-lookup"><span data-stu-id="3f31e-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="3f31e-134">**PreProjectTaskDelete** プラグインの null 参照例外に起因する、新しい検証とエラー メッセージを追加しました。</span><span class="sxs-lookup"><span data-stu-id="3f31e-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="3f31e-135">**営業**</span><span class="sxs-lookup"><span data-stu-id="3f31e-135">**Sales**</span></span>

<span data-ttu-id="3f31e-136">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="3f31e-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f31e-137">見積もりや契約でプロジェクト ベースの品目を選択する場合、**提案** ボタンを既存の製品に関連付けられた製品ベースの品目を選択した時だけ表示します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="3f31e-138">**Create_Product** 特権を **Create_ProjectContract** 特権から分割します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="3f31e-139">請求明細行を削除すると **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** で null 参照エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3f31e-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]