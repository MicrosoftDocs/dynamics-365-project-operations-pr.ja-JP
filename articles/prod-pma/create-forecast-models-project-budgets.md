---
title: プロジェクト予算の予測モデルを作成する
description: このトピックでは、残りの予算の予測モデルの作成方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271044"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="61ced-103">プロジェクト予算の予測モデルを作成する</span><span class="sxs-lookup"><span data-stu-id="61ced-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61ced-104">このトピックでは、残りの予算の予測モデルの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="61ced-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="61ced-105">予算管理の対象となるプロジェクトでは、元の予算と残りの予算の 2 種類の予算を使用します。</span><span class="sxs-lookup"><span data-stu-id="61ced-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="61ced-106">プロジェクト予算を作成する際には、**予測モデル** ページで作成した元の予算予測モデルと残りの予算予測モデルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61ced-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="61ced-107">指定したモデルに基づくプロジェクト予算は、プロジェクト予算のコミット時に作成されます。</span><span class="sxs-lookup"><span data-stu-id="61ced-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="61ced-108">予算管理で使用される予測モデルは、サブモデルを持つことも、サブモデルとして使用することもできません。</span><span class="sxs-lookup"><span data-stu-id="61ced-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="61ced-109">**プロジェクト管理と会計** > **設定** > **予測**  > **予測モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61ced-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="61ced-110">**新規** を選択して、新しい予測モデルを作成し、新しいモデルのモデル ID 番号と名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="61ced-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="61ced-111">**停止** オプションを **はい** に設定して、 予測モデルの予測ラインの変更を防止します。</span><span class="sxs-lookup"><span data-stu-id="61ced-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="61ced-112">モデルが関連付けられている予測ラインが総勘定元帳にキャッシュフロー予測を生成する必要がある場合は、、**キャッシュフロー予測に含める** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="61ced-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="61ced-113">プロジェクトの日付を請求書の日付として使用する場合は、**予測請求書の日付** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="61ced-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="61ced-114">**計算タイプ** フィールドで、次のいずれかのモデル タイプを選択します :</span><span class="sxs-lookup"><span data-stu-id="61ced-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="61ced-115">**当初の予算** : 当初の予算が作成され承認された際にコミットされた元の予算額を使用します。</span><span class="sxs-lookup"><span data-stu-id="61ced-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="61ced-116">**残りの予算** : プロジェクトの存続期間中、残りの予算額を使用します。</span><span class="sxs-lookup"><span data-stu-id="61ced-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="61ced-117">この予測モデルの残高は、実際のトランザクションによって減少し、予算の修正によって増減します。</span><span class="sxs-lookup"><span data-stu-id="61ced-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="61ced-118">**繰り越し** : プロジェクトの繰越予算額を使用します。</span><span class="sxs-lookup"><span data-stu-id="61ced-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="61ced-119">繰り越しは、未使用の予算額をある会計年度から別の会計年度に移すために実行できる任意のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="61ced-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="61ced-120">必要に応じて次のオプションを設定します :</span><span class="sxs-lookup"><span data-stu-id="61ced-120">Set the following options as required:</span></span>

   - <span data-ttu-id="61ced-121">**予測請求日** を有効にして、プロジェクトの日付を請求日として使用します。</span><span class="sxs-lookup"><span data-stu-id="61ced-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="61ced-122">仕掛品 (WIP) に基づいて予測する場合は、**WIP で予測** を有効にし、WIP の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="61ced-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="61ced-123">既定の **予算タイプ** を **無し** のままにするか、新しいタイプを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="61ced-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="61ced-124">レコードを変更しても予算タイプは変更できません。</span><span class="sxs-lookup"><span data-stu-id="61ced-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="61ced-125">既定の予算タイプを変更すると、他のすべてのオプションが更新できなくなり、この予測モデルを再利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="61ced-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]