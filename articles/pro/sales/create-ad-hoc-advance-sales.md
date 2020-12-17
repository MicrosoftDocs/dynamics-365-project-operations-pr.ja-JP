---
title: 契約のアドホック前払いを作成する
description: このトピックは、必要に応じて契約の前払いを作成するための情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 790a0281f72eff5f241d11da025b5b4af643a567
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596001"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="04054-103">契約のアドホック前払いを作成する</span><span class="sxs-lookup"><span data-stu-id="04054-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="04054-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="04054-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="04054-105">Microsoft Dynamics 365 Project Operations は、前払いと立て替えを伴う請求シナリオに対応しています。</span><span class="sxs-lookup"><span data-stu-id="04054-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="04054-106">**Project Operations** の **前払い** を利用するプロセスは、**保留** 契約と共通しています。</span><span class="sxs-lookup"><span data-stu-id="04054-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="04054-107">次の手順を実行して、顧客に事前請求します。</span><span class="sxs-lookup"><span data-stu-id="04054-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="04054-108">**プロジェクト契約** ページに移動し、**前払いと保有金ー** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="04054-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="04054-109">以前に記録されたすべての前払い金と立て替え金を一覧表示するサブグリッドで、**+新規プロジェクト契約保留金** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04054-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="04054-110">前払いや立替金を記録する **簡易作成** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="04054-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="04054-111">以下の表に、立替金を記録するためのフィールドと、新たなフィールドを作成する際に留意すべき考慮事項を示します。</span><span class="sxs-lookup"><span data-stu-id="04054-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="04054-112">フィールド</span><span class="sxs-lookup"><span data-stu-id="04054-112">Field</span></span> | <span data-ttu-id="04054-113">内容</span><span class="sxs-lookup"><span data-stu-id="04054-113">Description</span></span> | <span data-ttu-id="04054-114">下位への影響</span><span class="sxs-lookup"><span data-stu-id="04054-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="04054-115">**プロジェクト契約の顧客**</span><span class="sxs-lookup"><span data-stu-id="04054-115">**Project Contract Customer**</span></span> | <span data-ttu-id="04054-116">このフィールドは、契約のどの顧客にこの前払いの請求が行われるかを示します。</span><span class="sxs-lookup"><span data-stu-id="04054-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="04054-117">契約に複数の顧客が存在し、それぞれに特定の保留金や前払い金額を請求する場合は、それぞれの顧客に対して個別に前払いを作成します。</span><span class="sxs-lookup"><span data-stu-id="04054-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="04054-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="04054-118">**Description**</span></span> | <span data-ttu-id="04054-119">この前払いを特定するのに役立つ、前払いの目的またはタイミングの説明です。</span><span class="sxs-lookup"><span data-stu-id="04054-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="04054-120">この説明は、この前払いの請求書の明細行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="04054-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="04054-121">**金額**</span><span class="sxs-lookup"><span data-stu-id="04054-121">**Amount**</span></span> | <span data-ttu-id="04054-122">前払いまたは立替金の金額です。</span><span class="sxs-lookup"><span data-stu-id="04054-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="04054-123">この金額は、この前払いの請求書の明細行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="04054-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="04054-124">**請求書の日付**</span><span class="sxs-lookup"><span data-stu-id="04054-124">**Invoice Date**</span></span> | <span data-ttu-id="04054-125">この前払いが顧客に請求される日付です。</span><span class="sxs-lookup"><span data-stu-id="04054-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="04054-126">これは、この前払の請求書明細を作成する自動請求書作成プロセスの日付を表わします。</span><span class="sxs-lookup"><span data-stu-id="04054-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="04054-127">**請求書の状態**</span><span class="sxs-lookup"><span data-stu-id="04054-127">**Invoice Status**</span></span> | <span data-ttu-id="04054-128">この顧客の請求書のドラフトにこの前払金を追加するかどうかを示すオプション設定です。</span><span class="sxs-lookup"><span data-stu-id="04054-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="04054-129">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="04054-129">The possible values are:</span></span></br><span data-ttu-id="04054-130">- **請求準備未完了**</span><span class="sxs-lookup"><span data-stu-id="04054-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="04054-131">- **請求準備完了**</span><span class="sxs-lookup"><span data-stu-id="04054-131">- **Ready to invoice**</span></span> | <span data-ttu-id="04054-132">前払いまたは立替金が **請求準備完了** とマークされている場合は、請求書のドラフトにライン タイムとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="04054-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="04054-133">次の請求期間のプロジェクト費用との調整には、完全に請求された前払い金のみを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="04054-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="04054-134">簡易作成ダイアログで **保存して閉じる** を選択し、前払いまたは立替金を記録します。</span><span class="sxs-lookup"><span data-stu-id="04054-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>
