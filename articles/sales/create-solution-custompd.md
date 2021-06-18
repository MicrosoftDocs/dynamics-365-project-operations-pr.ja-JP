---
title: カスタム価格ディメンションのソリューションを作成する
description: このトピックでは、カスタム価格ディメンションに対するソリューションの作成方法を説明します。
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010342"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="d4178-103">カスタム価格ディメンションのソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="d4178-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="d4178-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d4178-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="d4178-105">すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4178-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="d4178-106">この重要なベスト プラクティスは、必要に応じて変更を更新や削除する柔軟性を実現し、作業の再利用に役立ち、変更を他のインスタンスに簡単に移植可能にします。</span><span class="sxs-lookup"><span data-stu-id="d4178-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="d4178-107">必要な変更を加えたら、このソリューションを **マネージド型** ソリューションとしてエクスポートし、他のインスタンスにインポートして再利用します。</span><span class="sxs-lookup"><span data-stu-id="d4178-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="d4178-108">カスタム価格ディメンションのソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="d4178-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="d4178-109">**設定** > **ソリューション** を選択し、次に **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4178-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="d4178-110">ソリューションに *<your organization name> 価格ディメンション* と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d4178-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="d4178-111">その他の必要情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4178-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![カスタム価格ディメンション ソリューションを作成する](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d4178-113">価格設定ディメンション ソリューションにすべての必須エンティティと、関連するコンポーネントを追加する</span><span class="sxs-lookup"><span data-stu-id="d4178-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="d4178-114">次の Project Service エンティティを価格ソリューションに追加して、この価格ソリューションで重要なスキーマの変更を行います。</span><span class="sxs-lookup"><span data-stu-id="d4178-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="d4178-115">この手順を完了すると、エンティティが新しい価格ディメンションを認識します。</span><span class="sxs-lookup"><span data-stu-id="d4178-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="d4178-116">**設定** > **ソリューション** を順に選択してから **<*組織名*> 価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4178-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="d4178-117">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4178-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="d4178-118">**ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:</span><span class="sxs-lookup"><span data-stu-id="d4178-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="d4178-119">**実績**</span><span class="sxs-lookup"><span data-stu-id="d4178-119">**Actual**</span></span>
   - <span data-ttu-id="d4178-120">**予約可能リソース**</span><span class="sxs-lookup"><span data-stu-id="d4178-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="d4178-121">**見積行**</span><span class="sxs-lookup"><span data-stu-id="d4178-121">**Estimate Line**</span></span>
   - <span data-ttu-id="d4178-122">**プロジェクト タスク**</span><span class="sxs-lookup"><span data-stu-id="d4178-122">**Project Task**</span></span>
   - <span data-ttu-id="d4178-123">**請求明細行の詳細**</span><span class="sxs-lookup"><span data-stu-id="d4178-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="d4178-124">**仕訳帳明細行**</span><span class="sxs-lookup"><span data-stu-id="d4178-124">**Journal Line**</span></span>
   - <span data-ttu-id="d4178-125">**プロジェクト契約品目の詳細**</span><span class="sxs-lookup"><span data-stu-id="d4178-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="d4178-126">**プロジェクト チーム メンバー**</span><span class="sxs-lookup"><span data-stu-id="d4178-126">**Project Team Member**</span></span>
   - <span data-ttu-id="d4178-127">**見積依頼明細行の詳細**</span><span class="sxs-lookup"><span data-stu-id="d4178-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="d4178-128">**ロール価格利幅**</span><span class="sxs-lookup"><span data-stu-id="d4178-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="d4178-129">**ロール価格**</span><span class="sxs-lookup"><span data-stu-id="d4178-129">**Role Price**</span></span>
   - <span data-ttu-id="d4178-130">**時間入力**</span><span class="sxs-lookup"><span data-stu-id="d4178-130">**Time Entry**</span></span>
 
   ![既存のエンティティのカスタム価格ディメンション ソリューションを追加する](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="d4178-132">各エンティティについて、追加するコンポーネントと各エンティティに対するエンティティ資産の最終一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="d4178-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="d4178-133">選択した各エンティティに対してフォームとビューをすべて含めます。</span><span class="sxs-lookup"><span data-stu-id="d4178-133">Include all forms and views for each of the selected entities.</span></span>

  ![追加したエンティティ](./media/solution-component-selection.png)


5.  <span data-ttu-id="d4178-135">選択したエンティティに依存エンティティを含めるようプロンプトが表示されたら **いいえ、必須コンポーネントを含めません** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4178-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![依存エンティティを含める](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]