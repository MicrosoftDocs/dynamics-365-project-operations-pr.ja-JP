---
title: 新しい価格ディメンションでプラグイン属性を更新する
description: このトピックでは、価格ディメンションのプラグイン属性の更新方法を説明します。
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274689"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="170af-103">新しい価格ディメンションでプラグイン属性を更新する</span><span class="sxs-lookup"><span data-stu-id="170af-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="170af-104">このトピックでは、価格ディメンションのプラグイン属性の更新方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="170af-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="170af-105">このトピックの対象は Dynamics 365 Project Operations の見積もりと契約の機能のみです。</span><span class="sxs-lookup"><span data-stu-id="170af-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="170af-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="170af-106">Prerequisites</span></span>
<span data-ttu-id="170af-107">このトピックの手順を完了する前に、以下のトピックの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="170af-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="170af-108">カスタム フィールドとエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="170af-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="170af-109">カスタム フィールドを価格設定およびトランザクション エンティティに追加する</span><span class="sxs-lookup"><span data-stu-id="170af-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="170af-110">[価格ディメンションとしてカスタム フィールドを設定します](set-up-custom-fields-pricing-dimensions.md)。</span><span class="sxs-lookup"><span data-stu-id="170af-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="170af-111">次に、これらの手順を完了していない場合は、完了後にこのトピックに戻ります。</span><span class="sxs-lookup"><span data-stu-id="170af-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="170af-112">プラグインの登録</span><span class="sxs-lookup"><span data-stu-id="170af-112">Register a plug-in</span></span>
<span data-ttu-id="170af-113">プロジェクト見積明細行の **見積依頼明細行** ページで見積依頼明細行詳細を作成すると、システムは見積明細行を 2 件作成します。</span><span class="sxs-lookup"><span data-stu-id="170af-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="170af-114">1 件は見積もりのコスト側で、もう 1 件は営業側です。</span><span class="sxs-lookup"><span data-stu-id="170af-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="170af-115">これは、プロジェクト契約品目の場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="170af-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="170af-116">数量への変更を行うとき、またはコスト側のフィールドを変更するとき、この変更が営業側に作成されます。</span><span class="sxs-lookup"><span data-stu-id="170af-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="170af-117">これが可能なのは、Quotelinedetail エンティティと契約品目詳細エンティティの PreOperation プラグインが、トランザクションでコスト側の特定属性が営業側に接続されているためです。</span><span class="sxs-lookup"><span data-stu-id="170af-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="170af-118">営業側の価格ディメンション値を変更し、コスト側でも変更する場合は、価格ディメンションの変更後に次のプラグインを再登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="170af-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="170af-119">これらは更新と再登録に使用するプラグインです。</span><span class="sxs-lookup"><span data-stu-id="170af-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="170af-120">PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction の更新**</span><span class="sxs-lookup"><span data-stu-id="170af-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="170af-121">PreOperationQuoteLineDetailUpdate - **msdyn_quotelinetransaction の更新**</span><span class="sxs-lookup"><span data-stu-id="170af-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="170af-122">プラグインの更新と再登録には、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="170af-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="170af-123">**PluginRegistrationTool** を開いて Project Operations の Dataverse 環境に接続します。</span><span class="sxs-lookup"><span data-stu-id="170af-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="170af-124">**検索** を選択して、更新するプラグイン名の最初の数文字を入力します。</span><span class="sxs-lookup"><span data-stu-id="170af-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="170af-125">プラグインが見つかったら選択し、**メイン フォームの選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="170af-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="170af-126">**Update msdyn_orderlinetransaction** ステップを選んで右クリックし、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="170af-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="170af-127">**更新** ダイアログ ページで、フィルタリング属性の省略記号 (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="170af-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="170af-128">フィルタリング属性ウィンドウが開き、エンティティが含むすべての属性と価格ディメンションの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="170af-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="170af-129">価格ディメンション属性のチェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="170af-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="170af-130">**OK** を選択してページを閉じ、**ステップの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="170af-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="170af-131">2 番目のプラグイン **PreOperationQuoteLineDetail** に対して手順 2 から 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="170af-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="170af-132">このプラグインでは **msdyn_quotelinetransaction の更新** ステップを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="170af-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="170af-133">**PluginRegistrationTool** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="170af-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]