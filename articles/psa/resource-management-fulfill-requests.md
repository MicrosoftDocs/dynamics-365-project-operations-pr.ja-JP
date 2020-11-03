---
title: リソース要件の履行
description: このトピックでは、リソース要件の履行方法について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 626828b96e110de4dcb6cad4a191994972ec26c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079491"
---
# <a name="fulfilling-resource-requests"></a><span data-ttu-id="df098-103">リソース要求の履行</span><span class="sxs-lookup"><span data-stu-id="df098-103">Fulfilling resource requests</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="df098-104">リソース要件は、リソース要求として、これらの要求を履行する責任があるリソース マネージャーに送信できます。</span><span class="sxs-lookup"><span data-stu-id="df098-104">Resource requirements can be sent as resource requests to the resource manager who is responsible for fulfilling those requests.</span></span>

<span data-ttu-id="df098-105">リソース要求は、 **アクティブなリソース要求** ビューで一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="df098-105">Resource requests are shown as a list in the **Active Resource Requests** view.</span></span>

> ![リソース要求のリスト](media/Resource-Management-image59.png)

<span data-ttu-id="df098-107">要求を履行するには、それをリストで選択して、 **リソースの検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df098-107">To fulfill a request, select it in the list, and then select **Find Resources**.</span></span> <span data-ttu-id="df098-108">または、行をダブルクリックして要求を開きます。</span><span class="sxs-lookup"><span data-stu-id="df098-108">Alternatively, double-click a row to open the request.</span></span> <span data-ttu-id="df098-109">次に **リソース要件** タブを選択すると、その要求の要件を表示できます。</span><span class="sxs-lookup"><span data-stu-id="df098-109">You can then select the **Resource Requirement** tab to view the requirements for that request.</span></span> <span data-ttu-id="df098-110">要求の履行を始めるには、 **リソースの検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df098-110">To start to fulfill the request, select **Find Resources**.</span></span>

> ![リソース要件の詳細](media/Resource-Management-image60.png)

<span data-ttu-id="df098-112">スケジュール アシスタントが表示され、要件別にフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="df098-112">The Schedule Assistant appears and is filtered by the requirements.</span></span> <span data-ttu-id="df098-113">リソースを選び、 **予約** を選びます。</span><span class="sxs-lookup"><span data-stu-id="df098-113">Select the resource, and then select **Book**.</span></span>

> ![選択したリソース](media/Resource-Management-image61.png)

<span data-ttu-id="df098-115">汎用チーム メンバーが、プロジェクト チームの本予約された名前の付いたリソースとプロジェクト スケジュール内のタスク割り当で置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="df098-115">The generic team member is replaced with the hard-booked named resource on the project team and task assignments in the project schedule.</span></span>
