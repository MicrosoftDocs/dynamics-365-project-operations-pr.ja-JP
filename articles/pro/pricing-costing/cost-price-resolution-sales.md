---
title: プロジェクトの見積もりと実績の原価価格を解決する
description: このトピックは、プロジェクトの見積もりと実績のコスト価格がどのように解決されるかについての情報を提供します。
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9f20631f41c560f1a4047aaaa624fa4e8651c687
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877271"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a><span data-ttu-id="aa100-103">プロジェクトの見積もりと実績の原価価格を解決する</span><span class="sxs-lookup"><span data-stu-id="aa100-103">Resolve cost prices on project estimates and actuals</span></span> 

<span data-ttu-id="aa100-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="aa100-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aa100-105">見積りと実績の原価価格と原価表を解決するには、関連するプロジェクトの **日付**、**通貨**、**契約単位** の各フィールドの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="aa100-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="aa100-106">原価価格を解決した後は、アプリケーションは原価率を解決します。</span><span class="sxs-lookup"><span data-stu-id="aa100-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="aa100-107">時間に向けた実際の明細行と見積もり明細行での原価率の解決</span><span class="sxs-lookup"><span data-stu-id="aa100-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="aa100-108">時間の見積もり明細行は、プロジェクトの時間とリソースの割り当てに関する見積もりと契約品目の詳細を参照します。</span><span class="sxs-lookup"><span data-stu-id="aa100-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="aa100-109">コスト価格表が解決されると、時間の見積行の **ロール** と **リソース単位** フィールドが価格表のロール価格明細行と照合されます。</span><span class="sxs-lookup"><span data-stu-id="aa100-109">After a cost price list is resolved, the **Role** and **Resourcing Unit** fields on the estimate line for Time are matched against the role price lines in the price list.</span></span> <span data-ttu-id="aa100-110">この一致は、人件費に標準の価格設定ディメンションを使用していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="aa100-110">This match assumes that you're using the standard pricing dimensions for labor cost.</span></span> <span data-ttu-id="aa100-111">システムがフィールドを一致させるように設定した場合は、代わりに、または **ロール** と **リソース ユニット** に加えて、別の組み合わせを使用して、一致する役割の価格ラインを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa100-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="aa100-112">アプリケーションが **ロール** と **リソーシング ユニット** の組み合わせの原価率を持つロール プライス ラインを検出した場合、それが既定の原価率となります。</span><span class="sxs-lookup"><span data-stu-id="aa100-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="aa100-113">アプリケーションが **ロール** と **リソース ユニット** の値を一致させることができない場合、一致するロールを持つロール価格行を取得しますが、**リソース ユニット** の null 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="aa100-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="aa100-114">一致するロールの価格レコードが設定されると、そのレコードからの原価率が既定となります。</span><span class="sxs-lookup"><span data-stu-id="aa100-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="aa100-115">**ロール**、**リソース ユニット** の優先順位が異なる構成になっている場合や、優先順位の高い他のディメンジョンがある場合は、それに応じてこの動作が変化します。</span><span class="sxs-lookup"><span data-stu-id="aa100-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="aa100-116">システムは、各価格設定ディメンション値のそれぞれに一致する値を持つロール価格レコードを優先度の高い順に取得し、それらのディメンションの null 値を持つ行が最後に来るようにします。</span><span class="sxs-lookup"><span data-stu-id="aa100-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="aa100-117">経費に向けた実際の明細行と見積もり明細行での原価率の解決</span><span class="sxs-lookup"><span data-stu-id="aa100-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="aa100-118">費用の見積もり明細とは、プロジェクト上の費用の見積もり明細と契約品目の詳細を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa100-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="aa100-119">原価価格表が解決された後、システムは経費見積行の **カテゴリ** と **単位** フィールドの組み合わせを使って、、解決された価格表の **カテゴリ価格** 行に突き合わせます。</span><span class="sxs-lookup"><span data-stu-id="aa100-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the expense estimate line to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="aa100-120">システムが **カテゴリー** と **ユニット** フィールドの組み合わせで原価率を持つカテゴリ価格ラインを検出した場合、原価率が既定になります。</span><span class="sxs-lookup"><span data-stu-id="aa100-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="aa100-121">システムが **カテゴリ** と **単位** 値を一致できない、または一致するカテゴリの価格明細行を見つけることができるが、価格設定方法が **出荷単位ごとの価格** でない場合、コスト率がデフォルトのゼロ (0) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="aa100-121">If the system can't match the **Category** and **Unit** values, or if it's able to find a matching category price line but the pricing method isn't **Price Per Unit**, the cost rate defaults to zero(0).</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="aa100-122">材料の実績と見積もり行の原価率を解決する</span><span class="sxs-lookup"><span data-stu-id="aa100-122">Resolving cost rates on actual and estimate lines for Material</span></span>

<span data-ttu-id="aa100-123">材料の見積もり行は、材料の見積もりおよび契約品目の詳細と、プロジェクトの材料見積もり行を参照します。</span><span class="sxs-lookup"><span data-stu-id="aa100-123">Estimate lines for Material refer to the quote and contract line details for materials and the material estimate lines on a project.</span></span>

<span data-ttu-id="aa100-124">原価表が解決された後、システムは解決済み価格表の **価格表品目** に一致する材料見積もりの見積もり行にある **製品** と **単位** の組み合わせを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa100-124">After a cost price list is resolved, the system uses a combination of the **Product** and **Unit** fields on the estimate line for a material estimate to match against the **Price List Items** lines on the resolved price list.</span></span> <span data-ttu-id="aa100-125">システムが、**製品** と **単位** フィールドの組み合わせの原価率を持つ製品価格行を見つけた場合、原価率が既定値になります。</span><span class="sxs-lookup"><span data-stu-id="aa100-125">If the system finds a product price line that has a cost rate for the **Product** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="aa100-126">システムが **製品** と **単位** 値を一致できない、または一致する価格表品目行を見つけることができたが、価格設定方法が標準原価または現在原価に基づいており、どちらも製品に定義されていない場合、単価は既定でゼロになります。</span><span class="sxs-lookup"><span data-stu-id="aa100-126">If the system can't match the **Product** and **Unit** values, or if it's able to find a matching price list item line but the pricing method is based on Standard cost or Current cost and neither is defined on the product, the unit cost defaults to zero.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
