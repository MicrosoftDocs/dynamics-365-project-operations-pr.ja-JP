---
title: 手動で見積送り状を作成する (ライト)
description: このトピックでは、Project Operations で見積送り状を手動で作成する方法について解説します。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274194"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="172eb-103">手動で見積送り状を作成する (ライト)</span><span class="sxs-lookup"><span data-stu-id="172eb-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="172eb-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="172eb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="172eb-105">Dynamics 365 Project Operations では、必要に応じて見積送り状を手動で作成できます。</span><span class="sxs-lookup"><span data-stu-id="172eb-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="172eb-106">**プロジェクト契約** 一覧ページまたは **プロジェクト契約** の詳細ページから、手動で見積送り状を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="172eb-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="172eb-107">プロジェクト契約の価格表</span><span class="sxs-lookup"><span data-stu-id="172eb-107">Project Contracts list page</span></span>

<span data-ttu-id="172eb-108">**プロジェクト契約** リストページで、1つ以上のプロジェクト契約を選択し、選択したすべてのレコードの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="172eb-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="172eb-109">システムは、選択されたプロジェクト契約のうち、今日の日付よりも前の日付の **請求書の発行準備完了** のバックログがあるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="172eb-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="172eb-110">これらの契約から、システムは見積送り状のドラフト版を作成します。</span><span class="sxs-lookup"><span data-stu-id="172eb-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="172eb-111">プロジェクト契約に複数の顧客がいる場合、顧客ごとに 1 つの請求書が作成され、プロジェクト契約ごとに複数の請求書が作成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="172eb-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="172eb-112">作成されたプロジェクトの請求書はすべて、**営業** エリアの **請求** のセクション内の **請求書** ページに掲載されています。</span><span class="sxs-lookup"><span data-stu-id="172eb-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="172eb-113">[プロジェクト契約の詳細] ページ</span><span class="sxs-lookup"><span data-stu-id="172eb-113">Project Contract details page</span></span>

<span data-ttu-id="172eb-114">見積送り状は、**プロジェクト契約** 詳細ページからも作成できます。</span><span class="sxs-lookup"><span data-stu-id="172eb-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="172eb-115">システムによって、プロジェクト契約に今日の日付より前の日付の **請求準備完了** バックログがあることが確認されます。</span><span class="sxs-lookup"><span data-stu-id="172eb-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="172eb-116">それらの契約から、システムによって各契約品目の顧客の数に基づいてドラフトの見積送り状が作成されます。</span><span class="sxs-lookup"><span data-stu-id="172eb-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="172eb-117">ひとつの見積送り状が作成されると、**請求書** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="172eb-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="172eb-118">そのプロジェクト契約に対して複数の見積送り状が作成された場合、**請求書** リスト ページが開き、作成されたすべての見積送り状が表示されます。</span><span class="sxs-lookup"><span data-stu-id="172eb-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]