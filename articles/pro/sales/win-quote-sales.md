---
title: 見積もりのクローズ
description: このトピックは、Project Operations で見積もりのクローズに関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896197"
---
# <a name="close-quotes"></a><span data-ttu-id="0812c-103">見積もりのクローズ</span><span class="sxs-lookup"><span data-stu-id="0812c-103">Close quotes</span></span> 

<span data-ttu-id="0812c-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="0812c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0812c-105">プロジェクトの見積もりは、受注または失注としてクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="0812c-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="0812c-106">見積もりのアクティブ化および変更の操作は、Microsoft Dynamics 365 Project Operations ではサポートされていないため、ドラフトの見積もりをクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="0812c-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="0812c-107">受注として見積もりをクローズする</span><span class="sxs-lookup"><span data-stu-id="0812c-107">Close a quote as Won</span></span>

<span data-ttu-id="0812c-108">受注としてプロジェクト見積もりをクローズすると、見積もりのステータスはクローズ済みとなり、ステータスの理由は受注と設定されます。</span><span class="sxs-lookup"><span data-stu-id="0812c-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="0812c-109">見積もりをクローズすると、読み取り専用になり、見積もり情報を含むドラフトのプロジェクト契約が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0812c-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="0812c-110">クローズ済みの見積もりは再び開くことができないため、確認ダイアログで確認します。クローズ済みの見積もりは再度開くことができず、変更を元に戻すことができないため、変更が行われる前に確認ダイアログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0812c-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="0812c-111">見積もりが営業案件に添付されている場合、その営業案件の他のプロジェクト見積もりは、すべて失注として自動的にクローズします。</span><span class="sxs-lookup"><span data-stu-id="0812c-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="0812c-112">受注として見積もりをクローズすることの財務上の影響</span><span class="sxs-lookup"><span data-stu-id="0812c-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="0812c-113">あるプロジェクトにおける工数の実績が記録されていて、ドラフト見積もりに添付されたままの場合、工数または費用のコストのみが記録されます。</span><span class="sxs-lookup"><span data-stu-id="0812c-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="0812c-114">見積もりが受注としてクローズされた後、アプリケーションは、古いコスト実績を元に戻し、新しいコスト実績を再作成することにより、コストをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="0812c-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="0812c-115">アプリケーションは、関連するプロジェクト契約品目の請求方法に基づいて、これらのコスト実績を処理します。</span><span class="sxs-lookup"><span data-stu-id="0812c-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="0812c-116">コスト実績が工数と材料の契約品目を参照している場合、見積もりがクローズされてプロジェクト契約が作成されたときに、対応する未請求の販売実績が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="0812c-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="0812c-117">コスト実績が固定価格契約品目を参照している場合、アプリケーションは、プロジェクト契約の顧客の分割請求ルールに基づいてコスト実績の再処理を停止します。</span><span class="sxs-lookup"><span data-stu-id="0812c-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="0812c-118">失注として見積もりをクローズする:</span><span class="sxs-lookup"><span data-stu-id="0812c-118">Closing a quote as lost:</span></span>

<span data-ttu-id="0812c-119">失注としてプロジェクト見積もりをクローズすると、見積もりのステータスはクローズ済みとなり、ステータスの理由は失注と設定されます。</span><span class="sxs-lookup"><span data-stu-id="0812c-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="0812c-120">見積もりを閉じると、プロジェクトの見積もりは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="0812c-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="0812c-121">クローズ済みの見積もりは再度オープンできないため、見積もりをクローズする前に、確認ダイアログで変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="0812c-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="0812c-122">失注としてクローズされたプロジェクト見積もりのいずれかの品目にプロジェクトが参照されている場合、そのプロジェクトもクローズ済みとしてマークされ、その日以降のリソース予約はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="0812c-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="0812c-123">Project Operations では、見積もりを受注または失注としてクローズしても、営業案件のステータスには影響しません。案件は、手動でクローズするまでオープンしたままになります。</span><span class="sxs-lookup"><span data-stu-id="0812c-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
