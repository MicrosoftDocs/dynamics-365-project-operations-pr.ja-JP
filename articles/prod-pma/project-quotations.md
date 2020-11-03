---
title: プロジェクト見積
description: この記事では、プロジェクト フェーズの最初のステップとして、顧客に魅力的なオファーを提供するために使用できるプロジェクト見積の概念を紹介します。 プロジェクト見積には、見積もられたアイテムやサービス、基本的な連絡先情報、特別な売買契約や割引き、税金や割増金が含まれる場合があります。
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationProjTable
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23621
ms.assetid: 1ba67109-8c5b-4ada-b730-a72cd46203fd
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ffb8d4bfefac52f65245f4ed6e4be216f5dc10e7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079255"
---
# <a name="project-quotations"></a><span data-ttu-id="93ebe-104">プロジェクト見積</span><span class="sxs-lookup"><span data-stu-id="93ebe-104">Project quotations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93ebe-105">この記事では、プロジェクト フェーズの最初のステップとして、顧客に魅力的なオファーを提供するために使用できるプロジェクト見積の概念を紹介します。</span><span class="sxs-lookup"><span data-stu-id="93ebe-105">This article introduces the concept of project quotations, which you can use to make an attractive offer to a customer as the first step of the project phase.</span></span> <span data-ttu-id="93ebe-106">プロジェクト見積には、見積もられたアイテムやサービス、基本的な連絡先情報、特別な売買契約や割引き、税金や割増金が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="93ebe-106">A project quotation might include the items and services that are quoted, basic contact information, special trade agreements and discounts, and possible taxes and surcharges.</span></span> 

<span data-ttu-id="93ebe-107">プロジェクト見積と受注のパイプラインを監視、確認、制御する機能は、プロジェクト管理の重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="93ebe-107">The ability to monitor, review, and control the pipeline of project quotations and orders is an important part of project management.</span></span> <span data-ttu-id="93ebe-108">これらのタスクにはさまざまなツールが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-108">Various tools can help with these tasks.</span></span> <span data-ttu-id="93ebe-109">たとえば、正しい参照データ定義 (見積タイプ、見積元、予後と確率) は、パイプラインの分析に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-109">For example, correct reference data definitions (quotation types, quotation origin, and prognosis and probability) help you analyze the pipeline.</span></span> <span data-ttu-id="93ebe-110">これらのツールを使用して、プロジェクト見積が受注または失注した理由を分類し、見積の潜在的な価値を判断できます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-110">You can use these tools to categorize the reasons why a project quotation was won or lost, and to determine the potential value of a quotation.</span></span> 

<span data-ttu-id="93ebe-111">プロジェクト見積には、プロジェクトのサービス、基本的な連絡先情報、特別な売買契約や割引き、税金や割増金の見積額を入力します。</span><span class="sxs-lookup"><span data-stu-id="93ebe-111">In a project quotation, you enter the services, basic contact information, special trade agreements and discounts, and estimated taxes and surcharges for a project.</span></span> <span data-ttu-id="93ebe-112">プロジェクトの活動またはタスクを選択して、タスクとサブタスクの階層を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-112">You can also select the activities or tasks for a project, and create a hierarchy of tasks and subtasks.</span></span> <span data-ttu-id="93ebe-113">活動ごとに、活動のタイミングと期間に関する詳細、および活動を実行する作業者に必要なスキルと経験に関する詳細を入力できます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-113">For each activity, you can enter details about the timing and duration of the activity, and about the skills and experience that are required for workers who perform the activity.</span></span> 

<span data-ttu-id="93ebe-114">プロジェクトの見積は、実行する必要がある作業の非バインド見積です。</span><span class="sxs-lookup"><span data-stu-id="93ebe-114">The project quotation is a non-binding estimate of the work that must be performed.</span></span> <span data-ttu-id="93ebe-115">ただし、見積の情報がプロジェクト契約に関連付けられているプロジェクトにコピーされた場合、その情報は両当事者間のバインド アグリーメントの一部になります。</span><span class="sxs-lookup"><span data-stu-id="93ebe-115">However, when the information in the quotation is copied to a project that is associated with a project contract, that information becomes part of a binding agreement between two parties.</span></span> 

<span data-ttu-id="93ebe-116">顧客がプロジェクト見積を承認した場合、プロジェクト見積の情報をプロジェクトにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-116">If the customer approves the project quotation, you can copy the information in the project quotation to a project.</span></span> <span data-ttu-id="93ebe-117">プロジェクト見積の情報をプロジェクト予測に同時にコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="93ebe-117">You can also copy the project quotation information to a project forecast at the same time.</span></span>



