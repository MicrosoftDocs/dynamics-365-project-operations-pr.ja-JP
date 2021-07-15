---
title: ドラフト プロジェクトの請求書提案の会計を修正する
description: このトピックでは、請求書の提案の会計に関する情報を調整する方法について説明します。
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251234"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="55f6d-103">ドラフト プロジェクトの請求書提案の会計を修正する</span><span class="sxs-lookup"><span data-stu-id="55f6d-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="55f6d-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="55f6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="55f6d-105">プロジェクト請求書の *運用詳細* は、プロジェクト マネージャーがプロフォーマ請求書で管理します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="55f6d-106">これらの詳細には、請求を発行する必要のある時間、費用、資料、またはマイルストーン、料金、および前払金額と保持金額の適用に関する決定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="55f6d-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="55f6d-107">オリジナルのプロフォーマ請求書を確認した後に、[修正プロフォーマ請求書](../proforma-invoicing/corrective-invoices.md)を作成、確認することで、運用内容を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="55f6d-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="55f6d-108">プロジェクトの請求書の *会計の詳細* は、顧客向けの請求書ドキュメントで管理されます。</span><span class="sxs-lookup"><span data-stu-id="55f6d-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="55f6d-109">これらの詳細には、請求書に適用される消費税の計算と財務分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="55f6d-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="55f6d-110">このトピックでは、プロジェクト請求書のドラフトでこれらの会計詳細を調整する方法について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="55f6d-111">消費税のの調整</span><span class="sxs-lookup"><span data-stu-id="55f6d-111">Adjust sales tax</span></span>

<span data-ttu-id="55f6d-112">既定の請求売上税グループと品目売上税グループは、請求書提案伝票で直接調整できます。</span><span class="sxs-lookup"><span data-stu-id="55f6d-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="55f6d-113">これらのグループを調整するには、**編集** を選択し、続いて各プロジェクト請求書の提案明細行で、**消費税グループ** フィールド、または **品目の消費税グループ** フィールドに新しい値を入力します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="55f6d-114">財務分析コードの調整</span><span class="sxs-lookup"><span data-stu-id="55f6d-114">Adjust financial dimensions</span></span>

<span data-ttu-id="55f6d-115">財務分析コードは、プロジェクトの請求書提案明細で直接編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="55f6d-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="55f6d-116">代わりに、以下の手順でプロジェクトの請求書提案の財務分析コードを調整します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="55f6d-117">プロジェクトの請求書の提案で、**すべて削除** を選択してプロジェクトの請求書提案の明細行を削除します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="55f6d-118">**すべて削除** ボタンは、システム管理者がこ次の機能を有効にした後でのみ使用できます: **機能管理** ワークスペースの **リソース ベース/非在庫のシナリオで Project Operations を使用する場合に、請求書の提案明細行を削除する** 機能。</span><span class="sxs-lookup"><span data-stu-id="55f6d-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="55f6d-119">財務分析コードの調整:</span><span class="sxs-lookup"><span data-stu-id="55f6d-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="55f6d-120">**当座預金取引 (請求マイルストーン):** **すべてのプロジェクト** \> **管理** \> **当座預金取引** にアクセスし、調整が必要なマイルストーンを選択します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="55f6d-121">次に、**財務分析コード** タブで、必要に応じて値を更新します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="55f6d-122">**投稿されたプロジェクトトランザクション** ページの **時間、費用、重要なトランザクション:** で、**会計の調整** を選択し、財務分析コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="55f6d-123">財務分析コード値の調整が終了後は、**プロジェクト管理と会計** \> **定期的** \> **Project Operations の統合** にアクセスし、**ステージングテーブルからインポート** を選択して定期的なプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="55f6d-124">このプロセスでは、更新された財務分析コードの値を使用して、プロジェクトの請求書提案明細を再作成します。</span><span class="sxs-lookup"><span data-stu-id="55f6d-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="55f6d-125">更新された値は、プロジェクトの請求書が計上される際に、プロジェクトのサブ台帳と全般台帳で使用されます。</span><span class="sxs-lookup"><span data-stu-id="55f6d-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
