---
title: 価格設定のディメンションをオフにする
description: このトピックでは、Project Service ソリューションの価格設定ディメンションを設定する方法を説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281844"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="1d524-103">価格設定のディメンションをオフにする</span><span class="sxs-lookup"><span data-stu-id="1d524-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1d524-104">価格設定戦略を数年度ごとにレビューし、更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d524-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="1d524-105">何らかの更新を行うと、既存の価格設定のディメンションを停止して新たに作成しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d524-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="1d524-106">たとえば、以前は、**ロール** によって価格設定を行っていたとしても、現在は、**ワーク エクスペリエンス** によって価格設定することを決定しています。</span><span class="sxs-lookup"><span data-stu-id="1d524-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="1d524-107">この場合、価格設定のディメンションとして、**ロール** を停止し、 **ワーク エクスペリエンス** を新しい価格設定のディメンションとして作成する必要があるかもしれます。</span><span class="sxs-lookup"><span data-stu-id="1d524-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="1d524-108">価格設定のディメンションを停止するには、それが標準であるかカスタムであるかにかかわらず、価格設定ディメンションの **コストに適用可能** および **営業に適用可能** フィールドを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1d524-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="1d524-109">ただし、これを実行すると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d524-109">However, when you do this, you might receive the following error message.</span></span>

![価格設定のディメンションを停止したとき、生じる可能性が高いビジネス プロセス エラー](media/Business-Process-Error.png)


<span data-ttu-id="1d524-111">このエラー メッセージは、停止されているディメンションに対して過去に設定済みの価格のレコードが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="1d524-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="1d524-112">ディメンションを参照するすべての **ロール価格** および **ロール価格利幅** レコード は、ディメンションの適用領域を **いいえ** に設定する可能性があればその前に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d524-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="1d524-113">このルールは、作成済みの双方の標準価格ディメンションおよび任意のカスタム価格ディメンションに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d524-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="1d524-114">この検証を行うのは、Project Service では **ロール価格** の各レコードに、制約上、一意のディメンションの組み合わせが必要であるためです。</span><span class="sxs-lookup"><span data-stu-id="1d524-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="1d524-115">たとえば、**US Cost Rates 2018** と呼ばれる価格表には、次の **ロール価格** 行があります。</span><span class="sxs-lookup"><span data-stu-id="1d524-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="1d524-116">標準タイトル</span><span class="sxs-lookup"><span data-stu-id="1d524-116">Standard Title</span></span>         | <span data-ttu-id="1d524-117">組織単位</span><span class="sxs-lookup"><span data-stu-id="1d524-117">Org Unit</span></span>    |<span data-ttu-id="1d524-118">出荷単位</span><span class="sxs-lookup"><span data-stu-id="1d524-118">Unit</span></span>   |<span data-ttu-id="1d524-119">価格</span><span class="sxs-lookup"><span data-stu-id="1d524-119">Price</span></span>  |<span data-ttu-id="1d524-120">[通貨]</span><span class="sxs-lookup"><span data-stu-id="1d524-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="1d524-121">システム エンジニア</span><span class="sxs-lookup"><span data-stu-id="1d524-121">Systems Engineer</span></span>|<span data-ttu-id="1d524-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1d524-122">Contoso US</span></span>|<span data-ttu-id="1d524-123">Hour</span><span class="sxs-lookup"><span data-stu-id="1d524-123">Hour</span></span>| <span data-ttu-id="1d524-124">100</span><span class="sxs-lookup"><span data-stu-id="1d524-124">100</span></span>|<span data-ttu-id="1d524-125">USD</span><span class="sxs-lookup"><span data-stu-id="1d524-125">USD</span></span>|
| <span data-ttu-id="1d524-126">シニア システム エンジニア</span><span class="sxs-lookup"><span data-stu-id="1d524-126">Senior Systems Engineer</span></span>|<span data-ttu-id="1d524-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1d524-127">Contoso US</span></span>|<span data-ttu-id="1d524-128">Hour</span><span class="sxs-lookup"><span data-stu-id="1d524-128">Hour</span></span>| <span data-ttu-id="1d524-129">150</span><span class="sxs-lookup"><span data-stu-id="1d524-129">150</span></span>| <span data-ttu-id="1d524-130">USD</span><span class="sxs-lookup"><span data-stu-id="1d524-130">USD</span></span>|


<span data-ttu-id="1d524-131">価格設定ディメンションとしての **標準タイトル** を停止する場合、Project Service 価格設定エンジンによって価格を検索する場合、入力コンテキストの **組織単位** 値のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d524-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="1d524-132">入力コンテキストの **組織単位** が 「Contoso US」であるとすると、その行の両方が一致するため、結果が非確定的になります。</span><span class="sxs-lookup"><span data-stu-id="1d524-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="1d524-133">このシナリオを回避するため、**ロール価格** レコードを作成する際に、Project Service によって、ディメンションの組み合わせが一意であることが検証されます。</span><span class="sxs-lookup"><span data-stu-id="1d524-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="1d524-134">**ロール価格** レコードを作成後にディメンションを停止した場合、この制約に違反する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d524-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="1d524-135">したがって、ディメンションを停止する前に必要なことは、ディメンション値が有効になっている **ロール価格** および **ロール価格の利幅** 行をすべて削除することです。</span><span class="sxs-lookup"><span data-stu-id="1d524-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]