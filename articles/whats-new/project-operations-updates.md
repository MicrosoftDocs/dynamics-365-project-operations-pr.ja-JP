---
title: Project Operations の更新
description: このトピックでは、Dynamics 365 Project Operations のリリース版について情報を提供します。
author: sigitac
manager: Annbe
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5a1ab3b506ae94bba3a6ca96b164437d3fd3a035
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877541"
---
# <a name="project-operations-updates"></a><span data-ttu-id="00555-103">Project Operations の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="00555-103">Project Operations updates</span></span>

<span data-ttu-id="00555-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations、Lite 展開 - 見積もり請求の取引、在庫/製造ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="00555-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, and Project Operations for stocked/production-based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a><span data-ttu-id="00555-105">Project Operations のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="00555-105">Project Operations components</span></span>

<span data-ttu-id="00555-106">Dynamics 365 Project Operations は 2 つのコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="00555-106">Dynamics 365 Project Operations consists of two components:</span></span>

- <span data-ttu-id="00555-107">Dataverse 環境での Project Operations は、営業案件から見積もり請求までの機能をカバーします。</span><span class="sxs-lookup"><span data-stu-id="00555-107">Project Operations on Dataverse environment covers capabilities from opportunity to proforma invoicing.</span></span> <span data-ttu-id="00555-108">Dataverse は、Project Operations の Lite 展開およびリソース/非在庫シナリオ展開で使用されます。</span><span class="sxs-lookup"><span data-stu-id="00555-108">Dataverse is used in the lite deployment and resource/non-stocked scenarios deployment of Project Operations.</span></span>
- <span data-ttu-id="00555-109">Dynamics 365 Finance 環境でのプロジェクト管理および会計は、経費管理機能、プロジェクト会計、および収益認識をカバーします。</span><span class="sxs-lookup"><span data-stu-id="00555-109">Project management and accounting in the Dynamics 365 Finance environment covers expense management capabilities, project accounting, and revenue recognition.</span></span> <span data-ttu-id="00555-110">Finance and Operations アプリ環境は、リソース/非在庫ベースのシナリオ向け Project Operations と、在庫/製造ベースのシナリオ向け Project Operations で使用されます。</span><span class="sxs-lookup"><span data-stu-id="00555-110">The Finance and Operations app environment is used in Project Operations for resource/non-stocked based scenarios and Project Operations for stocked/production-based scenarios.</span></span>

## <a name="project-operations-release-notes"></a><span data-ttu-id="00555-111">Project Operations リリース ノート</span><span class="sxs-lookup"><span data-stu-id="00555-111">Project Operations release notes</span></span>
- <span data-ttu-id="00555-112">[リソース/在庫なし](whats-new-apr-2021-resource-based.md) シナリオに関する Project Operations 最新リリース ノート。</span><span class="sxs-lookup"><span data-stu-id="00555-112">Project Operations latest release notes for [Resource/non-stocked](whats-new-apr-2021-resource-based.md) scenario.</span></span>
- <span data-ttu-id="00555-113">[ライト展開](../pro/whats-new/whats-new-apr-2021-lite.md) シナリオに関する Project Operations 最新リリース ノート。</span><span class="sxs-lookup"><span data-stu-id="00555-113">Project Operations latest release notes for [Lite deployment](../pro/whats-new/whats-new-apr-2021-lite.md) scenario.</span></span>
- <span data-ttu-id="00555-114">[在庫/製造](../prod-pma/whats-new/whats-new-mar-2021-stocked.md) シナリオに関する Project Operations 最新リリース ノート。</span><span class="sxs-lookup"><span data-stu-id="00555-114">Project Operations latest release notes for [stocked/production](../prod-pma/whats-new/whats-new-mar-2021-stocked.md) scenario.</span></span>

## <a name="project-operations-latest-version"></a><span data-ttu-id="00555-115">Project Operations の最新バージョン</span><span class="sxs-lookup"><span data-stu-id="00555-115">Project Operations latest version</span></span>

| <span data-ttu-id="00555-116">Dataverse 環境での Project Operations</span><span class="sxs-lookup"><span data-stu-id="00555-116">Project Operations on Dataverse environment</span></span> | <span data-ttu-id="00555-117">Finance and Operations アプリ環境でのプロジェクト管理および会計</span><span class="sxs-lookup"><span data-stu-id="00555-117">Project management and accounting in Finance and Operations apps environments</span></span> | 
| --- | --- |
| <span data-ttu-id="00555-118">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-118">4.9.0.221</span></span> | <span data-ttu-id="00555-119">10.0.17</span><span class="sxs-lookup"><span data-stu-id="00555-119">10.0.17</span></span> |

<span data-ttu-id="00555-120">Project Operations リソース/非在庫シナリオでは、デュアル書き込みオーケストレーション バージョン 2.2.2.50 以降を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00555-120">For Project Operations Resource/non-stocked scenario, we recommend to use Dual Write Orchestration version 2.2.2.50 or higher.</span></span>

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a><span data-ttu-id="00555-121">Dataverse 環境における Project Operations のリリース スケジュール</span><span class="sxs-lookup"><span data-stu-id="00555-121">Release schedule for Project Operations on Dataverse environment</span></span>

<span data-ttu-id="00555-122">Dataverse 環境における Project Operations の更新は毎月入手できます。</span><span class="sxs-lookup"><span data-stu-id="00555-122">Updates for Project Operations on Dataverse environment are available monthly.</span></span> 

| <span data-ttu-id="00555-123">ステーション</span><span class="sxs-lookup"><span data-stu-id="00555-123">Station</span></span>   | <span data-ttu-id="00555-124">リージョン</span><span class="sxs-lookup"><span data-stu-id="00555-124">Region</span></span>        | <span data-ttu-id="00555-125">現在のバージョン</span><span class="sxs-lookup"><span data-stu-id="00555-125">Current version</span></span> | <span data-ttu-id="00555-126">次のバージョン</span><span class="sxs-lookup"><span data-stu-id="00555-126">Next version</span></span> | <span data-ttu-id="00555-127">一般提供</span><span class="sxs-lookup"><span data-stu-id="00555-127">Generally available</span></span> |
|-----------|---------------|-----------------|--------------|---------------------|
| <span data-ttu-id="00555-128">ステーション 1</span><span class="sxs-lookup"><span data-stu-id="00555-128">Station 1</span></span> |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="00555-129">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="00555-129">First Release</span></span> |  <span data-ttu-id="00555-130">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-130">4.9.0.221</span></span>       | <span data-ttu-id="00555-131">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-131">TBD</span></span>     | <span data-ttu-id="00555-132">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-132">23-Apr-21</span></span>           |
| <span data-ttu-id="00555-133">ステーション 2</span><span class="sxs-lookup"><span data-stu-id="00555-133">Station 2</span></span> |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="00555-134">南米</span><span class="sxs-lookup"><span data-stu-id="00555-134">South America</span></span> |  <span data-ttu-id="00555-135">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-135">4.9.0.221</span></span>       | <span data-ttu-id="00555-136">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-136">TBD</span></span>     | <span data-ttu-id="00555-137">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-137">23-Apr-21</span></span>           |
|    &nbsp; | <span data-ttu-id="00555-138">カナダ</span><span class="sxs-lookup"><span data-stu-id="00555-138">Canada</span></span>        |  <span data-ttu-id="00555-139">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-139">4.9.0.221</span></span>       | <span data-ttu-id="00555-140">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-140">TBD</span></span>     | <span data-ttu-id="00555-141">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-141">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-142">インド</span><span class="sxs-lookup"><span data-stu-id="00555-142">India</span></span>         |  <span data-ttu-id="00555-143">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-143">4.9.0.221</span></span>       | <span data-ttu-id="00555-144">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-144">TBD</span></span>     | <span data-ttu-id="00555-145">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-145">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-146">フランス</span><span class="sxs-lookup"><span data-stu-id="00555-146">France</span></span>         |  <span data-ttu-id="00555-147">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-147">4.9.0.221</span></span>       | <span data-ttu-id="00555-148">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-148">TBD</span></span>     | <span data-ttu-id="00555-149">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-149">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-150">アラブ首長国連邦</span><span class="sxs-lookup"><span data-stu-id="00555-150">United Arab Emirates</span></span>         |  <span data-ttu-id="00555-151">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-151">4.9.0.221</span></span>       | <span data-ttu-id="00555-152">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-152">TBD</span></span>     | <span data-ttu-id="00555-153">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-153">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-154">南アフリカ</span><span class="sxs-lookup"><span data-stu-id="00555-154">South Africa</span></span>         |  <span data-ttu-id="00555-155">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-155">4.9.0.221</span></span>       | <span data-ttu-id="00555-156">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-156">TBD</span></span>     | <span data-ttu-id="00555-157">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-157">23-Apr-21</span></span>           |
| <span data-ttu-id="00555-158">ステーション 3</span><span class="sxs-lookup"><span data-stu-id="00555-158">Station 3</span></span>  |      &nbsp;   |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="00555-159">日本</span><span class="sxs-lookup"><span data-stu-id="00555-159">Japan</span></span>         |  <span data-ttu-id="00555-160">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-160">4.9.0.221</span></span>       | <span data-ttu-id="00555-161">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-161">TBD</span></span>     | <span data-ttu-id="00555-162">2021 年 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="00555-162">30-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-163">アジア太平洋</span><span class="sxs-lookup"><span data-stu-id="00555-163">Asia Pacific</span></span>  |  <span data-ttu-id="00555-164">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-164">4.9.0.221</span></span>       | <span data-ttu-id="00555-165">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-165">TBD</span></span>     | <span data-ttu-id="00555-166">2021 年 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="00555-166">30-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-167">英国</span><span class="sxs-lookup"><span data-stu-id="00555-167">Great Britain</span></span> |  <span data-ttu-id="00555-168">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-168">4.9.0.221</span></span>       | <span data-ttu-id="00555-169">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-169">TBD</span></span>     | <span data-ttu-id="00555-170">2021 年 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="00555-170">30-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="00555-171">オセアニア</span><span class="sxs-lookup"><span data-stu-id="00555-171">Oceania</span></span>       |  <span data-ttu-id="00555-172">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-172">4.9.0.221</span></span>       | <span data-ttu-id="00555-173">TBD</span><span class="sxs-lookup"><span data-stu-id="00555-173">TBD</span></span>     | <span data-ttu-id="00555-174">2021 年 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="00555-174">30-Apr-21</span></span>           |
| <span data-ttu-id="00555-175">ステーション 4</span><span class="sxs-lookup"><span data-stu-id="00555-175">Station 4</span></span> |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="00555-176">欧州</span><span class="sxs-lookup"><span data-stu-id="00555-176">Europe</span></span>        |  <span data-ttu-id="00555-177">4.8.0.92</span><span class="sxs-lookup"><span data-stu-id="00555-177">4.8.0.92</span></span>       | <span data-ttu-id="00555-178">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-178">4.9.0.221</span></span>     | <span data-ttu-id="00555-179">2021 年 4 月 16 日</span><span class="sxs-lookup"><span data-stu-id="00555-179">16-Apr-21</span></span>           |
| <span data-ttu-id="00555-180">ステーション 5</span><span class="sxs-lookup"><span data-stu-id="00555-180">Station 5</span></span> |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="00555-181">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="00555-181">North America</span></span> |  <span data-ttu-id="00555-182">4.8.0.92</span><span class="sxs-lookup"><span data-stu-id="00555-182">4.8.0.92</span></span>       | <span data-ttu-id="00555-183">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="00555-183">4.9.0.221</span></span>     | <span data-ttu-id="00555-184">2021 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="00555-184">23-Apr-21</span></span>           |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a><span data-ttu-id="00555-185">Finance and Operations アプリ環境でのプロジェクト管理および会計のリリース スケジュール</span><span class="sxs-lookup"><span data-stu-id="00555-185">Release schedule for Project management and accounting in the Finance and Operations apps environment</span></span>

<span data-ttu-id="00555-186">プロジェクト管理および会計の更新は、年に 8 回リリースされます。</span><span class="sxs-lookup"><span data-stu-id="00555-186">Updates for Project management and accounting are released eight times a year.</span></span>

| <span data-ttu-id="00555-187">サポートされるリリース</span><span class="sxs-lookup"><span data-stu-id="00555-187">Supported release</span></span> | <span data-ttu-id="00555-188">一般提供 (自己更新)</span><span class="sxs-lookup"><span data-stu-id="00555-188">Generally available (self-update)</span></span> |
| --- | --- |
| <span data-ttu-id="00555-189">10.0.17</span><span class="sxs-lookup"><span data-stu-id="00555-189">10.0.17</span></span> | <span data-ttu-id="00555-190">2021 年 3 月 19 日</span><span class="sxs-lookup"><span data-stu-id="00555-190">March 19, 2021</span></span> |
| <span data-ttu-id="00555-191">10.0.16</span><span class="sxs-lookup"><span data-stu-id="00555-191">10.0.16</span></span> | <span data-ttu-id="00555-192">2021 年 1 月 22 日</span><span class="sxs-lookup"><span data-stu-id="00555-192">January 22, 2021</span></span> |


<span data-ttu-id="00555-193">リリース予定日は変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="00555-193">Targeted release dates are subject to change.</span></span> <span data-ttu-id="00555-194">詳細については、[サービス更新プログラムの提供](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00555-194">For more information, see [Service update availability](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json).</span></span>

| <span data-ttu-id="00555-195">リリース予定日</span><span class="sxs-lookup"><span data-stu-id="00555-195">Targeted release date</span></span> | <span data-ttu-id="00555-196">一般提供 (自己更新)</span><span class="sxs-lookup"><span data-stu-id="00555-196">Generally available (self- updated)</span></span> |
| --- | --- |
| <span data-ttu-id="00555-197">10.0.18</span><span class="sxs-lookup"><span data-stu-id="00555-197">10.0.18</span></span> | <span data-ttu-id="00555-198">2021 年 4 月 16 日</span><span class="sxs-lookup"><span data-stu-id="00555-198">April 16, 2021</span></span> |
| <span data-ttu-id="00555-199">10.0.19</span><span class="sxs-lookup"><span data-stu-id="00555-199">10.0.19</span></span> | <span data-ttu-id="00555-200">2021 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="00555-200">June 18, 2021</span></span> |
| <span data-ttu-id="00555-201">10.0.20</span><span class="sxs-lookup"><span data-stu-id="00555-201">10.0.20</span></span> | <span data-ttu-id="00555-202">2021 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="00555-202">July 16, 2021</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
