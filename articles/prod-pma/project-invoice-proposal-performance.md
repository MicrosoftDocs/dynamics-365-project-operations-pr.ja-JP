---
title: プロジェクトの仮発行請求書のパフォーマンス
description: このトピックは、プロジェクトの仮発行請求書のパフォーマンス向上に関する情報を提供します。
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269796"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="2a560-103">プロジェクトの仮発行請求書のパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="2a560-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a560-104">新しい仮発行請求書を作成する場合、プロジェクトとサブプロジェクトの数が増えると、パフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a560-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="2a560-105">パフォーマンスを向上させるために、投稿されたプロジェクト トランザクションの新しい仮発行請求書を作成するために必要な時間を短縮する機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="2a560-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="2a560-106">プロジェクトの仮発行請求書拡張機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="2a560-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="2a560-107">プロジェクトの仮発行請求書のパフォーマンス拡張機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a560-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="2a560-108">**機能管理** > **すべて** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a560-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="2a560-109">機能リストで、**プロジェクトの仮発行請求書のパフォーマンス拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a560-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="2a560-110">**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a560-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="2a560-111">ブラウザを更新してから、新しい仮発行請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a560-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="2a560-112">プロジェクトの仮発行請求書拡張機能を無効にする</span><span class="sxs-lookup"><span data-stu-id="2a560-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="2a560-113">プロジェクトの仮発行請求書のパフォーマンス拡張機能を無効にする手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a560-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="2a560-114">**機能管理** > **すべて** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a560-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="2a560-115">機能リストで、**プロジェクトの仮発行請求書のパフォーマンス拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a560-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="2a560-116">**無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a560-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="2a560-117">ブラウザーを最新の情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="2a560-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="2a560-118">請求ルールが有効な場合、請求書の提案パフォーマンスが適用できません。</span><span class="sxs-lookup"><span data-stu-id="2a560-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="2a560-119">請求書案を作成するバッチ処理では、サブタスクの数は、入力した内容にかかわらず、請求書発行可能な取引のある契約数に応じた最大数にタスクが分割されます。</span><span class="sxs-lookup"><span data-stu-id="2a560-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="2a560-120">たとえば、一括で請求書案を作成するサブタスクの数に **3** を入力した場合でも、請求書発行可能な取引がある契約が 2 つしかないと、サブタスクは 2 つしか作成されません。</span><span class="sxs-lookup"><span data-stu-id="2a560-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
