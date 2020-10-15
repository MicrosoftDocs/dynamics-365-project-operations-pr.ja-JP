---
title: 展開の種類
description: このトピックでは、会社のプロジェクト オペレーションの正しい展開の種類を決定するのに役立つ情報を提供します。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948938"
---
# <a name="deployment-types"></a><span data-ttu-id="67546-103">展開の種類</span><span class="sxs-lookup"><span data-stu-id="67546-103">Deployment types</span></span>

<span data-ttu-id="67546-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="67546-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67546-105">ライセンスを購入した後、ここから開始して、[ガイド付きインストール フロー](https://aka.ms/provisionprojectoperations) を使用し Dynamics 365 Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="67546-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="67546-106">ガイド付きインストール フローを終了した後、正しい管理ポータルに移動してインストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="67546-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="67546-107">以下の展開の詳細を参照して、インストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="67546-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="67546-108">Dynamics 365 Project Service Automation を使用する Dynamics の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="67546-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="67546-109">Project Operations には、Project Service Automation に付属する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67546-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="67546-110">将来、これらの顧客に対してアップグレード パスがリリースされる予定です。</span><span class="sxs-lookup"><span data-stu-id="67546-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="67546-111">プロジェクト管理および会計を使用する Dynamics 365 Finance の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="67546-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="67546-112">プロジェクト管理および会計機能を使用する Finance の既存の顧客は、これをそのままの状態で引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="67546-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="67546-113">[在庫/製造オーダー シナリオ向け Project Operations](#pma) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67546-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="67546-114">Project Operations は、要件に合った複数の展開オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="67546-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="67546-115">新規または既存の Dynamics 365 の顧客のいずれの場合でも、Project Operations はニーズにあわせてサポートできます。</span><span class="sxs-lookup"><span data-stu-id="67546-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="67546-116">[展開アンケート](https://aka.ms/provisionprojectoperations) は、適切な展開を決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="67546-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="67546-117">結果により、次のいずれかの展開の種類にガイドされます。</span><span class="sxs-lookup"><span data-stu-id="67546-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="67546-118">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="67546-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="67546-119">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="67546-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="67546-120">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="67546-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="67546-121">Project Operations は、法人エンティティ レベルの構成を通じて、同じ環境で、在庫/製造オーダー シナリオおよび非在庫/リソースベースのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="67546-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="67546-122">たとえば、Contoso は、米国の製造施設 (法人 = 米国 Contoso Manufacturing) で在庫/製造オーダーの機能を、および英国のContoso Robotics Arms サービス施設 (法人 = 英国 Contoso Robotics) で非在庫/リソースベースの機能を活用できます。</span><span class="sxs-lookup"><span data-stu-id="67546-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="67546-123"><a name="lite"><a/>ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="67546-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="67546-124">ライト展開には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67546-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="67546-125">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="67546-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="67546-126">多次元の価格</span><span class="sxs-lookup"><span data-stu-id="67546-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="67546-127">統一リソース管理</span><span class="sxs-lookup"><span data-stu-id="67546-127">Unified Resource Management</span></span>
- <span data-ttu-id="67546-128">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="67546-128">Time Tracking</span></span>
- <span data-ttu-id="67546-129">基本経費</span><span class="sxs-lookup"><span data-stu-id="67546-129">Basic Expense</span></span>
- <span data-ttu-id="67546-130">請求書の提案</span><span class="sxs-lookup"><span data-stu-id="67546-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="67546-131">展開の手順:</span><span class="sxs-lookup"><span data-stu-id="67546-131">Deployment steps:</span></span>
<span data-ttu-id="67546-132">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="67546-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="67546-133">この展開については、[プレビュー サブスクリプションにサインアップする](lite-preview-subscription-sign-up.md) および[新しい環境をプロビジョニングする](lite-deployment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67546-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="67546-134"><a name="integrated"><a/>リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="67546-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="67546-135">リソース/非在庫のシナリオ向け Project Operations には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67546-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="67546-136">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="67546-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="67546-137">多次元の価格設定</span><span class="sxs-lookup"><span data-stu-id="67546-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="67546-138">統一リソース管理</span><span class="sxs-lookup"><span data-stu-id="67546-138">Unified Resource Management</span></span>
- <span data-ttu-id="67546-139">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="67546-139">Time Tracking</span></span>
- <span data-ttu-id="67546-140">基本経費</span><span class="sxs-lookup"><span data-stu-id="67546-140">Basic Expense</span></span>
- <span data-ttu-id="67546-141">フル経費</span><span class="sxs-lookup"><span data-stu-id="67546-141">Full Expense</span></span>
- <span data-ttu-id="67546-142">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="67546-142">Receipt OCR</span></span>
- <span data-ttu-id="67546-143">フル請求</span><span class="sxs-lookup"><span data-stu-id="67546-143">Full Invoicing</span></span>
- <span data-ttu-id="67546-144">売上認識</span><span class="sxs-lookup"><span data-stu-id="67546-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="67546-145">展開の手順:</span><span class="sxs-lookup"><span data-stu-id="67546-145">Deployment steps:</span></span>
<span data-ttu-id="67546-146">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="67546-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="67546-147">この展開については、[プレビュー サブスクリプションにサインアップする](resource-sign-up-preview-subscription.md) および[新しい環境をプロビジョニングする](resource-provision-new-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67546-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="67546-148">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="67546-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="67546-149">WBS を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="67546-149">Project planning using WBS</span></span>
- <span data-ttu-id="67546-150">リソース管理</span><span class="sxs-lookup"><span data-stu-id="67546-150">Resource Management</span></span>
- <span data-ttu-id="67546-151">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="67546-151">Time Tracking</span></span>
- <span data-ttu-id="67546-152">フル経費</span><span class="sxs-lookup"><span data-stu-id="67546-152">Full Expense</span></span>
- <span data-ttu-id="67546-153">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="67546-153">Receipt OCR</span></span>
- <span data-ttu-id="67546-154">フル請求</span><span class="sxs-lookup"><span data-stu-id="67546-154">Full Invoicing</span></span>
- <span data-ttu-id="67546-155">売上認識</span><span class="sxs-lookup"><span data-stu-id="67546-155">Revenue Recognition</span></span>
- <span data-ttu-id="67546-156">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="67546-156">Production Orders</span></span>
- <span data-ttu-id="67546-157">材料サポート</span><span class="sxs-lookup"><span data-stu-id="67546-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="67546-158">展開の手順:</span><span class="sxs-lookup"><span data-stu-id="67546-158">Deployment steps:</span></span>
<span data-ttu-id="67546-159">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="67546-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="67546-160">この展開については、[プレビュー サブスクリプションにサインアップする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) および[新しい環境をプロビジョニングする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67546-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



