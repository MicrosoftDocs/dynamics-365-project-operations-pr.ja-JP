---
title: 会社間経費
description: このトピックでは、会社間経費を使用して、作業が実行された法人に作業者の経費を割り当てる方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960838"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="5139a-103">会社間経費</span><span class="sxs-lookup"><span data-stu-id="5139a-103">Intercompany expenses</span></span>

<span data-ttu-id="5139a-104">組織内のある法人に雇用されている作業者が、同じ組織内の別の法人で作業を行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="5139a-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="5139a-105">会社間経費を使用して、作業が実行された法人に作業者の経費を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5139a-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="5139a-106">作業者を雇用する法人は、貸与法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5139a-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="5139a-107">作業者が費用を負担する法人は、借用法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5139a-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="5139a-108">作業者が会社間経費を作成して提出する前に、会社間経費明細行を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5139a-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="5139a-109">貸付法人では、**経費管理パラメーター** ページで、**会社間経費明細行を許可する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5139a-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="5139a-110">会社間費用の税転記</span><span class="sxs-lookup"><span data-stu-id="5139a-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5139a-111">経費精算書で借用法人 (ソース) ではなく貸与法人 (デスティネーション) に関連付けられている税グループを使用できるようになる前に、一般会計の消費税パラメーターのセットアップで機能を有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5139a-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="5139a-112">**会社間税転記の法人** パラメーターが **ソース** に設定され、**消費税課税ルールの適用** フィールドが **いいえ** に設定されている場合、貸与法人の税の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5139a-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="5139a-113">同じパラメーターが **宛先** に設定されている場合、借用法人の税の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5139a-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="5139a-114">米国の法人の場合、パラメーターが **ソース** に設定されている場合、**消費税収入** フィールドも新しい **元帳転記グループ** ページで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5139a-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="5139a-115">会計エンジンは、このフィールドの情報を税関連の会計入力に使用します。</span><span class="sxs-lookup"><span data-stu-id="5139a-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="5139a-116">プロジェクトの有無にかかわらず転記された経費明細の動作は一貫しています。</span><span class="sxs-lookup"><span data-stu-id="5139a-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
