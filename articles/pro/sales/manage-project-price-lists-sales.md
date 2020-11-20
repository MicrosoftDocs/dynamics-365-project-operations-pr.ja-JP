---
title: プロジェクト見積依頼のプロジェクト価格表を管理する (ライト)
description: このトピックでは、見積もりのプロジェクト価格表に関する作業について説明します。 (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175987"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a><span data-ttu-id="a9dad-104">プロジェクト見積依頼のプロジェクト価格表を管理する (ライト)</span><span class="sxs-lookup"><span data-stu-id="a9dad-104">Manage project price lists on project quotes - lite</span></span>

<span data-ttu-id="a9dad-105">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="a9dad-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a9dad-106">プロジェクト見積もりは、複数日有効な営業価格表をサポートするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="a9dad-106">Project quotes are designed to support multiple date effective sales price lists.</span></span> <span data-ttu-id="a9dad-107">Dynamics 365 Project Operations では、**プロジェクト価格表** という新しい関連付けエンティティが追加されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-107">With Dynamics 365 Project Operations, a new associated entity called **Project price lists** is added.</span></span> <span data-ttu-id="a9dad-108">このエンティティには、プロジェクト見積もりに対して一対多関連付けがあります。</span><span class="sxs-lookup"><span data-stu-id="a9dad-108">This entity has a 1-to-many relationship to a project quote.</span></span>

<span data-ttu-id="a9dad-109">プロジェクト価格表は、プロジェクトの時間と経費のトランザクションの価格設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-109">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="a9dad-110">見積もりに 1 つ以上のプロジェクト価格表がある場合、これらの価格表は、見積依頼明細行を通じて見積もりに関連付けられているプロジェクトの時間と経費の見積もりと実績の価格設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-110">When a quote has one or more project price lists, these price lists are used to price time and expense estimates and actuals on projects that are associated to the quote through the quote line.</span></span>

<span data-ttu-id="a9dad-111">プロジェクト見積もりにプロジェクト価格表がない場合は、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-111">When there are no project price lists on a project quote, you will receive a warning message.</span></span> <span data-ttu-id="a9dad-112">メッセージには、プロジェクト価格表がないため、プロジェクトの見積もりと実際の作業および経費の価格が設定されないことが表示されています。</span><span class="sxs-lookup"><span data-stu-id="a9dad-112">The message states that because there are no project price lists, your estimated and actual project work and expenses will not be priced.</span></span> <span data-ttu-id="a9dad-113">代わりに、販売額の価格はゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="a9dad-113">Instead, they will have zero (0) price for sales values.</span></span>

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a><span data-ttu-id="a9dad-114">プロジェクト見積もりでのプロジェクト価格表の関連付けまたは関連付け解除</span><span class="sxs-lookup"><span data-stu-id="a9dad-114">Associate or disassociate a project price list on a project quote</span></span>

<span data-ttu-id="a9dad-115">プロジェクトベースの作業と経費を見積もるための特定の価格表を作成または選択するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-115">To create or select a specific price list for estimating project-based work and expenses, complete the following steps.</span></span>

1. <span data-ttu-id="a9dad-116">見積もりで **プロジェクト価格** タブを選択し、サブグリッドで **+ 新しいプロジェクト価格表の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-116">On the quote, select the **Project Price** tab and in the subgrid, select **+ Add New Project Price List**.</span></span>
2. <span data-ttu-id="a9dad-117">簡易作成ページで、価格表を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-117">On the Quick Create page, select a price list.</span></span> <span data-ttu-id="a9dad-118">ドロップダウン リストには、コンテキストが **営業** に設定されているすべての価格表が表示され、通貨は見積もりの通貨と一致します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-118">The drop-down list shows all price lists that have the context set to **Sales** and the currency matches the currency on the quote.</span></span>
4. <span data-ttu-id="a9dad-119">プロジェクト価格表の関連付けの説明を入力し、**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-119">Enter a description for the project price list association and select **Save and Close**.</span></span>

<span data-ttu-id="a9dad-120">プロジェクト価格表の関連付けが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-120">A project price list association is created.</span></span>

<span data-ttu-id="a9dad-121">複数のプロジェクト価格表をプロジェクト見積もりに関連付ける必要がある場合は、このプロセスを繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-121">You can repeat this process if you need to associate more than one project price list to the project quote.</span></span> <span data-ttu-id="a9dad-122">関連するプロジェクト価格表ごとに有効日が異なる場合にのみ、複数のプロジェクト価格表を作成します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-122">Only create multiple project price lists if you have different effective dates on each of the associated project price lists.</span></span>

> [!NOTE]
> <span data-ttu-id="a9dad-123">Project Operations では、プロジェクト価格表の重複する日付の有効性はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a9dad-123">Project Operations does't support overlapping date effectivity of the project price lists.</span></span> <span data-ttu-id="a9dad-124">特定の日付のトランザクションに複数のプロジェクト価格表がある場合、そのトランザクションの価格は既定でゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="a9dad-124">If there are multiple project prices lists for a transaction with given date, the price on that transaction will be defaulted to zero (0).</span></span>
<span data-ttu-id="a9dad-125">プロジェクト価格表の関連付けを削除するには、プロジェクト価格表を選択してから、**見積もりプロジェクトの価格表を削除する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-125">To remove a project price list association, select the project price list and then select **Delete Quote Project Price List**.</span></span> <span data-ttu-id="a9dad-126">価格表は見積もりのプロジェクト価格表から削除されますが、価格表自体は削除されません。</span><span class="sxs-lookup"><span data-stu-id="a9dad-126">The price list is removed from the project price lists of the quote, but the price list itself is not deleted.</span></span> <span data-ttu-id="a9dad-127">見積もりへの関連付けのみが削除されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-127">Only the association to the quote is deleted.</span></span>

## <a name="set-up-default-project-price-lists-on-a-quote"></a><span data-ttu-id="a9dad-128">見積もりに既定のプロジェクト価格表を設定する</span><span class="sxs-lookup"><span data-stu-id="a9dad-128">Set up default project price lists on a quote</span></span>

<span data-ttu-id="a9dad-129">プロジェクト価格表は、プロジェクト見積もりで既定に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-129">Project price lists can be set up to default on a project quote.</span></span> <span data-ttu-id="a9dad-130">この設定により、組織内のすべての見積もりが常にその価格期間の標準価格表で始まることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-130">This setup ensures that all quotes in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-organizational-default-for-project-price-lists"></a><span data-ttu-id="a9dad-131">プロジェクト価格表に対して組織の既定を設定する</span><span class="sxs-lookup"><span data-stu-id="a9dad-131">Set up organizational default for project price lists</span></span>

1. <span data-ttu-id="a9dad-132">**設定** > **一般** > **パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-132">Go to **Settings** > **General** > **Parameters**.</span></span>
2. <span data-ttu-id="a9dad-133">**アクティブなパラメーター** リスト ページでレコードを検索し、ダブルクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-133">On the **Active Parameters** list page, locate the record and double-click to open it.</span></span> 
3. <span data-ttu-id="a9dad-134">**パラメーター** ページで、**価格表** タブを選択します。既定の価格表のリストを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-134">On the **Parameters** page, select the **Price List** tab. You can see the list of default price lists is shown.</span></span> <span data-ttu-id="a9dad-135">これは、標準コストと営業価格表のリストです。</span><span class="sxs-lookup"><span data-stu-id="a9dad-135">This is a list standard cost and sales price lists.</span></span> <span data-ttu-id="a9dad-136">販売するすべての通貨の営業価格表をここに関連付けると、この通貨でトランザクションする顧客に対して作成する見積もりで、この営業価格表が既定になります。</span><span class="sxs-lookup"><span data-stu-id="a9dad-136">Having a sales price list associated here for every currency that you sell in, will ensure that this sales price list is defaulted on any quote that you create for customers that transact in this currency.</span></span>

### <a name="set-up-customer-specific-project-price-lists"></a><span data-ttu-id="a9dad-137">顧客固有のプロジェクト価格表を設定する</span><span class="sxs-lookup"><span data-stu-id="a9dad-137">Set up customer-specific project price lists</span></span>

<span data-ttu-id="a9dad-138">顧客とマスター価格契約を交渉した場合、顧客固有のプロジェクト価格表を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-138">Customer-specific project price lists can also be set up when you have negotiated a master pricing agreement with your customers.</span></span>

<span data-ttu-id="a9dad-139">顧客固有のプロジェクト価格表を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-139">To set up a customer-specific project price list, complete the following steps.</span></span>

1. <span data-ttu-id="a9dad-140">**営業** 領域で **顧客** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-140">In the **Sales** area, select **Customers**.</span></span>
2. <span data-ttu-id="a9dad-141">アクティブなアカウントのリストで、特別価格表がある顧客レコードを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-141">In the list of your active accounts, select and open the customer record that you have special price list for.</span></span>
3. <span data-ttu-id="a9dad-142">に **プロジェクト価格表** タブで、新しい価格表の関連付けを作成して、この顧客に固有のプロジェクト価格表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-142">On the **Project Price Lists** tab, you can create a new price list association to have the project price list that is specific to this customer.</span></span>

## <a name="create-custom-pricing-on-a-project-quote"></a><span data-ttu-id="a9dad-143">プロジェクト見積もりにユーザー定義の価格を作成する</span><span class="sxs-lookup"><span data-stu-id="a9dad-143">Create custom pricing on a project quote</span></span>

<span data-ttu-id="a9dad-144">組織および顧客固有の既定のプロジェクト価格表を作成すると、これらのプロジェクト価格表の関連付けを使用してプロジェクト見積もりが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-144">After you have organizational and customer-specific default project price lists, your project quotes will automatically be created with these project price list associations.</span></span> <span data-ttu-id="a9dad-145">ただし、場合によっては、特定のプロジェクト見積もりに対してユーザー定義の価格を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dad-145">However, in certain cases, you may need to create custom pricing for a specific project quote.</span></span> 

1. <span data-ttu-id="a9dad-146">**プロジェクト見積もり** の **プロジェクト価格表** タブで、特定の価格表レコードがサブグリッドで選択されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-146">On the **Project Quote**, on the **Project Price List** tab, verify in the subgrid that no specific price list record is selected.</span></span>
2. <span data-ttu-id="a9dad-147">**ユーザー定義の価格** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dad-147">Select **Create Custom Pricing**.</span></span> <span data-ttu-id="a9dad-148">これにより、現在見積もりに関連付けられているすべての標準価格表のコピーが作成され、これらのコピーが見積もりに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-148">This will make copies of all the standard price lists currently associated to the quote and associate these copies to the quote.</span></span> <span data-ttu-id="a9dad-149">標準価格表への既存の関連付けは削除されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-149">The existing associations to standard price lists will be removed.</span></span> <span data-ttu-id="a9dad-150">その後、営業担当者はこれらのコピーの価格の編集を開始できます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-150">The salesperson can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="a9dad-151">これらの変更された価格は、このプロジェクト見積もりにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="a9dad-151">These changed prices will be applicable to this project quote only.</span></span>
