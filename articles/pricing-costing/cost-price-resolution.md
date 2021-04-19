---
title: 見積もりと実績の原価価格を解決する
description: このトピックは、見積もりと原価価格がどのように解決されるかについての情報を提供します。
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877318"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a><span data-ttu-id="6917b-103">見積もりと実績の原価価格を解決する</span><span class="sxs-lookup"><span data-stu-id="6917b-103">Resolving cost prices for estimates and actuals</span></span>

<span data-ttu-id="6917b-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6917b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6917b-105">見積りと実績の原価価格と原価表を解決するには、関連するプロジェクトの **日付**、**通貨**、**契約単位** の各フィールドの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="6917b-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="6917b-106">原価価格を解決した後は、アプリケーションは原価率を解決します。</span><span class="sxs-lookup"><span data-stu-id="6917b-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="6917b-107">時間に向けた実際の明細行と見積もり明細行での原価率の解決</span><span class="sxs-lookup"><span data-stu-id="6917b-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="6917b-108">時間の見積もり明細行は、プロジェクトの時間とリソースの割り当てに関する見積もりと契約品目の詳細を参照します。</span><span class="sxs-lookup"><span data-stu-id="6917b-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="6917b-109">原価価格のリストが解決された後、システムは、価格表のロール価格明細と一致させるために、時間の見積もり明細上の **ロール**、**リソース会社**、**リソース ユニット** のフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6917b-109">After a cost price list is resolved, the system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="6917b-110">この一致は、人件費に既成の価格設定を使用していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="6917b-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="6917b-111">システムが **ロール**、**リソース会社** と **リソース ユニット** のフィールドの代わりに、またはそれに加えて、フィールドに一致するようにシステムを構成した場合は、一致するロールの価格ラインを取得するために別の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6917b-111">If you configured the system to match fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="6917b-112">アプリケーションが、**役割**、**リソース会社**、**リソース ユニット** の組み合わせの原価率を持つ役割の価格ラインを検出した場合、これが既定ののコスト率となります。</span><span class="sxs-lookup"><span data-stu-id="6917b-112">If the application finds a role price line that has a cost rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="6917b-113">アプリケーションが **役割**、**リソース会社**、および **リソース単位** 値の組み合わせと正確に一致しない場合、役割の値が一致する役割価格行を取得しますが、**リソース単位** と **リソース会社** の値は null となります。</span><span class="sxs-lookup"><span data-stu-id="6917b-113">If the application can't exactly match the combination of **Role**, **Resourcing Company**, and **Resourcing Unit** values, it will retrieve role price lines with a matching role value, but have null values for **Resourcing Unit** and **Resourcing Company**.</span></span> <span data-ttu-id="6917b-114">一致する役割の価格値を持つ一致する役割の価格レコードが見つかると、原価率はそのレコードが既定値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6917b-114">After a matching role price record with matching role price value is found, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="6917b-115">**ロール**、**リソース会社**、**リソース ユニット** の異なる優先順位を構成した場合、または優先順位の高い他のディメンジョンがある場合、この動作はそれに応じて変更されます。</span><span class="sxs-lookup"><span data-stu-id="6917b-115">If you configure a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="6917b-116">システムは、優先順位の順に各価格設定ディメンション値に一致する値を持つ役割価格レコードを取得し、優先順位の最後に来る、ディメンションの値が null 値の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="6917b-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last in the priority order.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="6917b-117">経費に向けた実際の明細行と見積もり明細行での原価率の解決</span><span class="sxs-lookup"><span data-stu-id="6917b-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="6917b-118">費用の見積もり明細とは、プロジェクト上の費用の見積もり明細と契約品目の詳細を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6917b-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="6917b-119">原価価格のリストが解決されると、システムは見積り行の **カテゴリー** と **ユニット** フィールドの組み合わせを使用して、解決された価格リストの **カテゴリー価格** 行と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="6917b-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="6917b-120">システムが **カテゴリー** と **ユニット** フィールドの組み合わせで原価率を持つカテゴリ価格ラインを検出した場合、原価率が既定になります。</span><span class="sxs-lookup"><span data-stu-id="6917b-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="6917b-121">**カテゴリ** 値と **単位** の値が一致しない場合や、一致するカテゴリの価格ラインを検出しても、価格設定方法が **単位当たりの価格** ではない場合は、原価率は既定でゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="6917b-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="6917b-122">材料の実績と見積もり行の原価率を解決する</span><span class="sxs-lookup"><span data-stu-id="6917b-122">Resolving cost rates on actual and estimate lines for material</span></span>

<span data-ttu-id="6917b-123">材料の見積もり行は、材料の見積もりおよび契約品目の詳細と、プロジェクトの材料見積もり行を参照します。</span><span class="sxs-lookup"><span data-stu-id="6917b-123">Estimate lines for material refer to the quote and contract line details for materials and the material estimate lines on a project.</span></span>

<span data-ttu-id="6917b-124">原価表が解決された後、システムは解決済み価格表の **価格表品目** に一致する材料見積もりの見積もり行にある **製品** と **単位** の組み合わせを使用します。</span><span class="sxs-lookup"><span data-stu-id="6917b-124">After a cost price list is resolved, the system uses a combination of the **Product** and **Unit** fields on the estimate line for a material estimate to match against the **Price List Items** lines on the resolved price list.</span></span> <span data-ttu-id="6917b-125">システムが、**製品** と **単位** フィールドの組み合わせの原価率を持つ製品価格行を見つけた場合、原価率が既定値になります。</span><span class="sxs-lookup"><span data-stu-id="6917b-125">If the system finds a product price line that has a cost rate for the **Product** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="6917b-126">システムが **製品** と **単位** 値を一致できない場合、単価は既定でゼロになります。</span><span class="sxs-lookup"><span data-stu-id="6917b-126">If the system can't match the **Product** and **Unit** values, the unit cost defaults to zero.</span></span> <span data-ttu-id="6917b-127">この既定値は、一致する価格表品目行がある場合にも発生しますが、価格設定方法は、製品で定義されていない標準原価または現在の原価に基づいています。</span><span class="sxs-lookup"><span data-stu-id="6917b-127">This default will also happen if there is a matching price list item line, but the pricing method is based on a standard cost or current cost that isn't defined in the product.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
