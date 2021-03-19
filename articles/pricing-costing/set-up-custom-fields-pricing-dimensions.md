---
title: 価格ディメンションとしてカスタム フィールドを設定する
description: このトピックではユーザー定義の価格ディメンションの設定方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1468c3396a01c1bee1bc0f47eac1ee8b44eaa459
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274869"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="0e9eb-103">価格ディメンションとしてカスタム フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="0e9eb-103">Set up custom fields as pricing dimensions</span></span>

<span data-ttu-id="0e9eb-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="0e9eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e9eb-105">開始する前に、このトピックはユーザーが次のトピックの手順を完了していることを前提としています: [ユーザー定義のフィールドとエンティティの作成](create-custom-fields-entities-pricing-dimensions.md) および[ユーザー定義のフィールドを追加して価格設定とトランザクション エンティティを設定する](add-custom-fields-price-setup-transactional-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-105">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities-pricing-dimensions.md) and [Add required custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span> <span data-ttu-id="0e9eb-106">次に、これらの手順を完了していない場合は、戻ってこれらを完了してから、このトピックに戻ってください。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="0e9eb-107">このトピックではカスタム価格ディメンションのセットアップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-107">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="0e9eb-108">**パラメーター**  ページ、**金額ベースの価格設定ディメンション**  タブでは、価格設定ディメンション エンティティのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-108">On the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="0e9eb-109">既定では、このタブのグリッドには 2 つの行があります :</span><span class="sxs-lookup"><span data-stu-id="0e9eb-109">By default, there are two rows in the grid on this tab:</span></span>

- <span data-ttu-id="0e9eb-110">**msdyn_resourcecategory** (ロール)</span><span class="sxs-lookup"><span data-stu-id="0e9eb-110">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="0e9eb-111">**msdyn_OrganizationalUnit** (組織単位)</span><span class="sxs-lookup"><span data-stu-id="0e9eb-111">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e9eb-112">これらの行を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-112">Do not delete these rows.</span></span> <span data-ttu-id="0e9eb-113">ただし、これらが必要ない場合は、 **コストに適用可能**、**営業に適用可能**、**購入に適用可能** をすべて **いいえ** に設定することによって特定のコンテキストでは適用されないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-113">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="0e9eb-114">これらの属性値を **いいえ** に設定すると、価格ディメンションとしてのフィールドがないのと同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-114">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="0e9eb-115">価格ディメンションにするフィールドに関して、次のようにする必要があります:</span><span class="sxs-lookup"><span data-stu-id="0e9eb-115">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="0e9eb-116">**ロール価格** および **ロール価格の利幅** エンティティでフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-116">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="0e9eb-117">この方法についての詳細は、[価格設定とトランザクション エンティティに対してカスタム フィールドを追加する](add-custom-fields-price-setup-transactional-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-117">For more information on how to do this, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

- <span data-ttu-id="0e9eb-118">**価格ディメンション** テーブルに行が作成されました</span><span class="sxs-lookup"><span data-stu-id="0e9eb-118">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="0e9eb-119">たとえば、次のグラフィックに示すように、価格ディメンションの行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-119">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![金額ベースの価格ディメンションの行](media/Amt-based-PD.png)

<span data-ttu-id="0e9eb-121">リソースの作業時間 (**msdyn_resourceworkhours**)は 利幅ベースのディメンションとして追加され、また、 **利幅ベースの価格ディメンション** タブに追加されています。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-121">Resource Work hours (**msdyn_resourceworkhours**) is added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![利幅ベースの価格ディメンションの行](media/Markup-based-PD.png)


> [!IMPORTANT]
> <span data-ttu-id="0e9eb-123">このテーブルの価格ディメンション データに対する変更は、既存か新規かに関わらず、キャッシュの更新後は、価格設定のビジネス ロジックに反映されます。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-123">Any change to pricing dimension data in this table, existing or new, is propagated to the pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="0e9eb-124">キャッシュの更新時間は最大で10分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-124">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="0e9eb-125">この時間を使って、価格ディメンション データに対する変更に明らかに起因する既定の価格設定ロジックの変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-125">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="0e9eb-126">価格ディメンション テーブルの属性</span><span class="sxs-lookup"><span data-stu-id="0e9eb-126">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="0e9eb-127">次のセクションでは、**価格ディメンション** テーブルのさまざまな属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-127">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="0e9eb-128">価格ディメンションの名前</span><span class="sxs-lookup"><span data-stu-id="0e9eb-128">Pricing Dimension Name</span></span>
<span data-ttu-id="0e9eb-129">この値は、カスタム価格ディメンションの **ロール価格** テーブルに追加されているフィールドのスキーマ名と同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-129">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="0e9eb-130">フィールドを **ロール価格** テーブルに追加する方法の詳細については、[価格設定およびトランザクション エンティティにユーザー定義フィールドを追加する](add-custom-fields-price-setup-transactional-entities.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-130">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="0e9eb-131">ディメンションの種類</span><span class="sxs-lookup"><span data-stu-id="0e9eb-131">Type of dimension</span></span>
<span data-ttu-id="0e9eb-132">価格ディメンションには 2 種類あります。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-132">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="0e9eb-133">**金額ベースのディメンション**: 入力コンテキストからのディメンション値は、**ロール価格** 行のディメンション値に一致し、価格/コストは、既定になって **ロール価格** テーブルから直接取得されます。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-133">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="0e9eb-134">**利幅ベースのディメンション** : これらは、価格/コストを取得する目的で以下の 3 段階のプロセスを使用しているディメンションです :</span><span class="sxs-lookup"><span data-stu-id="0e9eb-134">**Markup-based dimensions**: These are dimensions where the following three-step process to get the price/cost is used:</span></span>
 
    1. <span data-ttu-id="0e9eb-135">入力コンテキストから非利幅ベースのディメンション値をロール価格の明細に一致させて、基本料金を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-135">The non-markup-based dimension values from the input context are matched to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="0e9eb-136">入力コンテキストからすべてのディメンション値を **ロール価格利幅** の明細に一致させて、利幅率を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-136">The dimension values from the input context are matched to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="0e9eb-137">2 番目の手順で得た利幅率を、最初の手順の **ロール価格** テーブルで取得済みの基本料金に適用して、最終的な価格/コストを算出します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-137">The markup percentage from the second step is applied to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="0e9eb-138">次の表は、価格利幅の計算について説明したものです。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-138">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="0e9eb-139">ロール</span><span class="sxs-lookup"><span data-stu-id="0e9eb-139">Role</span></span>        | <span data-ttu-id="0e9eb-140">組織単位</span><span class="sxs-lookup"><span data-stu-id="0e9eb-140">Org Unit</span></span>    |<span data-ttu-id="0e9eb-141">作業場所</span><span class="sxs-lookup"><span data-stu-id="0e9eb-141">Work Location</span></span>      |<span data-ttu-id="0e9eb-142">標準タイトル</span><span class="sxs-lookup"><span data-stu-id="0e9eb-142">Standard Title</span></span>      |<span data-ttu-id="0e9eb-143">リソースの作業時間</span><span class="sxs-lookup"><span data-stu-id="0e9eb-143">Resource Work Hours</span></span>      |  <span data-ttu-id="0e9eb-144">利幅</span><span class="sxs-lookup"><span data-stu-id="0e9eb-144">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="0e9eb-145">Contoso India</span><span class="sxs-lookup"><span data-stu-id="0e9eb-145">Contoso India</span></span>|<span data-ttu-id="0e9eb-146">オンサイト</span><span class="sxs-lookup"><span data-stu-id="0e9eb-146">Onsite</span></span>            |                    |<span data-ttu-id="0e9eb-147">残業</span><span class="sxs-lookup"><span data-stu-id="0e9eb-147">Overtime</span></span>                 |<span data-ttu-id="0e9eb-148">15</span><span class="sxs-lookup"><span data-stu-id="0e9eb-148">15</span></span>     |
|             | <span data-ttu-id="0e9eb-149">Contoso India</span><span class="sxs-lookup"><span data-stu-id="0e9eb-149">Contoso India</span></span>|<span data-ttu-id="0e9eb-150">ローカル</span><span class="sxs-lookup"><span data-stu-id="0e9eb-150">Local</span></span>             |                    |<span data-ttu-id="0e9eb-151">残業</span><span class="sxs-lookup"><span data-stu-id="0e9eb-151">Overtime</span></span>                 |<span data-ttu-id="0e9eb-152">10</span><span class="sxs-lookup"><span data-stu-id="0e9eb-152">10</span></span>     |
|             | <span data-ttu-id="0e9eb-153">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0e9eb-153">Contoso US</span></span>   |<span data-ttu-id="0e9eb-154">ローカル</span><span class="sxs-lookup"><span data-stu-id="0e9eb-154">Local</span></span>             |                    |<span data-ttu-id="0e9eb-155">残業</span><span class="sxs-lookup"><span data-stu-id="0e9eb-155">Overtime</span></span>                 |<span data-ttu-id="0e9eb-156">20</span><span class="sxs-lookup"><span data-stu-id="0e9eb-156">20</span></span>     |


<span data-ttu-id="0e9eb-157">Contoso India の基本料金が 100 米国ドルのリソースがオンサイトで従事していて、時間エントリで 8 時間の標準時間および 2 時間の残業をログした場合、価格設定エンジンは 8 時間に 100 の基本料金を使用して 800 米国ドルを記録します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-157">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="0e9eb-158">残業時間 2 時間に関しては、15% の利幅が 100 の基本料金に適用され、115 米国ドルの単価を取得し、230 米国ドルの合計コストを記録します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-158">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="0e9eb-159">コストに適用可能</span><span class="sxs-lookup"><span data-stu-id="0e9eb-159">Applicable to Cost</span></span> 
<span data-ttu-id="0e9eb-160">これを **はい** に設定する場合、コストと利幅レートを取得する際に、入力コンテキストのディメンション値を **ロール価格** および **ロール価格の利幅** に一致させるように使用する必要があるということが示されています。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-160">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="0e9eb-161">営業に適用可能</span><span class="sxs-lookup"><span data-stu-id="0e9eb-161">Applicable to Sales</span></span>
<span data-ttu-id="0e9eb-162">これを **はい** に設定する場合、請求書と利幅レートを取得する際に、入力コンテキストのディメンション値を **価格ロール** および **ロール価格の利幅** と一致させるように使用する必要があるということが示されています。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-162">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="0e9eb-163">購入に適用可能</span><span class="sxs-lookup"><span data-stu-id="0e9eb-163">Applicable to Purchase</span></span>
<span data-ttu-id="0e9eb-164">これを **はい** に設定する場合、購入価格を取得する際に、入力コンテキストのディメンション値を **ロール価格** および **ロール価格の利幅** と一致させるように使用する必要があるということが示されています。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-164">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="0e9eb-165">外注シナリオには対応していないため、このフィールドは使用されません。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-165">Subcontracting scenarios are not supported, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="0e9eb-166">優先順位</span><span class="sxs-lookup"><span data-stu-id="0e9eb-166">Priority</span></span>
<span data-ttu-id="0e9eb-167">ディメンションの優先度を設定すると、入力ディメンジョン値と **ロール価格** または **ロール価格値幅** テーブルの値が完全に一致しない場合でも、価格設定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-167">Setting the dimension priority helps pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="0e9eb-168">このシナリオでは、優先度の高い順にディメンションを重み付けすることで、一致しないディメンジョン値に null 値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-168">In this scenario, null values are used for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="0e9eb-169">**コストの優先度**: ディメンションのコストの優先度の値は、原価価格の設定と一致する場合のディメンションの重要度を示します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-169">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="0e9eb-170">**コストの優先度** の値は、 **コストに適用可能** なディメンション全体で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-170">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="0e9eb-171">**営業の優先度**: ディメンションの営業の優先度の値は、販売価格または請求レートの設定と一致する場合のディメンションの重要度を示します。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-171">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="0e9eb-172">**営業の優先度** の値は、 **営業に適用可能** であるディメンション全体で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e9eb-172">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]