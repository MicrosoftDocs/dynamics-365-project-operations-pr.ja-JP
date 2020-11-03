---
title: 経費ポリシーの設定
description: 従業員が経費報告書や出張申請書を Microsoft Dynamics 365 Finance で入力、提出する際に従う必要がある経費ポリシーを定義することができます。
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079415"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="7b01b-103">経費ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="7b01b-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b01b-104">従業員が経費報告書や出張申請書を入力、提出する際に従う必要があるポリシーを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="7b01b-105">経費のポリシーを実装すると、経費を効果的に管理できます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="7b01b-106">たとえば、ニューヨーク市のホテルの経費に関するポリシーを設定し、1 泊あたりの経費が USD 250 を超えてはいけないことを定めます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="7b01b-107">客室料金がこの金額を超える場合、従業員が経費報告書または出張申請書を提出すると、システムは</span><span class="sxs-lookup"><span data-stu-id="7b01b-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="7b01b-108">経費の規定額を超過していることを従業員に通知します。</span><span class="sxs-lookup"><span data-stu-id="7b01b-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="7b01b-109">従業員に表示するメッセージは、</span><span class="sxs-lookup"><span data-stu-id="7b01b-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="7b01b-110">ポリシーの定義時に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-110">define the policy.</span></span>      
        
<span data-ttu-id="7b01b-111">以下の 3 種類のポシリーを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="7b01b-112">警告 – 従業員は経費報告書や出張依頼書を提出できますが、経費はすべての承認者のためにマークされ、</span><span class="sxs-lookup"><span data-stu-id="7b01b-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="7b01b-113">後で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-113">for later reporting.</span></span>        

- <span data-ttu-id="7b01b-114">エラー – 従業員は、経費報告書または出張申請書を提出する前に、ポリシーに準拠するように経費を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b01b-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="7b01b-115">弁明 – 従業員または管理者が経費報告書や出張申請書を提出する前に、ポリシーで定められた金額を超えることの正当性を入力することを要求します。</span><span class="sxs-lookup"><span data-stu-id="7b01b-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="7b01b-116">ポリシーのポイント</span><span class="sxs-lookup"><span data-stu-id="7b01b-116">Policy tips</span></span>
<span data-ttu-id="7b01b-117">経費管理の新しいポリシーを作成する際に役立ついくつかの提案を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7b01b-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="7b01b-118">ポリシーは、日付の影響を受け、経費が発生した日以降の日付でポリシーが作成された場合には有効となりません。</span><span class="sxs-lookup"><span data-stu-id="7b01b-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="7b01b-119">たとえば、今日、最高で50ドルの食費を適用する新しいポリシーを作成している場合、昨日時点で入力された既存の費用は、このポリシーと照合されません。</span><span class="sxs-lookup"><span data-stu-id="7b01b-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="7b01b-120">項目化できる経費カテゴリのポリシーを作成する際には、経費明細タイプの条件を追加することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="7b01b-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="7b01b-121">領収書の要求などの一部のポリシーは、項目別の行には意味がない場合があり、ヘッダー行または項目別でない行にのみ適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b01b-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="7b01b-122">経費管理ポリシーは、既定ソース エンティティに対して評価されます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="7b01b-123">会社間のシナリオでは、代わりに宛先エンティティ (借用エンティティ) に対して評価されるポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="7b01b-124">宛先エンティティに対してポリシーを実行するには、 **機能管理** ワークスペース内の "借用法人に対する経費方針を評価する" 機能を有効化してください。</span><span class="sxs-lookup"><span data-stu-id="7b01b-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="7b01b-125">ポリシーを評価するタイミング</span><span class="sxs-lookup"><span data-stu-id="7b01b-125">When to evaluate policies</span></span>

<span data-ttu-id="7b01b-126">経費管理パラメータでは、明細行を保存する際、または経費レポートを送信する際に、経費管理ポリシーを評価するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="7b01b-127">明細行が保存される際に評価することを選択した場合、ユーザーは経費報告書を一度に完成させるために何をすべきかをより早く知ることができます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="7b01b-128">それ以外の設定では、ワークフローへの送信中の最後に検証を行うことで、ポリシーの評価を遅らせることができ、時間を節約することができます。</span><span class="sxs-lookup"><span data-stu-id="7b01b-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
