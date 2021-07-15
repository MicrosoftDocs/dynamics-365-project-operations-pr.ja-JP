---
title: 会社間請求の概要
description: このトピックでは、プロジェクトの会社間請求に関する情報と例を提供します。
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369382"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="0db1e-103">会社間請求の概要</span><span class="sxs-lookup"><span data-stu-id="0db1e-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="0db1e-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0db1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0db1e-105">組織には、プロジェクトのために製品とサービスを相互に転送する複数の部署、子会社、およびその他の法人が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0db1e-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="0db1e-106">サービスや製品を提供する法人は *貸付法人* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0db1e-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="0db1e-107">サービスや製品を受領する法人は *借入法人* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0db1e-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="0db1e-108">次の図は、Contoso Robotics USA (借入法人) と Contoso Robotics UK (貸付法人) の 2 つの法人がリソースを共有し、Adventure Works という顧客のためにプロジェクトを遂行するという典型的なシナリオを示しています。</span><span class="sxs-lookup"><span data-stu-id="0db1e-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="0db1e-109">このシナリオでは、Contoso Robotics USAは、Adventure Works に作業を提供する契約を結んでいます。</span><span class="sxs-lookup"><span data-stu-id="0db1e-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![会社間請求](./media/IntercompanyScenario.png) 

<span data-ttu-id="0db1e-111">Dynamics 365 Project Operations は会社間取引の処理に次のフローを使用します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="0db1e-112">貸付法人のリソースは、借入法人のプロジェクトに対して時間と費用を予約して、会社間の時間や経費のトランザクションを記録します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="0db1e-113">時間と経費のコストは、借入法人の単位原価の価格表を使用して貸付法人に記録します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="0db1e-114">会社間の未請求販売トランザクションは、借入法人の単位原価の価格表を使用して貸付法人に記録します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="0db1e-115">未請求売上は、プロジェクト契約の販売価格表を使用して借入法人に記録します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="0db1e-116">未請求売上の記録時に顧客に請求できます。</span><span class="sxs-lookup"><span data-stu-id="0db1e-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="0db1e-117">顧客は会社間請求処理の完了を待つ必要がありません。</span><span class="sxs-lookup"><span data-stu-id="0db1e-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="0db1e-118">会社間顧客請求書は貸付法人で定期的に作成します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="0db1e-119">この請求書は、手動または定期的な自動プロセスを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="0db1e-120">借入法人ごとに 1 つの請求書を作成することも、プロジェクトごとに個別の請求書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0db1e-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="0db1e-121">会社間顧客請求書を貸付法人に転記すると、対応する保留中のベンダー請求書が借入法人に作成されます。</span><span class="sxs-lookup"><span data-stu-id="0db1e-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="0db1e-122">ベンダー請求書の保留中コストは、請求書の転記時にプロジェクトの補助元帳に記録します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="0db1e-123">次の図は、会計イベントと一般会計への予測転記に関連する会社間請求を示します。</span><span class="sxs-lookup"><span data-stu-id="0db1e-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![会社間のフロー](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="0db1e-125">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0db1e-125">Additional resources</span></span>

- [<span data-ttu-id="0db1e-126">会社間請求の構成</span><span class="sxs-lookup"><span data-stu-id="0db1e-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="0db1e-127">会社間トランザクションの記録</span><span class="sxs-lookup"><span data-stu-id="0db1e-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="0db1e-128">会社間で顧客およびベンダーの請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="0db1e-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]