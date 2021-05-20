---
title: 仕入先請求書統合
description: このトピックは、Project Operations におけるベンダー請求書の統合に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955782"
---
# <a name="vendor-invoice-integration"></a><span data-ttu-id="44762-103">仕入先請求書統合</span><span class="sxs-lookup"><span data-stu-id="44762-103">Vendor invoice integration</span></span>

<span data-ttu-id="44762-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="44762-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="44762-105">Dynamics 365 Project Operations でのプロジェクト関連の調達は、**買掛金勘定** > **請求書** > **保留中のベンダーの請求書** にアクセスして保留中のベンダー請求書を使って記録することができます。</span><span class="sxs-lookup"><span data-stu-id="44762-105">Project-related procurement in Dynamics 365 Project Operations can be recorded by going to **Accounts Payable** > **Invoices** > **Pending vendor invoices** and using a pending vendor invoice document.</span></span> <span data-ttu-id="44762-106">詳細については、[保留中のベンダーの請求書を使って非在庫の材料を購入する](../procurement/pending-vendor-invoices.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44762-106">For more information, see [Purchase non-stocked materials using a pending vendor invoice](../procurement/pending-vendor-invoices.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44762-107">このトピックで説明されている機能を使用する前に、必要となる構成を確認して適用してください。</span><span class="sxs-lookup"><span data-stu-id="44762-107">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="44762-108">詳細については、[在庫のない資材と保留中のベンダーの請求書を有効にします](../procurement/configure-materials-nonstocked.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44762-108">For more information, see [Enable non-stocked materials and pending vendor invoices](../procurement/configure-materials-nonstocked.md).</span></span>

<span data-ttu-id="44762-109">Project Operations では、プロジェクト関連のベンダーの請求書は、特別な転記ルールを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="44762-109">In Project Operations, project-related vendor invoices are posted using special posting rules:</span></span>

- <span data-ttu-id="44762-110">プロジェクト関連のコスト (回収不能な税金を含む) は、総勘定元帳のプロジェクトのコスト勘定にすぐには計上されません。</span><span class="sxs-lookup"><span data-stu-id="44762-110">Project-related cost (including non-recoverable tax) isn't immediately posted to the project cost account in the general ledger.</span></span> <span data-ttu-id="44762-111">代わりに、コストは **調達の統合アカウント** に転記されます。</span><span class="sxs-lookup"><span data-stu-id="44762-111">Instead, the cost is posted to the **Procurement integration account**.</span></span> <span data-ttu-id="44762-112">この勘定は、**プロジェクト管理と会計** > **設定** > **プロジェクト管理と会計パラメーター**、**Dynamics 365 Customer engagement の Project Operations** タブで構成されています。</span><span class="sxs-lookup"><span data-stu-id="44762-112">This account is configured in **Project management and accounting** > **Setup** > **Project management and accounting parameters** on the **Project Operations on Dynamics 365 Customer engagement** tab.</span></span>
- <span data-ttu-id="44762-113">二重書き込みは、以下のテーブル マッピングを使用して、ベンダーの請求書明細を Microsoft Dataverse に同期します。</span><span class="sxs-lookup"><span data-stu-id="44762-113">Dual-write synchronizes vendor invoice details to Microsoft Dataverse using the following table maps:</span></span>

     - <span data-ttu-id="44762-114">**Project Operations 統合プロジェクトベンダーの請求書エクスポート エンティティ (msdyn_projectvendorinvoices)**: このテーブル マッピングは、ベンダーの請求書ヘッダー情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="44762-114">**Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)**: This table map synchronizes vendor invoice header information.</span></span> <span data-ttu-id="44762-115">プロジェクト ID を含む行がひとつ以上あるベンダーの請求書だけが  Dataverse に同期されます。</span><span class="sxs-lookup"><span data-stu-id="44762-115">Only vendor invoices with at least one line that contains a project ID are synchronized to Dataverse.</span></span>
     - <span data-ttu-id="44762-116">**Project Operations 統合プロジェクト ベンダーの請求書エクスポート明細のエンティティ (msdyn_projectvendorinvoicelines)**: このテーブル マッピングは、ベンダーの請求書明細の情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="44762-116">**Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)**: This table map synchronizes vendor invoice line information.</span></span> <span data-ttu-id="44762-117">プロジェクト ID を含む行のみが Dataverse に同期されます。</span><span class="sxs-lookup"><span data-stu-id="44762-117">Only lines that contain a project ID are synchronized to Dataverse.</span></span>

     > [!NOTE]
     > <span data-ttu-id="44762-118">Dataverse 内のベンダーの請求書の詳細は編集できません。</span><span class="sxs-lookup"><span data-stu-id="44762-118">Vendor invoice details in Dataverse are not editable.</span></span>

<span data-ttu-id="44762-119">税補助元帳、仕入先補助元帳、その他の財務転記は、ベンダーの請求書が転記された時点で、該当するものが Dynamics 365 Finance に転記されます。</span><span class="sxs-lookup"><span data-stu-id="44762-119">Tax subledger, vendor subledger, and other financial postings are recorded as applicable in Dynamics 365 Finance when the vendor invoice is posted.</span></span>

![仕入先請求書統合](media/DW7VendorInvoice.png)

<span data-ttu-id="44762-121">Dataverse の **ベンダーの請求書** エンティティに記録が書き込まれると、記録の自動承認プロセスが始まります。</span><span class="sxs-lookup"><span data-stu-id="44762-121">When records are written to a **Vendor invoice** entity in Dataverse, an automated approval process of the records begins.</span></span> <span data-ttu-id="44762-122">必要に応じて、次にアクセスすることで、Dataverse の自動承認プロセスの状態を確認できます : **高度な設定** > **システム** > **システム ジョブ**。</span><span class="sxs-lookup"><span data-stu-id="44762-122">If needed, the automated approval process status can be reviewed in Dataverse by going to **Advanced settings** > **System** > **System jobs**.</span></span> <span data-ttu-id="44762-123">承認が完了すると、システムは **実績** エンティティに材料トランザクション クラスのレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="44762-123">After the approval is complete, the system creates material transaction class records in the **Actuals** entity.</span></span>

<span data-ttu-id="44762-124">材料関連の実績は、二重書き込みテーブル マッピングの  **Project Operations 統合実績 (msdyn_actuals)** を使って処理されます。</span><span class="sxs-lookup"><span data-stu-id="44762-124">Material-related actuals are then processed using the dual-write table map, **Project Operations integration actuals (msdyn_actuals)**.</span></span> <span data-ttu-id="44762-125">詳細については、[プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44762-125">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span>

<span data-ttu-id="44762-126">定期的なプロセスである **ステージング テーブルからのインポート** では、ベンダーの請求書に関連する Project Operations 統合仕訳を作成します。</span><span class="sxs-lookup"><span data-stu-id="44762-126">The periodic process, **Import from staging** creates vendor invoice-related Project Operations integration journal lines.</span></span> <span data-ttu-id="44762-127">オフセット勘定は、既定で調達統合アカウントになります。</span><span class="sxs-lookup"><span data-stu-id="44762-127">The offset account defaults to the procurement integration account.</span></span> <span data-ttu-id="44762-128">統合仕訳が転記されると、ベンダーの請求書取引の勘定残高がクリアされ、明細の額がプロジェクト費用勘定に移動します。</span><span class="sxs-lookup"><span data-stu-id="44762-128">When the integration journal is posted, the account balance is cleared for the vendor invoice transaction and the line amount is moved to the project cost account.</span></span> <span data-ttu-id="44762-129">また、ダウンストリームの請求書作成や収益認識のために、プロジェクト サブリーダーのトランザクションも作成されます。</span><span class="sxs-lookup"><span data-stu-id="44762-129">Project subledger transactions are also created for downstream invoicing and revenue recognition purposes.</span></span>
