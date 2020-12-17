---
title: プロジェクトのコピーを使用してプロジェクト テンプレートを開発する
description: このトピックは、プロジェクトのコピー カスタム アクションを使用してプロジェクト テンプレートを作成する方法について解説します。
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642414"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="d8276-103">プロジェクトのコピーを使用してプロジェクト テンプレートを開発する</span><span class="sxs-lookup"><span data-stu-id="d8276-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="d8276-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d8276-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d8276-105">Dynamics 365 Project Operations はプロジェクトをコピーして、ロールを表す汎用リソースに割り当てをすべて戻す機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d8276-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="d8276-106">顧客はこの機能を使用して、基本的なプロジェクト テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d8276-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="d8276-107">**プロジェクトのコピー** を選択した場合、対象のプロジェクトの状態が更新されます。</span><span class="sxs-lookup"><span data-stu-id="d8276-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="d8276-108">**ステータス** を使用してコピー アクションがいつ完了するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d8276-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="d8276-109">**プロジェクトのコピー** を選択すると、対象のプロジェクト エンティティで対象の日付が検出されない場合、プロジェクトの開始日も現在の開始日に更新されます。</span><span class="sxs-lookup"><span data-stu-id="d8276-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="d8276-110">プロジェクトのカスタム アクションをコピーする</span><span class="sxs-lookup"><span data-stu-id="d8276-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="d8276-111">件名</span><span class="sxs-lookup"><span data-stu-id="d8276-111">Name</span></span> 

<span data-ttu-id="d8276-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="d8276-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="d8276-113">入力パラメーター</span><span class="sxs-lookup"><span data-stu-id="d8276-113">Input parameters</span></span>
<span data-ttu-id="d8276-114">3 つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="d8276-114">There are three input parameters:</span></span>

| <span data-ttu-id="d8276-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d8276-115">Parameter</span></span>          | <span data-ttu-id="d8276-116">型</span><span class="sxs-lookup"><span data-stu-id="d8276-116">Type</span></span>   | <span data-ttu-id="d8276-117">値</span><span class="sxs-lookup"><span data-stu-id="d8276-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="d8276-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="d8276-118">ProjectCopyOption</span></span>  | <span data-ttu-id="d8276-119">String</span><span class="sxs-lookup"><span data-stu-id="d8276-119">String</span></span> | <span data-ttu-id="d8276-120">**{"removeNamedResources":true}** または **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="d8276-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="d8276-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="d8276-121">SourceProject</span></span>      | <span data-ttu-id="d8276-122">エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="d8276-122">Entity Reference</span></span> | <span data-ttu-id="d8276-123">ソース プロジェクト</span><span class="sxs-lookup"><span data-stu-id="d8276-123">Source Project</span></span> |
| <span data-ttu-id="d8276-124">ターゲット</span><span class="sxs-lookup"><span data-stu-id="d8276-124">Target</span></span>             | <span data-ttu-id="d8276-125">エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="d8276-125">Entity Reference</span></span> | <span data-ttu-id="d8276-126">対象のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="d8276-126">Target Project</span></span> |


- <span data-ttu-id="d8276-127">**{"clearTeamsAndAssignments":true}**: Web 向けのプロジェクトの既定の動作で、すべての割り当てとチームメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="d8276-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="d8276-128">**{"removeNamedResources":true}** プロジェクト操作の既定の動作で、割り当てを汎用リソースに戻します。</span><span class="sxs-lookup"><span data-stu-id="d8276-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="d8276-129">既定の動作の詳細 : [Web API のアクションを使用する](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="d8276-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="d8276-130">コピーするフィールドを特定する</span><span class="sxs-lookup"><span data-stu-id="d8276-130">Specify fields to copy</span></span> 
<span data-ttu-id="d8276-131">アクションが呼び出されると、**プロジェクトのコピー** は、プロジェクト ビューの **コピー プロジェクト カラム** を見て、プロジェクトがコピーされる際にコピーするフィールドを決定します。</span><span class="sxs-lookup"><span data-stu-id="d8276-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
