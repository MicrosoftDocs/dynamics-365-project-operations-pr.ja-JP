---
title: 財務分析コードの既定値
description: このトピックは、財務分析コードの規定値を設定する方法について説明します。
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013312"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="0804c-103">財務分析コードの既定値</span><span class="sxs-lookup"><span data-stu-id="0804c-103">Financial dimension defaults</span></span>

<span data-ttu-id="0804c-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0804c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0804c-105">Dynamics 365 Project Operations は Dynamics 365 Finance の [財務分析コード](/dynamics365/finance/general-ledger/financial-dimensions) フレームワークを使用して、プロジェクトの補助元帳と総勘定元帳の取引に関する追加的な分析情報を提供しています。</span><span class="sxs-lookup"><span data-stu-id="0804c-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="0804c-106">既定の財務分析コードは、顧客、プロジェクトの資金源、マイルストーン、プロジェクトの契約品目、プロジェクトに設定できます。</span><span class="sxs-lookup"><span data-stu-id="0804c-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="0804c-107">顧客が使用する既定の財務分析コードを定義する</span><span class="sxs-lookup"><span data-stu-id="0804c-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="0804c-108">顧客分析コードの既定は、財務で指定されています。</span><span class="sxs-lookup"><span data-stu-id="0804c-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="0804c-109">以下の手順を実行して、分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0804c-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="0804c-110">**売掛金勘定** > **顧客** > **すべての顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0804c-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="0804c-111">**顧客** ページで、**財務分析コード** タブで、特定の顧客の財務分析コード値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0804c-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="0804c-112">プロジェクト契約で使用する既定の財務分析コードを定義する</span><span class="sxs-lookup"><span data-stu-id="0804c-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="0804c-113">プロジェクト契約は、 Common Data Service (CDS)で作成・管理されます。</span><span class="sxs-lookup"><span data-stu-id="0804c-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="0804c-114">プロジェクト契約の会計属性は、財務の **プロジェクト管理と会計** モジュールに設定されています。</span><span class="sxs-lookup"><span data-stu-id="0804c-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="0804c-115">プロジェクトの資金源の財務分析コードを設定する</span><span class="sxs-lookup"><span data-stu-id="0804c-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="0804c-116">**プロジェクト管理および会計** > **プロジェクト** > **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0804c-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="0804c-117">更新するレコードを選択し、**プロジェクト契約** タブで、**既定の会計を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0804c-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0804c-118">**関連情報** を展開し、**資金調達ソース** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="0804c-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="0804c-119">財務分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0804c-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="0804c-120">財務分析コードは顧客アカウントから既定に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0804c-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="0804c-121">プロジェクトの契約品目の財務分析コードを設定する</span><span class="sxs-lookup"><span data-stu-id="0804c-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="0804c-122">**プロジェクト管理および会計** > **プロジェクト** > **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0804c-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="0804c-123">更新するレコードを選択し、**プロジェクト契約** タブで、**既定の会計を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0804c-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0804c-124">**関連情報** を展開し、**契約品目** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="0804c-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="0804c-125">財務分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0804c-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="0804c-126">財務分析コードの既定が適用され、固定価格 (マイルストーン) 契約品目でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="0804c-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="0804c-127">これらの既定値は、関連するプロジェクトの分割払トランザクションおよび請求明細行で使用されます。</span><span class="sxs-lookup"><span data-stu-id="0804c-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="0804c-128">プロジェクトで使用する既定の財務分析コードを定義する</span><span class="sxs-lookup"><span data-stu-id="0804c-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="0804c-129">プロジェクトは、CDS で作成・管理されます。</span><span class="sxs-lookup"><span data-stu-id="0804c-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="0804c-130">プロジェクトの会計属性は、財務の **プロジェクト管理と会計** モジュールに設定されています。</span><span class="sxs-lookup"><span data-stu-id="0804c-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="0804c-131">**プロジェクト管理および会計** > **プロジェクト** > **すべてのプロジェクト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0804c-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="0804c-132">更新するレコードを選択し、**プロジェクト** タブで、**既定の会計を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0804c-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0804c-133">**関連情報** を展開し、**設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="0804c-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="0804c-134">財務分析コードの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0804c-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="0804c-135">顧客アカウントから財務分析コードの既定値が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0804c-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="0804c-136">プロジェクトが複数のプロジェクト契約顧客との契約品目に関連付けられている場合、主要顧客が財務分析コードの既定値に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0804c-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="0804c-137">プロジェクトの既定の財務分析コードを使用して、**Project Operations の統合仕訳帳** および関連するプロジェクト請求明細行の時間トランザクション、経費トランザクション、および手数料トランザクションの仕訳帳明細行の既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0804c-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]