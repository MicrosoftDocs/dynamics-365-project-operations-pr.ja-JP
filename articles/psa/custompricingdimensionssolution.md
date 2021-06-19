---
title: 価格設定ディメンションのカスタム ソリューションを作成する
description: このトピックでは、カスタム価格設定ディメンションを作成するときにカスタム ソリューションを作成する方法について説明します。
author: Rumant
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
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012322"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="b8e55-103">価格設定ディメンションのカスタム ソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="b8e55-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="b8e55-104">すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8e55-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="b8e55-105">この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。</span><span class="sxs-lookup"><span data-stu-id="b8e55-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b8e55-106">必要な変更を行った後、このソリューションを **管理ソリューション** としてエクスポートし、別のインスタンスにインポートして価格設定を再利用します。</span><span class="sxs-lookup"><span data-stu-id="b8e55-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="b8e55-107">**設定** > **ソリューション** を選択し、次に **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8e55-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="b8e55-108">**\<your organization name> 価格設定ディメンション** ソリューションの名称を決定し、その他必要な情報を入力し、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8e55-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![価格設定ディメンションのカスタムソリューションを作成する](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="b8e55-110">価格設定ディメンション ソリューションにすべての必須エンティティと、関連するコンポーネントを追加する</span><span class="sxs-lookup"><span data-stu-id="b8e55-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="b8e55-111">価格設定ソリューションには、以下の Project Service エンティティを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8e55-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="b8e55-112">この手順を完了して、エンティティが新しい価格設定ディメンションを認識できるよう、価格設定ソリューションで重要なスキーマ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="b8e55-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="b8e55-113">**設定** > **ソリューション** を選択し、続いて **\<your organization name>価格ディメンション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8e55-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b8e55-114">ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8e55-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="b8e55-115">**ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:</span><span class="sxs-lookup"><span data-stu-id="b8e55-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="b8e55-116">実績</span><span class="sxs-lookup"><span data-stu-id="b8e55-116">Actual</span></span>
- <span data-ttu-id="b8e55-117">予約可能リソース</span><span class="sxs-lookup"><span data-stu-id="b8e55-117">Bookable Resource</span></span>
- <span data-ttu-id="b8e55-118">見積行</span><span class="sxs-lookup"><span data-stu-id="b8e55-118">Estimate Line</span></span>
- <span data-ttu-id="b8e55-119">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="b8e55-119">Project Task</span></span>
- <span data-ttu-id="b8e55-120">請求明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="b8e55-120">Invoice Line Detail</span></span>
- <span data-ttu-id="b8e55-121">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="b8e55-121">Journal Line</span></span>
- <span data-ttu-id="b8e55-122">プロジェクト契約品目の詳細</span><span class="sxs-lookup"><span data-stu-id="b8e55-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="b8e55-123">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="b8e55-123">Project Team Member</span></span>
- <span data-ttu-id="b8e55-124">見積依頼明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="b8e55-124">Quote Line Detail</span></span>
- <span data-ttu-id="b8e55-125">ロール価格利幅</span><span class="sxs-lookup"><span data-stu-id="b8e55-125">Role Price Markup</span></span>
- <span data-ttu-id="b8e55-126">ロール価格</span><span class="sxs-lookup"><span data-stu-id="b8e55-126">Role Price</span></span> 
- <span data-ttu-id="b8e55-127">時間入力</span><span class="sxs-lookup"><span data-stu-id="b8e55-127">Time Entry</span></span> 

> ![価格設定ディメンション ソリューションに既存のエンティティを追加します。](media/Existing-entities-to-PD-solution.png)

> ![ソリューション コンポーネントの選択](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="b8e55-130">選択した各エンティティのすべてのフォームとビューが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b8e55-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="b8e55-131">選択したエンティティの依存エンティティを含めるかどうかを確認するダイアログが表示された場合、**いいえ** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="b8e55-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![すべての関連コンポーネントを含めない](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]