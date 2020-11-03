---
title: プロジェクト カレンダーの定義
description: このトピックでは、プロジェクト カレンダーを使用してプロジェクトのスケジュールを追跡する方法について説明します。
author: ruhercul
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079442"
---
# <a name="define-project-calendars"></a><span data-ttu-id="9513f-103">プロジェクト カレンダーの定義</span><span class="sxs-lookup"><span data-stu-id="9513f-103">Define project calendars</span></span>

<span data-ttu-id="9513f-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="9513f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9513f-105">プロジェクト スケジュールを作成するには、1 日分に対応する作業時間数と休業日を定義するプロジェクト カレンダー テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="9513f-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="9513f-106">プロジェクトのカレンダー テンプレートを作成するには、プロジェクトの **カレンダー テンプレート** フィールドで、作業テンプレートを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="9513f-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="9513f-107">作業テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9513f-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="9513f-108">左側のナビゲーション ウィンドウで、 **リソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="9513f-109">**リソース** リスト ページで、ユーザー レコードを開き、 **作業時間を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9513f-110">ブラウザー ページでポップアップを許可していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9513f-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="9513f-111">これにより、そのリソースに設定された作業時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9513f-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="9513f-112">**月次ビュー** タブで、 **設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="9513f-113">次の 3 つのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9513f-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="9513f-114">新しい週単位のスケジュール</span><span class="sxs-lookup"><span data-stu-id="9513f-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="9513f-115">1 日の作業スケジュール</span><span class="sxs-lookup"><span data-stu-id="9513f-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="9513f-116">休暇</span><span class="sxs-lookup"><span data-stu-id="9513f-116">Time Off</span></span>

4. <span data-ttu-id="9513f-117">**新規週単位スケジュール** を選択し、このリソース スケジュールのオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="9513f-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="9513f-118">定期的な週単位のスケジュール、毎日の時間パラメーター、休業日の設定などを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9513f-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="9513f-119">日付の範囲を設定して、 **保存** を選択し、 **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="9513f-120">**リソース** リストページへ戻り、作業時間のために設定するリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="9513f-121">作業テンプレートを設定するには、 **カレンダーを次のとおり設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="9513f-122">**作業テンプレート** ダイアログ ボックスで、作業テンプレートの名前を入力し、 **適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9513f-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="9513f-123">ここで、プロジェクトのカレンダー テンプレートがある作業テンプレートを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9513f-123">You can now associate the work template with a project calendar template.</span></span>
