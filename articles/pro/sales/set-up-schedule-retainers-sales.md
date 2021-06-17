---
title: 着手金スケジュールの設定
description: このトピックでは、Project Operations で着手金スケジュールを設定する方法について説明します。
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64bb94d0381696418330e9ba5c26af34a3fb6e5b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994187"
---
# <a name="set-up-a-retainer-schedule"></a><span data-ttu-id="0cc08-103">着手金スケジュールの設定</span><span class="sxs-lookup"><span data-stu-id="0cc08-103">Set up a retainer schedule</span></span>

<span data-ttu-id="0cc08-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="0cc08-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0cc08-105">着手金スケジュールは、Dynamics 365 Project Operations の **プロジェクト契約** ページに設定されます。</span><span class="sxs-lookup"><span data-stu-id="0cc08-105">Retainer schedules are set up on the **Project Contract** page in Dynamics 365 Project Operations.</span></span>

1. <span data-ttu-id="0cc08-106">**プロジェクト契約** ページの **前払金と着手金** タブで、**着手金スケジュールの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-106">On the **Project Contract** page, on the **Advances and Retainers** tab, select **Set up retainer schedule**.</span></span>
2. <span data-ttu-id="0cc08-107">表示されたダイアログ ページに、次の表にリストされているフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0cc08-107">On the dialog page that opens, the fields listed in the following table are shown.</span></span> <span data-ttu-id="0cc08-108">この表は、入力値が、作成される着手金スケジュールにどのような影響を与えるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0cc08-108">The table gives an idea on how the entered values impact or influence the retainer schedule that will be created.</span></span>

| <span data-ttu-id="0cc08-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="0cc08-109">Field</span></span> | <span data-ttu-id="0cc08-110">内容</span><span class="sxs-lookup"><span data-stu-id="0cc08-110">Description</span></span> | <span data-ttu-id="0cc08-111">下位への影響</span><span class="sxs-lookup"><span data-stu-id="0cc08-111">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0cc08-112">プロジェクト契約の顧客</span><span class="sxs-lookup"><span data-stu-id="0cc08-112">Project Contract Customer</span></span> | <span data-ttu-id="0cc08-113">この着手金あるいは前払金の請求を受ける契約上の顧客。</span><span class="sxs-lookup"><span data-stu-id="0cc08-113">The customer on the contract who will be invoiced for this retainer or advance.</span></span> | <span data-ttu-id="0cc08-114">契約に複数の顧客が存在し、それぞれに特定の着手金や前払金を請求する必要がある場合は、それぞれの顧客に 1 つの請求書を手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-114">If you have multiple customers on the contract, and if you need to invoice each of them for a specific retainer or advance amount, manually create one invoice for each customer.</span></span> |
| <span data-ttu-id="0cc08-115">着手金スケジュールの開始</span><span class="sxs-lookup"><span data-stu-id="0cc08-115">Retainer Schedule Start</span></span> | <span data-ttu-id="0cc08-116">着手金スケジュールの開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-116">Enter the start date of the retainer schedule.</span></span> | <span data-ttu-id="0cc08-117">この日付は、最初の着手金または前払金が作成された日付ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0cc08-117">This date may not be the date on which the first retainer or advance is created.</span></span> <span data-ttu-id="0cc08-118">最初の着手金または前払金が作成される日付も、請求頻度の影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="0cc08-118">The date on which the first retainer or advance is created, is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="0cc08-119">着手金スケジュールの終了</span><span class="sxs-lookup"><span data-stu-id="0cc08-119">Retainer Schedule End</span></span> | <span data-ttu-id="0cc08-120">着手金スケジュールの終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-120">Enter the end date of the retainer schedule.</span></span> | <span data-ttu-id="0cc08-121">この日付は、最後の着手金または前払金が作成された日付ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0cc08-121">This date may not be the date on which the last retainer or advance is created.</span></span> <span data-ttu-id="0cc08-122">最後の着手金または前払金が作成される日付も、請求頻度の影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="0cc08-122">The date on which the last retainer or advance is created is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="0cc08-123">作成する着手金の数</span><span class="sxs-lookup"><span data-stu-id="0cc08-123">Number of Retainers to Create</span></span> | <span data-ttu-id="0cc08-124">作成する着手金の数を入力すると、システムは開始日と頻度を使用して、このフィールドに数を作成します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-124">When you enter the number of retainers to create, the system uses the start date and frequency to create the number in this field.</span></span> | <span data-ttu-id="0cc08-125">このフィールドが手動で更新されると、システムは **着手金スケジュールの終了** フィールドの値を無視し、代わりに、特定の数の着手金または前払金を作成します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-125">When this field is manually updated, the system ignores the value in the **Retainer Schedule End** field and instead creates the specific number of retainers or advances.</span></span> |
| <span data-ttu-id="0cc08-126">請求頻度</span><span class="sxs-lookup"><span data-stu-id="0cc08-126">Invoice Frequency</span></span> | <span data-ttu-id="0cc08-127">アプリケーションが着手金と前払金を作成する頻度。</span><span class="sxs-lookup"><span data-stu-id="0cc08-127">How often the application will create retainers and advances.</span></span> | <span data-ttu-id="0cc08-128">この値は、着手金と前払金の数、および作成日に直接影響します。</span><span class="sxs-lookup"><span data-stu-id="0cc08-128">This value directly influences the number of retainers and advances and the created dates.</span></span> |
| <span data-ttu-id="0cc08-129">合計金額</span><span class="sxs-lookup"><span data-stu-id="0cc08-129">Total Amount</span></span> | <span data-ttu-id="0cc08-130">合計金額は、作成される個々の着手金または前払金に分割された金額です。</span><span class="sxs-lookup"><span data-stu-id="0cc08-130">The total amount is the amount that is split into the individual retainer or advance payments that will be created.</span></span> | <span data-ttu-id="0cc08-131">このフィールドから下位への影響はありません。</span><span class="sxs-lookup"><span data-stu-id="0cc08-131">There's no downstream impact for this field.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]