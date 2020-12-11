---
title: Project Service Automation 更新プログラム リリース 25、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 25、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183549"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="921f5-103">Project Service Automation 更新プログラム リリース 25、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="921f5-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="921f5-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="921f5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="921f5-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="921f5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="921f5-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="921f5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="921f5-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="921f5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="921f5-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="921f5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="921f5-109">このトピックでは、Project Service Automation V3、更新プログラム リリース 25 で新規または変更された機能と修正の一覧を示します。このバージョンのビルド番号は V 3.10.43.76 で、2020 年 10 月に自己更新で一般提供されます。</span><span class="sxs-lookup"><span data-stu-id="921f5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="921f5-110">更新プログラム 25</span><span class="sxs-lookup"><span data-stu-id="921f5-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="921f5-111">バグの修正</span><span class="sxs-lookup"><span data-stu-id="921f5-111">Bug fixes</span></span>

<span data-ttu-id="921f5-112">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="921f5-112">**Time and Expense**</span></span>

<span data-ttu-id="921f5-113">次の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="921f5-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="921f5-114">取得される間隔が大きすぎることに基づいて、追加データを示す時間エントリ グラフ。</span><span class="sxs-lookup"><span data-stu-id="921f5-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="921f5-115">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="921f5-115">**Resource Management**</span></span>

<span data-ttu-id="921f5-116">次の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="921f5-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="921f5-117">上位バージョンのパッチが既に存在する場合に、Universal Resource Scheduling のパッチ インポートをスキップする Package Deployer コードを追加しました。</span><span class="sxs-lookup"><span data-stu-id="921f5-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="921f5-118">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="921f5-118">**Project Management**</span></span>

<span data-ttu-id="921f5-119">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="921f5-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="921f5-120">プロジェクト追跡グリッドで不正確な予定コストにつながる、丸めと為替レートの不一致が修正されました。</span><span class="sxs-lookup"><span data-stu-id="921f5-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="921f5-121">**プロジェクト** フォームに 2 つ以上の対応グリッドを表示する機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="921f5-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="921f5-122">カレンダーの終了日を過ぎてタスクを割り当てると、リソースの割り当てに失敗することに対処するための検証が提供されました。</span><span class="sxs-lookup"><span data-stu-id="921f5-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="921f5-123">以下から生成される Null 参照例外に対処するためのエラー処理が改善されました:</span><span class="sxs-lookup"><span data-stu-id="921f5-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="921f5-124">**PreValidateProjectTeamMemberCreate** プラグイン</span><span class="sxs-lookup"><span data-stu-id="921f5-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="921f5-125">関連するプロジェクトなしでプロジェクト タスクが作成された場合の **PreValidateProjectTaskCreate**</span><span class="sxs-lookup"><span data-stu-id="921f5-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="921f5-126">**PreProjectTeamMemberCreate** プラグイン</span><span class="sxs-lookup"><span data-stu-id="921f5-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="921f5-127">**PostProjectTeamMemberDelete** プラグイン</span><span class="sxs-lookup"><span data-stu-id="921f5-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="921f5-128">**PreValidateProjectTaskDelete** プラグイン</span><span class="sxs-lookup"><span data-stu-id="921f5-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="921f5-129">**営業**</span><span class="sxs-lookup"><span data-stu-id="921f5-129">**Sales**</span></span>

<span data-ttu-id="921f5-130">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="921f5-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="921f5-131">**プロジェクトのコピー: HelperResource 管理の見積もり** から生成される Null 参照例外に対処するためのエラー処理が改善されました。</span><span class="sxs-lookup"><span data-stu-id="921f5-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="921f5-132">**時間と材料の請求バックログ** の **請求準備未完了** では、請求の状態がクリアされません。</span><span class="sxs-lookup"><span data-stu-id="921f5-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="921f5-133">**ロール価格** と **カタログ品目** タブの誤ってラベル付けされた **価格** ボタンが修正されました。</span><span class="sxs-lookup"><span data-stu-id="921f5-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>