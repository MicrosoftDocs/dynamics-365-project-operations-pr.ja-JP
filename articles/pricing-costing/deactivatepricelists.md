---
title: 価格表を非アクティブ化する
description: このトピックは、使用していないか古い価格表を非アクティブ化または削除する方法を説明しています。
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701946"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="d15a6-103">価格表を非アクティブ化する</span><span class="sxs-lookup"><span data-stu-id="d15a6-103">Deactivate price lists</span></span> 

<span data-ttu-id="d15a6-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d15a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d15a6-105">Dynamics 365 Project Operations から古いまたは使用していない価格表を削除するために実行するステップが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="d15a6-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="d15a6-106">特定のページから価格表を除去または削除します。</span><span class="sxs-lookup"><span data-stu-id="d15a6-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="d15a6-107">**価格表** ページで、アクティブな価格リストから価格リストを非アクティブ化または削除します。</span><span class="sxs-lookup"><span data-stu-id="d15a6-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="d15a6-108">価格表を完全に削除するには、両方の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d15a6-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="d15a6-109">[アクティブな価格リスト] ビューから価格リストを直接削除または非アクティブ化するステップ 2 を実行するだけでは不十分です。</span><span class="sxs-lookup"><span data-stu-id="d15a6-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="d15a6-110">また、ステップ 1 で説明したすべての場所から、この価格表の関連付けを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d15a6-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="d15a6-111">特定のページから価格表を削除します</span><span class="sxs-lookup"><span data-stu-id="d15a6-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="d15a6-112">Project Operations から価格表を削除するには、次のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="d15a6-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="d15a6-113">**プロジェクト パラメーター** ページ > **価格表** タブ</span><span class="sxs-lookup"><span data-stu-id="d15a6-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="d15a6-114">**組織単位** ページ > **価格表** グリッド</span><span class="sxs-lookup"><span data-stu-id="d15a6-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="d15a6-115">**アカウント** ページ > **プロジェクト価格表** グリッド</span><span class="sxs-lookup"><span data-stu-id="d15a6-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="d15a6-116">**プロジェクトの見積もり** ページ > **プロジェクト価格表** グリッド: これは、すべてのアクティブなプロジェクト見積もりに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d15a6-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="d15a6-117">**プロジェクト契約** ページ > **プロジェクト価格表** グリッド: これは、すべてのアクティブなプロジェクト契約に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d15a6-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="d15a6-118">ページごとに、削除する価格表を選択してから、**削除** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d15a6-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="d15a6-119">[価格表] ページで、価格リストを削除または非アクティブ化します</span><span class="sxs-lookup"><span data-stu-id="d15a6-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="d15a6-120">アクティブ価格表から価格表を削除するには、**販売** > **顧客** > **価格表** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d15a6-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="d15a6-121">削除する価格表を選択し、それから **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d15a6-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="d15a6-122">価格表が既存のトランザクションで参照されている場合、それを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="d15a6-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="d15a6-123">これが発生した場合は、価格表を非アクティブ化して、どのビューにも表示されないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d15a6-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="d15a6-124">価格表を非アクティブ化するには、価格表をもう一度選択してから、**非アクティブ化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d15a6-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
