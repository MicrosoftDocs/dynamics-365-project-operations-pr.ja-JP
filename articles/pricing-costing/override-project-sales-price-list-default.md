---
title: プロジェクト販売価格表の上書き
description: このトピックでは、カスタム価格表の作成について説明します。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130854"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="533a9-103">プロジェクト販売価格表の上書き</span><span class="sxs-lookup"><span data-stu-id="533a9-103">Override project sales price lists</span></span>

<span data-ttu-id="533a9-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="533a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="533a9-105">顧客固有のプロジェクト価格表</span><span class="sxs-lookup"><span data-stu-id="533a9-105">Customer-specific project price lists</span></span>

<span data-ttu-id="533a9-106">顧客固有の価格協定は、Dynamics 365 Project Operations の取引先企業レコードにプロジェクト価格表として設定できます。</span><span class="sxs-lookup"><span data-stu-id="533a9-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="533a9-107">顧客固有のプロジェクト価格表を設定するには、**営業** 領域で取引先企業レコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="533a9-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="533a9-108">**取引先企業** 一覧ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="533a9-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="533a9-109">顧客レコードを検索してダブルクリックし、**取引先企業** 詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="533a9-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="533a9-110">**プロジェクト価格表** タブで、\*\*+ 新しいプロジェクト価格表^^ を選択します。</span><span class="sxs-lookup"><span data-stu-id="533a9-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="533a9-111">**新しいプロジェクト価格表** ページで、ドロップダウンから価格表を選択します。</span><span class="sxs-lookup"><span data-stu-id="533a9-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="533a9-112">コンテキストが **営業** に設定され、その通貨がアカウントの通貨と一致する価格表のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="533a9-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="533a9-113">関連付けに名前を付け、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="533a9-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="533a9-114">顧客固有のプロジェクト価格表が作成されます。</span><span class="sxs-lookup"><span data-stu-id="533a9-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="533a9-115">この価格表は、見積もりまたはプロジェクト契約の作成日が価格表の有効日内にある場合には、この顧客用に作成されたプロジェクト見積もりまたは契約の既定のプロジェクト価格に使用されます。</span><span class="sxs-lookup"><span data-stu-id="533a9-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="533a9-116">プロジェクト見積もりのカスタム価格</span><span class="sxs-lookup"><span data-stu-id="533a9-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="533a9-117">プロジェクトの見積もりでは、顧客またはプロジェクト パラメータから既定値に設定された既定の標準価格表で始まるプロジェクト価格設定を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="533a9-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="533a9-118">特定の見積もりでプロジェクト関連の作業にカスタム価格が必要な場合は、関連するエンティティのプロジェクト価格表から取得できます。</span><span class="sxs-lookup"><span data-stu-id="533a9-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="533a9-119">見積もり固有のプロジェクト価格を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="533a9-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="533a9-120">プロジェクト見積もりを開き、**プロジェクト価格表** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="533a9-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="533a9-121">サブグリッドで、**カスタム価格の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="533a9-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="533a9-122">見積もりに添付されているすべてのプロジェクト価格表は、新しい価格表にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="533a9-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="533a9-123">新しい価格表の名前は、これらの価格表が作成された日時を示すスタンプが付いた見積もりの名前を反映しています。</span><span class="sxs-lookup"><span data-stu-id="533a9-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="533a9-124">これらの各価格表を使用して、労務 (ロール価格) と経費 (カテゴリ価格) の価格を更新できます。</span><span class="sxs-lookup"><span data-stu-id="533a9-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="533a9-125">これらの価格は、このプロジェクト見積もりにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="533a9-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="533a9-126">プロジェクト契約の価格表</span><span class="sxs-lookup"><span data-stu-id="533a9-126">Price lists on a project contract</span></span>

<span data-ttu-id="533a9-127">プロジェクト契約では、プロジェクトの価格設定は、契約名と作成日時を示すスタンプが名前に追加されたカスタム価格表として既定で設定されます。</span><span class="sxs-lookup"><span data-stu-id="533a9-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="533a9-128">これは、見積もりが成功したときに契約書が作成された場合でも、最初から契約書が作成された場合でも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="533a9-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="533a9-129">必要に応じて、カスタム価格表へのこの関連付けを削除し、代わりに標準価格表をプロジェクト契約に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="533a9-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="533a9-130">標準価格表を見積もりまたは契約のプロジェクト価格表に関連付けると、価格表の価格に加えられた変更は、価格表を使用するすべての見積もりおよび契約に影響します。</span><span class="sxs-lookup"><span data-stu-id="533a9-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
