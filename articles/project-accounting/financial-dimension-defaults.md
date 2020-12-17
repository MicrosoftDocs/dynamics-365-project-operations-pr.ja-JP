---
title: 財務分析コードの既定値
description: このトピックは、財務分析コードの規定値を設定する方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642369"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="15ad1-103">財務分析コードの既定値</span><span class="sxs-lookup"><span data-stu-id="15ad1-103">Financial dimension defaults</span></span>

<span data-ttu-id="15ad1-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="15ad1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="15ad1-105">Dynamics 365 Project Operations は Dynamics 365 Finance の [財務分析コード](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) フレームワークを使用して、プロジェクトの補助元帳と総勘定元帳の取引に関する追加的な分析情報を提供しています。</span><span class="sxs-lookup"><span data-stu-id="15ad1-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="15ad1-106">既定の財務分析コードは、顧客、プロジェクトの資金源、マイルストーン、プロジェクトの契約品目、プロジェクトに設定できます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="15ad1-107">顧客が使用する既定の財務分析コードを定義する</span><span class="sxs-lookup"><span data-stu-id="15ad1-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="15ad1-108">顧客分析コードの既定は、財務で指定されています。</span><span class="sxs-lookup"><span data-stu-id="15ad1-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="15ad1-109">以下の手順を実行して、分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="15ad1-110">**売掛金勘定** > **顧客** > **すべての顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="15ad1-111">**顧客** ページで、**財務分析コード** タブで、特定の顧客の財務分析コード値を設定します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="15ad1-112">プロジェクト契約で使用する既定の財務分析コードを定義する</span><span class="sxs-lookup"><span data-stu-id="15ad1-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="15ad1-113">プロジェクト契約は、 Common Data Service (CDS)で作成・管理されます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="15ad1-114">プロジェクト契約の会計属性は、財務の **プロジェクト管理と会計** モジュールに設定されています。</span><span class="sxs-lookup"><span data-stu-id="15ad1-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="15ad1-115">プロジェクトの資金源の財務分析コードを設定する</span><span class="sxs-lookup"><span data-stu-id="15ad1-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="15ad1-116">**プロジェクト管理および会計** > **プロジェクト** > **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="15ad1-117">更新するレコードを選択し、**プロジェクト契約** タブで、**既定の会計を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="15ad1-118">**関連情報** を展開し、**資金源** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="15ad1-119">財務分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="15ad1-120">財務分析コードは顧客アカウントから既定に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="15ad1-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="15ad1-121">プロジェクトの契約品目の財務分析コードを設定する</span><span class="sxs-lookup"><span data-stu-id="15ad1-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="15ad1-122">**プロジェクト管理および会計** > **プロジェクト** > **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="15ad1-123">更新するレコードを選択し、**プロジェクト契約** タブで、**既定の会計を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="15ad1-124">**関連情報** を展開し、**契約品目** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="15ad1-125">財務分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="15ad1-126">財務分析コードの既定が適用され、固定価格 (マイルストーン) 契約品目でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="15ad1-127">これらの既定は、関連するプロジェクトの当座預金取引および請求書明細で使用されます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="15ad1-128">プロジェクトで使用する既定の財務分析コードを定義する</span><span class="sxs-lookup"><span data-stu-id="15ad1-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="15ad1-129">プロジェクトは、CDS で作成・管理されます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="15ad1-130">プロジェクトの会計属性は、財務の **プロジェクト管理と会計** モジュールに設定されています。</span><span class="sxs-lookup"><span data-stu-id="15ad1-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="15ad1-131">**プロジェクト管理および会計** > **プロジェクト** > **すべてのプロジェクト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="15ad1-132">更新するレコードを選択し、**プロジェクト** タブで、**既定の会計を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="15ad1-133">**関連情報** を展開し、**設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="15ad1-134">財務分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="15ad1-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="15ad1-135">財務分析コードは顧客アカウントから既定に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="15ad1-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="15ad1-136">プロジェクトが複数のプロジェクト契約顧客を持つ契約品目に関連付けられている場合、プライマリ顧客は、既定の財務分析コードに使用されます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="15ad1-137">プロジェクトの既定の財務分析コードは、**プロジェクト運用統合ジャーナル** の時間、費用、手数料のトランザクションと関連するプロジェクトの請求書明細のジャーナル ラインの既定を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="15ad1-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
