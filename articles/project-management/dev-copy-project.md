---
title: プロジェクトのコピーを使用してプロジェクト テンプレートを開発する
description: この記事では、Copy Project カスタムアクションを使用して、プロジェクトのテンプレートを作成する方法について説明します。
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923838"
---
# <a name="develop-project-templates-with-copy-project"></a>プロジェクトのコピーを使用してプロジェクト テンプレートを開発する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations はプロジェクトをコピーして、ロールを表す汎用リソースに割り当てをすべて戻す機能をサポートします。 顧客はこの機能を使用して、基本的なプロジェクト テンプレートを作成できます。

**プロジェクトのコピー** を選択した場合、対象のプロジェクトの状態が更新されます。 **ステータス** を使用してコピー アクションがいつ完了するかを決定します。 **プロジェクトのコピー** を選択すると、対象のプロジェクト エンティティで対象の日付が検出されない場合、プロジェクトの開始日も現在の開始日に更新されます。

## <a name="copy-project-custom-action"></a>プロジェクトのカスタム アクションをコピーする

### <a name="name"></a>件名 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>入力パラメーター

3 つのパラメーターがあります。

- **ReplaceNamedResources** または **ClearTeamsAndAssignments** – オプションの一方のみを設定します。 両方を設定しないでください。

    - **\{"ReplaceNamedResources":true\}** – Project Operations の既定の動作。 名前付きリソースは、汎用リソースに置き換えられます。
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Web の既定の動作。 すべての割り当てとチームメンバーが削除されます。

- **SourceProject** – コピー元のソース プロジェクトのエンティティ参照。 このパラメーターを null にすることはできません。
- **Target** – コピー先のプロジェクトのエンティティ参照。 このパラメーターを null にすることはできません。

次の表は、3 つのパラメーターの概要を示しています。

| パラメーター                | タイプ             | 価値                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | ブール型          | **True** または **False** |
| ClearTeamsAndAssignments | ブール型          | **True** または **False** |
| SourceProject            | エンティティの参照 | ソース プロジェクト    |
| Target                   | エンティティの参照 | ターゲット プロジェクト    |

既定の動作の詳細については、[Web API のアクションを使用する](/powerapps/developer/common-data-service/webapi/use-web-api-actions)を参照してください。

### <a name="validations"></a>検証

次の検証が完了します。

1. Nullは、ソース プロジェクトと対象のプロジェクトをチェック・取得して、組織内に両方のプロジェクトが存在することを確認します。
2. システムは、以下の条件を確認することで、コピー対象のプロジェクトが有効であることを検証します。

    - プロジェクトに以前の活動 (**タスク** タブの選択を含む) がなく、プロジェクトが新規に作成された状態です。
    - 以前のコピーがなく、このプロジェクトでインポートが要求されておらず、プロジェクトに **失敗** 状態がありません。

3. この操作は、HTTP を使用して呼び出されません。

## <a name="specify-fields-to-copy"></a>コピーするフィールドを特定する

アクションが呼び出されると、**プロジェクトのコピー** は、プロジェクト ビューの **コピー プロジェクト カラム** を見て、プロジェクトがコピーされる際にコピーするフィールドを決定します。

### <a name="example"></a>例

次の例は、**CopyProjectV3** パラメータを設定して **removeNamedResources** カスタム アクションを呼び出す方法を示しています。

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
