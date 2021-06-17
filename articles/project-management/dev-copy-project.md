---
title: プロジェクトのコピーを使用してプロジェクト テンプレートを開発する
description: このトピックは、プロジェクトのコピー カスタム アクションを使用してプロジェクト テンプレートを作成する方法について解説します。
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005662"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="76260-103">プロジェクトのコピーを使用してプロジェクト テンプレートを開発する</span><span class="sxs-lookup"><span data-stu-id="76260-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="76260-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="76260-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="76260-105">Dynamics 365 Project Operations はプロジェクトをコピーして、ロールを表す汎用リソースに割り当てをすべて戻す機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="76260-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="76260-106">顧客はこの機能を使用して、基本的なプロジェクト テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="76260-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="76260-107">**プロジェクトのコピー** を選択した場合、対象のプロジェクトの状態が更新されます。</span><span class="sxs-lookup"><span data-stu-id="76260-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="76260-108">**ステータス** を使用してコピー アクションがいつ完了するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76260-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="76260-109">**プロジェクトのコピー** を選択すると、対象のプロジェクト エンティティで対象の日付が検出されない場合、プロジェクトの開始日も現在の開始日に更新されます。</span><span class="sxs-lookup"><span data-stu-id="76260-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="76260-110">プロジェクトのカスタム アクションをコピーする</span><span class="sxs-lookup"><span data-stu-id="76260-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="76260-111">件名</span><span class="sxs-lookup"><span data-stu-id="76260-111">Name</span></span> 

<span data-ttu-id="76260-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="76260-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="76260-113">入力パラメーター</span><span class="sxs-lookup"><span data-stu-id="76260-113">Input parameters</span></span>
<span data-ttu-id="76260-114">3 つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="76260-114">There are three input parameters:</span></span>

| <span data-ttu-id="76260-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76260-115">Parameter</span></span>          | <span data-ttu-id="76260-116">型</span><span class="sxs-lookup"><span data-stu-id="76260-116">Type</span></span>   | <span data-ttu-id="76260-117">値</span><span class="sxs-lookup"><span data-stu-id="76260-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="76260-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="76260-118">ProjectCopyOption</span></span>  | <span data-ttu-id="76260-119">String</span><span class="sxs-lookup"><span data-stu-id="76260-119">String</span></span> | <span data-ttu-id="76260-120">**{"removeNamedResources":true}** または **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="76260-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="76260-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="76260-121">SourceProject</span></span>      | <span data-ttu-id="76260-122">エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="76260-122">Entity Reference</span></span> | <span data-ttu-id="76260-123">ソース プロジェクト</span><span class="sxs-lookup"><span data-stu-id="76260-123">Source Project</span></span> |
| <span data-ttu-id="76260-124">ターゲット</span><span class="sxs-lookup"><span data-stu-id="76260-124">Target</span></span>             | <span data-ttu-id="76260-125">エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="76260-125">Entity Reference</span></span> | <span data-ttu-id="76260-126">対象のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="76260-126">Target Project</span></span> |


- <span data-ttu-id="76260-127">**{"clearTeamsAndAssignments":true}**: Web 向けのプロジェクトの既定の動作で、すべての割り当てとチームメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="76260-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="76260-128">**{"removeNamedResources":true}** プロジェクト操作の既定の動作で、割り当てを汎用リソースに戻します。</span><span class="sxs-lookup"><span data-stu-id="76260-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="76260-129">既定の動作の詳細 : [Web API のアクションを使用する](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="76260-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="76260-130">コピーするフィールドを特定する</span><span class="sxs-lookup"><span data-stu-id="76260-130">Specify fields to copy</span></span> 
<span data-ttu-id="76260-131">アクションが呼び出されると、**プロジェクトのコピー** は、プロジェクト ビューの **コピー プロジェクト カラム** を見て、プロジェクトがコピーされる際にコピーするフィールドを決定します。</span><span class="sxs-lookup"><span data-stu-id="76260-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="76260-132">例</span><span class="sxs-lookup"><span data-stu-id="76260-132">Example</span></span>
<span data-ttu-id="76260-133">次の例は、**CopyProject** カスタムアクションを **removeNamedResources** パラメーターセットと呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="76260-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]