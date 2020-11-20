---
title: 見積もりと実績の原価価格を解決する (ライト)
description: このトピックでは、見積もりや原価価格がどのように解決されるのかについて説明します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176797"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a><span data-ttu-id="8b3ba-103">見積もりと実績の原価価格を解決する (ライト)</span><span class="sxs-lookup"><span data-stu-id="8b3ba-103">Resolve cost prices on estimates and actuals - lite</span></span>

<span data-ttu-id="8b3ba-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="8b3ba-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b3ba-105">見積りと実績の原価価格と原価表を解決するには、関連するプロジェクトの **日付**、**通貨**、**契約単位** の各フィールドの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="8b3ba-106">原価価格を解決した後は、アプリケーションは原価率を解決します。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="8b3ba-107">時間に向けた実際の明細行と見積もり明細行での原価率の解決</span><span class="sxs-lookup"><span data-stu-id="8b3ba-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="8b3ba-108">時間の見積もり明細行は、プロジェクトの時間とリソースの割り当てに関する見積もりと契約品目の詳細を参照します。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="8b3ba-109">原価価格のリストが解決された後、システムは、価格表のロール価格明細と一致させるために、時間の見積もり明細上の **ロール**、**リソース ユニット** のフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-109">After a cost price list is resolved, the system uses the **Role** and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="8b3ba-110">この一致は、人件費に既成の価格設定を使用していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="8b3ba-111">システムがフィールドを一致させるように設定した場合は、代わりに、または **ロール** と **リソース ユニット** に加えて、別の組み合わせを使用して、一致する役割の価格ラインを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="8b3ba-112">アプリケーションが **ロール** と **リソーシング ユニット** の組み合わせの原価率を持つロール プライス ラインを検出した場合、それが既定の原価率となります。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="8b3ba-113">アプリケーションが **ロール** と **リソース ユニット** の値を一致させることができない場合、一致するロールを持つロール価格行を取得しますが、**リソース ユニット** の null 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="8b3ba-114">一致するロールの価格レコードが設定されると、そのレコードからの原価率が既定となります。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b3ba-115">**ロール**、**リソース ユニット** の優先順位が異なる構成になっている場合や、優先順位の高い他のディメンジョンがある場合は、それに応じてこの動作が変化します。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="8b3ba-116">システムは、各価格設定ディメンション値のそれぞれに一致する値を持つロール価格レコードを優先度の高い順に取得し、それらのディメンションの null 値を持つ行が最後に来るようにします。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="8b3ba-117">経費に向けた実際の明細行と見積もり明細行での原価率の解決</span><span class="sxs-lookup"><span data-stu-id="8b3ba-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="8b3ba-118">費用の見積もり明細とは、プロジェクト上の費用の見積もり明細と契約品目の詳細を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="8b3ba-119">原価価格のリストが解決されると、システムは見積り行の **カテゴリー** と **ユニット** フィールドの組み合わせを使用して、解決された価格リストの **カテゴリー価格** 行と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="8b3ba-120">システムが **カテゴリー** と **ユニット** フィールドの組み合わせで原価率を持つカテゴリ価格ラインを検出した場合、原価率が既定になります。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="8b3ba-121">**カテゴリ** 値と **単位** の値が一致しない場合や、一致するカテゴリの価格ラインを検出しても、価格設定方法が **単位当たりの価格** ではない場合は、原価率は既定でゼロ (0) になります。</span><span class="sxs-lookup"><span data-stu-id="8b3ba-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>
