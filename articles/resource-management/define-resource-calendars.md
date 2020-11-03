---
title: リソース カレンダーの定義
description: このトピックでは、プロジェクト オペレーションのリソースの作業時間カレンダーを定義する方法に関する情報を提供します。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079116"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="5ad3f-103">リソース カレンダーの定義</span><span class="sxs-lookup"><span data-stu-id="5ad3f-103">Define resource calendars</span></span>

<span data-ttu-id="5ad3f-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="5ad3f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ad3f-105">プロジェクトで作業するそれぞれの予約可能リソースには、空き時間を定義するための作業時間のカレンダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="5ad3f-106">リソースの作業時間は、次の 2 つの方法で定義できます。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="5ad3f-107">リソースの個々のカレンダー ルールを定義する</span><span class="sxs-lookup"><span data-stu-id="5ad3f-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="5ad3f-108">リソースに既存のカレンダー テンプレートを適用する</span><span class="sxs-lookup"><span data-stu-id="5ad3f-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="5ad3f-109">リソースの作業時間を定義する</span><span class="sxs-lookup"><span data-stu-id="5ad3f-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="5ad3f-110">**リソース** メニューで、 **リソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5ad3f-111">グリッド ビューから、該当する **予約可能なリソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="5ad3f-112">**リソース詳細** ページで、 **作業時間** タブを選択します。既定では、予約可能なリソース カレンダーは、組織に対して定義されている既定の作業時間テンプレートの作業時間に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="5ad3f-113">作業時間を更新するには、定義する提案されたカレンダー ルールの開始日を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="5ad3f-114">カレンダー ルールのメニューを使用して、特定の日、系列の残りの部分、またはカレンダー全体のカレンダー ルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="5ad3f-115">オプションを選択した後、次の項目を定義できます。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="5ad3f-116">作業時間が適用される曜日。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="5ad3f-117">各日内の作業時間。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-117">The working times within each day.</span></span>
    - <span data-ttu-id="5ad3f-118">カレンダー ルールのタイム ゾーン。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="5ad3f-119">該当する場合は、非作業時間をルールに指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="5ad3f-120">リソースへのカレンダー テンプレートの適用</span><span class="sxs-lookup"><span data-stu-id="5ad3f-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="5ad3f-121">**リソース** メニューで、 **リソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5ad3f-122">グリッド ビューから、最大 25 の **予約可能リソース** を選択して更新します。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="5ad3f-123">**カレンダーの設定** を選択すると、ダイアログでは使用できる作業時間テンプレートのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="5ad3f-124">使用するテンプレートを選択し、 **適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ad3f-124">Select the template you want to use, and then select **Apply**.</span></span>
