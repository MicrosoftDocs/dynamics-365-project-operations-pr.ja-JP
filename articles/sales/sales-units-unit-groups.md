---
title: 出荷単位および出荷単位一覧
description: このトピックでは、Dynamics 365 プロジェクト オペレーションでユニットとユニット グループを作成する方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079391"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="18d80-103">出荷単位および出荷単位一覧</span><span class="sxs-lookup"><span data-stu-id="18d80-103">Units and unit groups</span></span>

<span data-ttu-id="18d80-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="18d80-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="18d80-105">出荷単位とは、製品やサービスを販売する際の数量や単位です。</span><span class="sxs-lookup"><span data-stu-id="18d80-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="18d80-106">たとえば、園芸用品を販売する場合、種をパケット、箱、およびパレットの単位で販売することがあります。</span><span class="sxs-lookup"><span data-stu-id="18d80-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="18d80-107">出荷単位一覧は、このようにさまざまな出荷単位のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="18d80-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="18d80-108">このトピックの手順を完了するには、システム管理者、または Sales Professional マネージャーの役割が割り当てられているか、同等の権限を持っていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="18d80-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="18d80-109">出荷単位一覧の作成</span><span class="sxs-lookup"><span data-stu-id="18d80-109">Create a unit group</span></span>

1. <span data-ttu-id="18d80-110">サイトマップにて **単位** を選択します。</span><span class="sxs-lookup"><span data-stu-id="18d80-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="18d80-111">**新規** を選択し、 **出荷単位一覧の作成** ダイアログ ボックスに、単位の名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="18d80-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="18d80-112">**標準出荷単位** フィールドで、製品を販売する際の、共通測定単位の最小値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18d80-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="18d80-113">たとえば、「個」または「オンス」と入力します。</span><span class="sxs-lookup"><span data-stu-id="18d80-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="18d80-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="18d80-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="18d80-115">出荷単位一覧に単位を追加する</span><span class="sxs-lookup"><span data-stu-id="18d80-115">Add units to a unit group</span></span>

1. <span data-ttu-id="18d80-116">出荷単位一覧を開き、 **関連** タブの、 **単位** を選択します。</span><span class="sxs-lookup"><span data-stu-id="18d80-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="18d80-117">標準出荷単位が既に追加されていることが確認できます。</span><span class="sxs-lookup"><span data-stu-id="18d80-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="18d80-118">**新しい単位を追加** を選択し、 **クイック作成 : 単位** ページで、 **名前** フィールドに、単位の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="18d80-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="18d80-119">**数量** フィールドに、その単位が含有する数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="18d80-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="18d80-120">例えば、ひと箱あたりに2個収まるのであれば、「2」と入力します。</span><span class="sxs-lookup"><span data-stu-id="18d80-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="18d80-121">**基本単位** フィールドで、基本単位を選択し、単位の最小測定単位を設定します。</span><span class="sxs-lookup"><span data-stu-id="18d80-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="18d80-122">たとえば、「個」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18d80-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="18d80-123">**保存** を選択します :</span><span class="sxs-lookup"><span data-stu-id="18d80-123">Select **Save** :</span></span>
