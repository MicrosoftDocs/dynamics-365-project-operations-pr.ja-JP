---
title: 価格設定のディメンションとして Project Service 内の既存のフィールドを使用する
description: このトピックでは、価格設定のディメンションとして既存の Project Service フィールドを使用する方法について説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079346"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="960a3-103">価格設定のディメンションとして Project Service 内の既存のフィールドを使用する</span><span class="sxs-lookup"><span data-stu-id="960a3-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="960a3-104">Project Service Automation (PSA) の組織には、プロジェクト組織のリソース ベースの価格設定ディメンションとして使用できる **実績** エンティティに多数のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="960a3-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="960a3-105">たとえば、一つの共通フィールドは **予約可能リソース** です。</span><span class="sxs-lookup"><span data-stu-id="960a3-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="960a3-106">20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="960a3-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="960a3-107">ただし、請求対象の従業員が増加して、リソースが昇進し、経験が増え、あるいは異なるスキルセットを取得するにつれ、リソースのコストと請求レートは変化し始め、これを維持することは非動現実的となります。</span><span class="sxs-lookup"><span data-stu-id="960a3-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="960a3-108">この方法は依然として特定の規模の会社に機能しているため、[価格設定のディメンションとして予約可能リソースを使用する](bookable-resource-pricing-dimension.md) のトピックを参照して、既存の Project Service フィールドが価格設定ディメンションとして使用できるのかを理解してください。</span><span class="sxs-lookup"><span data-stu-id="960a3-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="960a3-109">もう一つの例がトランザクション カテゴリです。</span><span class="sxs-lookup"><span data-stu-id="960a3-109">Another example is that of transaction category.</span></span> <span data-ttu-id="960a3-110">顧客、および実装者は、PSA でトランザクション カテゴリを使用して作業を分類してきました。また、作業のカテゴリに基づく価格とコストのフィールドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="960a3-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="960a3-111">詳細については、 [価格設定のディメンションとして、トランザクション カテゴリを使用する](transaction-category-pricing-dimension.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="960a3-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
