---
title: Project Service Automation 更新プログラム リリース 19、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 19、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079221"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="e3279-103">Project Service Automation 更新プログラム リリース 19、V3</span><span class="sxs-lookup"><span data-stu-id="e3279-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="e3279-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="e3279-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e3279-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3279-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e3279-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="e3279-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e3279-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="e3279-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e3279-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3279-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e3279-109">このトピックには、PSA V3 更新プログラム 19 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="e3279-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="e3279-110">このバージョンのビルド番号は V3.10.30.41 であり、2020 年 5 月のセルフ アップデートを通じて一般提供されました。</span><span class="sxs-lookup"><span data-stu-id="e3279-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="e3279-111">更新プログラム 19</span><span class="sxs-lookup"><span data-stu-id="e3279-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e3279-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="e3279-112">Bug fixes</span></span>

<span data-ttu-id="e3279-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="e3279-113">**Time and Expense**</span></span>

<span data-ttu-id="e3279-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="e3279-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="e3279-115">時間エントリのインポートから派生したエラーが正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="e3279-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="e3279-116">時間エントリ グリッドは **日付のみ** フィールドの動作をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e3279-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="e3279-117">プロジェクト リソースは、プロジェクトで経費を作成できません。</span><span class="sxs-lookup"><span data-stu-id="e3279-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="e3279-118">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="e3279-118">**Project Management**</span></span>

<span data-ttu-id="e3279-119">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="e3279-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="e3279-120">孫タスクでは、完了 (EAC) 計算中に誤った工数の推定が発生します。</span><span class="sxs-lookup"><span data-stu-id="e3279-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="e3279-121">**営業**</span><span class="sxs-lookup"><span data-stu-id="e3279-121">**Sales**</span></span>

<span data-ttu-id="e3279-122">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="e3279-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="e3279-123">**再計算** アクションは、経費契約品目の詳細または見積依頼明細行の詳細では機能しません。</span><span class="sxs-lookup"><span data-stu-id="e3279-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="e3279-124">**価格の更新** が、経費の見積もりに欠けています。</span><span class="sxs-lookup"><span data-stu-id="e3279-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="e3279-125">顧客は、 **プロジェクト契約** ページからカスタム契約の状態の理由を選択できません。</span><span class="sxs-lookup"><span data-stu-id="e3279-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="e3279-126">見積もりからカスタム価格表を作成すると、パフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="e3279-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="e3279-127">**見積依頼明細行の詳細** ページと **契約品目の詳細** ページで **単位** の既定値に不整合が発生します。</span><span class="sxs-lookup"><span data-stu-id="e3279-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="e3279-128">請求不可トランザクション カテゴリ項目を請求可能な契約品目に追加しても、トランザクション カテゴリの **請求不可** の請求タイプは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="e3279-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="e3279-129">顧客は、以前に作成された契約で新たに追加されたロールとカテゴリを使用できません。</span><span class="sxs-lookup"><span data-stu-id="e3279-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="e3279-130">PreValidateProjectTeamMemberUpdate.cs でパフォーマンスの不要な取得が低下します</span><span class="sxs-lookup"><span data-stu-id="e3279-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="e3279-131">**リソース カテゴリ** の一覧で請求不可として設定されたロールは、プロジェクトの契約品目で **請求可能ロール** タブに **請求不可** として追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3279-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="e3279-132">**GetBookableResourceIdFromUser** がプライマリ ID だけでなく、予約可能なリソースのすべての列を取得するため、プロジェクトを作成するときに、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e3279-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="e3279-133">**TransactionType** エンティティに事前検証更新プラグインがないため、ユーザーがトランザクション タイプに対して無効な **単位** と **UnitGroups** を入力できません。</span><span class="sxs-lookup"><span data-stu-id="e3279-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="e3279-134">**削除** ステップは、時間エントリのインポートでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="e3279-134">The **Remove** step does not work for time entry import.</span></span>
