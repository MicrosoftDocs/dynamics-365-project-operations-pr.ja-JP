---
title: 出荷単位一覧および出荷単位
description: このトピックでは、単位グループと単位に関する情報を提供します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 78f154856acf796f408491c5873cb29da8ac55bb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079284"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="040df-103">出荷単位一覧および出荷単位</span><span class="sxs-lookup"><span data-stu-id="040df-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="040df-104">単位グループと単位は Microsoft Dynamics 365 の基本エンティティです。</span><span class="sxs-lookup"><span data-stu-id="040df-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="040df-105">単位は単一の測定単位であり、複数の単位を単位グループにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="040df-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="040df-106">単位グループは Dynamics 365 のユーザー インターフェイス (UI) で単位スケジュールと呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="040df-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="040df-107">以下に単位と単位グループの例をいくつか示します:</span><span class="sxs-lookup"><span data-stu-id="040df-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="040df-108">**単位グループ** : 距離</span><span class="sxs-lookup"><span data-stu-id="040df-108">**Unit group** : Distance</span></span> 
    - <span data-ttu-id="040df-109">**単位** : マイルやキロメートルなど。</span><span class="sxs-lookup"><span data-stu-id="040df-109">**Units** : Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="040df-110">**単位グループ** : 時間</span><span class="sxs-lookup"><span data-stu-id="040df-110">**Unit group** : Time</span></span>
    - <span data-ttu-id="040df-111">**単位** : 時間、日、週など。</span><span class="sxs-lookup"><span data-stu-id="040df-111">**Units** : Hour, day, week, and so on.</span></span> 

<span data-ttu-id="040df-112">単位グループに複数の単位を設定する場合、単位グループの既定や標準単位として設定した最初の単位を指定して、単位間の変換係数も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="040df-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="040df-113">たとえば **時間** 単位グループで **時** を最初のユニットとして設定した場合、システムは **時** を既定単位として指定します。</span><span class="sxs-lookup"><span data-stu-id="040df-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="040df-114">次に設定する単位が **日** の場合、 **日** から **時** への変換係数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="040df-114">If the next unit that you set up is **Day** , you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="040df-115">次に、3 番目の単位として **週** を追加する場合、 **日** または **時** から **週** への変換係数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="040df-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="040df-116">次の図は、 **日** 単位の設定例を示しています。 **数量** フィールドに 1 日の時間数が表示され、 **週** には **数量** フィールドに 1 週間の日数が表示されています。</span><span class="sxs-lookup"><span data-stu-id="040df-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week** , where the **Quantity** field show the number of days that are in a week.</span></span>

> ![単位グループ: 情報ページ](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="040df-118">単位と単位グループの使用</span><span class="sxs-lookup"><span data-stu-id="040df-118">Using units and unit groups</span></span>

<span data-ttu-id="040df-119">Dynamics 365 Project Service Automation は単位と単位グループを使用して、経費と時間の両方の見積もりとエントリを処理します。</span><span class="sxs-lookup"><span data-stu-id="040df-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="040df-120">経費については、各経費カテゴリに既定の単位グループと単位があります。</span><span class="sxs-lookup"><span data-stu-id="040df-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="040df-121">これらの値は、経費カテゴリの価格表エントリに既定値として入力されます。</span><span class="sxs-lookup"><span data-stu-id="040df-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="040df-122">たとえば、 **マイレージ** という名前の経費カテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="040df-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="040df-123">これには **距離** という名前の単位グループと、 **マイル** という名前の既定単位があります。</span><span class="sxs-lookup"><span data-stu-id="040df-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="040df-124">**距離** 単位グループを 2 つの単位 ( **マイル** と **キロメートル** ) を持つように設定した場合、価格表の **マイレージ** カテゴリに 2 つの価格を設定できます: マイルあたりの価格と、キロメートルあたりの価格。</span><span class="sxs-lookup"><span data-stu-id="040df-124">If you set up the **Distance** unit group so that it has two units ( **Mile** and **Kilometer** ), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="040df-125">経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="040df-125">Expense category</span></span>  | <span data-ttu-id="040df-126">単位グループ</span><span class="sxs-lookup"><span data-stu-id="040df-126">Unit group</span></span>  | <span data-ttu-id="040df-127">出荷単位</span><span class="sxs-lookup"><span data-stu-id="040df-127">Unit</span></span>      | <span data-ttu-id="040df-128">価格設定方法</span><span class="sxs-lookup"><span data-stu-id="040df-128">Pricing method</span></span>  | <span data-ttu-id="040df-129">出荷単位ごとの価格</span><span class="sxs-lookup"><span data-stu-id="040df-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="040df-130">マイレージ</span><span class="sxs-lookup"><span data-stu-id="040df-130">Mileage</span></span>           | <span data-ttu-id="040df-131">距離</span><span class="sxs-lookup"><span data-stu-id="040df-131">Distance</span></span>      | <span data-ttu-id="040df-132">マイル</span><span class="sxs-lookup"><span data-stu-id="040df-132">Mile</span></span>      | <span data-ttu-id="040df-133">出荷単位ごとの価格</span><span class="sxs-lookup"><span data-stu-id="040df-133">Price per unit</span></span>    | <span data-ttu-id="040df-134">10 米国ドル</span><span class="sxs-lookup"><span data-stu-id="040df-134">10 USD</span></span>            |
| <span data-ttu-id="040df-135">マイレージ</span><span class="sxs-lookup"><span data-stu-id="040df-135">Mileage</span></span>           | <span data-ttu-id="040df-136">距離</span><span class="sxs-lookup"><span data-stu-id="040df-136">Distance</span></span>      | <span data-ttu-id="040df-137">キロメートル</span><span class="sxs-lookup"><span data-stu-id="040df-137">Kilometer</span></span> | <span data-ttu-id="040df-138">出荷単位ごとの価格</span><span class="sxs-lookup"><span data-stu-id="040df-138">Price per unit</span></span>    |  <span data-ttu-id="040df-139">6 米国ドル</span><span class="sxs-lookup"><span data-stu-id="040df-139">6 USD</span></span>            |

<span data-ttu-id="040df-140">プロジェクトに経費を入力すると、システムは経費のカテゴリと単位の組み合わせにより価格を決定します。</span><span class="sxs-lookup"><span data-stu-id="040df-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="040df-141">経費の説明</span><span class="sxs-lookup"><span data-stu-id="040df-141">Expense description</span></span>        | <span data-ttu-id="040df-142">経費カテゴリ</span><span class="sxs-lookup"><span data-stu-id="040df-142">Expense category</span></span>  | <span data-ttu-id="040df-143">出荷単位</span><span class="sxs-lookup"><span data-stu-id="040df-143">Unit</span></span>  | <span data-ttu-id="040df-144">数量</span><span class="sxs-lookup"><span data-stu-id="040df-144">Quantity</span></span>  | <span data-ttu-id="040df-145">単価</span><span class="sxs-lookup"><span data-stu-id="040df-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="040df-146">クライアントの場所への移動</span><span class="sxs-lookup"><span data-stu-id="040df-146">Drive to client location</span></span> | <span data-ttu-id="040df-147">マイレージ</span><span class="sxs-lookup"><span data-stu-id="040df-147">Mileage</span></span>             | <span data-ttu-id="040df-148">マイル</span><span class="sxs-lookup"><span data-stu-id="040df-148">Mile</span></span>  | <span data-ttu-id="040df-149">10</span><span class="sxs-lookup"><span data-stu-id="040df-149">10</span></span>        | <span data-ttu-id="040df-150">10 米国ドル</span><span class="sxs-lookup"><span data-stu-id="040df-150">10 USD</span></span>         |

<span data-ttu-id="040df-151">時間については、それぞれの価格表ヘッダーに **既定の時間単位** フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="040df-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="040df-152">この値は、価格表ヘッダーを作成するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="040df-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="040df-153">次にこの単位を使用して、その価格表にすべての役割ベースの価格を設定します。</span><span class="sxs-lookup"><span data-stu-id="040df-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="040df-154">**見積もり時間** フィールドの見積もり行は、任意の時間単位で表現できます。</span><span class="sxs-lookup"><span data-stu-id="040df-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="040df-155">ただし、プロジェクトの見積もり行とプロジェクトの時間エントリでは、 **時** の時間単位のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="040df-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="040df-156">時間エントリや見積もり行の単位がその役割の価格表行の単位と一致しない場合、システムはプロジェクト見積もりやプロジェクトの実際のトランザクションで定義されている単位に価格を変換します。</span><span class="sxs-lookup"><span data-stu-id="040df-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="040df-157">次の例は、PSA が単位グループ、単位、変換係数を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="040df-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="040df-158">[出荷単位]</span><span class="sxs-lookup"><span data-stu-id="040df-158">Units</span></span>

   - <span data-ttu-id="040df-159">**単位グループ** : 時間</span><span class="sxs-lookup"><span data-stu-id="040df-159">**Unit group** : Time</span></span> 
   - <span data-ttu-id="040df-160">**単位** : 時</span><span class="sxs-lookup"><span data-stu-id="040df-160">**Units** : Hour</span></span> 
    
    - <span data-ttu-id="040df-161">**日** - 換算係数: 8 時間</span><span class="sxs-lookup"><span data-stu-id="040df-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="040df-162">**週** - 換算係数: 40 時間</span><span class="sxs-lookup"><span data-stu-id="040df-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="040df-163">プロジェクト A の価格表設定:</span><span class="sxs-lookup"><span data-stu-id="040df-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="040df-164">**名前** : 英国の販売価格 2016 年</span><span class="sxs-lookup"><span data-stu-id="040df-164">**Name** : UK sales prices 2016</span></span> 
    - <span data-ttu-id="040df-165">**既定の時間単位** : 日</span><span class="sxs-lookup"><span data-stu-id="040df-165">**Default time unit** : Day</span></span> 
    - <span data-ttu-id="040df-166">**通貨** : GBP</span><span class="sxs-lookup"><span data-stu-id="040df-166">**Currency** : GBP</span></span>

| <span data-ttu-id="040df-167">ロール</span><span class="sxs-lookup"><span data-stu-id="040df-167">Role</span></span>      | <span data-ttu-id="040df-168">単位グループ</span><span class="sxs-lookup"><span data-stu-id="040df-168">Unit group</span></span> | <span data-ttu-id="040df-169">出荷単位</span><span class="sxs-lookup"><span data-stu-id="040df-169">Unit</span></span> | <span data-ttu-id="040df-170">組織単位</span><span class="sxs-lookup"><span data-stu-id="040df-170">Organizational unit</span></span> | <span data-ttu-id="040df-171">価格</span><span class="sxs-lookup"><span data-stu-id="040df-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="040df-172">開発者</span><span class="sxs-lookup"><span data-stu-id="040df-172">Developer</span></span> | <span data-ttu-id="040df-173">Time</span><span class="sxs-lookup"><span data-stu-id="040df-173">Time</span></span>       | <span data-ttu-id="040df-174">Day</span><span class="sxs-lookup"><span data-stu-id="040df-174">Day</span></span>  | <span data-ttu-id="040df-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="040df-175">Contoso UK</span></span>          | <span data-ttu-id="040df-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="040df-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="040df-177">時間エントリ</span><span class="sxs-lookup"><span data-stu-id="040df-177">Time entry</span></span>

<span data-ttu-id="040df-178">次の表は、3 時間のプロジェクトに対して PSA が作成した結果の販売側のトランザクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="040df-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="040df-179">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="040df-179">Project</span></span>   | <span data-ttu-id="040df-180">タスク</span><span class="sxs-lookup"><span data-stu-id="040df-180">Task</span></span>    | <span data-ttu-id="040df-181">ロール</span><span class="sxs-lookup"><span data-stu-id="040df-181">Role</span></span>      | <span data-ttu-id="040df-182">数量</span><span class="sxs-lookup"><span data-stu-id="040df-182">Quantity</span></span> | <span data-ttu-id="040df-183">出荷単位</span><span class="sxs-lookup"><span data-stu-id="040df-183">Unit</span></span>  | <span data-ttu-id="040df-184">単価</span><span class="sxs-lookup"><span data-stu-id="040df-184">Unit price</span></span> | <span data-ttu-id="040df-185">未請求の売上金額</span><span class="sxs-lookup"><span data-stu-id="040df-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="040df-186">プロジェクト A</span><span class="sxs-lookup"><span data-stu-id="040df-186">Project A</span></span> | <span data-ttu-id="040df-187">[設計]</span><span class="sxs-lookup"><span data-stu-id="040df-187">Design</span></span>  | <span data-ttu-id="040df-188">開発者</span><span class="sxs-lookup"><span data-stu-id="040df-188">Developer</span></span> | <span data-ttu-id="040df-189">3</span><span class="sxs-lookup"><span data-stu-id="040df-189">3</span></span>        | <span data-ttu-id="040df-190">Hour</span><span class="sxs-lookup"><span data-stu-id="040df-190">Hour</span></span>  | <span data-ttu-id="040df-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="040df-191">100 GBP</span></span>    | <span data-ttu-id="040df-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="040df-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="040df-193">時間単位に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="040df-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="040df-194">経費の場合、PSA は異なる単位に変換しますか。</span><span class="sxs-lookup"><span data-stu-id="040df-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="040df-195">番号</span><span class="sxs-lookup"><span data-stu-id="040df-195">No.</span></span> <span data-ttu-id="040df-196">単位の変換は時間に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="040df-196">Unit conversion works only for time.</span></span> <span data-ttu-id="040df-197">経費については、システムが経費カテゴリと単位の組み合わせで価格を見つけることができない場合、価格は既定で 0.00 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="040df-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="040df-198">PSA が時間の単位を変換するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="040df-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="040df-199">一部の国や地域では、請求レートを日単位で設定する法的要件があります。</span><span class="sxs-lookup"><span data-stu-id="040df-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="040df-200">見積もりサイクル中の価格交渉と割引は、各請求可能な役割の日率を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="040df-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="040df-201">スケジュールの見積もりと時間の入力は「時」単位で行われます。</span><span class="sxs-lookup"><span data-stu-id="040df-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="040df-202">「時」単位でこの違いをサポートするために、PSA は時間単位を変換します。</span><span class="sxs-lookup"><span data-stu-id="040df-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="040df-203">プロジェクトの見積もりで時間単位を変更できますか。</span><span class="sxs-lookup"><span data-stu-id="040df-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="040df-204">番号</span><span class="sxs-lookup"><span data-stu-id="040df-204">No.</span></span> <span data-ttu-id="040df-205">現在、スケジュールの見積もりは「時」に限定されており、変更できません。</span><span class="sxs-lookup"><span data-stu-id="040df-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="040df-206">単位と単位グループを編集、削除、追加できますか。</span><span class="sxs-lookup"><span data-stu-id="040df-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="040df-207">はい。</span><span class="sxs-lookup"><span data-stu-id="040df-207">Yes.</span></span> <span data-ttu-id="040df-208">**時間** 単位グループと **時** 単位を除き、すべての単位を削除や編集することが可能で、新しい単位を追加できます。</span><span class="sxs-lookup"><span data-stu-id="040df-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="040df-209">PSA で **時間** 単位グループと **時** 単位は削除できません。</span><span class="sxs-lookup"><span data-stu-id="040df-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="040df-210">ただし、 **名前** フィールドの翻訳されたテキストで更新できます。</span><span class="sxs-lookup"><span data-stu-id="040df-210">However, they can be updated with a translated text for the **Name** field.</span></span>
