---
title: 経費の領収書の処理
description: このトピックでは、領収書の光学式文字認識 (OCR) 処理に関する説明をします。 この機能は、Microsoft Dynamics 365 Finance で経費報告書を作成する際のユーザー エクスペリエンスの向上を意図して設計されています。
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271809"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="98a0b-104">経費の領収書の処理</span><span class="sxs-lookup"><span data-stu-id="98a0b-104">Expense receipt processing</span></span>

<span data-ttu-id="98a0b-105">領収書の光学式文字認識 (OCR) 処理が導入され、経費入力が強化されました。</span><span class="sxs-lookup"><span data-stu-id="98a0b-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="98a0b-106">この機能は、経費報告書を作成する際のユーザー エクスペリエンスの向上を意図して設計されています。</span><span class="sxs-lookup"><span data-stu-id="98a0b-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="98a0b-107">主な機能</span><span class="sxs-lookup"><span data-stu-id="98a0b-107">Key features</span></span>

- <span data-ttu-id="98a0b-108">システムは、領収書からマーチャント名、日付、および合計金額を抽出します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="98a0b-109">この機能では、未添付の領収書と未添付の経費取引を照合します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="98a0b-110">領収書から手動で入力した経費トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="98a0b-111">使用例</span><span class="sxs-lookup"><span data-stu-id="98a0b-111">Usage examples</span></span>

<span data-ttu-id="98a0b-112">経費報告書の作成時にクレジットカード取引を含む領収書を自動的に添付するには、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="98a0b-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="98a0b-113">**経費管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="98a0b-114">**領収書** タブで、添付されていないレシートが存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="98a0b-115">**領収書** タブで領収書をアップロードすることも可能です。</span><span class="sxs-lookup"><span data-stu-id="98a0b-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="98a0b-116">**経費** タブで、添付されていない経費が存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="98a0b-117">一般的には、経費管理者はこれら経費をクレジットカード プロバイダーからインポートします。</span><span class="sxs-lookup"><span data-stu-id="98a0b-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="98a0b-118">**新規経費報告書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-118">Select **New expense report**.</span></span> <span data-ttu-id="98a0b-119">経費報告書を作成する際に、経費と領収書を含めることができることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="98a0b-120">経費と領収書の両方を追加すると、経費に対する領収書の自動照合がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="98a0b-121">経費の作成や領収書から経費を照合するには、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="98a0b-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="98a0b-122">経費報告書の **領収書** タブで、**領収書を追加する** を選択して領収書を添付します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="98a0b-123">アップロードされた領収書の画像の下部に、**作成** と **照合** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="98a0b-124">**作成** を選択して手動で入力した経費取引を作成し、領収書から抽出した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="98a0b-125">**照合** を選択した場合、システムは既存の経費を領収書と照合します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="98a0b-126">インストール</span><span class="sxs-lookup"><span data-stu-id="98a0b-126">Installation</span></span>

<span data-ttu-id="98a0b-127">この機能は、**新しくなった経費報告書** と組み合わせて使用することで、経費のエクスペリエンスを簡素化することができます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="98a0b-128">この機能は、サンドボックス環境と運用環境である Tier 2 +環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="98a0b-129">このような高度な経費の機能を使用するには、Microsoft Dynamics 365 Finance 用の経費管理サービス アドインをインストールし、インスタンスの機能をオンにしてください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="98a0b-130">Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからアドインにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="98a0b-131">LCS にサインインし、対象とする環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="98a0b-132">**完全な詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="98a0b-133">**管理** を選択し、**環境アドイン** クイックタブまで下方向にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="98a0b-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="98a0b-134">**新しいアドインをインストールする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="98a0b-135">**経費管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="98a0b-136">インストール ガイドに従い、利用規約に同意してください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="98a0b-137">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-137">Select **Install**.</span></span>

<span data-ttu-id="98a0b-138">**機能管理** ワークスペースにて、次の機能をオンにします :</span><span class="sxs-lookup"><span data-stu-id="98a0b-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="98a0b-139">再構築された経費報告書</span><span class="sxs-lookup"><span data-stu-id="98a0b-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="98a0b-140">領収書から経費を自動照合して作成する</span><span class="sxs-lookup"><span data-stu-id="98a0b-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="98a0b-141">これらの機能をオンにすると、次のアクションが発生します :</span><span class="sxs-lookup"><span data-stu-id="98a0b-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="98a0b-142">既存の **経費管理** ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="98a0b-143">経費フィールドの表示に使用する新たなメニュー項目が追加されました。</span><span class="sxs-lookup"><span data-stu-id="98a0b-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="98a0b-144">以前の **経費報告書** ページには、**経費管理 > 自分の経費 > 経費報告書** に移動すると表示することができます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="98a0b-145">ワークフローや承認では、既存の経費報告書のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="98a0b-146">領収書は Microsoft Azure Cognitive Services で処理され、メタデータが抽出されて追加されます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="98a0b-147">一致する未添付の領収書を含む経費レポートを作成できるオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="98a0b-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="98a0b-148">経費報告書に追加されたオプションを使用すると、領収書から経費明細を作成したり、既存の領収書を既存の経費明細に一致させたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="98a0b-149">経費報告書の新機能の詳細については、[新しくなった経費報告書](ExpenseWorkspaceNew.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="98a0b-150">よくあるご質問</span><span class="sxs-lookup"><span data-stu-id="98a0b-150">Frequently asked questions</span></span>

<span data-ttu-id="98a0b-151">**Microsoft はマイデータをモデルに使用していますか？**</span><span class="sxs-lookup"><span data-stu-id="98a0b-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="98a0b-152">いいえ、Microsoft は領収書処理サービスに使用する般的な機械学習モデルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="98a0b-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="98a0b-153">このモデルは、アップロードした領収書には基づいていません。</span><span class="sxs-lookup"><span data-stu-id="98a0b-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="98a0b-154">**この機能はどこで利用および処理できますか？**</span><span class="sxs-lookup"><span data-stu-id="98a0b-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="98a0b-155">現在、米国がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="98a0b-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="98a0b-156">**領収書はどこに行きますか？**</span><span class="sxs-lookup"><span data-stu-id="98a0b-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="98a0b-157">Finance は Cognitive Services に連絡してフィール ドデータを抽出します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="98a0b-158">Cognitive Services は、処理が行われている間、領収書のコピーを最大24時間保持します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="98a0b-159">処理が完了すると、Cognitive Services は領収書を削除します。</span><span class="sxs-lookup"><span data-stu-id="98a0b-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="98a0b-160">領収書は引き続き Finance に保管されます。</span><span class="sxs-lookup"><span data-stu-id="98a0b-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="98a0b-161">詳細については、[Form Recognizer の新機能を使用して領収書を有効にする](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98a0b-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]