---
title: 価格とコストのディメンションのホーム ページ
description: このトピックでは、価格ディメンションの概要を説明します。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752837"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="8e0e3-103">価格とコストのディメンションのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="8e0e3-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="8e0e3-104">価格およびコストを設定するために人的リソースで使用されるディメンションは、2 つのカテゴリに分類されます:</span><span class="sxs-lookup"><span data-stu-id="8e0e3-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="8e0e3-105">人員</span><span class="sxs-lookup"><span data-stu-id="8e0e3-105">People</span></span>
- <span data-ttu-id="8e0e3-106">予定作業</span><span class="sxs-lookup"><span data-stu-id="8e0e3-106">Planned work</span></span>

<span data-ttu-id="8e0e3-107">したがって、Project Service Automation (PSA)で使用可能な価格ディメンション値には 2 つの種類があります:</span><span class="sxs-lookup"><span data-stu-id="8e0e3-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="8e0e3-108">**オプション セット** - 一連の値の固定リストであるディメンション。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="8e0e3-109">**エンティティ ベースの値**  - 様々な値のセットとなるディメンション。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="8e0e3-110">価格ディメンション</span><span class="sxs-lookup"><span data-stu-id="8e0e3-110">Pricing dimensions</span></span>

<span data-ttu-id="8e0e3-111">PSAには、価格ディメンションの既定セットが付属しています。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="8e0e3-112">これらを表示するには、 **Project Service** > **パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="8e0e3-113">パラメーター レコードの **金額ベースの価格ディメンション** タブで、ロール **msdyn_resourcecategory** と リソース組織単位 **msdyn_organizationalunit** のフィールド **営業に適用可能** と **コストに適用可能** が **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="8e0e3-114">これによって各ロールや組織単位の組み合わせの価格とコストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![強調表示された 「営業に適用可能」 の Project Service パラメーターのスクリーンショット](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="8e0e3-116">PSAのバージョン 3 よりも前に、価格ディメンションとしてロールと組織単位の標準フィールドを使用していた場合、注目すべき変更はありません。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="8e0e3-117">通常どおり Project Service を引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="8e0e3-118">追加の属性を使用してリソースの価格やコストを設定する必要がある場合は、カスタマイズしたフィールド、エンティティおよびディメンションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="8e0e3-119">詳細については、以下のトピックを参照してください。ただし、次に示す順序で手順を実行する必要があることに注意してください:</span><span class="sxs-lookup"><span data-stu-id="8e0e3-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="8e0e3-120">カスタム フィールドとエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="8e0e3-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="8e0e3-121">価格設定とトランザクション エンティティに対してユーザー定義フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="8e0e3-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="8e0e3-122">価格ディメンションとしてカスタム フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="8e0e3-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="8e0e3-123">プラグインの属性を更新して新しい価格ディメンションを含める</span><span class="sxs-lookup"><span data-stu-id="8e0e3-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="8e0e3-124">人的リソース時間の価格設定</span><span class="sxs-lookup"><span data-stu-id="8e0e3-124">Pricing human resource time</span></span>
<span data-ttu-id="8e0e3-125">組織が人的リソース時間をどのように価格設定するかは、多くの場合、組織の収益性に直接影響する重要な戦略的考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="8e0e3-126">組織が人的リソース時間の請求レートとコスト レートの設定方法を決定する準備ができたら、財務チームおよび実務担当者と連携します。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="8e0e3-127">価格設定に関する他の検討事項には、現在価格ディメンションではないが組織の価格ディメンションとして適用されるフィールドまたはエンティティを再利用するかどうかがあります。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="8e0e3-128">**トランザクション カテゴリ** (**msdyn_transactioncategory**) と **予約可能リソース** (**bookableresource**) のようなフィールドが候補のディメンションの例です。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="8e0e3-129">また、価格ディメンションをテーブルにするかオプション セットにするかを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="8e0e3-130">10または12を超えるディメンション値の変更が予測され、これらの値の追加の属性が必要な場合は、オプション セットではなくエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="8e0e3-131">ほとんどのユーザーは、テーブルに新しい行を追加できますが、値の追加または削除などのオプション セットを管理するには、管理者または開発者が必要です。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="8e0e3-132">次の例にリソースが属するロールやリソースの組織単位に基づいて設定される請求レートを示します。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="8e0e3-133">通常、コスト レートは従業員の給与範囲および所属する組織単位に基づきます。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="8e0e3-134">この例では、請求レートとコストレートのテーブルは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="8e0e3-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="8e0e3-135">**サンプル請求レート**</span><span class="sxs-lookup"><span data-stu-id="8e0e3-135">**Sample bill rates**</span></span>

| <span data-ttu-id="8e0e3-136">ロール</span><span class="sxs-lookup"><span data-stu-id="8e0e3-136">Role</span></span>        | <span data-ttu-id="8e0e3-137">組織単位</span><span class="sxs-lookup"><span data-stu-id="8e0e3-137">Org Unit</span></span>    |<span data-ttu-id="8e0e3-138">出荷単位</span><span class="sxs-lookup"><span data-stu-id="8e0e3-138">Unit</span></span>      |<span data-ttu-id="8e0e3-139">価格</span><span class="sxs-lookup"><span data-stu-id="8e0e3-139">Price</span></span>      |<span data-ttu-id="8e0e3-140">[通貨]</span><span class="sxs-lookup"><span data-stu-id="8e0e3-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8e0e3-141">開発者</span><span class="sxs-lookup"><span data-stu-id="8e0e3-141">Developer</span></span>   | <span data-ttu-id="8e0e3-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8e0e3-142">Contoso US</span></span>  |<span data-ttu-id="8e0e3-143">Hour</span><span class="sxs-lookup"><span data-stu-id="8e0e3-143">Hour</span></span> | <span data-ttu-id="8e0e3-144">200</span><span class="sxs-lookup"><span data-stu-id="8e0e3-144">200</span></span>|<span data-ttu-id="8e0e3-145">USD</span><span class="sxs-lookup"><span data-stu-id="8e0e3-145">USD</span></span>     |
| <span data-ttu-id="8e0e3-146">開発者</span><span class="sxs-lookup"><span data-stu-id="8e0e3-146">Developer</span></span>   | <span data-ttu-id="8e0e3-147">Contoso India社</span><span class="sxs-lookup"><span data-stu-id="8e0e3-147">Contoso India</span></span> |<span data-ttu-id="8e0e3-148">Hour</span><span class="sxs-lookup"><span data-stu-id="8e0e3-148">Hour</span></span>|   <span data-ttu-id="8e0e3-149">112</span><span class="sxs-lookup"><span data-stu-id="8e0e3-149">112</span></span>|<span data-ttu-id="8e0e3-150">USD</span><span class="sxs-lookup"><span data-stu-id="8e0e3-150">USD</span></span>     |


<span data-ttu-id="8e0e3-151">**サンプル コスト レート**</span><span class="sxs-lookup"><span data-stu-id="8e0e3-151">**Sample cost rates**</span></span>

| <span data-ttu-id="8e0e3-152">給与範囲</span><span class="sxs-lookup"><span data-stu-id="8e0e3-152">Salary Band</span></span>     | <span data-ttu-id="8e0e3-153">組織単位</span><span class="sxs-lookup"><span data-stu-id="8e0e3-153">Org Unit</span></span>    |<span data-ttu-id="8e0e3-154">出荷単位</span><span class="sxs-lookup"><span data-stu-id="8e0e3-154">Unit</span></span>      |<span data-ttu-id="8e0e3-155">価格</span><span class="sxs-lookup"><span data-stu-id="8e0e3-155">Price</span></span>      |<span data-ttu-id="8e0e3-156">[通貨]</span><span class="sxs-lookup"><span data-stu-id="8e0e3-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8e0e3-157">自分の会社_Band1</span><span class="sxs-lookup"><span data-stu-id="8e0e3-157">My company_Band1</span></span> | <span data-ttu-id="8e0e3-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8e0e3-158">Contoso US</span></span>  |<span data-ttu-id="8e0e3-159">Hour</span><span class="sxs-lookup"><span data-stu-id="8e0e3-159">Hour</span></span> | <span data-ttu-id="8e0e3-160">145</span><span class="sxs-lookup"><span data-stu-id="8e0e3-160">145</span></span>|<span data-ttu-id="8e0e3-161">USD</span><span class="sxs-lookup"><span data-stu-id="8e0e3-161">USD</span></span>     |
| <span data-ttu-id="8e0e3-162">自分の会社_Band2</span><span class="sxs-lookup"><span data-stu-id="8e0e3-162">My company_Band2</span></span> | <span data-ttu-id="8e0e3-163">Contoso India社</span><span class="sxs-lookup"><span data-stu-id="8e0e3-163">Contoso India</span></span> |<span data-ttu-id="8e0e3-164">Hour</span><span class="sxs-lookup"><span data-stu-id="8e0e3-164">Hour</span></span>|   <span data-ttu-id="8e0e3-165">67</span><span class="sxs-lookup"><span data-stu-id="8e0e3-165">67</span></span>|<span data-ttu-id="8e0e3-166">USD</span><span class="sxs-lookup"><span data-stu-id="8e0e3-166">USD</span></span>     |
