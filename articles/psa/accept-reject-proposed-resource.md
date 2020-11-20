---
title: 提案されたプロジェクト リソースを承認または拒否する
description: このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 6e244ad48b4d6b50aea528d4ea378c28b8e42f2b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129864"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a><span data-ttu-id="acbaf-103">提案されたプロジェクト リソースを承認または拒否する</span><span class="sxs-lookup"><span data-stu-id="acbaf-103">Accept or reject a proposed project resource</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="acbaf-104">このトピックでは、提案されたプロジェクト リソースを承認または拒否する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="acbaf-104">This topic provides information about how to approve or reject a proposed project resource.</span></span>

<span data-ttu-id="acbaf-105">リソース マネージャーがプロジェクトの汎用リソース要求を満たすために名前付きリソースを提案すると、汎用チーム メンバーの **要求の状態** フィールドが **レビューが必要** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="acbaf-105">When a resource manager proposes a named resource to fill the generic resource request for a project, the **Request Status** field for the generic team member will be updated to **Needs Review**.</span></span> <span data-ttu-id="acbaf-106">要求が承認や拒否のためにプロジェクト マネージャーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="acbaf-106">The request will be sent to the project manager for approval or rejection.</span></span>

![提案がある汎用チーム メンバー](media/RM-how-to-19.png)

<span data-ttu-id="acbaf-108">**プロジェクト チーム メンバー** ページの **提案されたリソース** タブのグリッドには、提案されたリソースの現在の予約が表示されます。</span><span class="sxs-lookup"><span data-stu-id="acbaf-108">The grid on the **Proposed Resources** tab on the **Project Team Member** page shows the proposed resource’s current bookings.</span></span> <span data-ttu-id="acbaf-109">提案が承認された後、グリッドはその予約を反映して更新されます。</span><span class="sxs-lookup"><span data-stu-id="acbaf-109">After the proposal is accepted, the grid is updated to reflect that booking.</span></span> 

<span data-ttu-id="acbaf-110">提案されたリソースを承認してチームでそのリソースを予約するには **提案の承認** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="acbaf-110">To accept the proposed resource and book that resource on your team, click **Accept Proposals**.</span></span>  
<span data-ttu-id="acbaf-111">提案を拒否するには **リソースの拒否** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="acbaf-111">To reject the proposal, click **Reject Resource**.</span></span>

![リソース提案の承認](media/RM-how-to-20.png) 

<span data-ttu-id="acbaf-113">名前付きリソースで汎用リソース要求を直接満たすのと同様に、汎用リソースは置き換えられ、割り当てられたタスクは名前付きチーム メンバーで更新されます。</span><span class="sxs-lookup"><span data-stu-id="acbaf-113">Similar to directly fulfilling a generic resource request with a named resource, the generic resource will be replaced and the assigned tasks will be updated with the named team member.</span></span>
