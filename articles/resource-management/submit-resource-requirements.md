---
title: リソース要求の送信
description: リソース要求として生成されたリソース要件を送信できます。 要求は、実行する場合はリソース マネージャーに送信されます。
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279144"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="d0092-104">リソース要求の送信</span><span class="sxs-lookup"><span data-stu-id="d0092-104">Submit a resource request</span></span>

<span data-ttu-id="d0092-105">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d0092-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0092-106">リソース要求として生成されたリソース要件を送信できます。</span><span class="sxs-lookup"><span data-stu-id="d0092-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="d0092-107">要求の達成のため、要求はリソース マネージャーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="d0092-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="d0092-108">Dynamics 365 Project Operations の **プロジェクト** ページで、**チーム** タブを選択して、予約可能なリソースの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="d0092-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="d0092-109">一覧からリソース要件を持つ汎用リソースを選択し、**要求を送信する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0092-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="d0092-110">汎用要求チーム メンバーの要求の状態が **送信済み** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d0092-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="d0092-111">要求が満たされた後、リソース マネージャーが名前付きのリソースで要求を処理すると、汎用リソースが名前付きのリソースで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d0092-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="d0092-112">それ以外の場合は、リソース マネージャーが名前付きリソースを提案した場合、汎用リソースはチームに残り、要求の状態が **レビューが必要** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d0092-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]