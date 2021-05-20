---
title: 展開の種類を決定する
description: このトピックでは、会社のプロジェクト オペレーションの正しい展開の種類を決定するのに役立つ情報を提供します。
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948111"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="73c7c-103">展開の種類を決定する</span><span class="sxs-lookup"><span data-stu-id="73c7c-103">Determine your deployment type</span></span>

<span data-ttu-id="73c7c-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="73c7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73c7c-105">ライセンスを購入したら、[ガイド付きインストール フロー](https://aka.ms/provisionprojectoperations) を使って、ここから Dynamics 365 Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="73c7c-106">ガイド付きインストール フローを終了した後、正しい管理ポータルに移動してインストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="73c7c-107">展開の詳細を参照して、インストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="73c7c-108">Dynamics 365 Project Service Automation を使用する Dynamics の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="73c7c-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="73c7c-109">Project Operations には、Project Service Automation に付属する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="73c7c-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="73c7c-110">これらのお客様向けに、2021 年のリリースサイクル 1 でアップグレード パスがリリースされます。</span><span class="sxs-lookup"><span data-stu-id="73c7c-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="73c7c-111">プロジェクト管理および会計を使用する Dynamics 365 Finance の既存の顧客</span><span class="sxs-lookup"><span data-stu-id="73c7c-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="73c7c-112">プロジェクト管理および会計機能を使用する財務の既存のお客様は、そのままご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="73c7c-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="73c7c-113">[在庫/製造オーダー シナリオ向け Project Operations](#pma) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73c7c-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="73c7c-114">展開リージョン</span><span class="sxs-lookup"><span data-stu-id="73c7c-114">Deployment regions</span></span>
<span data-ttu-id="73c7c-115">Project Operations の展開をサポートするリージョンを決定するには、[Dynamics 365 および Power Platform レポートの地域的利用可能性](https://dynamics.microsoft.com/en-us/geographic-availability/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73c7c-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="73c7c-116">**レポートを見る** を選択して、**Dynamics 365 > オペレーション アプリ > Dynamics 365 Project Operations** を展開して、サポートされているリージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="73c7c-117">展開タイプ</span><span class="sxs-lookup"><span data-stu-id="73c7c-117">Deployment types</span></span>
<span data-ttu-id="73c7c-118">Project Operations では、要件に合わせて複数の展開オプションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="73c7c-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="73c7c-119">新規または既存の Dynamics 365 の顧客のいずれの場合でも、Project Operations はニーズにあわせた対応ができます。</span><span class="sxs-lookup"><span data-stu-id="73c7c-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="73c7c-120">[展開アンケート](https://aka.ms/provisionprojectoperations) は、適切な展開を決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="73c7c-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="73c7c-121">結果により、次のいずれかの展開の種類にガイドされます。</span><span class="sxs-lookup"><span data-stu-id="73c7c-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="73c7c-122">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="73c7c-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="73c7c-123">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="73c7c-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="73c7c-124">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="73c7c-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="73c7c-125">Project Operations は、法人エンティティ レベルの構成を通じて、同じ環境で、在庫/製造オーダー シナリオおよび非在庫/リソースベースのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="73c7c-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="73c7c-126">例えば、Contoso は、米国の製造施設で在庫/製造注文機能を使用できます (法人 = Contoso Manufacturing United States)。</span><span class="sxs-lookup"><span data-stu-id="73c7c-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="73c7c-127">Contoso は、英国の施設にサービスを提供する Contoso Robotics Arms で在庫のない/リソースベースの機能を使用できます (法人 = Contoso Robotics United Kingdom)。</span><span class="sxs-lookup"><span data-stu-id="73c7c-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="73c7c-128">ライト展開 - 見積もり請求の取引</span><span class="sxs-lookup"><span data-stu-id="73c7c-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="73c7c-129">ライト展開には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="73c7c-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="73c7c-130">Dynamics 365 Sales アプリケーションのエクスペリエンスを拡張するプロジェクトの営業プロセス</span><span class="sxs-lookup"><span data-stu-id="73c7c-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="73c7c-131">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="73c7c-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="73c7c-132">多次元の価格</span><span class="sxs-lookup"><span data-stu-id="73c7c-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="73c7c-133">統合されたリソース管理</span><span class="sxs-lookup"><span data-stu-id="73c7c-133">Unified resource management</span></span>
- <span data-ttu-id="73c7c-134">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="73c7c-134">Time tracking</span></span>
- <span data-ttu-id="73c7c-135">基本経費</span><span class="sxs-lookup"><span data-stu-id="73c7c-135">Basic expense</span></span>
- <span data-ttu-id="73c7c-136">プロジェクト マネージャーのレビューと編集のための見積請求</span><span class="sxs-lookup"><span data-stu-id="73c7c-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="73c7c-137">展開の手順</span><span class="sxs-lookup"><span data-stu-id="73c7c-137">Deployment steps</span></span>
<span data-ttu-id="73c7c-138">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="73c7c-139">この展開については、[プレビュー サブスクリプションにサインアップする](lite-preview-subscription-sign-up.md) および[新しい環境をプロビジョニングする](lite-deployment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73c7c-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="73c7c-140">リソース/非在庫のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="73c7c-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="73c7c-141">リソース/非在庫のシナリオ向け Project Operations には、次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="73c7c-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="73c7c-142">Dynamics 365 Sales アプリケーションのエクスペリエンスを拡張するプロジェクトの営業プロセス</span><span class="sxs-lookup"><span data-stu-id="73c7c-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="73c7c-143">Web 向けの Microsoft Project を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="73c7c-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="73c7c-144">多次元の価格</span><span class="sxs-lookup"><span data-stu-id="73c7c-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="73c7c-145">統一リソースの管理</span><span class="sxs-lookup"><span data-stu-id="73c7c-145">Unified resource management</span></span>
- <span data-ttu-id="73c7c-146">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="73c7c-146">Time tracking</span></span>
- <span data-ttu-id="73c7c-147">基本の経費</span><span class="sxs-lookup"><span data-stu-id="73c7c-147">Basic expense</span></span>
- <span data-ttu-id="73c7c-148">フル経費</span><span class="sxs-lookup"><span data-stu-id="73c7c-148">Full expense</span></span>
- <span data-ttu-id="73c7c-149">レシート OCR</span><span class="sxs-lookup"><span data-stu-id="73c7c-149">Receipt OCR</span></span>
- <span data-ttu-id="73c7c-150">見積送り状と顧客向けの請求書</span><span class="sxs-lookup"><span data-stu-id="73c7c-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="73c7c-151">プロジェクトに対する売上の認識</span><span class="sxs-lookup"><span data-stu-id="73c7c-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="73c7c-152">展開の手順</span><span class="sxs-lookup"><span data-stu-id="73c7c-152">Deployment steps</span></span>
<span data-ttu-id="73c7c-153">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="73c7c-154">この展開については、[プレビュー サブスクリプションにサインアップする](resource-sign-up-preview-subscription.md) および[新しい環境をプロビジョニングする](resource-provision-new-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73c7c-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="73c7c-155">在庫/製造指示のシナリオ向け Project Operations</span><span class="sxs-lookup"><span data-stu-id="73c7c-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="73c7c-156">WBS を使用したプロジェクト計画</span><span class="sxs-lookup"><span data-stu-id="73c7c-156">Project planning using WBS</span></span>
- <span data-ttu-id="73c7c-157">リソース管理</span><span class="sxs-lookup"><span data-stu-id="73c7c-157">Resource management</span></span>
- <span data-ttu-id="73c7c-158">時間のトラッキング</span><span class="sxs-lookup"><span data-stu-id="73c7c-158">Time tracking</span></span>
- <span data-ttu-id="73c7c-159">フル経費</span><span class="sxs-lookup"><span data-stu-id="73c7c-159">Full expense</span></span>
- <span data-ttu-id="73c7c-160">OCR の受け取り</span><span class="sxs-lookup"><span data-stu-id="73c7c-160">Receipt OCR</span></span>
- <span data-ttu-id="73c7c-161">完全な請求</span><span class="sxs-lookup"><span data-stu-id="73c7c-161">Full invoicing</span></span>
- <span data-ttu-id="73c7c-162">売上認識</span><span class="sxs-lookup"><span data-stu-id="73c7c-162">Revenue recognition</span></span>
- <span data-ttu-id="73c7c-163">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="73c7c-163">Production orders</span></span>
- <span data-ttu-id="73c7c-164">在庫による在庫材料のサポート</span><span class="sxs-lookup"><span data-stu-id="73c7c-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="73c7c-165">展開の手順</span><span class="sxs-lookup"><span data-stu-id="73c7c-165">Deployment steps</span></span>
<span data-ttu-id="73c7c-166">[展開アンケート](https://aka.ms/provisionprojectoperations) を使用して Project Operations の最適な展開モデルを決定します。</span><span class="sxs-lookup"><span data-stu-id="73c7c-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="73c7c-167">この展開については、[プレビュー サブスクリプションにサインアップする](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) および[新しい環境をプロビジョニングする](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73c7c-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]