---
title: プロジェクト見積の削除
description: このトピックは、プロジェクトの見積もりの完了後に、これを削除する方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079321"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="2ba2e-103">プロジェクト見積の削除</span><span class="sxs-lookup"><span data-stu-id="2ba2e-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ba2e-104">プロジェクトの見積もりでは、プロジェクトの見積もりと予定されている作業の財務的なビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="2ba2e-105">プロジェクトの見積もりを処理するには、プロジェクトを見積もりのプロジェクトに添付する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="2ba2e-106">見積もりのプロジェクトは常に既存のプロジェクトに基づいていますが、複数のプロジェクトが 1 つの見積もりプロジェクトを参照する場合があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="2ba2e-107">見積もりプロジェクトには、固定価格プロジェクトと投資プロジェクトのみを添付することができ、それらのプロジェクトは見積プロジェクトと同じプロジェクト グループに所属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="2ba2e-108">見積もりプロジェクトを削除するには、それが完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="2ba2e-109">次の手順では、見積もりを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="2ba2e-110">**プロジェクト管理と会計** > **すべてのプロジェクト** の順に移動し、プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="2ba2e-111">**管理する** タブで、 **見積り** を開き、 **見積もり** ページで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="2ba2e-112">**見積もりを削除する** ページの **全般** タブで、次のオプションを設定します :</span><span class="sxs-lookup"><span data-stu-id="2ba2e-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="2ba2e-113">**期間コード** : 期間コードを選択して、適切な見積もりプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="2ba2e-114">**見積もり日** : 削除を行う適切な見積もり日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="2ba2e-115">**WIP の警告で削除する** ：このオプションを有効にすると、仕掛品 (WIP) に関連付けられた見積もりが通知されます。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="2ba2e-116">このオプションが有効になっていない場合、見積もりがされていないトランザクションが存在すると、削除を続行できません。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="2ba2e-117">このオプションは、見積もりプロジェクトに消去が適用されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="2ba2e-118">定期的な転記を使用している場合は利用できません。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="2ba2e-119">この設定は、 **プロジェクト パラメーター** ページの **見積もり** タブの **見積もりされていないトランザクションが存在する場合に削除を許可する** フィールド グループの設定と連動します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="2ba2e-120">**ステージを完了に設定する** : このオプションを有効にすると、消去を実行した後に見積もりプロジェクトのステージを **完了** に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="2ba2e-121">**見積もりの一覧を印刷する** : 見積もりの一覧を印刷するときに含める情報を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="2ba2e-122">**情報ログを表示** : このオプションを有効にすると、情報ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="2ba2e-123">**転記日** : 見積もりの台帳転記日を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="2ba2e-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-124">Select **OK**.</span></span>
5. <span data-ttu-id="2ba2e-125">消去プロセスが完了すると、消去された見積もりのプロジェクトが負の値で表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="2ba2e-126">見積もりを誤って削除した場合は、削除された見積もりを選択して、 **削除の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ba2e-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
