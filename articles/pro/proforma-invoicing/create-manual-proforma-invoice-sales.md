---
title: 見積送り状を手動で作成する
description: このトピックでは、Project Operations で見積送り状を手動で作成する方法について解説します。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079497"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="8b0ed-103">見積送り状を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="8b0ed-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="8b0ed-104">_**適用対象:** ライト展開 - 見積もり請求の取引_</span><span class="sxs-lookup"><span data-stu-id="8b0ed-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b0ed-105">Dynamics 365 Project Operations では、見積送り状を必要に応じて手動で作成できます。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="8b0ed-106">**プロジェクト契約** 一覧ページまたは **プロジェクト契約** の詳細ページから、手動で見積送り状を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="8b0ed-107">プロジェクト契約の価格表</span><span class="sxs-lookup"><span data-stu-id="8b0ed-107">Project Contracts list page</span></span>

<span data-ttu-id="8b0ed-108">**プロジェクト契約** リストページで、1つ以上のプロジェクト契約を選択し、選択したすべてのレコードの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="8b0ed-109">システムは、選択されたプロジェクト契約のうち、今日の日付よりも前の日付の **請求書の発行準備完了** のバックログがあるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="8b0ed-110">これらの契約から、システムは見積送り状のドラフト版を作成します。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="8b0ed-111">プロジェクト契約に複数の顧客がいる場合、顧客ごとに 1 つの請求書が作成され、プロジェクト契約ごとに複数の請求書が作成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="8b0ed-112">作成されたプロジェクトの請求書はすべて、 **営業** エリアの **請求** のセクション内の **請求書** ページに掲載されています。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="8b0ed-113">プロジェクト契約詳細ページ</span><span class="sxs-lookup"><span data-stu-id="8b0ed-113">Project Contract details page</span></span>

<span data-ttu-id="8b0ed-114">見積送り状は、 **プロジェクト契約** の詳細ページからも作成することができ、その特定のプロジェクト契約の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="8b0ed-115">システムは、プロジェクト契約に今日の日付よりも前の日付の **請求書の発行準備完了** のバックログがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="8b0ed-116">これらの契約から、各契約ラインの顧客数に応じた見積送り状のドラフト版を作成します。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="8b0ed-117">ひとつの見積送り状が作成されると、 **請求書** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="8b0ed-118">そのプロジェクト契約に複数の請求書が作成されている場合、 **請求書** の一覧ページが開き、作成されたすべての請求書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b0ed-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
