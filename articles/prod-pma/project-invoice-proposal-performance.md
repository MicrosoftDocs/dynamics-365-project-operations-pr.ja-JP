---
title: プロジェクトの仮発行請求書のパフォーマンス
description: このトピックは、プロジェクトの仮発行請求書のパフォーマンス向上に関する情報を提供します。
author: Yowelle
ms.date: 04/20/2021
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999497"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="ac81f-103">プロジェクトの仮発行請求書のパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="ac81f-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac81f-104">新しい仮発行請求書を作成する場合、プロジェクトとサブプロジェクトの数が増えると、パフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ac81f-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="ac81f-105">パフォーマンスを向上させるために、投稿されたプロジェクト トランザクションの新しい仮発行請求書を作成するために必要な時間を短縮する機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ac81f-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="ac81f-106">プロジェクトの仮発行請求書拡張機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="ac81f-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="ac81f-107">プロジェクトの仮発行請求書のパフォーマンス拡張機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="ac81f-108">**機能管理** > **すべて** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="ac81f-109">機能リストで、**プロジェクトの仮発行請求書のパフォーマンス拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="ac81f-110">**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="ac81f-111">ブラウザを更新してから、新しい仮発行請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="ac81f-112">プロジェクトの仮発行請求書拡張機能を無効にする</span><span class="sxs-lookup"><span data-stu-id="ac81f-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="ac81f-113">プロジェクトの仮発行請求書のパフォーマンス拡張機能を無効にする手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="ac81f-114">**機能管理** > **すべて** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="ac81f-115">機能リストで、**プロジェクトの仮発行請求書のパフォーマンス拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="ac81f-116">**無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="ac81f-117">ブラウザーを最新の情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="ac81f-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="ac81f-118">請求ルールが有効になっている場合、またはバッチ プロセスが実行されている場合、仮発行請求書のパフォーマンスは適用できません。</span><span class="sxs-lookup"><span data-stu-id="ac81f-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
