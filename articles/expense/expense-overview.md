---
title: 経費の概要
description: このトピックでは、Project Operations での経費機能に関する情報を提供します。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967372"
---
# <a name="expense-home-page"></a><span data-ttu-id="46f17-103">経費ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="46f17-103">Expense home page</span></span>

<span data-ttu-id="46f17-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="46f17-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="46f17-105">Dynamics 365 Project Operations は、経費を処理する機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="46f17-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="46f17-106">経費処理は、ポリシー、トランザクション カテゴリ、および承認のカスタマイズ可能なワークフローを使用して、プロジェクトの有無にかかわらず発生します。</span><span class="sxs-lookup"><span data-stu-id="46f17-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="46f17-107">Project Operations では、経費に対して 2 つのサポートされている展開モデルがあります。</span><span class="sxs-lookup"><span data-stu-id="46f17-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="46f17-108">**完全**: 完全展開は、**リソース/非在庫ベースのシナリオ向け Project Operations** および**製造オーダーに基づくシナリオ向け Project Operations** 用に利用できます。</span><span class="sxs-lookup"><span data-stu-id="46f17-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="46f17-109">**基本**: 基本展開は**リソース/非在庫ベースのシナリオ向け Project Operations** および**ライト展開 – 見積もり請求の取引**用に利用できます。</span><span class="sxs-lookup"><span data-stu-id="46f17-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="46f17-110">すべて</span><span class="sxs-lookup"><span data-stu-id="46f17-110">Full</span></span> 
<span data-ttu-id="46f17-111">完全経費の展開は、次のような、ポリシーを作成する機能を含む完全なポリシーの実施を提供します。</span><span class="sxs-lookup"><span data-stu-id="46f17-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="46f17-112">経費カテゴリの制限</span><span class="sxs-lookup"><span data-stu-id="46f17-112">Expense category limits</span></span>
  - <span data-ttu-id="46f17-113">移動</span><span class="sxs-lookup"><span data-stu-id="46f17-113">Travel</span></span>
  - <span data-ttu-id="46f17-114">日当</span><span class="sxs-lookup"><span data-stu-id="46f17-114">Per diem</span></span>
  - <span data-ttu-id="46f17-115">クレジット カードのインポート</span><span class="sxs-lookup"><span data-stu-id="46f17-115">Credit card imports</span></span>
  - <span data-ttu-id="46f17-116">領収書の光学式文字認識</span><span class="sxs-lookup"><span data-stu-id="46f17-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="46f17-117">Basic</span><span class="sxs-lookup"><span data-stu-id="46f17-117">Basic</span></span> 
<span data-ttu-id="46f17-118">基本経費の展開シナリオでは、プロジェクトに対する基本経費のみを記録できます。</span><span class="sxs-lookup"><span data-stu-id="46f17-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="46f17-119">詳細については、[経費の入力 (ライト)](basic-expense.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="46f17-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="46f17-120">経費の展開を決定する</span><span class="sxs-lookup"><span data-stu-id="46f17-120">Determine your Expense deployment</span></span>
<span data-ttu-id="46f17-121">基本経費の管理展開を実行しているかどうかを決定するには、アドレス URL が **.crm.dynamics.com** で終わることを確認します。</span><span class="sxs-lookup"><span data-stu-id="46f17-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
