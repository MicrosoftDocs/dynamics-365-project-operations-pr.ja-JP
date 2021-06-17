---
title: セキュリティ モデル
description: このトピックは Dynamics 365 Project Operations のセキュリティ モデルに関する情報を提供します。
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ccca2f387ce3abef3b24cb96fdbcc69f3c0c075b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002252"
---
# <a name="security-model"></a><span data-ttu-id="2d7ce-103">セキュリティ モデル</span><span class="sxs-lookup"><span data-stu-id="2d7ce-103">Security Model</span></span>

<span data-ttu-id="2d7ce-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="2d7ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2d7ce-105">Microsoft Dynamics 365 Project Operations は独自のセキュリティモデルを含み、Microsoft Office グループと連携するロール ベースのビジネス セキュリティ モデルを利用できます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="2d7ce-106">セキュリティ ロール</span><span class="sxs-lookup"><span data-stu-id="2d7ce-106">Security roles</span></span>
<span data-ttu-id="2d7ce-107">Project Operations のフロントエンド機能には、次のロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="2d7ce-108">ロール</span><span class="sxs-lookup"><span data-stu-id="2d7ce-108">Role</span></span>                          | <span data-ttu-id="2d7ce-109">内容</span><span class="sxs-lookup"><span data-stu-id="2d7ce-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="2d7ce-110">範囲</span><span class="sxs-lookup"><span data-stu-id="2d7ce-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="2d7ce-111">プラクティス マネージャー</span><span class="sxs-lookup"><span data-stu-id="2d7ce-111">Practice manager</span></span>              | <span data-ttu-id="2d7ce-112">プロジェクト間のレポートをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="2d7ce-113">部署</span><span class="sxs-lookup"><span data-stu-id="2d7ce-113">Business unit</span></span>              |
| <span data-ttu-id="2d7ce-114">プロジェクト承認者</span><span class="sxs-lookup"><span data-stu-id="2d7ce-114">Project approver</span></span>              | <span data-ttu-id="2d7ce-115">プロジェクトに対する時間と経費を承認します。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="2d7ce-116">部署</span><span class="sxs-lookup"><span data-stu-id="2d7ce-116">Business unit</span></span> |
| <span data-ttu-id="2d7ce-117">プロジェクトの課金管理者</span><span class="sxs-lookup"><span data-stu-id="2d7ce-117">Project billing administrator</span></span> | <span data-ttu-id="2d7ce-118">請求書の提案を作成します。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="2d7ce-119">部署</span><span class="sxs-lookup"><span data-stu-id="2d7ce-119">Business unit</span></span> |
| <span data-ttu-id="2d7ce-120">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="2d7ce-120">Project manager</span></span>               | <span data-ttu-id="2d7ce-121">プロジェクト計画を作成し、リソースを要求します。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="2d7ce-122">部署</span><span class="sxs-lookup"><span data-stu-id="2d7ce-122">Business unit</span></span> |
| <span data-ttu-id="2d7ce-123">プロジェクト リソース</span><span class="sxs-lookup"><span data-stu-id="2d7ce-123">Project resource</span></span>              | <span data-ttu-id="2d7ce-124">予約して時間を報告できるチーム メンバー。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="2d7ce-125">部署</span><span class="sxs-lookup"><span data-stu-id="2d7ce-125">Business unit</span></span>|
| <span data-ttu-id="2d7ce-126">リソース マネージャー</span><span class="sxs-lookup"><span data-stu-id="2d7ce-126">Resource manager</span></span>              | <span data-ttu-id="2d7ce-127">リソース要求や予約の実行など、すべてのリソース管理機能は、ハイブリッド プロジェクト マネージャー + リソース マネージャー構成と単一の集中型リソース マネージャーのロールをサポートするために分離されています。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="2d7ce-128">部署</span><span class="sxs-lookup"><span data-stu-id="2d7ce-128">Business unit</span></span> |


<span data-ttu-id="2d7ce-129">Web 向けの Microsoft Project には、次のロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="2d7ce-130">ロール</span><span class="sxs-lookup"><span data-stu-id="2d7ce-130">Role</span></span>           | <span data-ttu-id="2d7ce-131">内容</span><span class="sxs-lookup"><span data-stu-id="2d7ce-131">Description</span></span>                                                                                                        | <span data-ttu-id="2d7ce-132">範囲</span><span class="sxs-lookup"><span data-stu-id="2d7ce-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="2d7ce-133">プロジェクト ユーザー</span><span class="sxs-lookup"><span data-stu-id="2d7ce-133">Project user</span></span>   | <span data-ttu-id="2d7ce-134">自分達のプロジェクトを作成し、共有されているプロジェクトを表示できる、プロジェクトの共同作業ユーザー。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="2d7ce-135">ユーザー </span><span class="sxs-lookup"><span data-stu-id="2d7ce-135">User</span></span>   |
| <span data-ttu-id="2d7ce-136">プロジェクト システム</span><span class="sxs-lookup"><span data-stu-id="2d7ce-136">Project system</span></span> | <span data-ttu-id="2d7ce-137">アプリケーション コンテキストに使用されるロール。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-137">Role used for application   context.</span></span> <span data-ttu-id="2d7ce-138">お客様は、このシステムのロールを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="2d7ce-139">グローバル</span><span class="sxs-lookup"><span data-stu-id="2d7ce-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="2d7ce-140">セキュリティの実施</span><span class="sxs-lookup"><span data-stu-id="2d7ce-140">Security enforcement</span></span>
<span data-ttu-id="2d7ce-141">プロジェクト レベルで実行されるアクションは、ログインしたユーザーのコンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="2d7ce-142">つまり、プロジェクトを作成、開く、または削除するには、ユーザーは CDS で使用可能なアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="2d7ce-143">CDS でのアクセスは、プラットフォームに含まれている可能なメカニズムのいずれかを介して許可される場合があります。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="2d7ce-144">たとえば、より広いスコープを持つユーザーがプロジェクトにアクセスしたり、ユーザーにアクセスを許可する明示的なプロジェクト共有アクションが実行された場合などです。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="2d7ce-145">Project Operations でプロジェクトを作成するときは、これを考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="2d7ce-146">Project Operations とモダン グループの共同作業</span><span class="sxs-lookup"><span data-stu-id="2d7ce-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="2d7ce-147">Web 向けの Project と Project Operations は、共同作業のためのモダン グループをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="2d7ce-148">グループを介してプロジェクトに追加されたユーザーは、プロジェクト計画を編集できます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="2d7ce-149">Web 向けの Project は、割り当て時にユーザーをグループに自動的に追加します。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="2d7ce-150">グループを使用すると、プロジェクトのアクセス許可とサポートするコラボレーション成果物を共同で作業できます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="2d7ce-151">次の図は、グループ割り当てプロセス中に発生するイベントと状態の変化を示しています。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="2d7ce-152">Project Operations は、暗黙的なアクションによってグループを作成するのではなく、グループを押すという明示的なアクションを介してのみ作成します。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="2d7ce-153">**グループ管理** ダイアログでのグループ メンバーの検索は、環境のセキュリティ グループの一部として設定されているユーザーに限定されています。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="2d7ce-154">詳細については、[環境へのユーザー アクセスのコントロール: セキュリティ グループおよびライセンス](/power-platform/admin/control-user-access) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![グループモード](./media/groupsmode.png)

1. <span data-ttu-id="2d7ce-156">プロジェクトは、作成するユーザーによって作成および所有されます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="2d7ce-157">プロジェクトの所有者がチームに更新されます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="2d7ce-158">所有者チームは、指定または作成された Office グループにマップされます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="2d7ce-159">プロジェクトの元の所有者が Office グループに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="2d7ce-160">展開に関する推奨事項</span><span class="sxs-lookup"><span data-stu-id="2d7ce-160">Deployment recommendation</span></span>
<span data-ttu-id="2d7ce-161">Office グループのコラボレーション モデルが拡張するにつれて、時間の経過とともにより詳細なコントロールを提供する機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="2d7ce-162">今日 Project Operations を展開しているお客様は、従来の Microsoft Dynamics 365 セキュリティ モデルに集中することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="2d7ce-163">詳細については、[Common Data Service のセキュリティ](/power-platform/admin/wp-security) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="2d7ce-164">Project Operations と Microsoft Dynamics 365 Finance セキュリティ</span><span class="sxs-lookup"><span data-stu-id="2d7ce-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="2d7ce-165">Project Operations には次のロールが含まれます:</span><span class="sxs-lookup"><span data-stu-id="2d7ce-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="2d7ce-166">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="2d7ce-166">Project manager</span></span>
- <span data-ttu-id="2d7ce-167">プロジェクト経理担当者</span><span class="sxs-lookup"><span data-stu-id="2d7ce-167">Project accountant</span></span>

<span data-ttu-id="2d7ce-168">Finance のセキュリティの詳細については、[ロールベースのセキュリティ](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d7ce-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]