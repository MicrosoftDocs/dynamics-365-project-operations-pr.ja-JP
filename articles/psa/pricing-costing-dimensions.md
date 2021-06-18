---
title: 価格とコストのディメンションのホーム ページ
description: このトピックでは、価格ディメンションの概要を説明します。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009262"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="42eeb-103">価格とコストのディメンションのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="42eeb-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="42eeb-104">プロジェクト ベースの組織で労働の価格とコストを設定するために使用されるディメンションは、次の属性の影響を受けます:</span><span class="sxs-lookup"><span data-stu-id="42eeb-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="42eeb-105">自分の経験、役割、または地理的に類似した仕事をしている人々</span><span class="sxs-lookup"><span data-stu-id="42eeb-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="42eeb-106">複雑さや時間帯に類似して行われる作業</span><span class="sxs-lookup"><span data-stu-id="42eeb-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="42eeb-107">これらの作業属性の典型的な性質と作業を実行するために必要な人員を考慮すると、Project Service Automation で使用できる価格ディメンション値には 2 つのタイプがあります:</span><span class="sxs-lookup"><span data-stu-id="42eeb-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="42eeb-108">**オプション セット** - 一連の値の固定リストである属性。</span><span class="sxs-lookup"><span data-stu-id="42eeb-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="42eeb-109">**エンティティ ベースの値** - 有限であるが時間の経過とともに変化する可能性のあるさまざまな値のセットを持つことができる属性。</span><span class="sxs-lookup"><span data-stu-id="42eeb-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="42eeb-110">価格ディメンション</span><span class="sxs-lookup"><span data-stu-id="42eeb-110">Pricing dimensions</span></span>

<span data-ttu-id="42eeb-111">PSAには、価格ディメンションの既定セットが付属しています。</span><span class="sxs-lookup"><span data-stu-id="42eeb-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="42eeb-112">これらを表示するには、 **Project Service** > **パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="42eeb-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="42eeb-113">パラメーター レコードの **金額ベースの価格ディメンション** タブで、ロール **msdyn_resourcecategory** と リソース組織単位 **msdyn_organizationalunit** のフィールド **営業に適用可能** と **コストに適用可能** が **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="42eeb-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="42eeb-114">これによって各ロールや組織単位の組み合わせの価格とコストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="42eeb-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![強調表示された 「営業に適用可能」 の Project Service パラメーターのスクリーンショット](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="42eeb-116">PSAのバージョン 3 よりも前に、価格ディメンションとしてロールと組織単位の標準フィールドを使用していた場合、注目すべき変更はありません。</span><span class="sxs-lookup"><span data-stu-id="42eeb-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="42eeb-117">通常どおり Project Service を引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="42eeb-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="42eeb-118">追加の属性を使用してリソースの価格やコストを設定する必要がある場合は、カスタマイズしたフィールド、エンティティおよびディメンションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="42eeb-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="42eeb-119">詳細については、以下のトピックを参照してください。ただし、次に示す順序で手順を実行する必要があることに注意してください:</span><span class="sxs-lookup"><span data-stu-id="42eeb-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="42eeb-120">カスタム フィールドとエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="42eeb-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="42eeb-121">価格設定とトランザクション エンティティに対してユーザー定義フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="42eeb-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="42eeb-122">価格ディメンションとしてカスタム フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="42eeb-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="42eeb-123">プラグインの属性を更新して新しい価格ディメンションを含める</span><span class="sxs-lookup"><span data-stu-id="42eeb-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="42eeb-124">人的リソース時間の価格設定</span><span class="sxs-lookup"><span data-stu-id="42eeb-124">Pricing human resource time</span></span>
<span data-ttu-id="42eeb-125">組織が人的リソース時間をどのように価格設定するかは、多くの場合、組織の収益性に直接影響する重要な戦略的考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="42eeb-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="42eeb-126">組織が人的リソース時間の請求レートとコスト レートの設定方法を決定する準備ができたら、財務チームおよび実務担当者と連携します。</span><span class="sxs-lookup"><span data-stu-id="42eeb-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="42eeb-127">価格設定に関する他の検討事項には、現在価格ディメンションではないが組織の価格ディメンションとして適用されるフィールドまたはエンティティを再利用するかどうかがあります。</span><span class="sxs-lookup"><span data-stu-id="42eeb-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="42eeb-128">**トランザクション カテゴリ** (**msdyn_transactioncategory**) と **予約可能リソース** (**bookableresource**) のようなフィールドが候補のディメンションの例です。</span><span class="sxs-lookup"><span data-stu-id="42eeb-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="42eeb-129">価格ディメンションをテーブルにするかオプション セットにするかを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42eeb-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="42eeb-130">10 または 12 を超えるディメンションの値への変更が予測され、これらの値に追加の属性が必要な場合は、オプション セットではなくエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="42eeb-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="42eeb-131">ほとんどのビジネス ユーザーは、テーブルに新しい行を追加できますが、値の追加や削除などのオプション セットを管理するには、管理者または開発者が必要です。</span><span class="sxs-lookup"><span data-stu-id="42eeb-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="42eeb-132">次の例にリソースが属するロールやリソースの組織単位に基づいて設定される請求レートを示します。</span><span class="sxs-lookup"><span data-stu-id="42eeb-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="42eeb-133">通常、コスト レートは従業員の給与範囲および所属する組織単位に基づきます。</span><span class="sxs-lookup"><span data-stu-id="42eeb-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="42eeb-134">この例では、請求レートとコストレートのテーブルは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="42eeb-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="42eeb-135">**サンプル請求レート**</span><span class="sxs-lookup"><span data-stu-id="42eeb-135">**Sample bill rates**</span></span>

| <span data-ttu-id="42eeb-136">ロール</span><span class="sxs-lookup"><span data-stu-id="42eeb-136">Role</span></span>        | <span data-ttu-id="42eeb-137">組織単位</span><span class="sxs-lookup"><span data-stu-id="42eeb-137">Org Unit</span></span>    |<span data-ttu-id="42eeb-138">単位</span><span class="sxs-lookup"><span data-stu-id="42eeb-138">Unit</span></span>      |<span data-ttu-id="42eeb-139">価格</span><span class="sxs-lookup"><span data-stu-id="42eeb-139">Price</span></span>      |<span data-ttu-id="42eeb-140">通貨</span><span class="sxs-lookup"><span data-stu-id="42eeb-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="42eeb-141">開発者</span><span class="sxs-lookup"><span data-stu-id="42eeb-141">Developer</span></span>   | <span data-ttu-id="42eeb-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="42eeb-142">Contoso US</span></span>  |<span data-ttu-id="42eeb-143">時</span><span class="sxs-lookup"><span data-stu-id="42eeb-143">Hour</span></span> | <span data-ttu-id="42eeb-144">200</span><span class="sxs-lookup"><span data-stu-id="42eeb-144">200</span></span>|<span data-ttu-id="42eeb-145">USD</span><span class="sxs-lookup"><span data-stu-id="42eeb-145">USD</span></span>     |
| <span data-ttu-id="42eeb-146">開発者</span><span class="sxs-lookup"><span data-stu-id="42eeb-146">Developer</span></span>   | <span data-ttu-id="42eeb-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="42eeb-147">Contoso India</span></span> |<span data-ttu-id="42eeb-148">時</span><span class="sxs-lookup"><span data-stu-id="42eeb-148">Hour</span></span>|   <span data-ttu-id="42eeb-149">112</span><span class="sxs-lookup"><span data-stu-id="42eeb-149">112</span></span>|<span data-ttu-id="42eeb-150">USD</span><span class="sxs-lookup"><span data-stu-id="42eeb-150">USD</span></span>     |


<span data-ttu-id="42eeb-151">**サンプル コスト レート**</span><span class="sxs-lookup"><span data-stu-id="42eeb-151">**Sample cost rates**</span></span>

| <span data-ttu-id="42eeb-152">給与範囲</span><span class="sxs-lookup"><span data-stu-id="42eeb-152">Salary Band</span></span>     | <span data-ttu-id="42eeb-153">組織単位</span><span class="sxs-lookup"><span data-stu-id="42eeb-153">Org Unit</span></span>    |<span data-ttu-id="42eeb-154">単位</span><span class="sxs-lookup"><span data-stu-id="42eeb-154">Unit</span></span>      |<span data-ttu-id="42eeb-155">価格</span><span class="sxs-lookup"><span data-stu-id="42eeb-155">Price</span></span>      |<span data-ttu-id="42eeb-156">通貨</span><span class="sxs-lookup"><span data-stu-id="42eeb-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="42eeb-157">自分の会社_Band1</span><span class="sxs-lookup"><span data-stu-id="42eeb-157">My company_Band1</span></span> | <span data-ttu-id="42eeb-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="42eeb-158">Contoso US</span></span>  |<span data-ttu-id="42eeb-159">時</span><span class="sxs-lookup"><span data-stu-id="42eeb-159">Hour</span></span> | <span data-ttu-id="42eeb-160">145</span><span class="sxs-lookup"><span data-stu-id="42eeb-160">145</span></span>|<span data-ttu-id="42eeb-161">USD</span><span class="sxs-lookup"><span data-stu-id="42eeb-161">USD</span></span>     |
| <span data-ttu-id="42eeb-162">自分の会社_Band2</span><span class="sxs-lookup"><span data-stu-id="42eeb-162">My company_Band2</span></span> | <span data-ttu-id="42eeb-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="42eeb-163">Contoso India</span></span> |<span data-ttu-id="42eeb-164">時</span><span class="sxs-lookup"><span data-stu-id="42eeb-164">Hour</span></span>|   <span data-ttu-id="42eeb-165">67</span><span class="sxs-lookup"><span data-stu-id="42eeb-165">67</span></span>|<span data-ttu-id="42eeb-166">USD</span><span class="sxs-lookup"><span data-stu-id="42eeb-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]