---
title: プロジェクト カレンダーの定義
description: このトピックでは、プロジェクトのスケジュールを追跡するためにカレンダーのテンプレートをプロジェクトに適用する方法について説明します。
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999002"
---
# <a name="define-project-calendars"></a><span data-ttu-id="0f667-103">プロジェクト カレンダーの定義</span><span class="sxs-lookup"><span data-stu-id="0f667-103">Define project calendars</span></span>

<span data-ttu-id="0f667-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="0f667-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0f667-105">プロジェクトを作成、管理するには、カレンダーのテンプレートをプロジェクトに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f667-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="0f667-106">カレンダーのテンプレートは、次のプロジェクト属性を定義します:</span><span class="sxs-lookup"><span data-stu-id="0f667-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="0f667-107">開始時間と終了時間を含む作業時間</span><span class="sxs-lookup"><span data-stu-id="0f667-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="0f667-108">営業日</span><span class="sxs-lookup"><span data-stu-id="0f667-108">Working days</span></span>
- <span data-ttu-id="0f667-109">非稼働日などのカレンダーの例外日</span><span class="sxs-lookup"><span data-stu-id="0f667-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="0f667-110">プロジェクトに適用されるカレンダーのテンプレートは、組織の設定で定義されたカレンダー テンプレートのコピーです。</span><span class="sxs-lookup"><span data-stu-id="0f667-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="0f667-111">カレンダーのテンプレートを変更しても、その変更はプロジェクトの作業時間には反映されません。</span><span class="sxs-lookup"><span data-stu-id="0f667-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="0f667-112">プロジェクトの作業時間を変更するには、新しいテンプレートを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f667-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="0f667-113">組織で使用するカレンダーのテンプレートを作成するには、次の 2 つの重要な要件があります:</span><span class="sxs-lookup"><span data-stu-id="0f667-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="0f667-114">新規または既存の予約可能なリソースを使用して、テンプレートに適用する作業時間を定義します。</span><span class="sxs-lookup"><span data-stu-id="0f667-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="0f667-115">新しいカレンダーテンプレートを作成し、そのテンプレートを予約可能なリソースに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="0f667-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="0f667-116">**テンプレートの作業時間を定義する**</span><span class="sxs-lookup"><span data-stu-id="0f667-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="0f667-117">**リソース** \> **リソース** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="0f667-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="0f667-118">カレンダーのテンプレートで参照する新しいリソースを作成するか、既存のリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f667-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="0f667-119">リソースの **作業時間** タブを選択し、[リソースの作業時間の設定](/dynamics365/field-service/set-work-hours-resource.md)に記載の手順に従って、カレンダーのルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f667-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="0f667-120">**新しいカレンダーのテンプレートを作成する**</span><span class="sxs-lookup"><span data-stu-id="0f667-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="0f667-121">**設定** \> **カレンダーのテンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0f667-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="0f667-122">**新規** を選択し、名前、説明、テンプレート リソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="0f667-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="0f667-123">カレンダーのテンプレートでリソースを参照すると、リソースのカレンダーのコピーがカレンダーのテンプレートに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="0f667-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="0f667-124">コピーしたテンプレートの作業時間が変更されても、この変更はカレンダーのテンプレートには反映されません。</span><span class="sxs-lookup"><span data-stu-id="0f667-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="0f667-125">ここで、プロジェクトのカレンダー テンプレートがある作業テンプレートを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0f667-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

