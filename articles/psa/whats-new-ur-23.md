---
title: Project Service Automation 更新プログラム リリース 23、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 23、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150044"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="05409-103">Project Service Automation 更新プログラム リリース 23、V3</span><span class="sxs-lookup"><span data-stu-id="05409-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="05409-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="05409-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="05409-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05409-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="05409-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="05409-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="05409-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="05409-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="05409-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05409-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="05409-109">このトピックには、Project Service Automation V3 更新プログラム 23 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="05409-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="05409-110">このバージョンのビルド番号は V 3.10.34.30 であり、一般的には 2020 年 8 月の自己プログラム更新の処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="05409-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="05409-111">更新プログラム 23</span><span class="sxs-lookup"><span data-stu-id="05409-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="05409-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="05409-112">Bug fixes</span></span>

<span data-ttu-id="05409-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="05409-113">**Time and Expense**</span></span>

<span data-ttu-id="05409-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="05409-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="05409-115">**プロジェクト チーム メンバーの削除** のエッジ ケースを処理して、意味のある例外を提供します。</span><span class="sxs-lookup"><span data-stu-id="05409-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="05409-116">割り当てをインポートすると、削除画面が空白になります。</span><span class="sxs-lookup"><span data-stu-id="05409-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="05409-117">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="05409-117">**Resource Management**</span></span>

<span data-ttu-id="05409-118">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="05409-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="05409-119">タイム スケールが 5 日を超えると、**リソース稼働率グリッド リソース カード** に誤ったデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="05409-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="05409-120">顧客が予約可能リソースを作成すると、プラグインは断続的にリソースを Microsoft Office 365 グループ に自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="05409-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="05409-121">**調整** ビューでは、**週** や **月** ビューに手動の配分型が正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="05409-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="05409-122">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="05409-122">**Project Management**</span></span>

<span data-ttu-id="05409-123">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="05409-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="05409-124">**RetrieveMultiple for usersettings** エンティティの数が多すぎると、プロジェクト承認やその他の操作のパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="05409-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="05409-125">**タスク計画** グリッドのリソース検索では、プロジェクト チームから最大 5 人のチーム メンバーのみを表示するように制限されています。</span><span class="sxs-lookup"><span data-stu-id="05409-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="05409-126">**タスク計画** グリッドのリソース検索では、非アクティブなリソースをフィルタリングしません。</span><span class="sxs-lookup"><span data-stu-id="05409-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="05409-127">手動モードは、プロジェクト計画 WBS (作業分解構造) で予想どおりに機能していません。</span><span class="sxs-lookup"><span data-stu-id="05409-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="05409-128">**タスク計画** グリッドには、**非アクティブなトランザクション カテゴリ** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="05409-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="05409-129">タスクに複数の割り当てがある場合、**リソース割り当て** グリッドは正しく丸められません。</span><span class="sxs-lookup"><span data-stu-id="05409-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="05409-130">丸め値は、1 つのタスクの計画コストと実際コストで異なります。</span><span class="sxs-lookup"><span data-stu-id="05409-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="05409-131">**営業**</span><span class="sxs-lookup"><span data-stu-id="05409-131">**Sales**</span></span>

<span data-ttu-id="05409-132">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="05409-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="05409-133">**すべてのトランザクション カテゴリの取得** のダブルクリックで、複数行を作成します。</span><span class="sxs-lookup"><span data-stu-id="05409-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
