---
title: 収益認識の概要
description: このトピックでは、Project Operations での売上認識について説明します。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278874"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="08450-103">収益認識の概要</span><span class="sxs-lookup"><span data-stu-id="08450-103">Revenue recognition overview</span></span>

<span data-ttu-id="08450-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="08450-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="08450-105">Dynamics 365 Project Operations で売上認識の原則は、プロジェクトやプロジェクトの一部に対して選択した請求方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="08450-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="08450-106">このトピックでは、Project Operations での売上認識について説明します。</span><span class="sxs-lookup"><span data-stu-id="08450-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="08450-107">時間と材料の請求方法で会計処理したトランザクション</span><span class="sxs-lookup"><span data-stu-id="08450-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="08450-108">コストと収益の認識は関連しています。</span><span class="sxs-lookup"><span data-stu-id="08450-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="08450-109">トランザクションのコストと未請求売上は [Project Operations の統合仕訳帳](../project-accounting/project-operations-integration-journal.md) を使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="08450-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="08450-110">プロジェクトのコストと売上プロファイルは、未請求の売上トランザクションを一般会計に転記するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08450-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="08450-111">**売上計上** を選択する場合、システムは転記中に **仕掛品販売額** と **売上計上の販売額** 勘定を使用します。</span><span class="sxs-lookup"><span data-stu-id="08450-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="08450-112">この方法の例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="08450-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="08450-113">トランザクションの種類</span><span class="sxs-lookup"><span data-stu-id="08450-113">Transaction type</span></span> | <span data-ttu-id="08450-114">借方/貸方</span><span class="sxs-lookup"><span data-stu-id="08450-114">Debit/Credit</span></span> | <span data-ttu-id="08450-115">金額</span><span class="sxs-lookup"><span data-stu-id="08450-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08450-116">仕掛品販売額</span><span class="sxs-lookup"><span data-stu-id="08450-116">WIP Sales value</span></span> | <span data-ttu-id="08450-117">借方</span><span class="sxs-lookup"><span data-stu-id="08450-117">Debit</span></span> | <span data-ttu-id="08450-118">100</span><span class="sxs-lookup"><span data-stu-id="08450-118">100</span></span> |
  | <span data-ttu-id="08450-119">売上計上の販売額</span><span class="sxs-lookup"><span data-stu-id="08450-119">Accrued revenue sales value</span></span> | <span data-ttu-id="08450-120">貸方</span><span class="sxs-lookup"><span data-stu-id="08450-120">Credit</span></span> | <span data-ttu-id="08450-121">100</span><span class="sxs-lookup"><span data-stu-id="08450-121">100</span></span> |

- <span data-ttu-id="08450-122">収益は請求時に認識されます。</span><span class="sxs-lookup"><span data-stu-id="08450-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="08450-123">システムは転記時に **請求済売上** 勘定を使用します。</span><span class="sxs-lookup"><span data-stu-id="08450-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="08450-124">この方法の例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="08450-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="08450-125">トランザクションの種類</span><span class="sxs-lookup"><span data-stu-id="08450-125">Transaction type</span></span> | <span data-ttu-id="08450-126">借方/貸方</span><span class="sxs-lookup"><span data-stu-id="08450-126">Debit/Credit</span></span> | <span data-ttu-id="08450-127">金額</span><span class="sxs-lookup"><span data-stu-id="08450-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08450-128">顧客残高</span><span class="sxs-lookup"><span data-stu-id="08450-128">Customer balance</span></span> | <span data-ttu-id="08450-129">借方</span><span class="sxs-lookup"><span data-stu-id="08450-129">Debit</span></span> | <span data-ttu-id="08450-130">120</span><span class="sxs-lookup"><span data-stu-id="08450-130">120</span></span> |
  | <span data-ttu-id="08450-131">未払い消費税</span><span class="sxs-lookup"><span data-stu-id="08450-131">Sales tax payable</span></span> | <span data-ttu-id="08450-132">貸方</span><span class="sxs-lookup"><span data-stu-id="08450-132">Credit</span></span> | <span data-ttu-id="08450-133">20</span><span class="sxs-lookup"><span data-stu-id="08450-133">20</span></span> |
  | <span data-ttu-id="08450-134">請求済み売上</span><span class="sxs-lookup"><span data-stu-id="08450-134">Invoiced Revenue</span></span> | <span data-ttu-id="08450-135">貸方</span><span class="sxs-lookup"><span data-stu-id="08450-135">Credit</span></span> | <span data-ttu-id="08450-136">100</span><span class="sxs-lookup"><span data-stu-id="08450-136">100</span></span> |

- <span data-ttu-id="08450-137">未請求売上の転記時に売上を計上した場合、システムは請求時に売上計上を取り消します。</span><span class="sxs-lookup"><span data-stu-id="08450-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="08450-138">トランザクションの種類</span><span class="sxs-lookup"><span data-stu-id="08450-138">Transaction type</span></span> | <span data-ttu-id="08450-139">借方/貸方</span><span class="sxs-lookup"><span data-stu-id="08450-139">Debit/Credit</span></span> | <span data-ttu-id="08450-140">金額</span><span class="sxs-lookup"><span data-stu-id="08450-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08450-141">仕掛品販売額</span><span class="sxs-lookup"><span data-stu-id="08450-141">WIP Sales value</span></span> | <span data-ttu-id="08450-142">貸方</span><span class="sxs-lookup"><span data-stu-id="08450-142">Credit</span></span> | <span data-ttu-id="08450-143">100</span><span class="sxs-lookup"><span data-stu-id="08450-143">100</span></span> |
  | <span data-ttu-id="08450-144">売上計上の販売額</span><span class="sxs-lookup"><span data-stu-id="08450-144">Accrued revenue sales value</span></span> | <span data-ttu-id="08450-145">借方</span><span class="sxs-lookup"><span data-stu-id="08450-145">Debit</span></span> | <span data-ttu-id="08450-146">100</span><span class="sxs-lookup"><span data-stu-id="08450-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="08450-147">固定価格の請求方法で会計処理したトランザクション</span><span class="sxs-lookup"><span data-stu-id="08450-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="08450-148">コストと収益の認識は独立しています。</span><span class="sxs-lookup"><span data-stu-id="08450-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="08450-149">トランザクションのコストは [Project Operations の統合仕訳帳](../project-accounting/project-operations-integration-journal.md) を使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="08450-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="08450-150">未請求の売上トランザクションは作成されません。</span><span class="sxs-lookup"><span data-stu-id="08450-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="08450-151">プロジェクトのコストと収益プロファイルで **プロジェクト完了計算に使用する原則** を **仕掛品なし** に設定する場合は、請求時に売上を認識できます。</span><span class="sxs-lookup"><span data-stu-id="08450-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="08450-152">この方法は、短期で単純なプロジェクトにのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="08450-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="08450-153">**完了した契約** または **完了割合の売上認識** の方法を使用すると、売上を固定価格の売上見積りを使用して認識できます。</span><span class="sxs-lookup"><span data-stu-id="08450-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08450-154">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="08450-154">Additional resources</span></span>
[<span data-ttu-id="08450-155">課金プロジェクトの会計構成に関する記事</span><span class="sxs-lookup"><span data-stu-id="08450-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="08450-156">固定価格売上見積もりプロジェクト</span><span class="sxs-lookup"><span data-stu-id="08450-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="08450-157">売上の見積もりの管理</span><span class="sxs-lookup"><span data-stu-id="08450-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="08450-158">完了までの原価の計算方法</span><span class="sxs-lookup"><span data-stu-id="08450-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]