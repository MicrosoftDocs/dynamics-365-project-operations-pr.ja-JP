---
title: 価格ディメンションとしてカスタム フィールドを設定する
description: このトピックではカスタム価格ディメンションのセットアップについて説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
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
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150359"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="691bf-103">価格ディメンションとしてカスタム フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="691bf-103">Setting up custom fields as pricing dimensions</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="691bf-104">開始する前に、このトピックはユーザーがこれらのトピックの手順を完了していることを前提としています: [カスタム フィールドおよびエンティティを作成する](create-custom-fields-entities.md) および[価格設定とトランザクション エンティティに対してユカスタム フィールドを追加する](field-references.md)</span><span class="sxs-lookup"><span data-stu-id="691bf-104">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md) and [Add custom fields to price setup and transactional entities](field-references.md).</span></span> <span data-ttu-id="691bf-105">次に、これらの手順を完了していない場合は、戻ってこれらを完了してから、このトピックに戻ってください。</span><span class="sxs-lookup"><span data-stu-id="691bf-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="691bf-106">このトピックではカスタム価格ディメンションのセットアップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="691bf-106">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="691bf-107">Project Service Web インターフェイスでは、**パラメーター** ページの **金額ベースの価格ディメンション** タブに、価格ディメンション エンティティのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="691bf-107">In the Project Service web interface, on the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="691bf-108">既定では、Project Service のインストールによって、このタブのグリッドには二つの行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="691bf-108">By default, Project Service installation creates 2 rows in the grid on this tab:</span></span>

- <span data-ttu-id="691bf-109">**msdyn_resourcecategory** (ロール)</span><span class="sxs-lookup"><span data-stu-id="691bf-109">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="691bf-110">**msdyn_OrganizationalUnit** (組織単位)</span><span class="sxs-lookup"><span data-stu-id="691bf-110">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="691bf-111">これらの行を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="691bf-111">Do not delete these rows.</span></span> <span data-ttu-id="691bf-112">ただし、これらが必要ない場合は、 **コストに適用可能**、**営業に適用可能**、**購入に適用可能** をすべて **いいえ** に設定することによって特定のコンテキストでは適用されないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="691bf-112">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="691bf-113">これらの属性値を **いいえ** に設定すると、価格ディメンションとしてのフィールドがないのと同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="691bf-113">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="691bf-114">価格ディメンションにするフィールドに関して、次のようにする必要があります:</span><span class="sxs-lookup"><span data-stu-id="691bf-114">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="691bf-115">**ロール価格** および **ロール価格の利幅** エンティティでフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="691bf-115">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="691bf-116">この方法についての詳細は、[価格設定とトランザクション エンティティに対してカスタム フィールドを追加する](field-references.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="691bf-116">For more information on how to do this, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>
- <span data-ttu-id="691bf-117">**価格ディメンション** テーブルに行が作成されました</span><span class="sxs-lookup"><span data-stu-id="691bf-117">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="691bf-118">たとえば、次のグラフィックに示すように、価格ディメンションの行を追加します。</span><span class="sxs-lookup"><span data-stu-id="691bf-118">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![金額ベースの価格ディメンションの行](media/Amt-based-PD.png)

<span data-ttu-id="691bf-120">注意: リソースの作業時間 (**msdyn_resourceworkhours**)は 利幅ベースのディメンションとして追加され、また、 **利幅ベースの価格ディメンション** タブに追加されました。</span><span class="sxs-lookup"><span data-stu-id="691bf-120">Notice that Resource Work hours (**msdyn_resourceworkhours**) has been added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![利幅ベースの価格ディメンションの行](media/Markup-based-PD.png)

> [!IMPORTANT]
> <span data-ttu-id="691bf-122">このテーブルの価格ディメンション データに対する変更は、既存か新規かに関わらず、キャッシュを更新した後、Project Service 価格設定のビジネス ロジックに伝播されます。</span><span class="sxs-lookup"><span data-stu-id="691bf-122">Any change to pricing dimension data in this table, existing or new, is propagated to the Project Service pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="691bf-123">キャッシュの更新時間は最大で10分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="691bf-123">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="691bf-124">この時間を使って、価格ディメンション データに対する変更に明らかに起因する既定の価格設定ロジックの変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="691bf-124">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="691bf-125">価格ディメンション テーブルの属性</span><span class="sxs-lookup"><span data-stu-id="691bf-125">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="691bf-126">次のセクションでは、**価格ディメンション** テーブルのさまざまな属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="691bf-126">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="691bf-127">価格ディメンションの名前</span><span class="sxs-lookup"><span data-stu-id="691bf-127">Pricing Dimension Name</span></span>
<span data-ttu-id="691bf-128">この値は、カスタム価格ディメンションの **ロール価格** テーブルに追加されているフィールドのスキーマ名と同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="691bf-128">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="691bf-129">フィールドを **ロール価格** テーブルに追加する方法の詳細については、[価格設定およびトランザクション エンティティにユーザー定義フィールドを追加する](field-references.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="691bf-129">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="691bf-130">ディメンションの種類</span><span class="sxs-lookup"><span data-stu-id="691bf-130">Type of dimension</span></span>
<span data-ttu-id="691bf-131">価格ディメンションには 2 種類あります。</span><span class="sxs-lookup"><span data-stu-id="691bf-131">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="691bf-132">**金額ベースのディメンション**: 入力コンテキストからのディメンション値は、**ロール価格** 行のディメンション値に一致し、価格/コストは、既定になって **ロール価格** テーブルから直接取得されます。</span><span class="sxs-lookup"><span data-stu-id="691bf-132">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="691bf-133">**利幅ベースのディメンション**: Project Service は、次の 3 段階ステップのプロセスが適用された、価格/コストを得るディメンションです。</span><span class="sxs-lookup"><span data-stu-id="691bf-133">**Markup-based dimensions**: These are dimensions where Project Service will adopt the following 3-step process to get the price/cost</span></span>
 
    1. <span data-ttu-id="691bf-134">Project Service では、入力コンテキストから非利幅ベースのディメンション値をロール価格行に一致させて、基本料金を取得します。</span><span class="sxs-lookup"><span data-stu-id="691bf-134">Project Service matches the non-markup-based dimension values from the input context to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="691bf-135">Project Service では、入力コンテキストからすべてのディメンション値を **ロール価格利幅** 行に一致させて、利幅率を取得できます。</span><span class="sxs-lookup"><span data-stu-id="691bf-135">Project Service matches all of the dimension values from the input context to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="691bf-136">Project Service では、2 番目の手順で得た利幅率を、最初の手順の **価格ロール** テーブルで取得済みの基本料金に適用して、最終的な価格/コストを算出します。</span><span class="sxs-lookup"><span data-stu-id="691bf-136">Project Service applies the markup percentage from the second step to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="691bf-137">次の表は、価格利幅の計算について説明したものです。</span><span class="sxs-lookup"><span data-stu-id="691bf-137">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="691bf-138">ロール</span><span class="sxs-lookup"><span data-stu-id="691bf-138">Role</span></span>        | <span data-ttu-id="691bf-139">組織単位</span><span class="sxs-lookup"><span data-stu-id="691bf-139">Org Unit</span></span>    |<span data-ttu-id="691bf-140">作業場所</span><span class="sxs-lookup"><span data-stu-id="691bf-140">Work Location</span></span>      |<span data-ttu-id="691bf-141">標準タイトル</span><span class="sxs-lookup"><span data-stu-id="691bf-141">Standard Title</span></span>      |<span data-ttu-id="691bf-142">リソースの作業時間</span><span class="sxs-lookup"><span data-stu-id="691bf-142">Resource Work Hours</span></span>      |  <span data-ttu-id="691bf-143">利幅</span><span class="sxs-lookup"><span data-stu-id="691bf-143">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="691bf-144">Contoso India</span><span class="sxs-lookup"><span data-stu-id="691bf-144">Contoso India</span></span>|<span data-ttu-id="691bf-145">オンサイト</span><span class="sxs-lookup"><span data-stu-id="691bf-145">Onsite</span></span>            |                    |<span data-ttu-id="691bf-146">残業</span><span class="sxs-lookup"><span data-stu-id="691bf-146">Overtime</span></span>                 |<span data-ttu-id="691bf-147">15</span><span class="sxs-lookup"><span data-stu-id="691bf-147">15</span></span>     |
|             | <span data-ttu-id="691bf-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="691bf-148">Contoso India</span></span>|<span data-ttu-id="691bf-149">ローカル</span><span class="sxs-lookup"><span data-stu-id="691bf-149">Local</span></span>             |                    |<span data-ttu-id="691bf-150">残業</span><span class="sxs-lookup"><span data-stu-id="691bf-150">Overtime</span></span>                 |<span data-ttu-id="691bf-151">10</span><span class="sxs-lookup"><span data-stu-id="691bf-151">10</span></span>     |
|             | <span data-ttu-id="691bf-152">Contoso US</span><span class="sxs-lookup"><span data-stu-id="691bf-152">Contoso US</span></span>   |<span data-ttu-id="691bf-153">ローカル</span><span class="sxs-lookup"><span data-stu-id="691bf-153">Local</span></span>             |                    |<span data-ttu-id="691bf-154">残業</span><span class="sxs-lookup"><span data-stu-id="691bf-154">Overtime</span></span>                 |<span data-ttu-id="691bf-155">20</span><span class="sxs-lookup"><span data-stu-id="691bf-155">20</span></span>     |


<span data-ttu-id="691bf-156">Contoso India の基本料金が 100 米国ドルのリソースがオンサイトで従事していて、時間エントリで 8 時間の標準時間および 2 時間の残業をログした場合、Project Service の価格設定エンジンは 8 時間に 100 の基本料金を使用して 800 米国ドルを記録します。</span><span class="sxs-lookup"><span data-stu-id="691bf-156">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the Project Service pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="691bf-157">残業時間 2 時間に関しては、15% の利幅が 100 の基本料金に適用され、115 米国ドルの単価を取得し、230 米国ドルの合計コストを記録します。</span><span class="sxs-lookup"><span data-stu-id="691bf-157">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="691bf-158">コストに適用可能</span><span class="sxs-lookup"><span data-stu-id="691bf-158">Applicable to Cost</span></span> 
<span data-ttu-id="691bf-159">これを **はい** に設定する場合、コストと利幅レートを取得する際に、入力コンテキストのディメンション値を **ロール価格** および **ロール価格の利幅** に一致させるように使用する必要があるということが示されています。</span><span class="sxs-lookup"><span data-stu-id="691bf-159">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="691bf-160">営業に適用可能</span><span class="sxs-lookup"><span data-stu-id="691bf-160">Applicable to Sales</span></span>
<span data-ttu-id="691bf-161">これを **はい** に設定する場合、請求書と利幅レートを取得する際に、入力コンテキストのディメンション値を **価格ロール** および **ロール価格の利幅** と一致させるように使用する必要があるということが示されています。</span><span class="sxs-lookup"><span data-stu-id="691bf-161">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="691bf-162">購入に適用可能</span><span class="sxs-lookup"><span data-stu-id="691bf-162">Applicable to Purchase</span></span>
<span data-ttu-id="691bf-163">これを **はい** に設定する場合、購入価格を取得する際に、入力コンテキストのディメンション値を **ロール価格** および **ロール価格の利幅** と一致させるように使用する必要があるということが示されています。</span><span class="sxs-lookup"><span data-stu-id="691bf-163">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="691bf-164">現在の Project Service は下請けシナリオをサポートしないため、このフィールドは使用されません。</span><span class="sxs-lookup"><span data-stu-id="691bf-164">Currently Project Service does not support subcontracting scenarios, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="691bf-165">重要度</span><span class="sxs-lookup"><span data-stu-id="691bf-165">Priority</span></span>
<span data-ttu-id="691bf-166">**ロール価格** または **ロール価格値幅** テーブルの入力ディメンション値と値の間で完全一致が見つからなくても、ディメンションのプライマリを設定をすることによって、Project Service 価格設定で価格を提供するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="691bf-166">Setting the dimension priority helps Project Service pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="691bf-167">このシナリオでは、Project Service によりディメンションが優先順位の順で重要視され、一致しないディメンション値に対しては null 値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="691bf-167">In this scenario, Project Service will use null values for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="691bf-168">**コストの優先度**: ディメンションのコストの優先度の値は、原価価格の設定と一致する場合のディメンションの重要度を示します。</span><span class="sxs-lookup"><span data-stu-id="691bf-168">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="691bf-169">**コストの優先度** の値は、 **コストに適用可能** なディメンション全体で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="691bf-169">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="691bf-170">**営業の優先度**: ディメンションの営業の優先度の値は、販売価格または請求レートの設定と一致する場合のディメンションの重要度を示します。</span><span class="sxs-lookup"><span data-stu-id="691bf-170">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="691bf-171">**営業の優先度** の値は、 **営業に適用可能** であるディメンション全体で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="691bf-171">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>
