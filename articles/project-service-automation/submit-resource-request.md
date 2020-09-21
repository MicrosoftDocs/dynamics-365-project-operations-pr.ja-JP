---
title: リソース要求を送信します
description: このトピックでは、プロジェクト リソースの要求を送信する方法について説明します。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752901"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="42e4e-103">リソース要求を送信します</span><span class="sxs-lookup"><span data-stu-id="42e4e-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="42e4e-104">リソース要求として生成されたリソース要件を送信できます。</span><span class="sxs-lookup"><span data-stu-id="42e4e-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="42e4e-105">要求は、実行する場合はリソース マネージャーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="42e4e-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="42e4e-106">Project Service Automation (PSA) の **プロジェクト** ページで、 **チーム** タブをクリックして一覧の予約可能リソースを表示します。</span><span class="sxs-lookup"><span data-stu-id="42e4e-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="42e4e-107">一覧からリソース要件を持つ汎用リソースを選択して、**要求を送信する**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42e4e-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![リソース要求を送信する](media/RM-how-to-18.png)

<span data-ttu-id="42e4e-109">汎用要求チーム メンバーの要求の状態が **送信済み**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="42e4e-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="42e4e-110">リソース マネージャーによって要求が満たされた後、名前付きリソースの予約を使用してリソース マネージャーが要求を満たすと、汎用リソースは名前付きリソースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="42e4e-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="42e4e-111">それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合は汎用リソースはチームに残り、要求の状態が **レビューが必要**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="42e4e-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
