---
title: 請求書プロセスの概要
description: このトピックでは、リソース/非在庫ベースのシナリオのため、Project Operations における請求書のプロセス概要を説明します。
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 13f16d42ffdc0a9a6f369c311dfd9e15ad3f7aff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001522"
---
# <a name="invoicing-process-overview"></a><span data-ttu-id="59b86-103">請求書プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="59b86-103">Invoicing process overview</span></span>

<span data-ttu-id="59b86-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="59b86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="59b86-105">リソース/非在庫ベースのシナリオ向けの Project Operations は、プロジェクト マネージャーと売掛金担当者/プロジェクト経理担当の両方のニーズに合うように調整された包括的な機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="59b86-105">Project Operations for resource/non-stocked based scenarios offers comprehensive capabilities tailored to fit the needs of both Project manager and Accounts receivable clerk/project accountant.</span></span> <span data-ttu-id="59b86-106">請求プロセスでは、プロジェクト マネージャーがプロジェクトの請求バックログを管理し、売掛金担当者/プロジェクト経理担当が準拠した正確な顧客向けの請求書ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="59b86-106">For the invoicing process, the Project manager manages the project billing backlog and the Accounts receivable clerk/project accountant creates a compliant and accurate customer-facing invoice document.</span></span>

![請求書のフロー図](./media/invoicing-flow.png)

<span data-ttu-id="59b86-108">プロジェクト契約品目は、関連するプロジェクト トランザクションの請求方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="59b86-108">The project contract line defines the billing method for associated project transactions.</span></span> <span data-ttu-id="59b86-109">プロジェクト マネージャーが時間と費用のトランザクションを承認すると、システムはトランザクションを **プロジェクト実績** エンティティに記録し、情報をDynamics 365 Finance の **プロジェクト管理および会計** モジュールに送信します。</span><span class="sxs-lookup"><span data-stu-id="59b86-109">When the Project manager approves time and expense transactions, the system records the transactions in the **Project Actuals** entity and sends the information to the **Project management and accounting** module in Dynamics 365 Finance.</span></span> <span data-ttu-id="59b86-110">次に、プロジェクト経理担当は、[Project Operations 統合仕訳帳](../project-accounting/project-operations-integration-journal.md)を使用してレコードを確認および転記します。</span><span class="sxs-lookup"><span data-stu-id="59b86-110">The Project accountant then reviews and posts the records using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="59b86-111">この仕訳帳には、請求、消費税グループ、請求項目消費税グループ、財務ディメンションなど、プロジェクト実績の重要な会計詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59b86-111">This journal includes important accounting details for project actuals, such as billing, sales tax group, billing item sales tax group, and financial dimensions.</span></span>

<span data-ttu-id="59b86-112">プロジェクト マネージャーは、[時間と材料の請求バックログ](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)および固定価格請求[固定価格のマイルストーン](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)の時間と材料の請求方法を使用して、未請求の販売トランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="59b86-112">The Project manager can review unbilled sales transactions using the time and material billing method in the [Time and material billing backlog](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) and fixed price billing in [Fixed price milestones](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones).</span></span> <span data-ttu-id="59b86-113">これらのビューを使用すると、次の請求サイクルに含める必要があるトランザクションをフィルター処理して選択し、**請求準備完了** としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="59b86-113">These views allow you to filter and select transactions that need to be included in the next billing cycle and then mark them as **Ready to Invoice**.</span></span>

<span data-ttu-id="59b86-114">[見積送り状は手動で作成する](../proforma-invoicing/create-manual-proforma-invoice.md)か、[定期的なプロセス](../proforma-invoicing/configure-automated-invoice-creation.md)を使用できます。</span><span class="sxs-lookup"><span data-stu-id="59b86-114">You can [manually create a proforma invoice](../proforma-invoicing/create-manual-proforma-invoice.md) or use a [periodic process](../proforma-invoicing/configure-automated-invoice-creation.md).</span></span> <span data-ttu-id="59b86-115">プロジェクトマネージャーは必要に応じて[ドラフト見積送り状を調整](../proforma-invoicing/manage-proforma-invoice.md)して、確認することができます。</span><span class="sxs-lookup"><span data-stu-id="59b86-115">The Project manager can [adjust a draft proforma invoice](../proforma-invoicing/manage-proforma-invoice.md) as needed and then confirm it.</span></span>

<span data-ttu-id="59b86-116">確認済みの見積送り状は Finance の **プロジェクト管理および会計** モジュールに送信されます。</span><span class="sxs-lookup"><span data-stu-id="59b86-116">The confirmed proforma invoice is sent to the **Project management and accounting** module in Finance.</span></span> <span data-ttu-id="59b86-117">プロジェクト経理担当は、プロジェクト仮発行請求書をフォーマットして更新してから、ドキュメントを転記して印刷します。</span><span class="sxs-lookup"><span data-stu-id="59b86-117">The Project accountant formats and updates the project invoice proposal, and then posts and prints the document.</span></span> <span data-ttu-id="59b86-118">転記されたプロジェクト請求書は、総勘定元帳に加えて、顧客とプロジェクトの補助元帳に記録されます。</span><span class="sxs-lookup"><span data-stu-id="59b86-118">Posted project invoices are recorded in the General ledger, as well as the Customer and Project subledgers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]