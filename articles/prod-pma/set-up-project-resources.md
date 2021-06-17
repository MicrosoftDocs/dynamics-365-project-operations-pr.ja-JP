---
title: プロジェクト リソースの設定
description: このトピックでは、プロジェクト リソースの設定または要求について説明します。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997697"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="fa52a-103">プロジェクト リソースの設定</span><span class="sxs-lookup"><span data-stu-id="fa52a-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa52a-104">カレンダーを設定し、それを従業員または作業者に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa52a-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="fa52a-105">カレンダーは、プロジェクトとプロジェクト用に予約されているリソースの作業時間をスケジュールするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="fa52a-106">カレンダーの設定中に、プロジェクト マネージャーはリソースの最適化の一部としてリソースの平準化を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="fa52a-107">カレンダーのスケジュールに基づいて、リソースに制限をかけることができます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="fa52a-108">**カレンダー** ページでカレンダーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="fa52a-109">作業者をプロジェクト リソースとして設定する場合、リソースを設定する会社で働く作業者から選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="fa52a-110">または、組織内の他の会社から作業者を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="fa52a-111">これらの作業者は会社間リソースとして知られています。</span><span class="sxs-lookup"><span data-stu-id="fa52a-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="fa52a-112">次の手順では、作業者を会社のプロジェクト リソースとして設定する方法と、会社間プロジェクト リソースを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="fa52a-113">作業者をプロジェクト リソースとして設定する</span><span class="sxs-lookup"><span data-stu-id="fa52a-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="fa52a-114">**作業者** ページで、**作業者** リストから、プロジェクト リソースとして追加する作業者を選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="fa52a-115">アクション ウィンドウで、**プロジェクト**&gt;**設定**&gt;**プロジェクトの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="fa52a-116">カレンダーを選択した後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="fa52a-117">リソースの既定のプロジェクトを、事前割り当てのタイプとして指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="fa52a-118">事前割り当ては、リソース マネージャーまたはプロジェクト マネージャーが、リソースが事前に作業するプロジェクトを周知している場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="fa52a-119">事前割り当ては、プロジェクトのスポンサーまたは顧客の要求に基づくこともできます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="fa52a-120">プロジェクトを事前に割り当てるには、**プロジェクトを割り当てる** ページ、**プロジェクト** タブ、**残りのプロジェクト** リストから適切なプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="fa52a-121">会社間リソースを設定する</span><span class="sxs-lookup"><span data-stu-id="fa52a-121">Set up an intercompany resource</span></span>

<span data-ttu-id="fa52a-122">作業者を会社間リソースとして設定する場合、融資会社と借入会社の両方で設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa52a-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="fa52a-123">融資会社で</span><span class="sxs-lookup"><span data-stu-id="fa52a-123">In the lending company</span></span>

1. <span data-ttu-id="fa52a-124">財務で、融資会社が選択されていることを確認してから、前のセクション「作業者をプロジェクト リソースとして設定」の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="fa52a-125">**会社間会計** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="fa52a-126">**法人 ID** フィールドで、融資会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="fa52a-127">必要に応じて残りのフィールドに入力し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="fa52a-128">**移転価格** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="fa52a-129">**借入法人** フィールドで、適切な会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="fa52a-130">このセクションの冒頭で作成したリソースのみを借用入会社に貸し出すには、**リソース** フィールドで、作成したリソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="fa52a-131">融資会社のすべてのリソースを借入会社が利用できるようにするには、**リソース** フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="fa52a-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="fa52a-132">**プロジェクト管理と会計パラメータ** ページの **会社間** タブで、**会社間リソースのスケジュールとタイムシートを有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="fa52a-133">借入会社で</span><span class="sxs-lookup"><span data-stu-id="fa52a-133">In the borrowing company</span></span>

- <span data-ttu-id="fa52a-134">**リソース リスト** ページの検索フィルターで、貸出会社用に作成したリソースの名前を入力して、その名前が借入会社のリソース リストに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="fa52a-135">プロジェクト リソースの要求</span><span class="sxs-lookup"><span data-stu-id="fa52a-135">Request project resources</span></span>
<span data-ttu-id="fa52a-136">プロジェクト リソース スケジュールの機能では、リソース マネージャーのみがエンゲージメントまたはプロジェクトのスタッフが配置されたリソースを配布できます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="fa52a-137">この機能を有効にするには、次のタスクを完了するか、それらが完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="fa52a-138">番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-138">Set up number sequences.</span></span>
- <span data-ttu-id="fa52a-139">プロジェクト管理および会計ワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="fa52a-140">リソース要求ワークフローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="fa52a-140">Enable resource request workflows.</span></span>

<span data-ttu-id="fa52a-141">上記のタスクが完了したら、必要に応じて次のタスクを完了できます。</span><span class="sxs-lookup"><span data-stu-id="fa52a-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="fa52a-142">仮予約されたスタッフが配置されたリソースからリソース要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="fa52a-143">リソース要求を監視します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-143">Monitor resource requests.</span></span>
- <span data-ttu-id="fa52a-144">リソース要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="fa52a-145">WBS からスタッフが配置されたリソースを要求します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="fa52a-146">スタッフが配置されたリソースをリクエストせずに、プロジェクトにリソースを予約します。</span><span class="sxs-lookup"><span data-stu-id="fa52a-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]