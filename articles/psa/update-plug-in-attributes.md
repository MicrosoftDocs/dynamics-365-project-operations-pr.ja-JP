---
title: プラグインの属性を更新して新しい価格ディメンションを含める
description: このトピックでは、価格ディメンションのプラグイン属性の更新について説明します。
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121854"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="3380c-103">プラグインの属性を更新して新しい価格ディメンションを含める</span><span class="sxs-lookup"><span data-stu-id="3380c-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="3380c-104">Project Service Automation (PSA) の見積もりおよび契約機能を使用していない場合、このトピックはスキップできます。</span><span class="sxs-lookup"><span data-stu-id="3380c-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="3380c-105">このトピックでは、ユーザーが次のトピックの手順を完了していることを前提としています。[カスタム フィールドおよびエンティティを作成する](create-custom-fields-entities.md)、[価格設定とトランザクション エンティティにカスタム フィールドを追加する](field-references.md)、[カスタム フィールドを価格ディメンションとしてセットアップする](set-up-pricing-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="3380c-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="3380c-106">次に、これらの手順を完了していない場合は、戻ってこれらを完了してから、このトピックに戻ってください。</span><span class="sxs-lookup"><span data-stu-id="3380c-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="3380c-107">プロジェクト見積依頼明細用に見積依頼明細行の詳細を **見積依頼明細行** のページで作成するとき、システムがバックグラウンドで 2 つの見積もり明細行を作成します -- 1 つは見積もりコスト側用で、もう 1 つは営業側用の明細行です。</span><span class="sxs-lookup"><span data-stu-id="3380c-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="3380c-108">これは、プロジェクト契約品目の場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="3380c-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3380c-109">数量への変更を行うとき、またはコスト側のフィールドを変更するとき、変更が営業側に伝播されます。</span><span class="sxs-lookup"><span data-stu-id="3380c-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="3380c-110">これは、可能です。次のプラグインでは、価格ディメンションに対する変更を行った後、再登録する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="3380c-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="3380c-111">PreOperationContractLineDetailUpdate - 更新 **msdyn_orderlinetransaction**。</span><span class="sxs-lookup"><span data-stu-id="3380c-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="3380c-112">PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**。</span><span class="sxs-lookup"><span data-stu-id="3380c-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="3380c-113">次の手順では、プラグインの登録に関して説明します。</span><span class="sxs-lookup"><span data-stu-id="3380c-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="3380c-114">**PluginRegistrationTool** 開いて、オンライン インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="3380c-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="3380c-115">**検索** をクリックし、更新するプラグインを検索します。</span><span class="sxs-lookup"><span data-stu-id="3380c-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![検索ツリーのスクリーンショット](media/PRT-1.png)

3. <span data-ttu-id="3380c-117">プラグインが見つかったらそれを選択し、**メイン フォームの選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3380c-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="3380c-118">更新すべきプラグインのステップを選んで右クリックし、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3380c-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![更新するプラグインのスクリーンショット](media/PRT-2.png)
 
5. <span data-ttu-id="3380c-120">[更新] ウィンドウで、フィルター属性の省略記号 (**...**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3380c-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![既存のステップ構成情報を更新するときのスクリーンショット](media/PRT-3.png)
 
6. <span data-ttu-id="3380c-122">価格属性チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3380c-122">Select the pricing attribute check boxes.</span></span>

 ![価格属性のチェック ボックスの選択が表示されたスクリーン ショット](media/PRT-4.png)

7. <span data-ttu-id="3380c-124">**OK** をクリックして ページを閉じ、 **ステップの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3380c-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![「手順の更新」 ボタンを示すスクリーン ショット](media/PRT-5.png)
 
8. <span data-ttu-id="3380c-126">この第 2 プラグイン、 **PreOperationQuoteLineDetail - msdyn_quotelinetransaction の更新** のプロセスを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3380c-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="3380c-127">プラグイン登録ツールを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3380c-127">Close the plug-in registration tool.</span></span>

