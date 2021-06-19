---
title: 期間タイプ
description: このトピックでは、売上見積もりに対する期間タイプを設定する方法について説明します。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013492"
---
# <a name="period-types"></a><span data-ttu-id="abc58-103">期間タイプ</span><span class="sxs-lookup"><span data-stu-id="abc58-103">Period types</span></span>

<span data-ttu-id="abc58-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="abc58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="abc58-105">期間タイプはプロジェクトの売上を見積もる頻度を定義します。</span><span class="sxs-lookup"><span data-stu-id="abc58-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="abc58-106">このトピックでは、売上見積もりに対する期間タイプを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="abc58-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="abc58-107">期間タイプを作成して操作する</span><span class="sxs-lookup"><span data-stu-id="abc58-107">Create and work with period types</span></span>
<span data-ttu-id="abc58-108">期間タイプの作成と操作には、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="abc58-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="abc58-109">Dynamics 365 Finance 環境で **プロジェクト管理と会計** > **設定** > **見積もり** > **期間タイプ** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="abc58-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="abc58-110">**新規** を選択して新しい期間タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="abc58-110">Select **New** to create new period type.</span></span> <span data-ttu-id="abc58-111">名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="abc58-111">Enter a name and description.</span></span>
3. <span data-ttu-id="abc58-112">**頻度** フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="abc58-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="abc58-113">**毎週**、**隔週**、**半月ごと**、**毎月**、**毎日**、**四半期ごと**、**毎年** を選択すると、このカレンダーを期間の生成に使用します。</span><span class="sxs-lookup"><span data-stu-id="abc58-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="abc58-114">**元帳期間** を選択すると、一般会計を構成する元帳期間を期間の生成に使用します。</span><span class="sxs-lookup"><span data-stu-id="abc58-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="abc58-115">**無制限** を選択した場合、カスタム期間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="abc58-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="abc58-116">期間タイプ レコードを選択してから **期間の生成** を選択して期間タイプの期間を作成します。</span><span class="sxs-lookup"><span data-stu-id="abc58-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="abc58-117">選択した期間頻度に基づいて、開始日や生成する期間の数を指定するオプションを利用できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="abc58-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="abc58-118">**期間** を選択して生成した期間を確認します。</span><span class="sxs-lookup"><span data-stu-id="abc58-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]