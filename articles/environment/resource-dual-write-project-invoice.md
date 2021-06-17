---
title: プロジェクト請求書統合
description: このトピックでは、顧客の請求書作成で使用する Project Operations 二重書き込みの統合についての情報を提供します。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996572"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="56b97-103">プロジェクト請求書統合</span><span class="sxs-lookup"><span data-stu-id="56b97-103">Project invoice integration</span></span>

<span data-ttu-id="56b97-104">このトピックでは、顧客の請求書作成で使用する Project Operations 二重書き込みの統合についての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="56b97-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="56b97-105">Project Operations では、プロジェクト マネージャーがプロジェクトの請求書のバックログを管理し、Microsoft Dataverse の顧客への仮の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="56b97-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="56b97-106">仮の請求書に基づいて、売掛金担当者やプロジェクト会計士が顧客向けの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="56b97-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="56b97-107">二重書き込みの統合により、仮の請求書の詳細が Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="56b97-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="56b97-108">顧客向けの請求書が転記された後、システムは Dataverse の関連するプロジェクトの実績を会計の詳細に合わせて更新します。</span><span class="sxs-lookup"><span data-stu-id="56b97-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="56b97-109">次の図は、この統合の高レベルの概念的概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="56b97-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![プロジェクト請求書統合](./media/DW5Invoicing.png)

<span data-ttu-id="56b97-111">プロジェクト マネージャーが Dataverse で仮の請求書を確認した後、仮の請求書のヘッダー情報は、二重書き込みテーブル マッピング **ロジェクト請求書提案 V2 (invoices)** を使って Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="56b97-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="56b97-112">これは Dataverse アプリから Finance and Operations アプリへの一方通行の統合です。</span><span class="sxs-lookup"><span data-stu-id="56b97-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="56b97-113">Finance and Operations アプリで直接プロジェクトの請求書案を作成や削除はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="56b97-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="56b97-114">Dataverse での請求書の確認は、**実績** エンティティに請求書関連のレコードを作成するビジネス ロジックのトリガーにもなります。</span><span class="sxs-lookup"><span data-stu-id="56b97-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="56b97-115">これらのレコードは、二重書き込みテーブルマッピングの **Project Operations 統合実績 (msdyn\_actuals)** を使って Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="56b97-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="56b97-116">詳細については、[プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56b97-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="56b97-117">プロジェクトの請求書提案の明細は、定期的なプロセスである **ステージングからのインポート** によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="56b97-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="56b97-118">このプロセスは、**実績のステージング** テーブル の請求済みの売上実績の詳細に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="56b97-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="56b97-119">詳細については、[プロジェクトの請求書提案を管理する](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56b97-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 
