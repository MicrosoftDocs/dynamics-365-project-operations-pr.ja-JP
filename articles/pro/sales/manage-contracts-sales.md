---
title: プロジェクト契約の管理
description: このトピックでは、プロジェクトベースの契約書の閲覧に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177337"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="7ab63-103">プロジェクト契約の管理</span><span class="sxs-lookup"><span data-stu-id="7ab63-103">Manage project contracts</span></span>

<span data-ttu-id="7ab63-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="7ab63-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7ab63-105">Dynamics 365 Project Operations のプロジェクト契約は、契約で合意されたプロジェクトのコミットメントと請求の詳細を取得して管理します。</span><span class="sxs-lookup"><span data-stu-id="7ab63-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="7ab63-106">プロジェクト運用におけるプロジェクト契約の構造は、次のコンポーネントを使用したプロジェクト ベースの作業に合わせて調整されています。</span><span class="sxs-lookup"><span data-stu-id="7ab63-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="7ab63-107">プロジェクトの請求書に高レベルのコンポーネントとして表示される作業の個別のコンポーネントを識別する契約品目です。</span><span class="sxs-lookup"><span data-stu-id="7ab63-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="7ab63-108">各高レベルのコンポーネント、または契約品目の作業を識別し、見積もりをする契約品目の詳細です。</span><span class="sxs-lookup"><span data-stu-id="7ab63-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="7ab63-109">見積もりには、契約品目に関連付けられた作業のスケジュールと財務面が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ab63-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="7ab63-110">契約モデルと課金対象コンポーネントは、各契約品目と契約全体の請求契約を保持する各契約品目に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7ab63-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="7ab63-111">プロジェクトベースの契約をすべて表示する</span><span class="sxs-lookup"><span data-stu-id="7ab63-111">View all project-based contracts</span></span>

<span data-ttu-id="7ab63-112">すべてのプロジェクト契約のリストは、**契約** リストページにあります。</span><span class="sxs-lookup"><span data-stu-id="7ab63-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="7ab63-113">**営業** > **取引先担当者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7ab63-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="7ab63-114">システム内のすべてのプロジェクト契約のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ab63-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="7ab63-115">**ビュースイッチャー**(ビュー名称の横にあるドロップダウン アロー)を選択し、他のフィルターされたビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ab63-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="7ab63-116">カスタム フィルター条件を使用して独自のビューを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7ab63-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="7ab63-117">契約は、このリストページまたは詳細ページから作成、削除できます。</span><span class="sxs-lookup"><span data-stu-id="7ab63-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
