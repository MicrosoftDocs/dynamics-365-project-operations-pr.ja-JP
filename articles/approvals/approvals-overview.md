---
title: 承認の概要
description: このトピックでは、Project Operations における承認の操作について説明します。
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996707"
---
# <a name="approvals-overview"></a><span data-ttu-id="a4ec6-103">承認の概要</span><span class="sxs-lookup"><span data-stu-id="a4ec6-103">Approvals overview</span></span>

<span data-ttu-id="a4ec6-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="a4ec6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a4ec6-105">時間、費用、および材料用途の提出は、承認ワークフローを通過します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="a4ec6-106">エントリが承認された後、トランザクションは実績に記録されるか、スケジュールに時間が予約されます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="a4ec6-107">承認ワークフロー</span><span class="sxs-lookup"><span data-stu-id="a4ec6-107">Approvals workflow</span></span>
<span data-ttu-id="a4ec6-108">時間、費用、または材料用途エントリを作成して送信すると、承認レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="a4ec6-109">プロジェクト承認者またはマネージャーは、エントリをレビューして承認します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="a4ec6-110">エントリがプロジェクトに関連している場合、実績は承認時に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="a4ec6-111">これにより、コストと請求先を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="a4ec6-112">エントリを承認する</span><span class="sxs-lookup"><span data-stu-id="a4ec6-112">Approve an entry</span></span>
<span data-ttu-id="a4ec6-113">**承認** ページでは、さまざまなタイプの承認を表示するために、各種ビューを切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="a4ec6-114">**承認** ページに異動して、**経費**、**時間**、**材料用途**、または **リコール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="a4ec6-115">各承認を確認し、承認する承認を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="a4ec6-116">**承認** を選択し、選択したエントリを承認します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="a4ec6-117">システムはこれらのエントリを処理し、実績を作成します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="a4ec6-118">エントリを拒否する</span><span class="sxs-lookup"><span data-stu-id="a4ec6-118">Reject an entry</span></span>
<span data-ttu-id="a4ec6-119">プロジェクトの承認者として、修正のためにエントリをユーザーに返送することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="a4ec6-120">**承認** ページに移動し、拒否するエントリを選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="a4ec6-121">**拒否** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-121">Select **Reject**.</span></span>
3. <span data-ttu-id="a4ec6-122">オプションで、**拒否コメント** ダイアログ ボックスにコメントを追加し、エントリが拒否された理由をユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="a4ec6-123">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-123">Select **OK**.</span></span> <span data-ttu-id="a4ec6-124">エントリはユーザーに返されます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="a4ec6-125">承認の取り消し</span><span class="sxs-lookup"><span data-stu-id="a4ec6-125">Cancel approval</span></span>
<span data-ttu-id="a4ec6-126">場合によっては、以前に承認されたエントリをキャンセルしなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="a4ec6-127">以前に承認されたエントリをキャンセルすると、経済的な影響があります。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="a4ec6-128">取り消し要求の承認</span><span class="sxs-lookup"><span data-stu-id="a4ec6-128">Approving recall requests</span></span>
<span data-ttu-id="a4ec6-129">場合によっては、コンサルタントが以前に承認されたエントリを取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="a4ec6-130">以前に承認されたエントリをキャンセルすると、経済的な影響があります。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="a4ec6-131">プロジェクト承認者は、実績のトランザクションを取り消すためにリコールを承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="a4ec6-132">プロジェクト承認者を指定する</span><span class="sxs-lookup"><span data-stu-id="a4ec6-132">Specify Project approvers</span></span>
<span data-ttu-id="a4ec6-133">各プロジェクトには、多数のプロジェクト チーム メンバーがいます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-133">Each project has a number of project team members.</span></span> <span data-ttu-id="a4ec6-134">プロジェクトの承認者でもあるチーム メンバーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="a4ec6-135">**プロジェクト** ページに移動し、リストからプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="a4ec6-136">**チーム** タブで、プロジェクト承認者となるチーム メンバーを選択し、次に **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="a4ec6-137">**プロジェクト承認者** フィールドを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="a4ec6-138">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-138">Select **Save**.</span></span>
5. <span data-ttu-id="a4ec6-139">プロジェクト承認者を追加するには、手順 2ｰ4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="a4ec6-140">ユーザーのマネージャーを構成する</span><span class="sxs-lookup"><span data-stu-id="a4ec6-140">Configure the user's manager</span></span>

1. <span data-ttu-id="a4ec6-141">**設定** > **セキュリティ** >  **ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="a4ec6-142">マネージャーを割り当てるユーザーを選択し、**組織情報** エリアで、リストからマネージャーを選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="a4ec6-143">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4ec6-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
