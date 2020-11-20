---
title: プロジェクト契約のプロジェクト価格表を管理する
description: このトピックは、プロジェクト契約のプロジェクト価格表の管理について説明します。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133375"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="36d96-103">プロジェクト契約のプロジェクト価格表を管理する</span><span class="sxs-lookup"><span data-stu-id="36d96-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="36d96-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="36d96-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="36d96-105">Dynamics 365 Project Operations のプロジェクト契約は、契約の複数の日付有効営業価格表に対応するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="36d96-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="36d96-106">プロジェクト オペレーションには、**プロジェクト価格表** と呼ばれる新たな関連エンティティがあります。</span><span class="sxs-lookup"><span data-stu-id="36d96-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="36d96-107">このエンティティは、プロジェクト契約と 1 対多の関係にあります。</span><span class="sxs-lookup"><span data-stu-id="36d96-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="36d96-108">プロジェクト価格表は、プロジェクトの時間と経費のトランザクションの価格設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="36d96-109">契約に 1 つ以上のプロジェクト価格表がある場合、これらの価格表は、契約品目を通じて契約に関連付けられているプロジェクトの時間と費用の見積もりと実際の価格設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="36d96-110">プロジェクト契約にプロジェクト価格表がない場合、プロジェクト価格表がないことを示す警告メッセージが表示され、見積もり、実際のプロジェクト作業、費用などの価格設定はされません。</span><span class="sxs-lookup"><span data-stu-id="36d96-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="36d96-111">販売価格の価格はありません。</span><span class="sxs-lookup"><span data-stu-id="36d96-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="36d96-112">プロジェクト契約のプロジェクト価格表の関連付け、または関連付けの解除</span><span class="sxs-lookup"><span data-stu-id="36d96-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="36d96-113">プロジェクトベースの仕事と経費の見積もりに使用する具体的な価格表を作成、または関連付ける</span><span class="sxs-lookup"><span data-stu-id="36d96-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="36d96-114">プロジェクト契約を開き、**プロジェクト価格表** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="36d96-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="36d96-115">サブグリッドで、**+新しいプロジェクトの価格表を追加する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d96-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="36d96-116">**クイック作成** スライダーで、価格表を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d96-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="36d96-117">ドロップダウン リストには、コンテキストが **営業** に設定されているすべての価格リストが表示され、価格表の通貨が契約上の通貨と一致します。</span><span class="sxs-lookup"><span data-stu-id="36d96-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="36d96-118">プロジェクト価格表の関連付けに対する説明を入力し、**保存** を選択して、**簡易作成** スライダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="36d96-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="36d96-119">プロジェクト価格表の関連付けが作成されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="36d96-120">手順 1 から 4 を繰り返して、複数のプロジェクト価格表をプロジェクト契約に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="36d96-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="36d96-121">関連するプロジェクト価格表のそれぞれで日付の有効性が異なる場合にのみ、複数のプロジェクト価格表を作成してください。</span><span class="sxs-lookup"><span data-stu-id="36d96-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="36d96-122">Project Operations では、プロジェクト価格表の日付の有効性の重複に対応していません。</span><span class="sxs-lookup"><span data-stu-id="36d96-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="36d96-123">特定の日付のトランザクションに複数のプロジェクト価格リストがある場合、そのトランザクションの価格は既定でゼロになります。</span><span class="sxs-lookup"><span data-stu-id="36d96-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="36d96-124">プロジェクト価格表の関連付けを削除する</span><span class="sxs-lookup"><span data-stu-id="36d96-124">Remove a project price list association</span></span>

- <span data-ttu-id="36d96-125">プロジェクトの価格表を選択してから、サブグリッド上の **契約プロジェクトの価格表を削除する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d96-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="36d96-126">価格表は、契約のプロジェクト価格表から削除されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="36d96-127">この場合、価格表自体が削除されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="36d96-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="36d96-128">契約に対する関連付けのみが削除されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="36d96-129">契約のプロジェクト価格表を自動で既定とする設定</span><span class="sxs-lookup"><span data-stu-id="36d96-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="36d96-130">プロジェクト価格表を、プロジェクト契約の既定のリストとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="36d96-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="36d96-131">この設定により、組織内のすべての契約が常にその価格期間の標準の価格表で開始されるようになります。</span><span class="sxs-lookup"><span data-stu-id="36d96-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="36d96-132">プロジェクト価格表の組織が既定で使用する価格表を設定する</span><span class="sxs-lookup"><span data-stu-id="36d96-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="36d96-133">**設定** > **全般** に移動し、**パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d96-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="36d96-134">**アクティブ パラメータ** リスト ページで、レコードを選択してダブルクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="36d96-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="36d96-135">ダブル クリックをする際は、ハイパーリンクのフィールド値をクリックしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="36d96-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="36d96-136">**アクティブ パラメータ** ページで、**価格表** タブを選択します。サブグリッドには、既定の価格表の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="36d96-137">これは、標準原価と販売価格表の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="36d96-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="36d96-138">販売するすべての通貨の **営業** 価格リストをここに関連付けておくことで、この通貨で取引する顧客に向けて作成したすべての契約で、販売価格表が既定になります。</span><span class="sxs-lookup"><span data-stu-id="36d96-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="36d96-139">顧客固有のプロジェクト価格表を作成する</span><span class="sxs-lookup"><span data-stu-id="36d96-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="36d96-140">また、顧客と価格設定の契約を交渉する際に、顧客固有のプロジェクト価格表を設定することも可能です。</span><span class="sxs-lookup"><span data-stu-id="36d96-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="36d96-141">**営業** > **顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="36d96-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="36d96-142">アクティブな取引先企業のリストから、特別な価格表のある顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="36d96-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="36d96-143">顧客レコードを選択して開き、**プロジェクト価格リスト** タブを選択します。サブグリッドには、この顧客に固有のプロジェクト価格リストのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="36d96-144">ここで新たな価格表の関連付けを作成して、この顧客に固有のプロジェクト価格表を作成します。</span><span class="sxs-lookup"><span data-stu-id="36d96-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="36d96-145">プロジェクト契約のカスタム価格</span><span class="sxs-lookup"><span data-stu-id="36d96-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="36d96-146">組織および顧客固有の既定のプロジェクト価格表を作成すると、これらのプロジェクト価格表の関連付けを使用してプロジェクト契約が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="36d96-147">ただし、プロジェクト契約のプロジェクト価格表は、常に日付と契約名が付記された状態でコピーされます。</span><span class="sxs-lookup"><span data-stu-id="36d96-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="36d96-148">アカウント マネージャーとプロジェクト マネージャーは、これらのコピーの価格の編集を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="36d96-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="36d96-149">これらの変更は、このプロジェクト契約にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="36d96-149">These changed prices will be applicable to this project contract only.</span></span>
