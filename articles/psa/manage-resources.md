---
title: リソースの管理
description: このトピックでは、リソースの管理方法について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079469"
---
# <a name="manage-resources"></a><span data-ttu-id="d60cd-103">リソースの管理</span><span class="sxs-lookup"><span data-stu-id="d60cd-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d60cd-104">Dynamics 365 Project Service Automation には、 組織全体のリソース需要と稼働率の視覚的概要を提供するリソース マネージャーのダッシュボードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d60cd-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="d60cd-105">次の情報を視覚化するために、このダッシュボードのグラフを使用できます:</span><span class="sxs-lookup"><span data-stu-id="d60cd-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="d60cd-106">**リソース需要** – **アクティブなリソース要求** グラフには、送信されたリソースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="d60cd-107">リソースは、ロールまたはプロジェクトごとに集計されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="d60cd-108">**未送信リソース需要** – **未割り当てリソース需要** グラフには、送信されていないすべてのリソース要件が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="d60cd-109">これにより、リソース マネージャーは、確定ではなく、リソース 要求を通じて送信される可能性のある需要の表示に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="d60cd-110">**先週の請求可能稼働率** – **ロール別稼働率** グラフ には、組織のロール別ターゲット請求可能稼働率に対してロール別実請求可能稼働率の割合が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d60cd-111">**ロール別稼働率** グラフを使用できるようにするには、 UpdateRoleUtilization ワークフローを実行するジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="d60cd-112">この定期的なジョブは 7 日ごとに実行され、過去 7 日間の請求可能稼働率が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="d60cd-113">結果は、ロールごとに集計されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="d60cd-114">プロジェクト チーム メンバーの管理</span><span class="sxs-lookup"><span data-stu-id="d60cd-114">Manage project team members</span></span>

<span data-ttu-id="d60cd-115">プロジェクト管理者は、リソース マネージャー ダッシュボードを使用して、プロジェクトのリソースを管理できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="d60cd-116">たとえば、プロジェクトにチーム メンバーを直接追加し、汎用リソースによって取得されたリソース要件を満たすためにチーム メンバーを予約することができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="d60cd-117">プロジェクトにチーム メンバーを直接追加する</span><span class="sxs-lookup"><span data-stu-id="d60cd-117">Add a team member directly to a project</span></span>

<span data-ttu-id="d60cd-118">プロジェクトにチーム メンバーを直接追加するためには、 **プロジェクト** ページの **チーム** タブで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="d60cd-119">**簡易作成:プロジェクト チーム メンバー** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="d60cd-120">このダイアログ ボックスでは、次のタスクを実行できます:</span><span class="sxs-lookup"><span data-stu-id="d60cd-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="d60cd-121">**名前付きリソースの予約** –  **予約可能リソース** フィールドでリソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="d60cd-122">次に、ロールを選択し、期間を設定し、割り当て方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="d60cd-123">選択した名前付きリソースは、選択した割り当て方法とリソース カレンダーを使用してプロジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="d60cd-124">**汎用リソースの追加** – **予約可能リソース** フィールドを空白ままにし、ロールを選択し、期間を設定して、優先割り当て方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="d60cd-125">汎用リソースは、チームに名前付きリソースを予約するために使用される需要パターンを保持するプレースホルダーとしてチームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="d60cd-126">要件はプロジェクトにカレンダーに従って作成されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="d60cd-127">**リソース キャパシティを消費せずに名前付きリソースをチームに追加する** – **予約可能リソース** で をリソース選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="d60cd-128">次に、期間を選択し、割り当て方法として **なし** ​​ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="d60cd-129">リソースはチームに追加されますが、リソース 容量は予約によって消費されません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="d60cd-130">チーム メンバーを予約して、汎用リソースのリソース要件を満たす</span><span class="sxs-lookup"><span data-stu-id="d60cd-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="d60cd-131">PSAで、プロジェクト チームで汎用リソースを予約し、ロール、必要な容量、容量の配分方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="d60cd-132">リソース要件では、汎用リソースに関連付けられる属性を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="d60cd-133">これらの属性には、必須スキル、優先組織単位および優先リソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="d60cd-134">開発者が、汎用リソースで必要なスキルを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d60cd-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="d60cd-135">**プロジェクト** ページの **チーム** タブで、汎用リソースを予約するために **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![チームで予約された汎用リソース](media/Resource-Management-image9.png)

2. <span data-ttu-id="d60cd-137">**すべてのチーム メンバー** ビューの **リソース要件** 列で、リンクを選択して、汎用リソースに必要なスキルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![要件リンク](media/Resource-Management-image10.png)

3. <span data-ttu-id="d60cd-139">表示する **リソース要件** ページの **スキル** グリッドで、省略記号 ( **...** ) を選択し、 **新しい要件特性を追加** を選択して、開発者のために必要なスキルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![新しい要件特性コマンドを追加](media/Resource-Management-image11.png)

4. <span data-ttu-id="d60cd-141">表示する **簡易作成: 要件特性** ダイアログ ボックスの **特性** フィールドで、 必要なスキルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="d60cd-142">次に、 **評価値** フィールドで、そのスキルの習熟レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="d60cd-143">最後に、 **リソース要件** フィールドに、組織単位または名前付きリソースからリソースを調達するための要件を設定します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="d60cd-144">終了したら、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-144">When you've finished, select **Save**.</span></span>

    ![簡易作成: 要件特性 ダイアログ ボックス](media/Resource-Management-image12.png)

5. <span data-ttu-id="d60cd-146">**リソース要件** ページでは、リソース要件を満たすために **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![リソース要件 ページのボタンを登録する](media/Resource-Management-image13.png)

    <span data-ttu-id="d60cd-148">**すべてのチーム メンバー** グリッドで汎用リソースを選択し、 **予約** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![すべてのチーム メンバー グリッド上部の予約ボタン](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="d60cd-150">この例では、汎用リソースには予約がないため、要求された時間は40時間ですが、実際の予約時間はありません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="d60cd-151">また、汎用リソースがチームに直接追加されるので、割り当てられた時間はありません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="d60cd-152">タスク割り当てを使用して追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="d60cd-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="d60cd-153">**スケジュール アシスタント** ページでは、リソース要件で指定されている要件に応じて使用可能なリソースにフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="d60cd-154">リソースは、スケジュール ボードで指定された並べ替えパラメーターに従って並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![スケジュール アシスタント ページ](media/Resource-Management-image15.png)

    <span data-ttu-id="d60cd-156">頻繁に使用されるフィルターは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="d60cd-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="d60cd-157">**評価と特性** – 習熟度の評価に加えて、スキル、認定資格、およびその他のリソース品質でフィルタします。</span><span class="sxs-lookup"><span data-stu-id="d60cd-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="d60cd-158">**ロール** – 予約可能リソースに割り当てられた既定のロールでフィルタします。</span><span class="sxs-lookup"><span data-stu-id="d60cd-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="d60cd-159">**組織単位** – 予約可能リソースを割り当てられている組織単位でフィルタします。</span><span class="sxs-lookup"><span data-stu-id="d60cd-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="d60cd-160">最初の要件検索の結果に満足でいない場合、フィルター条件を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="d60cd-161">左側の **フィルター ビュー** ウィンドウを展開し、 **検索** を選択し、追加リソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![ビュー ウィンドウ フィルター](media/Resource-Management-image16.png)

7. <span data-ttu-id="d60cd-163">結果の並べ替え方法を変更するには、 **並べ替え** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-163">To change how the results are sorted, select **Sort**.</span></span>

    ![コマンドの並べ替え](media/Resource-Management-image17.png)

8. <span data-ttu-id="d60cd-165">グリッドの上部に表示されるように要件に指定されている要求に従ってリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="d60cd-166">グリッド内のセルの選択を解除して、リソース キャパシティをオープンのままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="d60cd-167">一度に 1 つのリソースのみ予約済みとして選択できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="d60cd-168">選択したリソースを予約するには、 **予約** を選択し、スケジュール ボードを開いたままにしておくと、追加のリソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="d60cd-169">または、 **予約して終了** を選択して、選択したリソースを予約し、スケジュール ボードを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![予約するリソース](media/Resource-Management-image19.png)

    <span data-ttu-id="d60cd-171">予約時間に関する通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="d60cd-172">需要インジケーターは、予約要件がどれだけ満たされ、どれだけ残っているかを表示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="d60cd-173">選択したリソースの容量がどれだけ消費されているかも確認できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="d60cd-174">**展開** を選択して、リソース予約に関する詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="d60cd-175">**すべてのチーム メンバー** ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="d60cd-176">グリッドで、汎用リソースが名前付きリソースに置き換えられ、40時間がそのリソースの予約済みとしてリストされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d60cd-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![すべてのチーム メンバー グリッドの更新](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="d60cd-178">チームで直接予約されたため、割り当てられた時間は表示されません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="d60cd-179">タスク割り当てを使用して予約されていません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="d60cd-180">汎用リソースをタスクを割り当て、リソース要件を生成する</span><span class="sxs-lookup"><span data-stu-id="d60cd-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="d60cd-181">PSAで、タスクを作成し、それらに汎用リソースを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="d60cd-182">このようにして、スケジュールと財務数値を見積ながら、リソース需要はプレースホルダーで表すことができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="d60cd-183">次に汎用リソースのリソース要件を生成して、達成することができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="d60cd-184">**プロジェクト** ページの **スケジュール** タブで **追加** を選択して、タスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![新しいタスクが作成されました](media/Resource-Management-image21.png)

2. <span data-ttu-id="d60cd-186">**リソース** フィールドで **リソース選択** 記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="d60cd-187">リソース選択が表示され、プロジェクトの既存のチーム メンバーを表示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![リソース選択](media/Resource-Management-image22.png)

3. <span data-ttu-id="d60cd-189">新しい汎用リソースの名前を入力し、 **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![入力された新しい汎用リソースの名前](media/Resource-Management-image23.png)

4. <span data-ttu-id="d60cd-191">表示する **簡易作成: プロジェクト チーム メンバー** ダイアログ ボックスの **ロール** フィールドで、 汎用リソースのロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="d60cd-192">**リソース単位** フィールドでは、汎用リソースの組織単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="d60cd-193">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-193">Then select **Save**.</span></span>

    ![簡易作成: プロジェクト チーム メンバー ダイアログ ボックス](media/Resource-Management-image24.png)

    <span data-ttu-id="d60cd-195">汎用チーム メンバーがタスクに割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="d60cd-195">The generic team member is now assigned to the task.</span></span>

    ![タスクに割り当てられた汎用チーム メンバー](media/Resource-Management-image25.png)

    <span data-ttu-id="d60cd-197">**チーム** タブで、新しい汎用チーム メンバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="d60cd-198">時間のみが割り当てられていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d60cd-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="d60cd-199">これらの時間は、汎用チーム メンバーに割り当てられたすべてのタスクの合計です。</span><span class="sxs-lookup"><span data-stu-id="d60cd-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="d60cd-200">汎用チーム メンバーには、まだ必要な時間やリソース要件がありません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![チーム タブの汎用チーム メンバー](media/Resource-Management-image26.png)

5. <span data-ttu-id="d60cd-202">リソース選択を使用して、そのほかのタスクに汎用チーム メンバーを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![リソース選択の汎用チーム メンバー](media/Resource-Management-image27.png)

    <span data-ttu-id="d60cd-204">タスクへの汎用リソースの割り当てが完了したら、汎用リソースのリソース要件を生成できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="d60cd-205">**チーム** タブで、汎用リソースを選択して、 **要件の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![要件コマンドの生成](media/Resource-Management-image28.png)

    <span data-ttu-id="d60cd-207">要件が生成されると、汎用チーム メンバーには、リソース要件への所要時間とリンクがあります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![リソース要件リンク](media/Resource-Management-image29.png)

    <span data-ttu-id="d60cd-209">名前付きリソースを予約すると、汎用リソースがチームから削除され、名前付きリソースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![名前付きリソースによって置き換えられた汎用リソース](media/Resource-Management-image30.png)

    <span data-ttu-id="d60cd-211">**スケジュール** タブで、汎用リソースの割り当てが削除され、名前付きリソースとに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![スケジュール タブで、名前付きリソースに置き換えられた汎用リソースの割り当て](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="d60cd-213">この動作は、名前付きリソースが汎用リソース要件に対して完全に予約されている場合のみに発生します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="d60cd-214">名前付きリソースが汎用リソース要件を部分的に置き換えるか、複数の名前付きリソースが汎用リソース要件を置き換える場合、汎用リソースはタスクに割り当てられたままになります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="d60cd-215">次の図では、 80 時間のタスクが 5 日間 ( 5 日間で 1 日 16 時間) 計画されており、 **機能** という名の汎用リソースに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="d60cd-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![機能汎用リソースに割り当てられた 80 時間、 5 日間のタスク](media/Resource-Management-image32.png)

    <span data-ttu-id="d60cd-217">要件を生成すると、 5 日間で 80 時間です。</span><span class="sxs-lookup"><span data-stu-id="d60cd-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![5 日間 80 時間で生成された要件](media/Resource-Management-image33.png)

    <span data-ttu-id="d60cd-219">使用可能なリソースが 1 日に 8 時間しか機能しないため、要件を実現するには、 2 つのリソースが必要です。</span><span class="sxs-lookup"><span data-stu-id="d60cd-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![2番目のリソース](media/Resource-Management-image35.png)

    <span data-ttu-id="d60cd-221">**チーム** タブでは、汎用リソースに必要な時間がありませんが、割り当てられた時間は、フルフィルメントを構成する 2 つの名前付きリソースとともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![チーム タブの 2 つの名前付きリソース](media/Resource-Management-image36.png)

    <span data-ttu-id="d60cd-223">**スケジュール** タブでは、汎用リソースがタスクに割り当てられたままになります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![スケジュール タブの汎用リソース](media/Resource-Management-image37.png)

<span data-ttu-id="d60cd-225">PSAは、その動作により予測が困難なスケジュールが生成されるため、両方のリソースにタスクを割り当てません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="d60cd-226">この単純な例では、 2 つのリソース間で時間を均等に分けることは簡単です。</span><span class="sxs-lookup"><span data-stu-id="d60cd-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="d60cd-227">ただし、複数のタスクと複数のリソースを含むより複雑なシナリオでは、PSAは複数のリソースに対して受け取った予約を複数のタスクにどのように割り当てるべきかについて想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="d60cd-228">したがって、これらのシナリオでは、プロジェクト管理者が複数の予約を解析し、必要に応じて割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="d60cd-229">予約を割り当てるには、プロジェクト管理者が汎用リソースから名前付きリソースにタスクを割り当て、 **調整** ビューを使用して、割り当てが予約と連動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="d60cd-230">リソース要件の編集</span><span class="sxs-lookup"><span data-stu-id="d60cd-230">Edit a resource requirement</span></span>

<span data-ttu-id="d60cd-231">リソース要件を作成した後、プロジェクト管理者やリソース マネージャーは、スケジュール ボード使用時に、検索条件を絞り込むため詳細を編集する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="d60cd-232">リソース要件を編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d60cd-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="d60cd-233">**プロジェクト** ページの **チーム** タブで、汎用リソースの要件へのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="d60cd-234">表示される **リソース要件** ページで、複数の属性を更新できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="d60cd-235">ここに例を示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-235">Here are some examples:</span></span>

    - <span data-ttu-id="d60cd-236">Name</span><span class="sxs-lookup"><span data-stu-id="d60cd-236">Name</span></span>
    - <span data-ttu-id="d60cd-237">開始日</span><span class="sxs-lookup"><span data-stu-id="d60cd-237">From Date</span></span>
    - <span data-ttu-id="d60cd-238">終了日</span><span class="sxs-lookup"><span data-stu-id="d60cd-238">To Date</span></span>
    - <span data-ttu-id="d60cd-239">期間</span><span class="sxs-lookup"><span data-stu-id="d60cd-239">Duration</span></span>
    - <span data-ttu-id="d60cd-240">リソースの種類</span><span class="sxs-lookup"><span data-stu-id="d60cd-240">Resource Type</span></span>

<span data-ttu-id="d60cd-241">**リソース要件** ページで、プロジェクト管理者やリソース マネージャーは、以下の情報も定義できます:</span><span class="sxs-lookup"><span data-stu-id="d60cd-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="d60cd-242">スキル</span><span class="sxs-lookup"><span data-stu-id="d60cd-242">Skills</span></span>
- <span data-ttu-id="d60cd-243">ロール</span><span class="sxs-lookup"><span data-stu-id="d60cd-243">Roles</span></span>
- <span data-ttu-id="d60cd-244">リソースの基本設定</span><span class="sxs-lookup"><span data-stu-id="d60cd-244">Resource preferences</span></span>
- <span data-ttu-id="d60cd-245">優先する組織単位</span><span class="sxs-lookup"><span data-stu-id="d60cd-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="d60cd-246">プロジェクトに予約した後にリソース予約を更新する</span><span class="sxs-lookup"><span data-stu-id="d60cd-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="d60cd-247">プロジェクト チームに、汎用リソースまたは名前付きリソースを追加したら、リソースの予約を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="d60cd-248">**プロジェクト** ページの **チーム** タブで、チームメンバーを選択し、 **予約の維持** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![選択したチーム メンバー用に開かれたスケジュール ボード](media/Resource-Management-image40.png)

    <span data-ttu-id="d60cd-250">スケジュール ボードが表示され、プロジェクト チーム メンバーの予約が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="d60cd-251">チーム メンバーのレコードを展開して、チーム メンバーの容量を消費しているこのプロジェクトおよびほかのプロジェクトに対して予約された時間を表示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="d60cd-252">予約を選択およびドラッグして、延長または短縮します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="d60cd-253">予約を調整するため、 **リソース予約の作成** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![リソース予約ダイアログ ボックスの作成](media/Resource-Management-image41.png)

3. <span data-ttu-id="d60cd-255">予約を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="d60cd-255">Right-click the booking.</span></span> <span data-ttu-id="d60cd-256">そして、ショートカット メニューを使用して、次の操作を完了できます:</span><span class="sxs-lookup"><span data-stu-id="d60cd-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="d60cd-257">予約状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-257">Change the booking status.</span></span>
    - <span data-ttu-id="d60cd-258">予約を編集します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-258">Edit the booking.</span></span>
    - <span data-ttu-id="d60cd-259">プロジェクト チームのリソースを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="d60cd-260">予約状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-260">Change the booking status</span></span>

<span data-ttu-id="d60cd-261">既定またはカスタムの予約状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-261">You can change any default or custom booking status.</span></span>

![ステータス コマンドの変更](media/Resource-Management-image42.png)

<span data-ttu-id="d60cd-263">次の状態がPSAにあります:</span><span class="sxs-lookup"><span data-stu-id="d60cd-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="d60cd-264">**キャンセル済み** – この状態はリソースの予約をキャンセルし、リソースの容量を解放します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="d60cd-265">**本予約** – この状態はリソースの容量を消費します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="d60cd-266">通常、予約は、 **プロジェクト** ページの **すべてのチーム メンバー** グリッドから **予約の維持** すると、この状態になります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="d60cd-267">**仮予約** – この状態は、チームに対してリソースを追加しますが、リソースの容量を消費しません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="d60cd-268">これは、リソースは潜在的な作業に予約されていますが、そのほかの業務で必要な場合は、まだ容量があることを示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="d60cd-269">全体的なリソースの可用性の観点から、仮予約は本予約とは別の状態にあります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="d60cd-270">**提案済み** – この状態は、リソースに対するリソース マネージャーまたはプロジェクト マネージャーの提案を表します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="d60cd-271">提案はリソースの容量を消費せず、リソースはプロジェクト チームに追加されません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="d60cd-272">チームでリソースを本予約するには、プロジェクト管理者の提案を受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="d60cd-273">リソース要求の送信</span><span class="sxs-lookup"><span data-stu-id="d60cd-273">Submit resource requests</span></span>

<span data-ttu-id="d60cd-274">リソース要求は、リソース マネージャーによって実行される必要がある需要 (リソース要件) を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="d60cd-275">チームに既に存在する汎用リソースについては、リソース要求を直接送信できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="d60cd-276">リソース要求は、 2 つの方法で実行できます:</span><span class="sxs-lookup"><span data-stu-id="d60cd-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="d60cd-277">リソース マネージャーは、要求を直接処理します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="d60cd-278">この場合、汎用リソースは、名前付きリソースを持つ本予約に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="d60cd-279">リソース マネージャーは、プロジェクト管理者にリソースを提案し、プロジェクト管理者は、提案されたリソースを承認、または却下します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="d60cd-280">リソース要求の直接実行</span><span class="sxs-lookup"><span data-stu-id="d60cd-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="d60cd-281">リソース要件が生成されると、プロジェクト管理者はリソースを選択し、 **要求の送信** を選択することによって汎用リソースのリソース要求を送信できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![要求の送信 ボタン](media/Resource-Management-image45.png)

<span data-ttu-id="d60cd-283">リソースに関するコメントは、要求を実行するリソース マネージャーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="d60cd-284">要求を送信した後、チーム メンバーの **状態** フィールドは、 **送信済み** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![任意コメントの入力](media/Resource-Management-image46.png)

<span data-ttu-id="d60cd-286">リソース マネージャーが要求を処理すると、汎用チーム メンバーは **すべてのチーム メンバー** グリッドの名前付きリソースによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![すべてのチーム メンバー グリッドで名前付きリソースによって置き換えられた汎用チーム メンバー](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="d60cd-288">リソース要求にリソース提案を使用する</span><span class="sxs-lookup"><span data-stu-id="d60cd-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="d60cd-289">リソース要求でリソースを直接予約する代わりに、リソース マネージャーは、プロジェクト マネージャーにリソースを提案できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="d60cd-290">リソース マネージャーは、要件に完全に一致しない場合にこのオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="d60cd-291">リソース マネージャーにリソースを提案すると、プロジェクト管理者は、汎用チーム メンバーの **状態** フィールドが **レビューが必要** に変更されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![レビューが必要に変更された汎用チーム メンバーの状態](media/Resource-Management-image48.png)

<span data-ttu-id="d60cd-293">提案済みリソースを提案された予約の効果のビジュアル化とともに表示するには、 **レビューが必要** であるチーム メンバーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60cd-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="d60cd-294">そして、 **提案されたリソース** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-294">Then select the **Proposed Resources** tab.</span></span>

![提案されたリソース タブ](media/Resource-Management-image49.png)

<span data-ttu-id="d60cd-296">**すべての提案の受理** を選択して、すべての提案されたリソースを受け入れるか、 **すべての提案の拒否** を選択して、それらを却下します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="d60cd-297">提案されたリソースに同意すると、チーム メンバとしてプロジェクトに本予約され、汎用リソースが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="d60cd-298">すべての提案されたリソースに承諾または却下する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="d60cd-299">部分的に承諾または却下することはできません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="d60cd-300">プロジェクト チームのリソースを置き換える</span><span class="sxs-lookup"><span data-stu-id="d60cd-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="d60cd-301">場合によっては、プロジェクト管理者はプロジェクトで予約されたチーム メンバーを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="d60cd-302">**プロジェクト** ページの **チーム** タブで、置き換えが必要なリソースを選択し、 **予約の維持** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="d60cd-303">リソースを展開して、割り当てたプロジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![割り当てられたプロジェクトを表示するために展開されたリソース](media/Resource-Management-image50.png)

3. <span data-ttu-id="d60cd-305">プロジェクトを右クリックし、 **代替リソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="d60cd-306">現在のリソースの代わりに使用するリソースがわかる場合、名前を選択または入力して、 **再割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![代替リソースの指定](media/Resource-Management-image51.png)

    <span data-ttu-id="d60cd-308">または、次の手順に従ってリソースを検索します:</span><span class="sxs-lookup"><span data-stu-id="d60cd-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="d60cd-309">**代替リソースの検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-309">Select **Find Substitution**.</span></span>

        ![代替リソースの検索](media/Resource-Management-image52.png)

        <span data-ttu-id="d60cd-311">スケジュール アシスタントは使用可能な代替のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="d60cd-312">スケジュール アシスタントでは、適切な代替を見つけるために使用可能なリソースをさらにフィルターすることができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![使用可能な代替の一覧。](media/Resource-Management-image53.png)

    2. <span data-ttu-id="d60cd-314">リソースを代用するには、目的のリソースを選択して、 **代替** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![選択された代用リソース](media/Resource-Management-image54.png)

    <span data-ttu-id="d60cd-316">予約と割り当てが新しいリソースで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![新しいリソースで置き換えられた予約と割り当て](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="d60cd-318">チーム メンバーの予約や割り当ての調整</span><span class="sxs-lookup"><span data-stu-id="d60cd-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="d60cd-319">チーム メンバーの場合、予約と割り当ては緩く結び付けられます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="d60cd-320">つまり、リソースに割り当てはあっても予約はないか、リソースに予約はあっても割り当てはありません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="d60cd-321">理想としてはリソースがタスク割り当てを実行するキャパシティを持つように、予約と割り当てを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="d60cd-322">ただし、予約は空き時間に基づいて行われ、プロジェクトの続行に応じてタスクのタイミングが変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="d60cd-323">したがって、予約と割り当ての緩い結合は柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="d60cd-324">PSAには、 **調整** タブがあり、プロジェクト マネージャーはプロジェクト チームへのチーム メンバーの予約や割り当てを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![調整タブ](media/Resource-Management-image56.png)

<span data-ttu-id="d60cd-326">**調整** タブには、各チーム メンバーごとの個別タスクの割り当てレベルまで予約と割り当てが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="d60cd-327">月から日までの期間を表すセルに時間を表示します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="d60cd-328">タブには、合計列とともにプロジェクトの全体的な合計額も表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="d60cd-329">リソースごとに、タブはチーム メンバーの予約とチーム メンバーのタスクの割り当てのロールアップの差を計算します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="d60cd-330">理想としては、この差は 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="d60cd-331">つまり、予約と割り当てに差はありません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="d60cd-332">差は、 2 つの条件に注意を引くために色分けと影つけされます:</span><span class="sxs-lookup"><span data-stu-id="d60cd-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="d60cd-333">**予約不足** – 予約不足はリソースに予約よりも多くの割り当てがある場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="d60cd-334">この容量が予約されていないため、プロジェクト管理者は不足分に対応するためにリソースの予約を延長して、条件を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="d60cd-335">**予約過剰** – リソースがプロジェクトに予約されているがタスクには割り当てられていない場合に過剰予約が発生します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="d60cd-336">この条件はタスクの割り当てが発生する前に、リソースがプロジェクトに予約された場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="d60cd-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="d60cd-337">ただし、他の場合は、リソースはタスクに割り当てるように計画されていません。</span><span class="sxs-lookup"><span data-stu-id="d60cd-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="d60cd-338">このような場合、プロジェクト マネージャーは、そのリソースの予約のキャンセルを検討する必要があり、これによってキャパシティを他のプロジェクトに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="d60cd-339">場合によっては、時間を日レベルより上位レベル (たとえば、月レベル) で表示すると、リソース (つまり、予約=割り当て) の正味差がゼロになることがあります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="d60cd-340">ただし、週レベルで時間を表示すると、最初の週には 0 時間の割り当てと 40 時間の予約があり、2週目には 40 時間の割り当てと 0 時間の予約があることがわかります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="d60cd-341">全体として、予約と割り当ては調整されますが、週ごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="d60cd-342">上位レベルで時間を表示すると、 **調整** タブのセルには、下位レベルで差があることを知らせるインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="d60cd-343">セルをダブルクリックすると、拡大して差を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="d60cd-344">次に、右クリックして縮小します。リソースを選択して、グリッド ツール バーの **次の差分** コントロールを使用すると、そのリソースの予約と割り当ての次の差分に移動できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="d60cd-345">その後、 **前の差分** コントロールを使用して、戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="d60cd-346">**設定** で差分インジケータととナビゲーション動作をオフにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![差分インジケータ](media/Resource-Management-image57.png)

<span data-ttu-id="d60cd-348">リソースのタスク割り当てがあり、予約がない場合、 **プロジェクト** ページの **調整** タブで、予約不足を選択し、 **予約の延長** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d60cd-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="d60cd-349">**予約の延長** ダイアログ ボックスが表示され、リソースの不足に対応するために必要な予約が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="d60cd-350">また、すべてのプロジェクトまたは他のスケジュール可能なエンティティにわたるリソースの既存の予約も表示されます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="d60cd-351">**OK** を選択してリソースの予約を作成すると、そのリソースが使用可能かどうかにかかわらず、オーバブッキングが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d60cd-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![予約の延長 ダイアログ ボックス](media/Resource-Management-image58.png)

<span data-ttu-id="d60cd-353">プロジェクト管理者やリソース マネージャーは、スケジュール ボードを使用して、リソースが容量を超えてオーバーブッキングされる状況を管理できます。</span><span class="sxs-lookup"><span data-stu-id="d60cd-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
