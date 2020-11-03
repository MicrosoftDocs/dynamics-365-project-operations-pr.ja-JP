---
title: プロジェクトの見積りの確認、更新、送信
description: このトピックでは、顧客に見積りを送信して確認し、フィードバックに基づいて修正し、見積りを再送信する処理について説明します。
author: ruhercul
manager: AnnBe
ms.date: 05/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f9d76c65cb6732a96cd0bd6c4c36a2a73a65a2b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079406"
---
# <a name="confirm-update-and-send-a-project-quotation"></a><span data-ttu-id="6dafb-103">プロジェクトの見積りの確認、更新、送信</span><span class="sxs-lookup"><span data-stu-id="6dafb-103">Confirm, update, and send a project quotation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dafb-104">プロジェクトの見積りを作成し、顧客に送信した後、見積りのステータスを **送信済み** に更新する前に、顧客から確認を取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="6dafb-104">After you create and send a project quotation to a customer, you must get confirmation from the customer before you update the quotation status to **Sent**.</span></span> <span data-ttu-id="6dafb-105">顧客から要求された修正は、見積りの中で更新することができます。</span><span class="sxs-lookup"><span data-stu-id="6dafb-105">Any modifications requested by the customer can be updated in the quotation.</span></span> <span data-ttu-id="6dafb-106">見積りの状態を **送信済み** に更新した後は、変更できません。</span><span class="sxs-lookup"><span data-stu-id="6dafb-106">After you update the quotation status to **Sent** , you can’t modify it.</span></span> <span data-ttu-id="6dafb-107">以下の手順では、確認のために見積りを送信し、フィードバックに基づいて更新を行い、見積りを送信するオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-107">The following procedure describes the options to send a quotation for confirmation, make updates based on feedback, and then send the quotation.</span></span>

## <a name="send-a-project-quotation-confirmation"></a><span data-ttu-id="6dafb-108">プロジェクトの見積り確認を送信する</span><span class="sxs-lookup"><span data-stu-id="6dafb-108">Send a project quotation confirmation</span></span>  

<span data-ttu-id="6dafb-109">確認のために、既存のプロジェクトの見積書を電子メールで送信するか、印刷したコピーとして送信することができます。</span><span class="sxs-lookup"><span data-stu-id="6dafb-109">You can send an existing project quotation for confirmation through email or as a printed copy.</span></span> 

1. <span data-ttu-id="6dafb-110">**プロジェクト管理と会計** > **見積り** > **プロジェクトの見積り** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-110">Go to **Project management and accounting** > **Quotations** > **Project quotation.**</span></span> 
2. <span data-ttu-id="6dafb-111">**プロジェクトの見積り** ページで、確認のために送信する見積りを選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-111">On the **Project quotation** page, select the quotation you want to send for confirmation.</span></span> 
3. <span data-ttu-id="6dafb-112">**フォローアップ** タブの **全般** タブで、 **確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-112">On the **Follow up** tab, in the **Generate** group, select **Confirm**.</span></span> 
4. <span data-ttu-id="6dafb-113">**見積もりを確認する** ページで、必要なパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-113">On the **Confirm quotation** page, set the required parameters.</span></span> <span data-ttu-id="6dafb-114">たとえば、確認を印刷するには、 **印刷** オプションの配下で、 **印刷を確認する** をオンにして、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-114">For example, to print the confirmation, under **Print** options, turn on **Print confirmation** , and then select **OK**.</span></span>
5. <span data-ttu-id="6dafb-115">**見積りを送信する** ページで、 **オプション** を選択し、 **印刷先の設定** ページで、見積もりを **画面** 、 **Eメール** 、 **ファイル** 、 **アーカイブを印刷する** 、 **プリンター** に送信するかどうかを選択します。その後、見積書をルーティングするために、 **仕様** 領域で必要な調整を行います。</span><span class="sxs-lookup"><span data-stu-id="6dafb-115">On the **Send quotation** page, select **Options** , and on the **Print destination settings** page, select whether you want the quotation sent to **Screen** , **E-mail** , **File** , **Print archive** , or **Printer** , and then make any adjustments that you want in the **Specification** area to route the quotation.</span></span>
6. <span data-ttu-id="6dafb-116">**印刷先設定** ページで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-116">On the **Print destination settings** page, select **OK**.</span></span>  

## <a name="update-a-project-quotation"></a><span data-ttu-id="6dafb-117">プロジェクトの見積を更新する</span><span class="sxs-lookup"><span data-stu-id="6dafb-117">Update a project quotation</span></span>

<span data-ttu-id="6dafb-118">既存のプロジェクト見積りを変更するには、見積もりの状態が **作成済** になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6dafb-118">To modify an existing project quotation, the quotation status must be **Created**.</span></span> <span data-ttu-id="6dafb-119">次の手順を実行して、既存の見積もりを更新します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-119">Complete the following steps to update an existing quotation.</span></span> 

1. <span data-ttu-id="6dafb-120">**プロジェクト管理と会計** > **見積もり** > **プロジェクト見積もり** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-120">Go to **Project management and accounting** > **Quotations** > **Project quotations**.</span></span>
2. <span data-ttu-id="6dafb-121">**プロジェクトの見積もり** ページで、更新する見積もりを選択し、アクションペインで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-121">On the **Project quotations** page, select the quotation you want to update and on the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="6dafb-122">必要なフィールド情報を更新し、アクションペインで **保存する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-122">Update the necessary field information, and on the Action Pane, select **Save**.</span></span>  

## <a name="send-a-project-quotation-to-a-customer"></a><span data-ttu-id="6dafb-123">顧客にプロジェクトの見積もりを送る</span><span class="sxs-lookup"><span data-stu-id="6dafb-123">Send a project quotation to a customer</span></span> 

1. <span data-ttu-id="6dafb-124">**プロジェクト管理と会計** > **見積り** > **プロジェクトの見積り** にアクセスし、送信するプロジェクトの見積もりを選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-124">Go to **Project management and accounting** > **Quotations** > **Project quotations** , and select the project quotation that you want to send.</span></span>
2. <span data-ttu-id="6dafb-125">**プロジェクトの見積り** ページの、 **見積もり** タブで、 **処理** グループの **見積りの送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6dafb-125">On the **Project quotations** page, on the **Quote** tab, in the **Process** group, select **Send quotation**.</span></span> <span data-ttu-id="6dafb-126">見積りの状態が **送信済み** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="6dafb-126">The quotation status updates to **Sent**.</span></span>

> [!NOTE]
> <span data-ttu-id="6dafb-127">状態が **送信済み** に更新された後は、プロジェクトの見積りを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6dafb-127">You can’t modify a project quotation after the status is changed to **Sent**.</span></span>
