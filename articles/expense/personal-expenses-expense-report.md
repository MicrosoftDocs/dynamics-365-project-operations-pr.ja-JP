---
title: 経費精算書の個人経費の処理
description: このトピックでは、出張中に従業員が負担する個人的な経費を処理する方法に関する情報を説明します。
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025690"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="29a22-103">経費精算書の個人経費の処理</span><span class="sxs-lookup"><span data-stu-id="29a22-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="29a22-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="29a22-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29a22-105">出張時に、従業員が個人経費を会社のクレジット カードで支払う場合があります。</span><span class="sxs-lookup"><span data-stu-id="29a22-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="29a22-106">個人経費を処理するプロセスを定義していない場合、従業員が経費明細精算書を提出する際に経費精算書の承認プロセスが混乱する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="29a22-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="29a22-107">従業員の個人経費を処理する方法は 2 通りあります。</span><span class="sxs-lookup"><span data-stu-id="29a22-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="29a22-108">**従業員による支払い**: 組織は、会社のクレジット カードの請求書に記載されている個人的な経費を支払いません。</span><span class="sxs-lookup"><span data-stu-id="29a22-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="29a22-109">代わりに、従業員はクレジット カード ベンダーに直接支払います。</span><span class="sxs-lookup"><span data-stu-id="29a22-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="29a22-110">**会社による支払い**: 組織が会社のクレジット カードの全額を支払い、その後、個人経費を作業者の口座から引き落とします。</span><span class="sxs-lookup"><span data-stu-id="29a22-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="29a22-111">**経費管理パラメーター** ページで、組織が使用する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="29a22-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="29a22-112">個人金額フィールドに値が定義されている場合に経費分割機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="29a22-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="29a22-113">機能 **個人金額フィールドに値が定義されている場合に経費分割機能を有効にする** は、明細行レベルのワークフローを使用して承認された経費精算書にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="29a22-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="29a22-114">レポートは、**経費精算書の処理** > **自分に割り当てられた経費精算書** > **経費精算書を開く** の順に進んで承認します。</span><span class="sxs-lookup"><span data-stu-id="29a22-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="29a22-115">この機能を有効にするには、**ワークスペース** > **機能管理** に移動し、**個人金額フィールドに値が定義されている場合に経費分割機能を有効にする** を選択し、**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29a22-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="29a22-116">この機能を有効にすると、この機能を使用した経費明細行は、レポートの送信時に 2 つの明細行を生成します。</span><span class="sxs-lookup"><span data-stu-id="29a22-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="29a22-117">承認者が各明細行を個別に承認できるように、2 つの明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="29a22-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
