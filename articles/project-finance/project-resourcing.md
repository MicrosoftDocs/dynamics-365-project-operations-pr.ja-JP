---
title: プロジェクト リソース
description: このトピックでは、プロジェクト リソースについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752792"
---
# <a name="project-resourcing"></a><span data-ttu-id="2f76d-103">プロジェクト リソース</span><span class="sxs-lookup"><span data-stu-id="2f76d-103">Project resourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f76d-104">このトピックでは、プロジェクト リソースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="2f76d-105">プロジェクト計画ステージでのプロジェクト マネージャーとリソース マネージャーの課題の 1 つは、リソースの割り当てです。プロジェクトで作業するために適切なリソースを決定して予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="2f76d-106">Dynamics 365 Finance で、プロジェクトのリソース機能を使用すると、特定のエンゲージメントまたはエンゲージメントの一部のために予約できる一時的なリソースとして扱われるロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-106">In Dynamics 365 Finance, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="2f76d-107">このタイプのリソースでは、プロジェクト マネージャーとリソース マネージャーが次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="2f76d-108">リソースを簡単に一致させることができるように、必要なコンピテンシーを持つロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="2f76d-109">ロールを使用して、予約されたリソースに基づく初期エンゲージメント スケジュールを定義します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="2f76d-110">プロジェクトに割り当てられたロールとリソースに基づいて、コストを見積もり、初期予算を決定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="2f76d-111">ロールを使用して、各エンゲージメントに必要なリソース予約の数を見積もります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="2f76d-112">プロジェクトのライフ サイクル全体に必要なリソースの数を見積もります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="2f76d-113">初期のリソース割り当てを使用して作業分解構造 (WBS) を下書きします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="2f76d-114">[![プロジェクトのライフ サイクル](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f76d-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="2f76d-115">プロジェクトの計画が進むにつれ、計画されたリソースをスタッフが配置されたリソースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="2f76d-116">プロジェクト マネージャーは、プロジェクトのどのステージでも、リソースの予約に戻って更新することができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

## <a name="set-up-project-resources"></a><span data-ttu-id="2f76d-117">プロジェクト リソースの設定</span><span class="sxs-lookup"><span data-stu-id="2f76d-117">Set up project resources</span></span>
<span data-ttu-id="2f76d-118">カレンダーを設定し、それを従業員または作業者に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-118">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="2f76d-119">カレンダーは、プロジェクトとプロジェクト用に予約されているリソースの作業時間をスケジュールするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-119">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="2f76d-120">カレンダーの設定中に、プロジェクト マネージャーはリソースの最適化の一部としてリソースの平準化を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-120">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="2f76d-121">カレンダーのスケジュールに基づいて、リソースに制限をかけることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-121">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="2f76d-122">**カレンダー** ページでカレンダーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-122">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="2f76d-123">作業者をプロジェクト リソースとして設定する場合、リソースを設定する会社で働く作業者から選択できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-123">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="2f76d-124">または、組織内の他の会社から作業者を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-124">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="2f76d-125">これらの作業者は会社間リソースとして知られています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-125">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="2f76d-126">次の手順では、作業者を会社のプロジェクト リソースとして設定する方法と、会社間プロジェクト リソースを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-126">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

### <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="2f76d-127">作業者をプロジェクト リソースとして設定する</span><span class="sxs-lookup"><span data-stu-id="2f76d-127">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="2f76d-128">**作業者**ページで、**作業者**リストから、プロジェクト リソースとして追加する作業者を選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-128">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="2f76d-129">アクション ウィンドウで、**プロジェクト**&gt;**設定**&gt;**プロジェクトの設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-129">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="2f76d-130">カレンダーを選択した後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-130">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="2f76d-131">リソースの既定のプロジェクトを、事前割り当てのタイプとして指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-131">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="2f76d-132">事前割り当ては、リソース マネージャーまたはプロジェクト マネージャーが、リソースが事前に作業するプロジェクトを周知している場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-132">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="2f76d-133">事前割り当ては、プロジェクトのスポンサーまたは顧客の要求に基づくこともできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-133">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="2f76d-134">プロジェクトを事前に割り当てるには、**プロジェクトを割り当てる**ページ、**プロジェクト** タブ、**残りのプロジェクト** リストから適切なプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-134">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

### <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="2f76d-135">会社間リソースを設定する</span><span class="sxs-lookup"><span data-stu-id="2f76d-135">Set up an intercompany resource</span></span>

<span data-ttu-id="2f76d-136">作業者を会社間リソースとして設定する場合、融資会社と借入会社の両方で設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-136">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

<span data-ttu-id="2f76d-137">**融資会社で**</span><span class="sxs-lookup"><span data-stu-id="2f76d-137">**In the lending company**</span></span>

1. <span data-ttu-id="2f76d-138">財務で、融資会社が選択されていることを確認してから、前のセクション「作業者をプロジェクト リソースとして設定」の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-138">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="2f76d-139">**会社間会計**ページで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-139">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="2f76d-140">**法人 ID** フィールドで、融資会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-140">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="2f76d-141">必要に応じて残りのフィールドに入力し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-141">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="2f76d-142">**移転価格** ページで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-142">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="2f76d-143">**借入法人**フィールドで、適切な会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-143">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="2f76d-144">このセクションの冒頭で作成したリソースのみを借用入会社に貸し出すには、**リソース** フィールドで、作成したリソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-144">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="2f76d-145">融資会社のすべてのリソースを借入会社が利用できるようにするには、**リソース** フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-145">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="2f76d-146">**プロジェクト管理と会計パラメータ** ページの**会社間**タブで、**会社間リソースのスケジュールとタイムシートを有効にする**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-146">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

<span data-ttu-id="2f76d-147">**借入会社で**</span><span class="sxs-lookup"><span data-stu-id="2f76d-147">**In the borrowing company**</span></span>

- <span data-ttu-id="2f76d-148">**リソース リスト**ページの検索フィルターで、貸出会社用に作成したリソースの名前を入力して、その名前が借入会社のリソース リストに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-148">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="manage-resource-competencies"></a><span data-ttu-id="2f76d-149">リソース コンピテンシーの管理</span><span class="sxs-lookup"><span data-stu-id="2f76d-149">Manage resource competencies</span></span>
<span data-ttu-id="2f76d-150">リソース コンピテンシーは、リソース管理の不可欠な要素です。</span><span class="sxs-lookup"><span data-stu-id="2f76d-150">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="2f76d-151">コンピテンシーは、スキル、教育、認定、およびプロジェクト経験の正しい残高を持つリソースを決定するためのベースラインとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-151">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="2f76d-152">リソースごとにこの情報を設定し、定期的に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-152">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="2f76d-153">このようにして、プロジェクト リソースの割り当て中に特定のリソース コンピテンシーが一致したときに機能を最大化できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-153">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span>

<span data-ttu-id="2f76d-154">[![スキル、認定、教育、プロジェクトの経験の例](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f76d-154">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span>

<span data-ttu-id="2f76d-155">次の手順では、リソースのコンピテンシーを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-155">The following procedures explain how to set up some of the competencies for a resource.</span></span>

<span data-ttu-id="2f76d-156">作業者のコンピテンシーを設定するには、人事管理の**作業者**リスト ページまたはプロジェクト管理と会計の**リソース** リスト ページのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-156">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="2f76d-157">以下の手順では、人事管理の**作業者**リスト ページを使用しています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-157">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

### <a name="set-up-competencies-certificates"></a><span data-ttu-id="2f76d-158">コンピテンシーの設定: 証明書</span><span class="sxs-lookup"><span data-stu-id="2f76d-158">Set up competencies: Certificates</span></span>

1. <span data-ttu-id="2f76d-159">**作業者**リスト ページで、作業者が証明書情報を追加する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-159">On the **Workers** list page, select the line for the worker to add certificate information for.</span></span>
2. <span data-ttu-id="2f76d-160">アクション ウィンドウの**作業者**タブの**コンピテンシー** グループで、**証明書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-160">On the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Certificates**.</span></span>
3. <span data-ttu-id="2f76d-161">**新規**を選択してから、**証明書タイプ** フィールドで、**PMP** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-161">Select **New**, and then, in the **Certificate type** field, select **PMP**.</span></span>
4. <span data-ttu-id="2f76d-162">**開始日**フィールドで、**2015 年 10 月 1 日**を選択し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-162">In the **Start date** field, select **10/1/2015**, and select **Save**.</span></span>

### <a name="set-up-competencies-skills"></a><span data-ttu-id="2f76d-163">コンピテンシーの設定: スキル</span><span class="sxs-lookup"><span data-stu-id="2f76d-163">Set up competencies: Skills</span></span>

1. <span data-ttu-id="2f76d-164">**作業者**リスト ページで、前の手順で使用した作業者がまだ選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-164">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="2f76d-165">アクション ウィンドウの**作業者**タブ**のコンピテンシー** グループで、**スキル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-165">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Skills**.</span></span>
2. <span data-ttu-id="2f76d-166">**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-166">Select **New**.</span></span>
3. <span data-ttu-id="2f76d-167">**スキル** フィールドで、**プロジェクト管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-167">In the **Skill** field, select **Project management**.</span></span>
4. <span data-ttu-id="2f76d-168">**レベル** フィールドで **5 エキスパート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-168">In the **Level** field, select **5 Expert**.</span></span>
5. <span data-ttu-id="2f76d-169">**レベル日付**フィールドで **2014 年 1- 月 14 日**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-169">In the **Level date** field, select **1-/14/2014**.</span></span>
6. <span data-ttu-id="2f76d-170">**経験年数**フィールドに、**10** と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-170">In the **Years of experience** field, enter **10**.</span></span>
7. <span data-ttu-id="2f76d-171">**保存**を選択した後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="2f76d-172">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="2f76d-172">Create a new project</span></span>
1. <span data-ttu-id="2f76d-173">**プロジェクト管理**ページで、**新しいプロジェクト**を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-173">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="2f76d-174">**プロジェクト タイプ:** 時間と材料</span><span class="sxs-lookup"><span data-stu-id="2f76d-174">**Project type:** Time and material</span></span>
    - <span data-ttu-id="2f76d-175">**プロジェクト名:** XYZ アップグレード フェーズ 2</span><span class="sxs-lookup"><span data-stu-id="2f76d-175">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="2f76d-176">**プロジェクト グループ:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="2f76d-176">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="2f76d-177">**プロジェクト契約 ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="2f76d-177">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="2f76d-178">**プロジェクトの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-178">Select **Create project**.</span></span>

### <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="2f76d-179">リソースをプロジェクトに割り当てる</span><span class="sxs-lookup"><span data-stu-id="2f76d-179">Assign a resource to a project</span></span>

1. <span data-ttu-id="2f76d-180">**作業者**ページで、**作業者**リストから、以前にコンピテンシーを設定した作業者のレコードを選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-180">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="2f76d-181">アクション ウィンドウの**プロジェクト** タブの**設定**グループで、**プロジェクトを割り当てる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-181">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="2f76d-182">**リソース検証プロジェクトの割り当て**ページの、**プロジェクト** タブの、**選択したプロジェクトにプロジェクトを追加**フィールドで、**XYZ アップグレード フェーズ 2**プロジェクトをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-182">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="2f76d-183">**残りのプロジェクト** ウィンドウでプロジェクトを選択し、矢印ボタンを選択して**選択されたプロジェクト** ウィンドウを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-183">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="2f76d-184">必要に応じて、リソースにカテゴリを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-184">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="2f76d-185">カテゴリ タイプは、**原価**または**売上**のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="2f76d-185">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="2f76d-186">カテゴリ タイプは組織によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-186">The category type is determined by your organization.</span></span> <span data-ttu-id="2f76d-187">リソースにカテゴリが割り当てられていない場合、財務はコストと売上の時間単価で既定のカテゴリを検索します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-187">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

### <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="2f76d-188">プロジェクトのリソースとロールの特性を設定する</span><span class="sxs-lookup"><span data-stu-id="2f76d-188">Set up project resource and role characteristics</span></span>

<span data-ttu-id="2f76d-189">プロジェクト マネージャーは、プロジェクト リソース機能を使用して、プロジェクトに必要なロールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-189">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="2f76d-190">リソースが予約されているときに確認済みのリソースがまだ不明な場合は、ロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-190">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="2f76d-191">ロールは、計画されたリソースとして一時的に予約できるため、プロジェクトの計画ステージを続行できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-191">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="2f76d-192">[![ロールの例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f76d-192">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="2f76d-193">**シナリオ:** Contoso は、承認されたプロジェクト チャートを含む時間と材料のプロジェクトを完了するために雇われました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-193">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="2f76d-194">ジュニア プロジェクト マネージャーはまだプロジェクトの範囲を完了しています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-194">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="2f76d-195">リソース マネージャーは現在、新しいプロジェクトで作業するために予約される特定のリソースを識別しています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-195">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="2f76d-196">プロジェクトの重要な性質のため、プロジェクト スポンサーは、ロールの 1 つとしてシニア プロジェクト マネージャーを要求しました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-196">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="2f76d-197">リソース マネージャーは、プロジェクトの計画中にジュニア プロジェクト マネージャーがリソース情報を必要とする場合に備えて、新しいリソースを取得し、システムでのロールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-197">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="2f76d-198">次の手順は、リソース マネージャーがシニア プロジェクト マネージャーのロールを設定し、リソースの特性を関連付ける方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-198">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="2f76d-199">後で、ロールを使用して、必要なリソース コンピテンシーに一致する使用可能なリソースを検索できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-199">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="2f76d-200">**ロールの設定**ページで、**新規**を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-200">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2f76d-201">**ロール ID:** シニア プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="2f76d-201">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="2f76d-202">**説明:** シニア プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="2f76d-202">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="2f76d-203">**作成**を選びます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-203">Select **Create**.</span></span>
3. <span data-ttu-id="2f76d-204">**シニア プロジェクト マネージャー** ロールを選択し、**特性の構成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-204">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="2f76d-205">**特性タイプ** フィールドで、**スキル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-205">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="2f76d-206">**使用可能な特性**フィールドで、検索するスキルを入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-206">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="2f76d-207">**特性タイプ** フィールドで、**証明書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-207">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="2f76d-208">**使用可能な特性**フィールドで、検索する証明書のタイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-208">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

### <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="2f76d-209">プロジェクト リソースをプロジェクトに割り当てる</span><span class="sxs-lookup"><span data-stu-id="2f76d-209">Assign a project resource to a project</span></span>

1. <span data-ttu-id="2f76d-210">**すべてのプロジェクト** ページで、**XYZ アップグレード フェーズ 2** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-210">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2f76d-211">**プロジェクト チームとスケジュール** タブの、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-211">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="2f76d-212">**ロール** フィールドで、**チーム メンバー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-212">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="2f76d-213">**カレンダーから予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-213">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="2f76d-214">**リソースの使用可能**ページで、**設定のビュー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-214">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="2f76d-215">**ビュー設定を調整する**ページで、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-215">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="2f76d-216">**日付範囲ビューの形式:** 日</span><span class="sxs-lookup"><span data-stu-id="2f76d-216">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="2f76d-217">**可用性の説明の表示:** はい</span><span class="sxs-lookup"><span data-stu-id="2f76d-217">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="2f76d-218">**残りのキャパシティを表示:** はい</span><span class="sxs-lookup"><span data-stu-id="2f76d-218">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="2f76d-219">リソースのリストで、リソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-219">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="2f76d-220">**本予約**と**全キャパシティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-220">Select **Hard book** and **Full capacity**.</span></span>


### <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="2f76d-221">リソースを既定のロールに割り当てる</span><span class="sxs-lookup"><span data-stu-id="2f76d-221">Assign a resource to a default role</span></span>

<span data-ttu-id="2f76d-222">プロジェクト マネージャまたはリソースマ ネージャが、プロジェクトに予約できるリソースをさらにドリル ダウンできるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="2f76d-222">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="2f76d-223">既定のロールを既存のリソースまたは新しく取得したリソースに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-223">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="2f76d-224">たとえば、Daniel が採用された際、彼にはビジネス アナリストのロールを満たすための経験とスキルがありました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-224">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="2f76d-225">リソース マネージャーは、このロールを Daniel の既定のロールとして割り当てました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-225">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="2f76d-226">したがって、リソース マネージャーは、プロジェクトで作業可能なビジネス アナリストのプールに Daniel を追加しました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-226">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="2f76d-227">リソースの予約時に、プロジェクト マネージャーは、プロジェクトで作業可能なロール リソースをフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-227">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="2f76d-228">リソースのフルフィルメント中に複数条件の意思決定分析を実行するときに、この情報を 1 つの条件として使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-228">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="2f76d-229">また、他のリソース特性をフィルターに追加して、特定のプロジェクトの特定のスキル、教育、および経験を持つリソースを検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-229">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="2f76d-230">**シナリオ:** 承認されたプロジェクトが開始され、シニア プロジェクト マネージャーのロールは、プロジェクトの計画ステージで計画されたリソースとして予約されました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-230">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="2f76d-231">リソース マネージャーは、シニア プロジェクト マネージャーのロールを満たすリソースを取得しました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-231">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="2f76d-232">**リソース リスト** ページで、**Daniel Goldschmidt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-232">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="2f76d-233">**リソース ロール**ページで、**新規**を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-233">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2f76d-234">**有効:** 現在の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-234">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="2f76d-235">**有効期限:** **なし**と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-235">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="2f76d-236">**ロール:** **シニア プロジェクト マネージャー**と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-236">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="2f76d-237">**保存**を選択した後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-237">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="2f76d-238">**コンピテンシー** タブで、**ProjectMgmt** スキルと **PMP** 証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-238">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

## <a name="set-up-role-based-pricing"></a><span data-ttu-id="2f76d-239">ロール ベース価格を設定する</span><span class="sxs-lookup"><span data-stu-id="2f76d-239">Set up role-based pricing</span></span>
<span data-ttu-id="2f76d-240">すべてのコスト、営業、移転価格は、ロールに設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-240">All cost, sales, and transfer prices can be set up for roles.</span></span>

1. <span data-ttu-id="2f76d-241">**販売価格 (時間)** ページで、**新着**を選択し、有効日を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-241">On the **Sales price (hour)** page, select **New**, and enter an effective date.</span></span>
2. <span data-ttu-id="2f76d-242">**ロール**の列で、ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-242">In the **Role** column, select a role.</span></span>
3. <span data-ttu-id="2f76d-243">**価格**の列で、選択したリソース ロールの価格を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-243">In the **Pricing** column, enter a price for the selected resource role.</span></span>

## <a name="form-a-project-team"></a><span data-ttu-id="2f76d-244">プロジェクト チームのフォーム</span><span class="sxs-lookup"><span data-stu-id="2f76d-244">Form a project team</span></span>
<span data-ttu-id="2f76d-245">以前にプロジェクトで設定されたロールを使用するには、プロジェクト マネージャーがロールをプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-245">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="2f76d-246">プロジェクトには複数のロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-246">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="2f76d-247">混乱を防ぐために、これらのロールには予約時に自動的にラベルが付けられます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-247">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="2f76d-248">たとえば、プロジェクト マネージャーに 3 人のソフトウェア エンジニアが必要な場合、ラベルが自動的に生成される**ソフトウェア エンジニア 1**、**ソフトウェア エンジニア 2**、および**ソフトウェアエンジニア 3**の 3 つのソフトウェア エンジニアのロールがあります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-248">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="2f76d-249">ロールの特性が以前にロールに設定されている場合、それらはリソースの検索中にフィルターとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-249">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="2f76d-250">検索をさらに絞り込むために、必要に応じて追加の特性を追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-250">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="2f76d-251">ビューの設定をカスタマイズして、リソースの空き時間をわかりやすく表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-251">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="2f76d-252">時間ごと、毎日、毎週、毎月、四半期、および年間の可用性を表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-252">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="2f76d-253">リソースの使用可能なキャパシティと残りのキャパシティを表示するオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-253">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="2f76d-254">このオプションは、アクティビティまたはリソースの空き時間に使用可能な時間を見積もる場合の時間管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-254">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="2f76d-255">プロジェクト マネージャーは、ページでロールを選択し、要件に適合する使用可能なリソースがある場合は、ロールを満たすためのリソースを予約することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-255">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="2f76d-256">計画ステージのこの時点では、リソースを予約する必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f76d-256">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="2f76d-257">WBS を作成するときに、プロジェクトのロールをスタッフが配置されたリソースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-257">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="2f76d-258">ロールが WBS のスタッフが配置されたリソースに置き換えられた場合、リソースの設定により、プロジェクト チームのリストとスケジュールが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-258">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="2f76d-259">[![ロールと実際のリソースの両方を含むプロジェクト チーム リスト](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f76d-259">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="2f76d-260">プロジェクト マネージャーには、プロジェクトのリソースを予約するため、**残りのキャパシティ**、**全キャパシティ**、**キャパシティの割合**、および**時間を指定**などのさまざまなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-260">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="2f76d-261">リソースの割り当てが変更された場合、これらの予約オプションはいつでもキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-261">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="2f76d-262">2 種類の予約がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-262">Two types of booking are supported:</span></span>

- <span data-ttu-id="2f76d-263">**本予約** – リソース予約が承認され、指定された期間、エンゲージメントに取り組むことが確認されました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-263">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="2f76d-264">**仮予約** – リソース予約は、指定された期間、エンゲージメントに取り組むように一時的に設定されました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-264">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="2f76d-265">次の手順では、プロジェクト チームの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-265">The following procedure explains how to create a project team.</span></span>

### <a name="create-a-project-team"></a><span data-ttu-id="2f76d-266">プロジェクト チームの作成</span><span class="sxs-lookup"><span data-stu-id="2f76d-266">Create a project team</span></span>

1. <span data-ttu-id="2f76d-267">**すべてのプロジェクト**リスト ページで、プロジェクトを選択してから、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-267">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="2f76d-268">**プロジェクト チームとスケジュール** タブの、**スケジュール終了日**フィールドに、スケジュールの開始日と 1 か月を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-268">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="2f76d-269">たとえば、スケジュールの開始日が 2017 年 6 月 24 日 (2017年6月24日) の場合、**2017 年 7 月 24 日**と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-269">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="2f76d-270">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-270">Select **Add**.</span></span>
4. <span data-ttu-id="2f76d-271">**プロジェクトにロールを追加**ウィンドウの、**ロール** フィールドで、**シニア プロジェクト マネージャー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-271">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="2f76d-272">**必要なコンピテンシー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-272">Select **Required competencies**.</span></span>
6. <span data-ttu-id="2f76d-273">**特性を選択**ウィンドウでは、シニア プロジェクト マネージャー ロールに以前に設定した特性が既定で選択されています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-273">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="2f76d-274">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-274">Select **OK**.</span></span>
7. <span data-ttu-id="2f76d-275">**プロジェクトにロールを追加**ウィンドウの、**リソースの数**フィールドで、**1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-275">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="2f76d-276">**リソース** フィールドで、検索は必要なコンピテンシーを持つすべてのリソースを表示します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-276">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="2f76d-277">**Daniel Goldschmidt** を選択し、次に**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-277">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="2f76d-278">**プロジェクト** ページで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-278">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="2f76d-279">**プロジェクトにロールを追加**ウィンドウの、**ロール** フィールドで、**チーム マネージャー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-279">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="2f76d-280">**リソースの数**フィールドに、**5** と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-280">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="2f76d-281">**作成**を選びます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-281">Select **Create**.</span></span>
12. <span data-ttu-id="2f76d-282">**プロジェクト** ページで、**リソース処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-282">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="resource-capacity-synchronization"></a><span data-ttu-id="2f76d-283">リソース キャパシティの同期</span><span class="sxs-lookup"><span data-stu-id="2f76d-283">Resource capacity synchronization</span></span>
<span data-ttu-id="2f76d-284">リソース同期のプロセスは、カレンダーと基本カレンダーの情報がプロジェクトのリソース スケジュールに流れ込むことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-284">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="2f76d-285">カレンダーが変更された場合、プロセスはプロジェクト リソースのスケジュールに必要な更新を行います。</span><span class="sxs-lookup"><span data-stu-id="2f76d-285">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="2f76d-286">カレンダーのリソース情報は事前に同期されているため、プロセスはパフォーマンスの向上にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-286">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="2f76d-287">したがって、リソース スケジュール情報の更新はより迅速に行われます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-287">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="2f76d-288">プロセスは一度に 1 つではなくバッチとしてスケジュールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-288">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="2f76d-289">それ以外の場合は、情報が最後に同期された包括的な日付をユーザーが忘れるというリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-289">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="2f76d-290">包括的な日付を使用しない場合、日付の同期中にギャップが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-290">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="2f76d-292">リソース キャパシティ ロールアップの同期</span><span class="sxs-lookup"><span data-stu-id="2f76d-292">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="2f76d-293">同期プロセスは、すべてのリソース カレンダー情報を同期するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-293">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="2f76d-294">この情報には、プロジェクトのリソース カレンダーのキャパシティ テーブルへの変更に関する基本カレンダー情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f76d-294">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="2f76d-295">新しいリソースがプロジェクトに追加された場合、同期は、更新されたカレンダー情報が使用可能であることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-295">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="2f76d-296">この同期はいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-296">This synchronization can be done at any time.</span></span>

<span data-ttu-id="2f76d-297">バッチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-297">We recommend that you use a batch.</span></span> <span data-ttu-id="2f76d-298">オプションは、確保済能力の同期中に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-298">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="2f76d-299">**プロジェクト管理と会計**&gt;**定期的**&gt;**キャパシティの同期**&gt;**リソース キャパシティのロールアップの同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-299">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="2f76d-300">次の表にオプション設定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-300">Set the options in the following table.</span></span>

    | <span data-ttu-id="2f76d-301">オプション</span><span class="sxs-lookup"><span data-stu-id="2f76d-301">Option</span></span>      | <span data-ttu-id="2f76d-302">内容</span><span class="sxs-lookup"><span data-stu-id="2f76d-302">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="2f76d-303">期間コード</span><span class="sxs-lookup"><span data-stu-id="2f76d-303">Period code</span></span> | <span data-ttu-id="2f76d-304">必要に応じて、総勘定元帳の日付範囲コードを選択して、リソース キャパシティ ロールアップの同期プロセスの開始日と終了日を設定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-304">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="2f76d-305">開始日</span><span class="sxs-lookup"><span data-stu-id="2f76d-305">Start date</span></span>  | <span data-ttu-id="2f76d-306">リソース キャパシティ ロールアップの同期プロセスの開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-306">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="2f76d-307">終了日</span><span class="sxs-lookup"><span data-stu-id="2f76d-307">End date</span></span>    | <span data-ttu-id="2f76d-308">リソース キャパシティ ロールアップの同期プロセスの終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-308">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="2f76d-309">[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f76d-309">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

## <a name="set-up-roles-on-wbs-templates"></a><span data-ttu-id="2f76d-310">WBS テンプレートにロールを設定する</span><span class="sxs-lookup"><span data-stu-id="2f76d-310">Set up roles on WBS templates</span></span>
<span data-ttu-id="2f76d-311">プロジェクト マネージャーは、新しいプロジェクトの WBS を作成するときに適用できる WBS テンプレートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-311">Project managers can set up WBS templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="2f76d-312">プロジェクト マネージャーは、テンプレートを作成するときにロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-312">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="2f76d-313">次の手順を使用して、WBS テンプレートにロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-313">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="2f76d-314">**プロジェクト管理と会計**&gt;**設定**&gt;**プロジェクト**&gt;**作業分解構造テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-314">Select **Project management and accounting** &gt; **Setup** &gt; **Projects** &gt; **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="2f76d-315">選択した WBS テンプレートの**詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-315">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="2f76d-316">リストでタスクを選択し、**ロール** フィールドで、タスクに割り当てるロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-316">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

### <a name="work-with-a-wbs"></a><span data-ttu-id="2f76d-317">WBS を使用する</span><span class="sxs-lookup"><span data-stu-id="2f76d-317">Work with a WBS</span></span>

<span data-ttu-id="2f76d-318">新しい WBS を作成、または既存の WBS テンプレートから WBS をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-318">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="2f76d-319">プロジェクト マネージャーは、WBS の新しいタスクにロールを割り当てることにより、リソースを簡単に管理できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-319">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="2f76d-320">ロールは、リソースが取得された後、またはタスクで作業するために確認されたリソースが確認された後に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-320">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="2f76d-321">この柔軟性により、プロジェクト マネージャーは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-321">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="2f76d-322">WBS 作業パッケージに必要なリソースの数を特定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-322">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="2f76d-323">プロジェクト コストを見積もります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-323">Estimate project costs.</span></span>
- <span data-ttu-id="2f76d-324">暫定予算を決定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-324">Determine a preliminary budget.</span></span>
- <span data-ttu-id="2f76d-325">ロールとリソースに基づいて、活動期間を見積もります。</span><span class="sxs-lookup"><span data-stu-id="2f76d-325">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="2f76d-326">使用可能なプロジェクト情報に基づいて、いくつかのプロジェクト管理計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-326">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="2f76d-327">リソース機能をより効果的に使用するために、WBS に追加オプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="2f76d-327">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f76d-328">オプション</span><span class="sxs-lookup"><span data-stu-id="2f76d-328">Option</span></span></th>
<th><span data-ttu-id="2f76d-329">内容</span><span class="sxs-lookup"><span data-stu-id="2f76d-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f76d-330">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="2f76d-330">Resource assignments</span></span></td>
<td><span data-ttu-id="2f76d-331">WBS でタスクに割り当てられたリソース、日付、時間数、予約の種類を表示します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-331">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f76d-332">チームを自動生成</span><span class="sxs-lookup"><span data-stu-id="2f76d-332">Auto generate team</span></span></td>
<td><span data-ttu-id="2f76d-333">タスクに関連付けられているロールを使用して、計画されたリソースを自動的に追加します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-333">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="2f76d-334">財務は、ロールに基づく複数条件の意思決定分析を使用して、計画されたリソースを自動的に提案します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-334">Finance automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="2f76d-335">WBS でタスクにロールと工数 (時間) が設定し、構造がリリースされた後、<strong>チームの自動生成</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-335">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="2f76d-336">計画リソースの必要な数が WBS と<strong>プロジェクトとチームのスケジュール</strong> タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-336">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f76d-337">リソース (ドロップダウン リスト)</span><span class="sxs-lookup"><span data-stu-id="2f76d-337">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="2f76d-338"><strong>リソース割り当てを起動する</strong>ページで、指定した期間に基づいて、本予約または仮予約へのリソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-338">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="2f76d-339">ビュー設定を調整し、リソース活動の期間を表示および設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-339">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="2f76d-340">以下のオプションを使用して、作業パッケージ レベルでリソースを選択して割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-340">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="2f76d-341"><strong>同意する</strong> – タスクに割り当てられているリソースへの変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-341"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="2f76d-342"><strong>キャンセル</strong> – タスクに割り当てられているリソースへの変更をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-342"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="2f76d-343"><strong>自動的に割り当てる</strong> – 一致するロールを持つ使用可能なスタッフが配置されたリソースが自動的に選択され、選択したタスクに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-343"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="2f76d-344">**すべてのプロジェクト** ページで、**XYZ アップグレード フェーズ 2** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-344">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2f76d-345">**計画**&gt;**活動**&gt;**作業分解構造**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-345">Select **Plan** &gt; **Activities** &gt; **Work breakdown structure**.</span></span>
3. <span data-ttu-id="2f76d-346">**新着**を選択し、次のレベル 1 の活動を WBS に追加します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-346">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="2f76d-347">開始</span><span class="sxs-lookup"><span data-stu-id="2f76d-347">Initiating</span></span>
    - <span data-ttu-id="2f76d-348">プランニング</span><span class="sxs-lookup"><span data-stu-id="2f76d-348">Planning</span></span>
    - <span data-ttu-id="2f76d-349">実行中</span><span class="sxs-lookup"><span data-stu-id="2f76d-349">Executing</span></span>
    - <span data-ttu-id="2f76d-350">監視とコントロール</span><span class="sxs-lookup"><span data-stu-id="2f76d-350">Monitoring and Control</span></span>
    - <span data-ttu-id="2f76d-351">閉じる​​</span><span class="sxs-lookup"><span data-stu-id="2f76d-351">Close</span></span>

4. <span data-ttu-id="2f76d-352">次の図に示すように、日付と工数 (時間) を設定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-352">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="2f76d-353">[![日付と工数の設定](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f76d-353">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="2f76d-354">**開始**タスク ライン、**ロール** フィールド、**シニア プロジェクト マネージャー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-354">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="2f76d-355">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-355">Select **Publish**.</span></span>
7. <span data-ttu-id="2f76d-356">同じラインの、**リソース** フィールドで、**Daniel Goldschmidt**、次に**同意**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-356">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="2f76d-357">**計画**タスク ラインを選択し、**ロール**フィールドで、**ビジネス アナリスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-357">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="2f76d-358">**公開**を選択し、次に**チームの自動生成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-358">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="2f76d-359">表示されるメッセージ ボックスで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-359">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="2f76d-360">**リソース** フィールドで、値が**ビジネス アナリスト 1** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-360">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="2f76d-361">**ビジネス アナリスト 1** リソースのために、検索を開き、**リソース割り当ての起動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-361">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="2f76d-362">次に、タスクの作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-362">Then select a worker for the task.</span></span>
13. <span data-ttu-id="2f76d-363">**ソフト割り当て**&gt;**全キャパシティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-363">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="2f76d-364">リソースの数が 1 のままであるため、指定したリソースが 2 であるという警告は表示されません。</span><span class="sxs-lookup"><span data-stu-id="2f76d-364">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="2f76d-365">**作業分解構造**ページで、WBS でのリソース割り当てを検証し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-365">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>

## <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="2f76d-366">計画されたリソースのリソース フルフィルメント</span><span class="sxs-lookup"><span data-stu-id="2f76d-366">Resource fulfillment for planned resources</span></span>
<span data-ttu-id="2f76d-367">プロジェクト マネージャーは、プロジェクトに必要なリソースのロールを計画できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-367">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="2f76d-368">リソース マネージャーは、これらの計画されたリソースを、**リソース フルフィルメント** ページの要求として確認し、実際のリソースを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-368">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1. <span data-ttu-id="2f76d-369">**すべてのプロジェクト** ページで、**XYZ アップグレード フェーズ 2** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-369">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2f76d-370">**プロジェクト**を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-370">Select **Project**, and then select **Edit**.</span></span>
3. <span data-ttu-id="2f76d-371">**プロジェクト チームとスケジュール** タブの、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-371">On the **Project team and scheduling** tab, select **Add**.</span></span>
4. <span data-ttu-id="2f76d-372">**ロールの追加**ダイアログ ボックスで、**ソフトウェア開発者**のロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-372">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
5. <span data-ttu-id="2f76d-373">**作成**を選択し、プロジェクト ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-373">Select **Create**, and then close the project page.</span></span>
6. <span data-ttu-id="2f76d-374">**リソース フルフィルメント** ページで、**XYZ アップグレード プロジェクト フェーズ 2** プロジェクトのための**ソフトウェア開発者 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-374">On the **Resource fulfillment** page, select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
7. <span data-ttu-id="2f76d-375">作業者を選択し、**割り当て**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-375">Select a worker, and then select **Assign**.</span></span>
8. <span data-ttu-id="2f76d-376">**ソフトウェア開発者 1**のラインが **XYZ アップグレード プロジェクト フェーズ 2** プロジェクトのために削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-376">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
9. <span data-ttu-id="2f76d-377">**プロジェクト チームとスケジュール** タブで、**XYZ アップグレード フェーズ 2**プロジェクトの場合、前のステップで選択した作業者が**ソフトウェア開発者**として追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-377">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in the previous step has been added as **Software developer**.</span></span>

## <a name="requests-for-project-resources"></a><span data-ttu-id="2f76d-378">プロジェクト リソースの要求</span><span class="sxs-lookup"><span data-stu-id="2f76d-378">Requests for project resources</span></span>
<span data-ttu-id="2f76d-379">プロジェクト リソース スケジュールの機能では、リソース マネージャーのみがエンゲージメントまたはプロジェクトのスタッフが配置されたリソースを配布できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-379">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="2f76d-380">この機能を有効にするには、次のタスクを完了するか、それらが完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-380">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="2f76d-381">番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-381">Set up number sequences.</span></span>
- <span data-ttu-id="2f76d-382">プロジェクト管理および会計ワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-382">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="2f76d-383">リソース要求ワークフローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="2f76d-383">Enable resource request workflows.</span></span>

<span data-ttu-id="2f76d-384">上記のタスクが完了したら、必要に応じて次のタスクを完了できます。</span><span class="sxs-lookup"><span data-stu-id="2f76d-384">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="2f76d-385">仮予約されたスタッフが配置されたリソースからリソース要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-385">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="2f76d-386">リソース要求を監視します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-386">Monitor resource requests.</span></span>
- <span data-ttu-id="2f76d-387">リソース要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-387">Fulfill resource requests.</span></span>
- <span data-ttu-id="2f76d-388">WBS からスタッフが配置されたリソースを要求します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-388">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="2f76d-389">スタッフが配置されたリソースをリクエストせずに、プロジェクトにリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-389">Book resources to a project without having a request for a staffed resource.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="2f76d-390">プロジェクト チームを監視する</span><span class="sxs-lookup"><span data-stu-id="2f76d-390">Monitor project teams</span></span>
1. <span data-ttu-id="2f76d-391">**すべてのプロジェクト** ページで、**XYZ アップグレード フェーズ 2** プロジェクトの **プロジェクト ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-391">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2f76d-392">**プロジェクト チームとスケジュール** FastTab で、リストされているプロジェクト リソースが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f76d-392">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
