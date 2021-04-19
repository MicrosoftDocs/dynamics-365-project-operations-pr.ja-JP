---
title: プロジェクトの契約品目の請求可能コンポーネントを構成する
description: このトピックでは、契約品目に含まれるコンポーネント、有料コンポーネント、および非有料コンポーネントに関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858344"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a><span data-ttu-id="93183-103">プロジェクトの契約品目の請求可能コンポーネントを構成する</span><span class="sxs-lookup"><span data-stu-id="93183-103">Configure chargeable components of a project contract line</span></span>

<span data-ttu-id="93183-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="93183-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="93183-105">プロジェクトベースの契約品目には、付属するもの、課金されるもの、課金されないものという概念があります。</span><span class="sxs-lookup"><span data-stu-id="93183-105">A project-based contract line has the concept of included, chargeable, and non-chargeable components.</span></span>

<span data-ttu-id="93183-106">付属型コンポーネントは、プロジェクトベースの契約品目で定義された請求方法、顧客分割、超過しない限度額、および請求頻度の設定の対象となります。</span><span class="sxs-lookup"><span data-stu-id="93183-106">Included components are subject to the billing method, customer splits, not-to-exceed limits, and invoice frequency settings defined on the project-based contract line.</span></span>

<span data-ttu-id="93183-107">付属型コンポーネントのサブセットは、**請求タイプ** フィールドを更新して有料型としてマークですることができます。</span><span class="sxs-lookup"><span data-stu-id="93183-107">A subset of the included components can be marked as chargeable by updating the **Billing Type** field.</span></span>

<span data-ttu-id="93183-108">有料型のコンポーネントは、タスク、ロール、トランザクション カテゴリで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="93183-108">Chargeable components can be defined on roles, and transaction categories.</span></span>

<span data-ttu-id="93183-109">プロジェクト契約品目のロールで定義された課金対象は、**時間** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93183-109">For a project contract line, the chargeability defined on a role only applies to the **Time** transaction class.</span></span> <span data-ttu-id="93183-110">プロジェクトの契約品目の **時間を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**有料型ロール** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93183-110">If **Include Time** is set to **No** on a project contract line, the **Chargeable roles** tab isn't available.</span></span>

<span data-ttu-id="93183-111">プロジェクト契約品目のトランザクション カテゴリで定義された課金対象は、**経費** トランザクション クラスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93183-111">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="93183-112">プロジェクトの契約品目の **経費を含める** フィールドが空白であるか、**いいえ** に設定されている場合は、**有料型カテゴリー** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93183-112">If **Include Expenses** is set to **No** on a project contract line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="93183-113">ロールを課金対象、または非課金対象として更新します</span><span class="sxs-lookup"><span data-stu-id="93183-113">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="93183-114">ロールは、プロジェクトベースの契約品目では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="93183-114">A role can be chargeable or non-chargeable on specific project-based contract line.</span></span>

<span data-ttu-id="93183-115">プロジェクトベースの契約品目の **課金対象のロール** タブで、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドで、ロールの課金タイプを更新します。</span><span class="sxs-lookup"><span data-stu-id="93183-115">On the **Chargeable roles** tab of a projec-based contract line, on the **Chargeable Categories** subgrid, in the **Billing Type** field, update the billing type for a role.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="93183-116">トランザクション カテゴリを課金対象、または非課金対象として更新する</span><span class="sxs-lookup"><span data-stu-id="93183-116">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="93183-117">トランザクション カテゴリは、プロジェクトベースのの契約品目では課金対象となる場合と非課金対象となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="93183-117">A transaction category can be chargeable or non-chargeable on a specific project-based contract line.</span></span>

<span data-ttu-id="93183-118">プロジェクト ベースの契約品目の **課金対象のカテゴリ** タブで、**課金対象のカテゴリ** サブグリッドの **課金タイプ** フィールドで、トランザクションの課金タイプを更新します。</span><span class="sxs-lookup"><span data-stu-id="93183-118">On the **Chargeable Categories** tab of a project-based contract line, on the **Chargeable Categories** subgrid, in the **Billing Type** field, update the billing type for a transaction.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="93183-119">課金対象の解決</span><span class="sxs-lookup"><span data-stu-id="93183-119">Resolve chargeability</span></span>

<span data-ttu-id="93183-120">時間に対して作成された見積もりや実績は、契約品目に時間が含まれていて、かつ契約品目でタスクとロールが課金対象として設定されている場合にのみ、課金対象とみなされます。</span><span class="sxs-lookup"><span data-stu-id="93183-120">An estimate or actual created for time will only be considered chargeable if time is included on the contract line, and if the role is configured as chargeable on the contract line.</span></span>

<span data-ttu-id="93183-121">経費に対して作成された見積もりや実績は、契約品目に経費が含まれている場合、かつ契約品目でトランザクションのカテゴリが経費として設定されている場合にのみ、経費が発生するとみなされます。</span><span class="sxs-lookup"><span data-stu-id="93183-121">An estimate or actual created for expense will only be considered chargeable if expense is included on the contract line, and if the transaction category is configured as chargeable on the contract line.</span></span>

| <span data-ttu-id="93183-122">時間を含む</span><span class="sxs-lookup"><span data-stu-id="93183-122">Includes time</span></span> | <span data-ttu-id="93183-123">経費を含む</span><span class="sxs-lookup"><span data-stu-id="93183-123">Includes expense</span></span> | <span data-ttu-id="93183-124">ロール</span><span class="sxs-lookup"><span data-stu-id="93183-124">Role</span></span> | <span data-ttu-id="93183-125">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="93183-125">Category</span></span> | <span data-ttu-id="93183-126">タスク​</span><span class="sxs-lookup"><span data-stu-id="93183-126">Task</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="93183-127">有効</span><span class="sxs-lookup"><span data-stu-id="93183-127">Yes</span></span> | <span data-ttu-id="93183-128">有効</span><span class="sxs-lookup"><span data-stu-id="93183-128">Yes</span></span> | <span data-ttu-id="93183-129">請求可能</span><span class="sxs-lookup"><span data-stu-id="93183-129">Chargeable</span></span> | <span data-ttu-id="93183-130">請求可能</span><span class="sxs-lookup"><span data-stu-id="93183-130">Chargeable</span></span> | <span data-ttu-id="93183-131">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="93183-131">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="93183-132">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="93183-132">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="93183-133">有効</span><span class="sxs-lookup"><span data-stu-id="93183-133">Yes</span></span> | <span data-ttu-id="93183-134">有効</span><span class="sxs-lookup"><span data-stu-id="93183-134">Yes</span></span> | <span data-ttu-id="93183-135">請求不可</span><span class="sxs-lookup"><span data-stu-id="93183-135">Non - Chargeable</span></span> | <span data-ttu-id="93183-136">請求可能</span><span class="sxs-lookup"><span data-stu-id="93183-136">Chargeable</span></span> | <span data-ttu-id="93183-137">実績時間に基づく請求 : 非課金</span><span class="sxs-lookup"><span data-stu-id="93183-137">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="93183-138">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="93183-138">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="93183-139">有効</span><span class="sxs-lookup"><span data-stu-id="93183-139">Yes</span></span> | <span data-ttu-id="93183-140">有効</span><span class="sxs-lookup"><span data-stu-id="93183-140">Yes</span></span> | <span data-ttu-id="93183-141">請求不可</span><span class="sxs-lookup"><span data-stu-id="93183-141">Non-Chargeable</span></span> | <span data-ttu-id="93183-142">請求不可</span><span class="sxs-lookup"><span data-stu-id="93183-142">Non-Chargeable</span></span> | <span data-ttu-id="93183-143">実績時間に基づく請求 : 非課金</span><span class="sxs-lookup"><span data-stu-id="93183-143">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="93183-144">経費の実績に基づく請求タイプ : 非課金</span><span class="sxs-lookup"><span data-stu-id="93183-144">Billing type on an expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="93183-145">無効</span><span class="sxs-lookup"><span data-stu-id="93183-145">No</span></span> | <span data-ttu-id="93183-146">有効</span><span class="sxs-lookup"><span data-stu-id="93183-146">Yes</span></span> | <span data-ttu-id="93183-147">設定できません</span><span class="sxs-lookup"><span data-stu-id="93183-147">Can't be set</span></span> | <span data-ttu-id="93183-148">請求可能</span><span class="sxs-lookup"><span data-stu-id="93183-148">Chargeable</span></span> | <span data-ttu-id="93183-149">実績時間に基づく請求 : 非対応</span><span class="sxs-lookup"><span data-stu-id="93183-149">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="93183-150">経費の実績に基づく請求タイプ : 課金</span><span class="sxs-lookup"><span data-stu-id="93183-150">Billing type on an expense actual:Chargeable</span></span> |
| <span data-ttu-id="93183-151">無効</span><span class="sxs-lookup"><span data-stu-id="93183-151">No</span></span> | <span data-ttu-id="93183-152">有効</span><span class="sxs-lookup"><span data-stu-id="93183-152">Yes</span></span> | <span data-ttu-id="93183-153">設定できません</span><span class="sxs-lookup"><span data-stu-id="93183-153">Can't be set</span></span> | <span data-ttu-id="93183-154">請求不可</span><span class="sxs-lookup"><span data-stu-id="93183-154">Non-Chargeable</span></span> | <span data-ttu-id="93183-155">実績時間に基づく請求 : 非対応</span><span class="sxs-lookup"><span data-stu-id="93183-155">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="93183-156">経費の実績に基づく請求タイプ : 非課金</span><span class="sxs-lookup"><span data-stu-id="93183-156">Billing type on an expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="93183-157">有効</span><span class="sxs-lookup"><span data-stu-id="93183-157">Yes</span></span> | <span data-ttu-id="93183-158">無効</span><span class="sxs-lookup"><span data-stu-id="93183-158">No</span></span> | <span data-ttu-id="93183-159">請求可能</span><span class="sxs-lookup"><span data-stu-id="93183-159">Chargeable</span></span> | <span data-ttu-id="93183-160">設定できません</span><span class="sxs-lookup"><span data-stu-id="93183-160">Can't be set</span></span> | <span data-ttu-id="93183-161">実績時間に基づく請求 : 課金</span><span class="sxs-lookup"><span data-stu-id="93183-161">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="93183-162">経費の実績に基づく請求タイプ : 非対応</span><span class="sxs-lookup"><span data-stu-id="93183-162">Billing type on an expense actual: Not available</span></span> |
| <span data-ttu-id="93183-163">有効</span><span class="sxs-lookup"><span data-stu-id="93183-163">Yes</span></span> | <span data-ttu-id="93183-164">無効</span><span class="sxs-lookup"><span data-stu-id="93183-164">No</span></span> | <span data-ttu-id="93183-165">請求不可</span><span class="sxs-lookup"><span data-stu-id="93183-165">Non-Chargeable</span></span> | <span data-ttu-id="93183-166">設定できません</span><span class="sxs-lookup"><span data-stu-id="93183-166">Can't be set</span></span> | <span data-ttu-id="93183-167">実績時間に基づく請求 : 非課金</span><span class="sxs-lookup"><span data-stu-id="93183-167">Billing on a time actual: Non-chargeable</span></span> </br> <span data-ttu-id="93183-168">経費の実績に基づく請求タイプ : 非対応</span><span class="sxs-lookup"><span data-stu-id="93183-168">Billing type on an expense actual: Not available</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
