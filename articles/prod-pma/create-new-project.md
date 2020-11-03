---
title: 新しいプロジェクトの作成
description: このトピックでは、新規プロジェクトの作成方法に関する情報を提供します。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079403"
---
# <a name="create-a-new-project"></a><span data-ttu-id="f566e-103">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="f566e-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f566e-104">新しいプロジェクトを作成するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f566e-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="f566e-105">**プロジェクト管理** ページで、 **新しいプロジェクト** を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="f566e-106">**プロジェクト タイプ:** 時間と材料</span><span class="sxs-lookup"><span data-stu-id="f566e-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="f566e-107">**プロジェクト名:** XYZ アップグレード フェーズ 2</span><span class="sxs-lookup"><span data-stu-id="f566e-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="f566e-108">**プロジェクト グループ:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="f566e-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="f566e-109">**プロジェクト契約 ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="f566e-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="f566e-110">**プロジェクトの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="f566e-111">リソースをプロジェクトに割り当てる</span><span class="sxs-lookup"><span data-stu-id="f566e-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="f566e-112">**作業者** ページで、 **作業者** リストから、以前にコンピテンシーを設定した作業者のレコードを選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="f566e-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="f566e-113">アクション ウィンドウの **プロジェクト** タブの **設定** グループで、 **プロジェクトを割り当てる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="f566e-114">**リソース検証プロジェクトの割り当て** ページの、 **プロジェクト** タブの、 **選択したプロジェクトにプロジェクトを追加** フィールドで、 **XYZ アップグレード フェーズ 2** プロジェクトをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="f566e-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="f566e-115">**残りのプロジェクト** ウィンドウでプロジェクトを選択し、矢印ボタンを選択して **選択されたプロジェクト** ウィンドウを追加します。</span><span class="sxs-lookup"><span data-stu-id="f566e-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="f566e-116">必要に応じて、リソースにカテゴリを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="f566e-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="f566e-117">カテゴリ タイプは、 **原価** または **売上** のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="f566e-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="f566e-118">カテゴリ タイプは組織によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="f566e-118">The category type is determined by your organization.</span></span> <span data-ttu-id="f566e-119">リソースにカテゴリが割り当てられていない場合、財務はコストと売上の時間単価で既定のカテゴリを検索します。</span><span class="sxs-lookup"><span data-stu-id="f566e-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="f566e-120">プロジェクトのリソースとロールの特性を設定する</span><span class="sxs-lookup"><span data-stu-id="f566e-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="f566e-121">プロジェクト マネージャーは、プロジェクト リソース機能を使用して、プロジェクトに必要なロールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f566e-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="f566e-122">リソースが予約されているときに確認済みのリソースがまだ不明な場合は、ロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f566e-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="f566e-123">ロールは、計画されたリソースとして一時的に予約できるため、プロジェクトの計画ステージを続行できます。</span><span class="sxs-lookup"><span data-stu-id="f566e-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="f566e-124">[![ロールの例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="f566e-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="f566e-125">**シナリオ:** Contoso は、承認されたプロジェクト チャートを含む時間と材料のプロジェクトを完了するために雇われました。</span><span class="sxs-lookup"><span data-stu-id="f566e-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="f566e-126">ジュニア プロジェクト マネージャーはまだプロジェクトの範囲を完了しています。</span><span class="sxs-lookup"><span data-stu-id="f566e-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="f566e-127">リソース マネージャーは現在、新しいプロジェクトで作業するために予約される特定のリソースを識別しています。</span><span class="sxs-lookup"><span data-stu-id="f566e-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="f566e-128">プロジェクトの重要な性質のため、プロジェクト スポンサーは、ロールの 1 つとしてシニア プロジェクト マネージャーを要求しました。</span><span class="sxs-lookup"><span data-stu-id="f566e-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="f566e-129">リソース マネージャーは、プロジェクトの計画中にジュニア プロジェクト マネージャーがリソース情報を必要とする場合に備えて、新しいリソースを取得し、システムでのロールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f566e-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="f566e-130">次の手順は、リソース マネージャーがシニア プロジェクト マネージャーのロールを設定し、リソースの特性を関連付ける方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f566e-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="f566e-131">後で、ロールを使用して、必要なリソース コンピテンシーに一致する使用可能なリソースを検索できます。</span><span class="sxs-lookup"><span data-stu-id="f566e-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="f566e-132">**ロールの設定** ページで、 **新規** を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="f566e-133">**ロール ID:** シニア プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="f566e-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="f566e-134">**説明:** シニア プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="f566e-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="f566e-135">**作成** を選びます。</span><span class="sxs-lookup"><span data-stu-id="f566e-135">Select **Create**.</span></span>
3. <span data-ttu-id="f566e-136">**シニア プロジェクト マネージャー** ロールを選択し、 **特性の構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="f566e-137">**特性タイプ** フィールドで、 **スキル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="f566e-138">**使用可能な特性** フィールドで、検索するスキルを入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="f566e-139">**特性タイプ** フィールドで、 **証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="f566e-140">**使用可能な特性** フィールドで、検索する証明書のタイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="f566e-141">プロジェクト リソースをプロジェクトに割り当てる</span><span class="sxs-lookup"><span data-stu-id="f566e-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="f566e-142">**すべてのプロジェクト** ページで、 **XYZ アップグレード フェーズ 2** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="f566e-143">**プロジェクト チームとスケジュール** タブの、 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="f566e-144">**ロール** フィールドで、 **チーム メンバー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="f566e-145">**カレンダーから予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="f566e-146">**リソースの使用可能** ページで、 **設定のビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="f566e-147">**ビュー設定を調整する** ページで、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="f566e-148">**日付範囲ビューの形式:** 日</span><span class="sxs-lookup"><span data-stu-id="f566e-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="f566e-149">**可用性の説明の表示:** はい</span><span class="sxs-lookup"><span data-stu-id="f566e-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="f566e-150">**残りのキャパシティを表示:** はい</span><span class="sxs-lookup"><span data-stu-id="f566e-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="f566e-151">リソースのリストで、リソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="f566e-152">**本予約** と **全キャパシティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="f566e-153">リソースを既定のロールに割り当てる</span><span class="sxs-lookup"><span data-stu-id="f566e-153">Assign a resource to a default role</span></span>

<span data-ttu-id="f566e-154">プロジェクト マネージャまたはリソースマ ネージャが、プロジェクトに予約できるリソースをさらにドリル ダウンできるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="f566e-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="f566e-155">既定のロールを既存のリソースまたは新しく取得したリソースに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f566e-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="f566e-156">たとえば、Daniel が採用された際、彼にはビジネス アナリストのロールを満たすための経験とスキルがありました。</span><span class="sxs-lookup"><span data-stu-id="f566e-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="f566e-157">リソース マネージャーは、このロールを Daniel の既定のロールとして割り当てました。</span><span class="sxs-lookup"><span data-stu-id="f566e-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="f566e-158">したがって、リソース マネージャーは、プロジェクトで作業可能なビジネス アナリストのプールに Daniel を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f566e-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="f566e-159">リソースの予約時に、プロジェクト マネージャーは、プロジェクトで作業可能なロール リソースをフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="f566e-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="f566e-160">リソースのフルフィルメント中に複数条件の意思決定分析を実行するときに、この情報を 1 つの条件として使用できます。</span><span class="sxs-lookup"><span data-stu-id="f566e-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="f566e-161">また、他のリソース特性をフィルターに追加して、特定のプロジェクトの特定のスキル、教育、および経験を持つリソースを検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="f566e-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="f566e-162">**シナリオ:** 承認されたプロジェクトが開始され、シニア プロジェクト マネージャーのロールは、プロジェクトの計画ステージで計画されたリソースとして予約されました。</span><span class="sxs-lookup"><span data-stu-id="f566e-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="f566e-163">リソース マネージャーは、シニア プロジェクト マネージャーのロールを満たすリソースを取得しました。</span><span class="sxs-lookup"><span data-stu-id="f566e-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="f566e-164">**リソース リスト** ページで、 **Daniel Goldschmidt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f566e-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="f566e-165">**リソース ロール** ページで、 **新規** を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="f566e-166">**有効:** 現在の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="f566e-167">**有効期限:** **なし** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="f566e-168">**ロール:** **シニア プロジェクト マネージャー** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f566e-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="f566e-169">**保存** を選択した後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f566e-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="f566e-170">**コンピテンシー** タブで、 **ProjectMgmt** スキルと **PMP** 証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="f566e-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
