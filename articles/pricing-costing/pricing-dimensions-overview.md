---
title: 価格ディメンションの概要
description: このトピックは Dynamics 365 Project Operations の価格ディメンションに関する情報を提供します。
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ff675823d84c6e2b83be1e313f881bd672e53981
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275409"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="dc3ce-103">価格ディメンションの概要</span><span class="sxs-lookup"><span data-stu-id="dc3ce-103">Pricing dimensions overview</span></span>

<span data-ttu-id="dc3ce-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="dc3ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc3ce-105">価格およびコストを設定するために人的リソースで使用されるディメンションは、2 つのカテゴリに分類されます:</span><span class="sxs-lookup"><span data-stu-id="dc3ce-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="dc3ce-106">人員</span><span class="sxs-lookup"><span data-stu-id="dc3ce-106">People</span></span>
- <span data-ttu-id="dc3ce-107">予定作業</span><span class="sxs-lookup"><span data-stu-id="dc3ce-107">Planned work</span></span>

<span data-ttu-id="dc3ce-108">このため、2 種類の価格設定ディメンション値を使用できます :</span><span class="sxs-lookup"><span data-stu-id="dc3ce-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="dc3ce-109">**オプション セット** : 一連の値の固定リストであるディメンション。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="dc3ce-110">**エンティティに基づく値** : 様々な値のセットとなるディメンション。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="dc3ce-111">価格ディメンション</span><span class="sxs-lookup"><span data-stu-id="dc3ce-111">Pricing dimensions</span></span>

<span data-ttu-id="dc3ce-112">Dynamics 365 Project Operations には、価格ディメンションの既定セットが付属しています。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="dc3ce-113">これらの価格設定ディメンション表示するには、 **プロジェクト サービス** > **パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="dc3ce-114">パラメーター レコードの **金額ベースの価格ディメンション** タブで、ロール **msdyn_resourcecategory** と リソース組織単位 **msdyn_organizationalunit** のフィールド **営業に適用可能** と **コストに適用可能** が **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="dc3ce-115">これらのフィールドを有効化することで、各ロールや組織単位の組み合わせの価格とコストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![強調表示された 「営業に適用可能」 の Project Service パラメーターのスクリーンショット](media/PS-OOB-parameters.png)

<span data-ttu-id="dc3ce-117">追加の属性を使用してリソースの価格やコストを設定する必要がある場合は、カスタマイズしたフィールド、エンティティおよびディメンションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="dc3ce-118">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="dc3ce-119">この手順は一覧に表示された順序で完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="dc3ce-120">カスタム価格ディメンションのソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="dc3ce-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="dc3ce-121">カスタム フィールドとエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="dc3ce-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="dc3ce-122">カスタム フィールドを価格設定およびトランザクション エンティティに追加する</span><span class="sxs-lookup"><span data-stu-id="dc3ce-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="dc3ce-123">価格ディメンションとしてカスタム フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="dc3ce-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="dc3ce-124">プラグインの属性を更新して新しい価格ディメンションを含める</span><span class="sxs-lookup"><span data-stu-id="dc3ce-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="dc3ce-125">人的リソース時間の価格設定</span><span class="sxs-lookup"><span data-stu-id="dc3ce-125">Pricing human resource time</span></span>
<span data-ttu-id="dc3ce-126">組織が人的リソース時間をどのように価格設定するかは、多くの場合、組織の収益性に直接影響する重要な戦略的考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="dc3ce-127">組織が人的リソース時間の請求レートとコスト レートの設定方法を決定する準備ができたら、財務チームおよび実務担当者と連携します。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="dc3ce-128">価格設定に関する他の検討事項には、現在価格ディメンションではないが組織の価格ディメンションとして適用されるフィールドまたはエンティティを再利用するかどうかがあります。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="dc3ce-129">**トランザクション カテゴリ** (**msdyn_transactioncategory**) と **予約可能リソース** (**bookableresource**) のようなフィールドが候補のディメンションの例です。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="dc3ce-130">価格ディメンションをテーブルにするかオプション セットにするかを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="dc3ce-131">10または12を超えるディメンション値の変更が予測され、これらの値の追加の属性が必要な場合は、オプション セットではなくエンティティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="dc3ce-132">ほとんどのユーザーは、テーブルに新しい行を追加できますが、値の追加または削除などのオプション セットを管理するには、管理者または開発者が必要です。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="dc3ce-133">次の例にリソースが属するロールやリソースの組織単位に基づいて設定される請求レートを示します。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="dc3ce-134">通常、コスト レートは従業員の給与範囲および所属する組織単位に基づきます。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="dc3ce-135">この例では、請求レートとコストレートのテーブルは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="dc3ce-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="dc3ce-136">**サンプル請求レート**</span><span class="sxs-lookup"><span data-stu-id="dc3ce-136">**Sample bill rates**</span></span>

| <span data-ttu-id="dc3ce-137">ロール</span><span class="sxs-lookup"><span data-stu-id="dc3ce-137">Role</span></span>        | <span data-ttu-id="dc3ce-138">組織単位</span><span class="sxs-lookup"><span data-stu-id="dc3ce-138">Org Unit</span></span>    |<span data-ttu-id="dc3ce-139">出荷単位</span><span class="sxs-lookup"><span data-stu-id="dc3ce-139">Unit</span></span>      |<span data-ttu-id="dc3ce-140">価格</span><span class="sxs-lookup"><span data-stu-id="dc3ce-140">Price</span></span>      |<span data-ttu-id="dc3ce-141">[通貨]</span><span class="sxs-lookup"><span data-stu-id="dc3ce-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="dc3ce-142">開発者</span><span class="sxs-lookup"><span data-stu-id="dc3ce-142">Developer</span></span>   | <span data-ttu-id="dc3ce-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="dc3ce-143">Contoso US</span></span>  |<span data-ttu-id="dc3ce-144">Hour</span><span class="sxs-lookup"><span data-stu-id="dc3ce-144">Hour</span></span> | <span data-ttu-id="dc3ce-145">200</span><span class="sxs-lookup"><span data-stu-id="dc3ce-145">200</span></span>|<span data-ttu-id="dc3ce-146">USD</span><span class="sxs-lookup"><span data-stu-id="dc3ce-146">USD</span></span>     |
| <span data-ttu-id="dc3ce-147">開発者</span><span class="sxs-lookup"><span data-stu-id="dc3ce-147">Developer</span></span>   | <span data-ttu-id="dc3ce-148">Contoso India社</span><span class="sxs-lookup"><span data-stu-id="dc3ce-148">Contoso India</span></span> |<span data-ttu-id="dc3ce-149">Hour</span><span class="sxs-lookup"><span data-stu-id="dc3ce-149">Hour</span></span>|   <span data-ttu-id="dc3ce-150">112</span><span class="sxs-lookup"><span data-stu-id="dc3ce-150">112</span></span>|<span data-ttu-id="dc3ce-151">USD</span><span class="sxs-lookup"><span data-stu-id="dc3ce-151">USD</span></span>     |


<span data-ttu-id="dc3ce-152">**サンプル コスト レート**</span><span class="sxs-lookup"><span data-stu-id="dc3ce-152">**Sample cost rates**</span></span>

| <span data-ttu-id="dc3ce-153">給与範囲</span><span class="sxs-lookup"><span data-stu-id="dc3ce-153">Salary Band</span></span>     | <span data-ttu-id="dc3ce-154">組織単位</span><span class="sxs-lookup"><span data-stu-id="dc3ce-154">Org Unit</span></span>    |<span data-ttu-id="dc3ce-155">出荷単位</span><span class="sxs-lookup"><span data-stu-id="dc3ce-155">Unit</span></span>      |<span data-ttu-id="dc3ce-156">価格</span><span class="sxs-lookup"><span data-stu-id="dc3ce-156">Price</span></span>      |<span data-ttu-id="dc3ce-157">[通貨]</span><span class="sxs-lookup"><span data-stu-id="dc3ce-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="dc3ce-158">自分の会社_Band1</span><span class="sxs-lookup"><span data-stu-id="dc3ce-158">My company_Band1</span></span> | <span data-ttu-id="dc3ce-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="dc3ce-159">Contoso US</span></span>  |<span data-ttu-id="dc3ce-160">Hour</span><span class="sxs-lookup"><span data-stu-id="dc3ce-160">Hour</span></span> | <span data-ttu-id="dc3ce-161">145</span><span class="sxs-lookup"><span data-stu-id="dc3ce-161">145</span></span>|<span data-ttu-id="dc3ce-162">USD</span><span class="sxs-lookup"><span data-stu-id="dc3ce-162">USD</span></span>     |
| <span data-ttu-id="dc3ce-163">自分の会社_Band2</span><span class="sxs-lookup"><span data-stu-id="dc3ce-163">My company_Band2</span></span> | <span data-ttu-id="dc3ce-164">Contoso India社</span><span class="sxs-lookup"><span data-stu-id="dc3ce-164">Contoso India</span></span> |<span data-ttu-id="dc3ce-165">Hour</span><span class="sxs-lookup"><span data-stu-id="dc3ce-165">Hour</span></span>|   <span data-ttu-id="dc3ce-166">67</span><span class="sxs-lookup"><span data-stu-id="dc3ce-166">67</span></span>|<span data-ttu-id="dc3ce-167">USD</span><span class="sxs-lookup"><span data-stu-id="dc3ce-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]