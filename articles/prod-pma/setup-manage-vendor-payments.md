---
title: Pay-when-Paid (受給時支払) ベンダー支払いの設定と使用
description: このトピックは、顧客の支払いに基づいて部分的にベンダーへの支払いをおこなえるように、受給時支払 (PWP) 条件を作成する方法について説明します。
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079247"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="05842-103">Pay-when-Paid (受給時支払) ベンダー支払いの設定と使用</span><span class="sxs-lookup"><span data-stu-id="05842-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05842-104">ベンダーを下請け業者として仕事をすることを承認するとき、顧客がプロジェクトの代金を支払うまで、ベンダーへの支払いを保留したい場合があります。</span><span class="sxs-lookup"><span data-stu-id="05842-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="05842-105">このシナリオをサポートするために、ベンダーとの発注書 (PO) を設定するときに、受給時支払 (PWP) 条件を設定できます。</span><span class="sxs-lookup"><span data-stu-id="05842-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="05842-106">たとえば、顧客がプロジェクトの請求書に金額を支払う場合、ベンダーの請求書の金額の一部またはすべてをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="05842-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="05842-107">顧客から関連する支払いのある割合を受け取った後にベンダーに支払いが行われることを指定する PWP 条件を設定するだけです。</span><span class="sxs-lookup"><span data-stu-id="05842-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="05842-108">顧客から部分的に支払いを受け取った場合は、関連するベンダーの請求書の一部を手動でリリースして支払いを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="05842-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="05842-109">次の例は、PWP 条件が使用される場合のプロセスの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="05842-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="05842-110">例</span><span class="sxs-lookup"><span data-stu-id="05842-110">Example</span></span>

<span data-ttu-id="05842-111">あなたの組織は、ソフトウェアがインストールされている 100 台のコンピューターを、1 台のコンピューターあたり 150.00 米ドル (USD) の価格で顧客に提供することに同意しています。</span><span class="sxs-lookup"><span data-stu-id="05842-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="05842-112">次に、ソフトウェアがインストールされているコンピューターを提供ベンダーを雇います。</span><span class="sxs-lookup"><span data-stu-id="05842-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="05842-113">契約によると、顧客はあなたの組織に支払いをおこなう前にコンピューターの品質を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05842-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="05842-114">組織の方針では、顧客が組織に支払いをおこなうまでベンダーへの支払いを保留します。</span><span class="sxs-lookup"><span data-stu-id="05842-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="05842-115">したがって、PWP の割合が 100％ になるようにプロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="05842-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="05842-116">ベンダーは、ソフトウェアがインストールされている 100 台のコンピューターを、10,000.00 米国ドルの請求書とともに納品します。</span><span class="sxs-lookup"><span data-stu-id="05842-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="05842-117">このプロジェクトには PWP 条件が設定されているため、コンピューター受領時にベンダーに対して支払いをおこなう必要はありません。</span><span class="sxs-lookup"><span data-stu-id="05842-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="05842-118">代わりに、15,000.00 米国ドルの請求書を付けてコンピューターを顧客に発送します。</span><span class="sxs-lookup"><span data-stu-id="05842-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="05842-119">顧客はコンピューターを検査し、プロジェクトの請求書の全額を承認します。</span><span class="sxs-lookup"><span data-stu-id="05842-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="05842-120">顧客から全額の支払いを受け取った後、ベンダーの請求書の全額である 10,000.00 米国ドルをベンダーに支払います。</span><span class="sxs-lookup"><span data-stu-id="05842-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="05842-121">プロジェクトの PWP 条件を設定する</span><span class="sxs-lookup"><span data-stu-id="05842-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="05842-122">プロジェクトの PWP 条件を設定するときは、ベンダーに支払う前に、顧客がプロジェクトに対して支払う必要のある最小金額の率を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05842-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="05842-123">しきい値は、プロジェクトの顧客の請求書で自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="05842-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="05842-124">次の手順に従って、PWP 条件に対するしきい値のパーセンテージを設定します。</span><span class="sxs-lookup"><span data-stu-id="05842-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="05842-125">**プロジェクト管理と会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="05842-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="05842-126">PWP 条件を設定するプロジェクトを見つけて開きます。</span><span class="sxs-lookup"><span data-stu-id="05842-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="05842-127">**ベンダー契約** クイック タブで、 **明細行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="05842-128">**勘定コード** フィールドで、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="05842-129">**テーブル** – PWP 条件は、単一のベンダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="05842-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="05842-130">**グループ** – PWP 条件は、ベンダー グループ内のすべてのベンダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="05842-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="05842-131">**すべて** – PWP の条件は、すべてのベンダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="05842-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="05842-132">前のステップで **テーブル** または **グループ** を選択した場合、 **ベンダー/ベンダー グループ** フィールドで、PWP 条件が適用されるベンダーまたはベンダーグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="05842-133">前のステップで **すべて** を選択した場合は、 **ベンダー/ベンダーグループ** フィールドは編集できません。</span><span class="sxs-lookup"><span data-stu-id="05842-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="05842-134">プロジェクト内のベンダーに対してベンダー リテンション期間の条件が設定されている場合は、 **ベンダーリテンション期間条件** フィールドで、リテンション機関条件のルール ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="05842-135">**PWP しきい値のパーセンテージ** フィールドに、プロジェクトのしきい値のパーセンテージを入力します。</span><span class="sxs-lookup"><span data-stu-id="05842-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="05842-136">プロジェクトに入力するパーセンテージは、ベンダーに支払う前に顧客が支払う必要のある最小金額を定義します。</span><span class="sxs-lookup"><span data-stu-id="05842-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="05842-137">PWP 条件を持つ PO を作成する</span><span class="sxs-lookup"><span data-stu-id="05842-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="05842-138">仕入先からの請求書を転記するときに、仕入先が PWP 条件の対象である場合、それらの条件は PO の明細行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="05842-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="05842-139">PWP 条件を持つ PO を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="05842-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="05842-140">**調達と調達先** \> **発注書** \> **すべての発注書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="05842-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="05842-141">アクション ペインで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="05842-142">その後、 **発注書の作成** ダイアログ ボックスで、必要情報を入力して **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="05842-143">または、 **すべての注文書** リストページで既存の PO を開きます。</span><span class="sxs-lookup"><span data-stu-id="05842-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="05842-144">**発注書** ページの、 **発注書明細行** クイックタブで、ベンダーの PO 明細行の詳細をレビューします。</span><span class="sxs-lookup"><span data-stu-id="05842-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="05842-145">**受給時支払** オプションが自動的に選択され、 **PWP しきい値のパーセンテージ** フィールドは **プロジェクト** ページの **PWP しきい値のパーセンテージ** 上のフィールドから自動的にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="05842-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="05842-146">PO 明細行の仕入先に PWP 条件を適用したくない場合は、 **受給時支払い** オプションをクリアします。</span><span class="sxs-lookup"><span data-stu-id="05842-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="05842-147">この場合、PO 明細行の **PWP しきい値のパーセンテージ** フィールドは 0 (ゼロ) にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="05842-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="05842-148">顧客の支払いを更新し、ベンダーに支払う</span><span class="sxs-lookup"><span data-stu-id="05842-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="05842-149">ベンダーがプロジェクトでの作業を完了して請求書を送信したら、プロジェクトのステータスと顧客の請求書を確認して、プロジェクトの PWP 条件が満たされているかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05842-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="05842-150">ベンダーの PWP 条件が満たされている場合は、プロジェクトの顧客の支払いに基づいて、ベンダーの請求書のどの明細行を支払うかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="05842-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="05842-151">PWP 条件が満たされていない場合でもベンダーに支払うことにした場合は、 **受給時支払いのベンダーの請求書** ページで PWP 条件を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="05842-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="05842-152">**プロジェクト管理と会計** \> **照会とレポート** \> **リテンションに関する照会** \> **受給時支払いのベンダーの請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="05842-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="05842-153">**受給時支払いのベンダーの請求書** ページの検索フィールドで、値を入力してレビューするベンダーの請求書を検索して、 **検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="05842-154">**ベンダー請求書の明細行** クイックタブで、変更する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="05842-155">**受給時支払い** 条件が請求書明細行を満たす場合は、 **ベンダーの支払いをリリースする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05842-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="05842-156">**受給時支払い** オプションがクリアされ、 **支払い準備完了** フィールドの値が **はい** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="05842-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>
