---
title: 時間および実費払プロジェクトのプロジェクト受注
description: このトピックでは、時間および実費払プロジェクトのプロジェクト ベースの受注を作成する方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289060"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="e75b2-103">時間および実費払プロジェクトのプロジェクト受注</span><span class="sxs-lookup"><span data-stu-id="e75b2-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e75b2-104">このトピックでは、プロジェクトの受注を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e75b2-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="e75b2-105">受注は、タイプが **時間および実費払** のプロジェクトに対してのみ作成できます。</span><span class="sxs-lookup"><span data-stu-id="e75b2-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="e75b2-106">時間および実費払プロジェクトがプロジェクト契約に複数の資金調達ソースがある場合、**プロジェクト管理および会計パラメーター** ページの **複数の資金調達ソースがあるプロジェクトの受注を許可する** パラメーターを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e75b2-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="e75b2-107">複数の資金調達ソースがあるプロジェクト受注のサポートは、アプリケーション リリース 10.0.2 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e75b2-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="e75b2-108">複数の資金調達ソースを使用してのプロジェクトの受注のサポートを有効にするパラメーターは、2020 年 4 月のリリース ウェーブで削除され、その後、機能は常に有効になります。</span><span class="sxs-lookup"><span data-stu-id="e75b2-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="e75b2-109">プロジェクトベースの受注は、次の 2 つの方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="e75b2-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="e75b2-110">プロジェクト自体に移動します。</span><span class="sxs-lookup"><span data-stu-id="e75b2-110">Go to the project itself.</span></span> <span data-ttu-id="e75b2-111">アクションのウィンドウで、**管理 > 品目のタスク > 受注** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e75b2-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="e75b2-112">プロジェクト情報は、プロジェクトの受注に既定で設定されます。</span><span class="sxs-lookup"><span data-stu-id="e75b2-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="e75b2-113">プロジェクト契約に複数の資金調達ソースがある場合は、受注の顧客を設定する資金調達ソースを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e75b2-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="e75b2-114">プロジェクトの資金調達ソースが 1 つしかない場合、顧客は自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e75b2-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="e75b2-115">**すべての受注** の一覧ページに移動し、新規の受注を作成します。</span><span class="sxs-lookup"><span data-stu-id="e75b2-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="e75b2-116">受注のプロジェクトを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e75b2-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="e75b2-117">プロジェクトが選択されると、顧客は資金調達ソースから設定されるか、またはプロジェクト契約に複数の資金調達ソースがある場合は、資金調達ソースを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e75b2-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]