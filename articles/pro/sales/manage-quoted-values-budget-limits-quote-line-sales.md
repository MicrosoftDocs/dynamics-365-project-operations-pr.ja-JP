---
title: プロジェクトベースの見積依頼明細行の概要
description: このトピックは、プロジェクト作業のプロジェクトベースの見積依頼明細行の使用に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858704"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="5ca5d-103">プロジェクトベースの見積依頼明細行の概要</span><span class="sxs-lookup"><span data-stu-id="5ca5d-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="5ca5d-104">_**適用対象:** ライト展開 - 見積請求、リソース/非在庫ベースのシナリオ向けの Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5ca5d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5ca5d-105">プロジェクトベースの見積依頼明細行は、エンゲージメントに関するプロジェクトの作業の見積もりに役立つように設計されています。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="5ca5d-106">プロジェクトベースの見積依頼明細行の構造は、次の概念を使用してプロジェクト見積もり用に拡張されています。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="5ca5d-107">請求方法</span><span class="sxs-lookup"><span data-stu-id="5ca5d-107">Billing Method</span></span>
- <span data-ttu-id="5ca5d-108">プロジェクトとタスク マッピング</span><span class="sxs-lookup"><span data-stu-id="5ca5d-108">Project and Task Mapping</span></span>
- <span data-ttu-id="5ca5d-109">含まれるトランザクション クラス</span><span class="sxs-lookup"><span data-stu-id="5ca5d-109">Included Transaction classes</span></span>
- <span data-ttu-id="5ca5d-110">上限</span><span class="sxs-lookup"><span data-stu-id="5ca5d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="5ca5d-111">請求可否の設定</span><span class="sxs-lookup"><span data-stu-id="5ca5d-111">Chargeability setup</span></span>
- <span data-ttu-id="5ca5d-112">見積依頼明細行の詳細を使用した見積もり</span><span class="sxs-lookup"><span data-stu-id="5ca5d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="5ca5d-113">見積依頼明細行の顧客</span><span class="sxs-lookup"><span data-stu-id="5ca5d-113">Quote line Customers</span></span>

<span data-ttu-id="5ca5d-114">次の表に、プロジェクトベースの見積依頼明細行の **一般** タブのフィールドに関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="5ca5d-115">これらのフィールドは、プロジェクト作業の詳細な基礎的な見積もりの規準を設定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="5ca5d-116">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="5ca5d-116">**Field**</span></span> | <span data-ttu-id="5ca5d-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ca5d-117">**Description**</span></span> | <span data-ttu-id="5ca5d-118">**下流への影響**</span><span class="sxs-lookup"><span data-stu-id="5ca5d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5ca5d-119">件名</span><span class="sxs-lookup"><span data-stu-id="5ca5d-119">Name</span></span> | <span data-ttu-id="5ca5d-120">見積もり対象の見積もりの個別のコンポーネントを識別するのに役立つ見積もり行の名前。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="5ca5d-121">見積もりをが受注されると、この見積依頼明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-122">請求方法</span><span class="sxs-lookup"><span data-stu-id="5ca5d-122">Billing Method</span></span> | <span data-ttu-id="5ca5d-123">営業案件から作成された見積もりでは、この値は営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="5ca5d-124">このフィールドには、Dynamics 365 Project Operations によってサポートされる 2 つの主要な契約モデルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="5ca5d-125">- 固定価格</span><span class="sxs-lookup"><span data-stu-id="5ca5d-125">- Fixed price</span></span></br><span data-ttu-id="5ca5d-126">- 時間と材料。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-126">- Time and material.</span></span>| <span data-ttu-id="5ca5d-127">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-128">Project</span><span class="sxs-lookup"><span data-stu-id="5ca5d-128">Project</span></span> | <span data-ttu-id="5ca5d-129">このオプションのフィールドを使用して、このエンゲージメントの作業を提供するために使用されるプロジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="5ca5d-130">プロジェクトが見積依頼明細行にマップされると、請求可能タスクを設定したり、プロジェクトベースの見積もりを見積依頼明細行の詳細として見積依頼明細行に取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="5ca5d-131">プロジェクトがプロジェクトベースの見積依頼明細行にマップされていない場合は、各見積依頼明細行の詳細を作成して、見積もりを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="5ca5d-132">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="5ca5d-133">含まれるタスク</span><span class="sxs-lookup"><span data-stu-id="5ca5d-133">Included Tasks</span></span> | <span data-ttu-id="5ca5d-134">この見積依頼明細行が、選択したプロジェクトのすべてまたは一部のプロジェクト タスクに使用されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="5ca5d-135">このフィールドには以下の指定できる値が入ります。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-135">This field has the following possible values:</span></span></br><span data-ttu-id="5ca5d-136">- すべてのプロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="5ca5d-136">- All project tasks</span></span></br><span data-ttu-id="5ca5d-137">- 選択したプロジェクト タスクのみ</span><span class="sxs-lookup"><span data-stu-id="5ca5d-137">- Selected project tasks only</span></span></br><span data-ttu-id="5ca5d-138">このフィールドの空白の値は、**すべてのプロジェクト タスク** オプションに相当します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="5ca5d-139">プロジェクト ページで **選択したプロジェクト タスクのみ** が選択されている場合、**タスクの請求設定** タブを使用すると、特定のタスクを選択して、それらをこの見積もり行に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="5ca5d-140">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-141">時間を含む</span><span class="sxs-lookup"><span data-stu-id="5ca5d-141">Include Time</span></span> | <span data-ttu-id="5ca5d-142">**はい**/**いいえ** の値は、選択したプロジェクトの時間トランザクションまたは労務費がこの見積もり行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-143">**いいえ** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-144">**はい** の値は、時間トランザクションまたは人件費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5ca5d-145">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-146">経費を含む</span><span class="sxs-lookup"><span data-stu-id="5ca5d-146">Include Expense</span></span> | <span data-ttu-id="5ca5d-147">**はい**/**いいえ** の値は、選択したプロジェクトの経費の原価がこの見積もり行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-148">**いいえ** の値は、経費がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-149">**はい** の値は、経費がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5ca5d-150">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-151">材料を含む</span><span class="sxs-lookup"><span data-stu-id="5ca5d-151">Include Material</span></span> | <span data-ttu-id="5ca5d-152">**はい**/**いいえ** の値は、選択したプロジェクトの材料の原価がこの見積もり行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-153">**いいえ** の値は、選択したプロジェクトの材料原価がこの見積もり行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-154">**はい** の値は、選択したプロジェクトの材料原価がこの見積もり行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5ca5d-155">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-156">料金を含む</span><span class="sxs-lookup"><span data-stu-id="5ca5d-156">Include Fee</span></span> | <span data-ttu-id="5ca5d-157">**はい**/**いいえ** の値は、選択したプロジェクトの手数料がこの見積もり行の見積もりに含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-158">**いいえ** の値は、料金がこの見積依頼明細行の見積もりに含まれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5ca5d-159">**はい** の値は、料金がこの見積依頼明細行の見積もりに含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5ca5d-160">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-161">見積もり金額</span><span class="sxs-lookup"><span data-stu-id="5ca5d-161">Quoted Amount</span></span> | <span data-ttu-id="5ca5d-162">これは、このプロジェクトベースの見積もり行で予測されるすべての作業について顧客に見積もられる金額です。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="5ca5d-163">営業案件から作成された見積もりでは、この値は営業案件品目の **顧客予算** フィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="5ca5d-164">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の金額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="5ca5d-165">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-166">予測税額</span><span class="sxs-lookup"><span data-stu-id="5ca5d-166">Estimated Tax</span></span> | <span data-ttu-id="5ca5d-167">これは、ユーザーが見積依頼明細行に推定税額を追加するための編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="5ca5d-168">プロジェクトベースの見積依頼明細行に明細行の詳細がある場合、このフィールドは編集用にロックされ、見積依頼明細行の詳細の税額から集計されます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="5ca5d-169">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-170">税引き後の見積もり金額</span><span class="sxs-lookup"><span data-stu-id="5ca5d-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="5ca5d-171">このフィールドは税引き後の見積依頼明細行の金額であり、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="5ca5d-172">このフィールドの金額は *見積もり金額+税* として計算されます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="5ca5d-173">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-174">上限</span><span class="sxs-lookup"><span data-stu-id="5ca5d-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="5ca5d-175">このフィールドは編集可能であり、**時間と材料** 請求方法があるプロジェクトベースの見積依頼明細行でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="5ca5d-176">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5ca5d-177">顧客の予算</span><span class="sxs-lookup"><span data-stu-id="5ca5d-177">Customer Budget</span></span> | <span data-ttu-id="5ca5d-178">このフィールドは編集可能であり、営業案件から見積もりが作成されると、営業案件品目の対応するフィールドからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="5ca5d-179">この値は、見積もりが承認されたときにこの見積明細行から作成されたプロジェクト契約品目にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="5ca5d-180">プロジェクトベースの見積依頼明細行の全般タブのフィールドの検証ルール</span><span class="sxs-lookup"><span data-stu-id="5ca5d-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="5ca5d-181">**ルール 1**: **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトは見積依頼明細行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="5ca5d-182">**ルール 2**: **含まれるタスク** フィールドが空白の場合、または **すべてのプロジェクト タスク** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの 1 つのプロジェクトベースの見積依頼明細行にのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="5ca5d-183">**ルール 3**: **含まれるタスク** フィールドが **選択したプロジェクト タスクのみ** に設定されている場合、プロジェクトと特定のトランザクション クラスは、見積もりの複数のプロジェクトベースの見積依頼明細行に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="5ca5d-184">**ルール 4**: 営業案件に複数の見積もりがある場合、すべてが同じプロジェクトを参照し、同じトランザクション クラスを含む異なる見積もりからの見積依頼明細行が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="5ca5d-185">**ルール 5**: 見積もりが同じ営業案件に属していない場合、同じプロジェクトとトランザクション クラスを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="5ca5d-186">
                    <strong>営業案件</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="5ca5d-187">
                    <strong>見積もり</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="5ca5d-188">
                    <strong>見積依頼明細行</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5ca5d-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="5ca5d-190">
                    <strong>含まれるタスク</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="5ca5d-191">
                    <strong>時間を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="5ca5d-192">
                    <strong>経費を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="5ca5d-193">
                    <strong>材料を含む</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5ca5d-194">
                    <strong>参照項目</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5ca5d-195">
                    <strong>料金</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="5ca5d-196">
                    <strong>有効/無効</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="5ca5d-197">
                    <strong>理由</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ca5d-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-198">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-199">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-201">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-202">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-203">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-204">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-205">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-206">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-207">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-208">ルール #2 に違反。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-208">Violation of Rule #2.</span></span> <span data-ttu-id="5ca5d-209">P1 プロジェクトの時間、経費、および料金は、見積依頼明細行 QL1 および QL2 に含まれています</span><span class="sxs-lookup"><span data-stu-id="5ca5d-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-210">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-211">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-212">QL2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-213">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-214">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-215">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-216">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-217">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-218">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-219">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-220">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-221">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-222">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-223">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-224">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-225">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-226">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-227">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-228">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-229">ルール #2 に違反。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-229">Violation of Rule #2.</span></span> <span data-ttu-id="5ca5d-230">P1 プロジェクトの時間、材料、提供は、見積依頼明細行 QL1 および QL2 に含まれています</span><span class="sxs-lookup"><span data-stu-id="5ca5d-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-231">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-232">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-233">QL2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-234">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-235">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-236">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-237">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-238">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-239">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-240">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-241">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-242">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-243">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-244">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-245">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-246">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-247">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-248">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-249">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-250">P1 プロジェクトの時間、材料、および手数料は QL1 に含まれています</span><span class="sxs-lookup"><span data-stu-id="5ca5d-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="5ca5d-251">P1 プロジェクトの経費は QL2 に含まれています</span><span class="sxs-lookup"><span data-stu-id="5ca5d-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="5ca5d-252">各見積もり行に含まれているものに重複がないため、有効です。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-253">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-254">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-255">QL2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-256">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-257">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-258">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-259">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-260">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-261">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-262">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-263">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-264">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-265">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-266">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="5ca5d-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-267">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-268">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-269">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-270">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-271">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-272">ルール #2 に違反</span><span class="sxs-lookup"><span data-stu-id="5ca5d-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="5ca5d-273">Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、材料、経費、および手数料が含まれています</span><span class="sxs-lookup"><span data-stu-id="5ca5d-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="5ca5d-274">QL2 には、プロジェクト P1 全体の時間、費用、手数料が含まれているため、C1 に含まれるものと重複します。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-275">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-276">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-277">QL2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-278">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-279">空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-280">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-281">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-282">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-283">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-284">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-285">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-286">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-287">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-288">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="5ca5d-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-289">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-290">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-291">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-292">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-293">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-294">ルール #3 により、</span><span class="sxs-lookup"><span data-stu-id="5ca5d-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="5ca5d-295">Q1 には、プロジェクト P1 のタスクのサブセットに関する時間、材料、経費、および手数料が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5ca5d-296">QL2 には、プロジェクト P1 のタスクのサブセットに対する時間、材料、経費、および手数料が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5ca5d-297">唯一の追加の検証は、CL1 のタスクのサブセットが、CL2 のタスクのサブセットとは異なり、重複がないことを確認することです。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="5ca5d-298">これは、タスクが関連付けられたときにシステムによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-299">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-300">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-301">QL2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-302">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-303">選択したタスクのみ</span><span class="sxs-lookup"><span data-stu-id="5ca5d-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-304">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-305">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-306">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-307">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-308">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-309">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-310">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-311">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-312">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-313">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-314">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-315">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-316">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-317">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-318">ルール #5 によると、Q1 と Q2 は同じ営業案件の 2 つの見積もりであるため、どちらもプロジェクトの同じコンポーネントを見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-319">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-320">Q2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-321">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-322">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-323">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-324">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-325">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-326">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-327">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-328">O1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-329">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-330">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-331">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-332">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-333">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-334">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-335">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-336">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-337">無効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ca5d-338">ルール #4 によると、Q1 と Q2 は異なる営業案件の 2 つの見積もりであるため、どちらもプロジェクトの同じコンポーネントを見積もることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ca5d-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5ca5d-339">O2</span><span class="sxs-lookup"><span data-stu-id="5ca5d-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5ca5d-340">Q1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5ca5d-341">QL1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-342">P1</span><span class="sxs-lookup"><span data-stu-id="5ca5d-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5ca5d-343">すべてのプロジェクト タスクまたは空白</span><span class="sxs-lookup"><span data-stu-id="5ca5d-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5ca5d-344">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5ca5d-345">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5ca5d-346">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5ca5d-347">有効</span><span class="sxs-lookup"><span data-stu-id="5ca5d-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
