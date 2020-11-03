---
title: 経費カテゴリの構成
description: このトピックでは、プロジェクト カテゴリの設定について説明します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079164"
---
# <a name="configure-project-categories"></a><span data-ttu-id="acf4f-103">経費カテゴリの構成</span><span class="sxs-lookup"><span data-stu-id="acf4f-103">Configure project categories</span></span>

<span data-ttu-id="acf4f-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="acf4f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="acf4f-105">Project Operations は、プロジェクトの売上および経費を分類するための堅牢な機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="acf4f-106">カテゴリは、プロジェクト トランザクションを記録および分析し、総勘定元帳への転記を促進する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="acf4f-107">次の図は、トランザクション カテゴリ、共有カテゴリ、およびプロジェクト カテゴリ間の関連付けを示します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="acf4f-108">トランザクション カテゴリは、プロジェクト トランザクションの基本的なグループです。</span><span class="sxs-lookup"><span data-stu-id="acf4f-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="acf4f-109">そのグループ内には、アプリケーションやモジュール間で共有できる一連の共有カテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="acf4f-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="acf4f-110">さらに詳細に説明すると、プロジェクト カテゴリは最も詳細なレベルのカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="acf4f-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="acf4f-111">プロジェクト カテゴリは、法人、モジュール、およびアプリケーションに固有です。</span><span class="sxs-lookup"><span data-stu-id="acf4f-111">Project categories are specific to legal entity, module, and application.</span></span>

![トランザクション カテゴリ、共有カテゴリ、およびプロジェクト カテゴリ間の関連付け](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="acf4f-113">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="acf4f-113">Transaction categories</span></span>

<span data-ttu-id="acf4f-114">トランザクション カテゴリは、プロジェクト トランザクションの基本的なグループを表し、会社またはトランザクション タイプに固有のものではありません。</span><span class="sxs-lookup"><span data-stu-id="acf4f-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="acf4f-115">たとえば、Contoso Robotics は、設計、旅行、インストール、およびサービス トランザクション カテゴリを使用して、プロジェクト トランザクションをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="acf4f-116">トランザクション カテゴリは、Project Operations モジュールで定義されます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="acf4f-117">**設定** \> **トランザクション カテゴリ** の順に移動してフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="acf4f-118">**新規** または **Excel からインポート** のいずれかを選択して新しいトランザクション カテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="acf4f-119">共有カテゴリ</span><span class="sxs-lookup"><span data-stu-id="acf4f-119">Shared categories</span></span>

<span data-ttu-id="acf4f-120">Dynamics 365 は共有カテゴリの概念を使用して、Dynamics 365 Finance、Dynamics 365 Supply Chain、および Dynamics 365 Project Operations などの異なるアプリケーションで経費を分類します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="acf4f-121">作成されたトランザクション カテゴリごとに、Project Operations は関連する 4 つの共有カテゴリを自動的に作成します: 時間、経費、手数料、および項目。</span><span class="sxs-lookup"><span data-stu-id="acf4f-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="acf4f-122">**プロジェクト管理および会計** \> **設定** \> **カテゴリ** \> **共有カテゴリ** の順に移動して、共有カテゴリを確認および調整できます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="acf4f-123">プロジェクト カテゴリ</span><span class="sxs-lookup"><span data-stu-id="acf4f-123">Project categories</span></span>

<span data-ttu-id="acf4f-124">プロジェクト カテゴリは最も詳細なレベルのカテゴリ構成を表し、プロジェクト経理担当者が会社ごとに個別に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acf4f-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="acf4f-125">**プロジェクト管理および会計** \> **設定** \> **カテゴリ** \> **プロジェクト カテゴリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="acf4f-126">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="acf4f-126">Select **New**.</span></span>
3. <span data-ttu-id="acf4f-127">前のセクションで作成した共有カテゴリの **カテゴリ ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="acf4f-128">Project Operations では、トランザクション カテゴリに関連付けられた共有カテゴリのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="acf4f-129">カテゴリ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="acf4f-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="acf4f-130">カテゴリ グループ</span><span class="sxs-lookup"><span data-stu-id="acf4f-130">Category groups</span></span>

<span data-ttu-id="acf4f-131">カテゴリ グループは、関連するプロジェクト カテゴリ間でプロパティ (主に転記プロフィール) を共有するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="acf4f-132">トランザクション タイプごとに少なくとも 1 つのカテゴリ グループが必要であり、各プロジェクト カテゴリにはグループが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="acf4f-133">Project Operations の転記仕様は、プロジェクト コストと売上プロファイル ルール、プロジェクト カテゴリ、およびカテゴリ グループによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="acf4f-134">**プロジェクト管理および会計** \> **設定** \> **カテゴリ** \> **カテゴリ グループ** の順に移動して、カテゴリ グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="acf4f-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
