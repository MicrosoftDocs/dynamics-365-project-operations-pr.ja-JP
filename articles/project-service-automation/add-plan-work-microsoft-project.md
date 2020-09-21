---
title: Microsoft Project で作業を計画するための Project Service アドインの使用 | MicrosoftDocs
description: このトピックは、Microsoft Project Service の Microsoft Project アドインを追加、構成、使用する方法について説明します。
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752819"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="27f35-103">Microsoft Project で作業を計画するための Project Service Automation アドインの使用</span><span class="sxs-lookup"><span data-stu-id="27f35-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="27f35-104">を使用することで、より簡単に見積もりを含んだプロジェクト計画を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="27f35-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="27f35-105">最終提案を堤出するために費用、行動および販売額が明確になるように作業を定義できます。</span><span class="sxs-lookup"><span data-stu-id="27f35-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="27f35-106">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] をインストールして、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の使い慣れた環境で計画している作業を実行することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="27f35-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="27f35-107">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の強力な計画および管理機能を使用して、Project Service Automation のプロジェクト計画を更新します。</span><span class="sxs-lookup"><span data-stu-id="27f35-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="27f35-108">SharePoint のドキュメント管理機能を使用して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクトの [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルを保存するには、 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の管理者がドキュメント管理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f35-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="27f35-109">[特定のエンティティの SharePoint ドキュメント管理を有効にする](../admin/enable-sharepoint-document-management-specific-entities.md)</span><span class="sxs-lookup"><span data-stu-id="27f35-109">[Enable SharePoint document management for specific entities](../admin/enable-sharepoint-document-management-specific-entities.md)</span></span>  
> - <span data-ttu-id="27f35-110">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] は [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition とのみ互換性があります。</span><span class="sxs-lookup"><span data-stu-id="27f35-110">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="27f35-111">アドインのダウンロードおよびインストール</span><span class="sxs-lookup"><span data-stu-id="27f35-111">Download and install the add-in</span></span>  
 <span data-ttu-id="27f35-112">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] のサインイン情報を準備します。</span><span class="sxs-lookup"><span data-stu-id="27f35-112">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="27f35-113">この情報は、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] から [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に接続するために必要です。</span><span class="sxs-lookup"><span data-stu-id="27f35-113">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="27f35-114">ダウンロード センターからご利用の環境に対応している Project Service のバージョン [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) または [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) のアドインをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="27f35-114">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="27f35-115">ダウンロード リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-115">Click the download link.</span></span>  

3.  <span data-ttu-id="27f35-116">ダウンロードが完了したら、**はい** をクリックしてアドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="27f35-116">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="27f35-117">アドインの構成</span><span class="sxs-lookup"><span data-stu-id="27f35-117">Configure the add-in</span></span>  

1. <span data-ttu-id="27f35-118">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を開いて **Project Service** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-118">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="27f35-119">**接続**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-119">Click **Connect**.</span></span>  

3. <span data-ttu-id="27f35-120">サインイン情報を入力して、**サインイン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-120">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="27f35-121">これで、アドインを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="27f35-121">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="27f35-122">テンプレートからの読み取り</span><span class="sxs-lookup"><span data-stu-id="27f35-122">Read from a template</span></span>  
 <span data-ttu-id="27f35-123">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で作成して [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] にコピーしたテンプレートから読み取り、プロジェクト計画を開始します。</span><span class="sxs-lookup"><span data-stu-id="27f35-123">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="27f35-124">[プロジェクトのテンプレートの作成 (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="27f35-124">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1.  <span data-ttu-id="27f35-125">**Project Service** タブから、**読み取り** > **Project Service Automation プロジェクト テンプレート**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-125">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="27f35-126">リストからプロジェクト テンプレートを選択して、**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-126">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="27f35-127">既定では、テンプレートからプロジェクトにコピーされるタスクは、手動で予定するように設定されます。</span><span class="sxs-lookup"><span data-stu-id="27f35-127">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="27f35-128">プロジェクトのリソースに [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] のロールを割り当てる</span><span class="sxs-lookup"><span data-stu-id="27f35-128">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="27f35-129">プロジェクトを開いて、**タスク**リボンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-129">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="27f35-130">**ガント チャート**メニューをクリックして、**リソース シート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-130">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="27f35-131">リソース シートで、**Project Service のリソース ロール**ドロップダウン メニューをクリックして、Project Service Automation のロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-131">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="27f35-132">プロジェクトへのリソースの設定</span><span class="sxs-lookup"><span data-stu-id="27f35-132">Staff your project with resources</span></span>  

1.  <span data-ttu-id="27f35-133">[Project Service] タブから、行を選択して**リソースの検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-133">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="27f35-134">**リソースの予約**画面で、プロジェクトに使用したいリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-134">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="27f35-135">**予約**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-135">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="27f35-136">プロジェクトの公開</span><span class="sxs-lookup"><span data-stu-id="27f35-136">Publish your project</span></span>  
<span data-ttu-id="27f35-137">プロジェクト計画が完了した場合、次のステップはプロジェクトを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートして公開することです。</span><span class="sxs-lookup"><span data-stu-id="27f35-137">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="27f35-138">プロジェクトを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートします。</span><span class="sxs-lookup"><span data-stu-id="27f35-138">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="27f35-139">価格設定およびチーム生成プロセスが適用されます。</span><span class="sxs-lookup"><span data-stu-id="27f35-139">The pricing and team generation process are applied.</span></span> <span data-ttu-id="27f35-140">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でプロジェクトを開いて、チーム、プロジェクトの予測および作業分解構造が生成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="27f35-140">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="27f35-141">次の表は結果が表示される場所を示します。</span><span class="sxs-lookup"><span data-stu-id="27f35-141">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="27f35-142">**ガント チャート**</span><span class="sxs-lookup"><span data-stu-id="27f35-142">**Gantt Chart**</span></span>   | <span data-ttu-id="27f35-143">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **WBS (作業分解構造)** 画面にインポートします。</span><span class="sxs-lookup"><span data-stu-id="27f35-143">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="27f35-144">**シート リソース**</span><span class="sxs-lookup"><span data-stu-id="27f35-144">**Resource Sheet**</span></span> |   <span data-ttu-id="27f35-145">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **プロジェクト チーム メンバー**画面にインポートします。</span><span class="sxs-lookup"><span data-stu-id="27f35-145">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="27f35-146">**使用状況を使用**</span><span class="sxs-lookup"><span data-stu-id="27f35-146">**Use Usage**</span></span>    |    <span data-ttu-id="27f35-147">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **プロジェクト見積**画面にインポートします。</span><span class="sxs-lookup"><span data-stu-id="27f35-147">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="27f35-148">**プロジェクトをインポートして公開する**</span><span class="sxs-lookup"><span data-stu-id="27f35-148">**To import and publish your project**</span></span>  
1. <span data-ttu-id="27f35-149">**Project Service** タブから、**公開** > **新しい Project Service Automation プロジェクト**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-149">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="27f35-150">**Project Service の新しいプロジェクトへの公開**ダイアログ ボックスで、**プロジェクト名**を入力して**顧客**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-150">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="27f35-151">オプションで、**プロジェクト計画を Project Service Automation にリンクする**を選択すると、Project Service Automation に計画プロジェクト ファイルをリンクできます。</span><span class="sxs-lookup"><span data-stu-id="27f35-151">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="27f35-152">**発行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-152">Click **Publish**.</span></span>  

   <span data-ttu-id="27f35-153">プロジェクト ファイルを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にリンクすると、プロジェクト ファイルをマスターにして、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で作業分解構造を読み取り専用に設定できます。</span><span class="sxs-lookup"><span data-stu-id="27f35-153">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="27f35-154">プロジェクト計画への変更を行うためには、それを [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に更新として公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f35-154">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="27f35-155">インポートするプロジェクトの編集</span><span class="sxs-lookup"><span data-stu-id="27f35-155">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="27f35-156">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートするプロジェクト計画に変更を加えるには、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="27f35-156">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="27f35-157">マスター ファイルを開いて [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で編集します。</span><span class="sxs-lookup"><span data-stu-id="27f35-157">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="27f35-158">ファイルをリンク解除して、Project Service で直接編集します。</span><span class="sxs-lookup"><span data-stu-id="27f35-158">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="27f35-159">デフォルトで、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] からアップロードされたプロジェクトはロックされ、プロジェクトでのみ編集することができます。</span><span class="sxs-lookup"><span data-stu-id="27f35-159">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="27f35-160">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でファイルを編集するには、ファイルのリンクを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f35-160">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="27f35-161">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で編集する</span><span class="sxs-lookup"><span data-stu-id="27f35-161">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="27f35-162">メイン メニューから、**Project Service** > **プロジェクト**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-162">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="27f35-163">プロジェクトのリストから、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成したものをオープンします。</span><span class="sxs-lookup"><span data-stu-id="27f35-163">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="27f35-164">リボンの **MS Project で開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-164">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="27f35-165">これで、リンクされたファイルが [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開きます。</span><span class="sxs-lookup"><span data-stu-id="27f35-165">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="27f35-166">ファイルのリンクを切り、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] サービスで編集します。</span><span class="sxs-lookup"><span data-stu-id="27f35-166">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="27f35-167">メイン メニューから、**Project Service** > **プロジェクト**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-167">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="27f35-168">プロジェクトのリストから、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成したものをオープンします。</span><span class="sxs-lookup"><span data-stu-id="27f35-168">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="27f35-169">リボンの **MS Project からリンク解除する**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-169">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="27f35-170">プロジェクトファイルを SharePoint や Office グループにアップロードする</span><span class="sxs-lookup"><span data-stu-id="27f35-170">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="27f35-171">プロジェクト ファイルを SharePoint にアップロードすることが可能で、それは [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクトの [関連ドキュメント] の下に保存されます。</span><span class="sxs-lookup"><span data-stu-id="27f35-171">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="27f35-172">管理者に要請をして SharePoint のドキュメント管理を構成し、プロジェクト エンティティで使用できるように有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f35-172">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="27f35-173">[SharePoint の統合を設定する](../admin/set-up-sharepoint-integration.md)</span><span class="sxs-lookup"><span data-stu-id="27f35-173">[Set up SharePoint integration](../admin/set-up-sharepoint-integration.md)</span></span>  

 <span data-ttu-id="27f35-174">また、Office グループをセットアップ済みの場合は、プロジェクト ファイルを [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] にアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="27f35-174">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="27f35-175">[Office 365 グループを使用して同僚と共同作業する](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span><span class="sxs-lookup"><span data-stu-id="27f35-175">[Collaborate with your colleagues using Office 365 Groups](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span></span>  

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="27f35-176">SharePoint にファイルをアップロードする</span><span class="sxs-lookup"><span data-stu-id="27f35-176">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="27f35-177">メイン メニューから、**Project Service** > **アップロード**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-177">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="27f35-178">**Project Service Automation プロジェクト ドキュメントへ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-178">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="27f35-179">**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開くことを有効にする** ダイアログで、 **はい** または **いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-179">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="27f35-180">**はい** をクリックすると、Project Service Automation の **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開く** ボタンを選択した際に [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を起動して SharePoint ドキュメント ライブラリからプロジェクト ファイルを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="27f35-180">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="27f35-181">**いいえ**をクリックすると、 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開く** ボタン のリンクは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="27f35-181">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="27f35-182">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルは、特定の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクト用の**ドキュメント**の下にある [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="27f35-182">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="27f35-183">Office グループ用のファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="27f35-183">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="27f35-184">メイン メニューから、**Project Service** > **アップロード**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-184">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="27f35-185">**Project Service Automation プロジェクト ドキュメントへ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-185">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="27f35-186">**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開くことを有効にする** ダイアログで、 **はい** または **いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f35-186">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="27f35-187">**はい** をクリックすると、Project Service Automation の **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開く** ボタンを選択した際に [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を起動して SharePoint ドキュメント ライブラリからプロジェクト ファイルを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="27f35-187">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="27f35-188">**いいえ**をクリックすると、 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開く** ボタン のリンクは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="27f35-188">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="27f35-189">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルは、特定の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクト用の**ドキュメント**の下にある [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="27f35-189">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="27f35-190">テンプレートとしてのプロジェクトの公開</span><span class="sxs-lookup"><span data-stu-id="27f35-190">Publish  your project as a template</span></span>  
 <span data-ttu-id="27f35-191">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でプロジェクト テンプレートとして保存することで、プロジェクトを保存して再使用できます。</span><span class="sxs-lookup"><span data-stu-id="27f35-191">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="27f35-192">プロジェクト テンプレートは、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で再使用可能なプロジェクト計画です。</span><span class="sxs-lookup"><span data-stu-id="27f35-192">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="27f35-193">[プロジェクトのテンプレートの作成 (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="27f35-193">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1. <span data-ttu-id="27f35-194">**Project Service** タブから、**公開** > **新しい Project Service Automation プロジェクト テンプレート**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-194">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="27f35-195">**Project Service テンプレートの新しいプロジェクトへの公開**ダイアログ ボックスで、**プロジェクト テンプレート名**を入力します。</span><span class="sxs-lookup"><span data-stu-id="27f35-195">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="27f35-196">また任意で、**プロジェクト 計画を Project Service Automation にリンクする** を選択すると、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にプロジェクト ファイルをリンクします。</span><span class="sxs-lookup"><span data-stu-id="27f35-196">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="27f35-197">**発行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27f35-197">Click **Publish**.</span></span>  

<span data-ttu-id="27f35-198">プロジェクト ファイルを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にリンクすると、プロジェクト ファイルをマスターにして、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] テンプレートで作業分解構造を読み取り専用に設定できます。</span><span class="sxs-lookup"><span data-stu-id="27f35-198">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="27f35-199">プロジェクト計画への変更を行うためには、それを [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に更新として公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f35-199">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="27f35-200">関連項目</span><span class="sxs-lookup"><span data-stu-id="27f35-200">See Also</span></span>  
 [<span data-ttu-id="27f35-201">プロジェクト管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="27f35-201">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
