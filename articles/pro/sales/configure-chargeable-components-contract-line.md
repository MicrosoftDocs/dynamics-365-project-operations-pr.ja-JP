---
title: プロジェクトベースの契約品目の請求可能コンポーネントを構成する
description: このトピックでは、Project Operations の契約品目に課金コンポーネントを追加する方法ついて解説します。
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003727"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="d311d-103">プロジェクトベースの契約品目の請求可能コンポーネントを構成する</span><span class="sxs-lookup"><span data-stu-id="d311d-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="d311d-104">_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d311d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d311d-105">プロジェクト ベースの契約品目には、*付属型* コンポーネントと *課金型* コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d311d-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="d311d-106">付属型コンポーネントは、以下の対象となるコンポーネントです :</span><span class="sxs-lookup"><span data-stu-id="d311d-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="d311d-107">請求方法と顧客の分割</span><span class="sxs-lookup"><span data-stu-id="d311d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="d311d-108">上限</span><span class="sxs-lookup"><span data-stu-id="d311d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="d311d-109">プロジェクトベースの契約品目で定義された請求書の発行の頻度設定</span><span class="sxs-lookup"><span data-stu-id="d311d-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="d311d-110">付属型コンポーネントのサブセットは、**請求タイプ** フィールドを使用して課金型としてマークですることができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="d311d-111">**請求タイプ** フィールドは、契約品目のコンテキストで次の値を許可するオプションセットです :</span><span class="sxs-lookup"><span data-stu-id="d311d-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="d311d-112">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-112">Chargeable</span></span>
  - <span data-ttu-id="d311d-113">請求不可</span><span class="sxs-lookup"><span data-stu-id="d311d-113">Non-chargeable</span></span>

<span data-ttu-id="d311d-114">課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="d311d-115">課金対象は、プロジェクト契約品目のタスクで定義され、品目に含まれるすべてのトランザクション クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d311d-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="d311d-116">契約品目の **タスクを含める** フィールドが空白であるか、**プロジェクト全体** に設定されている場合は **課金型タスク** タブを使用できません。</span><span class="sxs-lookup"><span data-stu-id="d311d-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="d311d-117">プロジェクト契約品目のロールで定義された課金対象は、**時間** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d311d-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="d311d-118">契約品目の **時間を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**課金型ロール** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="d311d-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="d311d-119">プロジェクト契約品目のトランザクション カテゴリで定義された課金対象は、**経費** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d311d-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="d311d-120">**経費を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**課金型カテゴリ** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="d311d-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d311d-121">プロジェクト タスクを課金対象または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="d311d-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="d311d-122">プロジェクト タスクは、特定の契約品目で課金/非課金にすることができます。これにより、次の設定が可能になります: </span><span class="sxs-lookup"><span data-stu-id="d311d-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="d311d-123">プロジェクト ベースの契約品目に **時間** と特定のタスクが含まれる場合、、**T1** が課金として関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="d311d-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="d311d-124">**経費** を含む 2 つ目の契約品目がある場合は、契約品目の T1 タスクを非課金として関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="d311d-125">その結果、タスクに記録されたすべての時間は課金対象となり、すべての経費は課金対象外になります。</span><span class="sxs-lookup"><span data-stu-id="d311d-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="d311d-126">タスクの課金タイプは、契約品目タスク サブグリッドの **課金タイプ** フィールドを更新することで、契約品目の **課金タスク** タブで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="d311d-127">または、タスクに関連付けられた契約品目を表示するプロジェクトのタスクの課金設定のサブグリッドの **課金タイプ** フィールドを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d311d-128">ロールを課金対象または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="d311d-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="d311d-129">ロールは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d311d-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="d311d-130">ロールの請求タイプは、契約品目の **課金対象ロール** タブで構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="d311d-131">これを行うには、**課金対象の役割** サブグリッドの **課金タイプ** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="d311d-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d311d-132">トランザクション カテゴリを課金対象、または非課金対象として更新する</span><span class="sxs-lookup"><span data-stu-id="d311d-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="d311d-133">トランザクション カテゴリは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d311d-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="d311d-134">トランザクションの請求タイプは、プロジェクトベースの契約品目の **課金対象カテゴリ** タブで構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d311d-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="d311d-135">これを行うには、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="d311d-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="d311d-136">課金対象の解決</span><span class="sxs-lookup"><span data-stu-id="d311d-136">Resolve chargeability</span></span>

<span data-ttu-id="d311d-137">時間に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d311d-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="d311d-138">**時間** が契約品目に含まれている。</span><span class="sxs-lookup"><span data-stu-id="d311d-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="d311d-139">**役割** が契約品目で請求可能と構成されている。</span><span class="sxs-lookup"><span data-stu-id="d311d-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="d311d-140">**含まれるタスク** が、契約品目で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="d311d-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="d311d-141">これらの 3 つの条件が当てはまる場合、タスクは請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="d311d-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="d311d-142">経費に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d311d-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="d311d-143">**経費** が契約品目に含まれている</span><span class="sxs-lookup"><span data-stu-id="d311d-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="d311d-144">**トランザクション カテゴリ** が、契約品目で請求可能と構成されている</span><span class="sxs-lookup"><span data-stu-id="d311d-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="d311d-145">**含まれるタスク** が、契約品目で **選択したタスク** に設定されている</span><span class="sxs-lookup"><span data-stu-id="d311d-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="d311d-146">これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="d311d-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="d311d-147">材料に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d311d-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="d311d-148">**材料** が契約品目に含まれている</span><span class="sxs-lookup"><span data-stu-id="d311d-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="d311d-149">**含まれるタスク** が、契約品目で **選択したタスク** に設定されている</span><span class="sxs-lookup"><span data-stu-id="d311d-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="d311d-150">これらの 2 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="d311d-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-151">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d311d-152">
                    <strong>経費を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d311d-153">
                    <strong>材料を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="d311d-154">
                    <strong>含まれるタスク</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-155">
                    <strong>ロール</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-156">
                    <strong>カテゴリ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-157">
                    <strong>タスク​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="d311d-158">
                    <strong>請求可否</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-159">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-160">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-161">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-162">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-163">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-164">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-165">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-166">実績時間に基づく請求: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-167">経費の実績に基づく請求タイプ: <strong>課金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-168">材料実績の請求タイプ: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-169">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-170">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-171">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-172">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d311d-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-173">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-174">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-175">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-176">実績時間に基づく請求: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-177">経費の実績に基づく請求タイプ: <strong>課金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-178">材料実績の請求タイプ: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-179">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-180">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-181">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-182">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d311d-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-183">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-184">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-185">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-186">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-187">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="d311d-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d311d-188">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-189">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-190">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-191">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-192">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d311d-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-193">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-194">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-195">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-196">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-197">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-198">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-199">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-200">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-201">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-202">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d311d-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-203">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-204">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-205">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-206">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-207">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-208">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-209">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-210">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-211">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-212">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d311d-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-213">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-214">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-215">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-216">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-217">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-218">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-219">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-220">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-221">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-222">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-223">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-224">
                    <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-225">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-226">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-227">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="d311d-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d311d-228">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-229">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-230">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-231">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-232">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-233">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-234">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-235">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-236">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-237">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-238">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-239">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d311d-240">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-241">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-242">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-243">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-244">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-245">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-246">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="d311d-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d311d-247">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-248">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-249">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d311d-250">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d311d-251">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-252">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-253">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-254">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-255">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-256">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-257">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-258">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-259">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-260">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d311d-261">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-262">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-263">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-264">請求可能</span><span class="sxs-lookup"><span data-stu-id="d311d-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-265">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-266">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="d311d-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d311d-267">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="d311d-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d311d-268">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d311d-269">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d311d-270">有効</span><span class="sxs-lookup"><span data-stu-id="d311d-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d311d-271">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d311d-272">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="d311d-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d311d-273">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d311d-274">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d311d-275">設定できません</span><span class="sxs-lookup"><span data-stu-id="d311d-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d311d-276">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-277">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d311d-278">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d311d-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
