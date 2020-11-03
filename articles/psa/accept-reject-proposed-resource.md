---
title: 提案されたプロジェクト リソースを承認または拒否する
description: このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 4c10c55961c74c2dc53fabd1d041a935ca9a4870
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079432"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a><span data-ttu-id="41b28-103">提案されたプロジェクト リソースを承認または拒否する</span><span class="sxs-lookup"><span data-stu-id="41b28-103">Accept or reject a proposed project resource</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="41b28-104">このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="41b28-104">This topic provides information about how to approve or reject a proposed project resource.</span></span>

<span data-ttu-id="41b28-105">リソース マネージャーがプロジェクトの汎用リソース要求を満たすために名前付きリソースを提案すると、汎用チーム メンバーの **要求の状態** フィールドが **レビューが必要** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="41b28-105">When a resource manager proposes a named resource to fill the generic resource request for a project, the **Request Status** field for the generic team member will be updated to **Needs Review**.</span></span> <span data-ttu-id="41b28-106">要求が承認や拒否のためにプロジェクト マネージャーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="41b28-106">The request will be sent to the project manager for approval or rejection.</span></span>

![提案がある汎用チーム メンバー](media/RM-how-to-19.png)

<span data-ttu-id="41b28-108">**プロジェクト チーム メンバー** ページの **提案されたリソース** タブのグリッドには、提案されたリソースの現在の予約が表示されます。</span><span class="sxs-lookup"><span data-stu-id="41b28-108">The grid on the **Proposed Resources** tab on the **Project Team Member** page shows the proposed resource’s current bookings.</span></span> <span data-ttu-id="41b28-109">提案が承認された後、グリッドはその予約を反映して更新されます。</span><span class="sxs-lookup"><span data-stu-id="41b28-109">After the proposal is accepted, the grid is updated to reflect that booking.</span></span> 

<span data-ttu-id="41b28-110">提案されたリソースを承認してチームでそのリソースを予約するには **提案の承認** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41b28-110">To accept the proposed resource and book that resource on your team, click **Accept Proposals**.</span></span>  
<span data-ttu-id="41b28-111">提案を拒否するには **リソースの拒否** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41b28-111">To reject the proposal, click **Reject Resource**.</span></span>

![リソース提案の承認](media/RM-how-to-20.png) 

<span data-ttu-id="41b28-113">名前付きリソースで汎用リソース要求を直接満たすのと同様に、汎用リソースは置き換えられ、割り当てられたタスクは名前付きチーム メンバーで更新されます。</span><span class="sxs-lookup"><span data-stu-id="41b28-113">Similar to directly fulfilling a generic resource request with a named resource, the generic resource will be replaced and the assigned tasks will be updated with the named team member.</span></span>
