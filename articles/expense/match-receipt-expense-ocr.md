---
title: OCR を使用した領収書と経費の照合
description: このトピックでは、領収書の光学式文字認識 (OCR) 処理に関する説明をします。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124329"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="1eefa-103">OCR を使用した領収書と経費の照合</span><span class="sxs-lookup"><span data-stu-id="1eefa-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="1eefa-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1eefa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1eefa-105">領収書の光学式文字認識 (OCR) 処理が導入され、経費入力が強化されました。</span><span class="sxs-lookup"><span data-stu-id="1eefa-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="1eefa-106">この機能は、経費報告書を作成する際のユーザー エクスペリエンスを向上させるように意図されています。</span><span class="sxs-lookup"><span data-stu-id="1eefa-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="1eefa-107">主な機能</span><span class="sxs-lookup"><span data-stu-id="1eefa-107">Key features</span></span>

- <span data-ttu-id="1eefa-108">システムは、領収書からマーチャント名、日付、および合計金額を抽出します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="1eefa-109">システムは、添付されていない領収書を添付されていない経費トランザクションとの照合を試みます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="1eefa-110">領収書から手動で入力した経費取引を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="1eefa-111">領収書を経費報告書に添付する</span><span class="sxs-lookup"><span data-stu-id="1eefa-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="1eefa-112">経費報告書の作成時にクレジットカード取引を含む領収書を自動的に添付するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="1eefa-113">**経費管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="1eefa-114">**領収書** タブで、添付されていないレシートが存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1eefa-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="1eefa-115">**領収書** タブで領収書をアップロードすることも可能です。</span><span class="sxs-lookup"><span data-stu-id="1eefa-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="1eefa-116">**経費** タブで、添付されていない経費が存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1eefa-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="1eefa-117">一般的には、経費管理者はこれら経費をクレジットカード プロバイダーからインポートします。</span><span class="sxs-lookup"><span data-stu-id="1eefa-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="1eefa-118">**新規経費報告書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-118">Select **New expense report**.</span></span> <span data-ttu-id="1eefa-119">経費報告書を作成する際に、経費と領収書を含めることができることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1eefa-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="1eefa-120">経費と領収書の両方を追加すると、経費に対する領収書の自動照合がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="1eefa-121">領収書の作成や領収書と経費報告書を照合する</span><span class="sxs-lookup"><span data-stu-id="1eefa-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="1eefa-122">経費の作成や領収書から経費を照合するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="1eefa-123">経費報告書の **領収書** タブで、**領収書を追加する** を選択して領収書を添付します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="1eefa-124">アップロードされた領収書の画像の下部に、**作成** と **照合** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="1eefa-125">**作成** を選択して手動で入力した経費取引を作成し、領収書から抽出した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="1eefa-126">**照合** を選択した場合、システムは既存の経費を領収書と照合します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="1eefa-127">インストール</span><span class="sxs-lookup"><span data-stu-id="1eefa-127">Installation</span></span>

<span data-ttu-id="1eefa-128">このような高度な経費の機能を使用するには、Microsoft Dynamics 365 Finance 用の経費管理サービス アドインをインストールし、インスタンスの機能をオンにしてください。</span><span class="sxs-lookup"><span data-stu-id="1eefa-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="1eefa-129">Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからアドインにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="1eefa-130">LCS にサインインし、対象とする環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="1eefa-131">**完全な詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="1eefa-132">**管理** を選択し、**環境アドイン** クイックタブまで下方向にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="1eefa-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="1eefa-133">**新しいアドインをインストールする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="1eefa-134">**経費管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="1eefa-135">インストール ガイドに従い、利用規約に同意してください。</span><span class="sxs-lookup"><span data-stu-id="1eefa-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="1eefa-136">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-136">Select **Install**.</span></span>

<span data-ttu-id="1eefa-137">**機能管理** ワークスペースにて、次の機能をオンにします :</span><span class="sxs-lookup"><span data-stu-id="1eefa-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="1eefa-138">再構築された経費報告書</span><span class="sxs-lookup"><span data-stu-id="1eefa-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="1eefa-139">領収書から経費を自動照合して作成する</span><span class="sxs-lookup"><span data-stu-id="1eefa-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="1eefa-140">これらの機能をオンにすると、次のアクションが発生します :</span><span class="sxs-lookup"><span data-stu-id="1eefa-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="1eefa-141">既存の **経費管理** ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="1eefa-142">経費フィールドの表示に使用する新たなメニュー項目が追加されました。</span><span class="sxs-lookup"><span data-stu-id="1eefa-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="1eefa-143">以前の **経費報告書** ページには、**経費管理 > 自分の経費 > 経費報告書** に移動すると表示することができます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="1eefa-144">ワークフローや承認では、既存の経費報告書のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="1eefa-145">領収書は Microsoft Azure Cognitive Services で処理され、メタデータが抽出されて追加されます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="1eefa-146">一致する未添付の領収書を含む経費レポートを作成できるオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="1eefa-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="1eefa-147">経費報告書に追加されたオプションを使用すると、領収書から経費明細を作成したり、既存の領収書を既存の経費明細に一致させたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1eefa-148">よくあるご質問</span><span class="sxs-lookup"><span data-stu-id="1eefa-148">Frequently asked questions</span></span>

<span data-ttu-id="1eefa-149">**Microsoft はマイデータをモデルに使用していますか？**</span><span class="sxs-lookup"><span data-stu-id="1eefa-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="1eefa-150">いいえ、Microsoft は領収書処理サービスに使用する般的な機械学習モデルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="1eefa-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="1eefa-151">このモデルは、アップロードした領収書には基づいていません。</span><span class="sxs-lookup"><span data-stu-id="1eefa-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="1eefa-152">**この機能はどこで利用および処理できますか？**</span><span class="sxs-lookup"><span data-stu-id="1eefa-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="1eefa-153">現在、米国がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1eefa-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="1eefa-154">**領収書はどこに行きますか？**</span><span class="sxs-lookup"><span data-stu-id="1eefa-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="1eefa-155">Finance は Cognitive Services に連絡してフィール ドデータを抽出します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="1eefa-156">Cognitive Services は、処理が行われている間、領収書のコピーを最大24時間保持します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="1eefa-157">処理が完了すると、Cognitive Services は領収書を削除します。</span><span class="sxs-lookup"><span data-stu-id="1eefa-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="1eefa-158">領収書は引き続き Finance に保管されます。</span><span class="sxs-lookup"><span data-stu-id="1eefa-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="1eefa-159">詳細については、[Form Recognizer の新機能を使用して領収書を有効にする](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1eefa-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
