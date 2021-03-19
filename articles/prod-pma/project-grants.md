---
title: プロジェクト助成金
description: このトピックは、助成金を作成または変更する方法について説明します。
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289375"
---
# <a name="project-grants"></a><span data-ttu-id="b5a57-103">プロジェクト助成金</span><span class="sxs-lookup"><span data-stu-id="b5a57-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5a57-104">助成金は、特定の目的やプロジェクトに対するお金の授与です。</span><span class="sxs-lookup"><span data-stu-id="b5a57-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="b5a57-105">通常、助成金の使用方法には制限があります。</span><span class="sxs-lookup"><span data-stu-id="b5a57-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="b5a57-106">プロジェクト管理と会計では、助成金を入力して追跡し、それらのプロジェクトやプロジェクト契約とのリレーションシップを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="b5a57-107">例えば、次のタスクを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="b5a57-108">**プロジェクト** ページと **プロジェクト契約の詳細** ページへのリンクを通して助成金をプロジェクトや資金源に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="b5a57-109">助成金が 1 つのステータスから別のステータスに移動する際に、助成金への変更を入力および追跡します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="b5a57-110">コスト、要求金額、授与された金額を入力および追跡します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="b5a57-111">マスター助成金を作成し、サブグラントをそれらに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="b5a57-112">新しいレコードにすべての詳細を入力して許可を作成することも、既存の許可から詳細をコピーして更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="b5a57-113">新しい助成金の作成</span><span class="sxs-lookup"><span data-stu-id="b5a57-113">Create a new grant</span></span>

1. <span data-ttu-id="b5a57-114">**プロジェクト管理および会計** \> **助成金** \> **助成金** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="b5a57-115">**新着** \> **助成金** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="b5a57-116">助成金の詳細ページで、**一般** クイックタブで、**助成金 ID** フィールドに、助成金の英数字の識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="b5a57-117">**助成金名** フィールドに、助成金の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="b5a57-118">**説明** フィールドに、新しい助成金に関する詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="b5a57-119">ページ上の他のほとんどのフィールドはオプションであり、必要な情報を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="b5a57-120">次のリストは、付与の詳細ページの各クイックタブで指定されている情報について説明しています。</span><span class="sxs-lookup"><span data-stu-id="b5a57-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="b5a57-121">**一般** – 助成金の名前、ステータス、説明、目的、および金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="b5a57-122">**取引先担当者情報** – スタッフ、助成金を管理する部門、助成金の顧客または組織の助成金の出所に関する詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="b5a57-123">また、自分の組織が、助成金を受け取り、それを別の受領者に渡すパス スルー エンティティであるかどうかを示すこともできます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="b5a57-124">**追加** を選択して助成金を提供する組織の電話番号やメールアドレスなどの連絡先情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="b5a57-125">**日付と締め切り** – 助成金と助成金申請に関連する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="b5a57-126">例には、申請期日、提出日、助成金が承認または却下された日付などがあります。</span><span class="sxs-lookup"><span data-stu-id="b5a57-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="b5a57-127">**関連プロジェクトおよびプロジェクト契約** – **一般** クイックタブの **助成金ステータス** フィールドを **アクティブ** または **授与** に設定されているときのみこのクイックタブに情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="b5a57-128">次のオプションから選択して、関連するタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="b5a57-129">**資金源を追加する** – 助成金の新しい資金源を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="b5a57-130">ここですべての詳細を入力することも、規定の情報を使用して後で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="b5a57-131">**プロジェクト契約を追加する** – プロジェクト契約情報を追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="b5a57-132">**プロジェクトを追加** – プロジェクトの詳細を追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="b5a57-133">**セットアップ** – この情報が必要な場合は、マッチング ファンドに関する詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="b5a57-134">助成金を授与する多くの組織は、助成金で授与される金額と一致するように、受領者が自分のお金またはリソースの特定の金額を費やすことを要求します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="b5a57-135">**ローカルプロジェクトまたは追跡 ID** フィールドに、プロジェクト識別子とは異なる識別子を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b5a57-136">助成金の一部が別の組織に授与される場合は、**サブグランター** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="b5a57-137">米国で授与される助成金については、助成金が州の委任または連邦の委任のどちらで授与されるかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="b5a57-138">**ドローダウンの詳細** – 助成金の引き出し、請求、または使用の頻度に関する情報を追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="b5a57-139">コピーから新しい助成金を作成する</span><span class="sxs-lookup"><span data-stu-id="b5a57-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="b5a57-140">**プロジェクト管理および会計** \> **助成金** \> **助成金** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="b5a57-141">**新着** \> **助成金からコピー** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="b5a57-142">新しい助成金の英数字の識別子と名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="b5a57-143">助成金の詳細ページで、コピーした助成金の詳細を確認し、必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="b5a57-144">ページのほとんどのフィールドはオプションです。</span><span class="sxs-lookup"><span data-stu-id="b5a57-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="b5a57-145">助成金の詳細を表示または変更する</span><span class="sxs-lookup"><span data-stu-id="b5a57-145">View or modify grant details</span></span>

1. <span data-ttu-id="b5a57-146">**プロジェクト管理および会計** \> **助成金** \> **助成金** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="b5a57-147">変更する助成金を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="b5a57-148">アクション ペインで、**助成金** タブの **維持** グループで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5a57-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="b5a57-149">助成金の詳細を確認し、必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="b5a57-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]