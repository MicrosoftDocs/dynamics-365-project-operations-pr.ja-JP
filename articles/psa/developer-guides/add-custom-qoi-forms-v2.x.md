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
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144599"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="4bb19-103">新しいカスタム エンティティ フォームを追加する (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="4bb19-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="4bb19-104">フィールドの種類</span><span class="sxs-lookup"><span data-stu-id="4bb19-104">Type field</span></span> 

<span data-ttu-id="4bb19-105">Dynamics 365 Project Service Automation は営業案件、見積もり、受注、請求書エンティティの **種類** (**msdyn\_ordertype**) フィールドに依存しており、これらのエンティティの **作業ベース** バージョンを **品目ベース** や **サービス ベース** バージョンと区別します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="4bb19-106">これらのエンティティの作業ベースのバージョンは PSA によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="4bb19-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="4bb19-107">ソリューションのクライアント側とサーバー側の多くのビジネス ロジックは、**種類** フィールドに依存します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="4bb19-108">そのため、エンティティの作成時にフィールドを正しい値で初期化することが重要です。</span><span class="sxs-lookup"><span data-stu-id="4bb19-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="4bb19-109">不正な値は不正な動作の原因になる可能性があり、一部のビジネス ロジックは正しく実行されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4bb19-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="4bb19-110">自動フォーム切り替え</span><span class="sxs-lookup"><span data-stu-id="4bb19-110">Automatic form switching</span></span>

<span data-ttu-id="4bb19-111">誤った初期化と販売エンティティ レコードの編集で引き起こされる潜在的なデータ破損と予期しない動作を回避するために、PSA には標準のフォームに自動フォーム切り替え ジックを含むようになりました。</span><span class="sxs-lookup"><span data-stu-id="4bb19-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="4bb19-112">このロジックにより、ユーザーは作業ベースのバージョンやその他の種類の営業案件、見積もり、受注、請求書エンティティで作業する正しいフォームに移動します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="4bb19-113">ユーザーが営業案件、見積もり、受注、請求書エンティティの作業ベース バージョンを開くと、フォームは **プロジェクト情報** に切り替わります。</span><span class="sxs-lookup"><span data-stu-id="4bb19-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="4bb19-114">自動フォーム切り替えロジックは **フォーマット** 値と **msdyn\_ordertype** フィールドのマッピングに依存しています。</span><span class="sxs-lookup"><span data-stu-id="4bb19-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="4bb19-115">すべての標準フォームがそのマッピングに追加されました。</span><span class="sxs-lookup"><span data-stu-id="4bb19-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="4bb19-116">ただし、カスタム フォームを手動で追加して、処理するエンティティのバージョンを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bb19-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="4bb19-117">これは **msdyn\_ordertype** フィールドに基づいています。</span><span class="sxs-lookup"><span data-stu-id="4bb19-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="4bb19-118">フォームの切り替えがマッピングにない場合、ロジックはエンティティの **msdyn\_ordertype** フィールドに保存されている値に基づいて標準フォームに切り替わります。</span><span class="sxs-lookup"><span data-stu-id="4bb19-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="4bb19-119">カスタムフォームを追加し、フォーム切り替えロジックをオンにする</span><span class="sxs-lookup"><span data-stu-id="4bb19-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="4bb19-120">次の例は、作業ベースの営業案件で機能するように、カスタムフォーム **自分のプロジェクト情報** を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4bb19-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="4bb19-121">同じプロセスを使用してカスタム フォームを追加して、見積もり、受注、請求書を処理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4bb19-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="4bb19-122">次の手順に従って **プロジェクト情報** フォームのカスタム バージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="4bb19-123">営業案件エンティティで **プロジェクト情報** フォームを開き、**自分のプロジェクト情報** という名前でコピーを保存します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="4bb19-124">新しいフォームを開き、プロパティに **プロジェクト情報** フォームのフォーム初期化スクリプトが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="4bb19-125">このスクリプトを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="4bb19-125">Don't remove the scripts.</span></span> <span data-ttu-id="4bb19-126">削除すると一部のデータが誤って初期化される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4bb19-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="4bb19-127">フォームに **種類** (**msdyn\_ordertype**) フィールドが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="4bb19-128">このフィールドを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="4bb19-128">Don't remove this field.</span></span> <span data-ttu-id="4bb19-129">削除した場合は初期化スクリプトが失敗します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="4bb19-130">新しいフォームの **formId** 値を見つけます。</span><span class="sxs-lookup"><span data-stu-id="4bb19-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="4bb19-131">このステップは 2 つの方法で完了できます。</span><span class="sxs-lookup"><span data-stu-id="4bb19-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="4bb19-132">アンマネージド ソリューションの一部として **自分のプロジェクト情報** フォームをエクスポートし、エクスポートされたソリューションの「customization.xml」ファイルで **formId** 値を検索します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="4bb19-133">次の図に示すように、フォーム エディターで **自分のプロジェクト情報** フォームを開き、URL の **fromId** パラメータの横にあるグローバル一意識別子 (GUID) を探します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![URL の新しいフォームの formId 値](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="4bb19-135">msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Webリソースを編集して、**formId** 値の **msdyn\_ordertype** マッピングを作成します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="4bb19-136">リソースからコードを削除し、次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4bb19-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="4bb19-137">カスタマイズを保存し、公開します。</span><span class="sxs-lookup"><span data-stu-id="4bb19-137">Save and then publish the customizations.</span></span>
