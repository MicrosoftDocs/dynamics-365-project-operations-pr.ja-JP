---
title: 会社間経費
description: 組織内のある法人に雇用されている作業者は、同じ組織内の別の法人のために仕事をする場合があります。 この状況では、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079419"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="65ff1-104">会社間経費</span><span class="sxs-lookup"><span data-stu-id="65ff1-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65ff1-105">組織内のある法人に雇用されている作業者は、同じ組織内の別の法人のために仕事をする場合があります。</span><span class="sxs-lookup"><span data-stu-id="65ff1-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="65ff1-106">この状況では、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="65ff1-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="65ff1-107">作業者を雇用する法人は、貸与法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="65ff1-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="65ff1-108">作業者が費用を負担する法人は、借用法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="65ff1-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="65ff1-109">作業者が別の法人のために行われる作業の費用を作成して提出できるようにするには、貸与法人の **経費管理パラメーター** ページで、 **会社間経費明細の許可** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff1-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="65ff1-110">会社間費用の税転記</span><span class="sxs-lookup"><span data-stu-id="65ff1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65ff1-111">経費報告書で借用 (宛先) 法人の代わりに貸与 (ソース) 法人に関連付けられている税グループを使用する場合は、一般会計の消費税設定でこれを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ff1-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="65ff1-112">一般会計パラメーター、 **会社間税転記の法人** が **ソース** に設定され、 **消費税課税ルールの適用** が **いいえ** に設定されている場合、貸与法人の税の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="65ff1-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="65ff1-113">同じパラメーターが **宛先** に設定されている場合、借用法人の税の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="65ff1-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="65ff1-114">米国の法人の場合、パラメーターが **ソース** に設定されている場合、 **消費税収入** フィールドも新しい **元帳転記グループ** ページで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ff1-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="65ff1-115">会計エンジンは、このフィールドの情報を税関連の会計入力に使用します。</span><span class="sxs-lookup"><span data-stu-id="65ff1-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="65ff1-116">プロジェクトの有無にかかわらず転記された経費明細の動作は一貫しています。</span><span class="sxs-lookup"><span data-stu-id="65ff1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
