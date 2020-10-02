---
title: クレジット カードの統合の設定
description: このトピックでは、経費に関連するクレジットカードのトランザクションをインポートして管理する方法を説明しています。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896827"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="2732d-103">クレジット カードの統合の設定</span><span class="sxs-lookup"><span data-stu-id="2732d-103">Set up credit card integration</span></span>

<span data-ttu-id="2732d-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="2732d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2732d-105">経費に関連するクレジットカード トランザクションは、定期的なスケジュールで自動的にインポートされるように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2732d-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="2732d-106">または、トランザクションは必要に応じて手動でインポートできます。</span><span class="sxs-lookup"><span data-stu-id="2732d-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="2732d-107">クレジットカードのトランザクションは、クレジットカード トランザクションのデータ エンティティを通じてインポートされます。</span><span class="sxs-lookup"><span data-stu-id="2732d-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="2732d-108">クレジットカード トランザクションをインポートする</span><span class="sxs-lookup"><span data-stu-id="2732d-108">Import credit card transactions</span></span>

1. <span data-ttu-id="2732d-109">**クレジット カード トランザクション**ページで、**トランザクションのインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="2732d-110">データ管理を初めて開く場合は、続行する前に、システムによるデータ エンティティ リストの更新処理が必要となります。</span><span class="sxs-lookup"><span data-stu-id="2732d-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="2732d-111">**名前**フィールドに、インポート ジョブの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2732d-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="2732d-112">**ソースデータ形式**フィールドで、インポートするクレジットカード トランザクションを含むファイルの形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="2732d-113">**アップロード**を選択し、インポートするファイルを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="2732d-114">ファイルがアップロードされた後、タイル上の**マッピングを参照する**リンクを選択して、クレジット カード トランザクションファイルのマッピングとクレジットカード トランザクション データ エンティティの列を検証します。</span><span class="sxs-lookup"><span data-stu-id="2732d-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="2732d-115">マッピング エラーがある場合、またはマッピングを変更する必要がある場合は、**マッピングの視覚化**タブ、または**マッピングの詳細**タブのいずれかからマッピングを変更します。</span><span class="sxs-lookup"><span data-stu-id="2732d-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="2732d-116">クレジットカード トランザクションを自動化するには、**定期的なデータジョブを作成する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="2732d-117">次に、クレジット カード トランザクションのインポート頻度を定義する繰り返しの設定をします。</span><span class="sxs-lookup"><span data-stu-id="2732d-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="2732d-118">完了後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="2732d-119">選択したファイルをすぐにインポートするには、**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="2732d-120">インポート中にエラーが発生した場合、実行ログやステージング データを確認することで、修正が必要なデータを把握し、インポートを成功に導くことができます。</span><span class="sxs-lookup"><span data-stu-id="2732d-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="2732d-121">複数のファイル形式をインポートする必要がある場合は、形式の種類ごとに個別のインポート ジョブを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2732d-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="2732d-122">退職した従業員にクレジット カード トランザクションを再割り当てする</span><span class="sxs-lookup"><span data-stu-id="2732d-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="2732d-123">従業員レコードが終了すると、従業員の Active Directory Domain Services (AD DS) アカウントが無効になります。</span><span class="sxs-lookup"><span data-stu-id="2732d-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="2732d-124">ただし、まだ経費と精算が必要となる有効なクレジットカード トランザクションが残っている場合があります。</span><span class="sxs-lookup"><span data-stu-id="2732d-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="2732d-125">**クレジット カード決済**ページから、関連する従業員が退職したクレジット カード トランザクションに従業員を再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="2732d-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="2732d-126">1つ以上のクレジットカード トランザクションを選択してから、**トランザクションの再割り当て**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2732d-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="2732d-127">続いて、クレジットカード取引を割り当てる別の従業員を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2732d-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="2732d-128">クレジットカードの取引が再割り当てされた後は、経費報告書に選択し、経費報告書の精算を行う通常のプロセスで支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="2732d-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
