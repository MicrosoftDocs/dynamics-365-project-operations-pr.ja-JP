---
title: 製品
description: このトピックでは、提供する製品と価格についての情報を顧客に提供する製品カタログについて説明します。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 44f85982aa5c8e32ccde0dc32c3c9cd4339c4552
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011242"
---
# <a name="products"></a><span data-ttu-id="66a0a-103">製品</span><span class="sxs-lookup"><span data-stu-id="66a0a-103">Products</span></span>

<span data-ttu-id="66a0a-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="66a0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="66a0a-105">製品はビジネスの重要要素です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-105">Products are the backbone of your business.</span></span> <span data-ttu-id="66a0a-106">Dynamics 365 Sales Professional の製品カタログは、製品情報を価格情報の集合体です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-106">The product catalog in Dynamics 365 Sales Professional is a collection of products and pricing information.</span></span> <span data-ttu-id="66a0a-107">製品カタログを迅速に作成することで、営業チームの売り上げ増加に貢献します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-107">Make it easier for your sales reps to increase their sales by creating a product catalog quickly.</span></span>

## <a name="add-a-product"></a><span data-ttu-id="66a0a-108">製品を追加する</span><span class="sxs-lookup"><span data-stu-id="66a0a-108">Add a product</span></span>

1.  <span data-ttu-id="66a0a-109">Dynamics 365 Sales Professional に製品を登録するには、営業マネージャー プロフェッショナルまたはシステム管理者権限が必要となります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-109">Make sure you have the Sales Manager Professional or a System Administrator role so you can add products in Dynamics 365 Sales Professional.</span></span>
2.  <span data-ttu-id="66a0a-110">サイトマップ にて **設定** 配下の **製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-110">In the site map, under **Setup**, select **Products**.</span></span>
3.  <span data-ttu-id="66a0a-111">**製品を追加** を選択し、以下の情報を入力します :</span><span class="sxs-lookup"><span data-stu-id="66a0a-111">Select **Add Product** and fill in the following information:</span></span>

    -  <span data-ttu-id="66a0a-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="66a0a-112">**Name**</span></span>
    -  <span data-ttu-id="66a0a-113">**製品 ID**</span><span class="sxs-lookup"><span data-stu-id="66a0a-113">**Product ID**</span></span>
    -  <span data-ttu-id="66a0a-114">**親** : 製品に対して上位の製品ファミリを選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-114">**Parent**: Select a parent product family for the product.</span></span> <span data-ttu-id="66a0a-115">製品ファミリ内に下位製品を作成する場合、上位製品ファミリの名前がここに設定されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-115">If you're creating a child product in a product family, the name of the parent product family is populated here.</span></span> <span data-ttu-id="66a0a-116">これは、レコードの保存後は変更できません。</span><span class="sxs-lookup"><span data-stu-id="66a0a-116">This can't be changed after the record is saved.</span></span>
    -  <span data-ttu-id="66a0a-117">**有効開始日**/**有効終了日**: **有効開始日** と **有効終了日** を選択して製品の有効期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-117">**Valid From**/**Valid To**: Define the period the product is valid for by selecting a **Valid From** and **Valid To** date.</span></span>
    -  <span data-ttu-id="66a0a-118">**出荷単位一覧**: 出荷単位一覧を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-118">**Unit Group**: Select a unit group.</span></span> <span data-ttu-id="66a0a-119">出荷単位一覧は、製品が販売される種々の単位の集合で、個々の品目を大きな量にグループ化する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-119">A unit group is a collection of various units a product is sold in and defines how individual items are grouped into larger quantities.</span></span> <span data-ttu-id="66a0a-120">たとえば、製品として種を追加する場合は、既に「種」という単位グループが作成されており、標準出荷単位が「袋」と設定されている想定です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-120">For example, if you're adding seeds as a product, you might have created a unit group called "Seeds" and defined its primary unit as "packet."</span></span>
    -  <span data-ttu-id="66a0a-121">**既定の出荷単位**: 製品が販売される、最も一般的な出荷単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-121">**Default Unit**: Select the most common unit in which the product will be sold.</span></span> <span data-ttu-id="66a0a-122">出荷単位は、その製品を販売する数量または寸法です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-122">Units are the quantities or measurements that you sell your products in.</span></span> <span data-ttu-id="66a0a-123">たとえば、製品として種を追加する場合は、袋、箱やパレット単位で販売できます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-123">For example, if you're adding seeds as a product, you can sell it in packets, boxes, or pallets.</span></span> <span data-ttu-id="66a0a-124">これらは製品の出荷単位になります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-124">Each of these becomes a unit of the product.</span></span> <span data-ttu-id="66a0a-125">種が主にパケットで販売される場合、パケットを出荷単位として選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-125">If seeds are mostly sold in packets, select that as the unit.</span></span>
    -  <span data-ttu-id="66a0a-126">**既定の価格表**: 新しい製品の場合、このフィールドは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-126">**Default Price List**: If this is a new product, this field is read-only.</span></span> <span data-ttu-id="66a0a-127">既定の価格リストを選択する前に、必須項目への入力をすべて完了し、保存している必要があります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-127">Before you can select a default price list, you must complete all the required fields and then save the record.</span></span> <span data-ttu-id="66a0a-128">既定の価格表は必須でありませんが、製品レコードを保存した後で、各製品に既定の価格表を設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="66a0a-128">Although the default price list is not required, after you save the product record, it is a good idea to set a default price list for each product.</span></span> <span data-ttu-id="66a0a-129">顧客情報に価格リストが含まれていない場合、営業は既定の価格リストを使用して、見積もり、注文、インボイスを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-129">Then, if a customer record does not contain a price list, Sales can use the default price list for generating quotes, orders, and invoices.</span></span>
    -  <span data-ttu-id="66a0a-130">**小数点以下の桁数**: 0 から 5 までの整数を入力します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-130">**Decimals Supported**: Enter a whole number between 0 and 5.</span></span> <span data-ttu-id="66a0a-131">製品を半端な数量に分割できない場合は、0 を入力します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-131">If the product can't be divided into fractional quantities, enter 0.</span></span> <span data-ttu-id="66a0a-132">製品に価格リストが関連付けられていない場合、見積、注文、インボイスの製品情報の **数量** フィールドの精度は、このフィールドの値に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-132">The precision of the **Quantity** field in the quote, order, or invoice product record is validated against the value in this field if the product does not have an associated price list.</span></span>
    -  <span data-ttu-id="66a0a-133">**情報カテゴリ**: この製品に情報カテゴリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-133">**Subject**: Associate this product with a subject.</span></span> <span data-ttu-id="66a0a-134">情報カテゴリを使用すると、製品の分類とレポートのフィルター処理が行えます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-134">You can use subjects to categorize your products and to filter reports.</span></span>

4.  <span data-ttu-id="66a0a-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-135">Select **Save**.</span></span>
5.  <span data-ttu-id="66a0a-136">**詳細情報** タブに移動し、 **価格リストの品目** セクションにて、 **その他のコマンド** アイコンを選択し、 **新規価格リストの品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-136">On the **Additional Details** tab, in the **Price List Items** section, select **More commands**, and then select **Add New Price List Item**.</span></span>
7.  <span data-ttu-id="66a0a-137">**詳細情報** タブに移動し、 **製品の関連性** セクションにて、 **その他のコマンド** アイコンを選択し、 **製品の関連性を追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-137">On the **Additional Details** tab, in the **Product Relationship** section, select the **More commands** icon, and then select **Add New Product Relationship.**</span></span>
8.  <span data-ttu-id="66a0a-138">**新しい製品の関連性** フォームにて、以下の詳細情報を入力し、コマンド バーの **保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-138">In the **New Product Relationship** form, enter the following details, and on the command bar, select **Save and Close**:</span></span>

    -   <span data-ttu-id="66a0a-139">**関連製品** : 作業中の既存の製品レコードに対し、関連製品として追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-139">**Related Product**: Select a product that you want to add as a related product to the existing product record you're working on.</span></span>
    -   <span data-ttu-id="66a0a-140">**営業関連タイプ** : 製品をアップセル、クロスセル、アクセサリー、代替製品として追加するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-140">**Sales Relation Type**: Select whether you want to add the product as an up-sell, cross-sell, accessory, or substitute product.</span></span>
    -   <span data-ttu-id="66a0a-141">**方向性** : 製品間の関係性を一方向性にするか、双方向性にするかを選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-141">**Direction**:Select whether the relationship between the products will be unidirectional or bidirectional.</span></span> <span data-ttu-id="66a0a-142">一方向を選択した場合、 **関連する製品** にて指定した製品が既存の製品への推奨として表示されますが、未指定の製品の場合は推奨が表示されません。</span><span class="sxs-lookup"><span data-stu-id="66a0a-142">When you select unidirectional, the product that you select in **Related Product** will be shown as a recommendation for the existing product but not vice versa.</span></span>

9.  <span data-ttu-id="66a0a-143">製品フォームにて、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-143">On the Product form, select **Save**.</span></span>

## <a name="import-products"></a><span data-ttu-id="66a0a-144">製品のインポート</span><span class="sxs-lookup"><span data-stu-id="66a0a-144">Import products</span></span>

<span data-ttu-id="66a0a-145">インポートのテンプレートを使用することで、Dynamics 365 Sales に大量の製品データをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-145">You can use import templates to bring bulk product data into Dynamics 365 Sales.</span></span>

## <a name="revise-a-product"></a><span data-ttu-id="66a0a-146">製品を変更する</span><span class="sxs-lookup"><span data-stu-id="66a0a-146">Revise a product</span></span>

<span data-ttu-id="66a0a-147">必要に応じて製品プロパティを迅速に更新することで、製品在庫情報を最新に保ち、情報を更新することで販売代理店が最新の在庫変更を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-147">Keep the product inventory updated by quickly revising properties for the products, as required, and republishing the information so that your sales agents can see the latest changes to the inventory.</span></span>

1.  <span data-ttu-id="66a0a-148">システム管理者、システム カスタマイザー、営業課長、営業担当副社長、マーケティング担当副社長、最高経営責任者のいずれかのセキュリティ ロール、または同等のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-148">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="66a0a-149">サイト マップで **製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-149">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="66a0a-150">変更を行いたい有効な製品を開き、コマンドバーにて **修正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-150">Open an active product that you want to change, and on the command bar, select **Revise**.</span></span>
4.  <span data-ttu-id="66a0a-151">**変更の確認** ダイアログ ボックスで、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-151">In the **Confirm Revise** dialog box, select **Confirm**.</span></span> <span data-ttu-id="66a0a-152">これにより製品の状態が **改訂中** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-152">This will change the product status to **Under Revision**.</span></span>
5.  <span data-ttu-id="66a0a-153">変更が完了したら、コマンドバー上の **公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-153">After you're done making changes, on the command bar, select **Publish**.</span></span>

    > [!TIP]
    > <span data-ttu-id="66a0a-154">変更した内容を戻し、その製品の最終有効版を使う場合は、 **復元** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-154">To revert the changes and continue with the last active version of the product, select **Revert**.</span></span> <span data-ttu-id="66a0a-155">これにより製品の状態は **アクティブ** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-155">This changes the status of the product back to **Active**.</span></span>

## <a name="clone-a-product"></a><span data-ttu-id="66a0a-156">製品の複製</span><span class="sxs-lookup"><span data-stu-id="66a0a-156">Clone a product</span></span> 

<span data-ttu-id="66a0a-157">新たに製品を作成する場合は、既存の製品を複製することで効率化を図ることができます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-157">When you're creating a new product, save time by cloning an existing one.</span></span> <span data-ttu-id="66a0a-158">これにより、名前と ID 以外の詳細すべてを含む元のレコードのコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-158">This creates a copy of the original record with all the details except for the name and ID.</span></span>

1.  <span data-ttu-id="66a0a-159">システム管理者、システム カスタマイザー、営業課長、営業担当副社長、マーケティング担当副社長、最高経営責任者のいずれかのセキュリティ ロール、または同等のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-159">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="66a0a-160">サイト マップで **製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-160">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="66a0a-161">複製を行いたい製品情報を開き、コマンドバーにて **複製** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-161">Select a product record that you want to clone, and on the command bar, select **Clone**.</span></span> <span data-ttu-id="66a0a-162">確認ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-162">A confirmation dialog box appears.</span></span>
4.  <span data-ttu-id="66a0a-163">**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-163">Select **Confirm**.</span></span>

<span data-ttu-id="66a0a-164">製品の名称とID以外は、複製元の製品と同じ情報を持つ新規の製品情報が開きます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-164">A new product record opens with the same details as the original one except for the name and ID.</span></span>

## <a name="retire-a-product"></a><span data-ttu-id="66a0a-165">製品を廃止する</span><span class="sxs-lookup"><span data-stu-id="66a0a-165">Retire a product</span></span> 

<span data-ttu-id="66a0a-166">組織がある製品の販売を停止する場合、その製品を廃止して、営業代理店がその製品を使用できないようにします。</span><span class="sxs-lookup"><span data-stu-id="66a0a-166">If your organization doesn't sell a product anymore, retire it so that the product is no longer available to your sales agents.</span></span>

1.  <span data-ttu-id="66a0a-167">Sales Professional マネージャー または システム管理者などの権限が必要となります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-167">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="66a0a-168">サイト マップで **製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-168">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="66a0a-169">廃止を行う有効な製品を開き、コマンドバーにて **廃止** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-169">Open an active product that you want to retire, and on the command bar, select **Retire**.</span></span>
4.  <span data-ttu-id="66a0a-170">**廃止の確認** ダイアログ ボックスで、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-170">In the **Confirm Retire** dialog box, select **Confirm**.</span></span>


## <a name="delete-a-product"></a><span data-ttu-id="66a0a-171">製品の削除</span><span class="sxs-lookup"><span data-stu-id="66a0a-171">Delete a product</span></span>

<span data-ttu-id="66a0a-172">製品の販売を停止するため、削除します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-172">To stop selling a product, delete it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66a0a-173">削除されたレコードは復元することができません。</span><span class="sxs-lookup"><span data-stu-id="66a0a-173">You can't recover a deleted record.</span></span>

1.  <span data-ttu-id="66a0a-174">Sales Professional マネージャー または システム管理者などの権限が必要となります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-174">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="66a0a-175">サイト マップで **製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-175">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="66a0a-176">削除を行いたい製品情報を開き、コマンドバーにて **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-176">Select a product record you want to delete, and on the command bar, select **Delete**.</span></span>
4.  <span data-ttu-id="66a0a-177">**削除の確認** ダイアログ ボックスで、 **続ける** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66a0a-177">In the **Confirm Deletion** dialog box, select **Continue**.</span></span>
 
 ## <a name="quantity-factors-for-products"></a><span data-ttu-id="66a0a-178">製品の数量係数</span><span class="sxs-lookup"><span data-stu-id="66a0a-178">Quantity factors for products</span></span>

<span data-ttu-id="66a0a-179">数量係数を使用して、サブスクリプション ベースの製品の販売をサポートします。</span><span class="sxs-lookup"><span data-stu-id="66a0a-179">Quantity factors support the sale of subscription-based products.</span></span> <span data-ttu-id="66a0a-180">サブスクリプション ベース製品の場合、見積またはプロジェクト契約品目の数量はユーザー月数で表されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-180">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="66a0a-181">通常は、サブスクリプション ソフトウェア の価格は、ユーザーごとの月額として、カタログに保存されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-181">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="66a0a-182">ただし、代わりに別の時間の説明を使用できます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-182">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="66a0a-183">営業プロセスの間、見積依頼明細行の価格は通常、IT 販売代理店が交渉および割引した、ユーザーごと、月ごとの価格です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-183">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="66a0a-184">各取引には、異なる数のユーザーと異なる数のサブスクリプション月があります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-184">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="66a0a-185">見積依頼明細行の金額の計算に使用される数量は、ユーザーの数とサブスクリプション月数の積です。</span><span class="sxs-lookup"><span data-stu-id="66a0a-185">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="66a0a-186">数量係数は、製品の属性に依存します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-186">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="66a0a-187">製品の特定のプロパティを設定すると、それらのプロパティのサブセット、またはすべてのプロパティに数量係数としてフラグを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-187">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="66a0a-188">数値データ型を持つ数値プロパティ、または製品プロパティのみが、数量係数としてフラグ付けされていることがシステムによって検証されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-188">The system validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="66a0a-189">数量係数が設定されている製品が見積依頼明細行に追加されると、見積依頼明細行の **数量** フィールドは、読み取り専用フィールドになります。</span><span class="sxs-lookup"><span data-stu-id="66a0a-189">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="66a0a-190">数量係数である製品プロパティの値を入力すると、見積明細行の数量を計します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-190">After you enter values for product properties that are quantity factors, the quantity of the quote line is calculated.</span></span>

<span data-ttu-id="66a0a-191">たとえば、以下のプロパティがあるとします :</span><span class="sxs-lookup"><span data-stu-id="66a0a-191">For example, if there are the following properties:</span></span> 

- <span data-ttu-id="66a0a-192">**ユーザー数** : ユーザー数</span><span class="sxs-lookup"><span data-stu-id="66a0a-192">**No of users**: The number of users</span></span> 
- <span data-ttu-id="66a0a-193">**月数** : サブスクリプションの月数</span><span class="sxs-lookup"><span data-stu-id="66a0a-193">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="66a0a-194">**製品 SKU**</span><span class="sxs-lookup"><span data-stu-id="66a0a-194">**Product SKU**</span></span> 

<span data-ttu-id="66a0a-195">製品品目のプロパティを編集することにより、 **ユーザー数** と **月数** プロパティに数量係数としてフラグを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-195">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]