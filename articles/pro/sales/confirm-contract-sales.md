---
title: プロジェクト契約の確認
description: このトピックは、Project Operations で契約を確認する方法について説明します。
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003682"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="8946a-103">プロジェクト契約の確認</span><span class="sxs-lookup"><span data-stu-id="8946a-103">Confirm a project contract</span></span>

<span data-ttu-id="8946a-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="8946a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8946a-105">Dynamics 365 Project Operations のプロジェクト契約は、**確認済み** という理由でアクティブにするか、または **失注** という理由でクローズすることができます。</span><span class="sxs-lookup"><span data-stu-id="8946a-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="8946a-106">プロジェクト契約を確認すると、状態が **下書き** から **アクティブ** に更新され、状態の理由が **確認済み** になります。</span><span class="sxs-lookup"><span data-stu-id="8946a-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="8946a-107">アクティブまたはクローズされた契約は、編集や再開することはできません。</span><span class="sxs-lookup"><span data-stu-id="8946a-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="8946a-108">プロジェクト契約の確認による財務的影響</span><span class="sxs-lookup"><span data-stu-id="8946a-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="8946a-109">プロジェクト契約が確認された後、アプリケーションでは、古い原価実績を逆仕訳して新しい原価実績を作成することで、原価を再計算します。</span><span class="sxs-lookup"><span data-stu-id="8946a-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="8946a-110">新しい原価実績は、関連付けられているプロジェクト契約品目の請求方法に基づいて処理されます。</span><span class="sxs-lookup"><span data-stu-id="8946a-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="8946a-111">コスト実績が時間と材料の契約品目を参照している場合、アプリケーションは自動的に対応する未請求の売上実績を再作成します。</span><span class="sxs-lookup"><span data-stu-id="8946a-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="8946a-112">コスト実績が固定価格契約品目を参照している場合、アプリケーションはコスト実績の再処理を停止します。</span><span class="sxs-lookup"><span data-stu-id="8946a-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="8946a-113">限度額、課金設定、実績上の価格設定、原価計算を評価し、確認作業の一環として更新されます。</span><span class="sxs-lookup"><span data-stu-id="8946a-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="8946a-114">プロジェクト契約を失注としてクローズする</span><span class="sxs-lookup"><span data-stu-id="8946a-114">Close a project contract as lost</span></span>

<span data-ttu-id="8946a-115">失注したプロジェクト契約をクローズすると、契約の状態は **クローズ** に更新され、ステータスは **失注** となります。</span><span class="sxs-lookup"><span data-stu-id="8946a-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="8946a-116">プロジェクト契約は読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="8946a-116">The project contract becomes read-only.</span></span> <span data-ttu-id="8946a-117">クローズしたプロジェクト契約を再開することはできないため、変更が完了する前にじゃ確認ダイアログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8946a-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="8946a-118">失われたとしてクローズされたプロジェクト契約がそのライン上のプロジェクトを参照している場合、そのプロジェクトもクローズとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="8946a-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="8946a-119">この日付以降のリソース予約はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="8946a-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="8946a-120">プロジェクト契約書の未請求の売上実績が、請求書に載っていないものは取り消されてしまいます。</span><span class="sxs-lookup"><span data-stu-id="8946a-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="8946a-121">Dynamics 365 Project Operations では、失注としてプロジェクト契約をクローズしても、関連付けられた機会のそのステータスには影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="8946a-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="8946a-122">営業案件はオープンの状態のままなので、手動でクローズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8946a-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]