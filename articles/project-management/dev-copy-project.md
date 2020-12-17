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

既定の動作の詳細 : [Web API のアクションを使用する](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>コピーするフィールドを特定する 
アクションが呼び出されると、**プロジェクトのコピー** は、プロジェクト ビューの **コピー プロジェクト カラム** を見て、プロジェクトがコピーされる際にコピーするフィールドを決定します。
