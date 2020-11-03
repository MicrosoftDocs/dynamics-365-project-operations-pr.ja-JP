---
title: 価格設定のディメンションとしてのプロジェクト オペレーションフィールド
description: このトピックでは、Dynamics 365 プロジェクト オペレーションでフィールドを価格ディメンションとして使用する方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079331"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="1df5d-103">価格設定のディメンションとしてのプロジェクト オペレーションフィールド</span><span class="sxs-lookup"><span data-stu-id="1df5d-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="1df5d-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1df5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1df5d-105">**実績** エンティティには、リソースベースの料金設定に使用する料金設定ディメンションとして使用できる多くのフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="1df5d-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="1df5d-106">たとえば、一つの共通フィールドは **予約可能リソース** です。</span><span class="sxs-lookup"><span data-stu-id="1df5d-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="1df5d-107">20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1df5d-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="1df5d-108">ただし、請求対象の労働力が増大するにつれて、リソースに応じたレートを維持することが非現実的になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1df5d-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="1df5d-109">リソースのコストと請求レートは、リソースが昇進したり、より多くの経験を積んだり、異なるセットのスキルを身につけることで変化し始めます。</span><span class="sxs-lookup"><span data-stu-id="1df5d-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="1df5d-110">もう一つの例がトランザクション カテゴリです。</span><span class="sxs-lookup"><span data-stu-id="1df5d-110">Another example is that of transaction category.</span></span> <span data-ttu-id="1df5d-111">顧客と実施者は、トランザクション カテゴリを使用して作業を分類し、フィールドを使用して作業カテゴリに基づいて価格とコストを設定します。</span><span class="sxs-lookup"><span data-stu-id="1df5d-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
