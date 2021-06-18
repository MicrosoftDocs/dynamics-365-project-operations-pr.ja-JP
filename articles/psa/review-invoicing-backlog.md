---
title: プロジェクトおよびプロジェクト契約の請求バックログをレビューする
description: このトピックでは、時間、経費、製品バックログをレビューする方法と、「請求準備完了」としてマークする方法について説明します。
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008542"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="a5f78-103">プロジェクトおよびプロジェクト契約の請求バックログをレビューする</span><span class="sxs-lookup"><span data-stu-id="a5f78-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a5f78-104">トランザクション準備ができ、請求書が作成され、処理されたとき、トランザクションは **請求準備完了** としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="a5f78-105">このトピックでは、作成できるトランザクションの種類について説明します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="a5f78-106">時間と材料の請求バックログのレビュー</span><span class="sxs-lookup"><span data-stu-id="a5f78-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="a5f78-107">時間または経費エントリがプロジェクトに送信され承認されると、PSA によってプロジェクトの実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="a5f78-108">プロジェクトの組み合わせとトランザクション クラスが時間‐材料プロジェクトの契約品目にマップされている場合、2 つの実績はエントリが承認された時点で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="a5f78-109">コストの実績</span><span class="sxs-lookup"><span data-stu-id="a5f78-109">Cost actual</span></span> 
- <span data-ttu-id="a5f78-110">未請求売上の実績</span><span class="sxs-lookup"><span data-stu-id="a5f78-110">Unbilled sales actual</span></span>

<span data-ttu-id="a5f78-111">未請求売上の実績によって請求バックログが示され、請求書の状態を **請求準備完了** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5f78-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="a5f78-112">プロジェクトの請求書を作成すると、未請求営業の実績は **請求準備完了** とマークされ、請求品目の詳細にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="a5f78-113">時間と資料の請求バックログ数をレビューするには、**営業**\>**請求書**\>**時間と材料の請求バックログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="a5f78-114">請求準備完了となっているすべての未請求売上の実績を選択して、 **請求準備完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="a5f78-115">請求書の実績の状態は **請求準備完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![時間と材料の請求バックログ](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="a5f78-117">製品の請求バックログのレビュー</span><span class="sxs-lookup"><span data-stu-id="a5f78-117">Review the product billing backlog</span></span>

<span data-ttu-id="a5f78-118">PSAで、プロジェクト契約に製品ベースの契約品目が含まれている場合、それらの品目は、請求書がプロジェクト契約ごとに作成されるたびに請求書の対象となります。</span><span class="sxs-lookup"><span data-stu-id="a5f78-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="a5f78-119">**請求準備完了** とマークされた契約品目が存在する製品は、プロジェクトの請求品目としてプロジェクトの請求書にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="a5f78-120">製品の請求バックログを確認するには、**営業**\>**請求書**\>**製品の請求バックログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="a5f78-121">請求準備完了となっているすべて製品ベースの契約品目を選択して、 **請求準備完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="a5f78-122">これらの品目に関する請求書の状態は **請求準備完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![製品の請求バックログ](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="a5f78-124">固定価格の契約に関する請求マイルストーンのレビュー</span><span class="sxs-lookup"><span data-stu-id="a5f78-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="a5f78-125">固定価格の請求方法を持つ各プロジェクトの契約品目を用いて、契約のマイルストーンを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5f78-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="a5f78-126">これらの契約のマイルストーンが **請求準備完了** とマークされている場合にのみ、請求を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="a5f78-127">請求マイルストーンをレビューするには、**営業**\>**請求書**\>**固定価格のマイルストーン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="a5f78-128">請求準備完了となっているマイルストーンを選択して、**請求準備完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5f78-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="a5f78-129">これらのマイルストーンの請求の状態は **請求準備完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="a5f78-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![固定価格マイルストーン](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]