---
title: 経費の概要
description: このトピックでは、Project Operations での経費機能に関する情報を提供します。
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 921df6fa8f1eb33bd01792c0b7c787fc74604adf
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368572"
---
# <a name="expense-home-page"></a><span data-ttu-id="2f5d3-103">経費ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="2f5d3-103">Expense home page</span></span>

<span data-ttu-id="2f5d3-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="2f5d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2f5d3-105">Dynamics 365 Project Operations は、経費を処理する機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="2f5d3-106">経費処理は、ポリシー、トランザクション カテゴリ、および承認のカスタマイズ可能なワークフローを使用し、プロジェクトに関連して、またはプロジェクトに関連せず発生します。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="2f5d3-107">Project Operations では、経費に対して 2 つのサポートされている展開モデルがあります。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="2f5d3-108">**完全**: 完全展開は、**リソース/非在庫ベースのシナリオ向け Project Operations** および **製造オーダーに基づくシナリオ向け Project Operations** に利用できます。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="2f5d3-109">**基本**: 基本展開は **リソース/非在庫ベースのシナリオ向け Project Operations** および **ライト展開 – 見積もり請求の取引** 用に利用できます。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="2f5d3-110">すべて</span><span class="sxs-lookup"><span data-stu-id="2f5d3-110">Full</span></span> 
<span data-ttu-id="2f5d3-111">全経費展開は、次のようなポリシーを作成する機能を含む完全なポリシーの適用機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="2f5d3-112">経費カテゴリの制限</span><span class="sxs-lookup"><span data-stu-id="2f5d3-112">Expense category limits</span></span>
  - <span data-ttu-id="2f5d3-113">出張</span><span class="sxs-lookup"><span data-stu-id="2f5d3-113">Travel</span></span>
  - <span data-ttu-id="2f5d3-114">日当</span><span class="sxs-lookup"><span data-stu-id="2f5d3-114">Per diem</span></span>
  - <span data-ttu-id="2f5d3-115">クレジット カードのインポート</span><span class="sxs-lookup"><span data-stu-id="2f5d3-115">Credit card imports</span></span>
  - <span data-ttu-id="2f5d3-116">領収書の光学式文字認識</span><span class="sxs-lookup"><span data-stu-id="2f5d3-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="2f5d3-117">Basic</span><span class="sxs-lookup"><span data-stu-id="2f5d3-117">Basic</span></span> 
<span data-ttu-id="2f5d3-118">基本経費の展開シナリオでは、プロジェクトに対する基本経費のみを記録できます。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="2f5d3-119">詳細については、[経費の入力 (ライト)](basic-expense.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="2f5d3-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="2f5d3-120">経費の展開を決定する</span><span class="sxs-lookup"><span data-stu-id="2f5d3-120">Determine your Expense deployment</span></span>
<span data-ttu-id="2f5d3-121">基本経費の管理展開を実行しているかどうかを決定するには、アドレス URL が **.crm.dynamics.com** で終わることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f5d3-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]