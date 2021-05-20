---
title: 作業時間テンプレートの作成
description: このトピックは、Project Service で作業時間テンプレートを作成する方法について説明しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981261"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="0c851-103">作業時間テンプレートの作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0c851-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0c851-104">プロジェクトを作成、管理するには、カレンダーのテンプレートをプロジェクトに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c851-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="0c851-105">カレンダーのテンプレートは、次のプロジェクト属性を定義します:</span><span class="sxs-lookup"><span data-stu-id="0c851-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="0c851-106">開始時間と終了時間を含む作業時間</span><span class="sxs-lookup"><span data-stu-id="0c851-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="0c851-107">営業日</span><span class="sxs-lookup"><span data-stu-id="0c851-107">Working days</span></span>
- <span data-ttu-id="0c851-108">非稼働日などのカレンダーの例外日</span><span class="sxs-lookup"><span data-stu-id="0c851-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="0c851-109">プロジェクトに適用されるカレンダーのテンプレートは、組織の設定で定義されたカレンダー テンプレートのコピーです。</span><span class="sxs-lookup"><span data-stu-id="0c851-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="0c851-110">カレンダーのテンプレートを変更しても、その変更はプロジェクトの作業時間には反映されません。</span><span class="sxs-lookup"><span data-stu-id="0c851-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="0c851-111">プロジェクトの作業時間を変更するには、新しいテンプレートを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c851-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="0c851-112">組織で使用するカレンダーのテンプレートを作成するには、次の 2 つの重要な要件があります:</span><span class="sxs-lookup"><span data-stu-id="0c851-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="0c851-113">新規または既存の予約可能なリソースを使用して、テンプレートに適用する作業時間を定義します。</span><span class="sxs-lookup"><span data-stu-id="0c851-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="0c851-114">新しいカレンダーテンプレートを作成し、そのテンプレートを予約可能なリソースに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="0c851-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="0c851-115">**テンプレートの作業時間を定義する**</span><span class="sxs-lookup"><span data-stu-id="0c851-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="0c851-116">**リソース** \> **リソース** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="0c851-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="0c851-117">カレンダーのテンプレートで参照する新しいリソースを作成するか、既存のリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c851-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="0c851-118">リソースの **作業時間** タブを選択し、[リソースの作業時間の設定](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource)に記載の手順に従って、カレンダーのルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c851-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="0c851-119">**新しいカレンダーのテンプレートを作成する**</span><span class="sxs-lookup"><span data-stu-id="0c851-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="0c851-120">**設定** \> **カレンダーのテンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c851-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="0c851-121">**新規** を選択し、名前、説明、テンプレート リソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="0c851-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="0c851-122">カレンダーのテンプレートでリソースを参照すると、リソースのカレンダーのコピーがカレンダーのテンプレートに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="0c851-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="0c851-123">コピーしたテンプレートの作業時間が変更されても、この変更はカレンダーのテンプレートには反映されません。</span><span class="sxs-lookup"><span data-stu-id="0c851-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="0c851-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c851-124">See Also</span></span>  
 [<span data-ttu-id="0c851-125">リソースの設定</span><span class="sxs-lookup"><span data-stu-id="0c851-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
