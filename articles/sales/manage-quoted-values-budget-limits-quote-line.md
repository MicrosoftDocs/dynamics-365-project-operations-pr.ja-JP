---
title: プロジェクト見積依頼明細行の概要
description: このトピックは、プロジェクト作業にからプロジェクトの見積依頼明細行を使用する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858029"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="6d46d-103">プロジェクト見積依頼明細行の概要</span><span class="sxs-lookup"><span data-stu-id="6d46d-103">Project quote lines overview</span></span>

<span data-ttu-id="6d46d-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6d46d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6d46d-105">プロジェクトベースの見積依頼明細行は、エンゲージメントに関するプロジェクトの作業の見積もりに役立つように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6d46d-106">プロジェクトベースの見積依頼明細行の構造は、次の概念を使用してプロジェクト見積もり用に拡張されています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6d46d-107">請求方法</span><span class="sxs-lookup"><span data-stu-id="6d46d-107">Billing Method</span></span>
- <span data-ttu-id="6d46d-108">プロジェクト マッピング</span><span class="sxs-lookup"><span data-stu-id="6d46d-108">Project Mapping</span></span>
- <span data-ttu-id="6d46d-109">含まれるトランザクション クラス</span><span class="sxs-lookup"><span data-stu-id="6d46d-109">Included Transaction classes</span></span>
- <span data-ttu-id="6d46d-110">上限</span><span class="sxs-lookup"><span data-stu-id="6d46d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6d46d-111">請求可否の設定</span><span class="sxs-lookup"><span data-stu-id="6d46d-111">Chargeability setup</span></span>
- <span data-ttu-id="6d46d-112">見積依頼明細行の詳細を使用した見積もり</span><span class="sxs-lookup"><span data-stu-id="6d46d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6d46d-113">見積依頼明細行の顧客</span><span class="sxs-lookup"><span data-stu-id="6d46d-113">Quote line Customers</span></span>

<span data-ttu-id="6d46d-114">次の表に、プロジェクトベースの見積依頼明細行の **一般** タブのフィールドに関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6d46d-115">これらのフィールドは、プロジェクト作業の詳細な基礎的な見積もりの規準を設定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6d46d-116">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="6d46d-116">**Field**</span></span> | <span data-ttu-id="6d46d-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d46d-117">**Description**</span></span> | <span data-ttu-id="6d46d-118">**下流への影響**</span><span class="sxs-lookup"><span data-stu-id="6d46d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6d46d-119">件名</span><span class="sxs-lookup"><span data-stu-id="6d46d-119">Name</span></span> | <span data-ttu-id="6d46d-120">見積もられている見積もりの個別のコンポーネントを識別するのに役立つ見積依頼明細行の名前。</span><span class="sxs-lookup"><span data-stu-id="6d46d-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6d46d-121">見積もりをが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-122">請求方法</span><span class="sxs-lookup"><span data-stu-id="6d46d-122">Billing Method</span></span> | <span data-ttu-id="6d46d-123">営業案件から作成された見積もりでは、この値は営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6d46d-124">このフィールドには、Dynamics 365 Project Operations によってサポートされる 2 つの主要な契約モデルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6d46d-125">- 固定価格</span><span class="sxs-lookup"><span data-stu-id="6d46d-125">- Fixed price</span></span></br><span data-ttu-id="6d46d-126">- 時間と材料。</span><span class="sxs-lookup"><span data-stu-id="6d46d-126">- Time and material.</span></span>| <span data-ttu-id="6d46d-127">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-128">Project</span><span class="sxs-lookup"><span data-stu-id="6d46d-128">Project</span></span> | <span data-ttu-id="6d46d-129">このオプションのフィールドを使用して、このエンゲージメントの作業を提供するために使用されるプロジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6d46d-130">プロジェクトが見積依頼明細行にマップされると、請求可能タスクを設定したり、プロジェクトベースの見積もりを見積依頼明細行の詳細として見積依頼明細行に取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6d46d-131">プロジェクトがプロジェクトベースの見積依頼明細行にマップされていない場合は、各見積依頼明細行の詳細を作成して、見積もりを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d46d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6d46d-132">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-133">時間を含む</span><span class="sxs-lookup"><span data-stu-id="6d46d-133">Include Time</span></span> | <span data-ttu-id="6d46d-134">**はい**/**いいえ** のフラグは、選択したプロジェクトの時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6d46d-135">**いいえ** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6d46d-136">**はい** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6d46d-137">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-138">経費を含む</span><span class="sxs-lookup"><span data-stu-id="6d46d-138">Include Expense</span></span> | <span data-ttu-id="6d46d-139">**はい**/**いいえ** のフラグは、選択したプロジェクトの経費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6d46d-140">**いいえ** の値は、経費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6d46d-141">**はい** の値は、経費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6d46d-142">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-143">料金を含む</span><span class="sxs-lookup"><span data-stu-id="6d46d-143">Include Fee</span></span> | <span data-ttu-id="6d46d-144">**はい**/**いいえ** のフラグは、選択したプロジェクトの料金がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6d46d-145">**いいえ** の値は、料金がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6d46d-146">**はい** の値は、料金がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="6d46d-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6d46d-147">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-148">見積もり金額</span><span class="sxs-lookup"><span data-stu-id="6d46d-148">Quoted Amount</span></span> | <span data-ttu-id="6d46d-149">これは、このプロジェクトベースの見積依頼明細行で予測されるすべての作業について顧客に見積もられる金額です。</span><span class="sxs-lookup"><span data-stu-id="6d46d-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6d46d-150">営業案件から作成された見積もりでは、この値は営業案件品目の **顧客予算** フィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6d46d-151">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の金額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6d46d-152">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-153">予測税額</span><span class="sxs-lookup"><span data-stu-id="6d46d-153">Estimated Tax</span></span> | <span data-ttu-id="6d46d-154">これは、ユーザーが見積依頼明細行に推定税額を追加するための編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="6d46d-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6d46d-155">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の税額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6d46d-156">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-157">税引き後の見積もり金額</span><span class="sxs-lookup"><span data-stu-id="6d46d-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="6d46d-158">このフィールドは税引き後の見積依頼明細行の金額であり、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="6d46d-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6d46d-159">このフィールドの金額は *見積もり金額+税* として計算されます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6d46d-160">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-161">上限</span><span class="sxs-lookup"><span data-stu-id="6d46d-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="6d46d-162">このフィールドは編集可能であり、**時間と材料** 請求方法があるプロジェクトベースの見積依頼明細行でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6d46d-163">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6d46d-164">顧客の予算</span><span class="sxs-lookup"><span data-stu-id="6d46d-164">Customer Budget</span></span> | <span data-ttu-id="6d46d-165">このフィールドは編集可能であり、営業案件から見積もりが作成されると、営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6d46d-166">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6d46d-167">プロジェクトベースの見積依頼明細行の全般タブのフィールドの検証ルール</span><span class="sxs-lookup"><span data-stu-id="6d46d-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6d46d-168">**ルール 1**: 選択したプロジェクトの特定のトランザクション クラスは、見積もりの 1 つのプロジェクトベースの見積依頼明細行にのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6d46d-169">**ルール 2**: 営業案件に複数の見積もりがある場合、すべてが同じプロジェクトを参照し、同じトランザクション クラスを含む異なる見積もりからの見積依頼明細行が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6d46d-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6d46d-170">**ルール 3**: 見積もりが同じ営業案件に属していない場合、同じプロジェクトとトランザクション クラスを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6d46d-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6d46d-171">
                    <strong>営業案件</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6d46d-172">
                    <strong>見積もり</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6d46d-173">
                    <strong>見積依頼明細行</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6d46d-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6d46d-175">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6d46d-176">
                    <strong>経費を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6d46d-177">
                    <strong>含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6d46d-178">
                    <strong>料金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6d46d-179">
                    <strong>有効/無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6d46d-180">
                    <strong>理由</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d46d-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-181">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-182">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-183">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-184">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-185">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-186">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-187">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-188">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-189">ルール #1 に違反。</span><span class="sxs-lookup"><span data-stu-id="6d46d-189">Violation of Rule #1.</span></span> <span data-ttu-id="6d46d-190">P1 プロジェクトの時間、経費、および料金は、QL1 および QL2 の両方の見積依頼明細行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-191">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-192">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-193">QL2</span><span class="sxs-lookup"><span data-stu-id="6d46d-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-194">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-195">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-196">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-197">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-197">Yes</span></span> </p>
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
<span data-ttu-id="6d46d-198">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-199">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-201">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-202">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-203">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-204">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-205">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-206">ルール #1 に違反。</span><span class="sxs-lookup"><span data-stu-id="6d46d-206">Violation of Rule #1.</span></span> <span data-ttu-id="6d46d-207">P1 プロジェクトの時間および料金は、QL1 および QL2 の両方の見積依頼明細行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-208">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-209">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-210">QL2</span><span class="sxs-lookup"><span data-stu-id="6d46d-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-211">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-212">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-213">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-214">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-214">Yes</span></span> </p>
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
<span data-ttu-id="6d46d-215">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-216">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-217">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-218">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-219">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-220">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-221">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-222">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="6d46d-223">P1 プロジェクトの時間および料金は QL1 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6d46d-224">P1 プロジェクトの経費は QL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6d46d-225">各見積依頼明細行に含まれている内容に重複がないため、有効です。</span><span class="sxs-lookup"><span data-stu-id="6d46d-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-226">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-227">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-228">QL2</span><span class="sxs-lookup"><span data-stu-id="6d46d-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-229">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-230">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-231">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-232">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-232">No</span></span> </p>
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
<span data-ttu-id="6d46d-233">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-234">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-235">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-236">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-237">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-238">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-239">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-240">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-241">上記のルール #1 に違反</span><span class="sxs-lookup"><span data-stu-id="6d46d-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="6d46d-242">Q1 には、プロジェクト P1 全体の時間、費用、および料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6d46d-243">QL2 には、プロジェクト P1 全体の時間、経費、および料金が含まれており、Q1 に含まれているものと重複しています。</span><span class="sxs-lookup"><span data-stu-id="6d46d-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-244">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-245">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-246">QL2</span><span class="sxs-lookup"><span data-stu-id="6d46d-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-247">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-248">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-249">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-250">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-250">Yes</span></span> </p>
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
<span data-ttu-id="6d46d-251">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-252">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-254">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-255">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-256">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-257">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6d46d-258">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-259">ルール #2 に基づいて、Q1 と Q2 は同じ営業案件の 2 つの見積もりであるため、両方ともプロジェクトの同じコンポーネントを見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="6d46d-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-260">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-261">Q2</span><span class="sxs-lookup"><span data-stu-id="6d46d-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-262">Q2 の QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-263">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-264">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-265">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-266">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-266">Yes</span></span> </p>
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
<span data-ttu-id="6d46d-267">O1</span><span class="sxs-lookup"><span data-stu-id="6d46d-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-268">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-269">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-270">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-271">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-272">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-273">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6d46d-274">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d46d-275">ルール #3 に基づくと、Q1 と Q2 は異なる営業案件の 2 つの見積もりであるため、同じプロジェクトの同じコンポーネントを見積もることはできません。</span><span class="sxs-lookup"><span data-stu-id="6d46d-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6d46d-276">O2</span><span class="sxs-lookup"><span data-stu-id="6d46d-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6d46d-277">Q1</span><span class="sxs-lookup"><span data-stu-id="6d46d-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-278">QL1</span><span class="sxs-lookup"><span data-stu-id="6d46d-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-279">P1</span><span class="sxs-lookup"><span data-stu-id="6d46d-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-280">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6d46d-281">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6d46d-282">有効</span><span class="sxs-lookup"><span data-stu-id="6d46d-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6d46d-283">無効</span><span class="sxs-lookup"><span data-stu-id="6d46d-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
