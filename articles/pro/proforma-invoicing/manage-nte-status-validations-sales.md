---
title: 上限と検証の管理
description: このトピックは、Project Operations で実行される上限チェックに関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129999"
---
# <a name="manage-not-to-exceed-status-and-validations"></a><span data-ttu-id="31cbe-103">上限と検証の管理</span><span class="sxs-lookup"><span data-stu-id="31cbe-103">Manage not-to-exceed status and validations</span></span> 

<span data-ttu-id="31cbe-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="31cbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="not-to-exceed-on-approvals"></a><span data-ttu-id="31cbe-105">承認の上限</span><span class="sxs-lookup"><span data-stu-id="31cbe-105">Not-to-exceed on approvals</span></span>

<span data-ttu-id="31cbe-106">時間または経費の入力が送信されると、承認レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-106">When a time or expense entry is submitted, an approval record is created.</span></span> <span data-ttu-id="31cbe-107">承認が有料で、時間と材料の契約品目にマッピングされている場合、システムは次のレベルで上限の検証チェックを完了します。</span><span class="sxs-lookup"><span data-stu-id="31cbe-107">If the approval is chargeable and maps to a time and material contract line, the system completes a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="31cbe-108">プロジェクトの契約品目で顧客に設定された制限との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-108">Check against the limit set up for the customer on the project contract line</span></span>
  - <span data-ttu-id="31cbe-109">契約品目で設定された限度額との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-109">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="31cbe-110">顧客に設定された限度額との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-110">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="31cbe-111">契約で設定された限度額との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-111">Check against the limit set up on the contract</span></span>

<span data-ttu-id="31cbe-112">各レベルのチェックでは、既に記録されている請求バックログの金額と、そのレベルで現在までに請求された金額を計算した上で、この承認の売上額がそのレベルでの超過しない限度に違反しないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-112">The checks at each level involve ensuring that the amount of sales value on this approval will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="31cbe-113">チェックに合格すると、承認の検証ステータスが **成功** になります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-113">If the check passes, the approval is given a validation status of **Success**.</span></span>

<span data-ttu-id="31cbe-114">チェックで不合格になると、承認の検証ステータスが **失敗** になります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-114">If the check fails, the approval is given a validation status of **Failed**.</span></span> <span data-ttu-id="31cbe-115">上限の検証についての詳細は、どのレベルで検証に失敗したかをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="31cbe-115">The not-to-exceed validation detail will inform the user at which level the validation failed.</span></span>

<span data-ttu-id="31cbe-116">提出された時間または経費の入力が請求不可とみなされた場合、超過しない検証ステータスは **該当なし** に設定され、検証の詳細は **該当なし** に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-116">When the submitted time or expense entry is considered non-chargeable, the not-to-exceed validation status is set to **Not Applicable** with the validation detail equal to **Not applicable**.</span></span>

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a><span data-ttu-id="31cbe-117">未請求の販売実績の上限</span><span class="sxs-lookup"><span data-stu-id="31cbe-117">Not-to-exceed on unbilled sales actuals</span></span>

<span data-ttu-id="31cbe-118">時間や経費の入力が承認されると、原価および未請求の販売実績レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-118">When a time or expense entry is approved, cost and unbilled sales actuals records are created.</span></span> <span data-ttu-id="31cbe-119">作成された未請求の売上実績が有償であり、時間と材料の契約品目にマッピングされている場合、アプリケーションは以下のレベルで上限の検証チェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="31cbe-119">If the unbilled sales actual being created is chargeable and maps to a time and material contract line, the application performs a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="31cbe-120">プロジェクトの契約品目で顧客に設定された制限との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-120">Check against the limit set up for the customer of the project contract line</span></span>
  - <span data-ttu-id="31cbe-121">契約品目で設定された限度額との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-121">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="31cbe-122">顧客に設定された限度額との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-122">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="31cbe-123">契約で設定された限度額との照合</span><span class="sxs-lookup"><span data-stu-id="31cbe-123">Check against the limit set up on the contract</span></span>

<span data-ttu-id="31cbe-124">各レベルのチェックでは、すでに計上されている請求残高と、そのレベルでの現在までの請求額を考慮した上で、実際の販売額がそのレベルでの限度額を超過しないにことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-124">The checks at each level ensure that the amount of sales value on the actual will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="31cbe-125">チェックに合格すると、未請求の実際の売上のステータスが **コミット済み** になります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-125">If the check passes, the unbilled sales actual is given a not-to-exceed status of **Committed**.</span></span>

<span data-ttu-id="31cbe-126">チェックに不合格となると、未請求の実際の売上のステータスが **失敗** になります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-126">If the check fails, the unbilled sales actual is given a not-to-exceed status of **Failed**.</span></span> <span data-ttu-id="31cbe-127">検証の詳細は、どのレベルで検証に失敗したかをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="31cbe-127">The validation detail informs the user at which level the validation failed.</span></span>

<span data-ttu-id="31cbe-128">請求されていない売上実績が非課金または無料とみなされる場合、4 つのレベルのいずれにも限度額が設定されていない場合、または作成される実績がコスト、保留金、リソーシング ユニット、または組織間売上である場合、**上限の状態** および **検証の詳細の上限** フィールドを **該当なし** に設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="31cbe-128">When the unbilled sales actual is considered non-chargeable or complimentary, if there is no not-to-exceed limit setup at any of the four levels, or if the actual being created is Cost, Retainer, Resourcing Unit, or Inter-organization Sales, the **Not-to-Exceed Status** and **Not-to-Exceed Validation Detail** fields must be set to **Not Applicable**.</span></span>

## <a name="reset-the-not-to-exceed-status"></a><span data-ttu-id="31cbe-129">上限の状態をリセットする</span><span class="sxs-lookup"><span data-stu-id="31cbe-129">Reset the not-to-exceed status</span></span>

<span data-ttu-id="31cbe-130">上限の状態の一括リセットを実行できます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-130">You can perform a bulk reset of the not-to-exceed status.</span></span> <span data-ttu-id="31cbe-131">これにより、プロジェクト マネージャーは、特定の作業内容、時間、費用の請求を、すでに利用可能な上限金額から他の作業内容よりも優先して行うように調整することができます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-131">This allows Project managers to adjust not-to-exceed validation to prioritize invoicing of one particular body of work, time, or expenses over others that are already committed from the available not-to-exceed amount.</span></span>

<span data-ttu-id="31cbe-132">未請求の売上実績で上限の状態がリセットされた後、コミットした金額が減額されます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-132">After the not-to-exceed status is reset on unbilled sales actuals, the committed amount is reduced.</span></span> <span data-ttu-id="31cbe-133">プロジェクト マネージャーは、以前に上限の検証に失敗した別の作業、時間、経費を選択して再評価することができます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-133">The Project manager can select another body of work, time, or expenses that previously failed the not-to-exceed validation and reevaluate them.</span></span> <span data-ttu-id="31cbe-134">コミットされた金額が減少したことで、これらの実績値が検証に合格するようになります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-134">With the reduction in the committed amount, these actuals will now pass the validation.</span></span> <span data-ttu-id="31cbe-135">これにより、プロジェクト マネージャーは、その期間の請求可能なトランザクションに対してより大きな影響力と制御を発揮できます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-135">This helps the Project manager exert greater influence and control over the invoiceable transactions for that period.</span></span>

<span data-ttu-id="31cbe-136">上限の状態をリセットするには、**時間と材料の請求バックログ** ビューまたは **実績** ビューから 1 つ以上の実績を選択し、**上限の状態をリセットする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31cbe-136">To reset the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and then select **Reset Not-to-Exceed Status**.</span></span>

<span data-ttu-id="31cbe-137">上限の状態は、関連する選択されたすべての実績において、**評価されない** 状態にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-137">The not-to-exceed status is reset to **Not Evaluated** on all of the relevant selected actuals.</span></span> <span data-ttu-id="31cbe-138">上限の状態がリセットされてた実績は、請求書の下書きではなく、請求書がまだ発行されていない未請求の売上実績であり、請求可能とマークされています。</span><span class="sxs-lookup"><span data-stu-id="31cbe-138">Actuals that have their not-to-exceed status reset are unbilled sales actuals that aren't already invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="31cbe-139">その他の選択された実績は無視されます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-139">Any other selected actuals are ignored.</span></span>

## <a name="reevaluate-not-to-exceed-status"></a><span data-ttu-id="31cbe-140">上限の状態を再評価します</span><span class="sxs-lookup"><span data-stu-id="31cbe-140">Reevaluate not-to-exceed status</span></span>

<span data-ttu-id="31cbe-141">上限の状態の一括再評価を実行できます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-141">You can perform a bulk re-evaluation of the not-to-exceed status.</span></span> <span data-ttu-id="31cbe-142">上限の状態の再評価は、次のような場合に役立ちます :</span><span class="sxs-lookup"><span data-stu-id="31cbe-142">Re-evaluation of the not-to-exceed status is useful when:</span></span>

  - <span data-ttu-id="31cbe-143">顧客との間で限度額の再交渉があり、実際には再評価が必要になります。</span><span class="sxs-lookup"><span data-stu-id="31cbe-143">There was a renegotiation of not-to-exceed limits with the customer and actuals will need to be reevaluated.</span></span>
  - <span data-ttu-id="31cbe-144">プロジェクト マネージャーは、ある作業を別の作業よりも優先させることで、未請求の売上バックログの請求書を微調整したいと考えます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-144">The Project manager wants to fine-tune the invoicing of unbilled sales backlog by prioritizing one body of work over another.</span></span>

<span data-ttu-id="31cbe-145">上限の状態をを再評価するには、**時間と材料の請求バックログ** ビューまたは **実績** ビューから 1 つ以上の実績を選択し、**上限の状態を再評価する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31cbe-145">To reevaluate the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and select **Reevaluate Not-to-Exceed Status**.</span></span>

<span data-ttu-id="31cbe-146">上限に関連する選択されたすべての実績は、上限の設定に対して評価されます。</span><span class="sxs-lookup"><span data-stu-id="31cbe-146">All of the relevant selected actuals with a not-to-exceed limit will be evaluated against the not-to-exceed limit setup.</span></span> <span data-ttu-id="31cbe-147">上限の状態の再評価に関連する実績は、請求書が発行されておらず、請求書案にも記載されていない未請求の売上実績であり、請求可能と表示されているものです。</span><span class="sxs-lookup"><span data-stu-id="31cbe-147">Actuals that are relevant for re-evaluating the not-to-exceed status are unbilled sales actuals that are not invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="31cbe-148">その他の選択された任意の選択された実績です。</span><span class="sxs-lookup"><span data-stu-id="31cbe-148">Any other select actuals selected.</span></span>
