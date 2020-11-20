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
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177832"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="43f73-103">プロジェクト見積もりの管理</span><span class="sxs-lookup"><span data-stu-id="43f73-103">Manage project quotes</span></span>

<span data-ttu-id="43f73-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="43f73-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="43f73-105">Dynamics 365 Project Operations では、プロジェクトの見積もりは、プロジェクト作業の提案を作成を簡易化する意図で設計されています。</span><span class="sxs-lookup"><span data-stu-id="43f73-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="43f73-106">Project Operations におけるプロジェクト見積もりの構造は、以下のようなコンポーネントを使用したプロジェクト提案の構造となっています。</span><span class="sxs-lookup"><span data-stu-id="43f73-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="43f73-107">プロジェクトの請求書に高レベルのコンポーネントとして表示される作業の個別のコンポーネントを識別する見積もり品目です。</span><span class="sxs-lookup"><span data-stu-id="43f73-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="43f73-108">高レベルのコンポーネント、または見積品目ごとに作業内容を特定して見積もる見積ラインの詳細です。</span><span class="sxs-lookup"><span data-stu-id="43f73-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="43f73-109">スケジュールや日付の見積もりと作業のための財務的な側面は、その見積もり品目に結び付けられています。</span><span class="sxs-lookup"><span data-stu-id="43f73-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="43f73-110">契約モデルと有料コンポーネントは、見積もり品目ごとに設定されます。</span><span class="sxs-lookup"><span data-stu-id="43f73-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="43f73-111">この設定をすることで、各見積品目の収益、費用、利益のスプレッドと見積書全体の見積もりを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="43f73-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="43f73-112">プロジェクトベースの見積をすべて表示する</span><span class="sxs-lookup"><span data-stu-id="43f73-112">View all project-based quotes</span></span>

<span data-ttu-id="43f73-113">すべてのプロジェクトの **見積もり** の一覧は、見積つもり一覧のページから確認できます。</span><span class="sxs-lookup"><span data-stu-id="43f73-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="43f73-114">**営業** > **見積もり** に移動します。</span><span class="sxs-lookup"><span data-stu-id="43f73-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="43f73-115">システム内のすべてのプロジェクト見積もりの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="43f73-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="43f73-116">**ビュー スイッチャー** を使用して、フィルター処理された見積もりを選択します。</span><span class="sxs-lookup"><span data-stu-id="43f73-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="43f73-117">カスタム フィルター条件を使用して、独自のビューとナビゲーション オプションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="43f73-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="43f73-118">見積もりは、この一覧ページや詳細のページから作成、削除できます。</span><span class="sxs-lookup"><span data-stu-id="43f73-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
