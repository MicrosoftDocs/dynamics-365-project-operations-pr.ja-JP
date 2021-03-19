---
title: 2021 年 2 月の新機能 - Project Operations のライト展開
description: このトピックでは、Project Operations のライト展開の 2021 年 2 月リリースで利用可能な品質更新について説明します。
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: df6490d3d9c28b095efd5ef856064de4b1517055
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272169"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a><span data-ttu-id="59896-103">2021 年 2 月の新機能 - Project Operations のライト展開</span><span class="sxs-lookup"><span data-stu-id="59896-103">What's new February 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="59896-104">このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:</span><span class="sxs-lookup"><span data-stu-id="59896-104">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

  - <span data-ttu-id="59896-105">Dataverse 環境バージョン 4.7.0.95 での Project Operations</span><span class="sxs-lookup"><span data-stu-id="59896-105">Project Operations on Dataverse environment version 4.7.0.95</span></span>

## <a name="quality-updates"></a><span data-ttu-id="59896-106">品質更新プログラム</span><span class="sxs-lookup"><span data-stu-id="59896-106">Quality updates</span></span>

| <span data-ttu-id="59896-107">**機能領域**</span><span class="sxs-lookup"><span data-stu-id="59896-107">**Feature Area**</span></span> | <span data-ttu-id="59896-108">**照合番号**</span><span class="sxs-lookup"><span data-stu-id="59896-108">**Reference number**</span></span> | <span data-ttu-id="59896-109">**品質更新プログラム**</span><span class="sxs-lookup"><span data-stu-id="59896-109">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="59896-110">**請求と価格**</span><span class="sxs-lookup"><span data-stu-id="59896-110">**Billing and Pricing**</span></span> | <span data-ttu-id="59896-111">2053736</span><span class="sxs-lookup"><span data-stu-id="59896-111">2053736</span></span> | <span data-ttu-id="59896-112">請求書明細行の詳細には、**請求書** > **関連情報** に移動することでアクセスできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="59896-112">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="59896-113">**請求と価格**</span><span class="sxs-lookup"><span data-stu-id="59896-113">**Billing and Pricing**</span></span> | <span data-ttu-id="59896-114">2122613</span><span class="sxs-lookup"><span data-stu-id="59896-114">2122613</span></span> | <span data-ttu-id="59896-115">**アクティブ化** と **非アクティブ化** アクションが、**価格表** 関連付けエンティティから削除されました。</span><span class="sxs-lookup"><span data-stu-id="59896-115">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="59896-116">**請求と価格**</span><span class="sxs-lookup"><span data-stu-id="59896-116">**Billing and Pricing**</span></span> | <span data-ttu-id="59896-117">2128606</span><span class="sxs-lookup"><span data-stu-id="59896-117">2128606</span></span> | <span data-ttu-id="59896-118">**GetEstimatesForProject** プラグインの **ullReferenceException** の問題を解決しました。</span><span class="sxs-lookup"><span data-stu-id="59896-118">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="59896-119">**展開と構成**</span><span class="sxs-lookup"><span data-stu-id="59896-119">**Deployment and configuration**</span></span> | <span data-ttu-id="59896-120">2140569</span><span class="sxs-lookup"><span data-stu-id="59896-120">2140569</span></span> | <span data-ttu-id="59896-121">Dataverse Teams 環境にプロジェクト ソリューションをインストールしてはいけません。</span><span class="sxs-lookup"><span data-stu-id="59896-121">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="59896-122">**展開と構成**</span><span class="sxs-lookup"><span data-stu-id="59896-122">**Deployment and configuration**</span></span> | <span data-ttu-id="59896-123">2086991</span><span class="sxs-lookup"><span data-stu-id="59896-123">2086991</span></span> | <span data-ttu-id="59896-124">Web リソースのローカリゼーションのカスタマイズが制限されました。</span><span class="sxs-lookup"><span data-stu-id="59896-124">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="59896-125">**営業案件管理**</span><span class="sxs-lookup"><span data-stu-id="59896-125">**Opportunity Management**</span></span> | <span data-ttu-id="59896-126">2136794</span><span class="sxs-lookup"><span data-stu-id="59896-126">2136794</span></span> | <span data-ttu-id="59896-127">**請求書の確認** または **請求書を支払済みとマーク** プロセスが失敗したときに、正しいエラーメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="59896-127">Display correct error message when **Confirm invoice** or **Mark invoice as paid** process fails,</span></span> |
| <span data-ttu-id="59896-128">**営業案件管理**</span><span class="sxs-lookup"><span data-stu-id="59896-128">**Opportunity Management**</span></span> | <span data-ttu-id="59896-129">2146376</span><span class="sxs-lookup"><span data-stu-id="59896-129">2146376</span></span> | <span data-ttu-id="59896-130">請求対象外の実績の修正済み税額が、請求書確認から作成されます。</span><span class="sxs-lookup"><span data-stu-id="59896-130">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="59896-131">**プロジェクトの計画と追跡**</span><span class="sxs-lookup"><span data-stu-id="59896-131">**Project Planning and Tracking**</span></span> | <span data-ttu-id="59896-132">2099879</span><span class="sxs-lookup"><span data-stu-id="59896-132">2099879</span></span> | <span data-ttu-id="59896-133">Dataverse 環境展開では、静的 ID を使用して既定のトランザクションカテゴリを作成する必要があり、環境ごとにランダムに生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="59896-133">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="59896-134">**プロジェクトの計画と追跡**</span><span class="sxs-lookup"><span data-stu-id="59896-134">**Project Planning and Tracking**</span></span> | <span data-ttu-id="59896-135">2128577</span><span class="sxs-lookup"><span data-stu-id="59896-135">2128577</span></span> | <span data-ttu-id="59896-136">リソース割り当てのトランザクション カテゴリを更新するための Project service ユーザー権限を修正しました。</span><span class="sxs-lookup"><span data-stu-id="59896-136">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="59896-137">**プロジェクトの計画と追跡**</span><span class="sxs-lookup"><span data-stu-id="59896-137">**Project Planning and Tracking**</span></span> | <span data-ttu-id="59896-138">2164035</span><span class="sxs-lookup"><span data-stu-id="59896-138">2164035</span></span> | <span data-ttu-id="59896-139">**プロジェクトのコピー** 関数の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="59896-139">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="59896-140">**時間エントリ**</span><span class="sxs-lookup"><span data-stu-id="59896-140">**Time entry**</span></span> | <span data-ttu-id="59896-141">2129161</span><span class="sxs-lookup"><span data-stu-id="59896-141">2129161</span></span> | <span data-ttu-id="59896-142">送信または承認された時間エントリをユーザーが変更および更新できないようにするために、より厳しい制限が適用されました。</span><span class="sxs-lookup"><span data-stu-id="59896-142">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="59896-143">**時間エントリ**</span><span class="sxs-lookup"><span data-stu-id="59896-143">**Time entry**</span></span> | <span data-ttu-id="59896-144">2103572</span><span class="sxs-lookup"><span data-stu-id="59896-144">2103572</span></span> | <span data-ttu-id="59896-145">プロジェクト以外の時間エントリの時間承認で、プロジェクト承認者のロールを探さなくなりました。</span><span class="sxs-lookup"><span data-stu-id="59896-145">Time approval for non-project time entries must not be looking for project approver role.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]