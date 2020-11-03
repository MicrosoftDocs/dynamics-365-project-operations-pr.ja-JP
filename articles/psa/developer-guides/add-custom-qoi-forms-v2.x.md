---
title: 新しいカスタム エンティティ フォームを追加する (Project Service Automation 2.x)
description: このトピックでは、Dynamics 365 Project Service Automation 2.x で営業案件、見積もり、受注、請求書にカスタム エンティティ フォームを追加する方法について説明します。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079462"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>新しいカスタム エンティティ フォームを追加する (Project Service Automation 2.x)

## <a name="type-field"></a>フィールドの種類 

Dynamics 365 Project Service Automation は営業案件、見積もり、受注、請求書エンティティの **種類** ( **msdyn\_ordertype** ) フィールドに依存しており、これらのエンティティの **作業ベース** バージョンを **品目ベース** や **サービス ベース** バージョンと区別します。 これらのエンティティの作業ベースのバージョンは PSA によって処理されます。 ソリューションのクライアント側とサーバー側の多くのビジネス ロジックは、 **種類** フィールドに依存します。 そのため、エンティティの作成時にフィールドを正しい値で初期化することが重要です。 不正な値は不正な動作の原因になる可能性があり、一部のビジネス ロジックは正しく実行されない場合があります。

## <a name="automatic-form-switching"></a>自動フォーム切り替え

誤った初期化と販売エンティティ レコードの編集で引き起こされる潜在的なデータ破損と予期しない動作を回避するために、PSA には標準のフォームに自動フォーム切り替え ジックを含むようになりました。 このロジックにより、ユーザーは作業ベースのバージョンやその他の種類の営業案件、見積もり、受注、請求書エンティティで作業する正しいフォームに移動します。 ユーザーが営業案件、見積もり、受注、請求書エンティティの作業ベース バージョンを開くと、フォームは **プロジェクト情報** に切り替わります。

自動フォーム切り替えロジックは **フォーマット** 値と **msdyn\_ordertype** フィールドのマッピングに依存しています。 すべての標準フォームがそのマッピングに追加されました。 ただし、カスタム フォームを手動で追加して、処理するエンティティのバージョンを示す必要があります。 これは **msdyn\_ordertype** フィールドに基づいています。 フォームの切り替えがマッピングにない場合、ロジックはエンティティの **msdyn\_ordertype** フィールドに保存されている値に基づいて標準フォームに切り替わります。

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>カスタムフォームを追加し、フォーム切り替えロジックをオンにする

次の例は、作業ベースの営業案件で機能するように、カスタムフォーム **自分のプロジェクト情報** を追加する方法を示しています。 同じプロセスを使用してカスタム フォームを追加して、見積もり、受注、請求書を処理できるようにします。

次の手順に従って **プロジェクト情報** フォームのカスタム バージョンを作成します。

1. 営業案件エンティティで **プロジェクト情報** フォームを開き、 **自分のプロジェクト情報** という名前でコピーを保存します。
2. 新しいフォームを開き、プロパティに **プロジェクト情報** フォームのフォーム初期化スクリプトが存在することを確認します。 

    > [!IMPORTANT]
    > このスクリプトを削除しないでください。 削除すると一部のデータが誤って初期化される可能性があります。

3. フォームに **種類** ( **msdyn\_ordertype** ) フィールドが存在することを確認します。 

    > [!IMPORTANT]
    > このフィールドを削除しないでください。 削除した場合は初期化スクリプトが失敗します。

4. 新しいフォームの **formId** 値を見つけます。 このステップは 2 つの方法で完了できます。

    - アンマネージド ソリューションの一部として **自分のプロジェクト情報** フォームをエクスポートし、エクスポートされたソリューションの「customization.xml」ファイルで **formId** 値を検索します。
    - 次の図に示すように、フォーム エディターで **自分のプロジェクト情報** フォームを開き、URL の **fromId** パラメータの横にあるグローバル一意識別子 (GUID) を探します。

    ![URL の新しいフォームの formId 値](media/how-to-add-custom-forms-in-v2.0.png)

5. msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Webリソースを編集して、 **formId** 値の **msdyn\_ordertype** マッピングを作成します。 リソースからコードを削除し、次のコードに置き換えます。

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. カスタマイズを保存し、公開します。
