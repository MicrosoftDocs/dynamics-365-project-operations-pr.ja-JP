---
title: 展開の種類を決定する
description: このトピックでは、会社のプロジェクト オペレーションの正しい展開の種類を決定するのに役立つ情報を提供します。
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401224"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="ac28b-103">展開の種類を決定する</span><span class="sxs-lookup"><span data-stu-id="ac28b-103">Determine your deployment type</span></span>

<span data-ttu-id="ac28b-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="ac28b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac28b-105">ライセンスを購入した後、ここから開始して、[ガイド付きインストール フロー](https://aka.ms/provisionprojectoperations) を使用し Dynamics 365 Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="ac28b-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="ac28b-106">ガイド付きインストール フローを終了した後、正しい管理ポータルに移動してインストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="ac28b-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="ac28b-107">展開の詳細を参照して、インストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="ac28b-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="ac28b-108">Dynamics 365 Project Service Automation を使用する Dynamics の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="ac28b-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="ac28b-109">Project Operations には、Project Service Automation に付属する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac28b-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="ac28b-110">これらのお客様向けに、2021 年のリリースサイクル 1 でアップグレード パスがリリースされます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="ac28b-111">プロジェクト管理および会計を使用する Dynamics 365 Finance の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="ac28b-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="ac28b-112">プロジェクト管理および会計機能を使用する財務の既存のお客様は、そのままご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="ac28b-113">[在庫/製造オーダー シナリオ向け Project Operations](#pma) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac28b-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="ac28b-114">展開の種類</span><span class="sxs-lookup"><span data-stu-id="ac28b-114">Deployment types</span></span>
<span data-ttu-id="ac28b-115">Project Operations は、要件に合った複数の展開オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ac28b-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="ac28b-116">新規または既存の Dynamics 365 の顧客のいずれの場合でも、Project Operations はニーズにあわせた対応ができます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="ac28b-117">[展開アンケート](https://aka.ms/provisionprojectoperations) は、適切な展開を決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="ac28b-118">結果により、次のいずれかの展開の種類にガイドされます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="ac28b-119">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="ac28b-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="ac28b-120">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="ac28b-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="ac28b-121">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="ac28b-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="ac28b-122">Project Operations は、法人エンティティ レベルの構成を通じて、同じ環境で、在庫/製造オーダー シナリオおよび非在庫/リソースベースのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ac28b-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="ac28b-123">たとえば、Contoso 社は、米国の製造施設（法人= Contoso Manufacturing United States）で在庫/製造注文機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="ac28b-124">Contoso は、英国 の Contoso Robotics Arms サービス施設（法人= Contoso Robotics United Kingdom）で、在庫のない/リソースベースの機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ac28b-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="ac28b-125">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="ac28b-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="ac28b-126">ライト展開には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac28b-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="ac28b-127">Dynamics 365 Sales アプリケーションのエクスペリエンスを拡張するプロジェクトの営業プロセス</span><span class="sxs-lookup"><span data-stu-id="ac28b-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="ac28b-128">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="ac28b-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ac28b-129">多次元の価格</span><span class="sxs-lookup"><span data-stu-id="ac28b-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ac28b-130">統一リソースの管理</span><span class="sxs-lookup"><span data-stu-id="ac28b-130">Unified resource management</span></span>
- <span data-ttu-id="ac28b-131">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="ac28b-131">Time tracking</span></span>
- <span data-ttu-id="ac28b-132">基本の経費</span><span class="sxs-lookup"><span data-stu-id="ac28b-132">Basic expense</span></span>
- <span data-ttu-id="ac28b-133">見積送り状と顧客向けの請求書</span><span class="sxs-lookup"><span data-stu-id="ac28b-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="ac28b-134">展開の手順</span><span class="sxs-lookup"><span data-stu-id="ac28b-134">Deployment steps</span></span>
<span data-ttu-id="ac28b-135">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="ac28b-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ac28b-136">この展開については、[プレビュー サブスクリプションにサインアップする](lite-preview-subscription-sign-up.md) および[新しい環境をプロビジョニングする](lite-deployment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac28b-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="ac28b-137">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="ac28b-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="ac28b-138">リソース/非在庫のシナリオ向け Project Operations には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac28b-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="ac28b-139">Dynamics 365 Sales アプリケーションのエクスペリエンスを拡張するプロジェクトの営業プロセス</span><span class="sxs-lookup"><span data-stu-id="ac28b-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="ac28b-140">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="ac28b-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ac28b-141">多次元の価格</span><span class="sxs-lookup"><span data-stu-id="ac28b-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ac28b-142">統一リソースの管理</span><span class="sxs-lookup"><span data-stu-id="ac28b-142">Unified resource management</span></span>
- <span data-ttu-id="ac28b-143">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="ac28b-143">Time tracking</span></span>
- <span data-ttu-id="ac28b-144">基本の経費</span><span class="sxs-lookup"><span data-stu-id="ac28b-144">Basic expense</span></span>
- <span data-ttu-id="ac28b-145">フル経費</span><span class="sxs-lookup"><span data-stu-id="ac28b-145">Full expense</span></span>
- <span data-ttu-id="ac28b-146">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="ac28b-146">Receipt OCR</span></span>
- <span data-ttu-id="ac28b-147">見積送り状と顧客向けの請求書</span><span class="sxs-lookup"><span data-stu-id="ac28b-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="ac28b-148">プロジェクトに対する売上の認識</span><span class="sxs-lookup"><span data-stu-id="ac28b-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ac28b-149">展開の手順</span><span class="sxs-lookup"><span data-stu-id="ac28b-149">Deployment steps</span></span>
<span data-ttu-id="ac28b-150">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="ac28b-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ac28b-151">この展開については、[プレビュー サブスクリプションにサインアップする](resource-sign-up-preview-subscription.md) および[新しい環境をプロビジョニングする](resource-provision-new-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac28b-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="ac28b-152">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="ac28b-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="ac28b-153">WBS を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="ac28b-153">Project planning using WBS</span></span>
- <span data-ttu-id="ac28b-154">リソース管理</span><span class="sxs-lookup"><span data-stu-id="ac28b-154">Resource Management</span></span>
- <span data-ttu-id="ac28b-155">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="ac28b-155">Time Tracking</span></span>
- <span data-ttu-id="ac28b-156">フル経費</span><span class="sxs-lookup"><span data-stu-id="ac28b-156">Full Expense</span></span>
- <span data-ttu-id="ac28b-157">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="ac28b-157">Receipt OCR</span></span>
- <span data-ttu-id="ac28b-158">フル請求</span><span class="sxs-lookup"><span data-stu-id="ac28b-158">Full Invoicing</span></span>
- <span data-ttu-id="ac28b-159">売上認識</span><span class="sxs-lookup"><span data-stu-id="ac28b-159">Revenue Recognition</span></span>
- <span data-ttu-id="ac28b-160">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="ac28b-160">Production Orders</span></span>
- <span data-ttu-id="ac28b-161">材料サポート</span><span class="sxs-lookup"><span data-stu-id="ac28b-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ac28b-162">展開の手順</span><span class="sxs-lookup"><span data-stu-id="ac28b-162">Deployment steps</span></span>
<span data-ttu-id="ac28b-163">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="ac28b-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ac28b-164">この展開については、[プレビュー サブスクリプションにサインアップする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) および[新しい環境をプロビジョニングする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac28b-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

