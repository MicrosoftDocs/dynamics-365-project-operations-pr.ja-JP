---
title: 請求書自動作成の構成
description: このトピックでは、請求書を自動的に生成するシステムの設定方法について説明します。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122439"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="626fc-103">請求書自動作成の構成</span><span class="sxs-lookup"><span data-stu-id="626fc-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="626fc-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="626fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="626fc-105">Dynamics 365 プロジェクト オペレーションで請求書の自動生成の実行を構成するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="626fc-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="626fc-106">**設定** > **バッチ ジョブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="626fc-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="626fc-107">バッチ ジョブを作成して、 **プロジェクト オペレーション請求書の作成** と名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="626fc-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="626fc-108">バッチ ジョブの名前に、「請求書の作成」という語句を含めてください。</span><span class="sxs-lookup"><span data-stu-id="626fc-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="626fc-109">**ジョブの種類** フィールドで、 **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626fc-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="626fc-110">既定で、 **頻度 毎日** および **アクティブ** オプションは **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="626fc-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="626fc-111">**ワークフローの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626fc-111">Select **Run Workflow**.</span></span> <span data-ttu-id="626fc-112">**レコードの検索** ダイアログ ボックスで、 3 つのワークフローが表示されます:</span><span class="sxs-lookup"><span data-stu-id="626fc-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="626fc-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="626fc-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="626fc-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="626fc-114">ProcessRunner</span></span>
    - <span data-ttu-id="626fc-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="626fc-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="626fc-116">**ProcessRunCaller** を選択し、そして **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626fc-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="626fc-117">次のダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626fc-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="626fc-118">**スリープ** ワークフローの後に、 **プロセス** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="626fc-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="626fc-119">ステップ 5 で、 **ProcessRunner** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="626fc-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="626fc-120">**OK** を選択すると、 **プロセス** ワークフロー の後には、 **スリープ** ワークフローが続きます。</span><span class="sxs-lookup"><span data-stu-id="626fc-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="626fc-121">**ProcessRunCaller** および **ProcessRunner** ワークフローは、請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="626fc-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="626fc-122">**ProcessRunCaller** は **ProcessRunner** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="626fc-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="626fc-123">**ProcessRunner** は、実際に請求書を作成するワークフローです。</span><span class="sxs-lookup"><span data-stu-id="626fc-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="626fc-124">請求書を作成する必要のあるすべての契約品目を調べ、それらの明細の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="626fc-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="626fc-125">契約書を作成する契約品目を決定するために、ジョブは契約品目の請求書の実行日を参照します。</span><span class="sxs-lookup"><span data-stu-id="626fc-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="626fc-126">1 つの契約に属する契約品目の請求書実行日が同じ場合、トランザクションは、 2 つの請求明細行を持つ 1 つの請求書に統合されます。</span><span class="sxs-lookup"><span data-stu-id="626fc-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="626fc-127">請求書を作成するトランザクションがない場合、ジョブは請求書の作成をスキップします。</span><span class="sxs-lookup"><span data-stu-id="626fc-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="626fc-128">**ProcessRunner** の実行が完了すると、 **ProcessRunCaller** を呼び出して、終了時間が指定されてクローズされます。</span><span class="sxs-lookup"><span data-stu-id="626fc-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="626fc-129">**ProcessRunCaller** は、指定された終了時刻から24時間実行するタイマーを開始します。</span><span class="sxs-lookup"><span data-stu-id="626fc-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="626fc-130">タイマーが終了すると、 **ProcessRunCaller** が閉じられます。</span><span class="sxs-lookup"><span data-stu-id="626fc-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="626fc-131">請求書を作成するバッチ処理ジョブは、定期的なジョブです。</span><span class="sxs-lookup"><span data-stu-id="626fc-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="626fc-132">このバッチ処理を何度も実行すると、ジョブの複数のインスタンスが作成され、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="626fc-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="626fc-133">したがって、バッチ処理は一度だけ実行し、実行が停止した場合のみ、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626fc-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="626fc-134">バッチ請求は、請求スケジュールで構成されたプロジェクト契約明細に対してのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="626fc-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="626fc-135">固定価格の請求方法の契約品目には、マイルストーンを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626fc-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="626fc-136">時間と材料の請求方法を持つプロジェクト契約品目には、日付ベースの請求スケジュールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626fc-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="626fc-137">これは、プロジェクトベースの契約品目でも同じです。</span><span class="sxs-lookup"><span data-stu-id="626fc-137">The same applies to a project-based contract line.</span></span>     
