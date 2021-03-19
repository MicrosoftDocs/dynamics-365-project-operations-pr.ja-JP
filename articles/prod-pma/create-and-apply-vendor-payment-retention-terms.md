---
title: ベンダーの支払いリテンション期間の作成と適用
description: このトピックでは、ベンダーの支払いに向けたリテンション期間を設定し、維持する方法について解説します。
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270954"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="a19e2-103">ベンダーの支払いリテンション期間の作成と適用</span><span class="sxs-lookup"><span data-stu-id="a19e2-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="a19e2-104">ベンダーへの支払いの一部を保持したい場合には、プロジェクトにベンダーの支払いリテンション期間を設定しておくと便利です。</span><span class="sxs-lookup"><span data-stu-id="a19e2-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="a19e2-105">たとえば、納品された製品が期待通りになるまでベンダーへの支払いを保留したい場合などです。</span><span class="sxs-lookup"><span data-stu-id="a19e2-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="a19e2-106">ベンダー契約の交渉時に、ベンダー支払いリテンション期間を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="a19e2-107">ベンダーの支払いリテンション期間の作成</span><span class="sxs-lookup"><span data-stu-id="a19e2-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="a19e2-108">ベンダーの滞納金の割合と、以前に滞納していた金額の割合を入力して解除することができます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="a19e2-109">契約が指定された完了状態に達するまで、金額はベンダーの請求書に自動的に保持されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="a19e2-110">保持条件を設定したら、そのベンダーの任意のプロジェクトに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="a19e2-111">以下の手順を使用して、ベンダーの支払いに使用するリテンション期間を設定し、維持します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="a19e2-112">**プロジェクト管理と会計** > **保持** > **ベンダーの支払いリテンション期間** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="a19e2-113">**新規** を選択して新しいベンダーのリテンション期間を追加します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="a19e2-114">新しい機関に向けた **ルール ID** の値が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="a19e2-115">**説明** フィールドに簡単な説明を入力し、クイックタブの **期間** で **行の追加** を選択して、以下の条件の値を入力します :</span><span class="sxs-lookup"><span data-stu-id="a19e2-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="a19e2-116">**納品されたユニットの割合** : 期間の完了率を入力します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="a19e2-117">金額は、プロジェクトの完了段階が指定された割合になるまで、ベンダーの請求書に自動的に保持されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="a19e2-118">たとえば、50.00と入力すると、プロジェクトが50％完了するまで金額が保持されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="a19e2-119">**保持する割合**：ベンダーの請求金額のうち、保持する割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="a19e2-120">たとえば、10.00 と入力した場合、ベンダーの請求書に記載されている金額の 10% は、**納品されたユニットの割合** フィールドで設定されている完了率に達するまで保持されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="a19e2-121">**リリースするパーセンテージ** :  **追加行** を選択して、選択したレベルのプロジェクト完了のためにリリースされる、以前に保持された金額のパーセンテージを入力します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="a19e2-122">プロジェクトの完了レベルが異なる複数のマイルストーンがある場合は、それぞれのリテンション期間ごとにベンダーの保持する期間の行を個別に入力します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="a19e2-123">各行は、指定されたプロジェクト完了レベルごとに、異なるリテンション率と異なるリリース率を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="a19e2-124">ベンダーのリテンション条件を作成した後、プロジェクトに条件を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="a19e2-125">ベンダーのリテンション期間をプロジェクトに適用する</span><span class="sxs-lookup"><span data-stu-id="a19e2-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="a19e2-126">**プロジェクト管理と会計** > **プロジェクト** > **すべてのプロジェクト** に移動して、プロジェクトのリストページからプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="a19e2-127">**ベンダー契約** クイック タブで、**明細行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="a19e2-128">**取引先企業コード** フィールドで、次のいずれかのオプションを選択します :</span><span class="sxs-lookup"><span data-stu-id="a19e2-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="a19e2-129">**テーブル** : ベンダーのリテンション期間は、1つのベンダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="a19e2-130">**グループ** : ベンダーのリテンション期間は、ベンダー グループ内のすべてのベンダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="a19e2-131">**すべて** : ベンダーのリテンション期間は、すべてのベンダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="a19e2-132">**仕入先/仕入先グループ項目** で、ベンダーのリテンション期間が適用されるベンダーまたはベンダー グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="a19e2-133">前述の手順で **すべて** を選択した場合は、このフィールドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="a19e2-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="a19e2-134">**ベンダーのリテンション期間** フィールドで、前の手順で作成したリテンション期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="a19e2-135">プロジェクトにベンダーに PWP (Pay-when-paid) 条件が設定されている場合は、**PWP の閾値パーセンテージ** フィールドにプロジェクトの閾値パーセンテージを入力します。</span><span class="sxs-lookup"><span data-stu-id="a19e2-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="a19e2-136">ベンダーのリテンション期間は、ベンダー受けに作成した発注書にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="a19e2-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]