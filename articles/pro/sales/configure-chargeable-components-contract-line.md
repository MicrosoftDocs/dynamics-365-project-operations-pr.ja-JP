---
title: プロジェクトベースの契約品目の請求可能コンポーネントを構成する
description: このトピックでは、Project Operations の契約品目に課金コンポーネントを追加する方法ついて解説します。
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858479"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="7e133-103">プロジェクトベースの契約品目の請求可能コンポーネントを構成する</span><span class="sxs-lookup"><span data-stu-id="7e133-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="7e133-104">_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7e133-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e133-105">プロジェクト ベースの契約品目には、*付属型* コンポーネントと *課金型* コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7e133-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="7e133-106">付属型コンポーネントは、以下の対象となるコンポーネントです :</span><span class="sxs-lookup"><span data-stu-id="7e133-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="7e133-107">請求方法と顧客の分割</span><span class="sxs-lookup"><span data-stu-id="7e133-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="7e133-108">上限</span><span class="sxs-lookup"><span data-stu-id="7e133-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="7e133-109">プロジェクトベースの契約品目で定義された請求書の発行の頻度設定</span><span class="sxs-lookup"><span data-stu-id="7e133-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="7e133-110">付属型コンポーネントのサブセットは、**請求タイプ** フィールドを使用して課金型としてマークですることができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="7e133-111">**請求タイプ** フィールドは、契約品目のコンテキストで次の値を許可するオプションセットです :</span><span class="sxs-lookup"><span data-stu-id="7e133-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="7e133-112">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-112">Chargeable</span></span>
  - <span data-ttu-id="7e133-113">請求不可</span><span class="sxs-lookup"><span data-stu-id="7e133-113">Non-chargeable</span></span>

<span data-ttu-id="7e133-114">課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="7e133-115">課金対象は、プロジェクト契約品目のタスクで定義され、品目に含まれるすべてのトランザクション クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="7e133-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="7e133-116">契約品目の **タスクを含める** フィールドが空白であるか、**プロジェクト全体** に設定されている場合は **課金型タスク** タブを使用できません。</span><span class="sxs-lookup"><span data-stu-id="7e133-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="7e133-117">プロジェクト契約品目のロールで定義された課金対象は、**時間** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7e133-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="7e133-118">契約品目の **時間を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**課金型ロール** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7e133-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="7e133-119">プロジェクト契約品目のトランザクション カテゴリで定義された課金対象は、**経費** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7e133-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="7e133-120">**経費を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**課金型カテゴリ** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7e133-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7e133-121">プロジェクト タスクを課金対象または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="7e133-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="7e133-122">プロジェクト タスクは、特定の契約品目で課金/非課金にすることができます。これにより、次の設定が可能になります: </span><span class="sxs-lookup"><span data-stu-id="7e133-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="7e133-123">プロジェクト ベースの契約品目に **時間** と特定のタスクが含まれる場合、、**T1** が課金として関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="7e133-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="7e133-124">**経費** を含む 2 つ目の契約品目がある場合は、契約品目の T1 タスクを非課金として関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="7e133-125">その結果、タスクに記録されたすべての時間は課金対象となり、すべての経費は課金対象外になります。</span><span class="sxs-lookup"><span data-stu-id="7e133-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="7e133-126">タスクの課金タイプは、契約品目タスク サブグリッドの **課金タイプ** フィールドを更新することで、契約品目の **課金タスク** タブで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="7e133-127">または、タスクに関連付けられた契約品目を表示するプロジェクトのタスクの課金設定のサブグリッドの **課金タイプ** フィールドを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7e133-128">ロールを課金対象または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="7e133-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="7e133-129">ロールは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7e133-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="7e133-130">ロールの請求タイプは、契約品目の **課金対象ロール** タブで構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="7e133-131">これを行うには、**課金対象の役割** サブグリッドの **課金タイプ** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="7e133-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7e133-132">トランザクション カテゴリを課金対象、または非課金対象として更新する</span><span class="sxs-lookup"><span data-stu-id="7e133-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="7e133-133">トランザクション カテゴリは、特定の契約品目では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7e133-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="7e133-134">トランザクションの請求タイプは、プロジェクトベースの契約品目の **課金対象カテゴリ** タブで構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7e133-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="7e133-135">これを行うには、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="7e133-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="7e133-136">課金対象の解決</span><span class="sxs-lookup"><span data-stu-id="7e133-136">Resolve chargeability</span></span>

<span data-ttu-id="7e133-137">時間に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="7e133-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="7e133-138">**時間** が契約品目に含まれている。</span><span class="sxs-lookup"><span data-stu-id="7e133-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="7e133-139">**役割** が契約品目で請求可能と構成されている。</span><span class="sxs-lookup"><span data-stu-id="7e133-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="7e133-140">**含まれるタスク** が、契約品目で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="7e133-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="7e133-141">これらの 3 つの条件が当てはまる場合、タスクは請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="7e133-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="7e133-142">経費に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="7e133-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="7e133-143">**経費** が契約品目に含まれている</span><span class="sxs-lookup"><span data-stu-id="7e133-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="7e133-144">**トランザクション カテゴリ** が、契約品目で請求可能と構成されている</span><span class="sxs-lookup"><span data-stu-id="7e133-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="7e133-145">**含まれるタスク** が、契約品目で **選択したタスク** に設定されている</span><span class="sxs-lookup"><span data-stu-id="7e133-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="7e133-146">これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="7e133-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="7e133-147">材料に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="7e133-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="7e133-148">**材料** が契約品目に含まれている</span><span class="sxs-lookup"><span data-stu-id="7e133-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="7e133-149">**含まれるタスク** が、契約品目で **選択したタスク** に設定されている</span><span class="sxs-lookup"><span data-stu-id="7e133-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="7e133-150">これらの 2 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="7e133-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-151">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7e133-152">
                    <strong>経費を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7e133-153">
                    <strong>材料を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="7e133-154">
                    <strong>含まれるタスク</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-155">
                    <strong>ロール</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-156">
                    <strong>カテゴリ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-157">
                    <strong>タスク​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="7e133-158">
                    <strong>請求可否</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-159">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-160">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-161">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-162">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-163">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-164">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-165">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-166">実績時間に基づく請求: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-167">経費の実績に基づく請求タイプ: <strong>課金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-168">材料実績の請求タイプ: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-169">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-170">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-171">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-172">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="7e133-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-173">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-174">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-175">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-176">実績時間に基づく請求: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-177">経費の実績に基づく請求タイプ: <strong>課金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-178">材料実績の請求タイプ: <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-179">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-180">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-181">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-182">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="7e133-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-183">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-184">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-185">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-186">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-187">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="7e133-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7e133-188">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-189">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-190">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-191">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-192">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="7e133-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-193">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-194">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-195">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-196">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-197">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-198">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-199">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-200">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-201">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-202">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="7e133-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-203">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-204">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-205">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-206">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-207">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-208">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-209">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-210">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-211">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-212">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="7e133-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-213">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-214">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-215">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-216">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-217">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-218">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-219">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-220">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-221">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-222">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-223">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-224">
                    <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-225">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-226">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-227">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="7e133-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7e133-228">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-229">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-230">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-231">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-232">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-233">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-234">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-235">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-236">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-237">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-238">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-239">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7e133-240">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-241">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-242">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-243">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-244">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-245">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-246">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="7e133-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7e133-247">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-248">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-249">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7e133-250">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7e133-251">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-252">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-253">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-254">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-255">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-256">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-257">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-258">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-259">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-260">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7e133-261">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-262">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-263">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-264">請求可能</span><span class="sxs-lookup"><span data-stu-id="7e133-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-265">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-266">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="7e133-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7e133-267">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="7e133-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7e133-268">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7e133-269">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7e133-270">有効</span><span class="sxs-lookup"><span data-stu-id="7e133-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7e133-271">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7e133-272">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="7e133-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7e133-273">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7e133-274">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7e133-275">設定できません</span><span class="sxs-lookup"><span data-stu-id="7e133-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7e133-276">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-277">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7e133-278">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e133-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
