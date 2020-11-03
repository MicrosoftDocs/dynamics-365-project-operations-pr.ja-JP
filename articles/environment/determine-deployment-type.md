---
title: 展開の種類を決定する
description: このトピックでは、会社のプロジェクト オペレーションの正しい展開の種類を決定するのに役立つ情報を提供します。
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079272"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="603d7-103">展開の種類を決定する</span><span class="sxs-lookup"><span data-stu-id="603d7-103">Determine your deployment type</span></span>

<span data-ttu-id="603d7-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="603d7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="603d7-105">ライセンスを購入した後、ここから開始して、[ガイド付きインストール フロー](https://aka.ms/provisionprojectoperations) を使用し Dynamics 365 Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="603d7-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="603d7-106">ガイド付きインストール フローを終了した後、正しい管理ポータルに移動してインストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="603d7-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="603d7-107">展開の詳細を参照して、インストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="603d7-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="603d7-108">Dynamics 365 Project Service Automation を使用する Dynamics の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="603d7-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="603d7-109">Project Operations には、Project Service Automation に付属する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="603d7-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="603d7-110">将来、これらの顧客に対してアップグレード パスがリリースされる予定です。</span><span class="sxs-lookup"><span data-stu-id="603d7-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="603d7-111">プロジェクト管理および会計を使用する Dynamics 365 Finance の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="603d7-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="603d7-112">プロジェクト管理および会計機能を使用する財務の既存の顧客は、これをそのままの状態で引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="603d7-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="603d7-113">[在庫/製造オーダー シナリオ向け Project Operations](#pma) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="603d7-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="603d7-114">展開の種類</span><span class="sxs-lookup"><span data-stu-id="603d7-114">Deployment types</span></span>
<span data-ttu-id="603d7-115">Project Operations は、要件に合った複数の展開オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="603d7-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="603d7-116">新規または既存の Dynamics 365 の顧客のいずれの場合でも、Project Operations はニーズにあわせた対応ができます。</span><span class="sxs-lookup"><span data-stu-id="603d7-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="603d7-117">[展開アンケート](https://aka.ms/provisionprojectoperations) は、適切な展開を決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="603d7-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="603d7-118">結果により、次のいずれかの展開の種類にガイドされます。</span><span class="sxs-lookup"><span data-stu-id="603d7-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="603d7-119">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="603d7-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="603d7-120">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="603d7-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="603d7-121">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="603d7-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="603d7-122">Project Operations は、法人エンティティ レベルの構成を通じて、同じ環境で、在庫/製造オーダー シナリオおよび非在庫/リソースベースのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="603d7-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="603d7-123">たとえば、Contoso 社は、米国の製造施設（法人= Contoso Manufacturing United States）で在庫/製造注文機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="603d7-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="603d7-124">Contoso は、英国 の Contoso Robotics Arms サービス施設（法人= Contoso Robotics United Kingdom）で、在庫のない/リソースベースの機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="603d7-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="603d7-125">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="603d7-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="603d7-126">ライト展開には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="603d7-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="603d7-127">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="603d7-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="603d7-128">多次元の価格</span><span class="sxs-lookup"><span data-stu-id="603d7-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="603d7-129">統一リソース管理</span><span class="sxs-lookup"><span data-stu-id="603d7-129">Unified Resource Management</span></span>
- <span data-ttu-id="603d7-130">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="603d7-130">Time Tracking</span></span>
- <span data-ttu-id="603d7-131">基本経費</span><span class="sxs-lookup"><span data-stu-id="603d7-131">Basic Expense</span></span>
- <span data-ttu-id="603d7-132">請求書の提案</span><span class="sxs-lookup"><span data-stu-id="603d7-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="603d7-133">展開の手順</span><span class="sxs-lookup"><span data-stu-id="603d7-133">Deployment steps</span></span>
<span data-ttu-id="603d7-134">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="603d7-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="603d7-135">この展開については、[プレビュー サブスクリプションにサインアップする](lite-preview-subscription-sign-up.md) および[新しい環境をプロビジョニングする](lite-deployment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="603d7-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="603d7-136">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="603d7-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="603d7-137">リソース/非在庫のシナリオ向け Project Operations には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="603d7-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="603d7-138">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="603d7-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="603d7-139">多次元の価格設定</span><span class="sxs-lookup"><span data-stu-id="603d7-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="603d7-140">統一リソース管理</span><span class="sxs-lookup"><span data-stu-id="603d7-140">Unified Resource Management</span></span>
- <span data-ttu-id="603d7-141">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="603d7-141">Time Tracking</span></span>
- <span data-ttu-id="603d7-142">基本経費</span><span class="sxs-lookup"><span data-stu-id="603d7-142">Basic Expense</span></span>
- <span data-ttu-id="603d7-143">フル経費</span><span class="sxs-lookup"><span data-stu-id="603d7-143">Full Expense</span></span>
- <span data-ttu-id="603d7-144">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="603d7-144">Receipt OCR</span></span>
- <span data-ttu-id="603d7-145">フル請求</span><span class="sxs-lookup"><span data-stu-id="603d7-145">Full Invoicing</span></span>
- <span data-ttu-id="603d7-146">売上認識</span><span class="sxs-lookup"><span data-stu-id="603d7-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="603d7-147">展開の手順</span><span class="sxs-lookup"><span data-stu-id="603d7-147">Deployment steps</span></span>
<span data-ttu-id="603d7-148">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="603d7-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="603d7-149">この展開については、[プレビュー サブスクリプションにサインアップする](resource-sign-up-preview-subscription.md) および[新しい環境をプロビジョニングする](resource-provision-new-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="603d7-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="603d7-150">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="603d7-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="603d7-151">WBS を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="603d7-151">Project planning using WBS</span></span>
- <span data-ttu-id="603d7-152">リソース管理</span><span class="sxs-lookup"><span data-stu-id="603d7-152">Resource Management</span></span>
- <span data-ttu-id="603d7-153">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="603d7-153">Time Tracking</span></span>
- <span data-ttu-id="603d7-154">フル経費</span><span class="sxs-lookup"><span data-stu-id="603d7-154">Full Expense</span></span>
- <span data-ttu-id="603d7-155">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="603d7-155">Receipt OCR</span></span>
- <span data-ttu-id="603d7-156">フル請求</span><span class="sxs-lookup"><span data-stu-id="603d7-156">Full Invoicing</span></span>
- <span data-ttu-id="603d7-157">売上認識</span><span class="sxs-lookup"><span data-stu-id="603d7-157">Revenue Recognition</span></span>
- <span data-ttu-id="603d7-158">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="603d7-158">Production Orders</span></span>
- <span data-ttu-id="603d7-159">材料サポート</span><span class="sxs-lookup"><span data-stu-id="603d7-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="603d7-160">展開の手順</span><span class="sxs-lookup"><span data-stu-id="603d7-160">Deployment steps</span></span>
<span data-ttu-id="603d7-161">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="603d7-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="603d7-162">この展開については、[プレビュー サブスクリプションにサインアップする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) および[新しい環境をプロビジョニングする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="603d7-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

