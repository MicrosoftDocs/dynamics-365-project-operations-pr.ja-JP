---
title: 保留状態のベンダーの請求書を使って非在庫の材料を購入する
description: このトピックは、保留中のベンダーの請求書を記録する方法について説明しています。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993805"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="87379-103">保留状態のベンダーの請求書を使って非在庫の材料を購入する</span><span class="sxs-lookup"><span data-stu-id="87379-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="87379-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="87379-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87379-105">企業があるプロジェクトのために非在庫の材料を調達した場合に、このコストをすぐにプロジェクトに対して計上できます。</span><span class="sxs-lookup"><span data-stu-id="87379-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="87379-106">たとえば、Contoso Robotics US は機器更新プロジェクトを実行しており、ソフトウェア ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="87379-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="87379-107">これらのライセンスは、サードパーティ ベンダーが調達します。</span><span class="sxs-lookup"><span data-stu-id="87379-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="87379-108">Dynamics 365 Finance を使用して、買掛金勘定の担当者は、保留中のベンダーの請求書を記録し、ライセンス費用を機器の更新プロジェクトに直接帰属させます。</span><span class="sxs-lookup"><span data-stu-id="87379-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="87379-109">このトピックで説明されている機能を使用する前に、必要となる構成を確認して適用してください。</span><span class="sxs-lookup"><span data-stu-id="87379-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="87379-110">詳細については、[在庫のない資材と保留中のベンダーの請求書を有効にします](configure-materials-nonstocked.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87379-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="87379-111">プロジェクト関連の保留中のベンダーの請求書を転記する</span><span class="sxs-lookup"><span data-stu-id="87379-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="87379-112">保留中のベンダーの請求書は、**保留中のベンダーの請求書** ページ (**買掛金勘定** > **請求書** > **保留中のベンダーの請求書**) に記録できます。</span><span class="sxs-lookup"><span data-stu-id="87379-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="87379-113">プロジェクト関連の保留中のベンダー請求書を転記するには、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="87379-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="87379-114">**買掛金勘定** > **請求書** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87379-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="87379-115">**請求書勘定** フィールドで、ベンダーを選択し、**数** フィールドに、ベンダーの請求書IDを入力します。</span><span class="sxs-lookup"><span data-stu-id="87379-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="87379-116">ベンダーの請求書と **商品番号** フィールドに明細行を追加し、ベンダーから購入した非在庫品を選択します。</span><span class="sxs-lookup"><span data-stu-id="87379-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="87379-117">調達カテゴリーに基づいているベンダーの請求書の明細行は、プロジェクトに対して記録できません。</span><span class="sxs-lookup"><span data-stu-id="87379-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="87379-118">購入した数量を追加します。</span><span class="sxs-lookup"><span data-stu-id="87379-118">Add the quantity purchased.</span></span> <span data-ttu-id="87379-119">システムは、在庫のない品目の価格構成に基づいて単価を入力します。</span><span class="sxs-lookup"><span data-stu-id="87379-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="87379-120">合計金額やその他の必要事項を明細行で確認します。</span><span class="sxs-lookup"><span data-stu-id="87379-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="87379-121">明細行の詳細については、**プロジェクト** タブで、このアイテムが記録されるプロジェクトの ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="87379-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="87379-122">必要に応じて、アクティビティ番号を選択し、プロジェクトのカテゴリーと明細行のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="87379-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="87379-123">保留中のベンダーの請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="87379-123">Post pending vendor invoice.</span></span> <span data-ttu-id="87379-124">請求書が転記されると、システムは以下を記録します:</span><span class="sxs-lookup"><span data-stu-id="87379-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="87379-125">ベンダーの残高額です。</span><span class="sxs-lookup"><span data-stu-id="87379-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="87379-126">消費税の金額です。</span><span class="sxs-lookup"><span data-stu-id="87379-126">The sales tax amount.</span></span>
    - <span data-ttu-id="87379-127">プロジェクトに対する原価は、調達統合アカウントに記録されます。</span><span class="sxs-lookup"><span data-stu-id="87379-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="87379-128">プロジェクトの実際の取引は、Dataverse です。</span><span class="sxs-lookup"><span data-stu-id="87379-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="87379-129">この取引は、[Project Operations の統合仕訳帳](../project-accounting/project-operations-integration-journal.md) を使用してさらに処理されます。</span><span class="sxs-lookup"><span data-stu-id="87379-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="87379-130">この仕訳を転記すると、金額が調達統合勘定からプロジェクト原価勘定に移動します。</span><span class="sxs-lookup"><span data-stu-id="87379-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
