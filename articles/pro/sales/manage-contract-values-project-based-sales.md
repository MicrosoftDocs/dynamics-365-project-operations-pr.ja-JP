---
title: プロジェクトベースの契約品目の概要
description: このトピックでは、プロジェクトベースの契約品目を使用した作業について解説します。
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369922"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="2e2f0-103">プロジェクトベースの契約品目の概要</span><span class="sxs-lookup"><span data-stu-id="2e2f0-103">Project-based contract lines overview</span></span>

<span data-ttu-id="2e2f0-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="2e2f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e2f0-105">Dynamics 365 Project Operations のプロジェクトベースの契約品目は、エンゲージメントに関するプロジェクト作業の特定のコンポーネントの見積もりおよび請求契約を保持するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="2e2f0-106">プロジェクトベースの契約品目の構造は、次の概念によりプロジェクト見積および請求シナリオに対して拡張されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="2e2f0-107">請求方法</span><span class="sxs-lookup"><span data-stu-id="2e2f0-107">Billing method</span></span>
- <span data-ttu-id="2e2f0-108">プロジェクトとタスクのスケジュール</span><span class="sxs-lookup"><span data-stu-id="2e2f0-108">Project and task mapping</span></span>
- <span data-ttu-id="2e2f0-109">含まれるトランザクションのクラス</span><span class="sxs-lookup"><span data-stu-id="2e2f0-109">Included transaction classes</span></span>
- <span data-ttu-id="2e2f0-110">上限</span><span class="sxs-lookup"><span data-stu-id="2e2f0-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="2e2f0-111">請求可否の設定</span><span class="sxs-lookup"><span data-stu-id="2e2f0-111">Chargeability setup</span></span>
- <span data-ttu-id="2e2f0-112">契約品目の詳細を使用した見積もり</span><span class="sxs-lookup"><span data-stu-id="2e2f0-112">Estimates using contract line details</span></span>
- <span data-ttu-id="2e2f0-113">契約品目の顧客</span><span class="sxs-lookup"><span data-stu-id="2e2f0-113">Contract line customers</span></span>

<span data-ttu-id="2e2f0-114">以下の表には、プロジェクトベースの契約品目の **全般** タブのフィールドが含まれており、プロジェクトベースの作業で使用する詳細なゼロからの見積もりと請求の取り決めの基礎を設定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="2e2f0-115">フィールド</span><span class="sxs-lookup"><span data-stu-id="2e2f0-115">Field</span></span> | <span data-ttu-id="2e2f0-116">内容</span><span class="sxs-lookup"><span data-stu-id="2e2f0-116">Description</span></span> | <span data-ttu-id="2e2f0-117">下位への影響</span><span class="sxs-lookup"><span data-stu-id="2e2f0-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2e2f0-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-118">**Name**</span></span> | <span data-ttu-id="2e2f0-119">契約品目の名前です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-119">Name of the contract line.</span></span> <span data-ttu-id="2e2f0-120">見積もられている契約の個別のコンポーネントを識別します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="2e2f0-121">見積から作成されたプロジェクト契約書の場合、この値はプロジェクトベースの見積明細行の対応する値からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="2e2f0-122">請求書作成時にこの契約品目から作成されるプロジェクトの請求書行にコピーされた名前です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="2e2f0-123">**請求方法**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-123">**Billing Method**</span></span> | <span data-ttu-id="2e2f0-124">見積から作成されたプロジェクト契約書では、この値は見積明細行の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="2e2f0-125">これはオプション セットであり、Project Operations で対応している 2 つの主要な契約モデルを表しています :</span><span class="sxs-lookup"><span data-stu-id="2e2f0-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="2e2f0-126">- **固定価格**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-126">- **Fixed Price**</span></span></br><span data-ttu-id="2e2f0-127">- **時間と材料**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-127">- **Time and Material**</span></span> | <span data-ttu-id="2e2f0-128">参照した契約品目の課金方法に基づいて、実際のトランザクションが処理されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="2e2f0-129">実績で参照された契約品目に時間と材料に基づく課金方式がある場合は、原価と未請求の売上実績レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="2e2f0-130">実質が参照している契約品目に固定の課金方式がある場合は、原価実質のみを作成します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="2e2f0-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-131">**Project**</span></span> | <span data-ttu-id="2e2f0-132">このフィールドを使用して、このエンゲージメントの作業の提供に使用されるプロジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="2e2f0-133">この値は、**含まれるタスク** そして **含まれるトランザクション クラス** と併用して、実績または見積もり行レコードで契約品目参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="2e2f0-134">**含まれるタスク**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-134">**Included Tasks**</span></span> | <span data-ttu-id="2e2f0-135">この契約品目に、選択したプロジェクトのすべてのプロジェクト タスクが含まれるのか、タスクのサブセットのみが含まれるのかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="2e2f0-136">これは、次の値を持つオプション セットです :</span><span class="sxs-lookup"><span data-stu-id="2e2f0-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="2e2f0-137">- **すべてのプロジェクト タスク**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-137">- **All Project Tasks**</span></span></br><span data-ttu-id="2e2f0-138">- **選択したプロジェクト タスクのみ**。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="2e2f0-139">このフィールドの空白の値は、**すべてのプロジェクトタスク** 選択することと同じとなります。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="2e2f0-140">**選択されたタスクのみ** が選択されている場合、特定のタスクを選択して、**プロジェクト** ページの **タスク請求設定** タブでこの契約ラインに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="2e2f0-141">この値は、実際の品目レコードまたは見積品目レコードの契約品目参照を解決する目的で、**プロジェクト** クラスおよび **含まれるトランザクション** クラスと組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2e2f0-142">**時間を含む**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-142">**Include Time**</span></span> | <span data-ttu-id="2e2f0-143">**はい**/**いいえ** の値は、選択したプロジェクトの時間トランザクションまたは労務費がこの契約行に含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2e2f0-144">値が **いいえ** となっている場合は、時間トランザクションまたは人件費がこの契約品目に含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="2e2f0-145">値が **はい** の場合は、含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="2e2f0-146">この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2e2f0-147">**経費を含む**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-147">**Include Expense**</span></span> | <span data-ttu-id="2e2f0-148">**はい**/**いいえ** の値は、選択したプロジェクトの経費原価がこの契約行に含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2e2f0-149">値が **いいえ** となっている場合は、この契約品目には経費として計上されません。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="2e2f0-150">値が **はい** の場合は、計上されることを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="2e2f0-151">この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2e2f0-152">**材料を含む**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-152">**Include Materials**</span></span> | <span data-ttu-id="2e2f0-153">**はい**/**いいえ** の値は、選択したプロジェクトの材料原価がこの契約行に含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2e2f0-154">**いいえ** の値は、選択したプロジェクトの材料原価がこの契約行に含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="2e2f0-155">値が **はい** の場合は、計上されることを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="2e2f0-156">この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2e2f0-157">**料金を含む**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-157">**Include Fee**</span></span> | <span data-ttu-id="2e2f0-158">**はい**/**いいえ** の値は、選択したプロジェクトの手数料がこの契約行に含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2e2f0-159">値が **いいえ** となっている場合は、この契約品目には料金として計上されません。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="2e2f0-160">値が **はい** の場合は、含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="2e2f0-161">この値は、プロジェクトと併用し、実績行レコードまたは見積もり行レコードの契約品目参照を解決します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2e2f0-162">**契約金額**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-162">**Contracted Amount**</span></span> | <span data-ttu-id="2e2f0-163">固定価格の契約品目では、この金額は、この契約品目に関連するすべての作業コンポーネントについて顧客に請求される合意された値です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="2e2f0-164">時間と材料の契約品目では、この金額は、この契約品目に関連するすべての作業コンポーネントについて顧客に請求されるものの推定値です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="2e2f0-165">見積から作成されたプロジェクト契約書では、この値は見積明細行の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="2e2f0-166">プロジェクトベースの契約品目に明細行がある場合、このフィールドは編集用にロックされ、契約行の明細の金額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="2e2f0-167">契約品目に明細行がある場合、この値は明細の金額を変更することで、この値を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="2e2f0-168">固定価格の契約品目では、この値を利用して定期的な請求マイルストーンの税引前金額を生成します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="2e2f0-169">**予測税額**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-169">**Estimated Tax**</span></span> | <span data-ttu-id="2e2f0-170">ユーザーはこのフィールドを編集して、契約品目に推定税額を入力できます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="2e2f0-171">プロジェクトベースの契約品目に明細行がある場合、このフィールドは編集用にロックされ、契約行の明細の税額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="2e2f0-172">契約品目に明細行がある場合、この値は明細の金額を変更することで、この税額を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="2e2f0-173">固定価格契約品目では、この値は定期的な請求マイルストーンに対する税額を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="2e2f0-174">**税引き後の契約金額**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="2e2f0-175">税引き後の契約品目です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-175">The contract line amount after tax.</span></span> <span data-ttu-id="2e2f0-176">このフィールドは読み取り専用であり、**契約金額+税金** として計算されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="2e2f0-177">固定価格の契約品目では、この値は定期的な課金のマイルストーンを生成する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="2e2f0-178">**上限**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="2e2f0-179">ユーザーはこのフィールドを編集することができ、請求方法が時間と材料に設定されているプロジェクト ベースの契約品目でのみ利用可能です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="2e2f0-180">ユーザーはこのフィールドを編集できます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-180">The user can edit this field.</span></span> <span data-ttu-id="2e2f0-181">時間および材料の実績がこの時間および材料の契約品目を参照している場合、実績の金額は契約品目の超過しない限度額と比較して評価されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="2e2f0-182">この評価は、既に支出された金額とコミットされた金額を処理した後に完了します。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="2e2f0-183">**顧客の予算**</span><span class="sxs-lookup"><span data-stu-id="2e2f0-183">**Customer Budget**</span></span> | <span data-ttu-id="2e2f0-184">このフィールドは編集可能であり、契約が見積書から作成された場合、見積書の明細の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="2e2f0-185">このフィールドは情報としてのみ使用され、、ダウンストリームへの影響はありません。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="2e2f0-186">プロジェクト ベースの契約品目の全般タブのオプションで使用する検証ルール</span><span class="sxs-lookup"><span data-stu-id="2e2f0-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="2e2f0-187">ルール 1 : **含まれるタスク** フィールドが空白であるか、**すべてのプロジェクトタスク** に設定されている場合、プロジェクトのすべてのタスクは契約品目に含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="2e2f0-188">ルール 2 : **含まれるタスク** フィールドが空白であるか、**すべてのプロジェクト タスク** に明示的にに設定されている場合、プロジェクトと特定のトランザクション クラスは、プロジェクトベースの契約の 1 つの契約品目にのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="2e2f0-189">ルール 3 : **含まれるタスク** フィールドが空白であるか、**選択されたプロジェクト タスクのみ** に明示的にに設定されている場合、プロジェクトと特定のトランザクション クラスは、契約の複数のプロジェクト ベースの契約品目に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="2e2f0-190">
                    <strong>契約書</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2e2f0-191">
                    <strong>契約品目</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2e2f0-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="2e2f0-193">
                    <strong>含まれるタスク</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2e2f0-194">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2e2f0-195">
                    <strong>経費を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2e2f0-196">
                    <strong>材料を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2e2f0-197">
                    <strong>参照項目</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2e2f0-198">
                    <strong>料金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="2e2f0-199">
                    <strong>有効/無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="2e2f0-200">
                    <strong>理由</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e2f0-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-201">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-202">CL1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-203">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-204">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-205">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-206">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-207">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-208">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-209">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-210">ルール #2 に違反。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-210">Violation of Rule #2.</span></span> <span data-ttu-id="2e2f0-211">P1 プロジェクトの時間、経費、材料、および手数料は、契約行 CL1 と CL2 の両方に含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-212">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-213">CL2</span><span class="sxs-lookup"><span data-stu-id="2e2f0-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-214">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-215">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-216">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-217">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-218">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-219">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-220">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-221">CL1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-222">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-223">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-224">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-225">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-226">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-227">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-228">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-229">ルール #2 に違反。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-229">Violation of Rule #2.</span></span> <span data-ttu-id="2e2f0-230">P1 プロジェクトの時間、材料、および手数料は、契約行 CL1 と CL2 の両方に含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-231">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-232">CL2</span><span class="sxs-lookup"><span data-stu-id="2e2f0-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-233">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-234">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-235">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-236">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-237">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-238">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-239">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-240">CL1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-241">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-242">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-243">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-244">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-245">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-246">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-247">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-248">P1 プロジェクトの時間、材料、および手数料は CL1 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="2e2f0-249">P1 プロジェクトの経費は CL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="2e2f0-250">各契約行に含まれているものに重複がないため、有効です。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-251">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-252">CL2</span><span class="sxs-lookup"><span data-stu-id="2e2f0-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-253">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-254">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-255">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-256">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-257">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-258">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-259">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-260">CL1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-261">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-262">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="2e2f0-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-263">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-264">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-265">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-266">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-267">無効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-268">ルール #2 に違反</span><span class="sxs-lookup"><span data-stu-id="2e2f0-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="2e2f0-269">C1 には、プロジェクト P1 のタスクのサブセットに関する時間、材料、経費、および手数料が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2e2f0-270">CL2 には、プロジェクト P1 全体の時間、材料、経費、および手数料が含まれているため、C1 に含まれているものと重複しています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-271">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-272">CL2</span><span class="sxs-lookup"><span data-stu-id="2e2f0-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-273">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-274">空白</span><span class="sxs-lookup"><span data-stu-id="2e2f0-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-275">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-276">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-277">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-278">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-279">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-280">CL1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-281">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-282">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="2e2f0-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-283">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-284">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-285">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-286">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-287">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e2f0-288">ルール #3 による</span><span class="sxs-lookup"><span data-stu-id="2e2f0-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="2e2f0-289">C1 には、プロジェクト P1 のタスクのサブセットに関する時間、手数料、材料、経費、および手数料が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2e2f0-290">CL2 には、プロジェクト P1 のタスクのサブセットに対する時間、手数料、材料、経費、および手数料が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2e2f0-291">唯一の追加の検証は、CL1 のタスクのサブセットが、CL2 のタスクのサブセットとは異なり、重複がないことを確認することです。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="2e2f0-292">これは、タスクが関連付けられたときにシステムによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="2e2f0-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2e2f0-293">C1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2e2f0-294">CL2</span><span class="sxs-lookup"><span data-stu-id="2e2f0-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-295">P1</span><span class="sxs-lookup"><span data-stu-id="2e2f0-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2e2f0-296">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="2e2f0-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-297">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e2f0-298">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-299">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e2f0-300">有効</span><span class="sxs-lookup"><span data-stu-id="2e2f0-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
