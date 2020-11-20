---
title: プロジェクトベースの見積依頼明細行の概要 (ライト)
description: このトピックは、プロジェクト作業のプロジェクトベースの見積依頼明細行の使用に関する情報を提供します。 (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181098"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="d449b-104">プロジェクトベースの見積依頼明細行の概要 (ライト)</span><span class="sxs-lookup"><span data-stu-id="d449b-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="d449b-105">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="d449b-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d449b-106">プロジェクトベースの見積依頼明細行は、エンゲージメントに関するプロジェクトの作業の見積もりに役立つように設計されています。</span><span class="sxs-lookup"><span data-stu-id="d449b-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d449b-107">プロジェクトベースの見積依頼明細行の構造は、次の概念を使用してプロジェクト見積もり用に拡張されています。</span><span class="sxs-lookup"><span data-stu-id="d449b-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d449b-108">請求方法</span><span class="sxs-lookup"><span data-stu-id="d449b-108">Billing Method</span></span>
- <span data-ttu-id="d449b-109">プロジェクトとタスク マッピング</span><span class="sxs-lookup"><span data-stu-id="d449b-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d449b-110">含まれるトランザクション クラス</span><span class="sxs-lookup"><span data-stu-id="d449b-110">Included Transaction classes</span></span>
- <span data-ttu-id="d449b-111">上限</span><span class="sxs-lookup"><span data-stu-id="d449b-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d449b-112">請求可否の設定</span><span class="sxs-lookup"><span data-stu-id="d449b-112">Chargeability setup</span></span>
- <span data-ttu-id="d449b-113">見積依頼明細行の詳細を使用した見積もり</span><span class="sxs-lookup"><span data-stu-id="d449b-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d449b-114">見積依頼明細行の顧客</span><span class="sxs-lookup"><span data-stu-id="d449b-114">Quote line Customers</span></span>

<span data-ttu-id="d449b-115">次の表に、プロジェクトベースの見積依頼明細行の **一般** タブのフィールドに関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d449b-116">これらのフィールドは、プロジェクト作業の詳細な基礎的な見積もりの規準を設定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d449b-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d449b-117">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="d449b-117">**Field**</span></span> | <span data-ttu-id="d449b-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="d449b-118">**Description**</span></span> | <span data-ttu-id="d449b-119">**下流への影響**</span><span class="sxs-lookup"><span data-stu-id="d449b-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d449b-120">件名</span><span class="sxs-lookup"><span data-stu-id="d449b-120">Name</span></span> | <span data-ttu-id="d449b-121">見積もられている見積もりの個別のコンポーネントを識別するのに役立つ見積依頼明細行の名前。</span><span class="sxs-lookup"><span data-stu-id="d449b-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d449b-122">見積もりをが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-123">請求方法</span><span class="sxs-lookup"><span data-stu-id="d449b-123">Billing Method</span></span> | <span data-ttu-id="d449b-124">営業案件から作成された見積もりでは、この値は営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d449b-125">このフィールドには、Dynamics 365 Project Operations でサポートされている 2 つの主要な契約モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d449b-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d449b-126">- 固定価格</span><span class="sxs-lookup"><span data-stu-id="d449b-126">- Fixed price</span></span></br><span data-ttu-id="d449b-127">- 時間と材料。</span><span class="sxs-lookup"><span data-stu-id="d449b-127">- Time and material.</span></span>| <span data-ttu-id="d449b-128">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-129">Project</span><span class="sxs-lookup"><span data-stu-id="d449b-129">Project</span></span> | <span data-ttu-id="d449b-130">このオプションのフィールドを使用して、このエンゲージメントの作業を提供するために使用されるプロジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="d449b-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d449b-131">プロジェクトが見積依頼明細行にマップされると、請求可能タスクを設定したり、プロジェクトベースの見積もりを見積依頼明細行の詳細として見積依頼明細行に取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="d449b-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d449b-132">プロジェクトがプロジェクトベースの見積依頼明細行にマップされていない場合は、各見積依頼明細行の詳細を作成して、見積もりを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d449b-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d449b-133">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d449b-134">含まれるタスク</span><span class="sxs-lookup"><span data-stu-id="d449b-134">Included Tasks</span></span> | <span data-ttu-id="d449b-135">この見積依頼明細行が、選択したプロジェクトのすべてまたは一部のプロジェクト タスクに使用されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d449b-136">このフィールドには以下の指定できる値が入ります。</span><span class="sxs-lookup"><span data-stu-id="d449b-136">This field has the following possible values:</span></span></br><span data-ttu-id="d449b-137">- すべてのプロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="d449b-137">- All project tasks</span></span></br><span data-ttu-id="d449b-138">- 選択したプロジェクト タスクのみ</span><span class="sxs-lookup"><span data-stu-id="d449b-138">- Selected project tasks only</span></span></br><span data-ttu-id="d449b-139">このフィールドの空白の値は、**すべてのプロジェクト タスク** オプションに相当します。</span><span class="sxs-lookup"><span data-stu-id="d449b-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d449b-140">**選択したプロジェクト タスクのみ** が選択され、プロジェクト ページで、**タスクの請求の設定** タブでは、特定のタスクを選択して、それらをこの見積依頼明細行に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d449b-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d449b-141">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-142">時間を含む</span><span class="sxs-lookup"><span data-stu-id="d449b-142">Include Time</span></span> | <span data-ttu-id="d449b-143">**はい**/**いいえ** のフラグは、選択したプロジェクトの時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d449b-144">**いいえ** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d449b-145">**はい** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d449b-146">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-147">経費を含む</span><span class="sxs-lookup"><span data-stu-id="d449b-147">Include Expense</span></span> | <span data-ttu-id="d449b-148">**はい**/**いいえ** のフラグは、選択したプロジェクトの経費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d449b-149">**いいえ** の値は、経費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d449b-150">**はい** の値は、経費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d449b-151">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-152">料金を含む</span><span class="sxs-lookup"><span data-stu-id="d449b-152">Include Fee</span></span> | <span data-ttu-id="d449b-153">**はい**/**いいえ** のフラグは、選択したプロジェクトの料金がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d449b-154">**いいえ** の値は、料金がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d449b-155">**はい** の値は、料金がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="d449b-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d449b-156">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-157">見積もり金額</span><span class="sxs-lookup"><span data-stu-id="d449b-157">Quoted Amount</span></span> | <span data-ttu-id="d449b-158">これは、このプロジェクトベースの見積依頼明細行で予測されるすべての作業について顧客に見積もられる金額です。</span><span class="sxs-lookup"><span data-stu-id="d449b-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d449b-159">営業案件から作成された見積もりでは、この値は営業案件品目の **顧客予算** フィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d449b-160">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の金額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="d449b-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d449b-161">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-162">予測税額</span><span class="sxs-lookup"><span data-stu-id="d449b-162">Estimated Tax</span></span> | <span data-ttu-id="d449b-163">これは、ユーザーが見積依頼明細行に推定税額を追加するための編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="d449b-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d449b-164">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の税額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="d449b-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d449b-165">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-166">税引き後の見積もり金額</span><span class="sxs-lookup"><span data-stu-id="d449b-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d449b-167">このフィールドは税引き後の見積依頼明細行の金額であり、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="d449b-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d449b-168">このフィールドの金額は *見積もり金額+税* として計算されます。</span><span class="sxs-lookup"><span data-stu-id="d449b-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d449b-169">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-170">上限</span><span class="sxs-lookup"><span data-stu-id="d449b-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d449b-171">このフィールドは編集可能であり、**時間と材料** 請求方法があるプロジェクトベースの見積依頼明細行でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d449b-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d449b-172">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d449b-173">顧客の予算</span><span class="sxs-lookup"><span data-stu-id="d449b-173">Customer Budget</span></span> | <span data-ttu-id="d449b-174">このフィールドは編集可能であり、営業案件から見積もりが作成されると、営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d449b-175">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d449b-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d449b-176">プロジェクトベースの見積依頼明細行の全般タブのフィールドの検証ルール</span><span class="sxs-lookup"><span data-stu-id="d449b-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d449b-177">**ルール 1**: **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトは見積依頼明細行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="d449b-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="d449b-178">**ルール 2**: **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの 1 つのプロジェクトベースの見積依頼明細行にのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d449b-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d449b-179">**ルール 3**: **含まれるタスク** フィールドが **選択したプロジェクト タスクのみ** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの複数のプロジェクトベースの見積依頼明細行に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d449b-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d449b-180">**ルール 4**: 営業案件に複数の見積もりがある場合、すべてが同じプロジェクトを参照し、同じトランザクション クラスを含む異なる見積もりからの見積依頼明細行が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d449b-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d449b-181">**ルール 5**: 見積もりが同じ営業案件に属していない場合、同じプロジェクトとトランザクション クラスを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d449b-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d449b-182">
                    <strong>営業案件</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d449b-183">
                    <strong>見積もり</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d449b-184">
                    <strong>見積依頼明細行</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d449b-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d449b-186">
                    <strong>含まれるタスク</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d449b-187">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d449b-188">
                    <strong>経費を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d449b-189">
                    <strong>含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d449b-190">
                    <strong>料金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d449b-191">
                    <strong>有効/無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d449b-192">
                    <strong>理由</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d449b-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-193">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-194">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-196">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-197">空</span><span class="sxs-lookup"><span data-stu-id="d449b-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-198">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-199">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-200">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-201">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-202">ルール #2 に違反。</span><span class="sxs-lookup"><span data-stu-id="d449b-202">Violation of Rule #2.</span></span> <span data-ttu-id="d449b-203">P1 プロジェクトの時間、経費、および料金は、見積依頼明細行 QL1 および QL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="d449b-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-204">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-205">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d449b-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-207">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-208">空</span><span class="sxs-lookup"><span data-stu-id="d449b-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-209">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-210">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-211">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-212">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-213">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-215">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-216">空</span><span class="sxs-lookup"><span data-stu-id="d449b-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-217">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-218">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-219">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-220">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-221">ルール #2 に違反。</span><span class="sxs-lookup"><span data-stu-id="d449b-221">Violation of Rule #2.</span></span> <span data-ttu-id="d449b-222">P1 プロジェクトの時間および料金は、見積依頼明細行 QL1 および QL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="d449b-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-223">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-224">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d449b-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-226">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-227">空</span><span class="sxs-lookup"><span data-stu-id="d449b-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-228">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-229">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-230">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-231">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-232">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-234">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-235">空</span><span class="sxs-lookup"><span data-stu-id="d449b-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-236">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-237">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-238">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-239">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d449b-240">P1 プロジェクトの時間および料金は QL1 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="d449b-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d449b-241">P1 プロジェクトの経費は QL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="d449b-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d449b-242">各見積依頼明細行に含まれているものに重複はなく、有効です。</span><span class="sxs-lookup"><span data-stu-id="d449b-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-243">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-244">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d449b-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-246">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-247">空</span><span class="sxs-lookup"><span data-stu-id="d449b-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-248">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-249">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-250">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-251">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-252">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-254">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-255">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d449b-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-256">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-257">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-258">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-259">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-260">上記のルール #2 に違反</span><span class="sxs-lookup"><span data-stu-id="d449b-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d449b-261">Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、経費、および料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d449b-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d449b-262">QL2 には、プロジェクト P1 全体の時間、経費、および料金が含まれており、Q1 に含まれているものと重複しています。</span><span class="sxs-lookup"><span data-stu-id="d449b-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-263">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-264">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d449b-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-266">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-267">空</span><span class="sxs-lookup"><span data-stu-id="d449b-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-268">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-269">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-270">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-271">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-272">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-274">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-275">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d449b-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-276">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-277">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-278">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-279">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-280">上記のルール #3 に従い、</span><span class="sxs-lookup"><span data-stu-id="d449b-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d449b-281">Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、経費、および料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d449b-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d449b-282">QL2 には、プロジェクト P1 のタスクのサブセットに関する時間、経費、および料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d449b-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d449b-283">唯一の追加の検証は、QL2 のタスクのサブセットとは異なる QL1 のタスクのサブセットに関するものです。</span><span class="sxs-lookup"><span data-stu-id="d449b-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d449b-284">これにより、重複がなくなります。</span><span class="sxs-lookup"><span data-stu-id="d449b-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d449b-285">これは、タスクが関連付けられたときにシステムによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="d449b-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-286">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-287">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d449b-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-289">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-290">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="d449b-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-291">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-292">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-293">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-294">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-295">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-297">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-298">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="d449b-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-299">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-300">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-301">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d449b-302">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-303">ルール #5 に基づいて、Q1 と Q2 は同じ営業案件の 2 つの見積もりであるため、両方ともプロジェクトの同じコンポーネントを見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="d449b-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-304">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-305">Q2</span><span class="sxs-lookup"><span data-stu-id="d449b-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-307">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-308">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="d449b-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-309">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-310">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-311">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-312">O1</span><span class="sxs-lookup"><span data-stu-id="d449b-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-313">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-315">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-316">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="d449b-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-317">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-318">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-319">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d449b-320">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d449b-321">ルール #4 に基づいて、Q1 と Q2 は異なる営業案件の 2 つの見積もりであるため、両方が同じプロジェクトの同じコンポーネントを見積もることはできません。</span><span class="sxs-lookup"><span data-stu-id="d449b-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d449b-322">O2</span><span class="sxs-lookup"><span data-stu-id="d449b-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d449b-323">Q1</span><span class="sxs-lookup"><span data-stu-id="d449b-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d449b-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-325">P1</span><span class="sxs-lookup"><span data-stu-id="d449b-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d449b-326">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="d449b-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-327">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d449b-328">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d449b-329">有効</span><span class="sxs-lookup"><span data-stu-id="d449b-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d449b-330">無効</span><span class="sxs-lookup"><span data-stu-id="d449b-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

