---
title: 価格ディメンションの概要
description: このトピックでは、Dynamics 365 プロジェクト オペレーションの価格ディメンションについて説明します。
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128469"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="9349b-103">価格ディメンションの概要</span><span class="sxs-lookup"><span data-stu-id="9349b-103">Pricing dimensions overview</span></span>

<span data-ttu-id="9349b-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="9349b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9349b-105">価格およびコストを設定するために人的リソースで使用されるディメンションは、2 つのカテゴリに分類されます:</span><span class="sxs-lookup"><span data-stu-id="9349b-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="9349b-106">人員</span><span class="sxs-lookup"><span data-stu-id="9349b-106">People</span></span>
- <span data-ttu-id="9349b-107">予定作業</span><span class="sxs-lookup"><span data-stu-id="9349b-107">Planned work</span></span>

<span data-ttu-id="9349b-108">このため、2 種類の価格設定ディメンション値を使用できます :</span><span class="sxs-lookup"><span data-stu-id="9349b-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="9349b-109">**オプション セット** : 一連の値の固定リストであるディメンション。</span><span class="sxs-lookup"><span data-stu-id="9349b-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="9349b-110">**エンティティに基づく値** : 様々な値のセットとなるディメンション。</span><span class="sxs-lookup"><span data-stu-id="9349b-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="9349b-111">価格ディメンション</span><span class="sxs-lookup"><span data-stu-id="9349b-111">Pricing dimensions</span></span>

<span data-ttu-id="9349b-112">Dynamics 365 プロジェクト オペレーションには、価格設定ディメンションの既定のセットが付属しています。</span><span class="sxs-lookup"><span data-stu-id="9349b-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="9349b-113">これらの価格設定ディメンション表示するには、 **プロジェクト サービス** > **パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9349b-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="9349b-114">パラメーター レコードの **金額ベースの価格ディメンション** タブで、ロール **msdyn_resourcecategory** と リソース組織単位 **msdyn_organizationalunit** のフィールド **営業に適用可能** と **コストに適用可能** が **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9349b-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="9349b-115">これらのフィールドを有効化することで、各ロールや組織単位の組み合わせの価格とコストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9349b-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="9349b-116">追加の属性を使用してリソースの価格やコストを設定する必要がある場合は、カスタマイズしたフィールド、エンティティおよびディメンションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9349b-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="9349b-117">人的リソース時間の価格設定</span><span class="sxs-lookup"><span data-stu-id="9349b-117">Pricing human resource time</span></span>
<span data-ttu-id="9349b-118">組織が人的リソース時間をどのように価格設定するかは、多くの場合、組織の収益性に直接影響する重要な戦略的考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="9349b-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="9349b-119">組織が人的リソース時間の請求レートとコスト レートの設定方法を決定する準備ができたら、財務チームおよび実務担当者と連携します。</span><span class="sxs-lookup"><span data-stu-id="9349b-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="9349b-120">価格設定に関する他の検討事項には、現在価格ディメンションではないが組織の価格ディメンションとして適用されるフィールドまたはエンティティを再利用するかどうかがあります。</span><span class="sxs-lookup"><span data-stu-id="9349b-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="9349b-121">**トランザクション カテゴリ** (**msdyn_transactioncategory**) と **予約可能リソース** (**bookableresource**) のようなフィールドが候補のディメンションの例です。</span><span class="sxs-lookup"><span data-stu-id="9349b-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="9349b-122">価格ディメンションをテーブルにするかオプション セットにするかを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9349b-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="9349b-123">10または12を超えるディメンション値の変更が予測され、これらの値の追加の属性が必要な場合は、オプション セットではなくエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9349b-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="9349b-124">ほとんどのユーザーは、テーブルに新しい行を追加できますが、値の追加または削除などのオプション セットを管理するには、管理者または開発者が必要です。</span><span class="sxs-lookup"><span data-stu-id="9349b-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="9349b-125">次の例にリソースが属するロールやリソースの組織単位に基づいて設定される請求レートを示します。</span><span class="sxs-lookup"><span data-stu-id="9349b-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="9349b-126">通常、コスト レートは従業員の給与範囲および所属する組織単位に基づきます。</span><span class="sxs-lookup"><span data-stu-id="9349b-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="9349b-127">この例では、請求レートとコストレートのテーブルは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9349b-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="9349b-128">**サンプル請求レート**</span><span class="sxs-lookup"><span data-stu-id="9349b-128">**Sample bill rates**</span></span>

| <span data-ttu-id="9349b-129">ロール</span><span class="sxs-lookup"><span data-stu-id="9349b-129">Role</span></span>        | <span data-ttu-id="9349b-130">組織単位</span><span class="sxs-lookup"><span data-stu-id="9349b-130">Org Unit</span></span>    |<span data-ttu-id="9349b-131">出荷単位</span><span class="sxs-lookup"><span data-stu-id="9349b-131">Unit</span></span>      |<span data-ttu-id="9349b-132">価格</span><span class="sxs-lookup"><span data-stu-id="9349b-132">Price</span></span>      |<span data-ttu-id="9349b-133">[通貨]</span><span class="sxs-lookup"><span data-stu-id="9349b-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9349b-134">開発者</span><span class="sxs-lookup"><span data-stu-id="9349b-134">Developer</span></span>   | <span data-ttu-id="9349b-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="9349b-135">Contoso US</span></span>  |<span data-ttu-id="9349b-136">Hour</span><span class="sxs-lookup"><span data-stu-id="9349b-136">Hour</span></span> | <span data-ttu-id="9349b-137">200</span><span class="sxs-lookup"><span data-stu-id="9349b-137">200</span></span>|<span data-ttu-id="9349b-138">USD</span><span class="sxs-lookup"><span data-stu-id="9349b-138">USD</span></span>     |
| <span data-ttu-id="9349b-139">開発者</span><span class="sxs-lookup"><span data-stu-id="9349b-139">Developer</span></span>   | <span data-ttu-id="9349b-140">Contoso India社</span><span class="sxs-lookup"><span data-stu-id="9349b-140">Contoso India</span></span> |<span data-ttu-id="9349b-141">Hour</span><span class="sxs-lookup"><span data-stu-id="9349b-141">Hour</span></span>|   <span data-ttu-id="9349b-142">112</span><span class="sxs-lookup"><span data-stu-id="9349b-142">112</span></span>|<span data-ttu-id="9349b-143">USD</span><span class="sxs-lookup"><span data-stu-id="9349b-143">USD</span></span>     |


<span data-ttu-id="9349b-144">**サンプル コスト レート**</span><span class="sxs-lookup"><span data-stu-id="9349b-144">**Sample cost rates**</span></span>

| <span data-ttu-id="9349b-145">給与範囲</span><span class="sxs-lookup"><span data-stu-id="9349b-145">Salary Band</span></span>     | <span data-ttu-id="9349b-146">組織単位</span><span class="sxs-lookup"><span data-stu-id="9349b-146">Org Unit</span></span>    |<span data-ttu-id="9349b-147">出荷単位</span><span class="sxs-lookup"><span data-stu-id="9349b-147">Unit</span></span>      |<span data-ttu-id="9349b-148">価格</span><span class="sxs-lookup"><span data-stu-id="9349b-148">Price</span></span>      |<span data-ttu-id="9349b-149">[通貨]</span><span class="sxs-lookup"><span data-stu-id="9349b-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9349b-150">自分の会社_Band1</span><span class="sxs-lookup"><span data-stu-id="9349b-150">My company_Band1</span></span> | <span data-ttu-id="9349b-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="9349b-151">Contoso US</span></span>  |<span data-ttu-id="9349b-152">Hour</span><span class="sxs-lookup"><span data-stu-id="9349b-152">Hour</span></span> | <span data-ttu-id="9349b-153">145</span><span class="sxs-lookup"><span data-stu-id="9349b-153">145</span></span>|<span data-ttu-id="9349b-154">USD</span><span class="sxs-lookup"><span data-stu-id="9349b-154">USD</span></span>     |
| <span data-ttu-id="9349b-155">自分の会社_Band2</span><span class="sxs-lookup"><span data-stu-id="9349b-155">My company_Band2</span></span> | <span data-ttu-id="9349b-156">Contoso India社</span><span class="sxs-lookup"><span data-stu-id="9349b-156">Contoso India</span></span> |<span data-ttu-id="9349b-157">Hour</span><span class="sxs-lookup"><span data-stu-id="9349b-157">Hour</span></span>|   <span data-ttu-id="9349b-158">67</span><span class="sxs-lookup"><span data-stu-id="9349b-158">67</span></span>|<span data-ttu-id="9349b-159">USD</span><span class="sxs-lookup"><span data-stu-id="9349b-159">USD</span></span>     |
