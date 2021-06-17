---
title: 見積依頼明細行の請求可能コンポーネントを構成する
description: このトピックでは、プロジェクトベースの見積明細での課金対象コンポーネントと非課金対象コンポーネントの設定に関する情報を提供します。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003772"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="1b320-103">見積依頼明細行の請求可能コンポーネントを構成する</span><span class="sxs-lookup"><span data-stu-id="1b320-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="1b320-104">_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_</span><span class="sxs-lookup"><span data-stu-id="1b320-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1b320-105">プロジェクト ベースの見積品目には、*付属型* コンポーネントと *有料型* コンポーネントの概念があります。</span><span class="sxs-lookup"><span data-stu-id="1b320-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="1b320-106">含まれているコンポーネントは、次の対象となります :</span><span class="sxs-lookup"><span data-stu-id="1b320-106">Included components are subject to:</span></span>

  - <span data-ttu-id="1b320-107">請求方法と顧客の分割</span><span class="sxs-lookup"><span data-stu-id="1b320-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="1b320-108">上限</span><span class="sxs-lookup"><span data-stu-id="1b320-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="1b320-109">プロジェクト ベースの見積明細で定義された請求書の発行の頻度設定</span><span class="sxs-lookup"><span data-stu-id="1b320-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="1b320-110">付属型コンポーネントのサブセットは、**請求タイプ** フィールドを使用して課金型としてマークですることができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="1b320-111">**請求タイプ** フィールドは、見積明細のコンテキストで次の値を許可するオプションセットです :</span><span class="sxs-lookup"><span data-stu-id="1b320-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="1b320-112">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-112">Chargeable</span></span>
  - <span data-ttu-id="1b320-113">請求不可</span><span class="sxs-lookup"><span data-stu-id="1b320-113">Non-chargeable</span></span>

<span data-ttu-id="1b320-114">課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="1b320-115">課金対象は、見積明細のタスクで定義され、明細に含まれるすべてのトランザクション クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1b320-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="1b320-116">契約品目の **タスクを含める** フィールドが空白であるか、**プロジェクト全体** に設定されている場合は、**有料型タスク** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="1b320-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="1b320-117">プロジェクトの見積明細のロールで定義された課金対象は、**時間** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1b320-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="1b320-118">プロジェクトの見積明細の **時間を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**有料型ロール** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="1b320-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="1b320-119">見積品目のトランザクション カテゴリで定義された課金対象は、**経費** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1b320-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="1b320-120">プロジェクトの見積明細の **経費を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**有料型カテゴリ** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="1b320-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="1b320-121">プロジェクト タスクを課金対象または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="1b320-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="1b320-122">プロジェクト タスクは、特定のプロジェクトベースの見積明細で請求可/不可にすることができます。これにより、次の設定が可能になります。</span><span class="sxs-lookup"><span data-stu-id="1b320-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="1b320-123">プロジェクトベースの見積明細に **時間** とタスク **T1** が含まれている場合、タスクは課金対象として見積もり行に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="1b320-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="1b320-124">**経費** を含む 2 つ目の見積明細がある場合は、契約品目の **T1** タスクを非課金として関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="1b320-125">その結果、タスクに記録されたすべての時間は課金対象となり、経費に記録されているすべてのタスクは課金対象外になります。</span><span class="sxs-lookup"><span data-stu-id="1b320-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="1b320-126">タスクの課金タイプは、**見積もり品目タスク** サブグリッドの **課金タイプ** フィールドを更新することで、プロジェクト ベースの見積品目タブの **課金タスク** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="1b320-127">または、タスクに関連付けられた見積品目を表示するプロジェクトのタスクの課金設定のサブグリッドの **課金タイプ** フィールドで、プロジェクト タスクの課金タイプを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="1b320-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="1b320-128">ロールを課金対象、または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="1b320-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="1b320-129">ロールは、特定のプロジェクト ベースの見積明細のコンテキストによっては、課金または非課金にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="1b320-130">ロールの課金タイプは、**課金対象のロール** サブグリッドの **課金タイプ** フィールドを更新することで、プロジェクト ベースの見積品目タブの **課金タスク** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="1b320-131">トランザクション カテゴリを課金対象、または非課金対象として更新する</span><span class="sxs-lookup"><span data-stu-id="1b320-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="1b320-132">トランザクション カテゴリは、特定の見積明細では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1b320-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="1b320-133">トランザクションの課金タイプは、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドを更新することで、プロジェクト ベースの見積品目タブの **課金のカテゴリ** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1b320-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="1b320-134">課金対象の解決</span><span class="sxs-lookup"><span data-stu-id="1b320-134">Resolve chargeability</span></span>
<span data-ttu-id="1b320-135">時間に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1b320-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="1b320-136">**時間** が見積もり行に含まれている。</span><span class="sxs-lookup"><span data-stu-id="1b320-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="1b320-137">**役割** が見積もり行で請求可能と構成されている。</span><span class="sxs-lookup"><span data-stu-id="1b320-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="1b320-138">**含まれるタスク** が、見積もり行で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="1b320-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="1b320-139">これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="1b320-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="1b320-140">経費に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1b320-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="1b320-141">**経費** が、見積もり行に含まれている。</span><span class="sxs-lookup"><span data-stu-id="1b320-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="1b320-142">**トランザクション カテゴリ** が、見積もり行で請求可能と構成されている。</span><span class="sxs-lookup"><span data-stu-id="1b320-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="1b320-143">**含まれるタスク** が、見積もり行で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="1b320-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="1b320-144">これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="1b320-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="1b320-145">材料に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1b320-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="1b320-146">**材料** が、見積もり行に含まれている。</span><span class="sxs-lookup"><span data-stu-id="1b320-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="1b320-147">**含まれるタスク** が、見積もり行で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="1b320-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="1b320-148">これらの 2 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="1b320-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-149">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1b320-150">
                    <strong>経費を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1b320-151">
                    <strong>材料を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="1b320-152">
                    <strong>含まれるタスク</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-153">
                    <strong>ロール</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-154">
                    <strong>カテゴリ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-155">
                    <strong>タスク​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="1b320-156">
                    <strong>請求可否</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-157">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-158">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-159">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-160">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-161">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-162">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-163">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-164">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-165">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-166">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-167">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-168">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-169">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-170">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="1b320-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-171">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-172">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-173">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-174">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-175">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-176">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-177">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-178">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-179">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-180">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="1b320-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-181">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-182">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-183">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-184">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-185">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-186">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-187">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-188">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-189">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-190">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="1b320-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-191">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-192">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-193">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-194">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-195">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-196">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-197">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-198">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-199">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-200">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="1b320-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-201">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-202">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-203">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-204">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-205">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-206">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-207">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-208">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-209">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-210">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="1b320-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-211">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-212">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-213">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-214">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-215">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-216">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-217">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-218">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-219">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-220">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-221">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-222">
                    <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-223">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-224">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-225">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-226">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-227">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-228">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-229">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-230">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-231">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-232">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-233">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-234">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-235">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-236">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-237">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1b320-238">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-239">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-240">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-241">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-242">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-243">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-244">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-245">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-246">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-247">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1b320-248">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1b320-249">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-250">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-251">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-252">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-253">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-254">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-255">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-256">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-257">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-258">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1b320-259">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-260">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-261">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-262">請求可能</span><span class="sxs-lookup"><span data-stu-id="1b320-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-263">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-264">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-265">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="1b320-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1b320-266">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1b320-267">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1b320-268">有効</span><span class="sxs-lookup"><span data-stu-id="1b320-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1b320-269">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1b320-270">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="1b320-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1b320-271">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1b320-272">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1b320-273">設定不可</span><span class="sxs-lookup"><span data-stu-id="1b320-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1b320-274">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-275">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1b320-276">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1b320-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
