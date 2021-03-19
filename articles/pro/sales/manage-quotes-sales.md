---
title: プロジェクト見積もりの管理
description: このトピックでは、プロジェクトの見積もりについて説明します。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272934"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="68953-103">プロジェクト見積もりの管理</span><span class="sxs-lookup"><span data-stu-id="68953-103">Manage project quotes</span></span>

<span data-ttu-id="68953-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="68953-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="68953-105">Dynamics 365 Project Operations では、プロジェクト見積が、プロジェクト作業の提案を構築するのに役立つように設計されています。</span><span class="sxs-lookup"><span data-stu-id="68953-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="68953-106">Project Operations のプロジェクト見積の構造は、次のコンポーネントを含むプロジェクト提案のために構成されています。</span><span class="sxs-lookup"><span data-stu-id="68953-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="68953-107">上位レベルのコンポーネントとして表示される作業の個別のコンポーネントを識別する見積明細行。</span><span class="sxs-lookup"><span data-stu-id="68953-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="68953-108">各上位レベルのコンポーネントまたは見積明細行の作業を識別して見積もる見積明細行の詳細。</span><span class="sxs-lookup"><span data-stu-id="68953-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="68953-109">作業のスケジュールまたは日付見積、および財務的な側面は、その見積明細行に関連づけられています。</span><span class="sxs-lookup"><span data-stu-id="68953-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="68953-110">契約モデルと課金可能コンポーネントは、見積明細行ごとに設定されます。</span><span class="sxs-lookup"><span data-stu-id="68953-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="68953-111">この設定をすることで、各見積品目の収益、費用、利益のスプレッドと見積書全体の見積もりを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="68953-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="68953-112">プロジェクトベースの見積をすべて表示する</span><span class="sxs-lookup"><span data-stu-id="68953-112">View all project-based quotes</span></span>

<span data-ttu-id="68953-113">すべてのプロジェクトの **見積もり** の一覧は、見積つもり一覧のページから確認できます。</span><span class="sxs-lookup"><span data-stu-id="68953-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="68953-114">**営業** > **見積もり** に移動します。</span><span class="sxs-lookup"><span data-stu-id="68953-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="68953-115">システム内のすべてのプロジェクト見積もりの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="68953-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="68953-116">**ビュー スイッチャー** を使用して、フィルター処理された見積もりを選択します。</span><span class="sxs-lookup"><span data-stu-id="68953-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="68953-117">カスタム フィルター条件を使用して、独自のビューとナビゲーション オプションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="68953-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="68953-118">見積もりは、この一覧ページや詳細のページから作成、削除できます。</span><span class="sxs-lookup"><span data-stu-id="68953-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]