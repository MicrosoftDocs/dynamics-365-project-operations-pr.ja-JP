---
title: 固定価格売上見積もりプロジェクト
description: このトピックは、プロジェクトの固定価格売上に関する情報を提供します。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013807"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="f8ceb-103">固定価格売上見積もりプロジェクト</span><span class="sxs-lookup"><span data-stu-id="f8ceb-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="f8ceb-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f8ceb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f8ceb-105">Microsoft Dataverse の Dynamics 365 Project Operations で以下の属性を使用してプロジェクト契約品目を作成すると、システムは固定価格の売上見積もりプロジェクトを自動で作成します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="f8ceb-106">このプロジェクトの情報は、以下に基づいています。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="f8ceb-107">固定価格の請求方法。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="f8ceb-108">関連するプロジェクト。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-108">An associated project.</span></span>
  - <span data-ttu-id="f8ceb-109">**プロジェクト契約品目** ページの **請求スケジュール** タブで定義した少なくとも 1 件のマイルストーン。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="f8ceb-110">固定価格の売上見積もりプロジェクトを確認する</span><span class="sxs-lookup"><span data-stu-id="f8ceb-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="f8ceb-111">固定価格の売上見積もりプロジェクトを確認する際は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="f8ceb-112">Dynamics 365 Finance 環境で **プロジェクト管理と会計** > **プロジェクト** > **固定価格の売上見積もりプロジェクト** に順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="f8ceb-113">確認するプロジェクトを選択し、**見積もりプロジェクト ID** をダブルクリックしてレコードを開き、プロジェクトの詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="f8ceb-114">**プロジェクト** タブを展開します。**選択したプロジェクト** グリッドに 1 件のプロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="f8ceb-115">これはプロジェクト契約品目に関連付けられたプロジェクトなので、これを既定プロジェクトとしてシステムが使用します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="f8ceb-116">関連付けを変更する場合はさらにプロジェクトを選択して、それらを **選択したプロジェクト** グリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="f8ceb-117">このグリッドで複数のプロジェクトを選択すると、選択したすべてのプロジェクトに対してプロジェクトの完了割合と収益の見積もりを一緒に計算します。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="f8ceb-118">プロジェクトのコスト、売上プロファイル、コスト テンプレート、期間コードを手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="f8ceb-119">手動で設定しない場合は、プロジェクトのコストと売上プロファイルに対して構成したルールを使用するプロジェクトの最初の見積もり計算時に、この値が既定になります。</span><span class="sxs-lookup"><span data-stu-id="f8ceb-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]