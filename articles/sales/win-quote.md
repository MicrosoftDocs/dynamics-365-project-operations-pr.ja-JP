---
title: 見積もりをクローズする
description: このトピックは、Project Operations で見積もりのクローズに関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124689"
---
# <a name="close-a-quote"></a><span data-ttu-id="c8d1b-103">見積もりをクローズする</span><span class="sxs-lookup"><span data-stu-id="c8d1b-103">Close a quote</span></span>

<span data-ttu-id="c8d1b-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c8d1b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c8d1b-105">プロジェクトの見積もりは、受注または失注としてクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="c8d1b-106">アクティブ化および変更の機能は、Microsoft Dynamics 365 Project Operations の見積もりではサポートされていないため、ドラフトの見積もりをクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="c8d1b-107">受注として見積もりをクローズする</span><span class="sxs-lookup"><span data-stu-id="c8d1b-107">Close a quote as Won</span></span>

<span data-ttu-id="c8d1b-108">受注としてプロジェクト見積もりをクローズすると、見積もりのステータスは **クローズ済み** となり、ステータスの理由は **受注** と設定されます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="c8d1b-109">見積もりをクローズすると、読み取り専用になり、すべての見積もり情報を含むドラフトのプロジェクト契約が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="c8d1b-110">クローズ済みの見積もりは再度オープンできないため、見積もりをクローズする前に、確認ダイアログで変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c8d1b-111">プロジェクト見積もりから作成されたプロジェクト契約は、Project Operations のプロジェクト管理および会計モジュールでも利用できます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="c8d1b-112">プロジェクト契約がどの品目のプロジェクトにもマッピングされていない場合、このプロジェクト契約は非アクティブなプロジェクト契約として使用可能になり、プロジェクトが少なくとも 1 つの契約品目にマッピングされるとすぐにアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="c8d1b-113">見積もりが営業案件に添付されている場合、その営業案件の他のプロジェクト見積もりは、すべて失注として自動的にクローズします。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="c8d1b-114">受注として見積もりをクローズすることの財務上の影響</span><span class="sxs-lookup"><span data-stu-id="c8d1b-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="c8d1b-115">あるプロジェクトにおける工数の実績が記録されていて、ドラフト見積もりに添付されたままの場合、工数または費用のコストのみが記録されます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="c8d1b-116">見積もりが受注としてクローズされた後、アプリケーションは、古いコスト実績を元に戻し、新しいコスト実績を再作成することにより、コストをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="c8d1b-117">アプリケーションは、関連するプロジェクト契約品目の請求方法に基づいて、これらのコスト実績を処理します。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="c8d1b-118">コスト実績が工数と材料の契約品目を参照している場合、見積もりがクローズされてプロジェクト契約が作成されたときに、対応する未請求の販売実績が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="c8d1b-119">コスト実績が固定価格契約品目を参照している場合、アプリケーションは、プロジェクト契約の顧客の分割請求ルールに基づいてコスト実績の再処理を停止します。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="c8d1b-120">再処理されたすべての実績は、プロジェクト管理および会計モジュールで利用可能であり、プロジェクト会計担当者はレビュー、更新、および総勘定元帳への送信を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="c8d1b-121">失注として見積もりをクローズする</span><span class="sxs-lookup"><span data-stu-id="c8d1b-121">Close a quote as Lost</span></span>

<span data-ttu-id="c8d1b-122">失注としてプロジェクト見積もりをクローズすると、見積もりのステータスは **クローズ済み** となり、ステータスの理由は **失注** と設定されます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="c8d1b-123">見積もりをクローズすると、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="c8d1b-124">クローズ済みの見積もりは再度オープンできないため、見積もりをクローズする前に、確認ダイアログで変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c8d1b-125">失注としてクローズされたプロジェクト見積もりのいずれかの品目にプロジェクトが参照されている場合、そのプロジェクトもクローズ済みとしてマークされ、その日以降のリソース予約はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="c8d1b-126">Project Operations では、見積もりを受注または失注としてクローズしても、営業案件のステータスには影響しません。案件は、手動でクローズするまでオープンしたままになります。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
