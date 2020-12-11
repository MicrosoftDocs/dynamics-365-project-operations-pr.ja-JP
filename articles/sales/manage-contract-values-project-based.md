---
title: プロジェクト ベースの契約品目で作業する
description: このトピックでは、プロジェクトベースの契約品目の見積もりについて解説します。
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 14d880eccd5547c122ebe37b63022e64fa2fb6fe
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181727"
---
# <a name="work-with-projectbased-contract-lines"></a><span data-ttu-id="8604d-103">プロジェクト ベースの契約品目で作業する</span><span class="sxs-lookup"><span data-stu-id="8604d-103">Work with project–based contract lines</span></span>

<span data-ttu-id="8604d-104">Dynamics 365 Project Operations のプロジェクトベースの契約品目は、エンゲージメントに関するプロジェクト作業の特定のコンポーネントの見積もりおよび請求契約を保持するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="8604d-104">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="8604d-105">プロジェクトベースの契約品目の構造は、次の概念を使用してプロジェクトの見積もりと請求シナリオに拡張されます :</span><span class="sxs-lookup"><span data-stu-id="8604d-105">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="8604d-106">請求方法</span><span class="sxs-lookup"><span data-stu-id="8604d-106">Billing method</span></span>
- <span data-ttu-id="8604d-107">プロジェクトとタスクのマッピング</span><span class="sxs-lookup"><span data-stu-id="8604d-107">Project and task mapping</span></span>
- <span data-ttu-id="8604d-108">含まれるトランザクションのクラス</span><span class="sxs-lookup"><span data-stu-id="8604d-108">Included transaction classes</span></span>
- <span data-ttu-id="8604d-109">上限</span><span class="sxs-lookup"><span data-stu-id="8604d-109">Not-to-exceed limit</span></span>
- <span data-ttu-id="8604d-110">請求可否の設定</span><span class="sxs-lookup"><span data-stu-id="8604d-110">Chargeability setup</span></span>
- <span data-ttu-id="8604d-111">契約品目の詳細を使用した見積もり</span><span class="sxs-lookup"><span data-stu-id="8604d-111">Estimates using contract line details</span></span>
- <span data-ttu-id="8604d-112">契約品目の顧客</span><span class="sxs-lookup"><span data-stu-id="8604d-112">Contract line customers</span></span>

<span data-ttu-id="8604d-113">プロジェクトベースの契約品目の **全般** タブには次のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-113">The following fields are included on the **General** tab of project–based contract lines.</span></span> <span data-ttu-id="8604d-114">これらのフィールドは、プロジェクト ベースの作業で使用するゼロからの見積もりと請求の取り決めの基礎を設定する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8604d-114">These fields help to set up the basis for a detailed, ground–up estimate and the billing arrangements for project–based work.</span></span>

| <span data-ttu-id="8604d-115">フィールド</span><span class="sxs-lookup"><span data-stu-id="8604d-115">Field</span></span> | <span data-ttu-id="8604d-116">内容</span><span class="sxs-lookup"><span data-stu-id="8604d-116">Description</span></span> | <span data-ttu-id="8604d-117">下位への影響</span><span class="sxs-lookup"><span data-stu-id="8604d-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8604d-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="8604d-118">**Name**</span></span> | <span data-ttu-id="8604d-119">見積もられている契約の個別のコンポーネントを識別す契約品目の名前です。</span><span class="sxs-lookup"><span data-stu-id="8604d-119">The name of the contract line that identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="8604d-120">見積から作成されたプロジェクト契約書の場合、この値はプロジェクトベースの見積明細行の対応する値からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8604d-120">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="8604d-121">このフィールドの値は、請求書の作成時にこの契約明細から作成されるプロジェクト請求書の明細にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8604d-121">This field value is copied to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="8604d-122">**請求方法**</span><span class="sxs-lookup"><span data-stu-id="8604d-122">**Billing Method**</span></span> | <span data-ttu-id="8604d-123">見積から作成されたプロジェクト契約書では、この値は見積明細行の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8604d-123">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8604d-124">これはオプション セットであり、Project Operations で対応している 2 つの主要な契約モデルを表しています :</span><span class="sxs-lookup"><span data-stu-id="8604d-124">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="8604d-125">- **固定価格**</span><span class="sxs-lookup"><span data-stu-id="8604d-125">- **Fixed Price**</span></span></br><span data-ttu-id="8604d-126">- **時間と材料**</span><span class="sxs-lookup"><span data-stu-id="8604d-126">- **Time and Material**</span></span> | <span data-ttu-id="8604d-127">参照した契約品目の課金方法に基づいて、実際のトランザクションが処理されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-127">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="8604d-128">実績で参照された契約品目に時間と材料に基づく課金方式がある場合は、原価と未請求の売上実績レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-128">If the contract line referenced by the actual has a time and material billing method, a cost and an unbilled sales actual record are created.</span></span> <span data-ttu-id="8604d-129">実質が参照している契約品目に固定の課金方式がある場合は、原価実質のみを作成します。</span><span class="sxs-lookup"><span data-stu-id="8604d-129">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="8604d-130">**Project**</span><span class="sxs-lookup"><span data-stu-id="8604d-130">**Project**</span></span> | <span data-ttu-id="8604d-131">このフィールドを使用して、このエンゲージメントの作業の提供に使用されるプロジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="8604d-131">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="8604d-132">このフィールドの値は、**含まれるタスク** および **含まれるトランザクション クラス** フィールドと組み合わせて使用され、実際の品目レコードまたは見積品目レコードの契約品目の参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="8604d-132">The value in this field is used in conjunction with **Included Tasks** and **Included Transaction Classes** fields to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8604d-133">**時間を含む**</span><span class="sxs-lookup"><span data-stu-id="8604d-133">**Include Time**</span></span> | <span data-ttu-id="8604d-134">フラグは、選択したプロジェクトの時間トランザクションまたは人件費がこの契約品目に含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-134">A flag indicates if time transactions or labor costs on the selected project are included on this contract line.</span></span> <span data-ttu-id="8604d-135">値が **いいえ** となっている場合は、時間トランザクションまたは人件費がこの契約品目に含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-135">A **No** value indicates that the time transactions or labor costs will not be included on this contract line.</span></span> <span data-ttu-id="8604d-136">値が **はい** の場合は、含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-136">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8604d-137">このフィールドの値は、プロジェクトと組み合わせて使用され、実際の品目レコードまたは見積もり品目レコードの契約品目の参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="8604d-137">This field value is used in conjunction with project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8604d-138">**経費を含む**</span><span class="sxs-lookup"><span data-stu-id="8604d-138">**Include Expense**</span></span> | <span data-ttu-id="8604d-139">フラグは、選択したプロジェクトの経費がこの契約品目に含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-139">A flag indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8604d-140">値が **いいえ** となっている場合は、この契約品目には経費として計上されません。</span><span class="sxs-lookup"><span data-stu-id="8604d-140">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="8604d-141">値が **はい** の場合は、計上されることを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-141">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="8604d-142">このフィールドの値は、プロジェクトと組み合わせて使用され、実際の品目レコードまたは見積もり品目レコードの契約品目の参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="8604d-142">This field value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8604d-143">**料金を含む**</span><span class="sxs-lookup"><span data-stu-id="8604d-143">**Include Fee**</span></span> | <span data-ttu-id="8604d-144">フラグは、選択したプロジェクトの料金がこの契約品目に含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-144">A flag indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8604d-145">値が **いいえ** となっている場合は、この契約品目には料金として計上されません。</span><span class="sxs-lookup"><span data-stu-id="8604d-145">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="8604d-146">値が **はい** の場合は、含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="8604d-146">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8604d-147">このフィールドの値は、プロジェクトと組み合わせて使用され、実際の品目レコードまたは見積もり品目レコードの契約品目の参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="8604d-147">This field value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8604d-148">**契約金額**</span><span class="sxs-lookup"><span data-stu-id="8604d-148">**Contracted Amount**</span></span> | <span data-ttu-id="8604d-149">固定価格の契約品目では、この契約品目に関連するすべての作業コンポーネントについて顧客に請求される合意された値です。</span><span class="sxs-lookup"><span data-stu-id="8604d-149">On a fixed price contract line, this is the agreed-on value that will be invoiced to the customer for all the work components associated with this contract line.</span></span> <span data-ttu-id="8604d-150">時間と材料の契約品目では、この金額は、この契約品目に関連するすべての作業コンポーネントについて顧客に請求されるものの推定値です。</span><span class="sxs-lookup"><span data-stu-id="8604d-150">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="8604d-151">見積から作成されたプロジェクト契約書では、この値は見積明細行の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8604d-151">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8604d-152">プロジェクトベースの契約品目に明細行がある場合、このフィールドは編集用にロックされ、契約行の明細の金額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-152">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="8604d-153">契約品目に明細行がある場合、この値は明細の金額を変更することで、この値を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8604d-153">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="8604d-154">固定価格の契約品目では、この値を利用して定期的な請求マイルストーンの税引前金額を生成します。</span><span class="sxs-lookup"><span data-stu-id="8604d-154">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8604d-155">**予測税額**</span><span class="sxs-lookup"><span data-stu-id="8604d-155">**Estimated Tax**</span></span> | <span data-ttu-id="8604d-156">ユーザーはこのフィールドを編集して、契約品目に推定税額を入力できます。</span><span class="sxs-lookup"><span data-stu-id="8604d-156">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="8604d-157">プロジェクトベースの契約品目に明細行がある場合、このフィールドは編集用にロックされ、契約行の明細の税額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-157">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="8604d-158">契約品目に明細行がある場合、この値は明細の金額を変更することで、この税額を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8604d-158">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="8604d-159">固定価格契約品目では、この値は定期的な請求マイルストーンに対する税額を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-159">On a fixed price contract line, this value is used to generate tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8604d-160">**税引き後の契約金額**</span><span class="sxs-lookup"><span data-stu-id="8604d-160">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="8604d-161">税引き後の契約品目です。</span><span class="sxs-lookup"><span data-stu-id="8604d-161">The contract line amount after tax.</span></span> <span data-ttu-id="8604d-162">このフィールドは読み取り専用であり、**契約金額+税金** として計算されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-162">This field is read-only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="8604d-163">固定価格の契約品目では、この値は定期的な課金のマイルストーンを生成する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-163">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="8604d-164">**上限**</span><span class="sxs-lookup"><span data-stu-id="8604d-164">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="8604d-165">ユーザーはこのフィールドを編集でき、時間と材料の請求方法があるプロジェクトベースの契約品目でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8604d-165">The user can edit this field and it is only available on project-based contract lines that have a time and material billing method.</span></span> | <span data-ttu-id="8604d-166">ユーザーはこのフィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="8604d-166">The user can edit this field.</span></span> <span data-ttu-id="8604d-167">時間または費用の実際が時間と材料についてこの契約品目を参照する場合、実際の金額は、すでに使用されコミットされた金額を考慮した後、この契約品目の超過しない限度額と比較して評価されます。</span><span class="sxs-lookup"><span data-stu-id="8604d-167">When a time or expense actual references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on this contract line after accounting for the already spent and committed amounts.</span></span> |
| <span data-ttu-id="8604d-168">**顧客の予算**</span><span class="sxs-lookup"><span data-stu-id="8604d-168">**Customer Budget**</span></span> | <span data-ttu-id="8604d-169">このフィールドは編集可能で、見積書から契約書が作成された場合は、見積書明細の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8604d-169">This field is editable and is copied from the corresponding field on the quote line, if the contract was created from a quote.</span></span> | <span data-ttu-id="8604d-170">このフィールドは情報としてのみ使用され、、ダウンストリームへの影響はありません。</span><span class="sxs-lookup"><span data-stu-id="8604d-170">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="8604d-171">プロジェクト ベースの契約品目の全般タブのオプションで使用する検証ルール</span><span class="sxs-lookup"><span data-stu-id="8604d-171">Validation rule for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="8604d-172">ルール : プロジェクトと特定のトランザクション クラスは、契約書の 1 つのプロジェクト ベースの契約品目にのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8604d-172">Rule: A project and a certain transaction class can only be included on one project-based contract line in a contract.</span></span>

| <span data-ttu-id="8604d-173">契約 </span><span class="sxs-lookup"><span data-stu-id="8604d-173">Contract</span></span> | <span data-ttu-id="8604d-174">契約品目</span><span class="sxs-lookup"><span data-stu-id="8604d-174">Contract line</span></span> | <span data-ttu-id="8604d-175">Project</span><span class="sxs-lookup"><span data-stu-id="8604d-175">Project</span></span> | <span data-ttu-id="8604d-176">時間を含む</span><span class="sxs-lookup"><span data-stu-id="8604d-176">Include time</span></span> | <span data-ttu-id="8604d-177">経費を含む</span><span class="sxs-lookup"><span data-stu-id="8604d-177">Include expense</span></span> | <span data-ttu-id="8604d-178">料金を含む</span><span class="sxs-lookup"><span data-stu-id="8604d-178">Include fee</span></span> | <span data-ttu-id="8604d-179">有効/無効</span><span class="sxs-lookup"><span data-stu-id="8604d-179">Valid/not valid</span></span> | <span data-ttu-id="8604d-180">理由</span><span class="sxs-lookup"><span data-stu-id="8604d-180">Reason</span></span>                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8604d-181">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-181">C1</span></span>       | <span data-ttu-id="8604d-182">CL1</span><span class="sxs-lookup"><span data-stu-id="8604d-182">CL1</span></span>           | <span data-ttu-id="8604d-183">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-183">P1</span></span>      | <span data-ttu-id="8604d-184">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-184">Yes</span></span>          | <span data-ttu-id="8604d-185">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-185">Yes</span></span>             | <span data-ttu-id="8604d-186">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-186">Yes</span></span>         | <span data-ttu-id="8604d-187">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-187">Not valid</span></span>       | <span data-ttu-id="8604d-188">ルールに違反します。</span><span class="sxs-lookup"><span data-stu-id="8604d-188">Violates the rule.</span></span> <span data-ttu-id="8604d-189">プロジェクト P1 にかかる時間、費用、手数料は、CL1 と CL2 の両契約品目に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-189">Time,   expense, and fees on project P1 are included on both contract lines, CL1 and   CL2.</span></span>                                                                                       |
| <span data-ttu-id="8604d-190">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-190">C1</span></span>       | <span data-ttu-id="8604d-191">CL2</span><span class="sxs-lookup"><span data-stu-id="8604d-191">CL2</span></span>           | <span data-ttu-id="8604d-192">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-192">P1</span></span>      | <span data-ttu-id="8604d-193">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-193">Yes</span></span>          | <span data-ttu-id="8604d-194">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-194">Yes</span></span>             | <span data-ttu-id="8604d-195">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-195">Yes</span></span>         | <span data-ttu-id="8604d-196">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-196">Not valid</span></span>       | <span data-ttu-id="8604d-197">ルールに違反します。</span><span class="sxs-lookup"><span data-stu-id="8604d-197">Violates the rule.</span></span> <span data-ttu-id="8604d-198">プロジェクト P1 にかかる時間、費用、手数料は、CL1 と CL2 の両契約品目に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-198">Time,   expense, and fees on project P1 are included on both contract lines, CL1 and   CL2.</span></span>                                                                                       |
| <span data-ttu-id="8604d-199">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-199">C1</span></span>       | <span data-ttu-id="8604d-200">CL1</span><span class="sxs-lookup"><span data-stu-id="8604d-200">CL1</span></span>           | <span data-ttu-id="8604d-201">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-201">P1</span></span>      | <span data-ttu-id="8604d-202">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-202">Yes</span></span>          | <span data-ttu-id="8604d-203">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-203">No</span></span>              | <span data-ttu-id="8604d-204">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-204">Yes</span></span>         | <span data-ttu-id="8604d-205">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-205">Not valid</span></span>       | <span data-ttu-id="8604d-206">ルールに違反します。</span><span class="sxs-lookup"><span data-stu-id="8604d-206">Violates the rule.</span></span> <span data-ttu-id="8604d-207">プロジェクト P1 の時間と料金は、CL1 と CL2 の両契約品目に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-207">Time and   fees on project P1 are included on both contract lines, CL1 and CL2.</span></span>                                                                                                   |
| <span data-ttu-id="8604d-208">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-208">C1</span></span>       | <span data-ttu-id="8604d-209">CL2</span><span class="sxs-lookup"><span data-stu-id="8604d-209">CL2</span></span>           | <span data-ttu-id="8604d-210">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-210">P1</span></span>      | <span data-ttu-id="8604d-211">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-211">Yes</span></span>          | <span data-ttu-id="8604d-212">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-212">Yes</span></span>             | <span data-ttu-id="8604d-213">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-213">Yes</span></span>         | <span data-ttu-id="8604d-214">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-214">Not valid</span></span>       | <span data-ttu-id="8604d-215">ルールに違反します。</span><span class="sxs-lookup"><span data-stu-id="8604d-215">Violates the rule.</span></span> <span data-ttu-id="8604d-216">プロジェクト P1 の時間と料金は、CL1 と CL2 の両契約品目に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-216">Time and   fees on project P1 are included on both contract lines, CL1 and CL2.</span></span>                                                                                                   |
| <span data-ttu-id="8604d-217">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-217">C1</span></span>       | <span data-ttu-id="8604d-218">CL1</span><span class="sxs-lookup"><span data-stu-id="8604d-218">CL1</span></span>           | <span data-ttu-id="8604d-219">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-219">P1</span></span>      | <span data-ttu-id="8604d-220">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-220">Yes</span></span>          | <span data-ttu-id="8604d-221">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-221">No</span></span>              | <span data-ttu-id="8604d-222">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-222">Yes</span></span>         | <span data-ttu-id="8604d-223">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-223">Valid</span></span>           | <span data-ttu-id="8604d-224">プロジェクト P1 の時間と料金は CL1 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-224">Time and fees on project P1 are   included on the CL1.</span></span> <span data-ttu-id="8604d-225">P1 の経費は CL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-225">Expense on project P1 is included on CL2.</span></span> </br>   <span data-ttu-id="8604d-226">各契約品目に含まれているものは重複していないため、有効です。</span><span class="sxs-lookup"><span data-stu-id="8604d-226">There is no overlap in what is being included on each contract line and is   therefore valid.</span></span>  |
| <span data-ttu-id="8604d-227">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-227">C1</span></span>       | <span data-ttu-id="8604d-228">CL2</span><span class="sxs-lookup"><span data-stu-id="8604d-228">CL2</span></span>           | <span data-ttu-id="8604d-229">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-229">P1</span></span>      | <span data-ttu-id="8604d-230">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-230">No</span></span>           | <span data-ttu-id="8604d-231">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-231">Yes</span></span>             | <span data-ttu-id="8604d-232">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-232">No</span></span>          | <span data-ttu-id="8604d-233">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-233">Valid</span></span>           | <span data-ttu-id="8604d-234">プロジェクト P1 の時間と料金は CL1 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-234">Time and fees on project P1 are   included on the CL1.</span></span> <span data-ttu-id="8604d-235">P1 の経費は CL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-235">Expense on project P1 is included on CL2.</span></span> </br>   <span data-ttu-id="8604d-236">各契約品目に含まれているものは重複していないため、有効です。</span><span class="sxs-lookup"><span data-stu-id="8604d-236">There is no overlap in what is being included on each contract line and is   therefore valid.</span></span>  |
| <span data-ttu-id="8604d-237">C1</span><span class="sxs-lookup"><span data-stu-id="8604d-237">C1</span></span>       | <span data-ttu-id="8604d-238">CL1</span><span class="sxs-lookup"><span data-stu-id="8604d-238">CL1</span></span>           | <span data-ttu-id="8604d-239">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-239">P1</span></span>      | <span data-ttu-id="8604d-240">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-240">Yes</span></span>          | <span data-ttu-id="8604d-241">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-241">Yes</span></span>             | <span data-ttu-id="8604d-242">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-242">Yes</span></span>         | <span data-ttu-id="8604d-243">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-243">Not valid</span></span>       | <span data-ttu-id="8604d-244">ルールに違反します。</span><span class="sxs-lookup"><span data-stu-id="8604d-244">Violates the rule.</span></span> <span data-ttu-id="8604d-245">プロジェクト P1 の時間、費用、料金は、2つの契約の品目に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-245">Time,   expense, and fees on project P1 are included on the lines of two contracts.</span></span>                                                                                               |
| <span data-ttu-id="8604d-246">CL2</span><span class="sxs-lookup"><span data-stu-id="8604d-246">CL2</span></span>      | <span data-ttu-id="8604d-247">CL2</span><span class="sxs-lookup"><span data-stu-id="8604d-247">CL2</span></span>           | <span data-ttu-id="8604d-248">P1</span><span class="sxs-lookup"><span data-stu-id="8604d-248">P1</span></span>      | <span data-ttu-id="8604d-249">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-249">Yes</span></span>          | <span data-ttu-id="8604d-250">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-250">Yes</span></span>             | <span data-ttu-id="8604d-251">有効</span><span class="sxs-lookup"><span data-stu-id="8604d-251">Yes</span></span>         | <span data-ttu-id="8604d-252">無効</span><span class="sxs-lookup"><span data-stu-id="8604d-252">Not valid</span></span>       | <span data-ttu-id="8604d-253">ルールに違反します。</span><span class="sxs-lookup"><span data-stu-id="8604d-253">Violates the rule.</span></span> <span data-ttu-id="8604d-254">プロジェクト P1 の時間、費用、料金は、2つの契約の品目に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8604d-254">Time,   expense, and fees on project P1 are included on the lines of two contracts.</span></span>                                                                                               |