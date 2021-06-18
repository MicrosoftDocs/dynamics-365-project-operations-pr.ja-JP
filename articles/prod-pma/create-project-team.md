---
title: プロジェクト チームを作成する
description: このトピックでは、プロジェクトチームの作成方法や管理方法についての説明します。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006202"
---
# <a name="create-a-project-team"></a><span data-ttu-id="f9791-103">プロジェクト チームの作成</span><span class="sxs-lookup"><span data-stu-id="f9791-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9791-104">以前にプロジェクトで設定されたロールを使用するには、プロジェクト マネージャーがロールをプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9791-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="f9791-105">プロジェクトには複数のロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f9791-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="f9791-106">混乱を防ぐために、これらのロールには予約時に自動的にラベルが付けられます。</span><span class="sxs-lookup"><span data-stu-id="f9791-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="f9791-107">たとえば、プロジェクト マネージャーに 3 人のソフトウェア エンジニアが必要な場合、ラベルが自動的に生成される **ソフトウェア エンジニア 1**、**ソフトウェア エンジニア 2**、および **ソフトウェアエンジニア 3** の 3 つのソフトウェア エンジニアのロールがあります。</span><span class="sxs-lookup"><span data-stu-id="f9791-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="f9791-108">ロールの特性が以前にロールに設定されている場合、それらはリソースの検索中にフィルターとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="f9791-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="f9791-109">検索をさらに絞り込むために、必要に応じて追加の特性を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f9791-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="f9791-110">ビューの設定をカスタマイズして、リソースの空き時間をわかりやすく表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9791-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="f9791-111">時間ごと、毎日、毎週、毎月、四半期、および年間の可用性を表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f9791-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="f9791-112">リソースの使用可能なキャパシティと残りのキャパシティを表示するオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="f9791-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="f9791-113">このオプションは、アクティビティまたはリソースの空き時間に使用可能な時間を見積もる場合の時間管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f9791-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="f9791-114">プロジェクト マネージャーは、ページでロールを選択し、要件に適合する使用可能なリソースがある場合は、ロールを満たすためのリソースを予約することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f9791-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="f9791-115">計画ステージのこの時点では、リソースを予約する必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f9791-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="f9791-116">WBS を作成するときに、プロジェクトのロールをスタッフが配置されたリソースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="f9791-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="f9791-117">ロールが WBS のスタッフが配置されたリソースに置き換えられた場合、リソースの設定により、プロジェクト チームのリストとスケジュールが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="f9791-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="f9791-118">[![ロールと実際のリソースの両方を含むプロジェクト チーム リスト](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="f9791-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="f9791-119">プロジェクト マネージャーには、プロジェクトのリソースを予約するため、**残りのキャパシティ**、**全キャパシティ**、**キャパシティの割合**、および **時間を指定** などのさまざまなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f9791-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="f9791-120">リソースの割り当てが変更された場合、これらのオプションはいつでもキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="f9791-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="f9791-121">次の 2 つの予約タイプがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f9791-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="f9791-122">**本予約** - リソースの予約は承認済みであり、指定された期間のエンゲージメントに従事することが確認されています。</span><span class="sxs-lookup"><span data-stu-id="f9791-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="f9791-123">**仮予約** – リソース予約は、指定された期間、エンゲージメントに取り組むように一時的に設定されました。</span><span class="sxs-lookup"><span data-stu-id="f9791-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="f9791-124">次の手順では、プロジェクト チームの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f9791-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="f9791-125">プロジェクト チームの作成</span><span class="sxs-lookup"><span data-stu-id="f9791-125">Create a project team</span></span>

1. <span data-ttu-id="f9791-126">**すべてのプロジェクト** リスト ページで、プロジェクトを選択してから、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="f9791-127">**プロジェクト チームとスケジュール** タブの、**スケジュール終了日** フィールドに、スケジュールの開始日と 1 か月を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9791-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="f9791-128">たとえば、スケジュールの開始日が 2017 年 6 月 24 日 (2017年6月24日) の場合、**2017 年 7 月 24 日** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f9791-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="f9791-129">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-129">Select **Add**.</span></span>
4. <span data-ttu-id="f9791-130">**プロジェクトにロールを追加** ウィンドウの、**ロール** フィールドで、**シニア プロジェクト マネージャー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="f9791-131">**必要なコンピテンシー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="f9791-132">**特性を選択** ウィンドウでは、シニア プロジェクト マネージャー ロールに以前に設定した特性が既定で選択されています。</span><span class="sxs-lookup"><span data-stu-id="f9791-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="f9791-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-133">Select **OK**.</span></span>
7. <span data-ttu-id="f9791-134">**プロジェクトにロールを追加** ウィンドウの、**リソースの数** フィールドで、**1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f9791-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="f9791-135">**リソース** フィールドで、検索は必要なコンピテンシーを持つすべてのリソースを表示します。</span><span class="sxs-lookup"><span data-stu-id="f9791-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="f9791-136">**Daniel Goldschmidt** を選択し、次に **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="f9791-137">**プロジェクト** ページで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="f9791-138">**プロジェクトにロールを追加** ウィンドウの、**ロール** フィールドで、**チーム マネージャー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="f9791-139">**リソースの数** フィールドに、**5** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f9791-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="f9791-140">**作成** を選びます。</span><span class="sxs-lookup"><span data-stu-id="f9791-140">Select **Create**.</span></span>
12. <span data-ttu-id="f9791-141">**プロジェクト** ページで、**リソース処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="f9791-142">プロジェクト チームを監視する</span><span class="sxs-lookup"><span data-stu-id="f9791-142">Monitor project teams</span></span>
1. <span data-ttu-id="f9791-143">**すべてのプロジェクト** ページで、**XYZ アップグレード フェーズ 2** プロジェクトの **プロジェクト ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9791-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="f9791-144">**プロジェクト チームとスケジュール** FastTab で、リストされているプロジェクト リソースが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9791-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]