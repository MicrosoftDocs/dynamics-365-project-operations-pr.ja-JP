---
title: 経費のポリシーを定義する
description: 従業員が経費報告書や出張申請書を入力、提出する際に従う必要がある経費のポリシーを定義することができます。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001882"
---
# <a name="define-expense-policies"></a><span data-ttu-id="5fafe-103">経費のポリシーを定義する</span><span class="sxs-lookup"><span data-stu-id="5fafe-103">Define expense policies</span></span>

<span data-ttu-id="5fafe-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="5fafe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5fafe-105">従業員が経費報告書や出張申請書を入力、提出する際に従う必要があるポリシーを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="5fafe-106">経費ポリシーを実装すると、経費管理を効率化することができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="5fafe-107">たとえば、ニューヨークでのホテルの支払いに対して、1 泊の代金が 250 ドルを超えることを許可しないというポリシーを設定したとします。</span><span class="sxs-lookup"><span data-stu-id="5fafe-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="5fafe-108">客室料金がこの金額を超える場合、従業員が経費報告書または出張申請書を提出すると、システムは</span><span class="sxs-lookup"><span data-stu-id="5fafe-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="5fafe-109">経費の規定額を超過していることを従業員に通知します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="5fafe-110">従業員に表示するメッセージは、</span><span class="sxs-lookup"><span data-stu-id="5fafe-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="5fafe-111">ポリシーの定義時に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-111">define the policy.</span></span>      
        
<span data-ttu-id="5fafe-112">以下の 3 種類のポシリーを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="5fafe-113">**警告** : 従業員は経費報告書や出張依頼書を提出できますが、経費はすべての承認者のためにマークされ、</span><span class="sxs-lookup"><span data-stu-id="5fafe-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="5fafe-114">後で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-114">for later reporting.</span></span>        

- <span data-ttu-id="5fafe-115">**エラー** : 従業員は、経費報告書または出張申請書を提出する前に、ポリシーに準拠するように経費を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fafe-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="5fafe-116">**弁明** : 従業員または管理者が経費報告書や出張申請書を提出する前に、ポリシーで定められた金額を超えることの正当性を入力することを要求します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="5fafe-117">ポリシーのヒント</span><span class="sxs-lookup"><span data-stu-id="5fafe-117">Policy tips</span></span>
<span data-ttu-id="5fafe-118">経費管理で新しいポリシーを作成する際に役立つヒントをいくつかご提案します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="5fafe-119">ポリシーには有効日があり、経費が発生した日付よりも後に作成された経費にはポリシーが適用されません。</span><span class="sxs-lookup"><span data-stu-id="5fafe-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="5fafe-120">たとえば、1 回の食事代の上限を 50 ドルとするポリシーを、今日新しく作成した場合、</span><span class="sxs-lookup"><span data-stu-id="5fafe-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="5fafe-121">このポリシーによるチェックは、昨日の時点で入力された経費に対しては行われません。</span><span class="sxs-lookup"><span data-stu-id="5fafe-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="5fafe-122">明細に分けられる経費カテゴリに対してポリシーを作成する場合は、経費明細行の種類に条件を追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5fafe-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="5fafe-123">ポリシーが、「領収書が必要」などである場合、明細行によっては適用できない場合があるからです。</span><span class="sxs-lookup"><span data-stu-id="5fafe-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="5fafe-124">この場合は、ヘッダー行または明細に分かれてない行に対してのみ、ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="5fafe-125">経費管理ポリシーの評価は、既定でソース エンティティに対して行われます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="5fafe-126">企業間のシナリオでは、宛先エンティティ (借入エンティティ) に対して評価を行うように、ポリシーを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="5fafe-127">宛先エンティティに対してポリシーを実行するには、**機能管理** ワークスペース内の **借用法人に対する経費方針を評価する** 機能を有効化してください。</span><span class="sxs-lookup"><span data-stu-id="5fafe-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="5fafe-128">ポリシーを評価するタイミング</span><span class="sxs-lookup"><span data-stu-id="5fafe-128">When to evaluate policies</span></span>

<span data-ttu-id="5fafe-129">経費管理パラメータでは、明細を保存する際、または経費レポートを送信する際に、経費管理ポリシーを評価するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="5fafe-130">明細行が保存されるタイミングで評価することを選択した場合、ユーザーは経費報告書を一度に完成させるために何をすべきかをより早く知ることができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="5fafe-131">それ以外の設定では、ワークフローへの送信中の最後に検証を行うことで、ポリシーの評価を遅らせることができ、時間を節約することができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]