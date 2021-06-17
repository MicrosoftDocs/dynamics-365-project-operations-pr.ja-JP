---
title: スケジュール ボードを使用してプロジェクト リソースを予約する
description: このトピックでは、リソースの予約方法について説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bbd6e8c711f6c15221143514efdd43a388ef4e7f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998057"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="49927-103">スケジュール ボードを使用してプロジェクト リソースを予約する</span><span class="sxs-lookup"><span data-stu-id="49927-103">Use the Schedule Board to book project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="49927-104">プロジェクト内からのプロジェクト リソースの予約に加え、スケジュール ボードからリソースを本予約または仮予約することができます。</span><span class="sxs-lookup"><span data-stu-id="49927-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="49927-105">スケジュール ボードから予約する前に、リソース要件を作成するか、生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49927-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="49927-106">スケジュール ボードからリソース要件を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="49927-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="49927-107">ページ下部にある **予約の要件** ウィンドウが畳まれている場合は、拡張コントロールを選択して拡張します。</span><span class="sxs-lookup"><span data-stu-id="49927-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="49927-108">**予約の要件** ウィンドウで、**プロジェクト** タブで、予約する要件を選択します。</span><span class="sxs-lookup"><span data-stu-id="49927-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![プロジェクト タブで選択された要件](media/Resource-Management-image73.png)

3. <span data-ttu-id="49927-110">予約可能リソースをフィルター処理し、使用可能なリソースを表示するには、**使用可能性の検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49927-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="49927-111">スケジュール ボードから 1 つまたは複数のリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="49927-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="49927-112">ページの右側の **リソース予約の作成** ウィンドウで、予約情報を入力し、**予約して終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49927-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![選択した予約可能リソースのリソース予約ウィンドウの作成](media/Resource-Management-image74.png)

6. <span data-ttu-id="49927-114">要件が **リソース予約の作成** ウィンドウで選択されている間に、1 つまたは複数のリソースのセルを選択して予約を作成します。</span><span class="sxs-lookup"><span data-stu-id="49927-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![リソースに選択された複数セル](media/Resource-Management-image75.png)

7. <span data-ttu-id="49927-116">**予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49927-116">Select **Book**.</span></span>

<span data-ttu-id="49927-117">この要件は、選択されたリソースを使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="49927-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="49927-118">**予約の要件** ウィンドウで、要件が更新され、リソースがプロジェクトで予約済みとして表示されていることに注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="49927-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![プロジェクトで予約されたリソース](media/Resource-Management-image76.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]