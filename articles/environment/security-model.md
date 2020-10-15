---
title: セキュリティ モデル
description: このトピックでは、Dynamics 365 Project Operations のセキュリティ モデルについて説明します。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896737"
---
# <a name="security-model"></a><span data-ttu-id="263c6-103">セキュリティ モデル</span><span class="sxs-lookup"><span data-stu-id="263c6-103">Security Model</span></span>

<span data-ttu-id="263c6-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="263c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="263c6-105">Microsoft Dynamics 365 Project Operations には、Microsoft Office グループと連携する役割ベースのビジネス セキュリティ モデルを可能にする一意のセキュリティ モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="263c6-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="263c6-106">セキュリティ ロール</span><span class="sxs-lookup"><span data-stu-id="263c6-106">Security roles</span></span>
<span data-ttu-id="263c6-107">Project Operations のフロントエンド機能には、次のロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="263c6-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="263c6-108">ロール</span><span class="sxs-lookup"><span data-stu-id="263c6-108">Role</span></span>                          | <span data-ttu-id="263c6-109">内容</span><span class="sxs-lookup"><span data-stu-id="263c6-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="263c6-110">範囲</span><span class="sxs-lookup"><span data-stu-id="263c6-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="263c6-111">プラクティス マネージャー</span><span class="sxs-lookup"><span data-stu-id="263c6-111">Practice manager</span></span>              | <span data-ttu-id="263c6-112">プロジェクト間のレポートをサポートします。</span><span class="sxs-lookup"><span data-stu-id="263c6-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="263c6-113">部署</span><span class="sxs-lookup"><span data-stu-id="263c6-113">Business unit</span></span>              |
| <span data-ttu-id="263c6-114">プロジェクト承認者</span><span class="sxs-lookup"><span data-stu-id="263c6-114">Project approver</span></span>              | <span data-ttu-id="263c6-115">プロジェクトに対する時間と経費を承認します。</span><span class="sxs-lookup"><span data-stu-id="263c6-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="263c6-116">部署</span><span class="sxs-lookup"><span data-stu-id="263c6-116">Business unit</span></span> |
| <span data-ttu-id="263c6-117">プロジェクトの課金管理者</span><span class="sxs-lookup"><span data-stu-id="263c6-117">Project billing administrator</span></span> | <span data-ttu-id="263c6-118">請求書の提案を作成します。</span><span class="sxs-lookup"><span data-stu-id="263c6-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="263c6-119">部署</span><span class="sxs-lookup"><span data-stu-id="263c6-119">Business unit</span></span> |
| <span data-ttu-id="263c6-120">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="263c6-120">Project manager</span></span>               | <span data-ttu-id="263c6-121">プロジェクト計画を作成し、リソースを要求します。</span><span class="sxs-lookup"><span data-stu-id="263c6-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="263c6-122">部署</span><span class="sxs-lookup"><span data-stu-id="263c6-122">Business unit</span></span> |
| <span data-ttu-id="263c6-123">プロジェクト リソース</span><span class="sxs-lookup"><span data-stu-id="263c6-123">Project resource</span></span>              | <span data-ttu-id="263c6-124">予約して時間を報告できるチーム メンバー。</span><span class="sxs-lookup"><span data-stu-id="263c6-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="263c6-125">部署</span><span class="sxs-lookup"><span data-stu-id="263c6-125">Business unit</span></span>|
| <span data-ttu-id="263c6-126">リソース マネージャー</span><span class="sxs-lookup"><span data-stu-id="263c6-126">Resource manager</span></span>              | <span data-ttu-id="263c6-127">リソース要求や予約の実行など、すべてのリソース管理機能は、ハイブリッド プロジェクト マネージャー + リソース マネージャー構成と単一の集中型リソース マネージャーのロールをサポートするために分離されています。</span><span class="sxs-lookup"><span data-stu-id="263c6-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="263c6-128">部署</span><span class="sxs-lookup"><span data-stu-id="263c6-128">Business unit</span></span> |


<span data-ttu-id="263c6-129">Web 向けの Microsoft Project には、次のロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="263c6-129">Microsoft Project for the Web includes the following roles:</span></span>
| <span data-ttu-id="263c6-130">ロール</span><span class="sxs-lookup"><span data-stu-id="263c6-130">Role</span></span>                          | <span data-ttu-id="263c6-131">内容</span><span class="sxs-lookup"><span data-stu-id="263c6-131">Description</span></span>                                                                                                          | <span data-ttu-id="263c6-132">範囲</span><span class="sxs-lookup"><span data-stu-id="263c6-132">Scope</span></span> |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| <span data-ttu-id="263c6-133">プロジェクト ユーザー</span><span class="sxs-lookup"><span data-stu-id="263c6-133">Project user</span></span> | <span data-ttu-id="263c6-134">独自のプロジェクトを作成し、共有されているプロジェクトを表示できるプロジェクトの共同作業ユーザー。</span><span class="sxs-lookup"><span data-stu-id="263c6-134">Collaborative user of Project who is able to create their own projects and view any projects shared with them.</span></span>| <span data-ttu-id="263c6-135">ユーザー </span><span class="sxs-lookup"><span data-stu-id="263c6-135">User</span></span>|
| <span data-ttu-id="263c6-136">プロジェクト システム</span><span class="sxs-lookup"><span data-stu-id="263c6-136">Project system</span></span> | <span data-ttu-id="263c6-137">アプリケーション コンテキストに使用されるロール。</span><span class="sxs-lookup"><span data-stu-id="263c6-137">Role used for application context.</span></span> <span data-ttu-id="263c6-138">お客様は、このシステムのロールを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="263c6-138">Customers should not use this system role.</span></span> | <span data-ttu-id="263c6-139">グローバル</span><span class="sxs-lookup"><span data-stu-id="263c6-139">Global</span></span>|

## <a name="security-enforcement"></a><span data-ttu-id="263c6-140">セキュリティの実施</span><span class="sxs-lookup"><span data-stu-id="263c6-140">Security enforcement</span></span>
<span data-ttu-id="263c6-141">プロジェクト レベルで実行されるアクションは、ログインしたユーザーのコンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="263c6-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="263c6-142">つまり、プロジェクトを作成、開く、または削除するには、ユーザーは CDS で使用可能なアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="263c6-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="263c6-143">CDS でのアクセスは、プラットフォームに含まれている可能なメカニズムのいずれかを介して許可される場合があります。</span><span class="sxs-lookup"><span data-stu-id="263c6-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="263c6-144">たとえば、より広いスコープを持つユーザーがプロジェクトにアクセスしたり、ユーザーにアクセスを許可する明示的なプロジェクト共有アクションが実行された場合などです。</span><span class="sxs-lookup"><span data-stu-id="263c6-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="263c6-145">Project Operations でプロジェクトを作成するときは、これを考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="263c6-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="263c6-146">Project Operations とモダン グループの共同作業</span><span class="sxs-lookup"><span data-stu-id="263c6-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="263c6-147">Web 向けの Project と Project Operations は、共同作業のためのモダン グループをサポートします。</span><span class="sxs-lookup"><span data-stu-id="263c6-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="263c6-148">グループを介してプロジェクトに追加されたユーザーは、プロジェクト計画を編集できます。</span><span class="sxs-lookup"><span data-stu-id="263c6-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="263c6-149">Web 向けの Project は、割り当て時にユーザーをグループに自動的に追加します。</span><span class="sxs-lookup"><span data-stu-id="263c6-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="263c6-150">グループを使用すると、プロジェクトのアクセス許可とサポートするコラボレーション成果物を共同で作業できます。</span><span class="sxs-lookup"><span data-stu-id="263c6-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="263c6-151">次の図は、グループ割り当てプロセス中に発生するイベントと状態の変化を示しています。</span><span class="sxs-lookup"><span data-stu-id="263c6-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="263c6-152">Project Operations は、暗黙的なアクションによってグループを作成するのではなく、グループを押すという明示的なアクションを介してのみ作成します。</span><span class="sxs-lookup"><span data-stu-id="263c6-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="263c6-153">**グループ管理**ダイアログでのグループ メンバーの検索は、環境のセキュリティ グループの一部として設定されているユーザーに限定されています。</span><span class="sxs-lookup"><span data-stu-id="263c6-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="263c6-154">詳細については、[環境へのユーザー アクセスのコントロール: セキュリティ グループおよびライセンス](https://docs.microsoft.com/power-platform/admin/control-user-access) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="263c6-154">For more information, see [Control user access to environments: security groups and licenses](https://docs.microsoft.com/power-platform/admin/control-user-access).</span></span>

1. <span data-ttu-id="263c6-155">プロジェクトは、作成するユーザーによって作成および所有されます。</span><span class="sxs-lookup"><span data-stu-id="263c6-155">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="263c6-156">プロジェクトの所有者がチームに更新されます。</span><span class="sxs-lookup"><span data-stu-id="263c6-156">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="263c6-157">所有者チームは、指定または作成された Office グループにマップされます。</span><span class="sxs-lookup"><span data-stu-id="263c6-157">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="263c6-158">プロジェクトの元の所有者が Office グループに追加されます。</span><span class="sxs-lookup"><span data-stu-id="263c6-158">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="263c6-159">展開に関する推奨事項</span><span class="sxs-lookup"><span data-stu-id="263c6-159">Deployment recommendation</span></span>
<span data-ttu-id="263c6-160">Office グループのコラボレーション モデルが拡張するにつれて、時間の経過とともにより詳細なコントロールを提供する機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="263c6-160">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="263c6-161">今日 Project Operations を展開しているお客様は、従来の Microsoft Dynamics 365 セキュリティ モデルに集中することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="263c6-161">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="263c6-162">詳細については、[Common Data Service のセキュリティ](https://docs.microsoft.com/power-platform/admin/wp-security) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="263c6-162">For more information, see [Security in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="263c6-163">Project Operations と Microsoft Dynamics 365 Finance セキュリティ</span><span class="sxs-lookup"><span data-stu-id="263c6-163">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="263c6-164">Project Operations には次のロールが含まれます:</span><span class="sxs-lookup"><span data-stu-id="263c6-164">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="263c6-165">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="263c6-165">Project manager</span></span>
- <span data-ttu-id="263c6-166">プロジェクト経理担当者</span><span class="sxs-lookup"><span data-stu-id="263c6-166">Project accountant</span></span>

<span data-ttu-id="263c6-167">Finance のセキュリティの詳細については、[ロールベースのセキュリティ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="263c6-167">For more information about security in Finance, see [Role-based security](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>


