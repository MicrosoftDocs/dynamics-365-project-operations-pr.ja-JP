---
title: クレジット カード トランザクションのインポートと維持
description: このトピックでは、経費に関連するクレジットカードのトランザクションをインポートして管理する方法を説明しています。 これらのトランザクションは、定期的なスケジュールで自動的にインポートされるように設定することもできますし、必要に応じて手動でインポートすることもできます。
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951080"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="73acf-104">クレジット カード トランザクションのインポートと維持</span><span class="sxs-lookup"><span data-stu-id="73acf-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="73acf-105">経費に関連するクレジットカード トランザクションは、定期的なスケジュールで自動的にインポートされるように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="73acf-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="73acf-106">または、トランザクションは必要に応じて手動でインポートできます。</span><span class="sxs-lookup"><span data-stu-id="73acf-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="73acf-107">クレジットカードのトランザクションは、クレジットカード トランザクションのデータ エンティティを通じてインポートされます。</span><span class="sxs-lookup"><span data-stu-id="73acf-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="73acf-108">データエンティティの暗号化に関する詳細については、[データ エンティティ](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73acf-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="73acf-109">クレジットカード トランザクションをインポートする</span><span class="sxs-lookup"><span data-stu-id="73acf-109">Import credit card transactions</span></span>

1. <span data-ttu-id="73acf-110">**クレジット カード トランザクション** ページで、**トランザクションのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="73acf-111">データ管理を初めて開く場合は、続行する前に、システムによるデータ エンティティ リストの更新処理が必要となります。</span><span class="sxs-lookup"><span data-stu-id="73acf-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="73acf-112">**名前** フィールドに、インポート ジョブの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="73acf-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="73acf-113">**ソースデータ形式** フィールドで、インポートするクレジットカード トランザクションを含むファイルの形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="73acf-114">**アップロード** を選択し、インポートするファイルを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="73acf-115">ファイルがアップロードされた後、タイル上の **マッピングを参照する** リンクを選択して、クレジット カード トランザクションファイルのマッピングとクレジットカード トランザクション データ エンティティの列を検証します。</span><span class="sxs-lookup"><span data-stu-id="73acf-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="73acf-116">マッピング エラーがある場合、またはマッピングを変更する必要がある場合は、**マッピングの視覚化** タブ、または **マッピングの詳細** タブのいずれかからマッピングを変更します。</span><span class="sxs-lookup"><span data-stu-id="73acf-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="73acf-117">クレジットカード トランザクションを自動化するには、**定期的なデータジョブを作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="73acf-118">次に、クレジット カード トランザクションのインポート頻度を定義する繰り返しの設定をします。</span><span class="sxs-lookup"><span data-stu-id="73acf-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="73acf-119">完了後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="73acf-120">選択したファイルをすぐにインポートするには、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="73acf-121">インポート中にエラーが発生した場合、実行ログやステージング データを確認することで、修正が必要なデータを把握し、インポートを成功に導くことができます。</span><span class="sxs-lookup"><span data-stu-id="73acf-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="73acf-122">複数のファイル形式をインポートする必要がある場合は、形式の種類ごとに個別のインポート ジョブを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73acf-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="73acf-123">退職した従業員にクレジット カード トランザクションを再割り当てする</span><span class="sxs-lookup"><span data-stu-id="73acf-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="73acf-124">従業員レコードが終了すると、従業員の Active Directory Domain Services (AD DS) アカウントが無効になります。</span><span class="sxs-lookup"><span data-stu-id="73acf-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="73acf-125">ただし、まだ経費と精算が必要となる有効なクレジットカード トランザクションが残っている場合があります。</span><span class="sxs-lookup"><span data-stu-id="73acf-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="73acf-126">**クレジット カード決済** ページから、関連する従業員が退職したクレジット カード トランザクションに従業員を再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="73acf-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="73acf-127">1つ以上のクレジットカード トランザクションを選択してから、**トランザクションの再割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73acf-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="73acf-128">続いて、クレジットカード取引を割り当てる別の従業員を選択できます。</span><span class="sxs-lookup"><span data-stu-id="73acf-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="73acf-129">クレジットカードの取引が再割り当てされた後は、経費報告書に選択し、経費報告書の精算を行う通常のプロセスで支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="73acf-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]