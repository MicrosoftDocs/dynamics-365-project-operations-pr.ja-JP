---
title: クレジット カードの統合の設定
description: このトピックは、経費関連のクレジット カード トランザクションを処理する方法を説明しています。
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866689"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="d3f39-103">クレジット カードの統合の設定</span><span class="sxs-lookup"><span data-stu-id="d3f39-103">Set up credit card integration</span></span>

<span data-ttu-id="d3f39-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d3f39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d3f39-105">経費に関連するクレジットカード トランザクションは、定期的なスケジュールで自動的にインポートされるように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="d3f39-106">または、トランザクションは必要に応じて手動でインポートできます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="d3f39-107">クレジット カードのトランザクションは、クレジット カード トランザクションのデータ エンティティを通じてインポートされます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="d3f39-108">クレジットカード トランザクションをインポートする</span><span class="sxs-lookup"><span data-stu-id="d3f39-108">Import credit card transactions</span></span>

<span data-ttu-id="d3f39-109">クレジット カード トランザクションをインポートするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3f39-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="d3f39-110">**クレジット カード トランザクション** ページで、**トランザクションのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="d3f39-111">データ管理を初めて開く場合は、続行する前に、システムによるデータ エンティティ リストの更新処理が必要となります。</span><span class="sxs-lookup"><span data-stu-id="d3f39-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="d3f39-112">**名前** フィールドに、インポート ジョブの一意の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="d3f39-113">**ソースデータ形式** フィールドで、インポートするクレジットカード トランザクションを含むファイルの形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="d3f39-114">**アップロード** を選択し、インポートするファイルを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="d3f39-115">ファイルがアップロードされたら、タイル上の **マッピングを参照する** リンクを選択して、クレジット カード トランザクション ファイルのマッピングとクレジット カード トランザクション データ エンティティの列を検証します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="d3f39-116">マッピング エラーがある場合、またはマッピングを変更する必要がある場合は、**マッピングの視覚化** タブ、または **マッピングの詳細** タブのいずれかからマッピングを変更します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="d3f39-117">クレジットカード トランザクションを自動化するには、**定期的なデータジョブを作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="d3f39-118">次に、クレジット カード トランザクションのインポート頻度を定義する繰り返しの設定をします。</span><span class="sxs-lookup"><span data-stu-id="d3f39-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="d3f39-119">完了後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="d3f39-120">選択したファイルをすぐにインポートするには、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="d3f39-121">インポート中にエラーが発生した場合は、実行ログまたはステージング データを表示して、インポートを成功させるために修正すべきエラーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="d3f39-122">複数のファイル形式をインポートする必要がある場合は、形式タイプごとに個別のインポート ジョブを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3f39-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="d3f39-123">退職した従業員にクレジット カード トランザクションを再割り当てする</span><span class="sxs-lookup"><span data-stu-id="d3f39-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="d3f39-124">従業員レコードが終了すると、従業員の Active Directory Domain Services (AD DS) アカウントが無効になります。</span><span class="sxs-lookup"><span data-stu-id="d3f39-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="d3f39-125">ただし、まだ経費と精算が必要となる有効なクレジットカード トランザクションが残っている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3f39-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="d3f39-126">**クレジット カード トランザクション** ページでは、関連する従業員が解雇されたクレジット カード トランザクションに従業員を再割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="d3f39-127">1つ以上のクレジットカード トランザクションを選択してから、**トランザクションの再割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="d3f39-128">続いて、クレジットカード取引を割り当てる別の従業員を選択できます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="d3f39-129">クレジットカードの取引が再割り当てされた後は、経費報告書に選択し、経費報告書の精算を行う通常のプロセスで支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="d3f39-130">クレジット カード トランザクションを削除する</span><span class="sxs-lookup"><span data-stu-id="d3f39-130">Delete credit card transactions</span></span> 

<span data-ttu-id="d3f39-131">クレジット カード トランザクションをインポートした後、特定のトランザクションを削除しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3f39-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="d3f39-132">これは、トランザクションが重複しているか、データが正確でない可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="d3f39-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="d3f39-133">管理者は **「クレジットカード取引を削除する」** 機能を使って、経費報告書に **添付されていない** クレジット カード トランザクションを選択して削除できます。</span><span class="sxs-lookup"><span data-stu-id="d3f39-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="d3f39-134">**定期的なタスク** > **クレジット カード トランザクションを削除する** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="d3f39-135">**フィルター** を選択して、含めるレコードを識別するための情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="d3f39-136">レコードを削除するには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f39-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
