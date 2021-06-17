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
# <a name="develop-project-templates-with-copy-project"></a>プロジェクトのコピーを使用してプロジェクト テンプレートを開発する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations はプロジェクトをコピーして、ロールを表す汎用リソースに割り当てをすべて戻す機能をサポートします。 顧客はこの機能を使用して、基本的なプロジェクト テンプレートを作成できます。

**プロジェクトのコピー** を選択した場合、対象のプロジェクトの状態が更新されます。 **ステータス** を使用してコピー アクションがいつ完了するかを決定します。 **プロジェクトのコピー** を選択すると、対象のプロジェクト エンティティで対象の日付が検出されない場合、プロジェクトの開始日も現在の開始日に更新されます。

## <a name="copy-project-custom-action"></a>プロジェクトのカスタム アクションをコピーする 

### <a name="name"></a>件名 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>入力パラメーター
3 つのパラメーターがあります。

| パラメーター          | 型   | 値                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** または **{"clearTeamsAndAssignments":true}** |
| SourceProject      | エンティティの参照 | ソース プロジェクト |
| ターゲット             | エンティティの参照 | 対象のプロジェクト |


- **{"clearTeamsAndAssignments":true}**: Web 向けのプロジェクトの既定の動作で、すべての割り当てとチームメンバーを削除します。
- **{"removeNamedResources":true}** プロジェクト操作の既定の動作で、割り当てを汎用リソースに戻します。

既定の動作の詳細 : [Web API のアクションを使用する](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>コピーするフィールドを特定する 
アクションが呼び出されると、**プロジェクトのコピー** は、プロジェクト ビューの **コピー プロジェクト カラム** を見て、プロジェクトがコピーされる際にコピーするフィールドを決定します。


### <a name="example"></a>例
次の例は、**CopyProject** カスタムアクションを **removeNamedResources** パラメーターセットと呼び出す方法を示しています。
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