---
title: Microsoft Project Client の統合
description: プロジェクト スケジュールの計画と管理は複雑になる可能性があるため、プロジェクト マネージャーはこのタスクの管理に役立つツールを使用する必要があります。 Microsoft Project Client との統合により、プロジェクトの WBS (作業分解構造) を開いて管理するためのサポートが提供されます。
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289330"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="a5df1-104">Microsoft Project Client の統合</span><span class="sxs-lookup"><span data-stu-id="a5df1-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5df1-105">プロジェクト スケジュールの計画と管理は複雑になる可能性があるため、プロジェクト マネージャーはこのタスクの管理に役立つツールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5df1-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="a5df1-106">Microsoft Project Client との統合により、プロジェクトの WBS (作業分解構造) を開いて管理するためのサポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="a5df1-107">プロジェクト マネージャーは、変更内容を Dynamics 365 Finance プロジェクト WBS (作業分解構造) に公開できます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="a5df1-108">7 月の更新 (バージョン 10.0.4) を使用している場合は、サポート情報 4054797 および 4055884 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5df1-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="a5df1-109">Microsoft Project Client アドインの構成</span><span class="sxs-lookup"><span data-stu-id="a5df1-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="a5df1-110">Microsoft Project Client との統合を有効にするには、Microsoft Dynamics 365 アドインをユーザーのクライアント Microsoft Project アプリケーションにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5df1-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="a5df1-111">これは、**プロジェクト管理ワークスペース** を開いて行います。</span><span class="sxs-lookup"><span data-stu-id="a5df1-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="a5df1-112">•ワークスペースの **リンク** > **セットアップ** セクションから **プロジェクト クライアント アドインを構成する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="a5df1-113">•**開く** をクリックし、確認メッセージが表示されたら **実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="a5df1-114">Microsoft Project Client で既存のドラフト WBS (作業分解構造) を開いて編集する</span><span class="sxs-lookup"><span data-stu-id="a5df1-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="a5df1-115">Dynamics 365 Finance のプロジェクトで既に WBS (作業分解構造) が作成されている場合、WBS (作業分解構造) がドラフト状態の場合は Microsoft Project Client アプリケーションで WBS (作業分解構造) を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="a5df1-116">**プロジェクト** ページから開くには、**計画** タブの **Microsoft Projectで開く** のリンクをクリックします。このページは、**Microsoft Dynamics 365** タブの **開く** をクリックして Microsoft Project Client アプリケーションから開くこともできます。一覧で、**法人** および **プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="a5df1-117">ブラウザーとして Internet Explorer を使用している場合、ファイルがダウンロードされた場所から手動で開くには **保存** をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5df1-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="a5df1-118">または、**保存して開く** をクリックして Microsoft Project Client でファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="a5df1-119">保存時にファイル名を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="a5df1-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="a5df1-120">Microsoft Project Client を使用してファイルを編集する前に、ファイルを確認する必要があります。**Microsoft Dynamics 365** タブで **チェックアウト** をクリックします。これにより、他のユーザーが同時に Finance で WBS (作業分解構造) を編集することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="a5df1-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="a5df1-121">編集の完了後に WBS (作業分解構造) を公開するには、**Microsoft Dynamics 365** タブの **チェックイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="a5df1-122">プロジェクト チームが既に Finance のプロジェクトに追加されている場合、リソース リストにはチーム メンバーが設定されます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="a5df1-123">プロジェクト チームがまだプロジェクトに追加されていない場合は、**Microsoft Dynamics 365** タブの **リソース** ボタンをクリックしリソースを選択して Microsoft Project Client 内でチームを構築できます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="a5df1-124">次のデータは、チェックイン プロセスの一環として、Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="a5df1-125">• タスク名</span><span class="sxs-lookup"><span data-stu-id="a5df1-125">•   Task name</span></span>

<span data-ttu-id="a5df1-126">• 開始日</span><span class="sxs-lookup"><span data-stu-id="a5df1-126">•   Start date</span></span>

<span data-ttu-id="a5df1-127">• 終了日</span><span class="sxs-lookup"><span data-stu-id="a5df1-127">•   Finish date</span></span>

<span data-ttu-id="a5df1-128">• 前のタスク</span><span class="sxs-lookup"><span data-stu-id="a5df1-128">•   Predecessors</span></span>

<span data-ttu-id="a5df1-129">• リソース名</span><span class="sxs-lookup"><span data-stu-id="a5df1-129">•   Resource names</span></span>

<span data-ttu-id="a5df1-130">• カテゴリ</span><span class="sxs-lookup"><span data-stu-id="a5df1-130">•   Category</span></span>

<span data-ttu-id="a5df1-131">• リソース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="a5df1-131">•   Resource category</span></span>

<span data-ttu-id="a5df1-132">• 作業時間</span><span class="sxs-lookup"><span data-stu-id="a5df1-132">•   Work hours</span></span>

<span data-ttu-id="a5df1-133">• メモ</span><span class="sxs-lookup"><span data-stu-id="a5df1-133">•   Notes</span></span>

<span data-ttu-id="a5df1-134">• 優先度</span><span class="sxs-lookup"><span data-stu-id="a5df1-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="a5df1-135">Microsoft Project Client ファイルに他の列を追加しても、それらの列はファイルに保存されずファイルを再度開いたときに表示されません。</span><span class="sxs-lookup"><span data-stu-id="a5df1-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="a5df1-136">Microsoft Project Client を使用した既存プロジェクトの WBS (作業分解構造) の作成</span><span class="sxs-lookup"><span data-stu-id="a5df1-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="a5df1-137">Microsoft Project Client を使用して新しい WBS (作業分解構造) を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="a5df1-138">Microsoft Project Client を開きます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a5df1-139">**Microsoft Dynamics 365** タブで、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="a5df1-140">プロジェクトの **法人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="a5df1-141">**プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="a5df1-142">**Microsoft Dynamics 365** タブの **チェックアウト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="a5df1-143">財務に公開する準備ができたら、**Microsoft Dynamics 365** タブの **チェックイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="a5df1-144">Microsoft Project Client を使用した既存プロジェクトの既存 WBS (作業分解構造) の置換</span><span class="sxs-lookup"><span data-stu-id="a5df1-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="a5df1-145">Microsoft Project Client を使用して新しい WBS (作業分解構造) を作成し、既存プロジェクトの既存 WBS (作業分解構造) を置き換えるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a5df1-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="a5df1-146">Microsoft Project Client を開きます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a5df1-147">Microsoft Project Client でスケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="a5df1-148">**Microsoft Dynamics 365** タブで、**変更の保存** > **既存のプロジェクトを置き換え** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="a5df1-149">プロジェクトの **法人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="a5df1-150">**プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="a5df1-151">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="a5df1-152">Microsoft Project Client からの新しいプロジェクト作成</span><span class="sxs-lookup"><span data-stu-id="a5df1-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="a5df1-153">Microsoft Project Client を開きます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a5df1-154">Microsoft Project Client でスケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="a5df1-155">**Microsoft Dynamics 365** タブで、**変更の保存** > **新しいプロジェクトに保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="a5df1-156">プロジェクトの **法人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="a5df1-157">必要であれば、**プロジェクト ID** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="a5df1-158">**プロジェクト名** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="a5df1-159">**プロジェクト タイプ**、**プロジェクト グループ** および **プロジェクト契約 ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="a5df1-160">または、**新規** をクリックして新しいプロジェクト契約を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a5df1-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="a5df1-161">リソースで使用する **カレンダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5df1-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="a5df1-162">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5df1-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]