---
title: 価格設定のディメンションをオフにする
description: このトピックでは、Project Service ソリューションの価格設定ディメンションを設定する方法を説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752894"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="dedb9-103">価格設定のディメンションをオフにする</span><span class="sxs-lookup"><span data-stu-id="dedb9-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="dedb9-104">価格設定戦略を数年度ごとにレビューし、更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="dedb9-105">何らかの更新を行うと、既存の価格設定のディメンションを停止して新たに作成しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="dedb9-106">たとえば、以前は、**ロール**によって価格設定を行っていたとしても、現在は、**ワーク エクスペリエンス** によって価格設定することを決定しています。</span><span class="sxs-lookup"><span data-stu-id="dedb9-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="dedb9-107">この場合、価格設定のディメンションとして、**ロール** を停止し、 **ワーク エクスペリエンス** を新しい価格設定のディメンションとして作成する必要があるかもしれます。</span><span class="sxs-lookup"><span data-stu-id="dedb9-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="dedb9-108">価格設定のディメンションを停止するには、それが標準であるかカスタムであるかにかかわらず、価格設定ディメンションの**コストに適用可能** および **営業に適用可能** フィールドを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dedb9-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="dedb9-109">ただし、これを実行すると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-109">However, when you do this, you might receive the following error message.</span></span>

![価格設定のディメンションを停止したとき、生じる可能性が高いビジネス プロセス エラー](media/Business-Process-Error.png)


<span data-ttu-id="dedb9-111">このエラー メッセージは、停止されているディメンションに対して過去に設定済みの価格のレコードが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="dedb9-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="dedb9-112">ディメンションを参照するすべての **ロール価格** および **ロール価格利幅** レコード は、ディメンションの適用領域を **いいえ**に設定する可能性があればその前に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="dedb9-113">このルールは、作成済みの双方の標準価格ディメンションおよび任意のカスタム価格ディメンションに適用されます。</span><span class="sxs-lookup"><span data-stu-id="dedb9-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="dedb9-114">この検証を行うのは、Project Service では **ロール価格** の各レコードに、制約上、一意のディメンションの組み合わせが必要であるためです。</span><span class="sxs-lookup"><span data-stu-id="dedb9-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="dedb9-115">たとえば、**US Cost Rates 2018** と呼ばれる価格表には、次の **ロール価格** 行があります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="dedb9-116">標準タイトル</span><span class="sxs-lookup"><span data-stu-id="dedb9-116">Standard Title</span></span>         | <span data-ttu-id="dedb9-117">組織単位</span><span class="sxs-lookup"><span data-stu-id="dedb9-117">Org Unit</span></span>    |<span data-ttu-id="dedb9-118">出荷単位</span><span class="sxs-lookup"><span data-stu-id="dedb9-118">Unit</span></span>   |<span data-ttu-id="dedb9-119">価格</span><span class="sxs-lookup"><span data-stu-id="dedb9-119">Price</span></span>  |<span data-ttu-id="dedb9-120">[通貨]</span><span class="sxs-lookup"><span data-stu-id="dedb9-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="dedb9-121">システム エンジニア</span><span class="sxs-lookup"><span data-stu-id="dedb9-121">Systems Engineer</span></span>|<span data-ttu-id="dedb9-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="dedb9-122">Contoso US</span></span>|<span data-ttu-id="dedb9-123">Hour</span><span class="sxs-lookup"><span data-stu-id="dedb9-123">Hour</span></span>| <span data-ttu-id="dedb9-124">100</span><span class="sxs-lookup"><span data-stu-id="dedb9-124">100</span></span>|<span data-ttu-id="dedb9-125">USD</span><span class="sxs-lookup"><span data-stu-id="dedb9-125">USD</span></span>|
| <span data-ttu-id="dedb9-126">シニア システム エンジニア</span><span class="sxs-lookup"><span data-stu-id="dedb9-126">Senior Systems Engineer</span></span>|<span data-ttu-id="dedb9-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="dedb9-127">Contoso US</span></span>|<span data-ttu-id="dedb9-128">Hour</span><span class="sxs-lookup"><span data-stu-id="dedb9-128">Hour</span></span>| <span data-ttu-id="dedb9-129">150</span><span class="sxs-lookup"><span data-stu-id="dedb9-129">150</span></span>| <span data-ttu-id="dedb9-130">USD</span><span class="sxs-lookup"><span data-stu-id="dedb9-130">USD</span></span>|


<span data-ttu-id="dedb9-131">価格設定ディメンションとしての **標準タイトル** を停止する場合、Project Service 価格設定エンジンによって価格を検索する場合、入力コンテキストの **組織単位** 値のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dedb9-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="dedb9-132">入力コンテキストの **組織単位** が 「Contoso US」であるとすると、その行の両方が一致するため、結果が非確定的になります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="dedb9-133">このシナリオを回避するため、**ロール価格** レコードを作成する際に、Project Service によって、ディメンションの組み合わせが一意であることが検証されます。</span><span class="sxs-lookup"><span data-stu-id="dedb9-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="dedb9-134">**ロール価格** レコードを作成後にディメンションを停止した場合、この制約に違反する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dedb9-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="dedb9-135">したがって、ディメンションを停止する前に必要なことは、ディメンション値が有効になっている **ロール価格** および **ロール価格の利幅** 行をすべて削除することです。</span><span class="sxs-lookup"><span data-stu-id="dedb9-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

