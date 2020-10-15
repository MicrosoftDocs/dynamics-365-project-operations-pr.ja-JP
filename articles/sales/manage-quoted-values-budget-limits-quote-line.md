---
title: プロジェクトベースの見積依頼明細行
description: このトピックは、プロジェクト作業のプロジェクトベースの見積依頼明細行の使用に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906227"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="ab682-103">プロジェクトベースの見積依頼明細行</span><span class="sxs-lookup"><span data-stu-id="ab682-103">Project-based quote lines</span></span>

<span data-ttu-id="ab682-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ab682-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ab682-105">プロジェクトベースの見積依頼明細行は、エンゲージメントに関するプロジェクトの作業の見積もりに役立つように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ab682-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="ab682-106">プロジェクトベースの見積依頼明細行の構造は、次の概念を使用してプロジェクト見積もり用に拡張されています。</span><span class="sxs-lookup"><span data-stu-id="ab682-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="ab682-107">請求方法</span><span class="sxs-lookup"><span data-stu-id="ab682-107">Billing Method</span></span>
- <span data-ttu-id="ab682-108">プロジェクト マッピング</span><span class="sxs-lookup"><span data-stu-id="ab682-108">Project Mapping</span></span>
- <span data-ttu-id="ab682-109">含まれるトランザクション クラス</span><span class="sxs-lookup"><span data-stu-id="ab682-109">Included Transaction classes</span></span>
- <span data-ttu-id="ab682-110">上限</span><span class="sxs-lookup"><span data-stu-id="ab682-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="ab682-111">請求可否の設定</span><span class="sxs-lookup"><span data-stu-id="ab682-111">Chargeability setup</span></span>
- <span data-ttu-id="ab682-112">見積依頼明細行の詳細を使用した見積もり</span><span class="sxs-lookup"><span data-stu-id="ab682-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="ab682-113">見積依頼明細行の顧客</span><span class="sxs-lookup"><span data-stu-id="ab682-113">Quote line Customers</span></span>

<span data-ttu-id="ab682-114">次の表に、プロジェクトベースの見積依頼明細行の**一般**タブのフィールドに関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="ab682-115">これらのフィールドは、プロジェクト作業の詳細な基礎的な見積もりの規準を設定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ab682-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="ab682-116">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="ab682-116">**Field**</span></span> | <span data-ttu-id="ab682-117">**関連性、目的、およびガイダンス**</span><span class="sxs-lookup"><span data-stu-id="ab682-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="ab682-118">**下位への影響**</span><span class="sxs-lookup"><span data-stu-id="ab682-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ab682-119">件名</span><span class="sxs-lookup"><span data-stu-id="ab682-119">Name</span></span> | <span data-ttu-id="ab682-120">見積もられている見積もりの個別のコンポーネントを識別するのに役立つ見積依頼明細行の名前。</span><span class="sxs-lookup"><span data-stu-id="ab682-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="ab682-121">見積もりをが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-122">請求方法</span><span class="sxs-lookup"><span data-stu-id="ab682-122">Billing Method</span></span> | <span data-ttu-id="ab682-123">営業案件から作成された見積もりでは、この値は営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="ab682-124">このフィールドには、Dynamics 365 Project Operations でサポートされている 2 つの主要な契約モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab682-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="ab682-125">- 固定価格</span><span class="sxs-lookup"><span data-stu-id="ab682-125">- Fixed price</span></span></br><span data-ttu-id="ab682-126">- 時間と材料。</span><span class="sxs-lookup"><span data-stu-id="ab682-126">- Time and material.</span></span>| <span data-ttu-id="ab682-127">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-128">Project</span><span class="sxs-lookup"><span data-stu-id="ab682-128">Project</span></span> | <span data-ttu-id="ab682-129">このオプションのフィールドを使用して、このエンゲージメントの作業を提供するために使用されるプロジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="ab682-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="ab682-130">プロジェクトが見積依頼明細行にマップされると、請求可能タスクを設定したり、プロジェクトベースの見積もりを見積依頼明細行の詳細として見積依頼明細行に取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="ab682-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="ab682-131">プロジェクトがプロジェクトベースの見積依頼明細行にマップされていない場合は、各見積依頼明細行の詳細を作成して、見積もりを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab682-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="ab682-132">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-133">時間を含む</span><span class="sxs-lookup"><span data-stu-id="ab682-133">Include Time</span></span> | <span data-ttu-id="ab682-134">**はい**/**いいえ**のフラグは、選択したプロジェクトの時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ab682-135">**いいえ**の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ab682-136">**はい**の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ab682-137">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-138">経費を含む</span><span class="sxs-lookup"><span data-stu-id="ab682-138">Include Expense</span></span> | <span data-ttu-id="ab682-139">**はい**/**いいえ**のフラグは、選択したプロジェクトの経費がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ab682-140">**いいえ**の値は、経費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ab682-141">**はい**の値は、経費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ab682-142">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-143">料金を含む</span><span class="sxs-lookup"><span data-stu-id="ab682-143">Include Fee</span></span> | <span data-ttu-id="ab682-144">**はい**/**いいえ**のフラグは、選択したプロジェクトの料金がこの見積依頼明細行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ab682-145">**いいえ**の値は、料金がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ab682-146">**はい**の値は、料金がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="ab682-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ab682-147">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-148">見積もり金額</span><span class="sxs-lookup"><span data-stu-id="ab682-148">Quoted Amount</span></span> | <span data-ttu-id="ab682-149">これは、このプロジェクトベースの見積依頼明細行で予測されるすべての作業について顧客に見積もられる金額です。</span><span class="sxs-lookup"><span data-stu-id="ab682-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="ab682-150">営業案件から作成された見積もりでは、この値は営業案件品目の**顧客予算**フィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="ab682-151">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の金額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="ab682-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="ab682-152">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-153">予測税額</span><span class="sxs-lookup"><span data-stu-id="ab682-153">Estimated Tax</span></span> | <span data-ttu-id="ab682-154">これは、ユーザーが見積依頼明細行に推定税額を追加するための編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="ab682-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="ab682-155">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の税額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="ab682-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="ab682-156">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-157">税引き後の見積もり金額</span><span class="sxs-lookup"><span data-stu-id="ab682-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="ab682-158">このフィールドは税引き後の見積依頼明細行の金額であり、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="ab682-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="ab682-159">このフィールドの金額は*見積もり金額+税*として計算されます。</span><span class="sxs-lookup"><span data-stu-id="ab682-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="ab682-160">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-161">上限</span><span class="sxs-lookup"><span data-stu-id="ab682-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="ab682-162">このフィールドは編集可能であり、**時間と材料**請求方法があるプロジェクトベースの見積依頼明細行でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab682-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="ab682-163">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ab682-164">顧客の予算</span><span class="sxs-lookup"><span data-stu-id="ab682-164">Customer Budget</span></span> | <span data-ttu-id="ab682-165">このフィールドは編集可能であり、営業案件から見積もりが作成されると、営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="ab682-166">このフィールドの値は、見積もりが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ab682-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="ab682-167">プロジェクトベースの見積依頼明細行の全般タブのフィールドの検証ルール</span><span class="sxs-lookup"><span data-stu-id="ab682-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="ab682-168">**ルール 1**: 選択したプロジェクトの特定のトランザクション クラスは、見積もりの 1 つのプロジェクトベースの見積依頼明細行にのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ab682-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="ab682-169">**ルール 2**: 営業案件に複数の見積もりがある場合、すべてが同じプロジェクトを参照し、同じトランザクション クラスを含む異なる見積もりからの見積依頼明細行が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab682-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="ab682-170">**ルール 3**: 見積もりが同じ営業案件に属していない場合、同じプロジェクトとトランザクション クラスを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ab682-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="ab682-171">
                    <strong>営業案件</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="ab682-172">
                    <strong>見積もり</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ab682-173">
                    <strong>見積依頼明細行</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ab682-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ab682-175">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ab682-176">
                    <strong>経費を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ab682-177">
                    <strong>含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="ab682-178">
                    <strong>料金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="ab682-179">
                    <strong>有効/無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="ab682-180">
                    <strong>理由</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab682-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-181">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-182">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-183">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-184">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-185">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-186">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-187">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-188">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-189">ルール #1 に違反。</span><span class="sxs-lookup"><span data-stu-id="ab682-189">Violation of Rule #1.</span></span> <span data-ttu-id="ab682-190">P1 プロジェクトの時間、経費、および料金は、QL1 および QL2 の両方の見積依頼明細行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab682-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-191">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-192">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-193">QL2</span><span class="sxs-lookup"><span data-stu-id="ab682-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-194">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-195">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-196">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-197">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-197">Yes</span></span> </p>
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
<span data-ttu-id="ab682-198">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-199">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-200">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-201">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-202">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-203">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-204">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-205">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-206">ルール #1 に違反。</span><span class="sxs-lookup"><span data-stu-id="ab682-206">Violation of Rule #1.</span></span> <span data-ttu-id="ab682-207">P1 プロジェクトの時間および料金は、QL1 および QL2 の両方の見積依頼明細行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab682-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-208">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-209">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-210">QL2</span><span class="sxs-lookup"><span data-stu-id="ab682-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-211">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-212">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-213">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-214">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-214">Yes</span></span> </p>
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
<span data-ttu-id="ab682-215">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-216">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-217">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-218">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-219">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-220">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-221">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-222">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="ab682-223">P1 プロジェクトの時間および料金は QL1 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab682-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="ab682-224">P1 プロジェクトの経費は QL2 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab682-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="ab682-225">各見積依頼明細行に含まれている内容に重複がないため、有効です。</span><span class="sxs-lookup"><span data-stu-id="ab682-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-226">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-227">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-228">QL2</span><span class="sxs-lookup"><span data-stu-id="ab682-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-229">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-230">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-231">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-232">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-232">No</span></span> </p>
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
<span data-ttu-id="ab682-233">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-234">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-235">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-236">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-237">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-238">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-239">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-240">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-241">上記のルール #1 に違反</span><span class="sxs-lookup"><span data-stu-id="ab682-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="ab682-242">Q1 には、プロジェクト P1 全体の時間、費用、および料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ab682-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ab682-243">QL2 には、プロジェクト P1 全体の時間、経費、および料金が含まれており、Q1 に含まれているものと重複しています。</span><span class="sxs-lookup"><span data-stu-id="ab682-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-244">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-245">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-246">QL2</span><span class="sxs-lookup"><span data-stu-id="ab682-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-247">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-248">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-249">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-250">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-250">Yes</span></span> </p>
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
<span data-ttu-id="ab682-251">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-252">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-253">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-254">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-255">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-256">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-257">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ab682-258">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-259">ルール #2 に基づいて、Q1 と Q2 は同じ営業案件の 2 つの見積もりであるため、両方ともプロジェクトの同じコンポーネントを見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="ab682-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-260">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-261">Q2</span><span class="sxs-lookup"><span data-stu-id="ab682-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-262">Q2 の QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-263">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-264">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-265">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-266">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-266">Yes</span></span> </p>
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
<span data-ttu-id="ab682-267">O1</span><span class="sxs-lookup"><span data-stu-id="ab682-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-268">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-269">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-270">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-271">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-272">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-273">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ab682-274">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab682-275">ルール #3 に基づくと、Q1 と Q2 は異なる営業案件の 2 つの見積もりであるため、同じプロジェクトの同じコンポーネントを見積もることはできません。</span><span class="sxs-lookup"><span data-stu-id="ab682-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ab682-276">O2</span><span class="sxs-lookup"><span data-stu-id="ab682-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ab682-277">Q1</span><span class="sxs-lookup"><span data-stu-id="ab682-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-278">QL1</span><span class="sxs-lookup"><span data-stu-id="ab682-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-279">P1</span><span class="sxs-lookup"><span data-stu-id="ab682-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-280">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ab682-281">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ab682-282">有効</span><span class="sxs-lookup"><span data-stu-id="ab682-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ab682-283">無効</span><span class="sxs-lookup"><span data-stu-id="ab682-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

