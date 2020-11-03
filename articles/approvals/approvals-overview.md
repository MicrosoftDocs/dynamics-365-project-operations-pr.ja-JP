---
title: 承認の概要
description: このトピックでは、Project Operations における承認の操作について説明します。
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079128"
---
# <a name="approvals-overview"></a><span data-ttu-id="33aca-103">承認の概要</span><span class="sxs-lookup"><span data-stu-id="33aca-103">Approvals overview</span></span>

<span data-ttu-id="33aca-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="33aca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33aca-105">時間と経費の送信は、承認ワークフローを通じて移動します。</span><span class="sxs-lookup"><span data-stu-id="33aca-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="33aca-106">エントリが承認された後、トランザクションは実績に記録されるか、スケジュールに時間が予約されます。</span><span class="sxs-lookup"><span data-stu-id="33aca-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="33aca-107">承認ワークフロー</span><span class="sxs-lookup"><span data-stu-id="33aca-107">Approvals workflow</span></span>
<span data-ttu-id="33aca-108">時間または経費エントリを作成して送信すると、承認エントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="33aca-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="33aca-109">プロジェクト承認者またはマネージャーがエントリを確認して承認します。</span><span class="sxs-lookup"><span data-stu-id="33aca-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="33aca-110">エントリがプロジェクトに関連している場合、承認されると、実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="33aca-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="33aca-111">これにより、コストと請求先を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="33aca-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="33aca-112">エントリを承認する</span><span class="sxs-lookup"><span data-stu-id="33aca-112">Approve an entry</span></span>
<span data-ttu-id="33aca-113">**承認** フォームを使用すると、さまざまなビューを切り替えて、さまざまなタイプの承認を表示できます。</span><span class="sxs-lookup"><span data-stu-id="33aca-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="33aca-114">**承認** フォームに移動し、 **経費** 、 **時間** 、または **取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="33aca-115">各承認を確認し、承認する承認を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="33aca-116">**承認** を選択し、選択したエントリを承認します。</span><span class="sxs-lookup"><span data-stu-id="33aca-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="33aca-117">システムはこれらのエントリを処理し、実績または予約を作成します。</span><span class="sxs-lookup"><span data-stu-id="33aca-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="33aca-118">エントリを拒否する</span><span class="sxs-lookup"><span data-stu-id="33aca-118">Reject an entry</span></span>
<span data-ttu-id="33aca-119">プロジェクトの承認者として、修正のためにエントリをユーザーに返送することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="33aca-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="33aca-120">**承認** フォームに移動し、拒否するエントリを選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="33aca-121">**拒否** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-121">Select **Reject**.</span></span>
3. <span data-ttu-id="33aca-122">オプション- **拒否コメント** ダイアログにコメントを追加し、エントリが拒否された理由をユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="33aca-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="33aca-123">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-123">Select **OK**.</span></span> <span data-ttu-id="33aca-124">エントリはユーザーに返されます。</span><span class="sxs-lookup"><span data-stu-id="33aca-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="33aca-125">エントリの取り消し</span><span class="sxs-lookup"><span data-stu-id="33aca-125">Recall entries</span></span>
<span data-ttu-id="33aca-126">ある時点で、送信されたエントリを取り消すことが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="33aca-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="33aca-127">エントリーが承認されていない場合は、すぐに返送されます。</span><span class="sxs-lookup"><span data-stu-id="33aca-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="33aca-128">ただし、承認されたエントリは重大な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="33aca-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="33aca-129">プロジェクト承認者は、実績のトランザクションを取り消すために、取り消しを承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33aca-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="33aca-130">プロジェクト承認者を指定する</span><span class="sxs-lookup"><span data-stu-id="33aca-130">Specify Project approvers</span></span>
<span data-ttu-id="33aca-131">各プロジェクトには、多数のプロジェクト チーム メンバーがいます。</span><span class="sxs-lookup"><span data-stu-id="33aca-131">Each project has a number of project team members.</span></span> <span data-ttu-id="33aca-132">プロジェクトの承認者でもあるチーム メンバーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="33aca-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="33aca-133">**プロジェクト** リストに移動し、リストからプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="33aca-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="33aca-134">**チーム** タブで、プロジェクト承認者となるチーム メンバーを選択し、次に **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="33aca-135">**プロジェクト承認者** フィールドを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="33aca-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="33aca-136">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-136">Select **Save**.</span></span>
5. <span data-ttu-id="33aca-137">プロジェクト承認者を追加するには、手順 2ｰ4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="33aca-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="33aca-138">ユーザーのマネージャーを構成する</span><span class="sxs-lookup"><span data-stu-id="33aca-138">Configure the user's manager</span></span>

1. <span data-ttu-id="33aca-139">**設定** > **セキュリティ** >  **ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="33aca-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="33aca-140">マネージャーを割り当てるユーザーを選択し、 **組織情報** エリアで、リストからマネージャーを選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="33aca-141">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33aca-141">Select **Save**.</span></span>


