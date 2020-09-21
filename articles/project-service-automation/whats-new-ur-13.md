---
title: Project Service Automation バージョン 13、V3 更新プログラム の最新情報
description: このトピックでは、Project Service Automation バージョン 13、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752855"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="b9e11-103">Project Service Automation V3 、更新プログラム 13 の最新情報</span><span class="sxs-lookup"><span data-stu-id="b9e11-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="b9e11-104">Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。</span><span class="sxs-lookup"><span data-stu-id="b9e11-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b9e11-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9e11-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b9e11-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="b9e11-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b9e11-107">このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="b9e11-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b9e11-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9e11-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b9e11-109">このトピックには、Project Service Automation V3 更新プログラム 13 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="b9e11-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="b9e11-110">このバージョンのビルド番号は V3.10.3.18 であり、次のスケジュールで入手できます:</span><span class="sxs-lookup"><span data-stu-id="b9e11-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="b9e11-111">**一般的な入手（自己プログラム アップデート）：** 2019年11月</span><span class="sxs-lookup"><span data-stu-id="b9e11-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="b9e11-112">**自動更新:** 2019年12月</span><span class="sxs-lookup"><span data-stu-id="b9e11-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="b9e11-113">更新プログラム 13</span><span class="sxs-lookup"><span data-stu-id="b9e11-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="b9e11-114">バグ修正</span><span class="sxs-lookup"><span data-stu-id="b9e11-114">Bug fixes</span></span>

- <span data-ttu-id="b9e11-115">時間と経費</span><span class="sxs-lookup"><span data-stu-id="b9e11-115">Time and Expense</span></span>

     - <span data-ttu-id="b9e11-116">修正：**経費の承認**ページの検索機能が経費の検索として機能しない。</span><span class="sxs-lookup"><span data-stu-id="b9e11-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="b9e11-117">リソース管理</span><span class="sxs-lookup"><span data-stu-id="b9e11-117">Resource Management</span></span>

     - <span data-ttu-id="b9e11-118">修正：調整の数値が右揃えに更新されています。</span><span class="sxs-lookup"><span data-stu-id="b9e11-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="b9e11-119">修正：名前付きのリソースを、 **スケジュール** タブを介して割り当てできない。</span><span class="sxs-lookup"><span data-stu-id="b9e11-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="b9e11-120">プロジェクト管理</span><span class="sxs-lookup"><span data-stu-id="b9e11-120">Project Management</span></span>

     - <span data-ttu-id="b9e11-121">**TransactionType** が **単位** と **DefaultGroup** に対して未入力の場合に、チーム メンバーを割り当てするとNULL参照例外が発生する。</span><span class="sxs-lookup"><span data-stu-id="b9e11-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="b9e11-122">Sales</span><span class="sxs-lookup"><span data-stu-id="b9e11-122">Sales</span></span>

     - <span data-ttu-id="b9e11-123">修正：重複する取引タイプのレコードが、ロール価格レコードの作成時にエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="b9e11-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="b9e11-124">修正：追加のボタン **新規営業案件**、 **見積もり**、 **注文明細**、 **製品の追加** に新たなボタンが追加され、営業案件、見積もり、製品受注、プロジェクト ベースのラインのサブグリッド で表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9e11-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


