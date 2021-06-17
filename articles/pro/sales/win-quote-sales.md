---
title: 見積もりのクローズ - Lite
description: このトピックは、Project Operations で見積もりのクローズに関する情報を提供します。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994142"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="63fe1-103">見積もりのクローズ - Lite</span><span class="sxs-lookup"><span data-stu-id="63fe1-103">Close a quote - lite</span></span>

<span data-ttu-id="63fe1-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="63fe1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63fe1-105">プロジェクトの見積もりは、受注または失注としてクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="63fe1-106">Microsoft Dynamics 365 Project Operations では、見積もりのアクティブ化および改訂操作がサポートされていないため、見積もりの下書きをクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="63fe1-107">受注として見積もりをクローズする</span><span class="sxs-lookup"><span data-stu-id="63fe1-107">Close a quote as Won</span></span>

<span data-ttu-id="63fe1-108">プロジェクト見積もりを [受注] として閉じると、ステータスが [クローズ済み] に設定され、ステータス理由も [受注] になります。</span><span class="sxs-lookup"><span data-stu-id="63fe1-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="63fe1-109">見積もりをクローズすると、読み取り専用になり、見積もり情報を含むドラフトのプロジェクト契約が作成されます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="63fe1-110">クローズされた見積もりは再度開くことができないため、確認ダイアログにより変更が確認されます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="63fe1-111">見積もりが営業案件に添付されている場合、その営業案件の他のプロジェクト見積もりは、すべて失注として自動的にクローズします。</span><span class="sxs-lookup"><span data-stu-id="63fe1-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="63fe1-112">受注として見積もりをクローズすることの財務上の影響</span><span class="sxs-lookup"><span data-stu-id="63fe1-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="63fe1-113">下書きの見積もりに添付されたままのプロジェクトの時間の実績がある場合、時間または経費のコストのみが記録されます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="63fe1-114">見積もりが受注としてクローズされた後、アプリケーションは、古いコスト実績を元に戻し、新しいコスト実績を再作成することにより、コストをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="63fe1-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="63fe1-115">アプリケーションは、関連するプロジェクト契約品目の請求方法に基づいて、これらのコスト実績を処理します。</span><span class="sxs-lookup"><span data-stu-id="63fe1-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="63fe1-116">原価実績が時間と材料の契約品目を参照している場合、見積もりがクローズされてプロジェクト契約が作成されると、対応する未請求の販売実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="63fe1-117">原価実績が固定価格契約品目を参照している場合、アプリケーションは、プロジェクト契約顧客の分割請求ルールに基づく原価実績の再処理を停止します。</span><span class="sxs-lookup"><span data-stu-id="63fe1-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="63fe1-118">失注として見積もりをクローズする:</span><span class="sxs-lookup"><span data-stu-id="63fe1-118">Closing a quote as lost:</span></span>

<span data-ttu-id="63fe1-119">プロジェクト見積もりを [失注] として閉じると、ステータスが [クローズ済み] に設定され、ステータス理由も [失注] になります。</span><span class="sxs-lookup"><span data-stu-id="63fe1-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="63fe1-120">見積もりを閉じると、プロジェクトの見積もりは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="63fe1-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="63fe1-121">クローズ済みの見積もりは再度オープンできないため、見積もりをクローズする前に、確認ダイアログで変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="63fe1-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="63fe1-122">[失注] としてクローズされたプロジェクト見積もりがその行のいずれかでプロジェクトを参照している場合、そのプロジェクトも [クローズ済み] とマークされます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="63fe1-123">この日付以降のリソース予約はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="63fe1-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="63fe1-124">Project Operations では、見積もりを受注または失注としてクローズしても、営業案件のステータスには影響しません。案件は、手動でクローズするまでオープンしたままになります。</span><span class="sxs-lookup"><span data-stu-id="63fe1-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]