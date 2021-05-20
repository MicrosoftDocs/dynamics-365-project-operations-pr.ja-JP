---
title: Project Operations のセットアップと構成データの統合
description: このトピックでは、Project Operations 二重書き込みマッピングの設定および構成についての情報を提供します。
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939006"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a><span data-ttu-id="a6377-103">Project Operations のセットアップと構成データの統合</span><span class="sxs-lookup"><span data-stu-id="a6377-103">Project Operations setup and configuration data integration</span></span>

<span data-ttu-id="a6377-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a6377-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a6377-105">このトピックは、Project Operations の設定と構成エンティティの二重書き込み統合に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6377-105">This topic provides information about Project Operations dual-write integration for setup and configuration entities.</span></span>

## <a name="project-contracts-contract-lines-and-projects"></a><span data-ttu-id="a6377-106">プロジェクト契約、契約品目、プロジェクト</span><span class="sxs-lookup"><span data-stu-id="a6377-106">Project contracts, contract lines, and projects</span></span>

<span data-ttu-id="a6377-107">プロジェクト契約、契約品目、プロジェクトは、Dataverse で作成され、追加の会計のために Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="a6377-107">Project contracts, contract lines, and projects are created in Dataverse and synchronized to Finance and Operations apps for additional accounting.</span></span> <span data-ttu-id="a6377-108">これらのエンティティのレコードは、Dataverseでのみ作成、削除できます。</span><span class="sxs-lookup"><span data-stu-id="a6377-108">The records in these entities can be created and deleted only in Dataverse.</span></span> <span data-ttu-id="a6377-109">しかし、消費税のグループの既定値や財務分析コードなどの会計属性は、Finance and Operations アプリでこれらのレコードに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="a6377-109">However, accounting attributes such as sales tax group defaults and financial dimensions can be added to these records in the Finance and Operations apps.</span></span>

  ![プロジェクト契約統合の概念](./media/1ProjectContract.jpg)

<span data-ttu-id="a6377-111">営業活動のリード、営業案件、見積もりは Dataverse で追跡され、この活動に関連するダウンストリームの会計がないため Finance and Operations のアプリには同期されません。</span><span class="sxs-lookup"><span data-stu-id="a6377-111">Sales activity leads, opportunities, and quotes are tracked in Dataverse and don't synchronize to Finance and Operations apps because there is no downstream accounting associated with this activity.</span></span>

<span data-ttu-id="a6377-112">Dataverse のプロジェクト契約機能では、**プロジェクト契約ヘッダー (salesorders)** のテーブルマッピングを使って Finance and Operations アプリにプロジェクト契約のレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-112">The project contract functionality in Dataverse creates a project contract record in Finance and Operations apps using the **Project contract headers (salesorders)** table map.</span></span> <span data-ttu-id="a6377-113">Dataverse でプロジェクト契約を保存すると、プロジェクト契約の顧客エンティティ レコードの作成が開始されます。</span><span class="sxs-lookup"><span data-stu-id="a6377-113">Saving a project contract in Dataverse also starts the creation of a project contract customer entity record.</span></span> <span data-ttu-id="a6377-114">このレコードは、**プロジェクトの資金源 (msdyn\_projectcontractssplitbillingrules)** テーブル マッピングを使って Finance and Operations のアプリに同期しています。</span><span class="sxs-lookup"><span data-stu-id="a6377-114">This record is synchronized to Finance and Operations apps using the **Project funding source (msdyn\_projectcontractssplitbillingrules)** table map.</span></span> <span data-ttu-id="a6377-115">このマッピングは、プロジェクト契約の顧客の追加、更新、削除を同期します。</span><span class="sxs-lookup"><span data-stu-id="a6377-115">This map also synchronizes project contract customer additions, updates, and deletions.</span></span> <span data-ttu-id="a6377-116">プロジェクト契約の顧客間での分割請求のパーセンテージは、Dataverse でのみ管理され、Finance and Operations のアプリには同期されません。</span><span class="sxs-lookup"><span data-stu-id="a6377-116">Split billing percentages between project contract customers are mastered only in Dataverse and not synchronized to Finance and Operations apps.</span></span>

<span data-ttu-id="a6377-117">Dataverse でプロジェクト契約を作成した後、プロジェクト担当者は **プロジェクト管理と会計** > **プロジェクト契約** > **設定** > **既定の会計を表示** にアクセスして Finance and Operations アプリでこのプロジェクト契約の会計属性を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="a6377-117">After a project contract is created in Dataverse, the project accountant can update the accounting attributes for this project contract in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**.</span></span> <span data-ttu-id="a6377-118">経理担当者は、Finance and Operations アプリでプロジェクト契約 ID を選択し、Dataverse アプリで関連するプロジェクト契約レコードを開くことで、要められる納期や契約金額など、運用中のプロジェクト契約の属性を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="a6377-118">The accountant can review operational project contract attributes, such as requested delivery date and contract amount by selecting the project contract ID in Finance and Operations apps which opens the related project contract record in Dataverse.</span></span>

<span data-ttu-id="a6377-119">プロジェクト エンティティは、**Projects V2 (msdyn\_projects)** テーブル マッピングを使用して Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="a6377-119">The project entity is synchronized to Finance and Operations apps using the **Projects V2 (msdyn\_projects)** table map.</span></span> <span data-ttu-id="a6377-120">プロジェクト会計士は次のことができます:</span><span class="sxs-lookup"><span data-stu-id="a6377-120">The project accountant can:</span></span>

  - <span data-ttu-id="a6377-121">Finance and Operations アプリでプロジェクトを確認するには、**プロジェクト管理と会計** > **すべてのプロジェクト** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a6377-121">Review projects in Finance and Operations apps by going to **Project management and accounting** > **All projects**.</span></span> 
  - <span data-ttu-id="a6377-122">**プロジェクト管理と会計** > **すべてのプロジェクト** > **設定** > **既定の会計を表示する** にアクセスし、Finance and Operations アプリのプロジェクトの会計属性を更新します。</span><span class="sxs-lookup"><span data-stu-id="a6377-122">Update accounting attributes for the project in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Set up** > **Show default accounting**.</span></span>  
  - <span data-ttu-id="a6377-123">プロジェクトの開始予定日や終了予定日など、運用中のプロジェクトの属性を確認するには、Finance and Operations アプリでプロジェクト ID を選択し、Dataverse アプリで関連するプロジェクトのレコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6377-123">Review operational project attributes, such as estimated start and end dates, by selecting the project ID in Finance and Operations apps which opens the related project record in Dataverse.</span></span>

<span data-ttu-id="a6377-124">プロジェクトには、**プロジェクトの契約品目** エンティティを通じてプロジェクト契約が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a6377-124">A project is associated with a project contract through the **Project contract line** entity.</span></span>

<span data-ttu-id="a6377-125">Dataverse のプロジェクト契約品目は、**プロジェクト契約品目 (salesorderdetails)** のテーブル マッピングを使用して Finance and Operations アプリにプロジェクト契約の請求ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-125">Project contract lines in Dataverse creates a project contract billing rule in Finance and Operations apps using the **Project contract lines (salesorderdetails)** table map.</span></span> <span data-ttu-id="a6377-126">請求方法は、Finance and Operations アプリのプロジェクト契約の課金ルールタイプを定義します:</span><span class="sxs-lookup"><span data-stu-id="a6377-126">The billing method defines the project contract billing rule type in Finance and Operations apps:</span></span>

  - <span data-ttu-id="a6377-127">課金方法が時間と材料となっているプロジェクト契約品目は、時間と材料タイプの課金ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-127">Project contract lines with a billing method of time and material create a billing rule of time and material type.</span></span>
  - <span data-ttu-id="a6377-128">固定価格課金方式の契約品目では、マイルストーン課金のルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-128">Fixed price billing method contract lines create a milestone billing rule.</span></span>

<span data-ttu-id="a6377-129">プロジェクトの契約品目は、プロジェクトの会計担当者が Finance and Operations アプリで **プロジェクト管理と会計** > **プロジェクト契約** > **設定** > **既定の会計を表示する** にアクセスし、**契約品目** タブで詳細を確認することで確認できます。会計担当者は、このタブで固定価格請求方式の契約ラインに既定の財務分析コードを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a6377-129">Project contract lines can be reviewed by the project accountant in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**, and reviewing the details on the **Contract lines** tab. The accountant can also set default financial dimensions for the fixed price billing method contract lines on this tab.</span></span>

## <a name="billing-milestones"></a><span data-ttu-id="a6377-130">請求のマイルストーン</span><span class="sxs-lookup"><span data-stu-id="a6377-130">Billing milestones</span></span>

<span data-ttu-id="a6377-131">固定価格での請求方法を採用しているプロジェクト契約品目は、請求のマイルストーンを通じて請求されます。</span><span class="sxs-lookup"><span data-stu-id="a6377-131">Project contract lines using the fixed price billing method are invoiced through billing milestones.</span></span> <span data-ttu-id="a6377-132">請求のマイルストーンは、**Project Operations 統合の契約品目マイルストーン (msdyn\_contractlinescheduleofvalues)** テーブル マッピングを使用して、Finance and Operations アプリのプロジェクトの当座預金トランザクションに同期します。</span><span class="sxs-lookup"><span data-stu-id="a6377-132">Billing milestones are synchronized to project on-account transactions in Finance and Operations apps by using the **Project Operations integration contract line milestones (msdyn\_contractlinescheduleofvalues)** table map.</span></span>

  ![請求マイルストーンの統合](./media/2Milestones.jpg)

<span data-ttu-id="a6377-134">経理担当者は、当座預金取引を確認し、その取引の会計属性を調整するには、**プロジェクト管理と会計** > **プロジェクト契約** > **管理** > **当座預金取引** または **プロジェクト管理と会計** > **すべてのプロジェクト** > **管理** > **当座預金取引** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a6377-134">The accountant can review on-account transactions and adjust the accounting attributes for those transactions by going to **Project management and accounting** > **Project contracts** > **Maintain** > **On-account transactions** or **Project management and accounting** > **All projects** > **Maintain** > **On-account transactions**.</span></span>

<span data-ttu-id="a6377-135">特定のプロジェクト契約ラインの請求マイルストーンを最初に作成すると、システムはこの契約品目に関連付けられたプロジェクトの固定価格収益見積もりプロジェクトを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-135">When you first create a billing milestone for a given project contract line, the system automatically creates a fixed price revenue estimate project for the project associated with this contract line.</span></span> <span data-ttu-id="a6377-136">固定価格制の収益見積プロジェクトは、**プロジェクト管理と会計** > **固定価格の収益見積もりプロジェクト** にアクセスして確認することができます。</span><span class="sxs-lookup"><span data-stu-id="a6377-136">Fixed-price revenue estimate projects can be reviewed by going to **Project management and accounting** > **Fixed-price revenue estimate projects**.</span></span>

### <a name="project-tasks"></a><span data-ttu-id="a6377-137">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a6377-137">Project tasks</span></span>

<span data-ttu-id="a6377-138">プロジェクトのタスクは、参照用の **プロジェクト タスク (msdyn\_projecttasks)** テーブル マッピングを通じて、Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="a6377-138">Project tasks are synchronized to Finance and Operations apps through the **Project tasks (msdyn\_projecttasks)** table map for reference purposes only.</span></span> <span data-ttu-id="a6377-139">Finance and Operations アプリでは、作成、更新、削除の操作には対応していません。</span><span class="sxs-lookup"><span data-stu-id="a6377-139">Creating, updating, and deleting operations isn't supported through Finance and Operations apps.</span></span>

  ![プリジェクト タスクの統合](./media/3Tasks.jpg)

## <a name="project-resources"></a><span data-ttu-id="a6377-141">プロジェクト リソース</span><span class="sxs-lookup"><span data-stu-id="a6377-141">Project resources</span></span>

<span data-ttu-id="a6377-142">**プロジェクト リソースの役割** のエンティティは、参照用にFinance and Operations のテーブルマッピングを使って **すべての会社のプロジェクトリソースの役割 (bookableresourcecategories)** のアプリと同期しています。</span><span class="sxs-lookup"><span data-stu-id="a6377-142">The **Project resource roles** entity is synchronized to Finance and Operations apps using the **Project resource roles for all companies (bookableresourcecategories)** table map for reference purposes only.</span></span> <span data-ttu-id="a6377-143">Dataverse のリソースの役割は会社固有のものではないため、システムは、二重書きの統合範囲に含まれるすべての法人について、Finance and Operations アプリにそれぞれの会社固有のリソースの役割のレコードを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-143">Because resource roles in Dataverse are not company-specific, the system automatically creates respective company-specific resource roles records in Finance and Operations apps automatically for all legal entities included into dual-write integration scope.</span></span>

![リソース ロールの統合](./media/5Resources.jpg)

<span data-ttu-id="a6377-145">Project Operations のプロジェクト リソースは Dataverse で管理されており、Finance and Operations のアプリには同期されていません。</span><span class="sxs-lookup"><span data-stu-id="a6377-145">Project resources in Project Operations are maintained in Dataverse and aren't synchronized to Finance and Operations apps.</span></span>

### <a name="transaction-categories"></a><span data-ttu-id="a6377-146">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="a6377-146">Transaction categories</span></span>

<span data-ttu-id="a6377-147">トランザクションのカテゴリーは Dataverse に保持され、**プロジェクト トランザクション カテゴリ (msdyn\_transactioncategories)** のテーブル マッピングを使って Finance and Operations のアプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="a6377-147">Transaction categories are maintained in Dataverse and synchronized to Finance and Operations apps using the **Project transaction categories (msdyn\_transactioncategories)** table map.</span></span> <span data-ttu-id="a6377-148">トランザクションのカテゴリー レコードが同期されると、システムは自動的に 4 つの共有カテゴリー レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6377-148">After the transaction category record is synchronized, the system automatically creates four shared category records.</span></span> <span data-ttu-id="a6377-149">各レコードは Finance and Operations アプリのトランザクション タイプに対応しており、トランザクション カテゴリのレコードにリンクしています。</span><span class="sxs-lookup"><span data-stu-id="a6377-149">Each record corresponds to a transaction type in Finance and Operations apps and links them to the transaction category record.</span></span>

![トランザクション カテゴリの統合](./media/4TransactionCategories.jpg)

<span data-ttu-id="a6377-151">見積もりと実績にトランザクション カテゴリーを使用する場合は、プロジェクトの会計士またはシステム管理者は、すべての法人に対応するプロジェクト カテゴリーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6377-151">Using transaction categories for estimates and actuals requires the project accountant or system administrator to create corresponding project categories in every legal entity.</span></span> <span data-ttu-id="a6377-152">詳細については、[プロジェクト　カテゴリの構成](../project-accounting/configure-project-categories.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6377-152">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md).</span></span>
