---
title: 見積依頼明細行の請求可能コンポーネントを構成する
description: このトピックでは、プロジェクトベースの見積明細での課金対象コンポーネントと非課金対象コンポーネントの設定に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858299"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="8e840-103">見積依頼明細行の請求可能コンポーネントを構成する</span><span class="sxs-lookup"><span data-stu-id="8e840-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="8e840-104">_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8e840-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8e840-105">プロジェクト ベースの見積品目には、*付属型* コンポーネントと *有料型* コンポーネントの概念があります。</span><span class="sxs-lookup"><span data-stu-id="8e840-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="8e840-106">含まれているコンポーネントは、次の対象となります :</span><span class="sxs-lookup"><span data-stu-id="8e840-106">Included components are subject to:</span></span>

  - <span data-ttu-id="8e840-107">請求方法と顧客の分割</span><span class="sxs-lookup"><span data-stu-id="8e840-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="8e840-108">上限</span><span class="sxs-lookup"><span data-stu-id="8e840-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="8e840-109">プロジェクト ベースの見積明細で定義された請求書の発行の頻度設定</span><span class="sxs-lookup"><span data-stu-id="8e840-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="8e840-110">付属型コンポーネントのサブセットは、**請求タイプ** フィールドを使用して課金型としてマークですることができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="8e840-111">**請求タイプ** フィールドは、見積明細のコンテキストで次の値を許可するオプションセットです :</span><span class="sxs-lookup"><span data-stu-id="8e840-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="8e840-112">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-112">Chargeable</span></span>
  - <span data-ttu-id="8e840-113">請求不可</span><span class="sxs-lookup"><span data-stu-id="8e840-113">Non-chargeable</span></span>

<span data-ttu-id="8e840-114">課金型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="8e840-115">課金対象は、見積明細のタスクで定義され、明細に含まれるすべてのトランザクション クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="8e840-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="8e840-116">契約品目の **タスクを含める** フィールドが空白であるか、**プロジェクト全体** に設定されている場合は、**有料型タスク** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8e840-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="8e840-117">プロジェクトの見積明細のロールで定義された課金対象は、**時間** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8e840-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="8e840-118">プロジェクトの見積明細の **時間を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**有料型ロール** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8e840-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="8e840-119">見積品目のトランザクション カテゴリで定義された課金対象は、**経費** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8e840-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="8e840-120">プロジェクトの見積明細の **経費を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**有料型カテゴリ** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8e840-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="8e840-121">プロジェクト タスクを課金対象または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="8e840-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="8e840-122">プロジェクト タスクは、特定のプロジェクトベースの見積明細で請求可/不可にすることができます。これにより、次の設定が可能になります。</span><span class="sxs-lookup"><span data-stu-id="8e840-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="8e840-123">プロジェクトベースの見積明細に **時間** とタスク **T1** が含まれている場合、タスクは課金対象として見積もり行に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="8e840-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="8e840-124">**経費** を含む 2 つ目の見積明細がある場合は、契約品目の **T1** タスクを非課金として関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="8e840-125">その結果、タスクに記録されたすべての時間は課金対象となり、経費に記録されているすべてのタスクは課金対象外になります。</span><span class="sxs-lookup"><span data-stu-id="8e840-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="8e840-126">タスクの課金タイプは、**見積もり品目タスク** サブグリッドの **課金タイプ** フィールドを更新することで、プロジェクト ベースの見積品目タブの **課金タスク** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="8e840-127">または、タスクに関連付けられた見積品目を表示するプロジェクトのタスクの課金設定のサブグリッドの **課金タイプ** フィールドで、プロジェクト タスクの課金タイプを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="8e840-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="8e840-128">ロールを課金対象、または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="8e840-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="8e840-129">ロールは、特定のプロジェクト ベースの見積明細のコンテキストによっては、課金または非課金にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="8e840-130">ロールの課金タイプは、**課金対象のロール** サブグリッドの **課金タイプ** フィールドを更新することで、プロジェクト ベースの見積品目タブの **課金タスク** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="8e840-131">トランザクション カテゴリを課金対象、または非課金対象として更新する</span><span class="sxs-lookup"><span data-stu-id="8e840-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="8e840-132">トランザクション カテゴリは、特定の見積明細では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8e840-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="8e840-133">トランザクションの課金タイプは、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドを更新することで、プロジェクト ベースの見積品目タブの **課金のカテゴリ** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8e840-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="8e840-134">課金対象の解決</span><span class="sxs-lookup"><span data-stu-id="8e840-134">Resolve chargeability</span></span>
<span data-ttu-id="8e840-135">時間に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="8e840-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="8e840-136">**時間** が見積もり行に含まれている。</span><span class="sxs-lookup"><span data-stu-id="8e840-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="8e840-137">**役割** が見積もり行で請求可能と構成されている。</span><span class="sxs-lookup"><span data-stu-id="8e840-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="8e840-138">**含まれるタスク** が、見積もり行で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="8e840-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="8e840-139">これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="8e840-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="8e840-140">経費に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="8e840-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="8e840-141">**経費** が、見積もり行に含まれている。</span><span class="sxs-lookup"><span data-stu-id="8e840-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="8e840-142">**トランザクション カテゴリ** が、見積もり行で請求可能と構成されている。</span><span class="sxs-lookup"><span data-stu-id="8e840-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="8e840-143">**含まれるタスク** が、見積もり行で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="8e840-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="8e840-144">これらの 3 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="8e840-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="8e840-145">材料に対して作成された見積もりまたは実際の見積もりは、次の場合にのみ請求可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="8e840-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="8e840-146">**材料** が、見積もり行に含まれている。</span><span class="sxs-lookup"><span data-stu-id="8e840-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="8e840-147">**含まれるタスク** が、見積もり行で **選択したタスク** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="8e840-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="8e840-148">これらの 2 つの条件が当てはまる場合、**タスク** は請求可能と構成されます。</span><span class="sxs-lookup"><span data-stu-id="8e840-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-149">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="8e840-150">
                    <strong>経費を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="8e840-151">
                    <strong>材料を含む</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="8e840-152">
                    <strong>含まれるタスク</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-153">
                    <strong>ロール</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-154">
                    <strong>カテゴリ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-155">
                    <strong>タスク​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="8e840-156">
                    <strong>請求可否</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-157">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-158">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-159">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-160">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-161">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-162">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-163">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-164">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-165">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-166">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-167">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-168">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-169">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-170">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="8e840-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-171">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-172">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-173">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-174">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-175">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-176">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-177">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-178">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-179">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-180">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="8e840-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-181">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-182">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-183">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-184">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-185">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-186">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-187">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-188">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-189">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-190">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="8e840-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-191">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-192">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-193">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-194">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-195">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-196">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-197">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-198">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-199">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-200">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="8e840-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-201">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-202">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-203">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-204">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-205">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-206">材料実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-207">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-208">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-209">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-210">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="8e840-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-211">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-212">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-213">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-214">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-215">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-216">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-217">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-218">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-219">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-220">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-221">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-222">
                    <strong>請求可能</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-223">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-224">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-225">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-226">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-227">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-228">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-229">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-230">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-231">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-232">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-233">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-234">時間実績に基づく請求:<strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-235">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-236">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-237">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="8e840-238">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-239">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-240">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-241">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-242">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-243">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-244">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-245">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-246">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-247">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="8e840-248">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="8e840-249">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-250">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-251">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-252">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-253">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-254">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-255">経費実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-256">材料実績の請求タイプ: 請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-257">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-258">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="8e840-259">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-260">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-261">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-262">請求可能</span><span class="sxs-lookup"><span data-stu-id="8e840-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-263">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-264">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-265">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="8e840-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="8e840-266">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="8e840-267">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="8e840-268">有効</span><span class="sxs-lookup"><span data-stu-id="8e840-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="8e840-269">
                    <strong>無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="8e840-270">プロジェクトの全体</span><span class="sxs-lookup"><span data-stu-id="8e840-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8e840-271">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="8e840-272">
                    <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8e840-273">設定不可</span><span class="sxs-lookup"><span data-stu-id="8e840-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="8e840-274">時間実績に基づく請求: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-275">経費実績に基づく請求タイプ: <strong>請求不可</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="8e840-276">資材実績に基づく請求タイプ: <strong>非対応</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8e840-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
